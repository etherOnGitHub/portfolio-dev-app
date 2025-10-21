# 🧩 Project Setup Guide (Next.js + Tailwind + Prisma)

This guide walks through setting up the project locally, installing dependencies, and configuring VS Code for a smooth workflow.

---

## 🚀 1️⃣ Clone the Repository

```bash
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>
```

Make sure you open this folder in **VS Code** — it should contain `package.json`, `src/`, and `prisma/`.

---

## ⚙️ 2️⃣ Install Dependencies

```bash
npm install
```

Installs everything required to run the app:
- Next.js  
- React / TypeScript  
- Tailwind CSS  
- Prisma ORM  

---

## 🧮 3️⃣ Environment Variables

Create a `.env` file in the project root:

```bash
DATABASE_URL="postgresql://user:password@ep-yourdb-region.aws.neon.tech/neondb?sslmode=require"
```

> 🧠 If you don't have a Neon database, create one free at [neon.tech](https://neon.tech).

---

## 🔧 4️⃣ Prisma Client

Generate the Prisma client and push the schema to your database:

```bash
npx prisma generate
npx prisma db push
```

Optional — open Prisma Studio (visual database viewer):

```bash
npx prisma studio
```

---

## 🎨 5️⃣ Run the Development Server

```bash
npm run dev
```

The app runs at **http://localhost:3000**  
Tailwind updates instantly as you save changes.

---

## 🧱 6️⃣ Build for Production (optional)

```bash
npm run build
npm start
```

---

# 💻 Recommended VS Code Extensions

| Extension | What It Does | Publisher |
|------------|---------------|------------|
| **Prisma** | Syntax highlighting and auto-completion for `.prisma` files | Prisma |
| **Tailwind CSS IntelliSense** | Autocomplete, color previews, and linting for Tailwind classes | Tailwind Labs |
| **ESLint** | Linting aligned with Next.js rules | Microsoft |
| **Prettier – Code Formatter** | Formats code consistently on save | Prettier |
| **Path IntelliSense** | Autocompletes file/folder paths in imports | Christian Kohler |
| **Error Lens** | Shows lint and TypeScript issues inline | Alexander |
| **GitHub Pull Requests and Issues** | Manage PRs/issues inside VS Code | GitHub |
| **Thunder Client / REST Client** | Test your API routes directly from VS Code | Rangav / Huachao Mao |

---

## ⚡ Optional VS Code Tweaks

1. Enable **Format on Save**:  
   - Press `Ctrl + ,` → search for “Format on Save” → enable.  
2. (Optional) Create `.vscode/settings.json`:
   ```json
   {
     "editor.formatOnSave": true,
     "editor.defaultFormatter": "esbenp.prettier-vscode",
     "eslint.validate": ["typescript", "typescriptreact", "javascript", "javascriptreact"]
   }
   ```

---

## ✅ Summary

Once you’ve:
1. Cloned the repo  
2. Installed dependencies  
3. Added `.env`  
4. Generated Prisma client  
5. Run `npm run dev`

You’ll be up and running with a live Next.js + Tailwind + Prisma environment in under five minutes.

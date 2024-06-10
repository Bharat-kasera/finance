<a name="readme-top"></a>

# Track your income and expenses with Finance.

![Track your income and expenses with Finance.](/.github/images/img_main.png "Track your income and expenses with Finance.")

[![Ask Me Anything!](https://flat.badgen.net/static/Ask%20me/anything?icon=github&color=black&scale=1.01)](https://github.com/sanidhyy "Ask Me Anything!")
[![GitHub license](https://flat.badgen.net/github/license/sanidhyy/finance-dashboard?icon=github&color=black&scale=1.01)](https://github.com/sanidhyy/finance-dashboard/blob/main/LICENSE "GitHub license")
[![Maintenance](https://flat.badgen.net/static/Maintained/yes?icon=github&color=black&scale=1.01)](https://github.com/sanidhyy/finance-dashboard/commits/main "Maintenance")
[![GitHub branches](https://flat.badgen.net/github/branches/sanidhyy/finance-dashboard?icon=github&color=black&scale=1.01)](https://github.com/sanidhyy/finance-dashboard/branches "GitHub branches")
[![Github commits](https://flat.badgen.net/github/commits/sanidhyy/finance-dashboard?icon=github&color=black&scale=1.01)](https://github.com/sanidhyy/finance-dashboard/commits "Github commits")
[![GitHub issues](https://flat.badgen.net/github/issues/sanidhyy/finance-dashboard?icon=github&color=black&scale=1.01)](https://github.com/sanidhyy/finance-dashboard/issues "GitHub issues")
[![GitHub pull requests](https://flat.badgen.net/github/prs/sanidhyy/finance-dashboard?icon=github&color=black&scale=1.01)](https://github.com/sanidhyy/finance-dashboard/pulls "GitHub pull requests")
[![Vercel status](https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white)](https://appfinance.vercel.app/ "Vercel status")

<!-- Table of Contents -->
<details>

<summary>

# :notebook_with_decorative_cover: Table of Contents

</summary>

- [Folder Structure](#bangbang-folder-structure)
- [Getting Started](#toolbox-getting-started)
- [Screenshots](#camera-screenshots)
- [Tech Stack](#gear-tech-stack)
- [Stats](#wrench-stats)
- [Contribute](#raised_hands-contribute)
- [Acknowledgements](#gem-acknowledgements)
- [Buy Me a Coffee](#coffee-buy-me-a-coffee)
- [Follow Me](#rocket-follow-me)
- [Learn More](#books-learn-more)
- [Deploy on Vercel](#page_with_curl-deploy-on-vercel)
- [Give A Star](#star-give-a-star)
- [Star History](#star2-star-history)
- [Give A Star](#star-give-a-star)

</details>

## :bangbang: Folder Structure

Here is the folder structure of this app.

```bash
finance-dashboard/
  |- app/
    |-- (auth)/
    |-- (dashboard)/
    |-- api/
    |-- apple-icon.png
    |-- favicon.ico
    |-- globals.css
    |-- icon1.png
    |-- icon2.png
    |-- layout.tsx
  |- components/
    |-- ui/
  |- config/
    |-- index.ts
  |- db/
    |-- drizzle.ts
    |-- schema.ts
  |- drizzle/
  |- features/
    |-- accounts/
    |-- categories/
    |-- summary/
    |-- transactions/
  |- hooks/
    |-- use-confirm.tsx
  |- lib/
    |-- hono.ts
    |-- utils.ts
  |- providers/
    |-- query-provider.tsx
    |-- sheet-provider.tsx
  |- public/
    |-- data.csv
    |-- github.svg
    |-- logo.svg
  |- scripts/
    |-- seed.ts
  |- .env.example
  |- .env.local
  |- .eslintrc.json
  |- .gitignore
  |- .prettierrc
  |- bun.lockb
  |- components.json
  |- drizzle.config.ts
  |- environment.d.ts
  |- middleware.ts
  |- next.config.mjs
  |- package-lock.json
  |- package.json
  |- postcss.config.js
  |- tailwind.config.ts
  |- tsconfig.json
```

<br />

## :toolbox: Getting Started

1. Make sure **Git** and **NodeJS** is installed.
2. Clone this repository to your local computer.
3. Create `.env.local` file in **root** directory.
4. Contents of `.env.local`:

```env
# .env.local

# disabled next.js telemetry
NEXT_TELEMETRY_DISABLED=1

# clerk auth keys
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=pk_test_XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
CLERK_PUBLISHABLE_KEY=pk_test_XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
CLERK_SECRET_KEY=sk_test_XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

# clerk redirect url
NEXT_PUBLIC_CLERK_SIGN_IN_URL=/sign-in
NEXT_PUBLIC_CLERK_SIGN_UP_URL=/sign-up

# neon db url
DATABASE_URL=postgresql://<username>:<password>@<hostname>/<database>?sslmode=require

# app base url
NEXT_PUBLIC_APP_URL=http://localhost:3000

```

5. Obtain Clerk Authentication Keys

   1. **Source**: Clerk Dashboard or Settings Page
   2. **Procedure**:
      - Log in to your Clerk account.
      - Navigate to the dashboard or settings page.
      - Look for the section related to authentication keys.
      - Copy the `NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY` and `CLERK_SECRET_KEY` provided in that section.

6. Retrieve Neon Database URI

   1. **Source**: Database Provider (e.g., Neon, PostgreSQL)
   2. **Procedure**:
      - Access your database provider's platform or configuration.
      - Locate the database connection details.
      - Replace `<username>`, `<password>`, `<hostname>`, and `<database>` placeholders in the URI with your actual database credentials.
      - Ensure to include `?sslmode=require` at the end of the URI for SSL mode requirement.

7. Specify Public App URL

   1. **Procedure**:
      - Replace `http://localhost:3000` with the URL of your deployed application.

8. Save and Secure:

   - Save the changes to the `.env.local` file.

9. Install Project Dependencies using `npm install --legacy-peer-deps` or `yarn install --legacy-peer-deps`.

10. Migrate database:

In terminal, run `npm run db:generate` to generate database client and `npm run db:migrate` to make sure that your database is up-to-date along with schema.

11. Run the Seed Script:

In the same terminal, run the following command to execute the seed script:

```bash
npm run db:seed
```

This command uses `npm` to execute the Typescript file (`scripts/seed.ts`) and writes transaction data in database.

12. Verify Data in Database:

Once the script completes, check your database to ensure that the transaction data has been successfully seeded.

13. Now app is fully configured 👍 and you can start using this app using either one of `npm run dev` or `yarn dev`.

**NOTE:** Please make sure to keep your API keys and configuration values secure and do not expose them publicly.

## :camera: Screenshots

![Modern UI/UX](/.github/images/img1.png "Modern UI/UX")

![Transactions](/.github/images/img2.png "Transactions")

![Accounts](/.github/images/img3.png "Accounts")

## :gear: Tech Stack

[![React JS](https://skillicons.dev/icons?i=react "React JS")](https://react.dev/ "React JS") [![Next JS](https://skillicons.dev/icons?i=next "Next JS")](https://nextjs.org/ "Next JS") [![Typescript](https://skillicons.dev/icons?i=ts "Typescript")](https://www.typescriptlang.org/ "Typescript") [![Tailwind CSS](https://skillicons.dev/icons?i=tailwind "Tailwind CSS")](https://tailwindcss.com/ "Tailwind CSS") [![Vercel](https://skillicons.dev/icons?i=vercel "Vercel")](https://vercel.app/ "Vercel") [![Postgresql](https://skillicons.dev/icons?i=postgres "Postgresql")](https://www.postgresql.org/ "Postgresql")

## :wrench: Stats

[![Stats for Finance](/.github/images/stats.svg "Stats for Finance")](https://pagespeed.web.dev/analysis?url=https://appfinance.vercel.app/ "Stats for Finance")

## :raised_hands: Contribute

You might encounter some bugs while using this app. You are more than welcome to contribute. Just submit changes via pull request and I will review them before merging. Make sure you follow community guidelines.

## :books: Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js/) - your feedback and contributions are welcome!

## :page_with_curl: Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out [Next.js deployment documentation](https://nextjs.org/docs/deployment) for more details.

## :star: Give A Star

You can also give this repository a star to show more people and they can use this repository.

## :star2: Star History

<a href="https://star-history.com/#sanidhyy/finance-dashboard&Timeline">
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/svg?repos=sanidhyy/finance-dashboard&type=Timeline&theme=dark" />
  <source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/svg?repos=sanidhyy/finance-dashboard&type=Timeline" />
  <img alt="Star History Chart" src="https://api.star-history.com/svg?repos=sanidhyy/finance-dashboard&type=Timeline" />
</picture>
</a>

<br />
<p align="right">(<a href="#readme-top">back to top</a>)</p>


# 🖋️ Quill - AI-Powered PDF SaaS

Quill is a modern fullstack SaaS platform that allows users to upload PDF documents and have real-time, context-aware conversations with them. Built with the **Next.js 13.5 App Router**, it leverages RAG (Retrieval-Augmented Generation) to turn static documents into interactive chatbots.

## 🚀 Features

  * **PDF Interaction:** Upload PDFs and ask questions about the content.
  * **RAG Architecture:** Uses Pinecone as a vector database and OpenAI/Azure OpenAI for intelligent document processing.
  * **Authentication:** Secure login and registration powered by **Kinde Auth**.
  * **Streaming Responses:** Real-time AI chat interface using `ai` and `trpc`.
  * **Subscription Model:** Tiered pricing (Free & Pro) integrated with **Stripe**.
  * **Modern UI:** Built with **Tailwind CSS**, **Shadcn UI**, and **Lucide Icons**.
  * **Database:** **Prisma ORM** with MongoDB (or your preferred provider).
  * **File Handling:** Seamless PDF uploads via **UploadThing**.

-----

## 🛠️ Tech Stack

  * **Framework:** Next.js 13.5 (App Router)
  * **Language:** TypeScript
  * **AI SDK:** LangChain, OpenAI, Azure OpenAI
  * **Vector DB:** Pinecone
  * **Database:** Prisma (MongoDB)
  * **Styling:** Tailwind CSS, Radix UI
  * **API Layer:** tRPC, React Query
  * **Payments:** Stripe
  * **Auth:** Kinde

-----

## 📋 Prerequisites

Before you begin, ensure you have the following accounts set up:

  * [Kinde Auth](https://kinde.com/)
  * [OpenAI Platform](https://platform.openai.com/) or Azure OpenAI
  * [Pinecone](https://www.pinecone.io/)
  * [UploadThing](https://uploadthing.com/)
  * [Stripe](https://stripe.com/)
  * [MongoDB Atlas](https://www.mongodb.com/cloud/atlas)

-----

## ⚙️ Environment Variables

Create a `.env` file in the root directory and populate it with your credentials:

```env
# Kinde Auth
KINDE_CLIENT_ID=your_client_id
KINDE_CLIENT_SECRET=your_client_secret
KINDE_ISSUER_URL=your_kinde_url
KINDE_SITE_URL=http://localhost:3000
KINDE_POST_LOGOUT_REDIRECT_URL=http://localhost:3000
KINDE_POST_LOGIN_REDIRECT_URL=http://localhost:3000/dashboard

# Database (Prisma)
DATABASE_URL="mongodb+srv://..."

# UploadThing
UPLOADTHING_SECRET=sk_live_...
UPLOADTHING_APP_ID=...

# OpenAI / Azure OpenAI
OPENAI_API_KEY=sk-...
AZURE_OPENAI_API_KEY=...
AZURE_END_POINT=...
AZURE_API_VERSION=2024-02-15-preview
AZURE_INSTANCE_NAME=...
AZURE_EMBEDDINGS_DEPLOYMENT_NAME=...
AZURE_CHAT_DEPLOYMENT_NAME=...

# Stripe
STRIPE_SECRET_KEY=sk_test_...
STRIPE_WEBHOOK_SECRET=whsec_...

# Pinecone
PINECONE_API_KEY=...
PINECONE_ENVIRONMENT=gcp-starter
```

-----

## 🏗️ Installation & Setup

1.  **Clone the repository:**

    ```bash
    git clone https://github.com/your-username/quill.git
    cd quill
    ```

2.  **Install dependencies:**

    ```bash
    npm install
    ```

3.  **Sync Database Schema:**

    ```bash
    npx prisma generate
    npx prisma db push
    ```

4.  **Run the development server:**

    ```bash
    npm run dev
    ```

Open [http://localhost:3000](https://www.google.com/search?q=http://localhost:3000) with your browser to see the result.

-----

## 🧪 Deployment

This project is optimized for **Vercel**:

1.  Push your code to GitHub.
2.  Import the project into Vercel.
3.  Add all environment variables from your `.env` file to the Vercel project settings.
4.  Configure the **Stripe Webhook** to point to `your-domain.com/api/webhooks/stripe`.

-----

## 📜 Scripts

  * `npm run dev`: Runs the app in development mode.
  * `npm run build`: Creates an optimized production build.
  * `npm run start`: Starts the production server.
  * `npm run lint`: Checks for linting errors.

-----

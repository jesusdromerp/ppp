# Ganado Analytics

Versión profesional basada en el `index.html` entregado: Next.js + TypeScript + Supabase, preparada para Vercel.

## 1. Requisitos

- Node.js 20+
- Una cuenta de Supabase
- Una cuenta de Vercel

## 2. Instalar

```bash
npm install
npm run dev
```

Abre `http://localhost:3000`.

La interfaz funciona con datos de demostración incluso sin Supabase configurado.

## 3. Supabase

1. Crea un proyecto en Supabase.
2. Abre SQL Editor.
3. Ejecuta `supabase/schema.sql`.
4. Copia la URL y la anon key.
5. Duplica `.env.example` como `.env.local` y completa:

```env
NEXT_PUBLIC_SUPABASE_URL=https://TU-PROYECTO.supabase.co
NEXT_PUBLIC_SUPABASE_ANON_KEY=TU_ANON_KEY
```

## 4. Vercel

Sube el proyecto a GitHub y en Vercel selecciona **Import Project**.

Agrega las mismas dos variables de entorno en:

**Project Settings → Environment Variables**

Después despliega.

## 5. Estructura

- `app/` — páginas y estilos globales.
- `components/Dashboard.tsx` — interfaz principal y módulos.
- `lib/supabase.ts` — cliente Supabase.
- `lib/demo-data.ts` — datos iniciales de demostración.
- `types/` — tipos TypeScript.
- `supabase/schema.sql` — base de datos.

## 6. Siguiente etapa recomendada

Esta versión conserva la lógica y módulos del HTML original, pero el siguiente paso es conectar cada formulario y tabla al CRUD de Supabase y agregar autenticación por usuario/finca, almacenamiento de fotos y permisos por rol.

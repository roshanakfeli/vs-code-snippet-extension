# RQ Hooks

A VS Code extension providing helpful code snippets for quickly generating standard React Query (`@tanstack/react-query`) custom hooks. This helps maintain consistency and speeds up development.

## Features

This extension currently includes snippets for:

- **Standard Data-Fetching Hook (`useQuery`)**
- **Standard Data-Mutation Hook (`useMutation`)**

## How to Use

1. Ensure this extension ("RQ Hooks") is installed in your VS Code.
2. Open a `.tsx` or `.ts` file where you want to create a new hook.
3. Type one of the **prefixes** listed below for the desired snippet.
4. VS Code's IntelliSense will suggest the snippet. Select it and press `Enter` or `Tab`.
5. The snippet code will be inserted automatically.
6. Use the `Tab` key to jump between placeholders and fill in the required values for your specific API.

## Available Snippets

| Name                | Prefixes                    | Description                                       |
| ------------------- | --------------------------- | ------------------------------------------------- |
| React Query Hook    | `rqh`, `useQuerySnippet`    | Generates a `useQuery` hook for data fetching.    |
| React Mutation Hook | `rqm`, `useMutationSnippet` | Generates a `useMutation` hook for data mutation. |

---

### 1. React Query Hook

- **Prefixes:** `rqh`, `useQuerySnippet`
- **Description:** Creates a comprehensive `useQuery` hook for fetching data from an API using standard structure.
- **Placeholders to fill:**
  - `HookIdentifier`: Your custom hook’s base name (e.g., `AdminHospitalLog`)
  - `FeatureNameParams`: The type for API parameters (e.g., `LogHospitalExpenseParams`)
  - `FeatureNameResponse`: The type for the API response (e.g., `HospitalLogExpenseResponse`)
  - `QUERY_KEY_CONST`: React Query cache key constant (e.g., `ADMIN_HOSPITAL_EXPENSE_LOG`)
  - `apiCategory`: The API service category (e.g., `common`, `expense`)
  - `apiFunctionName`: The actual API method name (e.g., `getAdminHospitalExpenseLog`)

---

### 2. React Mutation Hook

- **Prefixes:** `rqm`, `useMutationSnippet`
- **Description:** Creates a reusable `useMutation` hook for submitting data via API (create/update/delete).
- **Placeholders to fill:**
  - `HookIdentifier`: Your custom hook’s base name (e.g., `AddHospitalExpense`)
  - `FeatureNameParams`: The type for API input params (e.g., `AddHospitalExpenseParams`)
  - `FeatureNameResponse`: The type for API response (e.g., `AddHospitalExpenseResponse`)
  - `apiCategory`: The API service category (e.g., `hospital`)
  - `apiFunctionName`: The actual API method name (e.g., `addHospitalExpense`)

---

## Important Notes

### ✅ Verify Import Paths

The snippets assume standard project folder structure. You may need to adjust paths to match your actual file organization:

```ts
import { APIs } from "services/APIs";
import { APIError, ReactQuerySideEffectTypes } from "models/APImodels";
import { FeatureNameParams, FeatureNameResponse } from "services/models";
```

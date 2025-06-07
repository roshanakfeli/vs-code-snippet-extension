# Sanaap RQ Hooks

A VS Code extension providing helpful code snippets for quickly generating standard React Query (`@tanstack/react-query`) custom hooks used in Sanaap projects. This helps maintain consistency and speeds up development.

## Features

This extension currently includes snippets for:

- **Standard Data-Fetching Hook (`useQuery`)**
- **Standard Data-Mutation Hook (`useMutation`)**

## How to Use

1.  Ensure this extension ("Sanaap RQ Hooks") is installed in your VS Code.
2.  Open a `.tsx` or `.ts` file where you want to create a new hook.
3.  Type one of the **prefixes** listed below for the desired snippet.
4.  VS Code's IntelliSense will suggest the snippet. Select it and press `Enter` or `Tab`.
5.  The snippet code will be inserted.
6.  Use the `Tab` key to jump between placeholders and fill in the required information for your specific hook.

## Available Snippets

### 1. Sanaap React Query Hook (Detailed)

- **Prefixes:** `rqhs`, `useQuerySanaap`
- **Description:** Creates a comprehensive `useQuery` hook structure for fetching data.
- **Placeholders to fill:**
  - `HookIdentifier`: The base name for your hook (e.g., `AdminHospitalLog`).
  - `FeatureNameParams`: The name of your Params type (e.g., `LogHospitalExpenseParams`).
  - `FeatureNameResponse`: The name of your Response type (e.g., `HospitalLogExpenseResponse`).
  - `QUERY_KEY_CONST`: The constant name for your React Query key (e.g., `ADMIN_HOSPITAL_EXPENSE_LOG`).
  - `apiCategory`: The category under `APIs` (e.g., `common`, `expense`).
  - `apiFunctionName`: The actual API function name (e.g., `getAdminHospitalExpenseLog`).

### 2. Sanaap React Mutation Hook

- **Prefixes:** `rqms`, `useMutationSanaap`
- **Description:** Creates a standard `useMutation` hook structure for creating, updating, or deleting data.
- **Placeholders to fill:**
  - `HookIdentifier`: The base name for your hook (e.g., `AddHospitalExpense`).
  - `FeatureNameParams`: The name of your Params type (e.g., `AddHospitalExpenseParams`).
  - `FeatureNameResponse`: The name of your Response type (e.g., `AddHospitalExpenseResponse`).
  - `apiCategory`: The category under `APIs` (e.g., `hospital`, `common`).
  - `apiFunctionName`: The actual API function name (e.g., `addHospitalExpense`).

## Important Notes & Configuration

**Verify Import Paths:**

The snippets include default import paths like:

```typescript
import { APIs } from "services/APIs";
import { APIError, ReactQuerySideEffectTypes } from "models/APImodels";
```

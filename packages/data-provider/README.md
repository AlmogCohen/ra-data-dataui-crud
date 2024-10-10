# Nest.js API Data Provider For React-Admin

fork of [ra-data-nestjsx-crud](https://github.com/rayman1104/ra-data-nestjsx-crud) which works with [@nestjsx/crud](https://github.com/nestjsx/crud) plugin which seems to be discontinued.

```ra-data-dataui-crud``` is a data-provider for [react-admin](https://github.com/marmelab/react-admin), that has been designed to make easier communication between a frontend application built with [react-admin](https://github.com/marmelab/react-admin),
and a backend application built with [nestjs](https://github.com/nestjs/nest) framework and [@dataui/crud](https://github.com/gid-oss/dataui-nestjs-crud).

## Install

Using **npm**:
```npm i ra-data-dataui-crud```

Using **yarn**:
```yarn add ra-data-dataui-crud```

## Usage

```jsx
"use client"; // remove this line if you choose Pages Router
import { Admin, Resource, ListGuesser, EditGuesser, DataProvider } from "react-admin";
import crudProvider from "ra-data-dataui-crud";

const dataProvider = crudProvider("http://localhost:3000");

const AdminApp = () => (
  <Admin dataProvider={dataProvider as DataProvider}>
    <Resource name="users" list={ListGuesser} edit={EditGuesser} recordRepresentation="name" />
    />
  </Admin>
);

export default AdminApp;
```

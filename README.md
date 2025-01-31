# Skoolab - ESlint Config Nest

Skoolab's custom ESLint configuration for NestJS is designed to provide a consistent linting and formatting experience for NestJS projects. It includes custom rules, Prettier integration, and support for functional programming styles.

---

## **Prerequisites**

Ensure the following tools are installed and compatible with your project:

- **Node.js**: Version `22` or higher.
- **npm**: Latest version.
- **eslint**: Version `^9.19.0` (peer dependency).
- **typescript**: Version `^5.7.3` (peer dependency).
- **prettier**: Version `^3.4.2` (peer dependency).

---

## **Installation**

To install the Skoolab ESLint Config NestJS configuration, run the following command:

```bash
npm install @skoolab/eslint-config-nest eslint typescript prettier -D
```

---

## **Usage**

1. **Create an ESLint Config File**  
   Add a `eslint.config.js` file to your project root with the following content:

   ```javascript
   import skoolabConfig from '@skoolab/eslint-config'

   export default [...skoolabConfig]
   ```

2. **Add prettier configuration file**
   Add a `.prettierrc` file to your project root with the following content:

   ```json
   {
     "singleQuote": true,
     "semi": false,
     "trailingComma": "es5",
     "tabWidth": 2,
     "useTabs": false,
     "printWidth": 80,
     "arrowParens": "avoid",
     "endOfLine": "lf"
   }
   ```

3. **Lint Your Project**  
   Use the following command to lint your files:

   ```bash
   npx eslint .
   ```

---

## **Custom Rules**

The configuration includes custom rules tailored for TypeScript projects:

- **No Direct Return**: Avoid direct returns; values must be assigned to variables before returning.
- **Method Call Order**: Methods must be ordered top-to-bottom, respecting their call hierarchy.
- **Interfaces in Separate Files**: Interfaces must be declared in separate files from implementation.
- **Enforce Enums**: Prefer enums over multiple related constants.

---

## **Features**

1. **Customizable Rules**: Extend or override the rules as needed.
2. **Prettier Integration**: Ensures consistent code formatting.
3. **Functional Style Support**: Includes rules for immutability and pure functions.
4. **Custom Linters**: Rules for interfaces, enums, and method order.

---

## **Support**

For issues or feature requests, visit our [GitHub Issues Page](https://github.com/Skoolab/eslint-config-nest/issues).

---

## **License**

This project is licensed under the [MIT License](https://opensource.org/licenses/MIT).

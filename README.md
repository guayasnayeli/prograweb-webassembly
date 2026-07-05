# Hello World — WebAssembly with AssemblyScript

## What does it do?
Three functions written in AssemblyScript are compiled to WebAssembly.
A JavaScript client loads the `.wasm` file in the browser and calls
each function when the user clicks a button — without any page reload.

## Functions implemented
- `sum(a, b)`        → returns the sum of two integers
- `multiply(a, b)`   → returns the product of two integers
- `factorial(n)`     → returns the factorial of n recursively

## How to run it

### 1. Install dependencies
npm install

### 2. Compile AssemblyScript to WebAssembly
npm run asbuild

### 3. Start local server
npx serve .

### 4. Open in browser
http://localhost:3000

## Key files
- assembly/index.ts  → functions written in AssemblyScript (compiled to Wasm)
- build/release.wasm → compiled binary loaded by the browser
- index.html         → HTML client that calls the Wasm functions via JavaScript

## Evidence
- The browser downloads release.wasm (0.1 kB) automatically on page load
- All operations execute inside the browser's WebAssembly engine
- Verified via Chrome DevTools → Network tab → Type: wasm
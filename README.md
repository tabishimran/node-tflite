# tflite-js

TensorFlow Lite for JavaScript (unofficial)

## Supported Platforms

- Node
  - [x] macOS
  - [ ] Windows
  - [ ] Linux
- WebAssembly
  - [ ] MVP
  - [ ] pthreads
  - [ ] pthreads + SIMD

## Install

```
npm install tflitejs
```

## Use

```js
import { Interpreter } from "tflitejs";

const modelData = fs.readFileSync(modelPath);
const interpreter = new Interpreter(modelData);

interpreter.allocateTensors();

interpreter.inputs[0].copyFrom(inputData);

interpreter.invoke();

interpreter.outputs[0].copyTo(outputData);
```

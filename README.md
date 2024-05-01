# @devtea2026/voluptates-laboriosam-asperiores-necessitatibus

[![npm version](https://img.shields.io/npm/v/@devtea2026/voluptates-laboriosam-asperiores-necessitatibus.svg)](https://npmjs.org/package/@devtea2026/voluptates-laboriosam-asperiores-necessitatibus)

Easy and small child_process.spawn.

- Promise-based
- Cross-platform
- Pass stdin as an argument
- Rejects on stderr by default, even if exit code is 0

## Install

```sh
$ npm install --save @devtea2026/voluptates-laboriosam-asperiores-necessitatibus
```

## Usage

```typescript
(
  command: string,
  args?: string[],
  options?: Options,
  spawnOptions?: any,
): Promise<{
  stdout: string
  stderr: string
}>
```

```js
import spawn from '@devtea2026/voluptates-laboriosam-asperiores-necessitatibus'

const { stdout, stderr } = await spawn('printf', ['please?'])

assert.equal(stdout, 'please?')
assert.equal(stderr, '')
```

## Options

- `rejectOnError: boolean` - Throws an error if stderr is non-empty. Default: true.
- `stdin: string` - Send stdin to the spawned child process.
- `stdout: (data: string) => void` - Stream stdout by chunk.
- `stderr: (data: string) => void` - Stream stderr by chunk.

## License

ISC © [Raine Revere](https://github.com/raineorshine)

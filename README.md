# most-create
> Create imperative stream for mostjs, useful for bridging custom events source (e.g react)

[![npm](https://img.shields.io/npm/v/most-create.svg)](https://www.npmjs.com/package/most-create)

## Install

```bash
npm i -S most-create
```

## Usage

### create

Create a mostjs stream with ability to manually emit event. Based on Proxy

Type: `function`

Context: `any`

Target: `any`

Produce: `stream`

```typescript
    private inputChangeStream = create<React.SyntheticEvent<HTMLInputElement>>("inputChangeStream");
    ...
    this.inputChangeStream.observe((e) => {
    	this.model.setDisplayValue(e.currentTarget.value);
    });
    ...
    public onInputChange = (e: React.SyntheticEvent<HTMLInputElement>): void => {
    	this.inputChangeStream.emit(e);
    };
```



## License

Apache License 2.0

[npm-image]: https://img.shields.io/npm/v/live-xxx.svg
[npm-url]: https://npmjs.org/package/live-xxx
[travis-image]: https://img.shields.io/travis/live-js/live-xxx/master.svg
[travis-url]: https://travis-ci.org/live-js/live-xxx
[coveralls-image]: https://img.shields.io/coveralls/live-js/live-xxx/master.svg
[coveralls-url]: https://coveralls.io/r/live-js/live-xxx?branch=master
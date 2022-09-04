# lightwaight-xlsx-file-parser

based on https://github.com/trevordixon/excel.js work for local files.

# installation

```sh
$ npm i lightwaight-xlsx-file-parser
```

# Usage

```js 
    import XLSXParser from 'lightwaight-xlsx-file-parser'

    ...
    const parser = new XLSXParser(buffer);
    const sheets = await parser.parse();
```

# sheet

```ts
class Sheet {
    cells: Cell[];
    columnNames: string[];
    name: string;
    constructor(init?: Partial<Sheet>);
    get numberOfRows(): number;
    get numberOfColumns(): number;
    get startRow(): number;
    get startColumn(): number;
    get rowsAsJson(): any[][];
    getRow(index: number): Row;
    getColumn(index: number): Column;
    getCell(row: number, column: number): Cell;
}
```


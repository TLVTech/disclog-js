# disclog

`disclog` is an npm package for logging messages to a Discord channel using a webhook. It provides a simple and easy-to-use interface for sending messages of different levels (info, warning, and error) to a Discord channel, with customizable formatting and colors.

## Preview
<img width="813" alt="image" src="https://user-images.githubusercontent.com/61319421/229336686-a2632373-2249-4166-b32e-ffbef3d0cd1b.png">


## Installation

You can install `disclog` using npm:

`npm install disclog `

## Usage

To use disclog in your project, first import the `Disclog` class:

```js
// Using require:
const { Disclog } = require('disclog');

// Using import (for ES6 / TypeScript):
import { Disclog } from 'disclog';
```
Then create a new instance of Disclog with your Discord webhook URL:

```js
const logger = new Disclog('https://discord.com/api/webhooks/1234567890/abcdefghijklmnopqrstuvwxyz');
```

You can then use the info(), warning(), and error() methods to send messages of different levels to your Discord channel:

```js
logger.info('Server started successfully on port 8080');
logger.warning('Authentication failed for user: jane.doe@example.com');
```

```js
try {
    throw new Error('Sample error message')
}catch(e){
    logger.error(e.message)
}  
```

## License

`disclog` is released under the MIT License. See LICENSE for more information.

```
MIT License

Copyright (c) [year] [fullname]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

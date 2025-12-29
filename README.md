# ELI Demo Projects

Example projects demonstrating how to use [ELI (Experimentation Local Interface)](https://github.com/briannorman/eli).

## Setup

1. Clone this repository:
   ```bash
   git clone https://github.com/briannorman/eli-demo-projects.git
   cd eli-demo-projects
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Configure ELI to use this directory:
   - Open the ELI Chrome extension
   - Enter the full path to this directory in the "Projects Directory" field
   - Click "Set"

4. Start the ELI server (if not already running):
   ```bash
   # From the main ELI repository
   npm start
   # or
   npx eli
   ```

5. Open the ELI extension popup and select a project/variant to test!

## Project Structure

Each project folder contains variant folders (v1, v2, etc.) with:
- JavaScript files (`.js`) - Main experiment code
- HTML files (`.html`) - Optional templates
- SCSS files (`.scss`) - Optional styles
- `shared.js` - Optional shared code for all variants

## Using Utils

All projects can use the ELI utils library:

```javascript
import utils from '@eli/utils';

// Wait for element
utils.waitForElement('#myElement').then(element => {
  console.log('Found:', element);
});

// DOM manipulation
utils.addClass('#button', 'active');
utils.on('#button', 'click', () => console.log('Clicked!'));
```

The utils are automatically available - no need to import them separately if you've run `npm install` in this directory.

## Projects

- `example-project-one` - Basic example with multiple variants
- `example-project-two` - Another example project

## License

MIT


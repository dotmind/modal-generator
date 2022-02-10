<div align="center">
  <img alt="Logo" src="https://github.com/dotmind/react-modals/raw/master/dotmind-logo.png" width="100" />
</div>
<h1 align="center">
  @dotmind/react-modals
</h1>
<p align="center">
  React Modals is a tool to quickly generate modals
</p>
<p align="center">
  <a href="https://github.com/dotmind/react-modals">
    <img src="https://img.shields.io/npm/v/@dotmind/react-modals" />
  </a>
  <a href="https://github.com/dotmind/react-modals">
    <img src="https://img.shields.io/github/license/dotmind/react-modals" />
  </a>
  <a href="https://github.com/dotmind/react-modals">
    <img src="https://img.shields.io/npm/types/typescript" />
  </a>
</p>

## Menu

- [Menu](#menu)
- [✋ Disclaimer](#-disclaimer)
- [💻 Installation](#-installation)
- [👷‍♂️ How it's work](#️-how-its-work)
  - [Modal usage](#modal-usage)
- [⚡️ Contributing](#️-contributing)
- [🔐 License](#-license)

## ✋ Disclaimer

This package helps to create custom modals in a blaze speed 🚀.

You need react >= 16.0.

## 💻 Installation

```bash
yarn add @dotmind/react-modals
```

or

```bash
npm i @dotmind/react-modals
```

## 👷‍♂️ How it's work

<p align="center">
  <a href="https://codesandbox.io/s/react-modals-jumgq">
    React Modals sandbox
  </a>
</p>

### Modal usage

```javascript
import React, { useCallback, useState } from 'react';

import Modal from 'react-modals';

const App: React.FC = () => {
  const [modalOpen, setModalOpen] = useState(false);

  const handleOpenModal = useCallback(() => {
    setModalOpen(true);
  }, []);

  const handleCloseModal = useCallback(() => {
    setModalOpen(false);
  }, []);

  return (
    <div>
      <h1>Test react modal</h1>
      <button onClick={handleOpenModal}>Click me !</button>
      <Modal modalOpen={modalOpen} onClose={handleCloseModal}>
        <h1>This is modal content</h1>
        <p>You can put your html here, have fun !</p>
      </Modal>
    </div>
  );
};
```

| props                | description                      | required | type                   |
| -------------------- | -------------------------------- | -------- | ---------------------- |
| modalOpen            | Modal state                      | true     | boolean                |
| onClose              | Close modal function             | true     | () => void             |
| children             | Modal content                    | true     | ReactNode              |
| closeButtonElement   | Modify close button element      | false    | ReactElement or string |
| closeButtonClassName | Add custom class on close button | false    | string                 |
| containerClassName   | Add custom class on container    | false    | string                 |
| contentClassName     | Add custom class on content      | false    | string                 |
| withShadow           | Add default box shadow           | false    | boolean                |

## ⚡️ Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## 🔐 License

[MIT](https://choosealicense.com/licenses/mit/)

## react-native-sliding-modal

Sliding modal as the name suggests a React Native modal you can slide up to expand, slide down to close.

## Example

## Usage

```shell
npm install https://github.com/nazimamin/react-native-sliding-modal/tarball/master --save
```

```js
import Modal from 'react-native-sliding-modal';
```

```html
  <Modal
    show={this.state.showModal}
    closeCallback={this.closeModal}
    top={Layout.window.height - 350}
    fullScreenCallback={() => {}}
  >
     <Modal.Header
        style={{
          alignItems: 'center',
          justifyContent: 'center'
        }}
      >
        <Icon
          name="minus"
          color="#5d0e8b8f"
          size={32}
          style={{
            top: -3
          }}
        />
        <Text
          Header Title
        </Text>
      </Modal.Header>
    {this.renderModalContent()}
  </Modal>
```

Props

```js
    show: PropTypes.bool.isRequired,
    children: PropTypes.node,
    closeCallback: PropTypes.func, //callback fires when clicking on backdrop, sliding down modal at `top` prop
    fullScreenCallback: PropTypes.func, //callback fires when modal is full screen
    halfScreenCallback: PropTypes.func, //callback fires when modal if half
    top: PropTypes.number  //if initially want to open the modal at a specific height
```

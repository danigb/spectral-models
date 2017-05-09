<a name="DFT"></a>

## DFT(size, [window]) ⇒ <code>Object</code>
Create a DFT model. A DFT model allows to perform dft analysis of a signal
using a fast fourier function.

**Kind**: global function  
**Returns**: <code>Object</code> - an object with two functions: analisys and synthesis  

| Param | Type | Description |
| --- | --- | --- |
| size | <code>number</code> | the size of the signal |
| [window] | <code>window</code> | the window to use (or a hamming window if not specified) |

**Example**  
```js
import DFT from 'spectral-models'
const dft = DFT(512)
dft.analisys(signal)
```

* [DFT(size, [window])](#DFT) ⇒ <code>Object</code>
    * [.analisys(input)](#DFT.analisys) ⇒ <code>Object</code>
    * [.synthesis(analisys)](#DFT.synthesis) ⇒ <code>Array</code>

<a name="DFT.analisys"></a>

### DFT.analisys(input) ⇒ <code>Object</code>
Given a real signal, create a { magnitudes, phases } object.
The size of the input must be the same as specified in the constructor.

**Kind**: static method of <code>[DFT](#DFT)</code>  
**Returns**: <code>Object</code> - a `{ magnitudes, phases }` object  

| Param | Type | Description |
| --- | --- | --- |
| input | <code>Array</code> | the input signal |

<a name="DFT.synthesis"></a>

### DFT.synthesis(analisys) ⇒ <code>Array</code>
Given a { magnitudes, phases } object, return the initial signal.
Notice that the signal will have a window applied.

**Kind**: static method of <code>[DFT](#DFT)</code>  
**Returns**: <code>Array</code> - the signal  

| Param | Type | Description |
| --- | --- | --- |
| analisys | <code>Object</code> | the analysis object |


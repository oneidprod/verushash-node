# verushash-node

Implementation of the VerusHash V1, V2, V2.1, V2.2 hash algorithm as a Node.js native addon.

## Verus / Node 18 Fork (oneidprod)

This fork patches the C++ addon for **Node.js 18 compatibility**.

### Changes from upstream

- `Handle<Object>` replaced with `Local<Object>` throughout
- All `String::NewFromUtf8` calls use `.ToLocalChecked()`
- `.ToObject()` calls updated to `.ToObject(isolate->GetCurrentContext()).ToLocalChecked()`
- `binding.gyp`: `-std=c++11` changed to `-std=c++17`

## Dependencies

```
sudo apt install libsodium-dev
```

## Testing

```bash
git clone https://github.com/oneidprod/verushash-node
cd verushash-node
npm install
node test.js
```

### Example output

```
'VerusHash1   Output' '2cd709e6569bd706f14a09e62042ddccfa63bd3725b21f35a8c98adbf4151184'
'VerusHash2   Output' '55cec43b110570481f6d565c3a8bb6ed174956494aeebf4c264283791dbd3ded'
'VerusHash2b  Output' 'f971af1d4e551e9e71d35c6266fc19a98c6ad0388be1e9979f66921e07b5c9ac'
'VerusHash2b1 Output' '0ef8b9530ce44a7ffb9b520daf8fcf59d1d22dd1bfa1a26ef4351d51e37071b7'
```

## Donate

If you find this useful, tips are appreciated:

| Coin | Address |
|-|-|
| LTC | LWpuHQUGw3qZg8MCHYGgTPRZ3a1i8jc5u3 |
| BTC | bc1qw0t40dunylgtz9kgfylwxac3a8vwp70cgrga5r |
| SOL | up9YvW6ewNati5fmmDjGHzFbq8UkSbHPccoDNzijk3G |
| POL | 0x5198f52fA768294ae66f0cB75A98DCc895a36F2E |
| DOGE | DJAg2fTzS5vN3yXDPn5gGPz9JSmzJn3cXD |
| VRSC | RXPo4WbNn6x494HL2MAHxD6eNvj6JqVKBU |

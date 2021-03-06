---
Description: A callback function that must be implemented by a user to set render state.
ms.assetid: a5a27e30-c141-44a4-b8d4-38c1d6076b2a
title: ID3DXEffectStateManager::SetRenderState method (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetRenderState
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
---

# ID3DXEffectStateManager::SetRenderState method

A callback function that must be implemented by a user to set render state.

## Syntax


```C++
HRESULT SetRenderState(
  [in] D3DRENDERSTATETYPE State,
  [in] DWORD              Value
);
```



## Parameters

<dl> <dt>

*State* \[in\]
</dt> <dd>

Type: **[**D3DRENDERSTATETYPE**](https://msdn.microsoft.com/library/Bb172599(v=VS.85).aspx)**

The render state to set. [**D3DRENDERSTATETYPE**](https://msdn.microsoft.com/library/Bb172599(v=VS.85).aspx)

</dd> <dt>

*Value* \[in\]
</dt> <dd>

Type: **[**DWORD**](https://msdn.microsoft.com/library/Aa383751(v=VS.85).aspx)**

The render state value. See [Effect States (Direct3D 9)](effect-states.md).

</dd> </dl>

## Return value

Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

The user-implemented method should return S\_OK. If the callback fails when setting the device state, either of the following will occur:

-   The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).
-   The dynamic effect state call (such as [**IDirect3DDevice9::SetRenderState**](https://msdn.microsoft.com/library/Bb174454(v=VS.85).aspx)) will fail.

## Requirements



|                    |                                                                                          |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Library<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## See also

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 





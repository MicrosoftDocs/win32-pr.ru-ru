---
description: Использует предоставляемую пользователем функцию для заполнения каждого шаг текселя каждого уровня MIP заданной текстуры.
ms.assetid: 9c822472-2bbf-4629-bdb3-6491573e8de2
title: Функция D3DXFillTexture (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFillTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 20790a9e4c1a9ce242a5e067dd617c7871a70b7c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354863"
---
# <a name="d3dxfilltexture-function"></a>Функция D3DXFillTexture

Использует предоставляемую пользователем функцию для заполнения каждого шаг текселя каждого уровня MIP заданной текстуры.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXFillTexture(
  _Out_ LPDIRECT3DTEXTURE9 pTexture,
  _In_  LPD3DXFILL2D       pFunction,
  _In_  LPVOID             pData
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*птекстуре* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Указатель на интерфейс [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , представляющий текстуру с заливкой.

</dd> <dt>

*пфунктион* \[ окне\]
</dt> <dd>

Тип: **[LPD3DXFILL2D](lpd3dxfill2d.md)**

Указатель на предоставляемую пользователем функцию оценщика, которая будет использоваться для вычисления значения каждого шаг текселя. Функция соответствует прототипу [LPD3DXFILL2D](lpd3dxfill2d.md).

</dd> <dt>

*pData* \[ окне\]
</dt> <dd>

Тип: **[ **лпвоид**](../winprog/windows-data-types.md)**

Указатель на произвольный блок определяемых пользователем данных. Этот указатель будет передан функции, предоставленной в *пфунктион*.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается с ошибкой, возвращаемое значение может быть одним из следующих значений: D3DERR \_ инвалидкалл.

## <a name="remarks"></a>Комментарии

Ниже приведен пример, в котором создается функция с именем Колорфилл, которая основывается на D3DXFillTexture.


```
// Define a function that matches the prototype of LPD3DXFILL3D
VOID WINAPI ColorFill (D3DXVECTOR4* pOut, const D3DXVECTOR2* pTexCoord, 
const D3DXVECTOR2* pTexelSize, LPVOID pData)
{
    *pOut = D3DXVECTOR4(pTexCoord->x, pTexCoord->y, 0.0f, 0.0f);
}
    
    
// Fill the texture using D3DXFillTexture
if (FAILED (hr = D3DXFillTexture (m_pTexture, ColorFill, NULL)))
{
    return hr;
}
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции текстуры в D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 

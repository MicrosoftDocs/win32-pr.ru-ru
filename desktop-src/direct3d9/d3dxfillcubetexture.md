---
description: Использует предоставляемую пользователем функцию для заполнения каждого шаг текселя каждого уровня MIP заданной текстуры Куба.
ms.assetid: 0390a1b6-6675-42e1-bc45-65dd7b2d83c5
title: Функция D3DXFillCubeTexture (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFillCubeTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2fe82650aba639d0cd506bcdf86019a316890e7312e9bd008f0d16542af09de3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118298552"
---
# <a name="d3dxfillcubetexture-function"></a>Функция D3DXFillCubeTexture

Использует предоставляемую пользователем функцию для заполнения каждого шаг текселя каждого уровня MIP заданной текстуры Куба.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXFillCubeTexture(
  _Out_ LPDIRECT3DCUBETEXTURE9 pTexture,
  _In_  LPD3DXFILL3D           pFunction,
  _In_  LPVOID                 pData
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*птекстуре* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)**

Указатель на интерфейс [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) , представляющий текстуру с заливкой.

</dd> <dt>

*пфунктион* \[ окне\]
</dt> <dd>

Тип: **[LPD3DXFILL3D](lpd3dxfill3d.md)**

Указатель на предоставляемую пользователем функцию оценщика, которая будет использоваться для вычисления значения каждого шаг текселя. Функция соответствует прототипу [LPD3DXFILL3D](lpd3dxfill3d.md).

</dd> <dt>

*pData* \[ окне\]
</dt> <dd>

Тип: **[ **лпвоид**](../winprog/windows-data-types.md)**

Указатель на произвольный блок определяемых пользователем данных. Этот указатель будет передан функции, предоставленной в *пфунктион*.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается с ошибкой, возвращаемое значение может быть одним из следующих значений: D3DERR \_ инвалидкалл.

## <a name="remarks"></a>Remarks

Ниже приведен пример, в котором создается функция с именем Колоркубефилл, которая основывается на D3DXFillCubeTexture.


```
// Define a function that matches the prototype of LPD3DXFILL3D
VOID WINAPI ColorCubeFill (D3DXVECTOR4* pOut, const D3DXVECTOR3* pTexCoord, 
const D3DXVECTOR3* pTexelSize, LPVOID pData)
{
    *pOut = D3DXVECTOR4(pTexCoord->x, pTexCoord->y, pTexCoord->z, 0.0f);
}
    
    
// Fill the texture using D3DXFillCubeTexture
if (FAILED (hr = D3DXFillCubeTexture (m_pTexture, ColorCubeFill, NULL)))
{
    return hr;
}
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции текстуры в D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 

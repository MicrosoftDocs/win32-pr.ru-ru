---
description: Использует предоставляемую пользователем функцию для заполнения каждого шаг текселя для каждого уровня MIP заданной текстуры тома.
ms.assetid: cc9eb051-8a62-4e35-87df-c255f10e94d8
title: Функция D3DXFillVolumeTexture (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFillVolumeTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7e0ef21c3fb9b5443cc488a3b6fc953953cffee6e5d0dc417dee69969907f86e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123294"
---
# <a name="d3dxfillvolumetexture-function"></a>Функция D3DXFillVolumeTexture

Использует предоставляемую пользователем функцию для заполнения каждого шаг текселя для каждого уровня MIP заданной текстуры тома.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXFillVolumeTexture(
  _Out_ LPDIRECT3DVOLUMETEXTURE9 pTexture,
  _In_  LPD3DXFILL3D             pFunction,
  _In_  LPVOID                   pData
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*птекстуре* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)**

Указатель на интерфейс [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) , представляющий текстуру с заливкой.

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

Если том не является динамическим (поскольку при его создании используется значение 0) и находится в видеопамяти (пул памяти со значением D3DPOOL \_ по умолчанию), **D3DXFillVolumeTexture** не удастся, так как том не может быть заблокирован.

В этом примере создается функция с именем Колорволумефилл, которая основывается на D3DXFillVolumeTexture.


```
// Define a function that matches the prototype of LPD3DXFILL3D
VOID WINAPI ColorVolumeFill (D3DXVECTOR4* pOut, const D3DXVECTOR3* pTexCoord, 
const D3DXVECTOR3* pTexelSize, LPVOID pData)
{
   *pOut = D3DXVECTOR4(pTexCoord->x, pTexCoord->y, pTexCoord->z, 0.0f);
}
    
    
// Fill volume texture
if (FAILED (hr = D3DXFillVolumeTexture (m_pTexture, ColorVolumeFill, NULL)))
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

 

 

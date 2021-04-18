---
description: Создает область прорисовки.
ms.assetid: 35e0007e-c405-46e1-a52b-625adc84732b
title: Функция D3DXCreateRenderToSurface (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateRenderToSurface
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6fc64cbc65d30838db2105e0458d3553247f1ab1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713697"
---
# <a name="d3dxcreaterendertosurface-function"></a>Функция D3DXCreateRenderToSurface

Создает область прорисовки.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXCreateRenderToSurface(
  _In_  LPDIRECT3DDEVICE9     pDevice,
  _In_  UINT                  Width,
  _In_  UINT                  Height,
  _In_  D3DFORMAT             Format,
  _In_  BOOL                  DepthStencil,
  _In_  D3DFORMAT             DepthStencilFormat,
  _Out_ LPD3DXRENDERTOSURFACE *ppRenderToSurface
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдевице* \[ окне\]
</dt> <dd>

Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , устройство, которое должно быть связано с областью прорисовки.

</dd> <dt>

*Ширина* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Ширина поверхности рендеринга в пикселях.

</dd> <dt>

*Высота* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Высота поверхности рендеринга (в пикселях).

</dd> <dt>

*Формат* \[ окне\]
</dt> <dd>

Тип: **[D3DFORMAT](d3dformat.md)**

Элемент перечисляемого типа [D3DFORMAT](d3dformat.md) , описывающий формат пикселей поверхности рендеринга.

</dd> <dt>

*ДепсстенЦил* \[ окне\]
</dt> <dd>

Тип: **[ **bool** .](../winprog/windows-data-types.md)**

Если **значение — true**, поверхность рендеринга поддерживает поверхность набора элементов глубины. В противном случае этому члену присваивается **значение false**. Эта функция создаст новый буфер глубины.

</dd> <dt>

*ДепсстенЦилформат* \[ окне\]
</dt> <dd>

Тип: **[D3DFORMAT](d3dformat.md)**

Если *депсстенЦил* имеет значение **true**, этот параметр является членом перечислимого типа [D3DFORMAT](d3dformat.md) , описывающим формат трафарета глубины области рендеринга.

</dd> <dt>

*ппрендертосурфаце* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXRENDERTOSURFACE**](id3dxrendertosurface.md)\***

Адрес указателя на интерфейс [**ID3DXRenderToSurface**](id3dxrendertosurface.md) , представляющий созданную область отрисовки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции общего назначения](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 

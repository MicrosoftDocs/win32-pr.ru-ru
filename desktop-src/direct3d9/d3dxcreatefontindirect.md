---
description: Создает объект шрифта косвенно для устройства и шрифта.
ms.assetid: 480f3012-8495-47ca-a649-11ce53cee06c
title: Функция D3DXCreateFontIndirect (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateFontIndirect
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 555c4b1f3615639d9da01fb7a2a96aa5cb15f697235c918d5130ffcd4d43baa4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988664"
---
# <a name="d3dxcreatefontindirect-function"></a>Функция D3DXCreateFontIndirect

Создает объект шрифта косвенно для устройства и шрифта.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXCreateFontIndirect(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_  const D3DXFONT_DESC     *pDesc,
  _Out_       LPD3DXFONT        *ppFont
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдевице* \[ окне\]
</dt> <dd>

Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , устройство, связываемое с объектом Font.

</dd> <dt>

*пдеск* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXFONT \_ DESC**](d3dxfont-desc.md) \***

Указатель на структуру [**\_ DESC D3DXFONT**](d3dxfont-desc.md) , описывающую атрибуты создаваемого объекта Font. Если для параметров компилятора требуется Юникод, тип данных D3DXFONT \_ DESC разрешается в D3DXFONT \_ дескв; в противном случае тип данных разрешается в D3DXFONT \_ DESC. См. заметки.

</dd> <dt>

*ппфонт* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXFONT**](id3dxfont.md)\***

Возвращает указатель на интерфейс [**ID3DXFont**](id3dxfont.md) , представляющий созданный объект Font.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarks

Параметр компилятора также определяет версию функции. Если определен Юникод, вызов функции разрешается в D3DXCreateFontIndirectW. В противном случае вызов функции разрешается в D3DXCreateFontIndirectA, так как используются строки ANSI.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[Функции общего назначения](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 

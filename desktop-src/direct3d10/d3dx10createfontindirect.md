---
description: Создает объект Font. Примечание. вместо использования этой функции рекомендуется использовать DirectWrite и библиотеку Директкстк, класс Спритефонт.
ms.assetid: 057ee033-37d8-4fc1-9f35-776393fff008
title: Функция D3DX10CreateFontIndirect (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateFontIndirect
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: ae69b02483a94a80a06ef52ee4857eb081cfcfb2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354483"
---
# <a name="d3dx10createfontindirect-function"></a>Функция D3DX10CreateFontIndirect

Создает объект Font.

> [!Note]  
> Вместо использования этой функции рекомендуется использовать [DirectWrite](../directwrite/direct-write-portal.md) и библиотеку [Директкстк](https://github.com/Microsoft/DirectXTK) , класс **спритефонт** .

 

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DX10CreateFontIndirect(
  _In_        ID3D10Device     *pDevice,
  _In_  const D3DX10_FONT_DESC *pDesc,
  _Out_       LPD3DX10FONT     *ppFont
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдевице* \[ окне\]
</dt> <dd>

Тип: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***

Указатель на интерфейс интерфейса [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) .

</dd> <dt>

*пдеск* \[ окне\]
</dt> <dd>

Тип: **const [**D3DX10 \_ Font \_ DESC**](d3dx10-font-desc.md) \***

Указатель на [**D3DX10 структуру \_ шрифта \_**](d3dx10-font-desc.md) с описанием атрибутов создаваемого объекта Font. Если определен Юникод, вызов функции разрешается в D3DXCreateFontIndirectW. В противном случае вызов функции разрешается в D3DXCreateFontIndirectA, так как используются строки ANSI.

</dd> <dt>

*ппфонт* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DX10FONT**](id3dx10font.md)\***

Возвращает указатель на [**интерфейс ID3DX10Font**](id3dx10font.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Core. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции общего назначения](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 

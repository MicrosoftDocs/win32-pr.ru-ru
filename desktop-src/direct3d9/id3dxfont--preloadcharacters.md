---
description: Загружает ряд символов в видеопамять для повышения эффективности отрисовки на устройстве.
ms.assetid: bb49842e-99de-406b-bf4b-139d6499f96e
title: 'ID3DXFont: метод:P Релоадчарактерс (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.PreloadCharacters
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2cad2a324a6a5d56ff88dd343cf091b8c4ff2b99cd829344ae91f364458ec51a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118295320"
---
# <a name="id3dxfontpreloadcharacters-method"></a>ID3DXFont: метод:P Релоадчарактерс

Загружает ряд символов в видеопамять для повышения эффективности отрисовки на устройстве.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT PreloadCharacters(
  [in] UINT First,
  [in] UINT Last
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Сначала* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Идентификатор первого символа, загружаемого в видеопамять.

</dd> <dt>

*Последний раз* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Идентификатор последнего символа, который должен быть загружен в видеопамять.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Remarks

Этот метод создает текстуры, содержащие глифы, представляющие входные символы. Глифы рисуются в виде ряда треугольников.

Символы не будут подготавливаться к просмотру на устройстве; Для визуализации символов необходимо по-прежнему вызывать [**DrawText**](id3dxfont--drawtext.md) . Однако при предварительной загрузке символов в видеопамять **DrawText** будет использовать значительно меньше ресурсов ЦП.

Этот метод внутренне преобразует символы в глифы с помощью функции GDI [**жетчарактерплацемент**](/windows/win32/api/wingdi/nf-wingdi-getcharacterplacementa).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXFont](id3dxfont.md)
</dt> </dl>

 

 

---
description: Интерфейс ID3DX10Font инкапсулирует текстуры и ресурсы, необходимые для отображения определенного шрифта на определенном устройстве.
ms.assetid: 81f4ffe3-f50d-47ce-ae85-15a2a19cacbd
title: Интерфейс ID3DX10Font (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 7d7c9fb1daa0934b5e6b3147f60803be5c0b5c07
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273798"
---
# <a name="id3dx10font-interface"></a>Интерфейс ID3DX10Font

Интерфейс ID3DX10Font инкапсулирует текстуры и ресурсы, необходимые для отображения определенного шрифта на определенном устройстве.

## <a name="members"></a>Элементы

Интерфейс **ID3DX10Font** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DX10Font** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ID3DX10Font** содержит следующие методы.



| Метод                                                     | Описание                                                                                                                                           |
|:-----------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DrawText**](id3dx10font-drawtext.md)                   | Рисование форматированного текста. Этот метод поддерживает строки ANSI и Юникод.<br/>                                                                        |
| [**GetDC**](id3dx10font-getdc.md)                         | Возвращает маркер для контекста дисплея устройства (DC), для которого установлен шрифт.<br/>                                                            |
| [**GetDesc**](id3dx10font-getdesc.md)                     | Получение описания текущего объекта Font.<br/>                                                                                              |
| [**GetDevice**](id3dx10font-getdevice.md)                 | Получите устройство Direct3D, связанное с объектом Font.<br/>                                                                              |
| [**жетглифдата**](id3dx10font-getglyphdata.md)           | Возвращает сведения о размещении и ориентации глифа в символьной ячейке.<br/>                                                     |
| [**жеттекстметрикс**](id3dx10font-gettextmetrics.md)       | Получение характеристик шрифта.<br/>                                                                                                             |
| [**прелоадчарактерс**](id3dx10font-preloadcharacters.md) | Загрузка последовательности символов в видеопамять для повышения эффективности отрисовки на устройстве.<br/>                                        |
| [**прелоадглифс**](id3dx10font-preloadglyphs.md)         | Загрузка ряда глифов в видеопамять для повышения эффективности отрисовки на устройстве.<br/>                                            |
| [**прелоадтекст**](id3dx10font-preloadtext.md)             | Загрузка форматированного текста в видеопамять для повышения эффективности отрисовки на устройстве. Этот метод поддерживает строки ANSI и Юникод.<br/> |



 

## <a name="remarks"></a>Комментарии

Интерфейс ID3DX10Font получается путем вызова [**D3DX10CreateFont**](d3dx10createfont.md) или [**D3DX10CreateFontIndirect**](d3dx10createfontindirect.md).

Тип LPD3DX10FONT определяется как указатель на интерфейс ID3DX10Font.


```
typedef interface ID3DX10Font ID3DX10Font;
typedef interface ID3DX10Font *LPD3DX10FONT;
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Интерфейсы D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 

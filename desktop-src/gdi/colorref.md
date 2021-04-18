---
Description: Значение COLORREF используется для указания цвета RGB.
ms.assetid: b87d3de2-7a13-44ef-8253-c6851a75fa54
title: COLORREF (Виндеф. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 6836cfcc1b18d0b20d5e347fb83206551b27de06
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "104998882"
---
# <a name="colorref"></a>COLORREF

Значение COLORREF используется для указания цвета [RGB](/windows/desktop/api/Wingdi/nf-wingdi-rgb) .


```C++
typedef DWORD COLORREF;
typedef DWORD* LPCOLORREF;
```



## <a name="remarks"></a>Примечания

При указании явного цвета [RGB](/windows/desktop/api/Wingdi/nf-wingdi-rgb) значение **COLORREF** имеет следующую шестнадцатеричную форму:

`0x00bbggrr`

Байт нижнего порядка содержит значение для относительной интенсивности красного цвета; второй байт содержит значение для зеленого цвета; третий байт содержит значение синего. Байт высокого порядка должен быть равен нулю. Максимальное значение для одного байта — 0xFF.

Чтобы создать значение цвета **COLORREF** , используйте макрос [RGB](/windows/desktop/api/Wingdi/nf-wingdi-rgb) . Чтобы извлечь отдельные значения для красного, зеленого и синего компонентов значения цвета, используйте макросы [**rvalue**](/windows/desktop/api/Wingdi/nf-wingdi-getrvalue), [жетгвалуе](/windows/desktop/api/Wingdi/nf-wingdi-getgvalue)и [жетбвалуе](/windows/desktop/api/Wingdi/nf-wingdi-getbvalue) соответственно.

## <a name="example"></a>Например, .

```cpp
// Color constants.
const COLORREF rgbRed   =  0x000000FF;
const COLORREF rgbGreen =  0x0000FF00;
const COLORREF rgbBlue  =  0x00FF0000;
const COLORREF rgbBlack =  0x00000000;
const COLORREF rgbWhite =  0x00FFFFFF;
```

Пример из [классической выборки Windows](https://github.com/microsoft/Windows-classic-samples) на сайте GitHub.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                              |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                    |
| Заголовок<br/>                   | <dl> <dt>Виндеф. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Общие сведения о цветах](colors.md)
</dt> <dt>

[Цветовые структуры](color-structures.md)
</dt> <dt>

[жетбвалуе](/windows/desktop/api/Wingdi/nf-wingdi-getbvalue)
</dt> <dt>

[жетгвалуе](/windows/desktop/api/Wingdi/nf-wingdi-getgvalue)
</dt> <dt>

[**RValue**](/windows/desktop/api/Wingdi/nf-wingdi-getrvalue)
</dt> <dt>

[RGB](/windows/desktop/api/Wingdi/nf-wingdi-rgb)
</dt> </dl>

 

 





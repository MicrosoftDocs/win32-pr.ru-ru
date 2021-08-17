---
description: Метаданные изображения можно хранить и получать с помощью объекта Пропертитем. Член данных типа объекта Пропертитем указывает тип данных значений, хранящихся в элементе данных значения этого же объекта Пропертитем.
ms.assetid: d05cdf42-4b30-45ce-85a1-025d4f4e9d13
title: Константы типа тега свойства Image (Гдиплусимагинг. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb565972b2dc8b8962e367c7d2f3c09b4f857382156538a83f7d6ee338c66ab6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977604"
---
# <a name="image-property-tag-type-constants"></a>Константы типа тега свойства Image

Метаданные изображения можно хранить и получать с помощью объекта [**пропертитем**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) . Член данных **типа** объекта **пропертитем** указывает тип данных значений, хранящихся в элементе данных значения этого же объекта **пропертитем** .

Следующие константы, определенные в Гдиплусимагинг. h, могут быть назначены члену данных **типа** объекта [**пропертитем**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) .



| Константа                                                                                                                                                                                                                                 | Описание                                                                                                                                                                                                                                                                                                                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PixelFormat4bppIndexed"></span><span id="pixelformat4bppindexed"></span><span id="PIXELFORMAT4BPPINDEXED"></span><dl> <dt>**PixelFormat4bppIndexed**</dt> </dl>         | Указывает, что форматом отводится 4 бита на пиксель и цвета индексированы.<br/>                                                                                                                                                                                                                                                                                                                       |
| <span id="PropertyTagTypeASCII"></span><span id="propertytagtypeascii"></span><span id="PROPERTYTAGTYPEASCII"></span><dl> <dt>**пропертитагтипеасЦии**</dt> </dl>                 | Указывает, что элемент данных **value** является СТРОКой ASCII, завершающейся нулем. Если задать для члена **типа** данных объекта [**пропертитем**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) значение пропертитагтипеасЦии, то в качестве элемента данных **длины** следует задать длину строки, включая знак завершения null. Например, строка `HELLO` будет иметь длину 6.<br/> |
| <span id="PropertyTagTypeByte"></span><span id="propertytagtypebyte"></span><span id="PROPERTYTAGTYPEBYTE"></span><dl> <dt>**пропертитагтипебите**</dt> </dl>                     | Указывает, что элемент данных **value** является массивом байтов.<br/>                                                                                                                                                                                                                                                                                                                |
| <span id="PropertyTagTypeLong"></span><span id="propertytagtypelong"></span><span id="PROPERTYTAGTYPELONG"></span><dl> <dt>**пропертитагтипелонг**</dt> </dl>                     | Указывает, что элемент данных **value** является массивом беззнаковых (32-разрядных) целых чисел.<br/>                                                                                                                                                                                                                                                                                      |
| <span id="PropertyTagTypeRational"></span><span id="propertytagtyperational"></span><span id="PROPERTYTAGTYPERATIONAL"></span><dl> <dt>**пропертитагтиператионал**</dt> </dl>     | Указывает, что элемент данных **value** является массивом пар длинных целых чисел без знака. Каждая пара представляет дробь; первое целое число — это числитель, а второе целое число — знаменатель.<br/>                                                                                                                                                                       |
| <span id="PropertyTagTypeShort"></span><span id="propertytagtypeshort"></span><span id="PROPERTYTAGTYPESHORT"></span><dl> <dt>**пропертитагтипешорт**</dt> </dl>                 | Указывает, что элемент данных **value** является массивом беззнаковых коротких (16-разрядных) целых чисел.<br/>                                                                                                                                                                                                                                                                                     |
| <span id="PropertyTagTypeSLONG"></span><span id="propertytagtypeslong"></span><span id="PROPERTYTAGTYPESLONG"></span><dl> <dt>**пропертитагтипеслонг**</dt> </dl>                 | Указывает, что элемент данных **value** является массивом длинных (32-разрядных) целых чисел.<br/>                                                                                                                                                                                                                                                                                        |
| <span id="PropertyTagTypeSRational"></span><span id="propertytagtypesrational"></span><span id="PROPERTYTAGTYPESRATIONAL"></span><dl> <dt>**пропертитагтипесратионал**</dt> </dl> | Указывает, что элемент данных **value** является массивом пар длинных целых чисел со знаком. Каждая пара представляет дробь; первое целое число — это числитель, а второе целое число — знаменатель.<br/>                                                                                                                                                                         |
| <span id="PropertyTagTypeUndefined"></span><span id="propertytagtypeundefined"></span><span id="PROPERTYTAGTYPEUNDEFINED"></span><dl> <dt>**пропертитагтипеундефинед**</dt> </dl> | Указывает, что элемент данных **value** представляет собой массив байтов, который может содержать значения любого типа данных. <br/>                                                                                                                                                                                                                                                                         |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Гдиплусимагинг. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Константы тега свойства Image](-gdiplus-constant-image-property-tag-constants.md)
</dt> <dt>

[Спецификации форматов файлов изображений](-gdiplus-constant-image-file-format-specifications.md)
</dt> <dt>

[Чтение и запись метаданных](-gdiplus-reading-and-writing-metadata-use.md)
</dt> </dl>

 

 

---
description: Файл значка может содержать несколько различных размеров одного изображения значка.
ms.assetid: 2d4d3689-a45a-4088-b466-e2b3bf4c8fb5
title: Атрибут элемента управления Иконсизе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cb615a53c589ebc2ad2cafb8a2ff7dec902865e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080673"
---
# <a name="iconsize-control-attribute"></a>Атрибут элемента управления Иконсизе

Файл значка может содержать несколько различных размеров одного изображения значка. Эти биты указывают, какой размер изображения значка нужно загрузить. Если ни один из битов не задан, будет загружен первый образ. Если задано только **msidbControlAttributesIconSize16** , загружается первое изображение 16x16. Если задан только параметр **msidbControlAttributesIconSize32** , загружается первое изображение размером 32x32. Если задано значение **msidbControlAttributesIconSize48** , загружается первое изображение 48x48.

## <a name="valid-controls"></a>Допустимые элементы управления

[CheckBox](checkbox-control.md)

[Значок](icon-control.md):

[PushButton](pushbutton-control.md)

[радиобуттонграуп](radiobuttongroup-control.md)

## <a name="value"></a>Значение



| Decimal | Шестнадцатеричный | Описание                          |
|---------|-------------|--------------------------------------|
| 2097152 | 0x00200000  | **msidbControlAttributesIconSize16** |
| 4194304 | 0x00400000  | **msidbControlAttributesIconSize32** |
| 6291456 | 0x00600000  | **msidbControlAttributesIconSize48** |



 

## <a name="remarks"></a>Комментарии

Чтобы задать этот атрибут для элемента управления, включите биты Иконсизе в столбец Attributes записи элемента управления в [таблице Control](control-table.md).

Если бит [FixedSize](fixedsize-control-attribute.md) не задан, загруженное изображение сжимается или растягивается в соответствии с элементом управления "значок". Если установлен бит [FixedSize](fixedsize-control-attribute.md) , а загруженное изображение меньше, чем элемент управления "значок", изображение отображается в центре элемента управления. Если установлен бит [FixedSize](fixedsize-control-attribute.md) , а загруженное изображение больше, чем элемент управления "значок", изображение уменьшается в соответствии с элементом управления.

См. раздел [атрибуты элементов управления](control-attributes.md) и элемент управления, которые необходимо создать в элементах [управления](controls.md).

 

 




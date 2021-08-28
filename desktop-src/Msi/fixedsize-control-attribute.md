---
description: Если установлен бит управления FixedSize, изображение обрезается или выравнивается по центру элемента управления без изменения его формы или размера.
ms.assetid: fb1ef0ba-5183-4708-a47d-26c83584df6c
title: Атрибут элемента управления FixedSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40094001115dc6e196e66075abe7ace7c93c8e715818ad34235f80caf8306a06
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649704"
---
# <a name="fixedsize-control-attribute"></a>Атрибут элемента управления FixedSize

Если установлен бит управления FixedSize, изображение обрезается или выравнивается по центру элемента управления без изменения его формы или размера.

Если этот бит не установлен, изображение растягивается для соответствия элементу управления.

## <a name="valid-controls"></a>Допустимые элементы управления

[Bitmap](bitmap-control.md)

[CheckBox](checkbox-control.md)

[Значок](icon-control.md):

[PushButton](pushbutton-control.md)

[радиобуттонграуп](radiobuttongroup-control.md)

## <a name="value"></a>Значение



| Decimal | Шестнадцатеричный | Константа                            |
|---------|-------------|-------------------------------------|
| 1048576 | 0x00100000  | **мсидбконтролаттрибутесфикседсизе** |



 

## <a name="remarks"></a>Remarks

Чтобы задать этот атрибут для элемента управления, включите бит FixedSize в столбец Attributes записи элемента управления в [таблице Control](control-table.md).

Установка бита FixedSize не влияет на [CheckBox](checkbox-control.md), [кнопка](pushbutton-control.md)или [радиобуттонграуп](radiobuttongroup-control.md) , если не задано ни [точечный рисунок](bitmap-control-attribute.md) , ни [значок](icon-control-attribute.md) .

Установка бита FixedSize не влияет на элемент управления "значок" или на значок, связанный со значком, если биты [иконсизе](iconsize-control-attribute.md) не заданы.

См. раздел [атрибуты элементов управления](control-attributes.md) и элемент управления, которые необходимо создать в элементах [управления](controls.md).

 

 




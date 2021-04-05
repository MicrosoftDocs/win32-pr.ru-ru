---
description: Если этот бит задан для элемента управления ProgressBar, он рисуется как ряд мелких прямоугольников. Если этот бит не задан, индикатор хода выполнения рисуется как один непрерывный прямоугольник.
ms.assetid: b2c43763-799c-4f09-b9f8-47a4a5f4faf3
title: Атрибут элемента управления Progress95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df2242dde671484274be946802ba4fd4c1cfd687
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911656"
---
# <a name="progress95-control-attribute"></a>Атрибут элемента управления Progress95

Если этот бит задан для [элемента управления ProgressBar](progressbar-control.md), он рисуется как ряд мелких прямоугольников. Если этот бит не задан, индикатор хода выполнения рисуется как один непрерывный прямоугольник.

## <a name="valid-controls"></a>Допустимые элементы управления

[ProgressBar](progressbar-control.md)

## <a name="value"></a>Значение



| Decimal | Шестнадцатеричный | Константа                             |
|---------|-------------|--------------------------------------|
| 65536   | 0x00010000  | **msidbControlAttributesProgress95** |



 

## <a name="remarks"></a>Remarks

Чтобы задать этот атрибут для элемента управления, включите бит Progress95 в столбец Attributes записи элемента управления в [таблице Control](control-table.md).

См. раздел [атрибуты элементов управления](control-attributes.md) и элемент управления, которые необходимо создать в элементах [управления](controls.md).

 

 




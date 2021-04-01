---
description: Если этот бит задан, элементы, перечисленные в элементе управления, отображаются в указанном порядке. Если бит не задан, элементы отображаются в алфавитном порядке.
ms.assetid: c55bf6bf-6625-47cb-867a-14b3ef8aea0a
title: Отсортированный атрибут элемента управления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a84af4b0683e35c66e159602b9ed2fe1b3005d8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072628"
---
# <a name="sorted-control-attribute"></a>Отсортированный атрибут элемента управления

Если этот бит задан, элементы, перечисленные в элементе управления, отображаются в указанном порядке. Если бит не задан, элементы отображаются в алфавитном порядке.

## <a name="valid-controls"></a>Допустимые элементы управления

[ComboBox](combobox-control.md)

 

[ListBox](listbox-control.md)

 

[Элемент управления ListView](listview-control.md)

## <a name="value"></a>Значение



| Decimal | Шестнадцатеричный | Константа                         |
|---------|-------------|----------------------------------|
| 65536   | 0x00010000  | **мсидбконтролаттрибутессортед** |



 

## <a name="remarks"></a>Комментарии

Чтобы отсортировать элементы в [ComboBox](combobox-control.md), включите сортированный бит в столбец Attributes [таблицы Control](control-table.md) и укажите порядок элементов в столбце Порядок [таблицы ComboBox](combobox-table.md).

Чтобы отсортировать элементы в [ListBox](listbox-control.md), включите сортированный бит в столбец Attributes [таблицы Control](control-table.md) и укажите порядок элементов в столбце Порядок [таблицы ComboBox](combobox-table.md).

Чтобы отсортировать элементы в [ListView](listview-control.md), включите сортированный бит в столбец Attributes [таблицы Control](control-table.md) и укажите порядок элементов в [таблице ComboBox](combobox-table.md).

См. раздел [Управление атрибутами](control-attributes.md) и [элементами управления](controls.md).

 

 




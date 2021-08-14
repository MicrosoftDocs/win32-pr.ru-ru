---
description: ICE95 проверяет таблицу управления и таблицу Ббконтрол, чтобы убедиться, что элементы управления объявления помещаются на все объявления.
ms.assetid: 8ba73536-65a5-4658-846c-76356f16b81c
title: ICE95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8f0f7d44554385c33648036f314406971193afc079b5aa8e72cf595695797ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119315264"
---
# <a name="ice95"></a>ICE95

ICE95 проверяет таблицу [управления](control-table.md) и [таблицу ббконтрол](bbcontrol-table.md) , чтобы убедиться, что элементы управления объявления помещаются на все объявления.

## <a name="result"></a>Результат

Если одно из следующих условий истинно, элемент управления "объявление" не поместится на объявление. ICE95 отправляет следующие предупреждения.



| Предупреждение ICE95                                                                                                                                                                                                              | Описание                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| Элемент Ббконтрол " \[ 1 \] . \[ 2 \] "в таблице ббконтрол не умещается во всех элементах управления" объявление "в таблице управления. Координата X превышает границу минимальной ширины элемента управления на стенде% s                   | Координата X элемента управления находится за пределами ширины объявления.                          |
| Элемент Ббконтрол " \[ 1 \] . \[ 2 \] "в таблице ббконтрол не умещается во всех элементах управления" объявление "в таблице управления. Координата Y превышает границу минимальной высоты элемента управления на стенде% s                  | Координата Y элемента управления находится ниже нижней границы объявления.                           |
| Элемент Ббконтрол " \[ 1 \] . \[ 2 \] "в таблице ббконтрол не умещается во всех элементах управления" объявление "в таблице управления. Координата X и ширина вместе превышают минимальную ширину элемента управления "объявление"% s   | Координата X элемента управления и ширина элемента управления выходят за пределы ширины объявления. |
| Элемент Ббконтрол " \[ 1 \] . \[ 2 \] "в таблице ббконтрол не умещается во всех элементах управления" объявление "в таблице управления. Координата Y и высота вместе превышают минимальную высоту элемента управления на стенде% s | Координата Y элемента управления плюс высота элемента управления ниже нижней границы объявления. |



 

## <a name="example"></a>Пример

ICE95 сообщает о следующих предупреждениях для примера:

``` syntax
The BBControl item 'billboard1.bbcontrol1' in the BBControl table does not fit in all the billboard controls in the Control table. The X coordinate exceeds the boundary of the minimum billboard control width 100
The BBControl item 'billboard1.bbcontrol2' in the BBControl table does not fit in all the billboard controls in the Control table. The Y coordinate exceeds the boundary of the minimum billboard control height 100
The BBControl item 'billboard1.bbcontrol3' in the BBControl table does not fit in all the billboard controls in the Control table. The X coordinate and the width combined together exceeds the minimum billboard control width 100
The BBControl item 'billboard1.bbcontrol4' in the BBControl table does not fit in all the billboard controls in the Control table. The Y coordinate and the height combined together exceeds the minimum billboard control height 100
```

Таблица управления (частичная) (частичная)



| Элемент  | Тип      | Ширина | Высота: |
|----------|-----------|-------|--------|
| control1 | Печат | 300   | 100    |
| Control2 | Печат | 100   | 300    |



 

[Таблица Ббконтрол](bbcontrol-table.md)



| Печат\_ | ббконтрол  | X   | Да   | Ширина | Высота: |
|-------------|------------|-----|-----|-------|--------|
| billboard1  | bbcontrol1 | 200 | 0   | 100   | 100    |
| billboard1  | bbcontrol2 | 0   | 200 | 100   | 100    |
| billboard1  | bbcontrol3 | 50  | 0   | 100   | 50     |
| billboard1  | bbcontrol4 | 0   | 50  | 50    | 100    |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Справочник по ICE](ice-reference.md)
</dt> </dl>

 

 




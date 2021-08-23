---
description: ICE10 проверяет, что состояние объявления дочерних компонентов совпадает с родительским компонентом.
ms.assetid: b0e0d837-245e-4c38-a7c4-06dda0eea25c
title: ICE10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80071bdb7f219904c03d7c6b5b947a1bd818af2c3ebc270b0bfb17f2cf185280
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581214"
---
# <a name="ice10"></a>ICE10

ICE10 проверяет, что состояние объявления дочерних компонентов совпадает с родительским компонентом.

Дочерняя функция может не запрещать объявление, пока ее родительский компонент допускает объявление. Таким образом, следующее сочетание родительских и дочерних атрибутов является недопустимым.

``` syntax
parent = msidbFeatureAttributesFavorAdvertise 
child = msidbFeatureAttributesDisallowAdvertise
```

Это сочетание является недопустимым, поскольку оно бы отключило родительский элемент всякий раз, когда ожидается объявление родителя. Однако обратная возможность разрешена. Дочерний элемент может быть помечен в качестве предпочтительного, когда родительский элемент помечен для запрета объявления.

Пользовательское действие ICE10 определяет состояние родительского и дочернего компонентов из столбца Attributes таблицы [Feature](feature-table.md) . Обратите внимание, что можно установить состояние компонента равным 0, и его родительский или дочерний набор будет использовать или запретить объявление.

## <a name="result"></a>Результат

ICE10 отправляет сообщение об ошибке, если столбец Attributes таблицы [Features](feature-table.md) содержит несоответствие в состоянии объявления.

## <a name="example"></a>Пример

ICE10 отправляет следующее сообщение об ошибке для приведенного примера.

``` syntax
Conflicting states, one favors, one disallows. Child: Word differs in advertise state 
from Parent: Office.
```

обратите внимание, что в этом примере Microsoft Excel и Microsoft Word являются дочерними функциями Microsoft Office.

Таблица [компонентов](feature-table.md) (частичная)



| Компонент | \_Родительский компонент функции | Атрибуты |
|---------|-----------------|------------|
| Office  | NULL            | 4          |
| Excel   | Office          | 4          |
| Word    | Office          | 8          |



 

В этом примере Word имеет значение запрет объявления, которое конфликтует с состоянием объявления родительского элемента, Office.

В некоторых случаях ICE10 отправляет следующую ошибку:

``` syntax
Parent feature: 'Parent' not found for child feature: 'Child'. This error means 
that for the child feature 'Child', the feature 'Parent' is not listed in the 
Feature table.
```

Это означает недопустимую ссылку на внешний ключ. Исправление заключается в том, чтобы дочерняя точка указывала на правильную родительскую функцию, или добавить запись для родительского компонента "Parent" в таблицу [компонентов](feature-table.md) .

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Справочник по ICE](ice-reference.md)
</dt> </dl>

 

 




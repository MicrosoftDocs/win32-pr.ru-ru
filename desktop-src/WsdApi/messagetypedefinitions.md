---
description: Создает константы C для таблиц схемы XML для типов сообщений.
ms.assetid: 0b322acb-3326-42a2-a852-07251585b314
title: Мессажетипедефинитионс, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a94fabdd2ceb2d32052a692f6daa1abba0a52f16d5d1b7dd0a4cef07d33de09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757084"
---
# <a name="messagetypedefinitions-element"></a>Мессажетипедефинитионс, элемент

Создает константы C для таблиц схемы XML для типов сообщений.

## <a name="usage"></a>Использование

``` syntax
<messageTypeDefinitions>
  child elements
</messageTypeDefinitions>
```

## <a name="attributes"></a>Атрибуты

Атрибуты отсутствуют.

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                   | Описание                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------|
| [**операцию**](operation.md)<br/> | Указывает операцию, для которой создается код.<br/> <br/>  |
| [**Порта**](porttype.md)<br/>   | Указывает тип порта, для которого создается код.<br/> <br/> |



### <a name="child-element-sequence"></a>Последовательность дочерних элементов

``` syntax
(
  portType?, 
  operation*
)
```

## <a name="parent-elements"></a>Родительские элементы



| Элемент                         | Описание                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**File**](file.md)<br/> | Выводит файл из генератора кода.<br/> <br/> |



## <a name="remarks"></a>Remarks

Этот элемент обычно используется в исходных файлах на языке C для предоставления таблиц схемы, объявленных с помощью [**мессажетипедекларатионс**](messagetypedeclarations.md).

## <a name="element-information"></a>Сведения об элементе



| Метка | Значение |
|-------------------------------------|---------------|
| Минимальная поддерживаемая система<br/> | Windows Vista |
| Может быть пустым                        | Да           |



 

 





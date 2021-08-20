---
description: Создает реализации для функций QueryInterface, AddRef и Release.
ms.assetid: 4b6abd0b-7570-4ae0-a727-cdb6cec58daf
title: Иункновндефинитионс, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f894c85138cb8567966ae154d68a99767d3f2058f5471fc5c5a3695a754de0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117920778"
---
# <a name="iunknowndefinitions-element"></a>Иункновндефинитионс, элемент

Создает реализации для функций QueryInterface, AddRef и Release.

## <a name="usage"></a>Использование

``` syntax
<IUnknownDefinitions
  proxyClass = "character_string"
  refCountVar = "character_string">
  child elements
</IUnknownDefinitions>
```

## <a name="attributes"></a>Атрибуты



| attribute                  | Тип                         | Обязательно       | Описание                                                |
|----------------------------|------------------------------|----------------|------------------------------------------------------------|
| **proxyClass**<br/>  | Символьная \_ строка<br/> | Да<br/> | Имя реализующего класса.<br/> <br/> |
| **рефкаунтвар**<br/> | Символьная \_ строка<br/> | Да<br/> | Имя переменной счетчика ссылок.<br/> <br/>  |



## <a name="child-elements"></a>Дочерние элементы



| Элемент                                   | Описание                                                                        |
|-------------------------------------------|------------------------------------------------------------------------------------|
| [**интерфейс**](interface.md)<br/> | Имя интерфейса, возвращаемого QueryInterface.<br/> <br/> |



### <a name="child-element-sequence"></a>Последовательность дочерних элементов

``` syntax
interface
```

## <a name="parent-elements"></a>Родительские элементы



| Элемент                         | Описание                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**File**](file.md)<br/> | Выводит файл из генератора кода.<br/> <br/> |



## <a name="element-information"></a>Сведения об элементе



| Метка | Значение |
|-------------------------------------|---------------|
| Минимальная поддерживаемая система<br/> | Windows Vista |
| Может быть пустым                        | нет            |



 

 





---
description: Создает реализации для функций QueryInterface, AddRef и Release.
ms.assetid: 4b6abd0b-7570-4ae0-a727-cdb6cec58daf
title: Иункновндефинитионс, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57ca92338e3dc97a12e04228510fc17eb2ef2483
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711708"
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



|                                     |               |
|-------------------------------------|---------------|
| Минимальная поддерживаемая система<br/> | Windows Vista |
| Может быть пустым                        | Нет            |



 

 





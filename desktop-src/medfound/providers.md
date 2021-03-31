---
description: Содержит список поставщиков трассировки для Мфтраце.
ms.assetid: ee483f0a-5a90-4150-ada4-0b63ae312523
title: Providers, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04e5aaedcd14d840cfdc0d85559f6a7981943593
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263495"
---
# <a name="providers-element"></a>Providers, элемент

Содержит список поставщиков трассировки для [мфтраце](mftrace.md).

## <a name="usage"></a>Использование

``` syntax
<providers>
  child elements
</providers>
```

## <a name="attributes"></a>Атрибуты

Атрибуты отсутствуют.

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                   | Описание                                                                                                      |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [**мфдетаурс**](mfdetours.md)<br/> | Указывает поставщик Media Foundation для обзора, который отслеживает вызовы API Media Foundation.<br/> <br/> |
| [**поставщики**](provider.md)<br/>   | Указывает поставщика трассировки (ETW или WPP).<br/> <br/>                                                  |



### <a name="child-element-sequence"></a>Последовательность дочерних элементов

``` syntax
(
  mfdetours?, 
  provider*
)
```

## <a name="parent-elements"></a>Родительские элементы

Нет родительских элементов.

## <a name="element-information"></a>Сведения об элементе



|              |     |
|--------------|-----|
| Может быть пустым | Да |



## <a name="see-also"></a>См. также

<dl> <dt>

[Файл конфигурации Мфтраце](mftrace-configuration-file.md)
</dt> </dl>

 

 





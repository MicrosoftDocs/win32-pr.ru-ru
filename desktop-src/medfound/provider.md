---
description: Указывает поставщика трассировки (ETW или WPP) для Мфтраце.
ms.assetid: 692cce3b-ebf5-4a49-8c37-48c8ef6caee7
title: элемент provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56ca319b686101766dacd79821ac6d9caf859cf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811573"
---
# <a name="provider-element"></a>элемент provider

Указывает поставщика трассировки (ETW или WPP) для [мфтраце](mftrace.md).

## <a name="usage"></a>Использование

``` syntax
<provider
  ID = "CDATA"
  level = "CDATA">
  child elements
</provider>
```

## <a name="attributes"></a>Атрибуты



| attribute            | Тип             | Обязательно       | Описание                                              |
|----------------------|------------------|----------------|----------------------------------------------------------|
| **Идентификатор**<br/>    | CDATA<br/> | Да<br/> | Имя или идентификатор GUID поставщика.<br/> <br/> |
| **level**<br/> | CDATA<br/> | Да<br/> | Уровень трассировки.<br/> <br/>                  |



## <a name="child-elements"></a>Дочерние элементы



| Элемент                               |
|---------------------------------------|
| [**This**](keyword.md)<br/> |



### <a name="child-element-sequence"></a>Последовательность дочерних элементов

``` syntax
keyword+
```

## <a name="parent-elements"></a>Родительские элементы



| Элемент                                   |
|-------------------------------------------|
| [**поставщик**](providers.md)<br/> |



## <a name="element-information"></a>Сведения об элементе



|              |     |
|--------------|-----|
| Может быть пустым | Нет  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Файл конфигурации Мфтраце](mftrace-configuration-file.md)
</dt> </dl>

 

 





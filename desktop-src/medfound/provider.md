---
description: Указывает поставщика трассировки (ETW или WPP) для Мфтраце.
ms.assetid: 692cce3b-ebf5-4a49-8c37-48c8ef6caee7
title: элемент provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d96b3015dddbcff74c09f77a1b6245d052fe034
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118449"
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

:::row:::
    :::column:::
        Может быть пустым
    :::column-end:::
    :::column span="2":::
        Нет
    :::column-end:::
:::row-end:::

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Файл конфигурации Мфтраце](mftrace-configuration-file.md)
</dt> </dl>

 

 





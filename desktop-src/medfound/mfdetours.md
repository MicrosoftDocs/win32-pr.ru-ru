---
description: Указывает поставщик Microsoft Media Foundation для обзора, который отслеживает вызовы API Media Foundation.
ms.assetid: 7c9abda9-7968-463c-b4a9-19b54012ef56
title: мфдетаурс, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3a0215d9d065bd27f0ad98ebea23abec8f7ecbbfc2223d522e0ddd1887990c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113644"
---
# <a name="mfdetours-element"></a>мфдетаурс, элемент

Указывает поставщик Microsoft Media Foundation для обзора, который отслеживает вызовы API Media Foundation.

## <a name="usage"></a>Использование

``` syntax
<mfdetours
  level = "CDATA">
  child elements
</mfdetours>
```

## <a name="attributes"></a>Атрибуты



| attribute            | Тип             | Обязательно       | Описание                             |
|----------------------|------------------|----------------|-----------------------------------------|
| **level**<br/> | CDATA<br/> | Да<br/> | Уровень трассировки.<br/> <br/> |



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
| [**providers**](providers.md)<br/> |



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

 

 





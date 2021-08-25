---
description: Задает ключевое слово для поставщика Мфтраце.
ms.assetid: 1ce4a5ee-c053-4d31-a984-dc11acebbf2a
title: элемент Keyword
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9df1f7a648e7861dc8d248141f051e9911c9cb93257f47fee5f2b4d2fd9d5469
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827554"
---
# <a name="keyword-element"></a>элемент Keyword

Задает ключевое слово для поставщика [мфтраце](mftrace.md) .

## <a name="usage"></a>Использование

``` syntax
<keyword
  ID = "CDATA"/>
```

## <a name="attributes"></a>Атрибуты



| attribute         | Тип             | Обязательно       | Описание                                             |
|-------------------|------------------|----------------|---------------------------------------------------------|
| **Идентификатор**<br/> | CDATA<br/> | Да<br/> | Имя или маска ключевого слова<br/> <br/> |



## <a name="child-elements"></a>Дочерние элементы

Нет дочерних элементов.

## <a name="parent-elements"></a>Родительские элементы

| Элемент                                   |
|-------------------------------------------|
| [**мфдетаурс**](mfdetours.md)<br/> |
| [**поставщики**](provider.md)<br/>   |



## <a name="remarks"></a>Remarks

Для элемента [**мфдетаурс**](mfdetours.md) допустимые ключевые слова перечислены в разделе [Ключевые слова мфтраце](mftrace-keywords.md).

Для элемента [**provider**](provider.md) ключевые слова зависят от поставщика событий. Для перечисления ключевых слов конкретного поставщика можно использовать служебную программу Wevtutil.exe.

## <a name="element-information"></a>Сведения об элементе

:::row:::
    :::column:::
        Может быть пустым
    :::column-end:::
    :::column span="2":::
        Да
    :::column-end:::
:::row-end:::

## <a name="see-also"></a>См. также

<dl> <dt>

[Файл конфигурации Мфтраце](mftrace-configuration-file.md)
</dt> <dt>

[Ключевые слова Мфтраце](mftrace-keywords.md)
</dt> </dl>

 

 





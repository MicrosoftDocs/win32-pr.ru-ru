---
description: Задает ключевое слово для поставщика Мфтраце.
ms.assetid: 1ce4a5ee-c053-4d31-a984-dc11acebbf2a
title: элемент Keyword
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ba871fea760ed3b604048ade2722afc0323e03b
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119379"
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

 

 





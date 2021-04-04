---
title: Атрибут Бвмоде VML
description: Атрибут Бвмоде VML
ms.assetid: 929daebb-c402-46a0-9abc-b91c4ebda7fa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f595159398e32fdb1c80ad5d949ef48758aea95
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792372"
---
# <a name="vml-bwmode-attribute"></a>Атрибут Бвмоде VML

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет, как будет отображаться фигура для устройств вывода черно-белого цвета. Read/write. [Вгблакквхитемоде](msdn-online-vml-vgblackwhitemode.md).

**Применимо к**:

[Фигурная](shape-element--vml.md)

**Синтаксис тега**

<v: *element* о:бвмоде = " *выражение* " >

**Замечания**

Если фигура печатается на черно-белом принтере или отображается в виде черно-белого представления в приложении, возможны несколько вариантов. Дополнительные сведения о значениях этого атрибута см. в разделе [вгблакквхитемоде](msdn-online-vml-vgblackwhitemode.md) . Значение по умолчанию — **Auto**.

Если указано значение **Auto** , [бвнормал](msdn-online-vml-bwnormal-attribute.md) используется для определения поведения обычных черно-белых выходных данных, а [бвпуре](msdn-online-vml-bwpure-attribute.md) используется для определения поведения для чистого вывода черно-белого цвета.

*Атрибут расширений Microsoft Office*

**Пример**

Черно-белый режим фигуры — **Auto**.


```HTML
   <v:rect id="myrect" fillcolor="red" o:bwmode="auto"
     style="top:1;left:1;width:20;height:20"/>
```



 

 
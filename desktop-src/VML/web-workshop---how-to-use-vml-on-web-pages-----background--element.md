---
title: Использование элемента Background
description: Использование элемента Background
ms.assetid: d11c1542-7f44-4ca7-9fb2-c8858fde3bc4
keywords:
- Веб-семинар, элемент Background
- Разработка веб-страниц, элемент Background
- Язык VML (VML), элемент Background
- VML (язык VML), элемент Background
- Векторная графика, элемент Background
- элемент Background
- Элементы VML, фон
- Фигуры VML, элемент Background
- Язык VML (VML), Настройка фона
- VML (язык VML), Настройка фона
- Векторная графика, Настройка фона
- Фигуры VML, Настройка фона
- Настройка фона
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fb4a694aa5458a0eae01fcbf577f72da8b8f54b7efda506423565aee362ce2f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512784"
---
# <a name="using-the-background-element"></a>Использование элемента Background

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

В этом разделе мы рассмотрим, как можно настроить фон веб-страницы с помощью `<background>` элемента, указанного в VML.

Как вы узнали из раздела [ `<fill>` use](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md) , можно поместить `<fill>` вложенный элемент внутри `<shape>` , `<shapetype>` или любого предопределенного элемента Shape, чтобы описать, как заполнить фигуру.

Аналогичным образом можно поместить `<fill>` вложенный элемент внутри `<background>` элемента, чтобы описать, как заполнять фон веб-страницы. Затем можно использовать атрибуты свойств `<fill>` вложенного элемента для настройки заливки, такие как [Градиентная заливка](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md), [узорная заливка](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md)или [Заливка рисунков](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md).

Например, для рисования фона, заполненного градиентом, можно ввести следующие строки в `<BODY>` области веб-страницы:


```HTML
<v:background fillcolor="red">
<v:fill type="gradient"/>
</v:background>
```





Дополнительные сведения об этом элементе см. в [спецификации VML](https://www.w3.org/TR/NOTE-VML#-toc416858389) .

 

 
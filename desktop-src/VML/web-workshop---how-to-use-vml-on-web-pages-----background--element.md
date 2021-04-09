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
ms.openlocfilehash: 9d0108b91f199fbc3bff1c28ebdf016bfba11957
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103890744"
---
# <a name="using-the-background-element"></a>Использование элемента Background

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

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

 

 
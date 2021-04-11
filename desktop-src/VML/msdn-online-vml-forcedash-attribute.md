---
title: Атрибут Форцедаш VML
description: Атрибут Форцедаш VML
ms.assetid: 659e99bb-16d9-425a-97b1-7767c065ec41
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5bcec4a694a6449412aa07ec69aa9a817aa917c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070314"
---
# <a name="vml-forcedash-attribute"></a>Атрибут Форцедаш VML

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет, используется ли пунктирная структура для рисования фигуры, если фигура не имеет линии или заливки. Read/write. **Вгтристате**.

**Применимо к**:

[Фигурная](shape-element--vml.md)

**Синтаксис тега**

<v: *element* о:форцедаш = " *выражение* " >

**Замечания**

Используется заполнителями Microsoft PowerPoint для рисования пунктирного контура, если нет линий и заливка для фигуры. Значение по умолчанию — **False**. Если **значение равно true**, то для обозначения заполнителя будет использоваться пунктирная структура.

*Атрибут расширений Microsoft Office*

**Пример**

Пунктирная линия будет использоваться для отрисовки фигуры при отсутствии линии или заливки.


```HTML
   <v:rect id=myrect fillcolor="red" o:forcedash="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 
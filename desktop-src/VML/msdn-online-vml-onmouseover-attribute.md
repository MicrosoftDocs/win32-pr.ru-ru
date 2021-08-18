---
title: Атрибут VML onmouseover
description: Атрибут VML onmouseover
ms.assetid: 68f0fa7a-0d22-4ede-8404-e007296960e5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d2bb65864987988996cfad710360fd908a5248c11857e8df1eb5a941b1b895b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999134"
---
# <a name="vml-onmouseover-attribute"></a>Атрибут VML onmouseover

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Активирует событие мыши для фигуры. Read/write. **Строка**.

**Применимо к**:

[Фигура](shape-element--vml.md)

**Синтаксис тега**

<v: *элемент* onmouseover = " *выражение* " >

**Замечания**

Событие «onmouseover» создается, когда указатель мыши находится на фигуре. Значение создается с помощью ключевого слова **this** (в качестве ссылки на объект), за которым следует синтаксис объектной модели. Например, чтобы изменить цвет заливки на красный, используйте следующую команду:

onmouseover = "this. FillColor = ' красный '"

Обратите внимание на использование одинарных и двойных кавычек для задания выражения.

*Стандартный атрибут VML*

**Пример**

Когда указатель мыши находится на фигуре, цвет заливки будет переключаться с красного на зеленый.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20"
   onmouseover='this.fillcolor="green"'>
   </v:rect>
```



[Пример атрибута onmouseover](/previous-versions/bb264088(v=vs.85)). (Требуется Microsoft Internet Explorer 5 или более поздней версии.)

 

 
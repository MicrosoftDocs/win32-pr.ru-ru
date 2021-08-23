---
title: Атрибут привязки VML V-Text-Anchor
description: Атрибут привязки VML V-Text-Anchor
ms.assetid: d6e2f60c-5cc7-4340-a9cd-b6c2b0b5b0be
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7c4b355aa4e56e3b0320200a092a66aa1f504b16be02f697e1335cd295627c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057702"
---
# <a name="vml-v-text-anchor-attribute"></a>Атрибут привязки VML V-Text-Anchor

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Определяет вертикальную привязку текста в текстовом поле. Read/write. **Строка**.

**Применимо к**:

[TextBox](msdn-online-vml-textbox-element.md)

**Синтаксис тега**

<v: *элемент* v-Text-Anchor = " *выражение* " >

**Замечания**

К этим значениям относятся следующие.

-   **Top** (по умолчанию)
-   **отчество**
-   **Нижний**
-   **сверху по центру**
-   **посередине по центру**
-   **внизу по центру**
-   **сверху — базовый план**
-   **снизу вверх**
-   **Верхний Центральный центр — базовый план**
-   **Нижняя-Центральная — базовый план**

Текст будет привязан к вертикальной точке в текстовом поле, как указано в значении атрибута. Выравнивание привязки к тексту становится очевидном только в том случае, если [MSO-Fit-Text-to-Shape](msdn-online-vml-mso-fit-text-to-shape-attribute.md) имеет **значение false**. Этот атрибут отличается от атрибута стиля **выравнивания по вертикали** , который используется для идеографических языков.

этот атрибут используется Microsoft Office для хранения данных в веб-документах, но не отображается в Microsoft Internet Explorer 5 или более поздней версии.

*Стандартный атрибут VML*

**Пример**

Текст выдается по нижнему краю текстового поля.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:10pt;left:10pt;width:50pt;height:50pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:textbox style="v-text-anchor:bottom" id="mytextbox">
   VML
   </v:textbox/>
   </v:shape>
```



 

 
---
title: Использование элемента TextBox
description: Использование элемента TextBox
ms.assetid: e0022722-a504-47da-aa3f-62aa7fb4ac4d
keywords:
- Веб-семинар, элемент TextBox
- Разработка веб-страниц, элемент TextBox
- Язык VML (VML), элемент TextBox
- VML (язык VML), элемент TextBox
- Векторная графика, элемент TextBox
- TextBox, элемент
- Элементы VML, текстовое поле
- Фигуры VML, элемент TextBox
- Язык VML (VML), присоединение текста
- VML (язык VML), присоединение текста
- Векторная графика, присоединение текста
- Фигуры VML, присоединение текста
- присоединение текста
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5388a359ca8cf4e320f95d708b4cf7055287d424
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488224"
---
# <a name="using-the-textbox-element"></a>Использование элемента TextBox

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

## <a name="examples"></a>Примеры:

Чтобы присоединить текст к прямоугольнику, можно ввести следующие строки в `<BODY>` области веб-страницы:


```HTML
<body>
<v:rect style='width:120pt;height:80pt;' fillcolor="red">
<v:textbox>
I'm attaching some text to this shape!!!
</v:textbox>
</v:rect>
</body>
```





Чтобы присоединить гиперссылку к скругленному прямоугольнику, который заполнен градиентом, можно ввести следующие строки в `<BODY>` области веб-страницы:

![textbox2.gif (1147 байт)](images/textbox2.gif)


```HTML
<body>
<v:roundrect style='width:80pt;height:30pt;' fillcolor="red">
<v:fill type="gradient" />
<v:textbox>
<a href="https://home.microsoft.com/"> Click here</a>
</v:textbox>
</v:roundrect>
</body>
```





Дополнительные сведения об этом элементе см. в [спецификации VML](https://www.w3.org/TR/NOTE-VML#-toc416858397) .

 

 
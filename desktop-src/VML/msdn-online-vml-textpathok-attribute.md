---
title: Атрибут Текстпасок VML
description: Атрибут Текстпасок VML
ms.assetid: 5d061258-1c4d-4391-81ce-13af90a4231c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06046a4f29c147ef109f0e4670d9965bab77a9fa
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103890692"
---
# <a name="vml-textpathok-attribute"></a>Атрибут Текстпасок VML

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет, будет ли отображаться текстовый путь. Read/write. **Вгтристате**.

**Применимо к**:

[Путь](msdn-online-vml-path-element.md)

**Синтаксис тега**

<v: *element* текстпасок = " *выражение* " >

**Синтаксис сценария**

*элемент* . текстпасок = "*выражение*"

*выражение* = *элемент*. текстпасок

**Замечания**

Если **значение равно false**, путь не может иметь текстовый путь. По умолчанию **False**. Этот атрибут должен иметь значение **true** для вывода текста по пути.

*Стандартный атрибут VML*

**Пример**

Фигура имеет текстовый путь. Текст "Hello VML" отображается в виде кривой в форме улыбающихся фигур.


```HTML
   <v:curve id="tc" style="position:relative"
   from="50px 100px" to="400px 100px"
   control1="200px 200px" control2="300px 200px">
   <v:stroke weight="1pt" color="blue"
   filltype="solid"/>
   <v:fill on="True" color="yellow" color2="green" type="gradient"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" id="mytp"
   style="font:normal normal normal 36pt Arial"
   fitpath="True" string="Hello VML"/>
   </v:curve>
```



 

 
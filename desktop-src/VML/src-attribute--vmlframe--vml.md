---
title: Атрибут src (Вмлфраме) (VML)
description: Атрибут src (Вмлфраме) (VML)
ms.assetid: 6ac7a3b5-3c1d-43a0-ab92-a03e3bd45733
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a9c3ec4849098c9469fba56f26d4c3dd514746
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337953"
---
# <a name="src-attribute-vmlframevml"></a>Атрибут src (Вмлфраме) (VML)

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет источник данных для кадра. Read/write. **Строка**.

**Применимо к**:

[вмлфраме](msdn-online-vml-vmlframe-element.md)

**Синтаксис тега**

<v: *элемент* src = " *выражение* " >

**Синтаксис сценария**

*element* . src = "*выражение*"

*выражение* = *элемент*. src

**Замечания**

Атрибут **src** может содержать следующие синтаксисы:

-   URL-адрес внешнего файла. Файл должен быть XML-файлом в следующем формате:
    ```HTML
       <xml xmlns:v = "urn:schemas-microsoft-com:vml">
       .
       .
       .
       </xml>
    ```

    

-   Внутри файла необходимо иметь одну или несколько фигур VML с допустимыми идентификаторами, на которые можно ссылаться с помощью этого синтаксиса:
    ```HTML
       filename#shapename
    ```

    

-   В следующей ссылке внешние файлы имеют расширение. VML, но можно использовать любое расширение:
    ```HTML
       external.vml#image01
    ```

    

-   Вы можете ссылаться на фигуру в том же файле с помощью следующего синтаксиса:
    ```HTML
       #shapename
    ```

    

Если значение **Clip** равно **false**, фигура будет масштабироваться в соответствии с размерами рамки. Если **значение равно true**, то все части фигуры, находящиеся за пределами рамки, не будут отображаться.

Обратите внимание, что [источник](origin-attribute--vmlframe--vml.md) и [Размер](size-attribute--vmlframe.md) не будут использоваться, если только значение **Clip** не равно **true**.

**Стандартный атрибут VML**

**Пример**

Изображение, определенное во внешнем файле, будет обрезано.


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 
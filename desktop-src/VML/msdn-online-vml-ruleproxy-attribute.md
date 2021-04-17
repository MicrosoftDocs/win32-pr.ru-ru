---
title: Атрибут Рулепрокси VML
description: Атрибут Рулепрокси VML
ms.assetid: 040e80f8-65b6-491d-812d-421800801374
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50c76116fc1f31c379f15c3229fcbe70dc7938f7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105672395"
---
# <a name="vml-ruleproxy-attribute"></a>Атрибут Рулепрокси VML

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет, будет ли использоваться прокси-сервер для обработчика правил. Read/write. **Вгтристате**.

**Применимо к**:

[Фигурная](shape-element--vml.md)

**Синтаксис тега**

<v: *element* рулепрокси = " *выражение* " >

**Замечания**

Значение по умолчанию равно **False**. Если задано **значение true**, используется прокси-сервер.

*Атрибут расширений Microsoft Office*

**Пример**

Для обработки фигуры используется прокси-сервер.


```HTML
   <v:rect id=myrect fillcolor="red" ruleproxy="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 
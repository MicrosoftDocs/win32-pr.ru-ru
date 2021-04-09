---
title: Атрибут Преферрелативе VML
description: Атрибут Преферрелативе VML
ms.assetid: 7de616e8-4fc3-4bcb-8e5e-ea153d6d4b54
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fa425321c1937c4df1bb766c554dbd73cc384b3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070098"
---
# <a name="vml-preferrelative-attribute"></a>Атрибут Преферрелативе VML

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет, сохраняется ли исходный размер объекта после переформатирования. Read/write. **Вгтристате**.

**Применимо к**:

[Фигурная](shape-element--vml.md)

**Синтаксис тега**

<v: *element* о:преферрелативе = " *выражение* " >

**Замечания**

По умолчанию **False**. Если **значение — true**, будет сохранен исходный размер объекта, а изменение размера будет основано на проценте от этого исходного размера. В противном случае при каждом изменении размера будет сброшен масштаб в 100%.

*Атрибут расширений Microsoft Office*

**Пример**

При изменении размера фигуры исходный размер не будет сохранен.


```HTML
   <v:rect id=myrect fillcolor="red" preferrelative="False"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 
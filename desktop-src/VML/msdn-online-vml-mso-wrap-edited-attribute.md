---
title: VML MSO-Wrap-изменяемый атрибут
description: VML MSO-Wrap-изменяемый атрибут
ms.assetid: cb0e8618-e649-4a3c-9433-2be77c4b65f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a272a56b57d82ca0fee9f69fbde2757316439fd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105672317"
---
# <a name="vml-mso-wrap-edited-attribute"></a>VML MSO-Wrap-изменяемый атрибут

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет, настроены ли координаты перетекания пользователем. Read/write. **Вгтристате**.

**Применимо к**:

[Фигурная](shape-element--vml.md)

**Синтаксис тега**

<v: Style *элемента* = "MSO-Wrap-Edited: *Expression* " >

**Замечания**

Если координаты перетекания создаются редактором, этот атрибут имеет **значение true**. в противном случае они были настроены пользователем.

*Атрибут расширений Microsoft Office*

**Пример**

Координаты обтекания фигуры были созданы редактором фигур.


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-edited:True"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



 

 
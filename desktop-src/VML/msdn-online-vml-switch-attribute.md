---
title: Атрибут переключателя VML
description: Атрибут переключателя VML
ms.assetid: fc099c0a-6789-41e8-ab08-36f4fd2d3bfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db2205f83449b09c22314c81ed460bee8410a3873e8f5550c073d7f3a1c1e8c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118123896"
---
# <a name="vml-switch-attribute"></a>Атрибут переключателя VML

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

Определяет, меняются ли направления обработчиков. Read/write. **Вгтристате**.

**Применимо к**:

[H](msdn-online-vml-h-element.md) (вложенный элемент [дескрипторов](msdn-online-vml-handles-element.md))

**Синтаксис тега**

<v: Switch *элемента* = " *выражение* " >

**Замечания**

Если **значение равно true**, то маркер переключается между направлениями x и y, если размер фигуры превышает ширину. Значение по умолчанию равно **False**.

Этот атрибут используется для фигур с поведением растяжения Лимо.

*Стандартный атрибут VML*

 

 
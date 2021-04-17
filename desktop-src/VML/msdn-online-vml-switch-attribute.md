---
title: Атрибут переключателя VML
description: Атрибут переключателя VML
ms.assetid: fc099c0a-6789-41e8-ab08-36f4fd2d3bfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9d102d6af20e698d8ec281cb1be6fae9690de4e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105672292"
---
# <a name="vml-switch-attribute"></a>Атрибут переключателя VML

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет, меняются ли направления обработчиков. Read/write. **Вгтристате**.

**Применимо к**:

[H](msdn-online-vml-h-element.md) (вложенный элемент [дескрипторов](msdn-online-vml-handles-element.md))

**Синтаксис тега**

<v: Switch *элемента* = " *выражение* " >

**Замечания**

Если **значение равно true**, то маркер переключается между направлениями x и y, если размер фигуры превышает ширину. Значение по умолчанию равно **False**.

Этот атрибут используется для фигур с поведением растяжения Лимо.

*Стандартный атрибут VML*

 

 
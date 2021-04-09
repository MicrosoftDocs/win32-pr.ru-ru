---
title: Атрибут Matrix (асимметрия) (VML)
description: Атрибут Matrix (асимметрия) (VML)
ms.assetid: 8d039865-2261-458b-8edf-01374af65cea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8327acfebfe4d968e673060f2f3cbef69d3e9db6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070528"
---
# <a name="matrix-attribute-skewvml"></a>Атрибут Matrix (асимметрия) (VML)

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет преобразование "Перспектива" для наклона. Read/write. **Строка**.

**Применимо к**:

[Отклонение](msdn-online-vml-skew-element.md)

**Синтаксис тега**

<o: *элемент* Matrix = " *выражение* " >

**Синтаксис сценария**

*element* . Matrix = "*выражение*"

*выражение* = *элемент*. Matrix

**Замечания**

Матрица представляет собой строку в форме "скскс, СКСИ, Сикс, сии, px, корректировка", где s — масштаб, p — перспектива, а x и y — значения x и y. Если значение [offset](offset-attribute--skew--vml.md) в абсолютных единицах, то числа px и корректировки находятся в ЕС ^-1 [единиц](msdn-online-vml-units.md) (в противном случае это обратная часть размера фигуры). Значение по умолчанию — "1, 0, 0, 1, 0, 0".

*Атрибут расширений Microsoft Office*

 

 
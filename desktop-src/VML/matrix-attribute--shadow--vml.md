---
title: Атрибут Matrix (тень) (VML)
description: Атрибут Matrix (тень) (VML)
ms.assetid: 29bebd2f-7f66-4883-8c12-57fef4a0ac9e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d599aa817e87481aefdec43dbe345b7235fc54bd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413568"
---
# <a name="matrix-attribute-shadowvml"></a>Атрибут Matrix (тень) (VML)

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Определяет преобразование перспективы для тени. Read/write. **Строка**.

**Применимо к**:

[Shadow](msdn-online-vml-shadow-element.md)

**Синтаксис тега**

<v: *элемент* Matrix = " *выражение* " >

**Синтаксис сценария**

*element* . Matrix = "*выражение*"

*выражение* = *элемент*. Matrix

**Замечания**

Матрица преобразования перспективы в форме "скскс, СКСИ, Сикс, сии, px, корректировка", где s = масштаб и p = перспектива. Если значение offset в абсолютных единицах, то px, корректировка производится в 1 или единицах ЕС. в противном случае это обратная часть размера фигуры.

*Стандартный атрибут VML*

 

 
---
title: Атрибут Matrix (тень) (VML)
description: Атрибут Matrix (тень) (VML)
ms.assetid: 29bebd2f-7f66-4883-8c12-57fef4a0ac9e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6124005ef3202e11dc8a4e7eeeaacba8e87e9c3a7cb3a1dd1eee55c595e40ecb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057932"
---
# <a name="matrix-attribute-shadowvml"></a>Атрибут Matrix (тень) (VML)

в этом разделе описывается функция VML, которая является устаревшей по отношению к Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). сведения, рекомендации и рекомендации относительно текущей версии Windows Internet explorer см. в [центре разработчиков internet explorer](https://msdn.microsoft.com/ie/).

 

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

 

 
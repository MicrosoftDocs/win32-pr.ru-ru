---
title: Атрибут Алсреф (Имажедата) (VML)
description: Атрибут Алсреф (Имажедата) (VML)
ms.assetid: c55ede90-3d57-4f27-9940-1fe4751cef71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 004625d769c12e67de024bf537ee04c377a18c8c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070190"
---
# <a name="althref-attribute-imagedatavml"></a>Атрибут Алсреф (Имажедата) (VML)

В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.

> [!Note]  
> По состоянию на Декабрь 2011 этот раздел был архивирован. В результате он больше не поддерживается. Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/). Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).

 

Указывает альтернативную ссылку для изображения. Read/write. **Строка**.

**Применимо к**:

[ImageData](msdn-online-vml-imagedata-element.md)

**Синтаксис тега**

<v: *element* о:алсреф = " *выражение* " >

**Синтаксис сценария**

*element* . алсреф = "*выражение*"

*выражение* = *element*. алсреф

**Замечания**

Поддерживает сохранение данных PICT через HTML переносе. При записи в формате HTML альтернативное представление (то есть исходные данные PICT, если файл был создан из Macintosh) сохраняется. При чтении HTML **алсреф** имеет приоритет над **src**.

*Атрибут расширений Microsoft Office*

 

 
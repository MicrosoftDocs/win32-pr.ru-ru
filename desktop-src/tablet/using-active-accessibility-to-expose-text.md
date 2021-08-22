---
description: Общие сведения об использовании Active Accessibility для представления текста.
ms.assetid: c04ade90-5f17-4e16-b82b-c99230000954
title: Использование Active Accessibility для представления текста
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 247d78149b82d15eb7c2dbd4ac2b2463d53c5d454dcb7877906197661de36ce4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119334794"
---
# <a name="using-active-accessibility-to-expose-text"></a>Использование Active Accessibility для представления текста

Приложения могут использовать Microsoft Active Accessibility для предоставления текста. Однако интерфейс [**IAccessible**](/windows/win32/api/oleacc/nn-oleacc-iaccessible) , определенный более ранними версиями Active Accessibility, не оптимизирован для предоставления больших объемов форматированного текста. Более поздние версии определяют интерфейсы, оптимизированные для предоставления больших объемов текста и текстовых атрибутов.

Чтобы предоставить большой объем текста, создайте отдельные объекты модели COM, поддерживающие [**IAccessible**](/windows/win32/api/oleacc/nn-oleacc-iaccessible)или дочерние элементы, для представления каждого выполнения текста. Запуск — это строка или часть строки, которая использует то же самое форматирование.

Active Accessibility предоставляет только текст и его расположение, но не имеет механизма для предоставления форматирования текста. Несмотря на эти ограничения, некоторые программы используют Active Accessibility для предоставления текста. например, Microsoft Internet Explorer и Microsoft Visual Studio используют Active Accessibility для предоставления больших объемов текста.

Дополнительные сведения о предоставлении текста с помощью Active Accessibility см. в разделе [Специальные возможности](../accessibility/accessibility.md).

 

 

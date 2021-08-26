---
title: Fragments
description: Fragments
ms.assetid: bc400251-32c4-4477-ba0c-a0046fe85327
keywords:
- OpenGL, фрагменты
- Конвейер обработки OpenGL, фрагменты
- фрагменты OpenGL
- фрамебуфферс, фрагменты, изменяющие Пиксели
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ab5d4124445455e518e4f091730e6e38e899442785b9f86ef73a230b99fbd41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082414"
---
# <a name="fragments"></a>Fragments

Фрагмент, созданный путем растрирования, изменяет соответствующий пиксель в буфера кадров только в том случае, если он проходит следующие тесты:

-   [Тестирование владения пикселями](pixel-ownership-test.md)
-   [Ножницное тестирование](scissor-test.md)
-   [Альфа-тест](alpha-test.md)
-   [Тест набора элементов](stencil-test.md)
-   [Тест буфера глубины](depth-buffer-test.md)

При передаче данные фрагмента могут заменить существующие значения буфера кадров или объединить его с существующими данными в буфера кадров в зависимости от состояния определенных режимов. Фрагмент можно объединить с данными в буфера кадров, выполнив следующие действия.

-   [Смешения](blending.md)
-   [Сглаживания](dithering.md)
-   [Логические операции](logical-operations.md)

 

 





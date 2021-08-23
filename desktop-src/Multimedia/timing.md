---
title: время (Windows мультимедиа)
description: Временные свойства
ms.assetid: 9ab284c7-eebc-4b44-b9e1-cc95efde22c1
keywords:
- Дравдиб, время
- Функция Дравдибтиме
- Дравдиб, отладка
- Отладка Дравдиб
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bc4324de5336a00b246ad644794ce8d0b3491bb644f34e8fc22dc8a7e460ba1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688084"
---
# <a name="timing-windows-multimedia"></a>время (Windows мультимедиа)

В рамках отладки приложения можно получить сведения о количестве времени, необходимого для выполнения повторяющихся операций Дравдиб. Функция [**дравдибтиме**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) возвращает сведения о времени для следующих операций:

-   Рисование точечного рисунка
-   Распаковка точечного рисунка
-   Сглаживание точечного рисунка
-   Растяжение растрового изображения
-   Передача точечного рисунка с помощью функции [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt)
-   Передача точечного рисунка с помощью функции [**стретчдибитс**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits)

После получения набора значений [**дравдибтиме**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) сбрасывает количество и значение для каждой операции.

Функция [**дравдибтиме**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) доступна только в отладочной версии функций дравдиб.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Рендеринг изображений](image-rendering.md)
</dt> </dl>

 

 

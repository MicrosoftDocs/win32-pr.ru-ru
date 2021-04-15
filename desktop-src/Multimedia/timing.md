---
title: Время (мультимедиа Windows)
description: Временные свойства
ms.assetid: 9ab284c7-eebc-4b44-b9e1-cc95efde22c1
keywords:
- Дравдиб, время
- Функция Дравдибтиме
- Дравдиб, отладка
- Отладка Дравдиб
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adddd43ff5067d08334a40f2e52e79109c8a8bb7
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104488754"
---
# <a name="timing-windows-multimedia"></a>Время (мультимедиа Windows)

В рамках отладки приложения можно получить сведения о количестве времени, необходимого для выполнения повторяющихся операций Дравдиб. Функция [**дравдибтиме**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) возвращает сведения о времени для следующих операций:

-   Рисование точечного рисунка
-   Распаковка точечного рисунка
-   Сглаживание точечного рисунка
-   Растяжение растрового изображения
-   Передача точечного рисунка с помощью функции [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt)
-   Передача точечного рисунка с помощью функции [**стретчдибитс**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits)

После получения набора значений [**дравдибтиме**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) сбрасывает количество и значение для каждой операции.

Функция [**дравдибтиме**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) доступна только в отладочной версии функций дравдиб.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Рендеринг изображений](image-rendering.md)
</dt> </dl>

 

 

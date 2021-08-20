---
description: Вы можете использовать сообщение WM \_ Paint для выполнения рисования, необходимого для отображения информации.
ms.assetid: cc56745f-95d0-4607-a206-1e7ed7109bf0
title: Использование сообщения WM_PAINT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1969d5aae7e64ad74d8070c7515daa6e9e782135ce0af54b49c7faab07f5d34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119037452"
---
# <a name="using-the-wm_paint-message"></a>Использование сообщения WM \_ Paint

Вы можете использовать сообщение [**WM \_ Paint**](wm-paint.md) для выполнения рисования, необходимого для отображения информации. Поскольку система отправляет сообщения WM \_ Paint в приложение при необходимости обновления окна или при явном запросе обновления, можно консолидировать код для рисования в процедуре окна приложения. Этот код можно использовать каждый раз, когда приложение должно рисовать либо новую, либо существующую информацию.

В следующих разделах показаны различные способы использования \_ сообщения WM Paint для рисования в окне:

-   [Рисование в клиентской области](drawing-in-the-client-area.md)
-   [Перерисовка всей клиентской области](redrawing-the-entire-client-area.md)
-   [Перерисовка в регионе обновления](redrawing-in-the-update-region.md)
-   [Идет недействительность клиентской области](invalidating-the-client-area.md)
-   [Рисование окна с минимальным объемом](drawing-a-minimized-window.md)
-   [Рисование пользовательского фона окна](drawing-a-custom-window-background.md)

 

 




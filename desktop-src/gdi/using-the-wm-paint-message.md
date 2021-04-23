---
description: Вы можете использовать сообщение WM \_ Paint для выполнения рисования, необходимого для отображения информации.
ms.assetid: cc56745f-95d0-4607-a206-1e7ed7109bf0
title: Использование сообщения WM_PAINT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba77246e04effc74de8158aef9bfc4aaf27471c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264125"
---
# <a name="using-the-wm_paint-message"></a><span data-ttu-id="aa4ce-103">Использование сообщения WM \_ Paint</span><span class="sxs-lookup"><span data-stu-id="aa4ce-103">Using the WM\_PAINT Message</span></span>

<span data-ttu-id="aa4ce-104">Вы можете использовать сообщение [**WM \_ Paint**](wm-paint.md) для выполнения рисования, необходимого для отображения информации.</span><span class="sxs-lookup"><span data-stu-id="aa4ce-104">You can use the [**WM\_PAINT**](wm-paint.md) message to carry out the drawing necessary for displaying information.</span></span> <span data-ttu-id="aa4ce-105">Поскольку система отправляет сообщения WM \_ Paint в приложение при необходимости обновления окна или при явном запросе обновления, можно консолидировать код для рисования в процедуре окна приложения.</span><span class="sxs-lookup"><span data-stu-id="aa4ce-105">Because the system sends WM\_PAINT messages to your application when your window must be updated or when you explicitly request an update, you can consolidate the code for drawing in your application's window procedure.</span></span> <span data-ttu-id="aa4ce-106">Этот код можно использовать каждый раз, когда приложение должно рисовать либо новую, либо существующую информацию.</span><span class="sxs-lookup"><span data-stu-id="aa4ce-106">You can then use this code whenever your application must draw either new or existing information.</span></span>

<span data-ttu-id="aa4ce-107">В следующих разделах показаны различные способы использования \_ сообщения WM Paint для рисования в окне:</span><span class="sxs-lookup"><span data-stu-id="aa4ce-107">The following sections show a variety of ways to use the WM\_PAINT message to draw in a window:</span></span>

-   [<span data-ttu-id="aa4ce-108">Рисование в клиентской области</span><span class="sxs-lookup"><span data-stu-id="aa4ce-108">Drawing in the Client Area</span></span>](drawing-in-the-client-area.md)
-   [<span data-ttu-id="aa4ce-109">Перерисовка всей клиентской области</span><span class="sxs-lookup"><span data-stu-id="aa4ce-109">Redrawing the Entire Client Area</span></span>](redrawing-the-entire-client-area.md)
-   [<span data-ttu-id="aa4ce-110">Перерисовка в регионе обновления</span><span class="sxs-lookup"><span data-stu-id="aa4ce-110">Redrawing in the Update Region</span></span>](redrawing-in-the-update-region.md)
-   [<span data-ttu-id="aa4ce-111">Идет недействительность клиентской области</span><span class="sxs-lookup"><span data-stu-id="aa4ce-111">Invalidating the Client Area</span></span>](invalidating-the-client-area.md)
-   [<span data-ttu-id="aa4ce-112">Рисование окна с минимальным объемом</span><span class="sxs-lookup"><span data-stu-id="aa4ce-112">Drawing a Minimized Window</span></span>](drawing-a-minimized-window.md)
-   [<span data-ttu-id="aa4ce-113">Рисование пользовательского фона окна</span><span class="sxs-lookup"><span data-stu-id="aa4ce-113">Drawing a Custom Window Background</span></span>](drawing-a-custom-window-background.md)

 

 




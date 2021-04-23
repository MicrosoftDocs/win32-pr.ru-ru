---
description: Функция GetDC используется для выполнения рисования, которое должно выполняться мгновенно, а не при \_ обработке сообщения WM Paint.
ms.assetid: 75525e26-72f5-4a58-a663-0bbdc2034759
title: Использование функции GetDC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98c018228eccbce7b487444341481165e24214b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985348"
---
# <a name="using-the-getdc-function"></a><span data-ttu-id="83dfb-103">Использование функции GetDC</span><span class="sxs-lookup"><span data-stu-id="83dfb-103">Using the GetDC Function</span></span>

<span data-ttu-id="83dfb-104">Функция [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) используется для выполнения рисования, которое должно выполняться мгновенно, а не при обработке сообщения [**WM \_ Paint**](wm-paint.md) .</span><span class="sxs-lookup"><span data-stu-id="83dfb-104">You use the [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) function to carry out drawing that must occur instantly rather than when a [**WM\_PAINT**](wm-paint.md) message is processing.</span></span> <span data-ttu-id="83dfb-105">Такая прорисовка обычно в ответ на какое-либо действие пользователем, например создание выделения или рисование с помощью мыши.</span><span class="sxs-lookup"><span data-stu-id="83dfb-105">Such drawing is usually in response to an action by the user, such as making a selection or drawing with the mouse.</span></span> <span data-ttu-id="83dfb-106">В таких случаях пользователь должен получить мгновенный отзыв и не должен вынужден прерывать выбор или прорисовку, чтобы приложение отображало результат.</span><span class="sxs-lookup"><span data-stu-id="83dfb-106">In such cases, the user should receive instant feedback and must not be forced to stop selecting or drawing in order for the application to display the result.</span></span> <span data-ttu-id="83dfb-107">В следующих разделах показано, как использовать GetDC для рисования в окне:</span><span class="sxs-lookup"><span data-stu-id="83dfb-107">The following sections show how to use GetDC to draw in a window:</span></span>

-   [<span data-ttu-id="83dfb-108">Рисование с помощью мыши</span><span class="sxs-lookup"><span data-stu-id="83dfb-108">Drawing with the Mouse</span></span>](drawing-with-the-mouse.md)
-   [<span data-ttu-id="83dfb-109">Рисование с интервалами времени</span><span class="sxs-lookup"><span data-stu-id="83dfb-109">Drawing at Timed Intervals</span></span>](drawing-at-timed-intervals.md)

 

 




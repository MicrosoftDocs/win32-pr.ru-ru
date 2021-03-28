---
description: Приложение делает недействительным часть окна и задает регион обновления с помощью функции Инвалидатерект или Инвалидатергн.
ms.assetid: ec8abb77-47bc-4198-9daf-f2ccb0864ccc
title: Идет непроверка и проверка региона обновления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ba895875f9ec1350b6eb28ccb8f1721df6999ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984949"
---
# <a name="invalidating-and-validating-the-update-region"></a><span data-ttu-id="f4278-103">Идет непроверка и проверка региона обновления</span><span class="sxs-lookup"><span data-stu-id="f4278-103">Invalidating and Validating the Update Region</span></span>

<span data-ttu-id="f4278-104">Приложение делает недействительным часть окна и задает регион обновления с помощью функции [**инвалидатерект**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) или [**инвалидатергн**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn) .</span><span class="sxs-lookup"><span data-stu-id="f4278-104">An application invalidates a portion of a window and sets the update region by using the [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) or [**InvalidateRgn**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn) function.</span></span> <span data-ttu-id="f4278-105">Эти функции добавляют указанный прямоугольник или область (в клиентских координатах) в область обновления, объединяя прямоугольник или область с любыми данными, которые система или приложение могли ранее добавить в регион обновления.</span><span class="sxs-lookup"><span data-stu-id="f4278-105">These functions add the specified rectangle or region (in client coordinates) to the update region, combining the rectangle or region with anything the system or the application may have previously added to the update region.</span></span>

<span data-ttu-id="f4278-106">Функции [**инвалидатерект**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) и [**инвалидатергн**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn) не создают сообщения [**WM \_ Paint**](wm-paint.md) .</span><span class="sxs-lookup"><span data-stu-id="f4278-106">The [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) and [**InvalidateRgn**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn) functions do not generate [**WM\_PAINT**](wm-paint.md) messages.</span></span> <span data-ttu-id="f4278-107">Вместо этого система накапливает изменения, внесенные этими функциями, и их собственные изменения, когда окно обрабатывает другие сообщения в очереди сообщений.</span><span class="sxs-lookup"><span data-stu-id="f4278-107">Instead, the system accumulates the changes made by these functions and its own changes while a window processes other messages in its message queue.</span></span> <span data-ttu-id="f4278-108">При накоплении изменений окно обрабатывает все изменения одновременно, вместо того чтобы обновлять биты и части на один шаг за раз.</span><span class="sxs-lookup"><span data-stu-id="f4278-108">By accumulating changes, a window processes all changes at once instead of updating bits and pieces one step at a time.</span></span>

<span data-ttu-id="f4278-109">Функции [**валидатерект**](/windows/desktop/api/Winuser/nf-winuser-validaterect) и [**валидатергн**](/windows/desktop/api/Winuser/nf-winuser-validatergn) проверяют часть окна путем удаления указанного прямоугольника или области из области обновления.</span><span class="sxs-lookup"><span data-stu-id="f4278-109">The [**ValidateRect**](/windows/desktop/api/Winuser/nf-winuser-validaterect) and [**ValidateRgn**](/windows/desktop/api/Winuser/nf-winuser-validatergn) functions validate a portion of the window by removing a specified rectangle or region from the update region.</span></span> <span data-ttu-id="f4278-110">Эти функции обычно используются, когда окно обновляет определенную часть экрана в области обновления перед получением сообщения [**WM \_ Paint**](wm-paint.md) .</span><span class="sxs-lookup"><span data-stu-id="f4278-110">These functions are typically used when the window has updated a specific part of the screen in the update region before receiving the [**WM\_PAINT**](wm-paint.md) message.</span></span>

 

 




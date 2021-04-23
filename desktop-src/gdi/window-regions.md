---
description: В дополнение к региону обновления каждое окно имеет видимую область, определяющую видимую для пользователя часть окна.
ms.assetid: 9d8beba1-93c0-437d-a138-76880a40bc79
title: Области окна
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02555339412c604f79f69294febbab524fc92a70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081178"
---
# <a name="window-regions"></a><span data-ttu-id="c0d00-103">Области окна</span><span class="sxs-lookup"><span data-stu-id="c0d00-103">Window Regions</span></span>

<span data-ttu-id="c0d00-104">В дополнение к региону обновления каждое окно имеет *видимую область* , определяющую видимую для пользователя часть окна.</span><span class="sxs-lookup"><span data-stu-id="c0d00-104">In addition to the update region, every window has a *visible region* that defines the window portion visible to the user.</span></span> <span data-ttu-id="c0d00-105">Система изменяет видимую область для окна всякий раз, когда размер окна изменяется, или при перемещении другого окна таким образом, что оно скрывает или представляет часть окна.</span><span class="sxs-lookup"><span data-stu-id="c0d00-105">The system changes the visible region for the window whenever the window changes size or whenever another window is moved such that it obscures or exposes a portion of the window.</span></span> <span data-ttu-id="c0d00-106">Приложения не могут изменять видимую область напрямую, но система автоматически использует видимую область для создания области обрезки для любого контекста устройства отображения, полученного для окна.</span><span class="sxs-lookup"><span data-stu-id="c0d00-106">Applications cannot change the visible region directly, but the system automatically uses the visible region to create the clipping region for any display device context retrieved for the window.</span></span>

<span data-ttu-id="c0d00-107">*Область обрезки* определяет, где система разрешает рисование.</span><span class="sxs-lookup"><span data-stu-id="c0d00-107">The *clipping region* determines where the system permits drawing.</span></span> <span data-ttu-id="c0d00-108">Когда приложение получает контекст устройства отображения с помощью функции [**бегинпаинт**](/windows/desktop/api/Winuser/nf-winuser-beginpaint), [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc)или [**жетдцекс**](/windows/desktop/api/Winuser/nf-winuser-getdcex) , система устанавливает область обрезки для контекста устройства на пересечение видимой области и региона обновления.</span><span class="sxs-lookup"><span data-stu-id="c0d00-108">When the application retrieves a display device context using the [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint), [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc), or [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) function, the system sets the clipping region for the device context to the intersection of the visible region and the update region.</span></span> <span data-ttu-id="c0d00-109">Приложения могут изменять область обрезки с помощью таких функций, как [**сетвиндовргн**](/windows/desktop/api/Winuser/nf-winuser-setwindowrgn), [**селектклиппас**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) и [**селектклипргн**](/windows/desktop/api/Wingdi/nf-wingdi-selectcliprgn), чтобы дополнительно ограничить рисование в определенной части области обновления.</span><span class="sxs-lookup"><span data-stu-id="c0d00-109">Applications can change the clipping region by using functions such as [**SetWindowRgn**](/windows/desktop/api/Winuser/nf-winuser-setwindowrgn), [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) and [**SelectClipRgn**](/windows/desktop/api/Wingdi/nf-wingdi-selectcliprgn), to further limit drawing to a particular portion of the update area.</span></span>

<span data-ttu-id="c0d00-110">Стили WS \_ клипчилдрен и WS \_ клипсиблингс дополнительно определяют, как система вычисляет видимую область для окна.</span><span class="sxs-lookup"><span data-stu-id="c0d00-110">The WS\_CLIPCHILDREN and WS\_CLIPSIBLINGS styles further specify how the system calculates the visible region for a window.</span></span> <span data-ttu-id="c0d00-111">Если окно имеет один или оба этих стиля, видимая область исключает все дочерние окна или одноуровневые окна (Windows с тем же родительским окном).</span><span class="sxs-lookup"><span data-stu-id="c0d00-111">If a window has one or both of these styles, the visible region excludes any child window or sibling windows (windows having the same parent window).</span></span> <span data-ttu-id="c0d00-112">Таким образом, прорисовка, которая в противном случае может поработать в этих окнах, будет всегда обрезана.</span><span class="sxs-lookup"><span data-stu-id="c0d00-112">Therefore, drawing that would otherwise intrude in these windows will always be clipped.</span></span>

 

 




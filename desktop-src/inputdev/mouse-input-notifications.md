---
title: Уведомления ввода с помощью мыши
description: .
ms.assetid: bf010650-4117-4ea5-8563-ca067d48f9cc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a9b8d7794d2122e89dc558331ac487e54b91e05
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410970"
---
# <a name="mouse-input-notifications"></a><span data-ttu-id="34036-103">Уведомления ввода с помощью мыши</span><span class="sxs-lookup"><span data-stu-id="34036-103">Mouse Input Notifications</span></span>

## <a name="in-this-section"></a><span data-ttu-id="34036-104">в этом разделе</span><span class="sxs-lookup"><span data-stu-id="34036-104">In This Section</span></span>

-   [<span data-ttu-id="34036-105">**WM \_ каптуречанжед**</span><span class="sxs-lookup"><span data-stu-id="34036-105">**WM\_CAPTURECHANGED**</span></span>](wm-capturechanged.md)
-   [<span data-ttu-id="34036-106">**WM \_ лбуттондблклк**</span><span class="sxs-lookup"><span data-stu-id="34036-106">**WM\_LBUTTONDBLCLK**</span></span>](wm-lbuttondblclk.md)
-   [<span data-ttu-id="34036-107">**WM \_ лбуттондовн**</span><span class="sxs-lookup"><span data-stu-id="34036-107">**WM\_LBUTTONDOWN**</span></span>](wm-lbuttondown.md)
-   [<span data-ttu-id="34036-108">**WM \_ лбуттонуп**</span><span class="sxs-lookup"><span data-stu-id="34036-108">**WM\_LBUTTONUP**</span></span>](wm-lbuttonup.md)
-   [<span data-ttu-id="34036-109">**WM \_ мбуттондблклк**</span><span class="sxs-lookup"><span data-stu-id="34036-109">**WM\_MBUTTONDBLCLK**</span></span>](wm-mbuttondblclk.md)
-   [<span data-ttu-id="34036-110">**WM \_ мбуттондовн**</span><span class="sxs-lookup"><span data-stu-id="34036-110">**WM\_MBUTTONDOWN**</span></span>](wm-mbuttondown.md)
-   [<span data-ttu-id="34036-111">**WM \_ мбуттонуп**</span><span class="sxs-lookup"><span data-stu-id="34036-111">**WM\_MBUTTONUP**</span></span>](wm-mbuttonup.md)
-   [<span data-ttu-id="34036-112">**WM \_ маусеактивате**</span><span class="sxs-lookup"><span data-stu-id="34036-112">**WM\_MOUSEACTIVATE**</span></span>](wm-mouseactivate.md)
-   [<span data-ttu-id="34036-113">**WM \_ маусеховер**</span><span class="sxs-lookup"><span data-stu-id="34036-113">**WM\_MOUSEHOVER**</span></span>](wm-mousehover.md)
-   [<span data-ttu-id="34036-114">**WM \_ маусехвхил**</span><span class="sxs-lookup"><span data-stu-id="34036-114">**WM\_MOUSEHWHEEL**</span></span>](wm-mousehwheel.md)
-   [<span data-ttu-id="34036-115">**WM \_ MOUSELEAVE**</span><span class="sxs-lookup"><span data-stu-id="34036-115">**WM\_MOUSELEAVE**</span></span>](wm-mouseleave.md)
-   [<span data-ttu-id="34036-116">**WM \_ MOUSEMOVE**</span><span class="sxs-lookup"><span data-stu-id="34036-116">**WM\_MOUSEMOVE**</span></span>](wm-mousemove.md)
-   [<span data-ttu-id="34036-117">**WM \_ маусевхил**</span><span class="sxs-lookup"><span data-stu-id="34036-117">**WM\_MOUSEWHEEL**</span></span>](wm-mousewheel.md)
-   [<span data-ttu-id="34036-118">**WM \_ нчиттест**</span><span class="sxs-lookup"><span data-stu-id="34036-118">**WM\_NCHITTEST**</span></span>](wm-nchittest.md)
-   [<span data-ttu-id="34036-119">**WM \_ нклбуттондблклк**</span><span class="sxs-lookup"><span data-stu-id="34036-119">**WM\_NCLBUTTONDBLCLK**</span></span>](wm-nclbuttondblclk.md)
-   [<span data-ttu-id="34036-120">**WM \_ нклбуттондовн**</span><span class="sxs-lookup"><span data-stu-id="34036-120">**WM\_NCLBUTTONDOWN**</span></span>](wm-nclbuttondown.md)
-   [<span data-ttu-id="34036-121">**WM \_ нклбуттонуп**</span><span class="sxs-lookup"><span data-stu-id="34036-121">**WM\_NCLBUTTONUP**</span></span>](wm-nclbuttonup.md)
-   [<span data-ttu-id="34036-122">**WM \_ нкмбуттондблклк**</span><span class="sxs-lookup"><span data-stu-id="34036-122">**WM\_NCMBUTTONDBLCLK**</span></span>](wm-ncmbuttondblclk.md)
-   [<span data-ttu-id="34036-123">**WM \_ нкмбуттондовн**</span><span class="sxs-lookup"><span data-stu-id="34036-123">**WM\_NCMBUTTONDOWN**</span></span>](wm-ncmbuttondown.md)
-   [<span data-ttu-id="34036-124">**WM \_ нкмбуттонуп**</span><span class="sxs-lookup"><span data-stu-id="34036-124">**WM\_NCMBUTTONUP**</span></span>](wm-ncmbuttonup.md)
-   [<span data-ttu-id="34036-125">**WM \_ нкмаусеховер**</span><span class="sxs-lookup"><span data-stu-id="34036-125">**WM\_NCMOUSEHOVER**</span></span>](wm-ncmousehover.md)
-   [<span data-ttu-id="34036-126">**WM \_ нкмауселеаве**</span><span class="sxs-lookup"><span data-stu-id="34036-126">**WM\_NCMOUSELEAVE**</span></span>](wm-ncmouseleave.md)
-   [<span data-ttu-id="34036-127">**WM \_ нкмаусемове**</span><span class="sxs-lookup"><span data-stu-id="34036-127">**WM\_NCMOUSEMOVE**</span></span>](wm-ncmousemove.md)
-   [<span data-ttu-id="34036-128">**WM \_ нкрбуттондблклк**</span><span class="sxs-lookup"><span data-stu-id="34036-128">**WM\_NCRBUTTONDBLCLK**</span></span>](wm-ncrbuttondblclk.md)
-   [<span data-ttu-id="34036-129">**WM \_ нкрбуттондовн**</span><span class="sxs-lookup"><span data-stu-id="34036-129">**WM\_NCRBUTTONDOWN**</span></span>](wm-ncrbuttondown.md)
-   [<span data-ttu-id="34036-130">**WM \_ нкрбуттонуп**</span><span class="sxs-lookup"><span data-stu-id="34036-130">**WM\_NCRBUTTONUP**</span></span>](wm-ncrbuttonup.md)
-   [<span data-ttu-id="34036-131">**WM \_ нкксбуттондблклк**</span><span class="sxs-lookup"><span data-stu-id="34036-131">**WM\_NCXBUTTONDBLCLK**</span></span>](wm-ncxbuttondblclk.md)
-   [<span data-ttu-id="34036-132">**WM \_ нкксбуттондовн**</span><span class="sxs-lookup"><span data-stu-id="34036-132">**WM\_NCXBUTTONDOWN**</span></span>](wm-ncxbuttondown.md)
-   [<span data-ttu-id="34036-133">**WM \_ нкксбуттонуп**</span><span class="sxs-lookup"><span data-stu-id="34036-133">**WM\_NCXBUTTONUP**</span></span>](wm-ncxbuttonup.md)
-   [<span data-ttu-id="34036-134">**WM \_ рбуттондблклк**</span><span class="sxs-lookup"><span data-stu-id="34036-134">**WM\_RBUTTONDBLCLK**</span></span>](wm-rbuttondblclk.md)
-   [<span data-ttu-id="34036-135">**WM \_ рбуттондовн**</span><span class="sxs-lookup"><span data-stu-id="34036-135">**WM\_RBUTTONDOWN**</span></span>](wm-rbuttondown.md)
-   [<span data-ttu-id="34036-136">**WM \_ рбуттонуп**</span><span class="sxs-lookup"><span data-stu-id="34036-136">**WM\_RBUTTONUP**</span></span>](wm-rbuttonup.md)
-   [<span data-ttu-id="34036-137">**WM \_ ксбуттондблклк**</span><span class="sxs-lookup"><span data-stu-id="34036-137">**WM\_XBUTTONDBLCLK**</span></span>](wm-xbuttondblclk.md)
-   [<span data-ttu-id="34036-138">**WM \_ ксбуттондовн**</span><span class="sxs-lookup"><span data-stu-id="34036-138">**WM\_XBUTTONDOWN**</span></span>](wm-xbuttondown.md)
-   [<span data-ttu-id="34036-139">**WM \_ ксбуттонуп**</span><span class="sxs-lookup"><span data-stu-id="34036-139">**WM\_XBUTTONUP**</span></span>](wm-xbuttonup.md)

 

 





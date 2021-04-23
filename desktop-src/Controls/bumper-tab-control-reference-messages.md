---
title: Управляющие сообщения вкладки
description: Управляющие сообщения вкладки
ms.assetid: a2993604-ba9c-46ff-9cf5-287c03295b4e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd2e0d3350d4b683ec93dcf59982cc1d5f33f6c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104000192"
---
# <a name="tab-control-messages"></a><span data-ttu-id="91481-103">Управляющие сообщения вкладки</span><span class="sxs-lookup"><span data-stu-id="91481-103">Tab Control Messages</span></span>

## <a name="in-this-section"></a><span data-ttu-id="91481-104">в этом разделе</span><span class="sxs-lookup"><span data-stu-id="91481-104">In This Section</span></span>

-   [<span data-ttu-id="91481-105">**\_АДЖУСТРЕКТ TCM**</span><span class="sxs-lookup"><span data-stu-id="91481-105">**TCM\_ADJUSTRECT**</span></span>](tcm-adjustrect.md)
-   [<span data-ttu-id="91481-106">**\_ДЕЛЕТЕАЛЛИТЕМС TCM**</span><span class="sxs-lookup"><span data-stu-id="91481-106">**TCM\_DELETEALLITEMS**</span></span>](tcm-deleteallitems.md)
-   [<span data-ttu-id="91481-107">**\_DELETEITEM TCM**</span><span class="sxs-lookup"><span data-stu-id="91481-107">**TCM\_DELETEITEM**</span></span>](tcm-deleteitem.md)
-   [<span data-ttu-id="91481-108">**\_ДЕСЕЛЕКТАЛЛ TCM**</span><span class="sxs-lookup"><span data-stu-id="91481-108">**TCM\_DESELECTALL**</span></span>](tcm-deselectall.md)
-   [<span data-ttu-id="91481-109">**\_ЖЕТКУРФОКУС TCM**</span><span class="sxs-lookup"><span data-stu-id="91481-109">**TCM\_GETCURFOCUS**</span></span>](tcm-getcurfocus.md)
-   [<span data-ttu-id="91481-110">**TCM \_**</span><span class="sxs-lookup"><span data-stu-id="91481-110">**TCM\_GETCURSEL**</span></span>](tcm-getcursel.md)
-   [<span data-ttu-id="91481-111">**\_ЖЕТЕКСТЕНДЕДСТИЛЕ TCM**</span><span class="sxs-lookup"><span data-stu-id="91481-111">**TCM\_GETEXTENDEDSTYLE**</span></span>](tcm-getextendedstyle.md)
-   [<span data-ttu-id="91481-112">**TCM \_ ImageList**</span><span class="sxs-lookup"><span data-stu-id="91481-112">**TCM\_GETIMAGELIST**</span></span>](tcm-getimagelist.md)
-   [<span data-ttu-id="91481-113">**TCM \_ DataItem**</span><span class="sxs-lookup"><span data-stu-id="91481-113">**TCM\_GETITEM**</span></span>](tcm-getitem.md)
-   [<span data-ttu-id="91481-114">**\_GETITEMCOUNT TCM**</span><span class="sxs-lookup"><span data-stu-id="91481-114">**TCM\_GETITEMCOUNT**</span></span>](tcm-getitemcount.md)
-   [<span data-ttu-id="91481-115">**\_ЖЕТИТЕМРЕКТ TCM**</span><span class="sxs-lookup"><span data-stu-id="91481-115">**TCM\_GETITEMRECT**</span></span>](tcm-getitemrect.md)
-   [<span data-ttu-id="91481-116">**TCM \_ ROWCOUNT**</span><span class="sxs-lookup"><span data-stu-id="91481-116">**TCM\_GETROWCOUNT**</span></span>](tcm-getrowcount.md)
-   [<span data-ttu-id="91481-117">**\_подсказки TCM**</span><span class="sxs-lookup"><span data-stu-id="91481-117">**TCM\_GETTOOLTIPS**</span></span>](tcm-gettooltips.md)
-   [<span data-ttu-id="91481-118">**\_ЖЕТУНИКОДЕФОРМАТ TCM**</span><span class="sxs-lookup"><span data-stu-id="91481-118">**TCM\_GETUNICODEFORMAT**</span></span>](tcm-getunicodeformat.md)
-   [<span data-ttu-id="91481-119">**\_ХИГХЛИГХТИТЕМ TCM**</span><span class="sxs-lookup"><span data-stu-id="91481-119">**TCM\_HIGHLIGHTITEM**</span></span>](tcm-highlightitem.md)
-   [<span data-ttu-id="91481-120">**\_HITTEST TCM**</span><span class="sxs-lookup"><span data-stu-id="91481-120">**TCM\_HITTEST**</span></span>](tcm-hittest.md)
-   [<span data-ttu-id="91481-121">**\_INSERTITEM TCM**</span><span class="sxs-lookup"><span data-stu-id="91481-121">**TCM\_INSERTITEM**</span></span>](tcm-insertitem.md)
-   [<span data-ttu-id="91481-122">**\_РЕМОВЕИМАЖЕ TCM**</span><span class="sxs-lookup"><span data-stu-id="91481-122">**TCM\_REMOVEIMAGE**</span></span>](tcm-removeimage.md)
-   [<span data-ttu-id="91481-123">**\_СЕТКУРФОКУС TCM**</span><span class="sxs-lookup"><span data-stu-id="91481-123">**TCM\_SETCURFOCUS**</span></span>](tcm-setcurfocus.md)
-   [<span data-ttu-id="91481-124">**\_СЕТКУРСЕЛ TCM**</span><span class="sxs-lookup"><span data-stu-id="91481-124">**TCM\_SETCURSEL**</span></span>](tcm-setcursel.md)
-   [<span data-ttu-id="91481-125">**\_СЕТЕКСТЕНДЕДСТИЛЕ TCM**</span><span class="sxs-lookup"><span data-stu-id="91481-125">**TCM\_SETEXTENDEDSTYLE**</span></span>](tcm-setextendedstyle.md)
-   [<span data-ttu-id="91481-126">**\_СЕТИМАЖЕЛИСТ TCM**</span><span class="sxs-lookup"><span data-stu-id="91481-126">**TCM\_SETIMAGELIST**</span></span>](tcm-setimagelist.md)
-   [<span data-ttu-id="91481-127">**\_СЕТИТЕМ TCM**</span><span class="sxs-lookup"><span data-stu-id="91481-127">**TCM\_SETITEM**</span></span>](tcm-setitem.md)
-   [<span data-ttu-id="91481-128">**\_СЕТИТЕМЕКСТРА TCM**</span><span class="sxs-lookup"><span data-stu-id="91481-128">**TCM\_SETITEMEXTRA**</span></span>](tcm-setitemextra.md)
-   [<span data-ttu-id="91481-129">**\_СЕТИТЕМСИЗЕ TCM**</span><span class="sxs-lookup"><span data-stu-id="91481-129">**TCM\_SETITEMSIZE**</span></span>](tcm-setitemsize.md)
-   [<span data-ttu-id="91481-130">**\_СЕТМИНТАБВИДС TCM**</span><span class="sxs-lookup"><span data-stu-id="91481-130">**TCM\_SETMINTABWIDTH**</span></span>](tcm-setmintabwidth.md)
-   [<span data-ttu-id="91481-131">**\_СЕТПАДДИНГ TCM**</span><span class="sxs-lookup"><span data-stu-id="91481-131">**TCM\_SETPADDING**</span></span>](tcm-setpadding.md)
-   [<span data-ttu-id="91481-132">**\_СЕТТУЛТИПС TCM**</span><span class="sxs-lookup"><span data-stu-id="91481-132">**TCM\_SETTOOLTIPS**</span></span>](tcm-settooltips.md)
-   [<span data-ttu-id="91481-133">**\_СЕТУНИКОДЕФОРМАТ TCM**</span><span class="sxs-lookup"><span data-stu-id="91481-133">**TCM\_SETUNICODEFORMAT**</span></span>](tcm-setunicodeformat.md)

 

 





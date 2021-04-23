---
title: Структуры представления списка
description: Структуры представления списка
ms.assetid: 12d77514-7281-4873-b456-252ff80ed7f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b603e9acd65448b3c4970aa9552f4d2b91ebccd
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "103820644"
---
# <a name="list-view-structures"></a><span data-ttu-id="a6c9c-103">Структуры представления списка</span><span class="sxs-lookup"><span data-stu-id="a6c9c-103">List View Structures</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a6c9c-104">в этом разделе</span><span class="sxs-lookup"><span data-stu-id="a6c9c-104">In This Section</span></span>

-   [<span data-ttu-id="a6c9c-105">**лвбкимаже**</span><span class="sxs-lookup"><span data-stu-id="a6c9c-105">**LVBKIMAGE**</span></span>](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea)
-   [<span data-ttu-id="a6c9c-106">**LVCOLUMN**</span><span class="sxs-lookup"><span data-stu-id="a6c9c-106">**LVCOLUMN**</span></span>](/windows/win32/api/commctrl/ns-commctrl-lvcolumna)
-   [<span data-ttu-id="a6c9c-107">**лвфиндинфо**</span><span class="sxs-lookup"><span data-stu-id="a6c9c-107">**LVFINDINFO**</span></span>](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa)
-   [<span data-ttu-id="a6c9c-108">**лвфутеринфо**</span><span class="sxs-lookup"><span data-stu-id="a6c9c-108">**LVFOOTERINFO**</span></span>](/windows/win32/api/commctrl/ns-commctrl-lvfooterinfo)
-   [<span data-ttu-id="a6c9c-109">**лвфутеритем**</span><span class="sxs-lookup"><span data-stu-id="a6c9c-109">**LVFOOTERITEM**</span></span>](/windows/win32/api/commctrl/ns-commctrl-lvfooteritem)
-   [<span data-ttu-id="a6c9c-110">**лвграуп**</span><span class="sxs-lookup"><span data-stu-id="a6c9c-110">**LVGROUP**</span></span>](/windows/win32/api/commctrl/ns-commctrl-lvgroup)
-   [<span data-ttu-id="a6c9c-111">**лвграупметрикс**</span><span class="sxs-lookup"><span data-stu-id="a6c9c-111">**LVGROUPMETRICS**</span></span>](/windows/win32/api/commctrl/ns-commctrl-lvgroupmetrics)
-   [<span data-ttu-id="a6c9c-112">**лвхиттестинфо**</span><span class="sxs-lookup"><span data-stu-id="a6c9c-112">**LVHITTESTINFO**</span></span>](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo)
-   [<span data-ttu-id="a6c9c-113">**лвинсертграупсортед**</span><span class="sxs-lookup"><span data-stu-id="a6c9c-113">**LVINSERTGROUPSORTED**</span></span>](/windows/win32/api/commctrl/ns-commctrl-lvinsertgroupsorted)
-   [<span data-ttu-id="a6c9c-114">**лвинсертмарк**</span><span class="sxs-lookup"><span data-stu-id="a6c9c-114">**LVINSERTMARK**</span></span>](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark)
-   [<span data-ttu-id="a6c9c-115">**лвитем**</span><span class="sxs-lookup"><span data-stu-id="a6c9c-115">**LVITEM**</span></span>](/windows/win32/api/commctrl/ns-commctrl-lvitema)
-   [<span data-ttu-id="a6c9c-116">**лвитеминдекс**</span><span class="sxs-lookup"><span data-stu-id="a6c9c-116">**LVITEMINDEX**</span></span>](/windows/win32/api/commctrl/ns-commctrl-lvitemindex)
-   [<span data-ttu-id="a6c9c-117">**лвсетинфотип**</span><span class="sxs-lookup"><span data-stu-id="a6c9c-117">**LVSETINFOTIP**</span></span>](/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip)
-   [<span data-ttu-id="a6c9c-118">**лвтилеинфо**</span><span class="sxs-lookup"><span data-stu-id="a6c9c-118">**LVTILEINFO**</span></span>](/windows/win32/api/commctrl/ns-commctrl-lvtileinfo)
-   [<span data-ttu-id="a6c9c-119">**лвтилевиевинфо**</span><span class="sxs-lookup"><span data-stu-id="a6c9c-119">**LVTILEVIEWINFO**</span></span>](/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo)
-   [<span data-ttu-id="a6c9c-120">**нмитемактивате**</span><span class="sxs-lookup"><span data-stu-id="a6c9c-120">**NMITEMACTIVATE**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate)
-   [<span data-ttu-id="a6c9c-121">**нмлиствиев**</span><span class="sxs-lookup"><span data-stu-id="a6c9c-121">**NMLISTVIEW**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmlistview)
-   [<span data-ttu-id="a6c9c-122">**нмлвкачехинт**</span><span class="sxs-lookup"><span data-stu-id="a6c9c-122">**NMLVCACHEHINT**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmlvcachehint)
-   [<span data-ttu-id="a6c9c-123">**нмлвкустомдрав**</span><span class="sxs-lookup"><span data-stu-id="a6c9c-123">**NMLVCUSTOMDRAW**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw)
-   [<span data-ttu-id="a6c9c-124">**нмлвдиспинфо**</span><span class="sxs-lookup"><span data-stu-id="a6c9c-124">**NMLVDISPINFO**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa)
-   [<span data-ttu-id="a6c9c-125">**нмлвемптимаркуп**</span><span class="sxs-lookup"><span data-stu-id="a6c9c-125">**NMLVEMPTYMARKUP**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmlvemptymarkup)
-   [<span data-ttu-id="a6c9c-126">**нмлвфиндитем**</span><span class="sxs-lookup"><span data-stu-id="a6c9c-126">**NMLVFINDITEM**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema)
-   [<span data-ttu-id="a6c9c-127">**нмлвжетинфотип**</span><span class="sxs-lookup"><span data-stu-id="a6c9c-127">**NMLVGETINFOTIP**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmlvgetinfotipa)
-   [<span data-ttu-id="a6c9c-128">**нмлвкэйдовн**</span><span class="sxs-lookup"><span data-stu-id="a6c9c-128">**NMLVKEYDOWN**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmlvkeydown)
-   [<span data-ttu-id="a6c9c-129">**NMLVLINK**</span><span class="sxs-lookup"><span data-stu-id="a6c9c-129">**NMLVLINK**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmlvlink)
-   [<span data-ttu-id="a6c9c-130">**нмлводстатечанже**</span><span class="sxs-lookup"><span data-stu-id="a6c9c-130">**NMLVODSTATECHANGE**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmlvodstatechange)
-   [<span data-ttu-id="a6c9c-131">**нмлвскролл**</span><span class="sxs-lookup"><span data-stu-id="a6c9c-131">**NMLVSCROLL**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmlvscroll)

 

 





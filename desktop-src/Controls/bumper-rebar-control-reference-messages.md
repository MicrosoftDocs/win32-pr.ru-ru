---
title: Управляющие сообщения главной панели
description: Управляющие сообщения главной панели
ms.assetid: 5fa1df55-0883-4b3b-bcde-7c40d574c792
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc43d8091b1a3808b98091b62ed8b7965f13bb9b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104081806"
---
# <a name="rebar-control-messages"></a><span data-ttu-id="70a49-103">Управляющие сообщения главной панели</span><span class="sxs-lookup"><span data-stu-id="70a49-103">Rebar Control Messages</span></span>

## <a name="in-this-section"></a><span data-ttu-id="70a49-104">в этом разделе</span><span class="sxs-lookup"><span data-stu-id="70a49-104">In This Section</span></span>

-   [<span data-ttu-id="70a49-105">**\_БЕГИНДРАГ RB**</span><span class="sxs-lookup"><span data-stu-id="70a49-105">**RB\_BEGINDRAG**</span></span>](rb-begindrag.md)
-   [<span data-ttu-id="70a49-106">**\_ДЕЛЕТЕБАНД RB**</span><span class="sxs-lookup"><span data-stu-id="70a49-106">**RB\_DELETEBAND**</span></span>](rb-deleteband.md)
-   [<span data-ttu-id="70a49-107">**\_ДРАГМОВЕ RB**</span><span class="sxs-lookup"><span data-stu-id="70a49-107">**RB\_DRAGMOVE**</span></span>](rb-dragmove.md)
-   [<span data-ttu-id="70a49-108">**\_ЕНДДРАГ RB**</span><span class="sxs-lookup"><span data-stu-id="70a49-108">**RB\_ENDDRAG**</span></span>](rb-enddrag.md)
-   [<span data-ttu-id="70a49-109">**\_ЖЕТБАНДБОРДЕРС RB**</span><span class="sxs-lookup"><span data-stu-id="70a49-109">**RB\_GETBANDBORDERS**</span></span>](rb-getbandborders.md)
-   [<span data-ttu-id="70a49-110">**\_ЖЕТБАНДКАУНТ RB**</span><span class="sxs-lookup"><span data-stu-id="70a49-110">**RB\_GETBANDCOUNT**</span></span>](rb-getbandcount.md)
-   [<span data-ttu-id="70a49-111">**\_ЖЕТБАНДИНФО RB**</span><span class="sxs-lookup"><span data-stu-id="70a49-111">**RB\_GETBANDINFO**</span></span>](rb-getbandinfo.md)
-   [<span data-ttu-id="70a49-112">**\_ЖЕТБАНДМАРГИНС RB**</span><span class="sxs-lookup"><span data-stu-id="70a49-112">**RB\_GETBANDMARGINS**</span></span>](rb-getbandmargins.md)
-   [<span data-ttu-id="70a49-113">**\_ЖЕТБАРХЕИГХТ RB**</span><span class="sxs-lookup"><span data-stu-id="70a49-113">**RB\_GETBARHEIGHT**</span></span>](rb-getbarheight.md)
-   [<span data-ttu-id="70a49-114">**\_ЖЕТБАРИНФО RB**</span><span class="sxs-lookup"><span data-stu-id="70a49-114">**RB\_GETBARINFO**</span></span>](rb-getbarinfo.md)
-   [<span data-ttu-id="70a49-115">**\_ЖЕТБККОЛОР RB**</span><span class="sxs-lookup"><span data-stu-id="70a49-115">**RB\_GETBKCOLOR**</span></span>](rb-getbkcolor.md)
-   [<span data-ttu-id="70a49-116">**\_ЖЕТКОЛОРСЧЕМЕ RB**</span><span class="sxs-lookup"><span data-stu-id="70a49-116">**RB\_GETCOLORSCHEME**</span></span>](rb-getcolorscheme.md)
-   [<span data-ttu-id="70a49-117">**\_ЖЕТДРОПТАРЖЕТ RB**</span><span class="sxs-lookup"><span data-stu-id="70a49-117">**RB\_GETDROPTARGET**</span></span>](rb-getdroptarget.md)
-   [<span data-ttu-id="70a49-118">**\_ЖЕТЕКСТЕНДЕДСТИЛЕ RB**</span><span class="sxs-lookup"><span data-stu-id="70a49-118">**RB\_GETEXTENDEDSTYLE**</span></span>](rb-getextendedstyle.md)
-   [<span data-ttu-id="70a49-119">**панель \_ RB**</span><span class="sxs-lookup"><span data-stu-id="70a49-119">**RB\_GETPALETTE**</span></span>](rb-getpalette.md)
-   [<span data-ttu-id="70a49-120">**RB \_**</span><span class="sxs-lookup"><span data-stu-id="70a49-120">**RB\_GETRECT**</span></span>](rb-getrect.md)
-   [<span data-ttu-id="70a49-121">**RB. \_ ROWCOUNT**</span><span class="sxs-lookup"><span data-stu-id="70a49-121">**RB\_GETROWCOUNT**</span></span>](rb-getrowcount.md)
-   [<span data-ttu-id="70a49-122">**\_ЖЕТРОВХЕИГХТ RB**</span><span class="sxs-lookup"><span data-stu-id="70a49-122">**RB\_GETROWHEIGHT**</span></span>](rb-getrowheight.md)
-   [<span data-ttu-id="70a49-123">**\_ЖЕТТЕКСТКОЛОР RB**</span><span class="sxs-lookup"><span data-stu-id="70a49-123">**RB\_GETTEXTCOLOR**</span></span>](rb-gettextcolor.md)
-   [<span data-ttu-id="70a49-124">**\_подсказки RB**</span><span class="sxs-lookup"><span data-stu-id="70a49-124">**RB\_GETTOOLTIPS**</span></span>](rb-gettooltips.md)
-   [<span data-ttu-id="70a49-125">**\_ЖЕТУНИКОДЕФОРМАТ RB**</span><span class="sxs-lookup"><span data-stu-id="70a49-125">**RB\_GETUNICODEFORMAT**</span></span>](rb-getunicodeformat.md)
-   [<span data-ttu-id="70a49-126">**\_HITTEST RB**</span><span class="sxs-lookup"><span data-stu-id="70a49-126">**RB\_HITTEST**</span></span>](rb-hittest.md)
-   [<span data-ttu-id="70a49-127">**\_ИДТОИНДЕКС RB**</span><span class="sxs-lookup"><span data-stu-id="70a49-127">**RB\_IDTOINDEX**</span></span>](rb-idtoindex.md)
-   [<span data-ttu-id="70a49-128">**\_ИНСЕРТБАНД RB**</span><span class="sxs-lookup"><span data-stu-id="70a49-128">**RB\_INSERTBAND**</span></span>](rb-insertband.md)
-   [<span data-ttu-id="70a49-129">**\_МАКСИМИЗЕБАНД RB**</span><span class="sxs-lookup"><span data-stu-id="70a49-129">**RB\_MAXIMIZEBAND**</span></span>](rb-maximizeband.md)
-   [<span data-ttu-id="70a49-130">**\_МИНИМИЗЕБАНД RB**</span><span class="sxs-lookup"><span data-stu-id="70a49-130">**RB\_MINIMIZEBAND**</span></span>](rb-minimizeband.md)
-   [<span data-ttu-id="70a49-131">**\_МОВЕБАНД RB**</span><span class="sxs-lookup"><span data-stu-id="70a49-131">**RB\_MOVEBAND**</span></span>](rb-moveband.md)
-   [<span data-ttu-id="70a49-132">**\_ПУШЧЕВРОН RB**</span><span class="sxs-lookup"><span data-stu-id="70a49-132">**RB\_PUSHCHEVRON**</span></span>](rb-pushchevron.md)
-   [<span data-ttu-id="70a49-133">**\_СЕТБАНДИНФО RB**</span><span class="sxs-lookup"><span data-stu-id="70a49-133">**RB\_SETBANDINFO**</span></span>](rb-setbandinfo.md)
-   [<span data-ttu-id="70a49-134">**\_СЕТБАНДВИДС RB**</span><span class="sxs-lookup"><span data-stu-id="70a49-134">**RB\_SETBANDWIDTH**</span></span>](rb-setbandwidth.md)
-   [<span data-ttu-id="70a49-135">**\_СЕТБАРИНФО RB**</span><span class="sxs-lookup"><span data-stu-id="70a49-135">**RB\_SETBARINFO**</span></span>](rb-setbarinfo.md)
-   [<span data-ttu-id="70a49-136">**\_СЕТБККОЛОР RB**</span><span class="sxs-lookup"><span data-stu-id="70a49-136">**RB\_SETBKCOLOR**</span></span>](rb-setbkcolor.md)
-   [<span data-ttu-id="70a49-137">**\_СЕТКОЛОРСЧЕМЕ RB**</span><span class="sxs-lookup"><span data-stu-id="70a49-137">**RB\_SETCOLORSCHEME**</span></span>](rb-setcolorscheme.md)
-   [<span data-ttu-id="70a49-138">**\_СЕТЕКСТЕНДЕДСТИЛЕ RB**</span><span class="sxs-lookup"><span data-stu-id="70a49-138">**RB\_SETEXTENDEDSTYLE**</span></span>](rb-setextendedstyle.md)
-   [<span data-ttu-id="70a49-139">**\_СЕТПАЛЕТТЕ RB**</span><span class="sxs-lookup"><span data-stu-id="70a49-139">**RB\_SETPALETTE**</span></span>](rb-setpalette.md)
-   [<span data-ttu-id="70a49-140">**\_СЕТПАРЕНТ RB**</span><span class="sxs-lookup"><span data-stu-id="70a49-140">**RB\_SETPARENT**</span></span>](rb-setparent.md)
-   [<span data-ttu-id="70a49-141">**\_СЕТТЕКСТКОЛОР RB**</span><span class="sxs-lookup"><span data-stu-id="70a49-141">**RB\_SETTEXTCOLOR**</span></span>](rb-settextcolor.md)
-   [<span data-ttu-id="70a49-142">**\_СЕТТУЛТИПС RB**</span><span class="sxs-lookup"><span data-stu-id="70a49-142">**RB\_SETTOOLTIPS**</span></span>](rb-settooltips.md)
-   [<span data-ttu-id="70a49-143">**\_СЕТУНИКОДЕФОРМАТ RB**</span><span class="sxs-lookup"><span data-stu-id="70a49-143">**RB\_SETUNICODEFORMAT**</span></span>](rb-setunicodeformat.md)
-   [<span data-ttu-id="70a49-144">**\_SETWINDOWTHEME RB**</span><span class="sxs-lookup"><span data-stu-id="70a49-144">**RB\_SETWINDOWTHEME**</span></span>](rb-setwindowtheme.md)
-   [<span data-ttu-id="70a49-145">**\_ШОВБАНД RB**</span><span class="sxs-lookup"><span data-stu-id="70a49-145">**RB\_SHOWBAND**</span></span>](rb-showband.md)
-   [<span data-ttu-id="70a49-146">**\_СИЗЕТОРЕКТ RB**</span><span class="sxs-lookup"><span data-stu-id="70a49-146">**RB\_SIZETORECT**</span></span>](rb-sizetorect.md)

 

 





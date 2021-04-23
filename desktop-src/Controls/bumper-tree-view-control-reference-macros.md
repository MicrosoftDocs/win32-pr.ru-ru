---
title: Макросы представления в виде дерева
description: Макросы представления в виде дерева
ms.assetid: ee569a0e-21f3-4d46-ac7d-e152f8b35391
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc69c9ebc400975bba1d9e43c820b6a7314981c7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104273660"
---
# <a name="tree-view-macros"></a><span data-ttu-id="9dfb5-103">Макросы представления в виде дерева</span><span class="sxs-lookup"><span data-stu-id="9dfb5-103">Tree View Macros</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9dfb5-104">в этом разделе</span><span class="sxs-lookup"><span data-stu-id="9dfb5-104">In This Section</span></span>

-   [<span data-ttu-id="9dfb5-105">**\_Креатедрагимаже TreeView**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-105">**TreeView\_CreateDragImage**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_createdragimage)
-   [<span data-ttu-id="9dfb5-106">**\_Делетеаллитемс TreeView**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-106">**TreeView\_DeleteAllItems**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteallitems)
-   [<span data-ttu-id="9dfb5-107">**\_DeleteItem TreeView**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-107">**TreeView\_DeleteItem**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteitem)
-   [<span data-ttu-id="9dfb5-108">**\_Едитлабел TreeView**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-108">**TreeView\_EditLabel**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_editlabel)
-   [<span data-ttu-id="9dfb5-109">**\_Ендедитлабелнов TreeView**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-109">**TreeView\_EndEditLabelNow**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_endeditlabelnow)
-   [<span data-ttu-id="9dfb5-110">**\_Енсуревисибле TreeView**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-110">**TreeView\_EnsureVisible**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_ensurevisible)
-   [<span data-ttu-id="9dfb5-111">**\_Развернуть TreeView**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-111">**TreeView\_Expand**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_expand)
-   [<span data-ttu-id="9dfb5-112">**\_Жетбкколор TreeView**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-112">**TreeView\_GetBkColor**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getbkcolor)
-   [<span data-ttu-id="9dfb5-113">**\_Жетчеккстате TreeView**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-113">**TreeView\_GetCheckState**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getcheckstate)
-   [<span data-ttu-id="9dfb5-114">**Элемент управления TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-114">**TreeView\_GetChild**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getchild)
-   [<span data-ttu-id="9dfb5-115">**Число в TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-115">**TreeView\_GetCount**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getcount)
-   [<span data-ttu-id="9dfb5-116">**\_Жетдрофилигхт TreeView**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-116">**TreeView\_GetDropHilight**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getdrophilight)
-   [<span data-ttu-id="9dfb5-117">**\_Жетедитконтрол TreeView**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-117">**TreeView\_GetEditControl**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_geteditcontrol)
-   [<span data-ttu-id="9dfb5-118">**\_Жетекстендедстиле TreeView**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-118">**TreeView\_GetExtendedStyle**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getextendedstyle)
-   [<span data-ttu-id="9dfb5-119">**\_Жетфирствисибле TreeView**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-119">**TreeView\_GetFirstVisible**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getfirstvisible)
-   [<span data-ttu-id="9dfb5-120">**TreeView — \_ ImageList**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-120">**TreeView\_GetImageList**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getimagelist)
-   [<span data-ttu-id="9dfb5-121">**Отступ в TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-121">**TreeView\_GetIndent**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getindent)
-   [<span data-ttu-id="9dfb5-122">**\_Жетинсертмаркколор TreeView**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-122">**TreeView\_GetInsertMarkColor**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getinsertmarkcolor)
-   [<span data-ttu-id="9dfb5-123">**\_Жетисеарчстринг TreeView**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-123">**TreeView\_GetISearchString**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getisearchstring)
-   [<span data-ttu-id="9dfb5-124">**\_Элемент TreeView**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-124">**TreeView\_GetItem**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitem)
-   [<span data-ttu-id="9dfb5-125">**\_GetItemHeight TreeView**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-125">**TreeView\_GetItemHeight**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemheight)
-   [<span data-ttu-id="9dfb5-126">**\_Жетитемпартрект TreeView**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-126">**TreeView\_GetItemPartRect**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitempartrect)
-   [<span data-ttu-id="9dfb5-127">**\_Жетитемрект TreeView**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-127">**TreeView\_GetItemRect**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemrect)
-   [<span data-ttu-id="9dfb5-128">**\_Жетитемстате TreeView**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-128">**TreeView\_GetItemState**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemstate)
-   [<span data-ttu-id="9dfb5-129">**\_Жетластвисибле TreeView**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-129">**TreeView\_GetLastVisible**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getlastvisible)
-   [<span data-ttu-id="9dfb5-130">**\_Жетлинеколор TreeView**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-130">**TreeView\_GetLineColor**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getlinecolor)
-   [<span data-ttu-id="9dfb5-131">**\_Жетнекститем TreeView**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-131">**TreeView\_GetNextItem**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextitem)
-   [<span data-ttu-id="9dfb5-132">**\_Жетнекстселектед TreeView**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-132">**TreeView\_GetNextSelected**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextselected)
-   [<span data-ttu-id="9dfb5-133">**\_Жетнекстсиблинг TreeView**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-133">**TreeView\_GetNextSibling**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextsibling)
-   [<span data-ttu-id="9dfb5-134">**\_Жетнекствисибле TreeView**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-134">**TreeView\_GetNextVisible**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextvisible)
-   [<span data-ttu-id="9dfb5-135">**\_Родители TreeView**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-135">**TreeView\_GetParent**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getparent)
-   [<span data-ttu-id="9dfb5-136">**\_Жетпревсиблинг TreeView**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-136">**TreeView\_GetPrevSibling**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getprevsibling)
-   [<span data-ttu-id="9dfb5-137">**\_Жетпреввисибле TreeView**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-137">**TreeView\_GetPrevVisible**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getprevvisible)
-   [<span data-ttu-id="9dfb5-138">**\_Корень TreeView**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-138">**TreeView\_GetRoot**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getroot)
-   [<span data-ttu-id="9dfb5-139">**\_Жетскроллтиме TreeView**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-139">**TreeView\_GetScrollTime**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getscrolltime)
-   [<span data-ttu-id="9dfb5-140">**\_Жетселектедкаунт TreeView**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-140">**TreeView\_GetSelectedCount**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getselectedcount)
-   [<span data-ttu-id="9dfb5-141">**\_Выбор TreeView**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-141">**TreeView\_GetSelection**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getselection)
-   [<span data-ttu-id="9dfb5-142">**\_Жеттекстколор TreeView**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-142">**TreeView\_GetTextColor**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_gettextcolor)
-   [<span data-ttu-id="9dfb5-143">**\_Подсказки TreeView**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-143">**TreeView\_GetToolTips**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_gettooltips)
-   [<span data-ttu-id="9dfb5-144">**\_Жетуникодеформат TreeView**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-144">**TreeView\_GetUnicodeFormat**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getunicodeformat)
-   [<span data-ttu-id="9dfb5-145">**\_Жетвисиблекаунт TreeView**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-145">**TreeView\_GetVisibleCount**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getvisiblecount)
-   [<span data-ttu-id="9dfb5-146">**\_HitTest TreeView**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-146">**TreeView\_HitTest**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_hittest)
-   [<span data-ttu-id="9dfb5-147">**\_InsertItem TreeView**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-147">**TreeView\_InsertItem**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_insertitem)
-   [<span data-ttu-id="9dfb5-148">**\_МапакЦидтохтриитем TreeView**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-148">**TreeView\_MapAccIDToHTREEITEM**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_mapaccidtohtreeitem)
-   [<span data-ttu-id="9dfb5-149">**\_МафтриитемтоакЦид TreeView**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-149">**TreeView\_MapHTREEITEMtoAccID**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_maphtreeitemtoaccid)
-   [<span data-ttu-id="9dfb5-150">**\_Выбор TreeView**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-150">**TreeView\_Select**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_select)
-   [<span data-ttu-id="9dfb5-151">**\_Селектдроптаржет TreeView**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-151">**TreeView\_SelectDropTarget**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectdroptarget)
-   [<span data-ttu-id="9dfb5-152">**\_Селектитем TreeView**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-152">**TreeView\_SelectItem**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectitem)
-   [<span data-ttu-id="9dfb5-153">**\_Селектсетфирствисибле TreeView**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-153">**TreeView\_SelectSetFirstVisible**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectsetfirstvisible)
-   [<span data-ttu-id="9dfb5-154">**\_Сетаутоскроллинфо TreeView**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-154">**TreeView\_SetAutoScrollInfo**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setautoscrollinfo)
-   [<span data-ttu-id="9dfb5-155">**\_Сетбкколор TreeView**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-155">**TreeView\_SetBkColor**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setbkcolor)
-   [<span data-ttu-id="9dfb5-156">**\_Сетбордер TreeView**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-156">**TreeView\_SetBorder**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setborder)
-   [<span data-ttu-id="9dfb5-157">**\_Сетчеккстате TreeView**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-157">**TreeView\_SetCheckState**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setcheckstate)
-   [<span data-ttu-id="9dfb5-158">**\_Сетекстендедстиле TreeView**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-158">**TreeView\_SetExtendedStyle**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setextendedstyle)
-   [<span data-ttu-id="9dfb5-159">**\_Сесот TreeView**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-159">**TreeView\_SetHot**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sethot)
-   [<span data-ttu-id="9dfb5-160">**\_Сетимажелист TreeView**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-160">**TreeView\_SetImageList**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setimagelist)
-   [<span data-ttu-id="9dfb5-161">**\_Сетиндент TreeView**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-161">**TreeView\_SetIndent**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setindent)
-   [<span data-ttu-id="9dfb5-162">**\_Сетинсертмарк TreeView**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-162">**TreeView\_SetInsertMark**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setinsertmark)
-   [<span data-ttu-id="9dfb5-163">**\_Сетинсертмаркколор TreeView**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-163">**TreeView\_SetInsertMarkColor**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setinsertmarkcolor)
-   [<span data-ttu-id="9dfb5-164">**\_Сетитем TreeView**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-164">**TreeView\_SetItem**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitem)
-   [<span data-ttu-id="9dfb5-165">**\_Сетитемхеигхт TreeView**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-165">**TreeView\_SetItemHeight**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitemheight)
-   [<span data-ttu-id="9dfb5-166">**\_Сетитемстате TreeView**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-166">**TreeView\_SetItemState**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitemstate)
-   [<span data-ttu-id="9dfb5-167">**\_Сетлинеколор TreeView**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-167">**TreeView\_SetLineColor**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setlinecolor)
-   [<span data-ttu-id="9dfb5-168">**\_Сетскроллтиме TreeView**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-168">**TreeView\_SetScrollTime**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setscrolltime)
-   [<span data-ttu-id="9dfb5-169">**\_Сеттекстколор TreeView**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-169">**TreeView\_SetTextColor**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_settextcolor)
-   [<span data-ttu-id="9dfb5-170">**\_Сеттултипс TreeView**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-170">**TreeView\_SetToolTips**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_settooltips)
-   [<span data-ttu-id="9dfb5-171">**\_Сетуникодеформат TreeView**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-171">**TreeView\_SetUnicodeFormat**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setunicodeformat)
-   [<span data-ttu-id="9dfb5-172">**\_Шовинфотип TreeView**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-172">**TreeView\_ShowInfoTip**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_showinfotip)
-   [<span data-ttu-id="9dfb5-173">**\_Сортчилдрен TreeView**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-173">**TreeView\_SortChildren**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sortchildren)
-   [<span data-ttu-id="9dfb5-174">**\_Сортчилдренкб TreeView**</span><span class="sxs-lookup"><span data-stu-id="9dfb5-174">**TreeView\_SortChildrenCB**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sortchildrencb)

 

 





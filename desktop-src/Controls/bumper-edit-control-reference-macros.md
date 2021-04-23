---
title: Изменить макросы элемента управления
description: Изменить макросы элемента управления
ms.assetid: 7c2bb80e-57ca-4d95-a499-b65eefe0352c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 795aba77e2f0dc439fdd6bdaab6a4358a15596ee
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352915"
---
# <a name="edit-control-macros"></a><span data-ttu-id="0bccf-103">Изменить макросы элемента управления</span><span class="sxs-lookup"><span data-stu-id="0bccf-103">Edit Control Macros</span></span>

## <a name="in-this-section"></a><span data-ttu-id="0bccf-104">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="0bccf-104">In this section</span></span>

-   [<span data-ttu-id="0bccf-105">**Изменить \_ канундо**</span><span class="sxs-lookup"><span data-stu-id="0bccf-105">**Edit\_CanUndo**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_canundo)
-   [<span data-ttu-id="0bccf-106">**Изменить \_ емптюндобуффер**</span><span class="sxs-lookup"><span data-stu-id="0bccf-106">**Edit\_EmptyUndoBuffer**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_emptyundobuffer)
-   [<span data-ttu-id="0bccf-107">**Изменение \_ включения**</span><span class="sxs-lookup"><span data-stu-id="0bccf-107">**Edit\_Enable**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_enable)
-   [<span data-ttu-id="0bccf-108">**Изменить \_ фмтлинес**</span><span class="sxs-lookup"><span data-stu-id="0bccf-108">**Edit\_FmtLines**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_fmtlines)
-   [<span data-ttu-id="0bccf-109">**Изменить \_ жеткуебаннертекст**</span><span class="sxs-lookup"><span data-stu-id="0bccf-109">**Edit\_GetCueBannerText**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_getcuebannertext)
-   [<span data-ttu-id="0bccf-110">**Изменить \_ жетфирствисиблелине**</span><span class="sxs-lookup"><span data-stu-id="0bccf-110">**Edit\_GetFirstVisibleLine**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_getfirstvisibleline)
-   [<span data-ttu-id="0bccf-111">**Изменить \_ getHandler**</span><span class="sxs-lookup"><span data-stu-id="0bccf-111">**Edit\_GetHandle**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_gethandle)
-   [<span data-ttu-id="0bccf-112">**Изменить \_ жесилите**</span><span class="sxs-lookup"><span data-stu-id="0bccf-112">**Edit\_GetHilite**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_gethilite)
-   [<span data-ttu-id="0bccf-113">**Изменить \_ подстроку**</span><span class="sxs-lookup"><span data-stu-id="0bccf-113">**Edit\_GetLine**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_getline)
-   [<span data-ttu-id="0bccf-114">**Изменить \_ жетлинекаунт**</span><span class="sxs-lookup"><span data-stu-id="0bccf-114">**Edit\_GetLineCount**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_getlinecount)
-   [<span data-ttu-id="0bccf-115">**Изменить \_ изменение**</span><span class="sxs-lookup"><span data-stu-id="0bccf-115">**Edit\_GetModify**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_getmodify)
-   [<span data-ttu-id="0bccf-116">**Изменить \_ жетпассвордчар**</span><span class="sxs-lookup"><span data-stu-id="0bccf-116">**Edit\_GetPasswordChar**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_getpasswordchar)
-   [<span data-ttu-id="0bccf-117">**Изменить \_ Коrect**</span><span class="sxs-lookup"><span data-stu-id="0bccf-117">**Edit\_GetRect**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_getrect)
-   [<span data-ttu-id="0bccf-118">**Изменить \_ жетсел**</span><span class="sxs-lookup"><span data-stu-id="0bccf-118">**Edit\_GetSel**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_getsel)
-   [<span data-ttu-id="0bccf-119">**Изменить \_ gettext**</span><span class="sxs-lookup"><span data-stu-id="0bccf-119">**Edit\_GetText**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_gettext)
-   [<span data-ttu-id="0bccf-120">**Изменить \_ жеттекстленгс**</span><span class="sxs-lookup"><span data-stu-id="0bccf-120">**Edit\_GetTextLength**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_gettextlength)
-   [<span data-ttu-id="0bccf-121">**Изменить \_ жетвордбреакпрок**</span><span class="sxs-lookup"><span data-stu-id="0bccf-121">**Edit\_GetWordBreakProc**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_getwordbreakproc)
-   [<span data-ttu-id="0bccf-122">**Изменить \_ хидебаллунтип**</span><span class="sxs-lookup"><span data-stu-id="0bccf-122">**Edit\_HideBalloonTip**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_hideballoontip)
-   [<span data-ttu-id="0bccf-123">**Изменить \_ лимиттекст**</span><span class="sxs-lookup"><span data-stu-id="0bccf-123">**Edit\_LimitText**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_limittext)
-   [<span data-ttu-id="0bccf-124">**Изменить \_ линефромчар**</span><span class="sxs-lookup"><span data-stu-id="0bccf-124">**Edit\_LineFromChar**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_linefromchar)
-   [<span data-ttu-id="0bccf-125">**Изменить \_ линеиндекс**</span><span class="sxs-lookup"><span data-stu-id="0bccf-125">**Edit\_LineIndex**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_lineindex)
-   [<span data-ttu-id="0bccf-126">**Изменить \_ линеленгс**</span><span class="sxs-lookup"><span data-stu-id="0bccf-126">**Edit\_LineLength**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_linelength)
-   [<span data-ttu-id="0bccf-127">**Изменить \_ носетфокус**</span><span class="sxs-lookup"><span data-stu-id="0bccf-127">**Edit\_NoSetFocus**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_nosetfocus)
-   [<span data-ttu-id="0bccf-128">**Изменить \_ реплацесел**</span><span class="sxs-lookup"><span data-stu-id="0bccf-128">**Edit\_ReplaceSel**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_replacesel)
-   [<span data-ttu-id="0bccf-129">**Изменить \_ прокрутку**</span><span class="sxs-lookup"><span data-stu-id="0bccf-129">**Edit\_Scroll**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_scroll)
-   [<span data-ttu-id="0bccf-130">**Изменить \_ скроллкарет**</span><span class="sxs-lookup"><span data-stu-id="0bccf-130">**Edit\_ScrollCaret**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_scrollcaret)
-   [<span data-ttu-id="0bccf-131">**Изменить \_ сеткуебаннертекст**</span><span class="sxs-lookup"><span data-stu-id="0bccf-131">**Edit\_SetCueBannerText**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_setcuebannertext)
-   [<span data-ttu-id="0bccf-132">**Изменить \_ сеткуебаннертекстфокусед**</span><span class="sxs-lookup"><span data-stu-id="0bccf-132">**Edit\_SetCueBannerTextFocused**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_setcuebannertextfocused)
-   [<span data-ttu-id="0bccf-133">**Изменить \_ сесандле**</span><span class="sxs-lookup"><span data-stu-id="0bccf-133">**Edit\_SetHandle**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_sethandle)
-   [<span data-ttu-id="0bccf-134">**Изменить \_ сесилите**</span><span class="sxs-lookup"><span data-stu-id="0bccf-134">**Edit\_SetHilite**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_sethilite)
-   [<span data-ttu-id="0bccf-135">**Изменить \_ сетмодифи**</span><span class="sxs-lookup"><span data-stu-id="0bccf-135">**Edit\_SetModify**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_setmodify)
-   [<span data-ttu-id="0bccf-136">**Изменить \_ сетпассвордчар**</span><span class="sxs-lookup"><span data-stu-id="0bccf-136">**Edit\_SetPasswordChar**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_setpasswordchar)
-   [<span data-ttu-id="0bccf-137">**Изменить \_ SetReadOnly**</span><span class="sxs-lookup"><span data-stu-id="0bccf-137">**Edit\_SetReadOnly**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_setreadonly)
-   [<span data-ttu-id="0bccf-138">**Изменить \_ SetRect**</span><span class="sxs-lookup"><span data-stu-id="0bccf-138">**Edit\_SetRect**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_setrect)
-   [<span data-ttu-id="0bccf-139">**Изменить \_ сетректнопаинт**</span><span class="sxs-lookup"><span data-stu-id="0bccf-139">**Edit\_SetRectNoPaint**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_setrectnopaint)
-   [<span data-ttu-id="0bccf-140">**Изменить \_ сетсел**</span><span class="sxs-lookup"><span data-stu-id="0bccf-140">**Edit\_SetSel**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_setsel)
-   [<span data-ttu-id="0bccf-141">**Изменить \_ сеттабстопс**</span><span class="sxs-lookup"><span data-stu-id="0bccf-141">**Edit\_SetTabStops**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_settabstops)
-   [<span data-ttu-id="0bccf-142">**Изменить \_ SetText**</span><span class="sxs-lookup"><span data-stu-id="0bccf-142">**Edit\_SetText**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_settext)
-   [<span data-ttu-id="0bccf-143">**Изменить \_ сетвордбреакпрок**</span><span class="sxs-lookup"><span data-stu-id="0bccf-143">**Edit\_SetWordBreakProc**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_setwordbreakproc)
-   [<span data-ttu-id="0bccf-144">**Изменить \_ шовбаллунтип**</span><span class="sxs-lookup"><span data-stu-id="0bccf-144">**Edit\_ShowBalloonTip**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_showballoontip)
-   [<span data-ttu-id="0bccf-145">**Изменить \_ такефокус**</span><span class="sxs-lookup"><span data-stu-id="0bccf-145">**Edit\_TakeFocus**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_takefocus)
-   [<span data-ttu-id="0bccf-146">**Изменить \_ отмену**</span><span class="sxs-lookup"><span data-stu-id="0bccf-146">**Edit\_Undo**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_undo)

 

 





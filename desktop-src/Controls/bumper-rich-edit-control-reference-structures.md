---
title: Расширенные структуры редактирования
description: Расширенные структуры редактирования
ms.assetid: f7679e81-0a50-408b-8f60-9a3da4650f2c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e63005040ca5b980f8aa78f7db8039b1e5254dd9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "103914480"
---
# <a name="rich-edit-structures"></a><span data-ttu-id="b69c6-103">Расширенные структуры редактирования</span><span class="sxs-lookup"><span data-stu-id="b69c6-103">Rich Edit Structures</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b69c6-104">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="b69c6-104">In this section</span></span>

-   [<span data-ttu-id="b69c6-105">**бидиоптионс**</span><span class="sxs-lookup"><span data-stu-id="b69c6-105">**BIDIOPTIONS**</span></span>](/windows/desktop/api/Richedit/ns-richedit-bidioptions)
-   [<span data-ttu-id="b69c6-106">**чанженотифи**</span><span class="sxs-lookup"><span data-stu-id="b69c6-106">**CHANGENOTIFY**</span></span>](/windows/desktop/api/Textserv/ns-textserv-changenotify)
-   [<span data-ttu-id="b69c6-107">**чарформат**</span><span class="sxs-lookup"><span data-stu-id="b69c6-107">**CHARFORMAT**</span></span>](/windows/win32/api/richedit/ns-richedit-charformata)
-   [<span data-ttu-id="b69c6-108">**CHARFORMAT2**</span><span class="sxs-lookup"><span data-stu-id="b69c6-108">**CHARFORMAT2**</span></span>](/windows/desktop/api/Richedit/ns-richedit-charformat2a)
-   [<span data-ttu-id="b69c6-109">**чарранже**</span><span class="sxs-lookup"><span data-stu-id="b69c6-109">**CHARRANGE**</span></span>](/windows/desktop/api/Richedit/ns-richedit-charrange)
-   [<span data-ttu-id="b69c6-110">**клипбоардформат**</span><span class="sxs-lookup"><span data-stu-id="b69c6-110">**CLIPBOARDFORMAT**</span></span>](/windows/desktop/api/Richedit/ns-richedit-clipboardformat)
-   [<span data-ttu-id="b69c6-111">**компколор**</span><span class="sxs-lookup"><span data-stu-id="b69c6-111">**COMPCOLOR**</span></span>](/windows/desktop/api/Richedit/ns-richedit-compcolor)
-   [<span data-ttu-id="b69c6-112">**едитстреам**</span><span class="sxs-lookup"><span data-stu-id="b69c6-112">**EDITSTREAM**</span></span>](/windows/desktop/api/Richedit/ns-richedit-editstream)
-   [<span data-ttu-id="b69c6-113">**енкорректтекст**</span><span class="sxs-lookup"><span data-stu-id="b69c6-113">**ENCORRECTTEXT**</span></span>](/windows/desktop/api/Richedit/ns-richedit-encorrecttext)
-   [<span data-ttu-id="b69c6-114">**ендкомпоситионнотифи**</span><span class="sxs-lookup"><span data-stu-id="b69c6-114">**ENDCOMPOSITIONNOTIFY**</span></span>](/windows/win32/api/richedit/ns-richedit-endcompositionnotify)
-   [<span data-ttu-id="b69c6-115">**ендропфилес**</span><span class="sxs-lookup"><span data-stu-id="b69c6-115">**ENDROPFILES**</span></span>](/windows/desktop/api/Richedit/ns-richedit-endropfiles)
-   [<span data-ttu-id="b69c6-116">**енлинк**</span><span class="sxs-lookup"><span data-stu-id="b69c6-116">**ENLINK**</span></span>](/windows/desktop/api/Richedit/ns-richedit-enlink)
-   [<span data-ttu-id="b69c6-117">**енловфиртф**</span><span class="sxs-lookup"><span data-stu-id="b69c6-117">**ENLOWFIRTF**</span></span>](/windows/desktop/api/Richedit/ns-richedit-enlowfirtf)
-   [<span data-ttu-id="b69c6-118">**енолеопфаилед**</span><span class="sxs-lookup"><span data-stu-id="b69c6-118">**ENOLEOPFAILED**</span></span>](/windows/desktop/api/Richedit/ns-richedit-enoleopfailed)
-   [<span data-ttu-id="b69c6-119">**енпротектед**</span><span class="sxs-lookup"><span data-stu-id="b69c6-119">**ENPROTECTED**</span></span>](/windows/desktop/api/Richedit/ns-richedit-enprotected)
-   [<span data-ttu-id="b69c6-120">**енсавеклипбоард**</span><span class="sxs-lookup"><span data-stu-id="b69c6-120">**ENSAVECLIPBOARD**</span></span>](/windows/desktop/api/Richedit/ns-richedit-ensaveclipboard)
-   [<span data-ttu-id="b69c6-121">**СТРОКИ FINDTEXT**</span><span class="sxs-lookup"><span data-stu-id="b69c6-121">**FINDTEXT**</span></span>](/windows/win32/api/richedit/ns-richedit-findtexta)
-   [<span data-ttu-id="b69c6-122">**финдтекстекс**</span><span class="sxs-lookup"><span data-stu-id="b69c6-122">**FINDTEXTEX**</span></span>](/windows/desktop/api/Richedit/ns-richedit-findtextexa)
-   [<span data-ttu-id="b69c6-123">**форматранже**</span><span class="sxs-lookup"><span data-stu-id="b69c6-123">**FORMATRANGE**</span></span>](/windows/desktop/api/Richedit/ns-richedit-formatrange)
-   [<span data-ttu-id="b69c6-124">**жетконтекстменуекс**</span><span class="sxs-lookup"><span data-stu-id="b69c6-124">**GETCONTEXTMENUEX**</span></span>](/windows/desktop/api/Richedit/ns-richedit-getcontextmenuex)
-   [<span data-ttu-id="b69c6-125">**жеттекстекс**</span><span class="sxs-lookup"><span data-stu-id="b69c6-125">**GETTEXTEX**</span></span>](/windows/desktop/api/Richedit/ns-richedit-gettextex)
-   [<span data-ttu-id="b69c6-126">**жеттекстленгсекс**</span><span class="sxs-lookup"><span data-stu-id="b69c6-126">**GETTEXTLENGTHEX**</span></span>](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex)
-   [<span data-ttu-id="b69c6-127">**хифенатеинфо**</span><span class="sxs-lookup"><span data-stu-id="b69c6-127">**HYPHENATEINFO**</span></span>](/windows/win32/api/richedit/ns-richedit-hyphenateinfo)
-   [<span data-ttu-id="b69c6-128">**хифресулт**</span><span class="sxs-lookup"><span data-stu-id="b69c6-128">**HYPHRESULT**</span></span>](/windows/desktop/api/Richedit/ns-richedit-hyphresult)
-   [<span data-ttu-id="b69c6-129">**имекомптекст**</span><span class="sxs-lookup"><span data-stu-id="b69c6-129">**IMECOMPTEXT**</span></span>](/windows/desktop/api/Richedit/ns-richedit-imecomptext)
-   [<span data-ttu-id="b69c6-130">**мсгфилтер**</span><span class="sxs-lookup"><span data-stu-id="b69c6-130">**MSGFILTER**</span></span>](/windows/desktop/api/Richedit/ns-richedit-msgfilter)
-   [<span data-ttu-id="b69c6-131">**обжектпоситионс**</span><span class="sxs-lookup"><span data-stu-id="b69c6-131">**OBJECTPOSITIONS**</span></span>](/windows/desktop/api/Richedit/ns-richedit-objectpositions)
-   [<span data-ttu-id="b69c6-132">\**ФОРМАТ \**</span><span class="sxs-lookup"><span data-stu-id="b69c6-132">**PARAFORMAT**</span></span>](/windows/desktop/api/Richedit/ns-richedit-paraformat)
-   [<span data-ttu-id="b69c6-133">**PARAFORMAT2**</span><span class="sxs-lookup"><span data-stu-id="b69c6-133">**PARAFORMAT2**</span></span>](/windows/desktop/api/Richedit/ns-richedit-paraformat2)
-   [<span data-ttu-id="b69c6-134">**ЗНАКИ ПРЕПИНАНИЯ**</span><span class="sxs-lookup"><span data-stu-id="b69c6-134">**PUNCTUATION**</span></span>](/windows/desktop/api/Richedit/ns-richedit-punctuation)
-   [<span data-ttu-id="b69c6-135">**Переобъектировать**</span><span class="sxs-lookup"><span data-stu-id="b69c6-135">**REOBJECT**</span></span>](/windows/desktop/api/Richole/ns-richole-reobject)
-   [<span data-ttu-id="b69c6-136">**репастеспеЦиал**</span><span class="sxs-lookup"><span data-stu-id="b69c6-136">**REPASTESPECIAL**</span></span>](/windows/desktop/api/Richedit/ns-richedit-repastespecial)
-   [<span data-ttu-id="b69c6-137">**рекресизе**</span><span class="sxs-lookup"><span data-stu-id="b69c6-137">**REQRESIZE**</span></span>](/windows/desktop/api/Richedit/ns-richedit-reqresize)
-   [<span data-ttu-id="b69c6-138">**\_Параметры изображения \_ RichEdit**</span><span class="sxs-lookup"><span data-stu-id="b69c6-138">**RICHEDIT\_IMAGE\_PARAMETERS**</span></span>](/windows/win32/api/richedit/ns-richedit-richedit_image_parameters)
-   [<span data-ttu-id="b69c6-139">**селчанже**</span><span class="sxs-lookup"><span data-stu-id="b69c6-139">**SELCHANGE**</span></span>](/windows/desktop/api/Richedit/ns-richedit-selchange)
-   [<span data-ttu-id="b69c6-140">**сеттекстекс**</span><span class="sxs-lookup"><span data-stu-id="b69c6-140">**SETTEXTEX**</span></span>](/windows/desktop/api/Richedit/ns-richedit-settextex)
-   [<span data-ttu-id="b69c6-141">**таблецеллпармс**</span><span class="sxs-lookup"><span data-stu-id="b69c6-141">**TABLECELLPARMS**</span></span>](/windows/desktop/api/Richedit/ns-richedit-tablecellparms)
-   [<span data-ttu-id="b69c6-142">**таблеровпармс**</span><span class="sxs-lookup"><span data-stu-id="b69c6-142">**TABLEROWPARMS**</span></span>](/windows/desktop/api/Richedit/ns-richedit-tablerowparms)
-   [<span data-ttu-id="b69c6-143">**TEXTRANGE**</span><span class="sxs-lookup"><span data-stu-id="b69c6-143">**TEXTRANGE**</span></span>](/windows/win32/api/richedit/ns-richedit-textrangea)

 

 





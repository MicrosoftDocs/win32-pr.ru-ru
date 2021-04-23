---
title: Функции списка изображений
description: Функции списка изображений
ms.assetid: b5754633-f673-414e-9e0b-3f6f211ecd2a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb3e877e4f264aa9c0440b183a2c528592b6ccee
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352375"
---
# <a name="image-list-functions"></a><span data-ttu-id="51187-103">Функции списка изображений</span><span class="sxs-lookup"><span data-stu-id="51187-103">Image List Functions</span></span>

## <a name="in-this-section"></a><span data-ttu-id="51187-104">в этом разделе</span><span class="sxs-lookup"><span data-stu-id="51187-104">In This Section</span></span>

-   [<span data-ttu-id="51187-105">**ХИМАЖЕЛИСТ \_ QueryInterface**</span><span class="sxs-lookup"><span data-stu-id="51187-105">**HIMAGELIST\_QueryInterface**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-himagelist_queryinterface)
-   [<span data-ttu-id="51187-106">**\_Добавление ImageList**</span><span class="sxs-lookup"><span data-stu-id="51187-106">**ImageList\_Add**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_add)
-   [<span data-ttu-id="51187-107">**\_Аддмаскед ImageList**</span><span class="sxs-lookup"><span data-stu-id="51187-107">**ImageList\_AddMasked**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_addmasked)
-   [<span data-ttu-id="51187-108">**\_Бегиндраг ImageList**</span><span class="sxs-lookup"><span data-stu-id="51187-108">**ImageList\_BeginDrag**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag)
-   [<span data-ttu-id="51187-109">**CoCreateInstance для ImageList \_**</span><span class="sxs-lookup"><span data-stu-id="51187-109">**ImageList\_CoCreateInstance**</span></span>](/windows/desktop/api/CommonControls/nf-commoncontrols-imagelist_cocreateinstance)
-   [<span data-ttu-id="51187-110">**\_Копия ImageList**</span><span class="sxs-lookup"><span data-stu-id="51187-110">**ImageList\_Copy**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_copy)
-   [<span data-ttu-id="51187-111">**\_Создание ImageList**</span><span class="sxs-lookup"><span data-stu-id="51187-111">**ImageList\_Create**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create)
-   [<span data-ttu-id="51187-112">**\_Уничтожение ImageList**</span><span class="sxs-lookup"><span data-stu-id="51187-112">**ImageList\_Destroy**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_destroy)
-   [<span data-ttu-id="51187-113">**\_DragEnter ImageList**</span><span class="sxs-lookup"><span data-stu-id="51187-113">**ImageList\_DragEnter**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragenter)
-   [<span data-ttu-id="51187-114">**\_DragLeave ImageList**</span><span class="sxs-lookup"><span data-stu-id="51187-114">**ImageList\_DragLeave**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragleave)
-   [<span data-ttu-id="51187-115">**\_Драгмове ImageList**</span><span class="sxs-lookup"><span data-stu-id="51187-115">**ImageList\_DragMove**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragmove)
-   [<span data-ttu-id="51187-116">**\_Драгшовнолокк ImageList**</span><span class="sxs-lookup"><span data-stu-id="51187-116">**ImageList\_DragShowNolock**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragshownolock)
-   [<span data-ttu-id="51187-117">**\_Прорисовка ImageList**</span><span class="sxs-lookup"><span data-stu-id="51187-117">**ImageList\_Draw**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw)
-   [<span data-ttu-id="51187-118">**\_Дравекс ImageList**</span><span class="sxs-lookup"><span data-stu-id="51187-118">**ImageList\_DrawEx**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawex)
-   [<span data-ttu-id="51187-119">**\_Дравиндирект ImageList**</span><span class="sxs-lookup"><span data-stu-id="51187-119">**ImageList\_DrawIndirect**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawindirect)
-   [<span data-ttu-id="51187-120">**\_Дубликаты ImageList**</span><span class="sxs-lookup"><span data-stu-id="51187-120">**ImageList\_Duplicate**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_duplicate)
-   [<span data-ttu-id="51187-121">**\_Енддраг ImageList**</span><span class="sxs-lookup"><span data-stu-id="51187-121">**ImageList\_EndDrag**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_enddrag)
-   [<span data-ttu-id="51187-122">**\_Жетбкколор ImageList**</span><span class="sxs-lookup"><span data-stu-id="51187-122">**ImageList\_GetBkColor**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_getbkcolor)
-   [<span data-ttu-id="51187-123">**\_Жетдрагимаже ImageList**</span><span class="sxs-lookup"><span data-stu-id="51187-123">**ImageList\_GetDragImage**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_getdragimage)
-   [<span data-ttu-id="51187-124">**\_Значок ImageList**</span><span class="sxs-lookup"><span data-stu-id="51187-124">**ImageList\_GetIcon**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_geticon)
-   [<span data-ttu-id="51187-125">**\_Жетиконсизе ImageList**</span><span class="sxs-lookup"><span data-stu-id="51187-125">**ImageList\_GetIconSize**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_geticonsize)
-   [<span data-ttu-id="51187-126">**\_Жетимажекаунт ImageList**</span><span class="sxs-lookup"><span data-stu-id="51187-126">**ImageList\_GetImageCount**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_getimagecount)
-   [<span data-ttu-id="51187-127">**\_Жетимажеинфо ImageList**</span><span class="sxs-lookup"><span data-stu-id="51187-127">**ImageList\_GetImageInfo**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_getimageinfo)
-   [<span data-ttu-id="51187-128">**\_Лоадимаже ImageList**</span><span class="sxs-lookup"><span data-stu-id="51187-128">**ImageList\_LoadImage**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_loadimagea)
-   [<span data-ttu-id="51187-129">**\_Слияние ImageList**</span><span class="sxs-lookup"><span data-stu-id="51187-129">**ImageList\_Merge**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_merge)
-   [<span data-ttu-id="51187-130">**\_Чтение ImageList**</span><span class="sxs-lookup"><span data-stu-id="51187-130">**ImageList\_Read**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_read)
-   [<span data-ttu-id="51187-131">**\_Реадекс ImageList**</span><span class="sxs-lookup"><span data-stu-id="51187-131">**ImageList\_ReadEx**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_readex)
-   [<span data-ttu-id="51187-132">**\_Удаление ImageList**</span><span class="sxs-lookup"><span data-stu-id="51187-132">**ImageList\_Remove**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_remove)
-   [<span data-ttu-id="51187-133">**\_Замещение ImageList**</span><span class="sxs-lookup"><span data-stu-id="51187-133">**ImageList\_Replace**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_replace)
-   [<span data-ttu-id="51187-134">**\_Реплацеикон ImageList**</span><span class="sxs-lookup"><span data-stu-id="51187-134">**ImageList\_ReplaceIcon**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_replaceicon)
-   [<span data-ttu-id="51187-135">**\_Сетбкколор ImageList**</span><span class="sxs-lookup"><span data-stu-id="51187-135">**ImageList\_SetBkColor**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setbkcolor)
-   [<span data-ttu-id="51187-136">**\_Сетколортабле ImageList**</span><span class="sxs-lookup"><span data-stu-id="51187-136">**ImageList\_SetColorTable**</span></span>](imagelist-setcolortable.md)
-   [<span data-ttu-id="51187-137">**\_Сетдрагкурсоримаже ImageList**</span><span class="sxs-lookup"><span data-stu-id="51187-137">**ImageList\_SetDragCursorImage**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setdragcursorimage)
-   [<span data-ttu-id="51187-138">**\_Сетиконсизе ImageList**</span><span class="sxs-lookup"><span data-stu-id="51187-138">**ImageList\_SetIconSize**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_seticonsize)
-   [<span data-ttu-id="51187-139">**\_Сетимажекаунт ImageList**</span><span class="sxs-lookup"><span data-stu-id="51187-139">**ImageList\_SetImageCount**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setimagecount)
-   [<span data-ttu-id="51187-140">**\_Сетоверлайимаже ImageList**</span><span class="sxs-lookup"><span data-stu-id="51187-140">**ImageList\_SetOverlayImage**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setoverlayimage)
-   [<span data-ttu-id="51187-141">**\_Запись ImageList**</span><span class="sxs-lookup"><span data-stu-id="51187-141">**ImageList\_Write**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_write)
-   [<span data-ttu-id="51187-142">**\_Вритикс ImageList**</span><span class="sxs-lookup"><span data-stu-id="51187-142">**ImageList\_WriteEx**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_writeex)

 

 





---
title: Сообщение TVM_SETIMAGELIST (Коммктрл. h)
description: Задает стандартный список или изображение состояния для элемента управления "представление дерева" и перерисовывает элемент управления с помощью новых изображений. Это сообщение можно отправить явно или с помощью \_ макроса Сетимажелист TreeView.
ms.assetid: 1a7bf2f8-c7db-44a8-b234-0ffc498e9000
keywords:
- Элементы управления Windows для TVM_SETIMAGELIST сообщений
topic_type:
- apiref
api_name:
- TVM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f308cb8a56b2e74a5703af144bac03c271efc95
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802315"
---
# <a name="tvm_setimagelist-message"></a><span data-ttu-id="d7d0b-105">\_Сообщение TVM сетимажелист</span><span class="sxs-lookup"><span data-stu-id="d7d0b-105">TVM\_SETIMAGELIST message</span></span>

<span data-ttu-id="d7d0b-106">Задает стандартный список или изображение состояния для элемента управления "представление дерева" и перерисовывает элемент управления с помощью новых изображений.</span><span class="sxs-lookup"><span data-stu-id="d7d0b-106">Sets the normal or state image list for a tree-view control and redraws the control using the new images.</span></span> <span data-ttu-id="d7d0b-107">Это сообщение можно отправить явно или с помощью макроса [**\_ сетимажелист TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setimagelist) .</span><span class="sxs-lookup"><span data-stu-id="d7d0b-107">You can send this message explicitly or by using the [**TreeView\_SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d7d0b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d7d0b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7d0b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d7d0b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d7d0b-110">Тип списка изображений для задания.</span><span class="sxs-lookup"><span data-stu-id="d7d0b-110">Type of image list to set.</span></span> <span data-ttu-id="d7d0b-111">Этот параметр может принимать одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="d7d0b-111">This parameter can be one of the following values:</span></span>



| <span data-ttu-id="d7d0b-112">Значение</span><span class="sxs-lookup"><span data-stu-id="d7d0b-112">Value</span></span>                                                                                                                                                      | <span data-ttu-id="d7d0b-113">Значение</span><span class="sxs-lookup"><span data-stu-id="d7d0b-113">Meaning</span></span>                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVSIL_NORMAL"></span><span id="tvsil_normal"></span><dl> <span data-ttu-id="d7d0b-114"><dt>**ТВСИЛ, \_ Обычная**</dt></span><span class="sxs-lookup"><span data-stu-id="d7d0b-114"><dt>**TVSIL\_NORMAL**</dt></span></span> </dl> | <span data-ttu-id="d7d0b-115">Указывает на нормальный список изображений, который содержит выделенные, невыбранные и наложенные изображения для элементов элемента управления "дерево-представление".</span><span class="sxs-lookup"><span data-stu-id="d7d0b-115">Indicates the normal image list, which contains selected, nonselected, and overlay images for the items of a tree-view control.</span></span><br/>                                                          |
| <span id="TVSIL_STATE"></span><span id="tvsil_state"></span><dl> <span data-ttu-id="d7d0b-116"><dt>**\_состояние твсил**</dt></span><span class="sxs-lookup"><span data-stu-id="d7d0b-116"><dt>**TVSIL\_STATE**</dt></span></span> </dl>    | <span data-ttu-id="d7d0b-117">Указывает список изображений состояния.</span><span class="sxs-lookup"><span data-stu-id="d7d0b-117">Indicates the state image list.</span></span> <span data-ttu-id="d7d0b-118">Изображения состояний можно использовать для обозначения состояний элементов, определенных приложением.</span><span class="sxs-lookup"><span data-stu-id="d7d0b-118">You can use state images to indicate application-defined item states.</span></span> <span data-ttu-id="d7d0b-119">Изображение состояния отображается слева от выбранного или невыделенного изображения элемента.</span><span class="sxs-lookup"><span data-stu-id="d7d0b-119">A state image is displayed to the left of an item's selected or nonselected image.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d7d0b-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d7d0b-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d7d0b-121">Обработчик для списка изображений.</span><span class="sxs-lookup"><span data-stu-id="d7d0b-121">Handle to the image list.</span></span> <span data-ttu-id="d7d0b-122">Если параметр *lParam* имеет **значение NULL**, сообщение удаляет указанный список изображений из элемента управления "дерево-представление".</span><span class="sxs-lookup"><span data-stu-id="d7d0b-122">If *lParam* is **NULL**, the message removes the specified image list from the tree-view control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7d0b-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d7d0b-123">Return value</span></span>

<span data-ttu-id="d7d0b-124">Возвращает маркер для предыдущего списка изображений, если он есть, или **значение NULL** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="d7d0b-124">Returns the handle to the previous image list, if any, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7d0b-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d7d0b-125">Remarks</span></span>

<span data-ttu-id="d7d0b-126">Элемент управления "дерево-представление" не уничтожает список изображений, указанный в этом сообщении.</span><span class="sxs-lookup"><span data-stu-id="d7d0b-126">The tree-view control will not destroy the image list specified with this message.</span></span> <span data-ttu-id="d7d0b-127">Приложение должно уничтожить список изображений, если он больше не нужен.</span><span class="sxs-lookup"><span data-stu-id="d7d0b-127">Your application must destroy the image list when it is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7d0b-128">Требования</span><span class="sxs-lookup"><span data-stu-id="d7d0b-128">Requirements</span></span>



| <span data-ttu-id="d7d0b-129">Требование</span><span class="sxs-lookup"><span data-stu-id="d7d0b-129">Requirement</span></span> | <span data-ttu-id="d7d0b-130">Значение</span><span class="sxs-lookup"><span data-stu-id="d7d0b-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d7d0b-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d7d0b-131">Minimum supported client</span></span><br/> | <span data-ttu-id="d7d0b-132">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d7d0b-132">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d7d0b-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d7d0b-133">Minimum supported server</span></span><br/> | <span data-ttu-id="d7d0b-134">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d7d0b-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d7d0b-135">Header</span><span class="sxs-lookup"><span data-stu-id="d7d0b-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7d0b-136"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7d0b-136"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7d0b-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d7d0b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7d0b-138">**TVM. \_ ImageList**</span><span class="sxs-lookup"><span data-stu-id="d7d0b-138">**TVM\_GETIMAGELIST**</span></span>](tvm-getimagelist.md)
</dt> </dl>

 

 






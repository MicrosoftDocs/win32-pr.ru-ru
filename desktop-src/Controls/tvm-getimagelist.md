---
title: Сообщение TVM_GETIMAGELIST (Коммктрл. h)
description: Получает маркер для обычного или нештатного списка изображений, связанных с элементом управления "дерево-представление". Это сообщение можно отправить явным образом или с помощью \_ макроса TreeView.
ms.assetid: bcf5eac8-cb07-4cf8-ad93-47319fc915a5
keywords:
- Элементы управления Windows для TVM_GETIMAGELIST сообщений
topic_type:
- apiref
api_name:
- TVM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e4e2503d9c6d57743059ee1da3049a36ed17f2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803694"
---
# <a name="tvm_getimagelist-message"></a><span data-ttu-id="7c3ff-105">Сообщение TVM/ \_ ImageList</span><span class="sxs-lookup"><span data-stu-id="7c3ff-105">TVM\_GETIMAGELIST message</span></span>

<span data-ttu-id="7c3ff-106">Получает маркер для обычного или нештатного списка изображений, связанных с элементом управления "дерево-представление".</span><span class="sxs-lookup"><span data-stu-id="7c3ff-106">Retrieves the handle to the normal or state image list associated with a tree-view control.</span></span> <span data-ttu-id="7c3ff-107">Это сообщение можно отправить явным образом или с помощью макроса [**TreeView \_**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getimagelist) .</span><span class="sxs-lookup"><span data-stu-id="7c3ff-107">You can send this message explicitly or by using the [**TreeView\_GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="7c3ff-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7c3ff-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c3ff-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7c3ff-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7c3ff-110">Тип списка изображений для извлечения.</span><span class="sxs-lookup"><span data-stu-id="7c3ff-110">Type of image list to retrieve.</span></span> <span data-ttu-id="7c3ff-111">Этот параметр может принимать одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="7c3ff-111">This parameter can be one of the following values:</span></span>



| <span data-ttu-id="7c3ff-112">Значение</span><span class="sxs-lookup"><span data-stu-id="7c3ff-112">Value</span></span>                                                                                                                                                      | <span data-ttu-id="7c3ff-113">Значение</span><span class="sxs-lookup"><span data-stu-id="7c3ff-113">Meaning</span></span>                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVSIL_NORMAL"></span><span id="tvsil_normal"></span><dl> <span data-ttu-id="7c3ff-114"><dt>**ТВСИЛ, \_ Обычная**</dt></span><span class="sxs-lookup"><span data-stu-id="7c3ff-114"><dt>**TVSIL\_NORMAL**</dt></span></span> </dl> | <span data-ttu-id="7c3ff-115">Указывает на нормальный список изображений, который содержит выделенные, невыбранные и наложенные изображения для элементов элемента управления "дерево-представление".</span><span class="sxs-lookup"><span data-stu-id="7c3ff-115">Indicates the normal image list, which contains selected, nonselected, and overlay images for the items of a tree-view control.</span></span><br/>                                                          |
| <span id="TVSIL_STATE"></span><span id="tvsil_state"></span><dl> <span data-ttu-id="7c3ff-116"><dt>**\_состояние твсил**</dt></span><span class="sxs-lookup"><span data-stu-id="7c3ff-116"><dt>**TVSIL\_STATE**</dt></span></span> </dl>    | <span data-ttu-id="7c3ff-117">Указывает список изображений состояния.</span><span class="sxs-lookup"><span data-stu-id="7c3ff-117">Indicates the state image list.</span></span> <span data-ttu-id="7c3ff-118">Изображения состояний можно использовать для обозначения состояний элементов, определенных приложением.</span><span class="sxs-lookup"><span data-stu-id="7c3ff-118">You can use state images to indicate application-defined item states.</span></span> <span data-ttu-id="7c3ff-119">Изображение состояния отображается слева от выбранного или невыделенного изображения элемента.</span><span class="sxs-lookup"><span data-stu-id="7c3ff-119">A state image is displayed to the left of an item's selected or nonselected image.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="7c3ff-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7c3ff-120">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="7c3ff-121">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="7c3ff-121">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c3ff-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7c3ff-122">Return value</span></span>

<span data-ttu-id="7c3ff-123">Возвращает маркер ХИМАЖЕЛИСТ для указанного списка изображений.</span><span class="sxs-lookup"><span data-stu-id="7c3ff-123">Returns an HIMAGELIST handle to the specified image list.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c3ff-124">Требования</span><span class="sxs-lookup"><span data-stu-id="7c3ff-124">Requirements</span></span>



| <span data-ttu-id="7c3ff-125">Требование</span><span class="sxs-lookup"><span data-stu-id="7c3ff-125">Requirement</span></span> | <span data-ttu-id="7c3ff-126">Значение</span><span class="sxs-lookup"><span data-stu-id="7c3ff-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7c3ff-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7c3ff-127">Minimum supported client</span></span><br/> | <span data-ttu-id="7c3ff-128">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7c3ff-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7c3ff-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7c3ff-129">Minimum supported server</span></span><br/> | <span data-ttu-id="7c3ff-130">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7c3ff-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7c3ff-131">Header</span><span class="sxs-lookup"><span data-stu-id="7c3ff-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c3ff-132"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c3ff-132"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c3ff-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7c3ff-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c3ff-134">**TVM \_ сетимажелист**</span><span class="sxs-lookup"><span data-stu-id="7c3ff-134">**TVM\_SETIMAGELIST**</span></span>](tvm-setimagelist.md)
</dt> </dl>

 

 






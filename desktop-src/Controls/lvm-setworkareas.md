---
title: Сообщение LVM_SETWORKAREAS (Коммктрл. h)
description: Задает рабочие области в элементе управления "представление списка". Это сообщение можно отправить явным образом или использовать \_ макрос Сетворкареас ListView.
ms.assetid: 87ac192d-f481-43ac-b8a5-c754cf33e487
keywords:
- Элементы управления Windows для LVM_SETWORKAREAS сообщений
topic_type:
- apiref
api_name:
- LVM_SETWORKAREAS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4166238c97b5766a5f2bbb19e0de853526d83385
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989166"
---
# <a name="lvm_setworkareas-message"></a><span data-ttu-id="fb288-105">\_Сообщение LVM сетворкареас</span><span class="sxs-lookup"><span data-stu-id="fb288-105">LVM\_SETWORKAREAS message</span></span>

<span data-ttu-id="fb288-106">Задает рабочие области в элементе управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="fb288-106">Sets the working areas within a list-view control.</span></span> <span data-ttu-id="fb288-107">Это сообщение можно отправить явным образом или использовать макрос [**\_ сетворкареас ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setworkareas) .</span><span class="sxs-lookup"><span data-stu-id="fb288-107">You can send this message explicitly or use the [**ListView\_SetWorkAreas**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setworkareas) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="fb288-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="fb288-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb288-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fb288-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fb288-110">Число структур в массиве по адресу *ЛПРК*.</span><span class="sxs-lookup"><span data-stu-id="fb288-110">The number of structures in the array at *lprc*.</span></span> <span data-ttu-id="fb288-111">Максимально допустимое количество рабочих областей определяется \_ \_ ЗНАЧЕНИЕМ параметра LV Max воркареас.</span><span class="sxs-lookup"><span data-stu-id="fb288-111">The maximum number of working areas allowed is defined by the LV\_MAX\_WORKAREAS value.</span></span>

</dd> <dt>

<span data-ttu-id="fb288-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fb288-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fb288-113">Указатель на массив структур [**Rect**](/previous-versions//dd162897(v=vs.85)) , содержащих новые рабочие области элемента управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="fb288-113">Pointer to an array of [**RECT**](/previous-versions//dd162897(v=vs.85)) structures that contain the new working areas of the list-view control.</span></span> <span data-ttu-id="fb288-114">Значения в этих структурах находятся в клиентских координатах.</span><span class="sxs-lookup"><span data-stu-id="fb288-114">Values in these structures are in client coordinates.</span></span> <span data-ttu-id="fb288-115">Если этот параметр имеет **значение NULL**, то Рабочая область будет задаваться в клиентской области элемента управления.</span><span class="sxs-lookup"><span data-stu-id="fb288-115">If this parameter is **NULL**, the working area will be set to the client area of the control.</span></span> <span data-ttu-id="fb288-116">*wParam* задает количество структур в этом массиве.</span><span class="sxs-lookup"><span data-stu-id="fb288-116">*wParam* specifies the number of structures in this array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb288-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fb288-117">Return value</span></span>

<span data-ttu-id="fb288-118">Возвращаемое значение для этого сообщения не используется.</span><span class="sxs-lookup"><span data-stu-id="fb288-118">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb288-119">Требования</span><span class="sxs-lookup"><span data-stu-id="fb288-119">Requirements</span></span>



| <span data-ttu-id="fb288-120">Требование</span><span class="sxs-lookup"><span data-stu-id="fb288-120">Requirement</span></span> | <span data-ttu-id="fb288-121">Значение</span><span class="sxs-lookup"><span data-stu-id="fb288-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fb288-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fb288-122">Minimum supported client</span></span><br/> | <span data-ttu-id="fb288-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fb288-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fb288-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fb288-124">Minimum supported server</span></span><br/> | <span data-ttu-id="fb288-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fb288-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fb288-126">Header</span><span class="sxs-lookup"><span data-stu-id="fb288-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb288-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb288-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb288-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fb288-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb288-129">Использование элементов управления List-View</span><span class="sxs-lookup"><span data-stu-id="fb288-129">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 


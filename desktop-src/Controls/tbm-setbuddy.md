---
title: Сообщение TBM_SETBUDDY (Коммктрл. h)
description: Назначает окно в качестве дружественного окна для элемента управления TrackBar. Элементы TrackBar. окна автоматически отображаются в расположении относительно ориентации элемента управления (по горизонтали или по вертикали).
ms.assetid: ab35911f-bf81-47f3-98aa-0901aa877dea
keywords:
- Элементы управления Windows для TBM_SETBUDDY сообщений
topic_type:
- apiref
api_name:
- TBM_SETBUDDY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab33e53117933390d7a34ec75a49724003255108
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071324"
---
# <a name="tbm_setbuddy-message"></a><span data-ttu-id="5328c-105">\_Сообщение ТБМ сетбудди</span><span class="sxs-lookup"><span data-stu-id="5328c-105">TBM\_SETBUDDY message</span></span>

<span data-ttu-id="5328c-106">Назначает окно в качестве дружественного окна для элемента управления TrackBar.</span><span class="sxs-lookup"><span data-stu-id="5328c-106">Assigns a window as the buddy window for a trackbar control.</span></span> <span data-ttu-id="5328c-107">Элементы TrackBar. окна автоматически отображаются в расположении относительно ориентации элемента управления (по горизонтали или по вертикали).</span><span class="sxs-lookup"><span data-stu-id="5328c-107">Trackbar buddy windows are automatically displayed in a location relative to the control's orientation (horizontal or vertical).</span></span>

## <a name="parameters"></a><span data-ttu-id="5328c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="5328c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5328c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5328c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5328c-110">Значение, указывающее расположение, в котором будет отображаться окно собеседника.</span><span class="sxs-lookup"><span data-stu-id="5328c-110">Value specifying the location at which to display the buddy window.</span></span> <span data-ttu-id="5328c-111">Значение может быть одним из следующих.</span><span class="sxs-lookup"><span data-stu-id="5328c-111">This value can be one of the following:</span></span>



| <span data-ttu-id="5328c-112">Значение</span><span class="sxs-lookup"><span data-stu-id="5328c-112">Value</span></span>                                                                                                                                | <span data-ttu-id="5328c-113">Значение</span><span class="sxs-lookup"><span data-stu-id="5328c-113">Meaning</span></span>                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <span data-ttu-id="5328c-114"><dt>**УСЛОВИЯ**</dt></span><span class="sxs-lookup"><span data-stu-id="5328c-114"><dt>**TRUE**</dt></span></span> </dl>    | <span data-ttu-id="5328c-115">Если элемент управления TrackBar использует стиль [**TBS \_ горизонтали**](trackbar-control-styles.md) , то в левой части ползунка будет отображаться друг.</span><span class="sxs-lookup"><span data-stu-id="5328c-115">The buddy will appear to the left of the trackbar if the trackbar control uses the [**TBS\_HORZ**](trackbar-control-styles.md) style.</span></span> <span data-ttu-id="5328c-116">Если значение TrackBar использует стиль [**по \_ вертикали**](trackbar-control-styles.md) , то он отображается над элементом управления TrackBar.</span><span class="sxs-lookup"><span data-stu-id="5328c-116">If the trackbar uses the [**TBS\_VERT**](trackbar-control-styles.md) style, the buddy appears above the trackbar control.</span></span><br/>  |
| <span id="FALSE"></span><span id="false"></span><dl> <span data-ttu-id="5328c-117"><dt>**ISFALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="5328c-117"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="5328c-118">Контакт будет отображаться справа от TrackBar, если элемент управления TrackBar использует стиль [**TBS \_ горизонтали**](trackbar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="5328c-118">The buddy will appear to the right of the trackbar if the trackbar control uses the [**TBS\_HORZ**](trackbar-control-styles.md) style.</span></span> <span data-ttu-id="5328c-119">Если ползунок использует стиль [**по \_ вертикали**](trackbar-control-styles.md) , то он отображается под элементом управления TrackBar.</span><span class="sxs-lookup"><span data-stu-id="5328c-119">If the trackbar uses the [**TBS\_VERT**](trackbar-control-styles.md) style, the buddy appears below the trackbar control.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5328c-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5328c-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5328c-121">Маркер окна, который будет установлен в качестве собеседника элемента управления TrackBar.</span><span class="sxs-lookup"><span data-stu-id="5328c-121">Handle to the window that will be set as the trackbar control's buddy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5328c-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5328c-122">Return value</span></span>

<span data-ttu-id="5328c-123">Возвращает маркер окна, которое ранее было назначено элементу управления в этом расположении.</span><span class="sxs-lookup"><span data-stu-id="5328c-123">Returns the handle to the window that was previously assigned to the control at that location.</span></span>

## <a name="remarks"></a><span data-ttu-id="5328c-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5328c-124">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5328c-125">Элементы управления TrackBar поддерживают до двух окон с двумя собеседниками.</span><span class="sxs-lookup"><span data-stu-id="5328c-125">Trackbar controls support up to two buddy windows.</span></span> <span data-ttu-id="5328c-126">Это может быть полезно, когда необходимо отображать текст или изображения на каждом конце элемента управления.</span><span class="sxs-lookup"><span data-stu-id="5328c-126">This can be useful when you must display text or images at each end of the control.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5328c-127">Требования</span><span class="sxs-lookup"><span data-stu-id="5328c-127">Requirements</span></span>



| <span data-ttu-id="5328c-128">Требование</span><span class="sxs-lookup"><span data-stu-id="5328c-128">Requirement</span></span> | <span data-ttu-id="5328c-129">Значение</span><span class="sxs-lookup"><span data-stu-id="5328c-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5328c-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5328c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="5328c-131">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5328c-131">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5328c-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5328c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="5328c-133">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5328c-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5328c-134">Header</span><span class="sxs-lookup"><span data-stu-id="5328c-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="5328c-135"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="5328c-135"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






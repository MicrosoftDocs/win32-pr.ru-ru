---
title: Сообщение HDM_GETIMAGELIST (Коммктрл. h)
description: Возвращает маркер для списка изображений, установленного для существующего элемента управления "заголовок". Это сообщение можно отправить явным образом или воспользоваться заголовком \_ \_ макроса жетстатеимажелист заголовка.
ms.assetid: 3e1a979c-60c5-4538-bd4d-16238829062e
keywords:
- Элементы управления Windows для HDM_GETIMAGELIST сообщений
topic_type:
- apiref
api_name:
- HDM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e199d603af873f1957d33855ccf5c59a90a4002
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802860"
---
# <a name="hdm_getimagelist-message"></a><span data-ttu-id="9588f-105">Сообщение HDM в виде \_ ImageList</span><span class="sxs-lookup"><span data-stu-id="9588f-105">HDM\_GETIMAGELIST message</span></span>

<span data-ttu-id="9588f-106">Возвращает маркер для списка изображений, установленного для существующего элемента управления "заголовок".</span><span class="sxs-lookup"><span data-stu-id="9588f-106">Gets the handle to the image list that has been set for an existing header control.</span></span> <span data-ttu-id="9588f-107">Это сообщение можно отправить явным образом или воспользоваться заголовком макроса [**\_ жетстатеимажелист**](/windows/desktop/api/Commctrl/nf-commctrl-header_getstateimagelist) [**заголовка \_**](/windows/desktop/api/Commctrl/nf-commctrl-header_getimagelist) .</span><span class="sxs-lookup"><span data-stu-id="9588f-107">You can send this message explicitly or use the [**Header\_GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_getimagelist) or [**Header\_GetStateImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_getstateimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="9588f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9588f-108">Parameters</span></span>

<dl> <span data-ttu-id="9588f-109"><dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="9588f-109"><dt>*wParam* </dt> </span></span><dd><span data-ttu-id="9588f-110">Одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="9588f-110">One of the following values:</span></span>

| <span data-ttu-id="9588f-111">Значение</span><span class="sxs-lookup"><span data-stu-id="9588f-111">Value</span></span>                                                                                                                                                      | <span data-ttu-id="9588f-112">Значение</span><span class="sxs-lookup"><span data-stu-id="9588f-112">Meaning</span></span>                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="HDSIL_NORMAL"></span><span id="hdsil_normal"></span><dl> <span data-ttu-id="9588f-113"><dt>**ХДСИЛ, \_ Обычная**</dt></span><span class="sxs-lookup"><span data-stu-id="9588f-113"><dt>**HDSIL\_NORMAL**</dt></span></span> </dl> | <span data-ttu-id="9588f-114">Указывает, что это стандартный список изображений.</span><span class="sxs-lookup"><span data-stu-id="9588f-114">Indicates that this is a normal image list.</span></span><br/> |
| <span id="HDSIL_STATE"></span><span id="hdsil_state"></span><dl> <span data-ttu-id="9588f-115"><dt>**\_состояние хдсил**</dt></span><span class="sxs-lookup"><span data-stu-id="9588f-115"><dt>**HDSIL\_STATE**</dt></span></span> </dl>    | <span data-ttu-id="9588f-116">Указывает, что это список изображений состояния.</span><span class="sxs-lookup"><span data-stu-id="9588f-116">Indicates that this is a state image list.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="9588f-117">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9588f-117">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="9588f-118">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="9588f-118">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9588f-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9588f-119">Return value</span></span>

<span data-ttu-id="9588f-120">Возвращает маркер, заданный для элемента управления "заголовок" в списке изображений.</span><span class="sxs-lookup"><span data-stu-id="9588f-120">Returns a handle to the image list set for the header control.</span></span>

## <a name="requirements"></a><span data-ttu-id="9588f-121">Требования</span><span class="sxs-lookup"><span data-stu-id="9588f-121">Requirements</span></span>



| <span data-ttu-id="9588f-122">Требование</span><span class="sxs-lookup"><span data-stu-id="9588f-122">Requirement</span></span> | <span data-ttu-id="9588f-123">Значение</span><span class="sxs-lookup"><span data-stu-id="9588f-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9588f-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9588f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="9588f-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9588f-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9588f-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9588f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="9588f-127">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9588f-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9588f-128">Header</span><span class="sxs-lookup"><span data-stu-id="9588f-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="9588f-129"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="9588f-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






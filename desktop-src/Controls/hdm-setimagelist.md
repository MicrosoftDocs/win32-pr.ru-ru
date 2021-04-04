---
title: Сообщение HDM_SETIMAGELIST (Коммктрл. h)
description: Присваивает список изображений существующему элементу управления "заголовок". Вы можете явно отправить это сообщение или использовать макрос Header \_ сетимажелист или Header \_ сетстатеимажелист.
ms.assetid: 1d7f07fa-f6f4-422a-949c-97d0388343e3
keywords:
- Элементы управления Windows для HDM_SETIMAGELIST сообщений
topic_type:
- apiref
api_name:
- HDM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17fe21d64b141cf27d32e00fac0ce78228421518
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988596"
---
# <a name="hdm_setimagelist-message"></a><span data-ttu-id="d0c7c-105">\_Сообщение СЕТИМАЖЕЛИСТ HDM</span><span class="sxs-lookup"><span data-stu-id="d0c7c-105">HDM\_SETIMAGELIST message</span></span>

<span data-ttu-id="d0c7c-106">Присваивает список изображений существующему элементу управления "заголовок".</span><span class="sxs-lookup"><span data-stu-id="d0c7c-106">Assigns an image list to an existing header control.</span></span> <span data-ttu-id="d0c7c-107">Вы можете явно отправить это сообщение или использовать макрос [**Header \_ Сетимажелист**](/windows/desktop/api/Commctrl/nf-commctrl-header_setimagelist) или [**Header \_ сетстатеимажелист**](/windows/desktop/api/Commctrl/nf-commctrl-header_setstateimagelist) .</span><span class="sxs-lookup"><span data-stu-id="d0c7c-107">You can send this message explicitly or use the [**Header\_SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_setimagelist) or [**Header\_SetStateImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_setstateimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d0c7c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d0c7c-108">Parameters</span></span>

<dl> <span data-ttu-id="d0c7c-109"><dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="d0c7c-109"><dt>*wParam* </dt> </span></span><dd><span data-ttu-id="d0c7c-110">Одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="d0c7c-110">One of the following values:</span></span>

| <span data-ttu-id="d0c7c-111">Значение</span><span class="sxs-lookup"><span data-stu-id="d0c7c-111">Value</span></span>                                                                                                                                                      | <span data-ttu-id="d0c7c-112">Значение</span><span class="sxs-lookup"><span data-stu-id="d0c7c-112">Meaning</span></span>                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="HDSIL_NORMAL"></span><span id="hdsil_normal"></span><dl> <span data-ttu-id="d0c7c-113"><dt>**ХДСИЛ, \_ Обычная**</dt></span><span class="sxs-lookup"><span data-stu-id="d0c7c-113"><dt>**HDSIL\_NORMAL**</dt></span></span> </dl> | <span data-ttu-id="d0c7c-114">Указывает, что это стандартный список изображений.</span><span class="sxs-lookup"><span data-stu-id="d0c7c-114">Indicates that this is a normal image list.</span></span><br/> |
| <span id="HDSIL_STATE"></span><span id="hdsil_state"></span><dl> <span data-ttu-id="d0c7c-115"><dt>**\_состояние хдсил**</dt></span><span class="sxs-lookup"><span data-stu-id="d0c7c-115"><dt>**HDSIL\_STATE**</dt></span></span> </dl>    | <span data-ttu-id="d0c7c-116">Указывает, что это список изображений состояния.</span><span class="sxs-lookup"><span data-stu-id="d0c7c-116">Indicates that this is a state image list.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="d0c7c-117">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d0c7c-117">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d0c7c-118">Маркер для списка изображений.</span><span class="sxs-lookup"><span data-stu-id="d0c7c-118">A handle to an image list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0c7c-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d0c7c-119">Return value</span></span>

<span data-ttu-id="d0c7c-120">Возвращает маркер в список изображений, ранее связанный с элементом управления.</span><span class="sxs-lookup"><span data-stu-id="d0c7c-120">Returns the handle to the image list previously associated with the control.</span></span> <span data-ttu-id="d0c7c-121">Возвращает **значение NULL** при сбое или если список изображений не был задан ранее.</span><span class="sxs-lookup"><span data-stu-id="d0c7c-121">Returns **NULL** upon failure or if no image list was set previously.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0c7c-122">Требования</span><span class="sxs-lookup"><span data-stu-id="d0c7c-122">Requirements</span></span>



| <span data-ttu-id="d0c7c-123">Требование</span><span class="sxs-lookup"><span data-stu-id="d0c7c-123">Requirement</span></span> | <span data-ttu-id="d0c7c-124">Значение</span><span class="sxs-lookup"><span data-stu-id="d0c7c-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d0c7c-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d0c7c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d0c7c-126">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d0c7c-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d0c7c-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d0c7c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d0c7c-128">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d0c7c-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d0c7c-129">Header</span><span class="sxs-lookup"><span data-stu-id="d0c7c-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0c7c-130"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0c7c-130"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






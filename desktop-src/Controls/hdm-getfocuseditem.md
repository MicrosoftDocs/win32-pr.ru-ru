---
title: Сообщение HDM_GETFOCUSEDITEM (Коммктрл. h)
description: Возвращает элемент в элементе управления "заголовок", который находится в фокусе. Отправляйте это сообщение явным образом или с помощью \_ макроса Жетфокуседитем заголовка.
ms.assetid: 9ad8e497-6f81-4226-b138-d1101f2fd8b3
keywords:
- Элементы управления Windows для HDM_GETFOCUSEDITEM сообщений
topic_type:
- apiref
api_name:
- HDM_GETFOCUSEDITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c21fcb29f5f431e32ca3f07265b7e96620d5a67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491478"
---
# <a name="hdm_getfocuseditem-message"></a><span data-ttu-id="9567f-105">\_Сообщение ЖЕТФОКУСЕДИТЕМ HDM</span><span class="sxs-lookup"><span data-stu-id="9567f-105">HDM\_GETFOCUSEDITEM message</span></span>

<span data-ttu-id="9567f-106">Возвращает элемент в элементе управления "заголовок", который находится в фокусе.</span><span class="sxs-lookup"><span data-stu-id="9567f-106">Gets the item in a header control that has the focus.</span></span> <span data-ttu-id="9567f-107">Отправляйте это сообщение явным образом или с помощью макроса [**\_ жетфокуседитем заголовка**](/windows/desktop/api/Commctrl/nf-commctrl-header_getfocuseditem) .</span><span class="sxs-lookup"><span data-stu-id="9567f-107">Send this message explicitly or by using the [**Header\_GetFocusedItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_getfocuseditem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="9567f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9567f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9567f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9567f-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="9567f-110">Не используется.</span><span class="sxs-lookup"><span data-stu-id="9567f-110">Not used.</span></span> <span data-ttu-id="9567f-111">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="9567f-111">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="9567f-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9567f-112">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="9567f-113">Не используется.</span><span class="sxs-lookup"><span data-stu-id="9567f-113">Not used.</span></span> <span data-ttu-id="9567f-114">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="9567f-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9567f-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9567f-115">Return value</span></span>

<span data-ttu-id="9567f-116">Возвращает индекс элемента в фокусе.</span><span class="sxs-lookup"><span data-stu-id="9567f-116">Returns the index of the item in focus.</span></span>

## <a name="requirements"></a><span data-ttu-id="9567f-117">Требования</span><span class="sxs-lookup"><span data-stu-id="9567f-117">Requirements</span></span>



| <span data-ttu-id="9567f-118">Требование</span><span class="sxs-lookup"><span data-stu-id="9567f-118">Requirement</span></span> | <span data-ttu-id="9567f-119">Значение</span><span class="sxs-lookup"><span data-stu-id="9567f-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9567f-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9567f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9567f-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9567f-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9567f-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9567f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9567f-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9567f-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9567f-124">Header</span><span class="sxs-lookup"><span data-stu-id="9567f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9567f-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="9567f-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9567f-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9567f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9567f-127">Сведения об элементах управления "заголовок"</span><span class="sxs-lookup"><span data-stu-id="9567f-127">About Header Controls</span></span>](header-controls.md)
</dt> </dl>

 

 






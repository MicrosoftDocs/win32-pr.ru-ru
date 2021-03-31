---
title: Сообщение HDM_SETFOCUSEDITEM (Коммктрл. h)
description: Устанавливает фокус на указанный элемент в элементе управления "заголовок". Отправляйте это сообщение явным образом или с помощью \_ макроса Сетфокуседитем заголовка.
ms.assetid: 20a321ce-4420-4239-b34d-9e7f24a89fc3
keywords:
- Элементы управления Windows для HDM_SETFOCUSEDITEM сообщений
topic_type:
- apiref
api_name:
- HDM_SETFOCUSEDITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fd416744478248760f4e2c9f94a362db5a8d327
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136974"
---
# <a name="hdm_setfocuseditem-message"></a><span data-ttu-id="0785b-105">\_Сообщение СЕТФОКУСЕДИТЕМ HDM</span><span class="sxs-lookup"><span data-stu-id="0785b-105">HDM\_SETFOCUSEDITEM message</span></span>

<span data-ttu-id="0785b-106">Устанавливает фокус на указанный элемент в элементе управления "заголовок".</span><span class="sxs-lookup"><span data-stu-id="0785b-106">Sets the focus to a specified item in a header control.</span></span> <span data-ttu-id="0785b-107">Отправляйте это сообщение явным образом или с помощью макроса [**\_ сетфокуседитем заголовка**](/windows/desktop/api/Commctrl/nf-commctrl-header_setfocuseditem) .</span><span class="sxs-lookup"><span data-stu-id="0785b-107">Send this message explicitly or by using the [**Header\_SetFocusedItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_setfocuseditem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="0785b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="0785b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0785b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0785b-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0785b-110">Не используется.</span><span class="sxs-lookup"><span data-stu-id="0785b-110">Not used.</span></span> <span data-ttu-id="0785b-111">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="0785b-111">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="0785b-112">*lParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0785b-112">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0785b-113">Индекс элемента.</span><span class="sxs-lookup"><span data-stu-id="0785b-113">The index of item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0785b-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0785b-114">Return value</span></span>

<span data-ttu-id="0785b-115">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="0785b-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="0785b-116">Требования</span><span class="sxs-lookup"><span data-stu-id="0785b-116">Requirements</span></span>



| <span data-ttu-id="0785b-117">Требование</span><span class="sxs-lookup"><span data-stu-id="0785b-117">Requirement</span></span> | <span data-ttu-id="0785b-118">Значение</span><span class="sxs-lookup"><span data-stu-id="0785b-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0785b-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0785b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0785b-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0785b-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0785b-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0785b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0785b-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0785b-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0785b-123">Header</span><span class="sxs-lookup"><span data-stu-id="0785b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0785b-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="0785b-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0785b-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0785b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0785b-126">Сведения об элементах управления "заголовок"</span><span class="sxs-lookup"><span data-stu-id="0785b-126">About Header Controls</span></span>](header-controls.md)
</dt> </dl>

 

 






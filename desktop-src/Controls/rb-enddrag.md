---
title: Сообщение RB_ENDDRAG (Коммктрл. h)
description: Прерывает операцию перетаскивания элемента управления главной панели. Это сообщение не приводит к \_ отправке уведомления РБН енддраг.
ms.assetid: 4991dda6-32ea-4d3e-9d39-17c2b6995f09
keywords:
- Элементы управления Windows для RB_ENDDRAG сообщений
topic_type:
- apiref
api_name:
- RB_ENDDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b6f201471b6f260555aacb9d89c1363492ed6bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988988"
---
# <a name="rb_enddrag-message"></a><span data-ttu-id="8eaf6-105">\_Сообщение ЕНДДРАГ RB</span><span class="sxs-lookup"><span data-stu-id="8eaf6-105">RB\_ENDDRAG message</span></span>

<span data-ttu-id="8eaf6-106">Прерывает операцию перетаскивания элемента управления главной панели.</span><span class="sxs-lookup"><span data-stu-id="8eaf6-106">Terminates the rebar control's drag-and-drop operation.</span></span> <span data-ttu-id="8eaf6-107">Это сообщение не приводит к отправке уведомления [РБН \_ енддраг](rbn-enddrag.md) .</span><span class="sxs-lookup"><span data-stu-id="8eaf6-107">This message does not cause an [RBN\_ENDDRAG](rbn-enddrag.md) notification to be sent.</span></span>

## <a name="parameters"></a><span data-ttu-id="8eaf6-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8eaf6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8eaf6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8eaf6-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="8eaf6-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="8eaf6-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="8eaf6-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8eaf6-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="8eaf6-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="8eaf6-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8eaf6-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8eaf6-113">Return value</span></span>

<span data-ttu-id="8eaf6-114">Возвращаемое значение для этого сообщения не используется.</span><span class="sxs-lookup"><span data-stu-id="8eaf6-114">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="8eaf6-115">Требования</span><span class="sxs-lookup"><span data-stu-id="8eaf6-115">Requirements</span></span>



| <span data-ttu-id="8eaf6-116">Требование</span><span class="sxs-lookup"><span data-stu-id="8eaf6-116">Requirement</span></span> | <span data-ttu-id="8eaf6-117">Значение</span><span class="sxs-lookup"><span data-stu-id="8eaf6-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8eaf6-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8eaf6-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8eaf6-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8eaf6-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8eaf6-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8eaf6-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8eaf6-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8eaf6-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8eaf6-122">Header</span><span class="sxs-lookup"><span data-stu-id="8eaf6-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8eaf6-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="8eaf6-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8eaf6-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8eaf6-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="8eaf6-125">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="8eaf6-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8eaf6-126">**\_БЕГИНДРАГ RB**</span><span class="sxs-lookup"><span data-stu-id="8eaf6-126">**RB\_BEGINDRAG**</span></span>](rb-begindrag.md)
</dt> <dt>

[<span data-ttu-id="8eaf6-127">**\_ДРАГМОВЕ RB**</span><span class="sxs-lookup"><span data-stu-id="8eaf6-127">**RB\_DRAGMOVE**</span></span>](rb-dragmove.md)
</dt> </dl>

 

 






---
title: Сообщение EM_CANREDO (RichEdit. h)
description: Определяет, есть ли какие либо действия в очереди повторов элемента управления.
ms.assetid: 4a76adc8-f815-4cf7-8742-b7695e5a0f64
keywords:
- Элементы управления Windows для EM_CANREDO сообщений
topic_type:
- apiref
api_name:
- EM_CANREDO
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccfb12f8e72bdf5321151cd3a70b74f322a46591
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892249"
---
# <a name="em_canredo-message"></a><span data-ttu-id="e0cf3-104">\_Сообщение КАНРЕДО EM</span><span class="sxs-lookup"><span data-stu-id="e0cf3-104">EM\_CANREDO message</span></span>

<span data-ttu-id="e0cf3-105">Определяет, есть ли какие либо действия в очереди повторов элемента управления.</span><span class="sxs-lookup"><span data-stu-id="e0cf3-105">Determines whether there are any actions in the control redo queue.</span></span>

## <a name="parameters"></a><span data-ttu-id="e0cf3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e0cf3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0cf3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e0cf3-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e0cf3-108">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="e0cf3-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="e0cf3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e0cf3-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e0cf3-110">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="e0cf3-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0cf3-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e0cf3-111">Return value</span></span>

<span data-ttu-id="e0cf3-112">Если в очереди повторов элемента управления есть действия, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="e0cf3-112">If there are actions in the control redo queue, the return value is a nonzero value.</span></span>

<span data-ttu-id="e0cf3-113">Если очередь повтора пуста, возвращаемое значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="e0cf3-113">If the redo queue is empty, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0cf3-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e0cf3-114">Remarks</span></span>

<span data-ttu-id="e0cf3-115">Чтобы повторить последнюю операцию отмены, отправьте сообщение о [**\_ возврате EM**](em-redo.md) .</span><span class="sxs-lookup"><span data-stu-id="e0cf3-115">To redo the most recent undo operation, send the [**EM\_REDO**](em-redo.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0cf3-116">Требования</span><span class="sxs-lookup"><span data-stu-id="e0cf3-116">Requirements</span></span>



| <span data-ttu-id="e0cf3-117">Требование</span><span class="sxs-lookup"><span data-stu-id="e0cf3-117">Requirement</span></span> | <span data-ttu-id="e0cf3-118">Значение</span><span class="sxs-lookup"><span data-stu-id="e0cf3-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e0cf3-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e0cf3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e0cf3-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e0cf3-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e0cf3-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e0cf3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e0cf3-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e0cf3-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e0cf3-123">Header</span><span class="sxs-lookup"><span data-stu-id="e0cf3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0cf3-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0cf3-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0cf3-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e0cf3-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="e0cf3-126">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="e0cf3-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e0cf3-127">**EM \_ жетредонаме**</span><span class="sxs-lookup"><span data-stu-id="e0cf3-127">**EM\_GETREDONAME**</span></span>](em-getredoname.md)
</dt> <dt>

[<span data-ttu-id="e0cf3-128">**EM \_ жетундонаме**</span><span class="sxs-lookup"><span data-stu-id="e0cf3-128">**EM\_GETUNDONAME**</span></span>](em-getundoname.md)
</dt> <dt>

[<span data-ttu-id="e0cf3-129">**\_Повтор EM**</span><span class="sxs-lookup"><span data-stu-id="e0cf3-129">**EM\_REDO**</span></span>](em-redo.md)
</dt> <dt>

[<span data-ttu-id="e0cf3-130">**\_Отмена EM**</span><span class="sxs-lookup"><span data-stu-id="e0cf3-130">**EM\_UNDO**</span></span>](em-undo.md)
</dt> </dl>

 

 






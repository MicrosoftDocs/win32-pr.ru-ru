---
title: Сообщение EM_SETUNDOLIMIT (RichEdit. h)
description: Задает максимальное число действий, которые могут храниться в очереди отмены элемента управления Rich Edit.
ms.assetid: 485dbcda-89f4-40de-ad55-cd524958e910
keywords:
- Элементы управления Windows для EM_SETUNDOLIMIT сообщений
topic_type:
- apiref
api_name:
- EM_SETUNDOLIMIT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5b668d047f1de6d8720f09af5baf23e7cfc9cc2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988819"
---
# <a name="em_setundolimit-message"></a><span data-ttu-id="ee941-104">\_Сообщение СЕТУНДОЛИМИТ EM</span><span class="sxs-lookup"><span data-stu-id="ee941-104">EM\_SETUNDOLIMIT message</span></span>

<span data-ttu-id="ee941-105">Задает максимальное число действий, которые могут храниться в очереди отмены элемента управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="ee941-105">Sets the maximum number of actions that can stored in the undo queue of a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="ee941-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ee941-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee941-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ee941-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ee941-108">Указывает максимальное число действий, которые могут храниться в очереди отмены.</span><span class="sxs-lookup"><span data-stu-id="ee941-108">Specifies the maximum number of actions that can be stored in the undo queue.</span></span>

</dd> <dt>

<span data-ttu-id="ee941-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ee941-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ee941-110">Этот параметр не используется; оно должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="ee941-110">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee941-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ee941-111">Return value</span></span>

<span data-ttu-id="ee941-112">Возвращаемое значение — это новое максимальное число действий отмены для элемента управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="ee941-112">The return value is the new maximum number of undo actions for the rich edit control.</span></span> <span data-ttu-id="ee941-113">Это значение может быть меньше, чем *wParam* , если память ограничена.</span><span class="sxs-lookup"><span data-stu-id="ee941-113">This value may be less than *wParam* if memory is limited.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee941-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ee941-114">Remarks</span></span>

<span data-ttu-id="ee941-115">По умолчанию максимальное число действий в очереди отмены — 100.</span><span class="sxs-lookup"><span data-stu-id="ee941-115">By default, the maximum number of actions in the undo queue is 100.</span></span> <span data-ttu-id="ee941-116">Если увеличить это число, должно быть достаточно памяти для размещения нового номера.</span><span class="sxs-lookup"><span data-stu-id="ee941-116">If you increase this number, there must be enough available memory to accommodate the new number.</span></span> <span data-ttu-id="ee941-117">Для повышения производительности установите ограничение на наименьшее возможное значение.</span><span class="sxs-lookup"><span data-stu-id="ee941-117">For better performance, set the limit to the smallest possible value.</span></span>

<span data-ttu-id="ee941-118">Если установить ограничение равным нулю, функция **отмены** будет отключена.</span><span class="sxs-lookup"><span data-stu-id="ee941-118">Setting the limit to zero disables the **Undo** feature.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee941-119">Требования</span><span class="sxs-lookup"><span data-stu-id="ee941-119">Requirements</span></span>



| <span data-ttu-id="ee941-120">Требование</span><span class="sxs-lookup"><span data-stu-id="ee941-120">Requirement</span></span> | <span data-ttu-id="ee941-121">Значение</span><span class="sxs-lookup"><span data-stu-id="ee941-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ee941-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ee941-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ee941-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ee941-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ee941-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ee941-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ee941-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ee941-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ee941-126">Header</span><span class="sxs-lookup"><span data-stu-id="ee941-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee941-127"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee941-127"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee941-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ee941-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="ee941-129">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="ee941-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ee941-130">**EM \_ канредо**</span><span class="sxs-lookup"><span data-stu-id="ee941-130">**EM\_CANREDO**</span></span>](em-canredo.md)
</dt> <dt>

[<span data-ttu-id="ee941-131">**EM \_ жетредонаме**</span><span class="sxs-lookup"><span data-stu-id="ee941-131">**EM\_GETREDONAME**</span></span>](em-getredoname.md)
</dt> <dt>

[<span data-ttu-id="ee941-132">**EM \_ жетундонаме**</span><span class="sxs-lookup"><span data-stu-id="ee941-132">**EM\_GETUNDONAME**</span></span>](em-getundoname.md)
</dt> <dt>

[<span data-ttu-id="ee941-133">**\_Повтор EM**</span><span class="sxs-lookup"><span data-stu-id="ee941-133">**EM\_REDO**</span></span>](em-redo.md)
</dt> <dt>

[<span data-ttu-id="ee941-134">**\_Отмена EM**</span><span class="sxs-lookup"><span data-stu-id="ee941-134">**EM\_UNDO**</span></span>](em-undo.md)
</dt> </dl>

 

 






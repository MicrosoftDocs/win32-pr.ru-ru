---
title: Сообщение EM_REDO (RichEdit. h)
description: Отправляет сообщение о \_ возврате EM в форматируемый элемент управления, чтобы повторить следующее действие в очереди повторов элемента управления.
ms.assetid: 28ec1ec2-a56d-442f-b3cb-9feeb92edaeb
keywords:
- Элементы управления Windows для EM_REDO сообщений
topic_type:
- apiref
api_name:
- EM_REDO
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bba7a684db0d40ebcfeec4a540989c4dab4c5dd2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491493"
---
# <a name="em_redo-message"></a><span data-ttu-id="f6fe9-104">\_Сообщение о возврате EM</span><span class="sxs-lookup"><span data-stu-id="f6fe9-104">EM\_REDO message</span></span>

<span data-ttu-id="f6fe9-105">Отправляет сообщение **о \_ возврате EM** в форматируемый элемент управления, чтобы повторить следующее действие в очереди повторов элемента управления.</span><span class="sxs-lookup"><span data-stu-id="f6fe9-105">Sends an **EM\_REDO** message to a rich edit control to redo the next action in the control's redo queue.</span></span>

## <a name="parameters"></a><span data-ttu-id="f6fe9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f6fe9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6fe9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f6fe9-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f6fe9-108">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="f6fe9-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="f6fe9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f6fe9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f6fe9-110">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="f6fe9-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6fe9-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f6fe9-111">Return value</span></span>

<span data-ttu-id="f6fe9-112">Если операция **повтора** завершилась удачно, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="f6fe9-112">If the **Redo** operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="f6fe9-113">Если операция **повтора** завершается неудачно, возвращаемое значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="f6fe9-113">If the **Redo** operation fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6fe9-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f6fe9-114">Remarks</span></span>

<span data-ttu-id="f6fe9-115">Чтобы определить, есть ли какие либо действия в очереди повторов элемента управления, отправьте сообщение [**EM \_ канредо**](em-canredo.md) .</span><span class="sxs-lookup"><span data-stu-id="f6fe9-115">To determine whether there are any actions in the control's redo queue, send the [**EM\_CANREDO**](em-canredo.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6fe9-116">Требования</span><span class="sxs-lookup"><span data-stu-id="f6fe9-116">Requirements</span></span>



| <span data-ttu-id="f6fe9-117">Требование</span><span class="sxs-lookup"><span data-stu-id="f6fe9-117">Requirement</span></span> | <span data-ttu-id="f6fe9-118">Значение</span><span class="sxs-lookup"><span data-stu-id="f6fe9-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f6fe9-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f6fe9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f6fe9-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f6fe9-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f6fe9-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f6fe9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f6fe9-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f6fe9-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f6fe9-123">Header</span><span class="sxs-lookup"><span data-stu-id="f6fe9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6fe9-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6fe9-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6fe9-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f6fe9-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="f6fe9-126">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="f6fe9-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f6fe9-127">**EM \_ канредо**</span><span class="sxs-lookup"><span data-stu-id="f6fe9-127">**EM\_CANREDO**</span></span>](em-canredo.md)
</dt> <dt>

[<span data-ttu-id="f6fe9-128">**EM \_ жетредонаме**</span><span class="sxs-lookup"><span data-stu-id="f6fe9-128">**EM\_GETREDONAME**</span></span>](em-getredoname.md)
</dt> <dt>

[<span data-ttu-id="f6fe9-129">**EM \_ жетундонаме**</span><span class="sxs-lookup"><span data-stu-id="f6fe9-129">**EM\_GETUNDONAME**</span></span>](em-getundoname.md)
</dt> <dt>

[<span data-ttu-id="f6fe9-130">**\_Отмена EM**</span><span class="sxs-lookup"><span data-stu-id="f6fe9-130">**EM\_UNDO**</span></span>](em-undo.md)
</dt> </dl>

 

 






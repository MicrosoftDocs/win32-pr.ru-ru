---
title: Сообщение EM_GETUNDONAME (RichEdit. h)
description: Microsoft Rich Edit 2,0 и более поздних версий Извлекает тип следующего действия отмены, если оно есть. Microsoft Rich Edit 1,0 это сообщение не поддерживается.
ms.assetid: 43351909-f8bc-425a-9d9b-655e3b47eb75
keywords:
- Элементы управления Windows для EM_GETUNDONAME сообщений
topic_type:
- apiref
api_name:
- EM_GETUNDONAME
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0c29b5815da5569059ba80c007d6af39d1e389f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989087"
---
# <a name="em_getundoname-message"></a><span data-ttu-id="1f4ba-104">\_Сообщение ЖЕТУНДОНАМЕ EM</span><span class="sxs-lookup"><span data-stu-id="1f4ba-104">EM\_GETUNDONAME message</span></span>

<span data-ttu-id="1f4ba-105">Microsoft Rich Edit 2,0 и более поздние версии: Извлекает тип следующего действия отмены, если оно есть.</span><span class="sxs-lookup"><span data-stu-id="1f4ba-105">Microsoft Rich Edit 2.0 and later: Retrieves the type of the next undo action, if any.</span></span>

<span data-ttu-id="1f4ba-106">Microsoft Rich Edit 1,0: это сообщение не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1f4ba-106">Microsoft Rich Edit 1.0: This message is not supported.</span></span>

## <a name="parameters"></a><span data-ttu-id="1f4ba-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="1f4ba-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f4ba-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1f4ba-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1f4ba-109">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="1f4ba-109">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="1f4ba-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1f4ba-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1f4ba-111">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="1f4ba-111">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f4ba-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1f4ba-112">Return value</span></span>

<span data-ttu-id="1f4ba-113">Если имеется действие отмены, возвращается значение перечисления [**ундонамеид**](/windows/desktop/api/Richedit/ne-richedit-undonameid) , указывающее тип следующего действия в очереди отмены элемента управления.</span><span class="sxs-lookup"><span data-stu-id="1f4ba-113">If there is an undo action, the value returned is an [**UNDONAMEID**](/windows/desktop/api/Richedit/ne-richedit-undonameid) enumeration value that indicates the type of the next action in the control's undo queue.</span></span>

<span data-ttu-id="1f4ba-114">Если нет действий, которые можно отменить, или тип следующего действия отмены неизвестен, возвращаемое значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="1f4ba-114">If there are no actions that can be undone or the type of the next undo action is unknown, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f4ba-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1f4ba-115">Remarks</span></span>

<span data-ttu-id="1f4ba-116">Типы действий, которые могут быть отменены или повторно выполнены, включают операции ввода, удаления, перетаскивания, удаления, вырезания и вставки.</span><span class="sxs-lookup"><span data-stu-id="1f4ba-116">The types of actions that can be undone or redone include typing, delete, drag, drop, cut, and paste operations.</span></span> <span data-ttu-id="1f4ba-117">Эти сведения могут быть полезны для приложений, которые предоставляют расширенный пользовательский интерфейс для операций отмены и повтора, например раскрывающийся список действий, которые могут быть отменены.</span><span class="sxs-lookup"><span data-stu-id="1f4ba-117">This information can be useful for applications that provide an extended user interface for undo and redo operations, such as a drop-down list box of actions that can be undone.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f4ba-118">Требования</span><span class="sxs-lookup"><span data-stu-id="1f4ba-118">Requirements</span></span>



| <span data-ttu-id="1f4ba-119">Требование</span><span class="sxs-lookup"><span data-stu-id="1f4ba-119">Requirement</span></span> | <span data-ttu-id="1f4ba-120">Значение</span><span class="sxs-lookup"><span data-stu-id="1f4ba-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1f4ba-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1f4ba-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1f4ba-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1f4ba-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1f4ba-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1f4ba-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1f4ba-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1f4ba-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1f4ba-125">Header</span><span class="sxs-lookup"><span data-stu-id="1f4ba-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f4ba-126"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f4ba-126"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f4ba-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1f4ba-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="1f4ba-128">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="1f4ba-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1f4ba-129">**EM \_ жетредонаме**</span><span class="sxs-lookup"><span data-stu-id="1f4ba-129">**EM\_GETREDONAME**</span></span>](em-getredoname.md)
</dt> <dt>

[<span data-ttu-id="1f4ba-130">**\_Повтор EM**</span><span class="sxs-lookup"><span data-stu-id="1f4ba-130">**EM\_REDO**</span></span>](em-redo.md)
</dt> <dt>

[<span data-ttu-id="1f4ba-131">**\_Отмена EM**</span><span class="sxs-lookup"><span data-stu-id="1f4ba-131">**EM\_UNDO**</span></span>](em-undo.md)
</dt> <dt>

[<span data-ttu-id="1f4ba-132">**ундонамеид**</span><span class="sxs-lookup"><span data-stu-id="1f4ba-132">**UNDONAMEID**</span></span>](/windows/desktop/api/Richedit/ne-richedit-undonameid)
</dt> </dl>

 

 






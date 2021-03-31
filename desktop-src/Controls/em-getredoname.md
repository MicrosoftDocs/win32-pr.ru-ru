---
title: Сообщение EM_GETREDONAME (RichEdit. h)
description: Возвращает тип следующего действия (при его наличии) в очереди повтора элемента управления Rich Edit.
ms.assetid: 8649236f-32dc-45d3-847e-c9f65ffba44c
keywords:
- Элементы управления Windows для EM_GETREDONAME сообщений
topic_type:
- apiref
api_name:
- EM_GETREDONAME
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ea44257344b9ebdb8ffe91ad97e939aae0db9b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988767"
---
# <a name="em_getredoname-message"></a><span data-ttu-id="026eb-104">\_Сообщение ЖЕТРЕДОНАМЕ EM</span><span class="sxs-lookup"><span data-stu-id="026eb-104">EM\_GETREDONAME message</span></span>

<span data-ttu-id="026eb-105">Возвращает тип следующего действия (при его наличии) в очереди повтора элемента управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="026eb-105">Retrieves the type of the next action, if any, in the rich edit control's redo queue.</span></span>

## <a name="parameters"></a><span data-ttu-id="026eb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="026eb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="026eb-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="026eb-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="026eb-108">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="026eb-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="026eb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="026eb-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="026eb-110">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="026eb-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="026eb-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="026eb-111">Return value</span></span>

<span data-ttu-id="026eb-112">Если очередь повтора для элемента управления не пуста, возвращается значение перечисления [**ундонамеид**](/windows/desktop/api/Richedit/ne-richedit-undonameid) , указывающее тип следующего действия в очереди повторов элемента управления.</span><span class="sxs-lookup"><span data-stu-id="026eb-112">If the redo queue for the control is not empty, the value returned is an [**UNDONAMEID**](/windows/desktop/api/Richedit/ne-richedit-undonameid) enumeration value that indicates the type of the next action in the control's redo queue.</span></span>

<span data-ttu-id="026eb-113">Если нет действий, доступных для повторяемости, или тип следующего повторяемого действия неизвестен, возвращаемое значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="026eb-113">If there are no redoable actions or the type of the next redoable action is unknown, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="026eb-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="026eb-114">Remarks</span></span>

<span data-ttu-id="026eb-115">Типы действий, которые могут быть отменены или повторно выполнены, включают операции ввода, удаления, перетаскивания, вырезания и вставки.</span><span class="sxs-lookup"><span data-stu-id="026eb-115">The types of actions that can be undone or redone include typing, delete, drag-drop, cut, and paste operations.</span></span> <span data-ttu-id="026eb-116">Эти сведения могут быть полезны для приложений, которые предоставляют расширенный пользовательский интерфейс для операций отмены и повтора, например раскрывающийся список действий, которые можно повторить.</span><span class="sxs-lookup"><span data-stu-id="026eb-116">This information can be useful for applications that provide an extended user interface for undo and redo operations, such as a drop-down list box of redoable actions.</span></span>

## <a name="requirements"></a><span data-ttu-id="026eb-117">Требования</span><span class="sxs-lookup"><span data-stu-id="026eb-117">Requirements</span></span>



| <span data-ttu-id="026eb-118">Требование</span><span class="sxs-lookup"><span data-stu-id="026eb-118">Requirement</span></span> | <span data-ttu-id="026eb-119">Значение</span><span class="sxs-lookup"><span data-stu-id="026eb-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="026eb-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="026eb-120">Minimum supported client</span></span><br/> | <span data-ttu-id="026eb-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="026eb-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="026eb-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="026eb-122">Minimum supported server</span></span><br/> | <span data-ttu-id="026eb-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="026eb-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="026eb-124">Header</span><span class="sxs-lookup"><span data-stu-id="026eb-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="026eb-125"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="026eb-125"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="026eb-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="026eb-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="026eb-127">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="026eb-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="026eb-128">**EM \_ жетундонаме**</span><span class="sxs-lookup"><span data-stu-id="026eb-128">**EM\_GETUNDONAME**</span></span>](em-getundoname.md)
</dt> <dt>

[<span data-ttu-id="026eb-129">**\_Повтор EM**</span><span class="sxs-lookup"><span data-stu-id="026eb-129">**EM\_REDO**</span></span>](em-redo.md)
</dt> <dt>

[<span data-ttu-id="026eb-130">**\_Отмена EM**</span><span class="sxs-lookup"><span data-stu-id="026eb-130">**EM\_UNDO**</span></span>](em-undo.md)
</dt> <dt>

[<span data-ttu-id="026eb-131">**ундонамеид**</span><span class="sxs-lookup"><span data-stu-id="026eb-131">**UNDONAMEID**</span></span>](/windows/desktop/api/Richedit/ne-richedit-undonameid)
</dt> </dl>

 

 






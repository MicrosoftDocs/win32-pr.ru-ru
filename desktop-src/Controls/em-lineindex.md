---
title: Сообщение EM_LINEINDEX (Winuser. h)
description: Возвращает индекс символа первого символа указанной строки в многострочном элементе управления "поле ввода".
ms.assetid: vs|controls|~\controls\editcontrols\editcontrolreference\editcontrolmessages\em_lineindex.htm
keywords:
- Элементы управления Windows для EM_LINEINDEX сообщений
topic_type:
- apiref
api_name:
- EM_LINEINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 611d4ff892f95287c45166ae55ff2389f454512c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988488"
---
# <a name="em_lineindex-message-winuserh"></a><span data-ttu-id="c8f28-104">Сообщение EM_LINEINDEX (Winuser. h)</span><span class="sxs-lookup"><span data-stu-id="c8f28-104">EM_LINEINDEX message (Winuser.h)</span></span>

<span data-ttu-id="c8f28-105">Возвращает индекс символа первого символа указанной строки в многострочном элементе управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="c8f28-105">Gets the character index of the first character of a specified line in a multiline edit control.</span></span> <span data-ttu-id="c8f28-106">Индекс символа — это Отсчитываемый от нуля индекс символа, начиная с начала элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="c8f28-106">A character index is the zero-based index of the character from the beginning of the edit control.</span></span> <span data-ttu-id="c8f28-107">Это сообщение можно отправить либо в элемент управления "поле ввода", либо в элемент управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="c8f28-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="c8f28-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c8f28-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8f28-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c8f28-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c8f28-110">Номер строки, начинающейся с нуля.</span><span class="sxs-lookup"><span data-stu-id="c8f28-110">The zero-based line number.</span></span> <span data-ttu-id="c8f28-111">Значение-1 указывает текущий номер строки (строка, содержащая курсор).</span><span class="sxs-lookup"><span data-stu-id="c8f28-111">A value of -1 specifies the current line number (the line that contains the caret).</span></span>

</dd> <dt>

<span data-ttu-id="c8f28-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c8f28-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c8f28-113">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="c8f28-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8f28-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c8f28-114">Return value</span></span>

<span data-ttu-id="c8f28-115">Возвращаемое значение — это индекс символа строки, указанной в параметре *wParam* , или-1, если номер строки больше числа строк в элементе управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="c8f28-115">The return value is the character index of the line specified in the *wParam* parameter, or it is -1 if the specified line number is greater than the number of lines in the edit control.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8f28-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c8f28-116">Remarks</span></span>

<span data-ttu-id="c8f28-117">**Расширенное редактирование:** Поддерживается в Microsoft Rich Edit 1,0 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="c8f28-117">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="c8f28-118">Дополнительные сведения о совместимости расширенных версий редактирования с различными версиями системы см. в разделе [Общие сведения об элементах управления редактированием](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="c8f28-118">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c8f28-119">Требования</span><span class="sxs-lookup"><span data-stu-id="c8f28-119">Requirements</span></span>



| <span data-ttu-id="c8f28-120">Требование</span><span class="sxs-lookup"><span data-stu-id="c8f28-120">Requirement</span></span> | <span data-ttu-id="c8f28-121">Значение</span><span class="sxs-lookup"><span data-stu-id="c8f28-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8f28-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c8f28-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c8f28-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c8f28-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c8f28-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c8f28-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c8f28-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c8f28-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c8f28-126">Header</span><span class="sxs-lookup"><span data-stu-id="c8f28-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8f28-127"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c8f28-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8f28-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c8f28-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8f28-129">**EM \_ линефромчар**</span><span class="sxs-lookup"><span data-stu-id="c8f28-129">**EM\_LINEFROMCHAR**</span></span>](em-linefromchar.md)
</dt> </dl>

 

 






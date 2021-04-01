---
title: Сообщение EM_LINESCROLL (Winuser. h)
description: Прокручивает текст в многострочном элементе управления Edit.
ms.assetid: 5398082d-f1ef-4a3a-9e5a-83cf286adbf1
keywords:
- Элементы управления Windows для EM_LINESCROLL сообщений
topic_type:
- apiref
api_name:
- EM_LINESCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 646e225ef269ccddca2cdc29caf635d94c1671e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071819"
---
# <a name="em_linescroll-message"></a><span data-ttu-id="7d54a-104">\_Сообщение ЛИНЕСКРОЛЛ EM</span><span class="sxs-lookup"><span data-stu-id="7d54a-104">EM\_LINESCROLL message</span></span>

<span data-ttu-id="7d54a-105">Прокручивает текст в многострочном элементе управления Edit.</span><span class="sxs-lookup"><span data-stu-id="7d54a-105">Scrolls the text in a multiline edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="7d54a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7d54a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d54a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7d54a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7d54a-108">**Изменить элементы управления:** Число символов для горизонтальной прокрутки.</span><span class="sxs-lookup"><span data-stu-id="7d54a-108">**Edit controls:** The number of characters to scroll horizontally.</span></span>

<span data-ttu-id="7d54a-109">**Элементы управления Rich Edit:** Этот параметр не используется; оно должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="7d54a-109">**Rich edit controls:** This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="7d54a-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7d54a-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7d54a-111">Число строк для вертикальной прокрутки.</span><span class="sxs-lookup"><span data-stu-id="7d54a-111">The number of lines to scroll vertically.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d54a-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7d54a-112">Return value</span></span>

<span data-ttu-id="7d54a-113">Если сообщение отправляется в многострочный элемент управления Edit, возвращается значение **true**.</span><span class="sxs-lookup"><span data-stu-id="7d54a-113">If the message is sent to a multiline edit control, the return value is **TRUE**.</span></span>

<span data-ttu-id="7d54a-114">Если сообщение отправляется в однострочный элемент управления Edit, возвращается значение **false**.</span><span class="sxs-lookup"><span data-stu-id="7d54a-114">If the message is sent to a single-line edit control, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d54a-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7d54a-115">Remarks</span></span>

<span data-ttu-id="7d54a-116">Элемент управления не выполняет вертикальную прокрутку за последней строкой текста в элементе управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="7d54a-116">The control does not scroll vertically past the last line of text in the edit control.</span></span> <span data-ttu-id="7d54a-117">Если текущая строка плюс число строк, заданное параметром *lParam* , превышает общее число строк в элементе управления "поле ввода", значение корректируется таким образом, что последняя строка элемента управления "поле ввода" прокручивается до верхней границы окна "Правка-элемент управления".</span><span class="sxs-lookup"><span data-stu-id="7d54a-117">If the current line plus the number of lines specified by the *lParam* parameter exceeds the total number of lines in the edit control, the value is adjusted so that the last line of the edit control is scrolled to the top of the edit-control window.</span></span>

<span data-ttu-id="7d54a-118">**Изменить элементы управления:** Сообщение **EM \_ линескролл** прокручивает текст по вертикали или горизонтали в многострочном элементе управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="7d54a-118">**Edit controls:** The **EM\_LINESCROLL** message scrolls the text vertically or horizontally in a multiline edit control.</span></span> <span data-ttu-id="7d54a-119">Сообщение **EM \_ линескролл** можно использовать для прокрутки по горизонтали за последним символом любой строки.</span><span class="sxs-lookup"><span data-stu-id="7d54a-119">The **EM\_LINESCROLL** message can be used to scroll horizontally past the last character of any line.</span></span>

<span data-ttu-id="7d54a-120">**Расширенное редактирование:** Поддерживается в Microsoft Rich Edit 1,0 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="7d54a-120">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="7d54a-121">Сообщение **EM \_ линескролл** прокручивает текст по вертикали в многострочном элементе управления Edit.</span><span class="sxs-lookup"><span data-stu-id="7d54a-121">The **EM\_LINESCROLL** message scrolls the text vertically in a multiline edit control.</span></span> <span data-ttu-id="7d54a-122">Дополнительные сведения о совместимости расширенных версий редактирования с различными версиями системы см. в разделе [Общие сведения об элементах управления редактированием](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="7d54a-122">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7d54a-123">Требования</span><span class="sxs-lookup"><span data-stu-id="7d54a-123">Requirements</span></span>



| <span data-ttu-id="7d54a-124">Требование</span><span class="sxs-lookup"><span data-stu-id="7d54a-124">Requirement</span></span> | <span data-ttu-id="7d54a-125">Значение</span><span class="sxs-lookup"><span data-stu-id="7d54a-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d54a-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7d54a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="7d54a-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7d54a-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7d54a-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7d54a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="7d54a-129">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7d54a-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7d54a-130">Header</span><span class="sxs-lookup"><span data-stu-id="7d54a-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d54a-131"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7d54a-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

 






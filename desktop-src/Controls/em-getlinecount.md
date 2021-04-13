---
title: Сообщение EM_GETLINECOUNT (Winuser. h)
description: Возвращает число строк в многострочном элементе управления "поле ввода". Это сообщение можно отправить либо в элемент управления "поле ввода", либо в элемент управления Rich Edit.
ms.assetid: 9fe63c10-7395-4f98-a672-14960a70d14f
keywords:
- Элементы управления Windows для EM_GETLINECOUNT сообщений
topic_type:
- apiref
api_name:
- EM_GETLINECOUNT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15ffbeafb13850317faccb4be44571d81b0d7e36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489462"
---
# <a name="em_getlinecount-message-winuserh"></a><span data-ttu-id="e0356-105">Сообщение EM_GETLINECOUNT (Winuser. h)</span><span class="sxs-lookup"><span data-stu-id="e0356-105">EM_GETLINECOUNT message (Winuser.h)</span></span>

<span data-ttu-id="e0356-106">Возвращает число строк в многострочном элементе управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="e0356-106">Gets the number of lines in a multiline edit control.</span></span> <span data-ttu-id="e0356-107">Это сообщение можно отправить либо в элемент управления "поле ввода", либо в элемент управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="e0356-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="e0356-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e0356-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0356-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e0356-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e0356-110">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="e0356-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="e0356-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e0356-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e0356-112">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="e0356-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0356-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e0356-113">Return value</span></span>

<span data-ttu-id="e0356-114">Возвращаемое значение — это целое число, указывающее общее количество текстовых строк в элементе управления "поле ввода" или форматированном элементе управления.</span><span class="sxs-lookup"><span data-stu-id="e0356-114">The return value is an integer specifying the total number of text lines in the multiline edit control or rich edit control.</span></span> <span data-ttu-id="e0356-115">Если элемент управления не содержит текста, возвращается значение 1.</span><span class="sxs-lookup"><span data-stu-id="e0356-115">If the control has no text, the return value is 1.</span></span> <span data-ttu-id="e0356-116">Возвращаемое значение никогда не будет меньше 1.</span><span class="sxs-lookup"><span data-stu-id="e0356-116">The return value will never be less than 1.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0356-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e0356-117">Remarks</span></span>

<span data-ttu-id="e0356-118">Сообщение **EM \_ жетлинекаунт** извлекает общее количество текстовых строк, а не только число видимых в данный момент строк.</span><span class="sxs-lookup"><span data-stu-id="e0356-118">The **EM\_GETLINECOUNT** message retrieves the total number of text lines, not just the number of lines that are currently visible.</span></span>

<span data-ttu-id="e0356-119">Если функция переноса слов включена, число строк может измениться при изменении размеров окна редактирования.</span><span class="sxs-lookup"><span data-stu-id="e0356-119">If the Wordwrap feature is enabled, the number of lines can change when the dimensions of the editing window change.</span></span>

<span data-ttu-id="e0356-120">**Расширенное редактирование:** Поддерживается в Microsoft Rich Edit 1,0 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="e0356-120">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="e0356-121">Дополнительные сведения о совместимости расширенных версий редактирования с различными версиями системы см. в разделе [Общие сведения об элементах управления редактированием](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="e0356-121">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e0356-122">Требования</span><span class="sxs-lookup"><span data-stu-id="e0356-122">Requirements</span></span>



| <span data-ttu-id="e0356-123">Требование</span><span class="sxs-lookup"><span data-stu-id="e0356-123">Requirement</span></span> | <span data-ttu-id="e0356-124">Значение</span><span class="sxs-lookup"><span data-stu-id="e0356-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0356-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e0356-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e0356-126">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e0356-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e0356-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e0356-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e0356-128">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e0356-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e0356-129">Header</span><span class="sxs-lookup"><span data-stu-id="e0356-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0356-130"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e0356-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0356-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e0356-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="e0356-132">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="e0356-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e0356-133">**EM, \_ строка**</span><span class="sxs-lookup"><span data-stu-id="e0356-133">**EM\_GETLINE**</span></span>](em-getline.md)
</dt> <dt>

[<span data-ttu-id="e0356-134">**EM \_ линеленгс**</span><span class="sxs-lookup"><span data-stu-id="e0356-134">**EM\_LINELENGTH**</span></span>](em-linelength.md)
</dt> <dt>

[<span data-ttu-id="e0356-135">**Изменить \_ жетлинекаунт**</span><span class="sxs-lookup"><span data-stu-id="e0356-135">**Edit\_GetLineCount**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_getlinecount)
</dt> </dl>

 

 






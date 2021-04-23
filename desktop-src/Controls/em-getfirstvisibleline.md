---
title: Сообщение EM_GETFIRSTVISIBLELINE (Winuser. h)
description: Возвращает отсчитываемый от нуля индекс самой верхней видимой строки в многострочном элементе управления "поле ввода". Это сообщение можно отправить либо в элемент управления "поле ввода", либо в элемент управления Rich Edit.
ms.assetid: 022838d2-7948-4c5a-92ca-655822c4f672
keywords:
- Элементы управления Windows для EM_GETFIRSTVISIBLELINE сообщений
topic_type:
- apiref
api_name:
- EM_GETFIRSTVISIBLELINE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bb759be166b69b3cfa488e9e23d61d9e0ec42d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534688"
---
# <a name="em_getfirstvisibleline-message"></a><span data-ttu-id="9c0d1-105">\_Сообщение ЖЕТФИРСТВИСИБЛЕЛИНЕ EM</span><span class="sxs-lookup"><span data-stu-id="9c0d1-105">EM\_GETFIRSTVISIBLELINE message</span></span>

<span data-ttu-id="9c0d1-106">Возвращает отсчитываемый от нуля индекс самой верхней видимой строки в многострочном элементе управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="9c0d1-106">Gets the zero-based index of the uppermost visible line in a multiline edit control.</span></span> <span data-ttu-id="9c0d1-107">Это сообщение можно отправить либо в элемент управления "поле ввода", либо в элемент управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="9c0d1-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="9c0d1-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9c0d1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c0d1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9c0d1-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9c0d1-110">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="9c0d1-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="9c0d1-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9c0d1-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9c0d1-112">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="9c0d1-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c0d1-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9c0d1-113">Return value</span></span>

<span data-ttu-id="9c0d1-114">Возвращаемое значение — это Отсчитываемый от нуля индекс самой верхней видимой строки в многострочном элементе управления Edit.</span><span class="sxs-lookup"><span data-stu-id="9c0d1-114">The return value is the zero-based index of the uppermost visible line in a multiline edit control.</span></span>

<span data-ttu-id="9c0d1-115">**Изменить элементы управления:** Для однострочных элементов управления редактирования возвращаемое значение представляет собой отсчитываемый от нуля индекс первого видимого символа.</span><span class="sxs-lookup"><span data-stu-id="9c0d1-115">**Edit controls:** For single-line edit controls, the return value is the zero-based index of the first visible character.</span></span>

<span data-ttu-id="9c0d1-116">**Элементы управления Rich Edit:** Для однострочных элементов управления Rich Edit возвращаемое значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="9c0d1-116">**Rich edit controls:** For single-line rich edit controls, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c0d1-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9c0d1-117">Remarks</span></span>

<span data-ttu-id="9c0d1-118">Число строк и длина строк в элементе управления "поле ввода" зависят от ширины элемента управления и текущего параметра переноса слов.</span><span class="sxs-lookup"><span data-stu-id="9c0d1-118">The number of lines and the length of the lines in an edit control depend on the width of the control and the current Wordwrap setting.</span></span>

<span data-ttu-id="9c0d1-119">**Расширенное редактирование:** Поддерживается в Microsoft Rich Edit 1,0 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="9c0d1-119">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="9c0d1-120">Дополнительные сведения о совместимости расширенных версий редактирования с различными версиями системы см. в разделе [Общие сведения об элементах управления редактированием](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="9c0d1-120">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9c0d1-121">Требования</span><span class="sxs-lookup"><span data-stu-id="9c0d1-121">Requirements</span></span>



| <span data-ttu-id="9c0d1-122">Требование</span><span class="sxs-lookup"><span data-stu-id="9c0d1-122">Requirement</span></span> | <span data-ttu-id="9c0d1-123">Значение</span><span class="sxs-lookup"><span data-stu-id="9c0d1-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c0d1-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9c0d1-124">Minimum supported client</span></span><br/> | <span data-ttu-id="9c0d1-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9c0d1-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9c0d1-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9c0d1-126">Minimum supported server</span></span><br/> | <span data-ttu-id="9c0d1-127">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9c0d1-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9c0d1-128">Header</span><span class="sxs-lookup"><span data-stu-id="9c0d1-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c0d1-129"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9c0d1-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

 






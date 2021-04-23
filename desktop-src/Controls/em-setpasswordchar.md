---
title: Сообщение EM_SETPASSWORDCHAR (Winuser. h)
description: Задает или удаляет символ пароля для элемента управления "поле ввода". Если задан символ пароля, этот символ отображается вместо символов, вводимых пользователем. Это сообщение можно отправить либо в элемент управления "поле ввода", либо в элемент управления Rich Edit.
ms.assetid: 9091892c-9f37-4e06-a084-9326c5f7f31e
keywords:
- Элементы управления Windows для EM_SETPASSWORDCHAR сообщений
topic_type:
- apiref
api_name:
- EM_SETPASSWORDCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dd2c75039a6d447809cc17e5c44d70c6e612ede
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490227"
---
# <a name="em_setpasswordchar-message"></a><span data-ttu-id="9999a-106">\_Сообщение СЕТПАССВОРДЧАР EM</span><span class="sxs-lookup"><span data-stu-id="9999a-106">EM\_SETPASSWORDCHAR message</span></span>

<span data-ttu-id="9999a-107">Задает или удаляет символ пароля для элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="9999a-107">Sets or removes the password character for an edit control.</span></span> <span data-ttu-id="9999a-108">Если задан символ пароля, этот символ отображается вместо символов, вводимых пользователем.</span><span class="sxs-lookup"><span data-stu-id="9999a-108">When a password character is set, that character is displayed in place of the characters typed by the user.</span></span> <span data-ttu-id="9999a-109">Это сообщение можно отправить либо в элемент управления "поле ввода", либо в элемент управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="9999a-109">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="9999a-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="9999a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9999a-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9999a-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9999a-112">Символ, отображаемый вместо символов, вводимых пользователем.</span><span class="sxs-lookup"><span data-stu-id="9999a-112">The character to be displayed in place of the characters typed by the user.</span></span> <span data-ttu-id="9999a-113">Если этот параметр равен нулю, элемент управления удаляет текущий символ пароля и отображает символы, введенные пользователем.</span><span class="sxs-lookup"><span data-stu-id="9999a-113">If this parameter is zero, the control removes the current password character and displays the characters typed by the user.</span></span>

</dd> <dt>

<span data-ttu-id="9999a-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9999a-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9999a-115">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="9999a-115">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9999a-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9999a-116">Return value</span></span>

<span data-ttu-id="9999a-117">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="9999a-117">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9999a-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9999a-118">Remarks</span></span>

<span data-ttu-id="9999a-119">Когда элемент управления "поле ввода" получает сообщение **EM \_ сетпассвордчар** , элемент управления перерисовывает все видимые символы, используя символ, заданный параметром *wParam* .</span><span class="sxs-lookup"><span data-stu-id="9999a-119">When an edit control receives the **EM\_SETPASSWORDCHAR** message, the control redraws all visible characters using the character specified by the *wParam* parameter.</span></span> <span data-ttu-id="9999a-120">Если параметр *wParam* равен нулю, элемент управления перерисовывает все видимые символы, используя символы, введенные пользователем.</span><span class="sxs-lookup"><span data-stu-id="9999a-120">If *wParam* is zero, the control redraws all visible characters using the characters typed by the user.</span></span>

<span data-ttu-id="9999a-121">Если элемент управления "поле ввода" создается с использованием [**\_ пароля ES**](edit-control-styles.md) , символу пароля по умолчанию присваивается звездочка ( \* ).</span><span class="sxs-lookup"><span data-stu-id="9999a-121">If an edit control is created with the [**ES\_PASSWORD**](edit-control-styles.md) style, the default password character is set to an asterisk (\*).</span></span> <span data-ttu-id="9999a-122">Если элемент управления "поле ввода" создается без стиля **\_ пароля ES** , то символ пароля отсутствует.</span><span class="sxs-lookup"><span data-stu-id="9999a-122">If an edit control is created without the **ES\_PASSWORD** style, there is no password character.</span></span> <span data-ttu-id="9999a-123">Стиль **\_ пароля ES** удаляется при отправке сообщения **EM \_ сетпассвордчар** с параметром *wParam* , равным нулю.</span><span class="sxs-lookup"><span data-stu-id="9999a-123">The **ES\_PASSWORD** style is removed if an **EM\_SETPASSWORDCHAR** message is sent with the *wParam* parameter set to zero.</span></span>

<span data-ttu-id="9999a-124">**Изменить элементы управления:** Элементы управления многострочного редактирования не поддерживают стиль или сообщения пароля.</span><span class="sxs-lookup"><span data-stu-id="9999a-124">**Edit controls:** Multiline edit controls do not support the password style or messages.</span></span>

<span data-ttu-id="9999a-125">**Расширенное редактирование:** Поддерживается в Microsoft Rich Edit 2,0 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="9999a-125">**Rich Edit:** Supported in Microsoft Rich Edit 2.0 and later.</span></span> <span data-ttu-id="9999a-126">Оба элемента управления для однострочного и многострочного редактирования поддерживают стиль и сообщения пароля.</span><span class="sxs-lookup"><span data-stu-id="9999a-126">Both single-line and multiline edit controls support the password style and messages.</span></span> <span data-ttu-id="9999a-127">Дополнительные сведения о совместимости расширенных версий редактирования с различными версиями системы см. в разделе [Общие сведения об элементах управления редактированием](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="9999a-127">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9999a-128">Требования</span><span class="sxs-lookup"><span data-stu-id="9999a-128">Requirements</span></span>



| <span data-ttu-id="9999a-129">Требование</span><span class="sxs-lookup"><span data-stu-id="9999a-129">Requirement</span></span> | <span data-ttu-id="9999a-130">Значение</span><span class="sxs-lookup"><span data-stu-id="9999a-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9999a-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9999a-131">Minimum supported client</span></span><br/> | <span data-ttu-id="9999a-132">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9999a-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9999a-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9999a-133">Minimum supported server</span></span><br/> | <span data-ttu-id="9999a-134">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9999a-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9999a-135">Header</span><span class="sxs-lookup"><span data-stu-id="9999a-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="9999a-136"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9999a-136"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9999a-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9999a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9999a-138">**EM \_ жетпассвордчар**</span><span class="sxs-lookup"><span data-stu-id="9999a-138">**EM\_GETPASSWORDCHAR**</span></span>](em-getpasswordchar.md)
</dt> </dl>

 

 






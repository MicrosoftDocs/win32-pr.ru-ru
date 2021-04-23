---
title: Сообщение EM_GETPASSWORDCHAR (Winuser. h)
description: Возвращает символ пароля, который отображается в элементе управления "поле ввода", когда пользователь вводит текст. Это сообщение можно отправить либо в элемент управления "поле ввода", либо в элемент управления Rich Edit.
ms.assetid: 874336f6-701b-466a-afa6-0cb3e787ba4c
keywords:
- Элементы управления Windows для EM_GETPASSWORDCHAR сообщений
topic_type:
- apiref
api_name:
- EM_GETPASSWORDCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6285f002554e22c89896711d3d1d355a95c6bb7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892486"
---
# <a name="em_getpasswordchar-message"></a><span data-ttu-id="32609-105">\_Сообщение ЖЕТПАССВОРДЧАР EM</span><span class="sxs-lookup"><span data-stu-id="32609-105">EM\_GETPASSWORDCHAR message</span></span>

<span data-ttu-id="32609-106">Возвращает символ пароля, который отображается в элементе управления "поле ввода", когда пользователь вводит текст.</span><span class="sxs-lookup"><span data-stu-id="32609-106">Gets the password character that an edit control displays when the user enters text.</span></span> <span data-ttu-id="32609-107">Это сообщение можно отправить либо в элемент управления "поле ввода", либо в элемент управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="32609-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="32609-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="32609-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32609-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="32609-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="32609-110">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="32609-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="32609-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="32609-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="32609-112">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="32609-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32609-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="32609-113">Return value</span></span>

<span data-ttu-id="32609-114">Возвращаемое значение указывает символ, отображаемый вместо любого символа, введенного пользователем.</span><span class="sxs-lookup"><span data-stu-id="32609-114">The return value specifies the character to be displayed in place of any characters typed by the user.</span></span> <span data-ttu-id="32609-115">Если возвращаемое значение равно **null**, то символ пароля отсутствует, а элемент управления отображает символы, введенные пользователем.</span><span class="sxs-lookup"><span data-stu-id="32609-115">If the return value is **NULL**, there is no password character, and the control displays the characters typed by the user.</span></span>

## <a name="remarks"></a><span data-ttu-id="32609-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="32609-116">Remarks</span></span>

<span data-ttu-id="32609-117">Если элемент управления "поле ввода" создается с использованием [**\_ пароля ES**](edit-control-styles.md) , символу пароля по умолчанию присваивается звездочка ( \* ).</span><span class="sxs-lookup"><span data-stu-id="32609-117">If an edit control is created with the [**ES\_PASSWORD**](edit-control-styles.md) style, the default password character is set to an asterisk (\*).</span></span> <span data-ttu-id="32609-118">Если элемент управления "поле ввода" создается без стиля **\_ пароля ES** , то символ пароля отсутствует.</span><span class="sxs-lookup"><span data-stu-id="32609-118">If an edit control is created without the **ES\_PASSWORD** style, there is no password character.</span></span> <span data-ttu-id="32609-119">Чтобы изменить символ пароля, отправьте сообщение [**\_ сетпассвордчар EM**](em-setpasswordchar.md) .</span><span class="sxs-lookup"><span data-stu-id="32609-119">To change the password character, send the [**EM\_SETPASSWORDCHAR**](em-setpasswordchar.md) message.</span></span>

<span data-ttu-id="32609-120">**Изменить элементы управления:** Элементы управления многострочного редактирования не поддерживают стиль или сообщения пароля.</span><span class="sxs-lookup"><span data-stu-id="32609-120">**Edit controls:** Multiline edit controls do not support the password style or messages.</span></span>

<span data-ttu-id="32609-121">**Расширенное редактирование:** Поддерживается в Microsoft Rich Edit 2,0 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="32609-121">**Rich edit:** Supported in Microsoft Rich Edit 2.0 and later.</span></span> <span data-ttu-id="32609-122">Оба элемента управления для однострочного и многострочного редактирования поддерживают стиль и сообщения пароля.</span><span class="sxs-lookup"><span data-stu-id="32609-122">Both single-line and multiline edit controls support the password style and messages.</span></span> <span data-ttu-id="32609-123">Дополнительные сведения о совместимости расширенных версий редактирования с различными версиями системы см. в разделе [Общие сведения об элементах управления редактированием](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="32609-123">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="32609-124">Требования</span><span class="sxs-lookup"><span data-stu-id="32609-124">Requirements</span></span>



| <span data-ttu-id="32609-125">Требование</span><span class="sxs-lookup"><span data-stu-id="32609-125">Requirement</span></span> | <span data-ttu-id="32609-126">Значение</span><span class="sxs-lookup"><span data-stu-id="32609-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32609-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="32609-127">Minimum supported client</span></span><br/> | <span data-ttu-id="32609-128">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="32609-128">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="32609-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="32609-129">Minimum supported server</span></span><br/> | <span data-ttu-id="32609-130">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="32609-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="32609-131">Header</span><span class="sxs-lookup"><span data-stu-id="32609-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="32609-132"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="32609-132"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32609-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="32609-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32609-134">**EM \_ сетпассвордчар**</span><span class="sxs-lookup"><span data-stu-id="32609-134">**EM\_SETPASSWORDCHAR**</span></span>](em-setpasswordchar.md)
</dt> </dl>

 

 






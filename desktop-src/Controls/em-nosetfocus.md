---
title: Сообщение EM_NOSETFOCUS (Коммктрл. h)
description: Предотвращает получение фокуса клавиатуры с помощью однострочного элемента управления Edit Control. Это сообщение можно отправить явным образом или с помощью \_ макроса Edit носетфокус.
ms.assetid: aeb5ed6b-7d4f-4c0d-a172-6cee7cab959c
keywords:
- Элементы управления Windows для EM_NOSETFOCUS сообщений
topic_type:
- apiref
api_name:
- EM_NOSETFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b82830cda3402d2089d3421debaa7c4dbf13de5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136847"
---
# <a name="em_nosetfocus-message"></a><span data-ttu-id="2d00e-105">\_Сообщение НОСЕТФОКУС EM</span><span class="sxs-lookup"><span data-stu-id="2d00e-105">EM\_NOSETFOCUS message</span></span>

<span data-ttu-id="2d00e-106">\[Предназначен для внутреннего использования; не рекомендуется для использования в приложениях.</span><span class="sxs-lookup"><span data-stu-id="2d00e-106">\[Intended for internal use; not recommended for use in applications.</span></span> <span data-ttu-id="2d00e-107">Это сообщение может не поддерживаться в будущих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2d00e-107">This message may not be supported in future versions of Windows.\]</span></span>

<span data-ttu-id="2d00e-108">Предотвращает получение фокуса клавиатуры с помощью однострочного элемента управления Edit Control.</span><span class="sxs-lookup"><span data-stu-id="2d00e-108">Prevents a single-line edit control from receiving keyboard focus.</span></span> <span data-ttu-id="2d00e-109">Это сообщение можно отправить явным образом или с помощью макроса [**Edit \_ носетфокус**](/windows/desktop/api/Commctrl/nf-commctrl-edit_nosetfocus) .</span><span class="sxs-lookup"><span data-stu-id="2d00e-109">You can send this message explicitly or by using the [**Edit\_NoSetFocus**](/windows/desktop/api/Commctrl/nf-commctrl-edit_nosetfocus) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2d00e-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="2d00e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d00e-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2d00e-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2d00e-112">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="2d00e-112">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="2d00e-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2d00e-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2d00e-114">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="2d00e-114">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d00e-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2d00e-115">Return value</span></span>

<span data-ttu-id="2d00e-116">Возвращаемое значение не используется.</span><span class="sxs-lookup"><span data-stu-id="2d00e-116">The return value is not used.</span></span>

## <a name="security-considerations"></a><span data-ttu-id="2d00e-117">Соображения безопасности</span><span class="sxs-lookup"><span data-stu-id="2d00e-117">Security Considerations</span></span>

<span data-ttu-id="2d00e-118">Использование этого сообщения может нарушить безопасность программы.</span><span class="sxs-lookup"><span data-stu-id="2d00e-118">Using this message might compromise the security of your program.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d00e-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2d00e-119">Remarks</span></span>

<span data-ttu-id="2d00e-120">Это сообщение пропускается, если элемент управления "поле ввода" не является элементом управления "поле ввода" с одной строкой.</span><span class="sxs-lookup"><span data-stu-id="2d00e-120">This message is ignored if the edit control is not a single-line edit control.</span></span>

<span data-ttu-id="2d00e-121">После отправки сообщения этот результат будет постоянным.</span><span class="sxs-lookup"><span data-stu-id="2d00e-121">After this message is sent, the effect is permanent.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d00e-122">Требования</span><span class="sxs-lookup"><span data-stu-id="2d00e-122">Requirements</span></span>



| <span data-ttu-id="2d00e-123">Требование</span><span class="sxs-lookup"><span data-stu-id="2d00e-123">Requirement</span></span> | <span data-ttu-id="2d00e-124">Значение</span><span class="sxs-lookup"><span data-stu-id="2d00e-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2d00e-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2d00e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2d00e-126">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2d00e-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2d00e-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2d00e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2d00e-128">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2d00e-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2d00e-129">Header</span><span class="sxs-lookup"><span data-stu-id="2d00e-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d00e-130"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d00e-130"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d00e-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2d00e-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="2d00e-132">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="2d00e-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2d00e-133">**Изменить \_ носетфокус**</span><span class="sxs-lookup"><span data-stu-id="2d00e-133">**Edit\_NoSetFocus**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_nosetfocus)
</dt> <dt>

[<span data-ttu-id="2d00e-134">**EM \_ такефокус**</span><span class="sxs-lookup"><span data-stu-id="2d00e-134">**EM\_TAKEFOCUS**</span></span>](em-takefocus.md)
</dt> </dl>

 

 






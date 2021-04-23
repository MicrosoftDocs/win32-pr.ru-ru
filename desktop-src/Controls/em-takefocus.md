---
title: Сообщение EM_TAKEFOCUS (Коммктрл. h)
description: Принудительное получение фокуса клавиатуры с помощью однострочного элемента управления Edit. Это сообщение можно отправить явным образом или с помощью \_ макроса Edit такефокус.
ms.assetid: 27470857-4219-4426-bc69-e1271afc6ffb
keywords:
- Элементы управления Windows для EM_TAKEFOCUS сообщений
topic_type:
- apiref
api_name:
- EM_TAKEFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e4abdf926cdd337760b5cf151c3f8ee08cb418b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490719"
---
# <a name="em_takefocus-message"></a><span data-ttu-id="dccc9-105">\_Сообщение ТАКЕФОКУС EM</span><span class="sxs-lookup"><span data-stu-id="dccc9-105">EM\_TAKEFOCUS message</span></span>

<span data-ttu-id="dccc9-106">\[Предназначен для внутреннего использования; не рекомендуется для использования в приложениях.</span><span class="sxs-lookup"><span data-stu-id="dccc9-106">\[Intended for internal use; not recommended for use in applications.</span></span> <span data-ttu-id="dccc9-107">Это сообщение может не поддерживаться в будущих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="dccc9-107">This message may not be supported in future versions of Windows.\]</span></span>

<span data-ttu-id="dccc9-108">Принудительное получение фокуса клавиатуры с помощью однострочного элемента управления Edit.</span><span class="sxs-lookup"><span data-stu-id="dccc9-108">Forces a single-line edit control to receive keyboard focus.</span></span> <span data-ttu-id="dccc9-109">Это сообщение можно отправить явным образом или с помощью макроса [**Edit \_ такефокус**](/windows/desktop/api/Commctrl/nf-commctrl-edit_takefocus) .</span><span class="sxs-lookup"><span data-stu-id="dccc9-109">You can send this message explicitly or by using the [**Edit\_TakeFocus**](/windows/desktop/api/Commctrl/nf-commctrl-edit_takefocus) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="dccc9-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="dccc9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dccc9-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dccc9-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dccc9-112">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="dccc9-112">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="dccc9-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dccc9-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dccc9-114">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="dccc9-114">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dccc9-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dccc9-115">Return value</span></span>

<span data-ttu-id="dccc9-116">Возвращаемое значение не используется.</span><span class="sxs-lookup"><span data-stu-id="dccc9-116">The return value is not used.</span></span>

## <a name="security-considerations"></a><span data-ttu-id="dccc9-117">Соображения безопасности</span><span class="sxs-lookup"><span data-stu-id="dccc9-117">Security Considerations</span></span>

<span data-ttu-id="dccc9-118">Использование этого сообщения может нарушить безопасность программы.</span><span class="sxs-lookup"><span data-stu-id="dccc9-118">Using this message might compromise the security of your program.</span></span>

## <a name="remarks"></a><span data-ttu-id="dccc9-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dccc9-119">Remarks</span></span>

<span data-ttu-id="dccc9-120">Это сообщение пропускается, если элемент управления "поле ввода" не является элементом управления "поле ввода" с одной строкой.</span><span class="sxs-lookup"><span data-stu-id="dccc9-120">This message is ignored if the edit control is not a single-line edit control.</span></span>

<span data-ttu-id="dccc9-121">Если в элементе управления "поле ввода" ранее было получено сообщение [**EM \_ носетфокус**](em-nosetfocus.md) , элемент управления "поле ввода" получит фокус, не имея его на самом деле; в противном случае элемент управления "поле ввода" получит фокус.</span><span class="sxs-lookup"><span data-stu-id="dccc9-121">If the edit control previously received an [**EM\_NOSETFOCUS**](em-nosetfocus.md) message, the edit control will appear to have the focus without actually having it; otherwise, the edit control will receive focus.</span></span>

## <a name="requirements"></a><span data-ttu-id="dccc9-122">Требования</span><span class="sxs-lookup"><span data-stu-id="dccc9-122">Requirements</span></span>



| <span data-ttu-id="dccc9-123">Требование</span><span class="sxs-lookup"><span data-stu-id="dccc9-123">Requirement</span></span> | <span data-ttu-id="dccc9-124">Значение</span><span class="sxs-lookup"><span data-stu-id="dccc9-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dccc9-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dccc9-125">Minimum supported client</span></span><br/> | <span data-ttu-id="dccc9-126">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dccc9-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dccc9-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dccc9-127">Minimum supported server</span></span><br/> | <span data-ttu-id="dccc9-128">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="dccc9-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dccc9-129">Header</span><span class="sxs-lookup"><span data-stu-id="dccc9-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="dccc9-130"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="dccc9-130"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dccc9-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dccc9-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="dccc9-132">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="dccc9-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="dccc9-133">**Изменить \_ такефокус**</span><span class="sxs-lookup"><span data-stu-id="dccc9-133">**Edit\_TakeFocus**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_takefocus)
</dt> <dt>

[<span data-ttu-id="dccc9-134">**EM \_ носетфокус**</span><span class="sxs-lookup"><span data-stu-id="dccc9-134">**EM\_NOSETFOCUS**</span></span>](em-nosetfocus.md)
</dt> </dl>

 

 






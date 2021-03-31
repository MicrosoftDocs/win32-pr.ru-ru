---
title: Сообщение LVM_EDITLABEL (Коммктрл. h)
description: Начинает редактирование указанного текста элемента списка представления. Сообщение неявно выбирает и фокусируется на указанном элементе. Это сообщение можно отправить явно или с помощью \_ макроса Едитлабел ListView.
ms.assetid: b63f13f1-6e66-4770-af84-30bcdb241727
keywords:
- Элементы управления Windows для LVM_EDITLABEL сообщений
topic_type:
- apiref
api_name:
- LVM_EDITLABEL
- LVM_EDITLABELA
- LVM_EDITLABELW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25cb4e119731c41130e1c19fdea2f74882796435
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801126"
---
# <a name="lvm_editlabel-message"></a><span data-ttu-id="934f5-106">\_Сообщение LVM едитлабел</span><span class="sxs-lookup"><span data-stu-id="934f5-106">LVM\_EDITLABEL message</span></span>

<span data-ttu-id="934f5-107">Начинает редактирование указанного текста элемента списка представления.</span><span class="sxs-lookup"><span data-stu-id="934f5-107">Begins in-place editing of the specified list-view item's text.</span></span> <span data-ttu-id="934f5-108">Сообщение неявно выбирает и фокусируется на указанном элементе.</span><span class="sxs-lookup"><span data-stu-id="934f5-108">The message implicitly selects and focuses the specified item.</span></span> <span data-ttu-id="934f5-109">Это сообщение можно отправить явно или с помощью макроса [**\_ едитлабел ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_editlabel) .</span><span class="sxs-lookup"><span data-stu-id="934f5-109">You can send this message explicitly or by using the [**ListView\_EditLabel**](/windows/desktop/api/Commctrl/nf-commctrl-listview_editlabel) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="934f5-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="934f5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="934f5-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="934f5-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="934f5-112">Индекс элемента представления списка.</span><span class="sxs-lookup"><span data-stu-id="934f5-112">The index of the list-view item.</span></span> <span data-ttu-id="934f5-113">Чтобы отменить редактирование, задайте для индекса значение-1.</span><span class="sxs-lookup"><span data-stu-id="934f5-113">To cancel editing, set the index to -1.</span></span>

</dd> <dt>

<span data-ttu-id="934f5-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="934f5-114">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="934f5-115">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="934f5-115">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="934f5-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="934f5-116">Return value</span></span>

<span data-ttu-id="934f5-117">Возвращает маркер для элемента управления "поле ввода", который используется для изменения текста элемента при его успешном выполнении, или **значение NULL** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="934f5-117">Returns the handle to the edit control that is used to edit the item text if successful, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="934f5-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="934f5-118">Remarks</span></span>

<span data-ttu-id="934f5-119">Когда пользователь завершает или отменяет редактирование, элемент управления "поле ввода" уничтожается и маркер становится недействительным.</span><span class="sxs-lookup"><span data-stu-id="934f5-119">When the user completes or cancels editing, the edit control is destroyed and the handle is no longer valid.</span></span> <span data-ttu-id="934f5-120">Можно создать подкласс элемента управления "поле ввода", но не следует его уничтожить.</span><span class="sxs-lookup"><span data-stu-id="934f5-120">You can subclass the edit control, but you should not destroy it.</span></span>

<span data-ttu-id="934f5-121">Элемент управления должен иметь фокус перед отправкой этого сообщения элементу управления.</span><span class="sxs-lookup"><span data-stu-id="934f5-121">The control must have the focus before you send this message to the control.</span></span> <span data-ttu-id="934f5-122">Фокус можно задать с помощью функции [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) .</span><span class="sxs-lookup"><span data-stu-id="934f5-122">Focus can be set using the [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) function.</span></span>

<span data-ttu-id="934f5-123">Если *wParam* имеет значение-1, отправляется код уведомления [ЛВН \_ ендлабеледит](lvn-endlabeledit.md) .</span><span class="sxs-lookup"><span data-stu-id="934f5-123">If *wParam* is -1, an [LVN\_ENDLABELEDIT](lvn-endlabeledit.md) notification code is sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="934f5-124">Требования</span><span class="sxs-lookup"><span data-stu-id="934f5-124">Requirements</span></span>



| <span data-ttu-id="934f5-125">Требование</span><span class="sxs-lookup"><span data-stu-id="934f5-125">Requirement</span></span> | <span data-ttu-id="934f5-126">Значение</span><span class="sxs-lookup"><span data-stu-id="934f5-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="934f5-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="934f5-127">Minimum supported client</span></span><br/> | <span data-ttu-id="934f5-128">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="934f5-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="934f5-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="934f5-129">Minimum supported server</span></span><br/> | <span data-ttu-id="934f5-130">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="934f5-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="934f5-131">Header</span><span class="sxs-lookup"><span data-stu-id="934f5-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="934f5-132"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="934f5-132"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="934f5-133">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="934f5-133">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="934f5-134">**LVM \_ ЕДИТЛАБЕЛВ** (Юникод) и **LVM \_ едитлабела** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="934f5-134">**LVM\_EDITLABELW** (Unicode) and **LVM\_EDITLABELA** (ANSI)</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="934f5-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="934f5-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="934f5-136">**WM \_ канцелмоде**</span><span class="sxs-lookup"><span data-stu-id="934f5-136">**WM\_CANCELMODE**</span></span>](/windows/desktop/winmsg/wm-cancelmode)
</dt> </dl>

 


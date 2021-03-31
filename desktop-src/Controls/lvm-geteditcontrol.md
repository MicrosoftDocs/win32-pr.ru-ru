---
title: Сообщение LVM_GETEDITCONTROL (Коммктрл. h)
description: Возвращает маркер элемента управления "поле ввода", используемый для изменения текста элемента представления списка. Это сообщение можно отправить явно или с помощью \_ макроса Жетедитконтрол ListView.
ms.assetid: 70450b24-9879-4be8-9bc9-f87008b66415
keywords:
- Элементы управления Windows для LVM_GETEDITCONTROL сообщений
topic_type:
- apiref
api_name:
- LVM_GETEDITCONTROL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79a8790f86fee17f72078f61899edcd79b331759
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071121"
---
# <a name="lvm_geteditcontrol-message"></a><span data-ttu-id="3a934-105">\_Сообщение LVM жетедитконтрол</span><span class="sxs-lookup"><span data-stu-id="3a934-105">LVM\_GETEDITCONTROL message</span></span>

<span data-ttu-id="3a934-106">Возвращает маркер элемента управления "поле ввода", используемый для изменения текста элемента представления списка.</span><span class="sxs-lookup"><span data-stu-id="3a934-106">Gets the handle to the edit control being used to edit a list-view item's text.</span></span> <span data-ttu-id="3a934-107">Это сообщение можно отправить явно или с помощью макроса [**\_ жетедитконтрол ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_geteditcontrol) .</span><span class="sxs-lookup"><span data-stu-id="3a934-107">You can send this message explicitly or by using the [**ListView\_GetEditControl**](/windows/desktop/api/Commctrl/nf-commctrl-listview_geteditcontrol) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="3a934-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3a934-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a934-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3a934-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="3a934-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="3a934-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="3a934-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3a934-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="3a934-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="3a934-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a934-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3a934-113">Return value</span></span>

<span data-ttu-id="3a934-114">Возвращает маркер в элемент управления "поле ввода", если он успешно, или **значение NULL** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="3a934-114">Returns the handle to the edit control if successful, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a934-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3a934-115">Remarks</span></span>

<span data-ttu-id="3a934-116">При начале редактирования метки создается, размещается и инициализируется элемент управления Edit.</span><span class="sxs-lookup"><span data-stu-id="3a934-116">When label editing begins, an edit control is created, positioned, and initialized.</span></span> <span data-ttu-id="3a934-117">Перед отображением элемент управления "представление списка" отправляет родительскому окну код уведомления [ЛВН \_ бегинлабеледит](lvn-beginlabeledit.md) .</span><span class="sxs-lookup"><span data-stu-id="3a934-117">Before it is displayed, the list-view control sends its parent window an [LVN\_BEGINLABELEDIT](lvn-beginlabeledit.md) notification code.</span></span>

<span data-ttu-id="3a934-118">Чтобы настроить редактирование меток, реализуйте обработчик для [ЛВН \_ бегинлабеледит](lvn-beginlabeledit.md) и отправьте сообщение **LVM \_ жетедитконтрол** в элемент управления List-View.</span><span class="sxs-lookup"><span data-stu-id="3a934-118">To customize label editing, implement a handler for [LVN\_BEGINLABELEDIT](lvn-beginlabeledit.md) and have it send an **LVM\_GETEDITCONTROL** message to the list-view control.</span></span> <span data-ttu-id="3a934-119">Если метка редактируется, возвращаемое значение будет обработано элементом управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="3a934-119">If a label is being edited, the return value will be a handle to the edit control.</span></span> <span data-ttu-id="3a934-120">Используйте этот маркер для настройки элемента управления "поле ввода", отправляя обычные сообщения **EM \_ xxx** .</span><span class="sxs-lookup"><span data-stu-id="3a934-120">Use this handle to customize the edit control by sending the usual **EM\_XXX** messages.</span></span>

<span data-ttu-id="3a934-121">Когда пользователь завершает или отменяет редактирование, элемент управления "поле ввода" уничтожается и маркер становится недействительным.</span><span class="sxs-lookup"><span data-stu-id="3a934-121">When the user completes or cancels editing, the edit control is destroyed and the handle is no longer valid.</span></span> <span data-ttu-id="3a934-122">Можно создать подкласс элемента управления "поле ввода", но не следует его уничтожить.</span><span class="sxs-lookup"><span data-stu-id="3a934-122">You can subclass the edit control, but you should not destroy it.</span></span> <span data-ttu-id="3a934-123">Чтобы отменить изменение, отправьте элемент управления List-View в сообщение [**WM \_ канцелмоде**](/windows/desktop/winmsg/wm-cancelmode) .</span><span class="sxs-lookup"><span data-stu-id="3a934-123">To cancel editing, send the list-view control a [**WM\_CANCELMODE**](/windows/desktop/winmsg/wm-cancelmode) message.</span></span>

<span data-ttu-id="3a934-124">Редактируемый элемент списка — это текущий элемент, элемент которого находится в состоянии "в режиме".</span><span class="sxs-lookup"><span data-stu-id="3a934-124">The list-view item being edited is the currently focused item that is, the item in the focused state.</span></span> <span data-ttu-id="3a934-125">Чтобы найти элемент на основе его состояния, используйте сообщение [**LVM \_ жетнекститем**](lvm-getnextitem.md) .</span><span class="sxs-lookup"><span data-stu-id="3a934-125">To find an item based on its state, use the [**LVM\_GETNEXTITEM**](lvm-getnextitem.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a934-126">Требования</span><span class="sxs-lookup"><span data-stu-id="3a934-126">Requirements</span></span>



| <span data-ttu-id="3a934-127">Требование</span><span class="sxs-lookup"><span data-stu-id="3a934-127">Requirement</span></span> | <span data-ttu-id="3a934-128">Значение</span><span class="sxs-lookup"><span data-stu-id="3a934-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3a934-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3a934-129">Minimum supported client</span></span><br/> | <span data-ttu-id="3a934-130">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3a934-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3a934-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3a934-131">Minimum supported server</span></span><br/> | <span data-ttu-id="3a934-132">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3a934-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3a934-133">Header</span><span class="sxs-lookup"><span data-stu-id="3a934-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a934-134"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a934-134"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a934-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3a934-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a934-136">**\_Жетедитконтрол ListView**</span><span class="sxs-lookup"><span data-stu-id="3a934-136">**ListView\_GetEditControl**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-listview_geteditcontrol)
</dt> </dl>

 


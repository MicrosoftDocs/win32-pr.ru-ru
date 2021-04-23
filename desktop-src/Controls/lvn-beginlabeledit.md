---
title: Код уведомления LVN_BEGINLABELEDIT (Коммктрл. h)
description: Сообщает родительскому окну элемента управления "представление списка" о начале редактирования метки для элемента. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: c13a9e95-22a9-476e-aeee-4928b8b096b0
keywords:
- LVN_BEGINLABELEDIT кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- LVN_BEGINLABELEDIT
- LVN_BEGINLABELEDITA
- LVN_BEGINLABELEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f77550b474534cee096b610a0805bce547d9b429
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988237"
---
# <a name="lvn_beginlabeledit-notification-code"></a><span data-ttu-id="ba9ec-105">\_Код уведомления ЛВН бегинлабеледит</span><span class="sxs-lookup"><span data-stu-id="ba9ec-105">LVN\_BEGINLABELEDIT notification code</span></span>

<span data-ttu-id="ba9ec-106">Сообщает родительскому окну элемента управления "представление списка" о начале редактирования метки для элемента.</span><span class="sxs-lookup"><span data-stu-id="ba9ec-106">Notifies a list-view control's parent window about the start of label editing for an item.</span></span> <span data-ttu-id="ba9ec-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="ba9ec-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_BEGINLABELEDIT

    pdi = (LPNMLVDISPINFO) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="ba9ec-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ba9ec-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba9ec-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ba9ec-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ba9ec-110">Указатель на структуру [**нмлвдиспинфо**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) .</span><span class="sxs-lookup"><span data-stu-id="ba9ec-110">Pointer to an [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) structure.</span></span> <span data-ttu-id="ba9ec-111">**Элемент** этой структуры является структурой [**Лвитем**](/windows/win32/api/commctrl/ns-commctrl-lvitema) , член **Член iItem** которой определяет редактируемый элемент.</span><span class="sxs-lookup"><span data-stu-id="ba9ec-111">The **item** member of this structure is an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure whose **iItem** member identifies the item being edited.</span></span> <span data-ttu-id="ba9ec-112">Обратите внимание, что подэлементы нельзя изменять. элемент **iSubItem** всегда имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="ba9ec-112">Note that subitems cannot be edited; the **iSubItem** member is always set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba9ec-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ba9ec-113">Return value</span></span>

<span data-ttu-id="ba9ec-114">Чтобы разрешить пользователю изменять метку, возвратите **значение false**.</span><span class="sxs-lookup"><span data-stu-id="ba9ec-114">To allow the user to edit the label, return **FALSE**.</span></span>

<span data-ttu-id="ba9ec-115">Чтобы запретить пользователю изменять метку, возвратите **значение true**.</span><span class="sxs-lookup"><span data-stu-id="ba9ec-115">To prevent the user from editing the label, return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba9ec-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ba9ec-116">Remarks</span></span>

<span data-ttu-id="ba9ec-117">При начале редактирования метки создается, размещается и инициализируется элемент управления Edit.</span><span class="sxs-lookup"><span data-stu-id="ba9ec-117">When label editing begins, an edit control is created, positioned, and initialized.</span></span> <span data-ttu-id="ba9ec-118">Перед отображением элемент управления "представление списка" отправляет родительскому окну \_ код уведомления ЛВН бегинлабеледит.</span><span class="sxs-lookup"><span data-stu-id="ba9ec-118">Before it is displayed, the list-view control sends its parent window an LVN\_BEGINLABELEDIT notification code.</span></span>

<span data-ttu-id="ba9ec-119">Чтобы настроить редактирование меток, реализуйте обработчик для ЛВН \_ бегинлабеледит и отправьте сообщение [**LVM \_ жетедитконтрол**](lvm-geteditcontrol.md) в элемент управления List-View.</span><span class="sxs-lookup"><span data-stu-id="ba9ec-119">To customize label editing, implement a handler for LVN\_BEGINLABELEDIT and have it send an [**LVM\_GETEDITCONTROL**](lvm-geteditcontrol.md) message to the list-view control.</span></span> <span data-ttu-id="ba9ec-120">Если метка редактируется, возвращаемое значение будет обработано элементом управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="ba9ec-120">If a label is being edited, the return value will be a handle to the edit control.</span></span> <span data-ttu-id="ba9ec-121">Используйте этот маркер для настройки элемента управления "поле ввода", отправляя обычные сообщения **EM \_ xxx** .</span><span class="sxs-lookup"><span data-stu-id="ba9ec-121">Use this handle to customize the edit control by sending the usual **EM\_XXX** messages.</span></span>

<span data-ttu-id="ba9ec-122">Когда пользователь отменяет или завершает редактирование, родительское окно получает код уведомления [ЛВН \_ ендлабеледит](lvn-endlabeledit.md) .</span><span class="sxs-lookup"><span data-stu-id="ba9ec-122">When the user cancels or completes the editing, the parent window receives an [LVN\_ENDLABELEDIT](lvn-endlabeledit.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba9ec-123">Требования</span><span class="sxs-lookup"><span data-stu-id="ba9ec-123">Requirements</span></span>



| <span data-ttu-id="ba9ec-124">Требование</span><span class="sxs-lookup"><span data-stu-id="ba9ec-124">Requirement</span></span> | <span data-ttu-id="ba9ec-125">Значение</span><span class="sxs-lookup"><span data-stu-id="ba9ec-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ba9ec-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ba9ec-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ba9ec-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ba9ec-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ba9ec-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ba9ec-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ba9ec-129">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ba9ec-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ba9ec-130">Header</span><span class="sxs-lookup"><span data-stu-id="ba9ec-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba9ec-131"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba9ec-131"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="ba9ec-132">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="ba9ec-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ba9ec-133">**ЛВН \_ БЕГИНЛАБЕЛЕДИТВ** (Юникод) и **ЛВН \_ бегинлабеледита** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ba9ec-133">**LVN\_BEGINLABELEDITW** (Unicode) and **LVN\_BEGINLABELEDITA** (ANSI)</span></span><br/>     |



 

 






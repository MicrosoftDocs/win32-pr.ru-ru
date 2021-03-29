---
title: Код уведомления TVN_BEGINLABELEDIT (Коммктрл. h)
description: Сообщает родительскому окну элемента управления иерархического представления о начале редактирования метки для элемента. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 67ed1f1f-7ccc-4e84-9540-4a46f6cd3a44
keywords:
- TVN_BEGINLABELEDIT кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TVN_BEGINLABELEDIT
- TVN_BEGINLABELEDITA
- TVN_BEGINLABELEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34eccdeda553d0792a2862e3ca81a0889539d5ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654523"
---
# <a name="tvn_beginlabeledit-notification-code"></a><span data-ttu-id="d2ab2-105">\_Код уведомления ТВН бегинлабеледит</span><span class="sxs-lookup"><span data-stu-id="d2ab2-105">TVN\_BEGINLABELEDIT notification code</span></span>

<span data-ttu-id="d2ab2-106">Сообщает родительскому окну элемента управления иерархического представления о начале редактирования метки для элемента.</span><span class="sxs-lookup"><span data-stu-id="d2ab2-106">Notifies a tree-view control's parent window about the start of label editing for an item.</span></span> <span data-ttu-id="d2ab2-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="d2ab2-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_BEGINLABELEDIT 

    ptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a><span data-ttu-id="d2ab2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d2ab2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2ab2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d2ab2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d2ab2-110">Указатель на структуру [**нмтвдиспинфо**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) .</span><span class="sxs-lookup"><span data-stu-id="d2ab2-110">Pointer to an [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) structure.</span></span> <span data-ttu-id="d2ab2-111">Элемент **Item** является структурой [**твитем**](/windows/win32/api/commctrl/ns-commctrl-tvitema) , содержащей допустимые сведения об изменяемом элементе в членах **хитем**, **State**, **lParam** и **псзтекст** .</span><span class="sxs-lookup"><span data-stu-id="d2ab2-111">The **item** member is a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure that contains valid information about the item being edited in the **hItem**, **state**, **lParam**, and **pszText** members.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2ab2-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d2ab2-112">Return value</span></span>

<span data-ttu-id="d2ab2-113">Возвращает **значение true** , чтобы отменить изменение метки.</span><span class="sxs-lookup"><span data-stu-id="d2ab2-113">Returns **TRUE** to cancel label editing.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2ab2-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d2ab2-114">Remarks</span></span>

<span data-ttu-id="d2ab2-115">Когда начинается редактирование метки, элемент управления "Правка" создается, но не размещается или не отображается.</span><span class="sxs-lookup"><span data-stu-id="d2ab2-115">When label editing begins, an edit control is created but not positioned or displayed.</span></span> <span data-ttu-id="d2ab2-116">Перед отображением элемент управления "дерево" отправляет родительскому окну \_ код уведомления ТВН бегинлабеледит.</span><span class="sxs-lookup"><span data-stu-id="d2ab2-116">Before it is displayed, the tree-view control sends its parent window a TVN\_BEGINLABELEDIT notification code.</span></span>

<span data-ttu-id="d2ab2-117">Чтобы настроить редактирование меток, реализуйте обработчик для ТВН \_ бегинлабеледит и отправьте сообщение [**TVM \_ жетедитконтрол**](tvm-geteditcontrol.md) в элемент управления "дерево-представление".</span><span class="sxs-lookup"><span data-stu-id="d2ab2-117">To customize label editing, implement a handler for TVN\_BEGINLABELEDIT and have it send a [**TVM\_GETEDITCONTROL**](tvm-geteditcontrol.md) message to the tree-view control.</span></span> <span data-ttu-id="d2ab2-118">Если метка редактируется, возвращаемое значение будет обработано элементом управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="d2ab2-118">If a label is being edited, the return value will be a handle to the edit control.</span></span> <span data-ttu-id="d2ab2-119">Используйте этот маркер для настройки элемента управления "поле ввода", отправляя обычные \_ сообщения EM XXX.</span><span class="sxs-lookup"><span data-stu-id="d2ab2-119">Use this handle to customize the edit control by sending the usual EM\_XXX messages.</span></span>

<span data-ttu-id="d2ab2-120">Когда пользователь отменяет или завершает редактирование, родительское окно получает код уведомления [ТВН \_ ендлабеледит](tvn-endlabeledit.md) .</span><span class="sxs-lookup"><span data-stu-id="d2ab2-120">When the user cancels or completes the editing, the parent window receives a [TVN\_ENDLABELEDIT](tvn-endlabeledit.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2ab2-121">Требования</span><span class="sxs-lookup"><span data-stu-id="d2ab2-121">Requirements</span></span>



| <span data-ttu-id="d2ab2-122">Требование</span><span class="sxs-lookup"><span data-stu-id="d2ab2-122">Requirement</span></span> | <span data-ttu-id="d2ab2-123">Значение</span><span class="sxs-lookup"><span data-stu-id="d2ab2-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d2ab2-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d2ab2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d2ab2-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d2ab2-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d2ab2-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d2ab2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d2ab2-127">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d2ab2-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d2ab2-128">Header</span><span class="sxs-lookup"><span data-stu-id="d2ab2-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2ab2-129"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2ab2-129"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="d2ab2-130">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="d2ab2-130">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d2ab2-131">**ТВН \_ БЕГИНЛАБЕЛЕДИТВ** (Юникод) и **ТВН \_ бегинлабеледита** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="d2ab2-131">**TVN\_BEGINLABELEDITW** (Unicode) and **TVN\_BEGINLABELEDITA** (ANSI)</span></span><br/>     |



 

 






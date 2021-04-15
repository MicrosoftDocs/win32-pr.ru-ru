---
title: Код уведомления LVN_ENDLABELEDIT (Коммктрл. h)
description: Сообщает родительскому окну элемента управления "представление списка" об окончании редактирования метки для элемента. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 03129fef-abf1-4374-b4b8-503c46ef7115
keywords:
- LVN_ENDLABELEDIT кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- LVN_ENDLABELEDIT
- LVN_ENDLABELEDITA
- LVN_ENDLABELEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a33ab69a04202aeb3817d3eeadf01fb6f1fcaac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654736"
---
# <a name="lvn_endlabeledit-notification-code"></a><span data-ttu-id="8e847-105">\_Код уведомления ЛВН ендлабеледит</span><span class="sxs-lookup"><span data-stu-id="8e847-105">LVN\_ENDLABELEDIT notification code</span></span>

<span data-ttu-id="8e847-106">Сообщает родительскому окну элемента управления "представление списка" об окончании редактирования метки для элемента.</span><span class="sxs-lookup"><span data-stu-id="8e847-106">Notifies a list-view control's parent window about the end of label editing for an item.</span></span> <span data-ttu-id="8e847-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="8e847-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_ENDLABELEDIT

    pdi = (LPNMLVDISPINFO) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="8e847-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8e847-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e847-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8e847-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8e847-110">Указатель на структуру [**нмлвдиспинфо**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) .</span><span class="sxs-lookup"><span data-stu-id="8e847-110">Pointer to an [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) structure.</span></span> <span data-ttu-id="8e847-111">**Элемент** этой структуры является структурой [**Лвитем**](/windows/win32/api/commctrl/ns-commctrl-lvitema) , член **Член iItem** которой определяет редактируемый элемент.</span><span class="sxs-lookup"><span data-stu-id="8e847-111">The **item** member of this structure is an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure whose **iItem** member identifies the item being edited.</span></span> <span data-ttu-id="8e847-112">Элемент **псзтекст** **элемента Item** содержит допустимое значение при \_ отправке кода уведомления ендлабеледит ЛВН, независимо от того, установлен ли флаг лвиф \_ Text в элементе **Mask** структуры **лвитем** .</span><span class="sxs-lookup"><span data-stu-id="8e847-112">The **pszText** member of **item** contains a valid value when the LVN\_ENDLABELEDIT notification code is sent, regardless of whether the LVIF\_TEXT flag is set in the **mask** member of the **LVITEM** structure.</span></span> <span data-ttu-id="8e847-113">Если пользователь отменяет правку, элемент **псзтекст** структуры **Лвитем** имеет **значение NULL**. в противном случае **псзтекст** является адресом редактируемого текста.</span><span class="sxs-lookup"><span data-stu-id="8e847-113">If the user cancels editing, the **pszText** member of the **LVITEM** structure is **NULL**; otherwise, **pszText** is the address of the edited text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e847-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8e847-114">Return value</span></span>

<span data-ttu-id="8e847-115">Если элемент **псзтекст** структуры [**лвитем**](/windows/win32/api/commctrl/ns-commctrl-lvitema) имеет значение, отличное от **null**, возвращает **значение true** , чтобы задать метку элемента для редактируемого текста.</span><span class="sxs-lookup"><span data-stu-id="8e847-115">If the **pszText** member of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure is non-**NULL**, return **TRUE** to set the item's label to the edited text.</span></span> <span data-ttu-id="8e847-116">Возвращает **значение false** , чтобы отклонить измененный текст и вернуться к исходной метке.</span><span class="sxs-lookup"><span data-stu-id="8e847-116">Return **FALSE** to reject the edited text and revert to the original label.</span></span>

<span data-ttu-id="8e847-117">Если элемент **псзтекст** структуры [**Лвитем**](/windows/win32/api/commctrl/ns-commctrl-lvitema) имеет **значение NULL**, возвращаемое значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="8e847-117">If the **pszText** member of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure is **NULL**, the return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e847-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8e847-118">Remarks</span></span>

<span data-ttu-id="8e847-119">Возвращаемое значение процедуры диалогового окна определяет, было ли сообщение обработано.</span><span class="sxs-lookup"><span data-stu-id="8e847-119">The return value of the dialog procedure is whether the message was handled.</span></span> <span data-ttu-id="8e847-120">Второе возвращаемое значение должно быть задано путем вызова [**сетвиндовлонгптр**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) с **DWLP_MSGRESULT**.</span><span class="sxs-lookup"><span data-stu-id="8e847-120">The second return value must be set by calling [**SetwindowLongPtr**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) with **DWLP_MSGRESULT**.</span></span>

<span data-ttu-id="8e847-121">Когда пользователь начинает изменять метку элемента, родительское окно элемента управления "представление списка" получает код уведомления [ЛВН \_ бегинлабеледит](lvn-beginlabeledit.md) .</span><span class="sxs-lookup"><span data-stu-id="8e847-121">When the user begins editing an item label, the parent window of the list-view control receives an [LVN\_BEGINLABELEDIT](lvn-beginlabeledit.md) notification code.</span></span> <span data-ttu-id="8e847-122">Когда пользователь отменяет или завершает редактирование, родительское окно получает \_ код уведомления ЛВН ендлабеледит.</span><span class="sxs-lookup"><span data-stu-id="8e847-122">When the user cancels or completes the editing, the parent window receives an LVN\_ENDLABELEDIT notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e847-123">Требования</span><span class="sxs-lookup"><span data-stu-id="8e847-123">Requirements</span></span>



| <span data-ttu-id="8e847-124">Требование</span><span class="sxs-lookup"><span data-stu-id="8e847-124">Requirement</span></span> | <span data-ttu-id="8e847-125">Значение</span><span class="sxs-lookup"><span data-stu-id="8e847-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8e847-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8e847-126">Minimum supported client</span></span><br/> | <span data-ttu-id="8e847-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8e847-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8e847-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8e847-128">Minimum supported server</span></span><br/> | <span data-ttu-id="8e847-129">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8e847-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8e847-130">Header</span><span class="sxs-lookup"><span data-stu-id="8e847-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e847-131"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e847-131"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="8e847-132">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="8e847-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="8e847-133">**ЛВН \_ ЕНДЛАБЕЛЕДИТВ** (Юникод) и **ЛВН \_ ендлабеледита** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="8e847-133">**LVN\_ENDLABELEDITW** (Unicode) and **LVN\_ENDLABELEDITA** (ANSI)</span></span><br/>         |



 

 






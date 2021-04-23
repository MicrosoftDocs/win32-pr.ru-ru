---
title: Код уведомления CBN_CLOSEUP (Winuser. h)
description: Посылается, когда список поля со списком был закрыт. Родительское окно поля со списком получает этот код уведомления через \_ командное сообщение WM.
ms.assetid: 79b2108e-1ef3-433d-a0b0-ac9ad1a93905
keywords:
- CBN_CLOSEUP кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- CBN_CLOSEUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec67cf68109d32d6e1ad714f91a97987f9a3734d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137742"
---
# <a name="cbn_closeup-notification-code"></a><span data-ttu-id="39a09-105">\_Код уведомления КБН крупный план</span><span class="sxs-lookup"><span data-stu-id="39a09-105">CBN\_CLOSEUP notification code</span></span>

<span data-ttu-id="39a09-106">Посылается, когда список поля со списком был закрыт.</span><span class="sxs-lookup"><span data-stu-id="39a09-106">Sent when the list box of a combo box has been closed.</span></span> <span data-ttu-id="39a09-107">Родительское окно поля со списком получает этот код уведомления через [**\_ командное сообщение WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="39a09-107">The parent window of the combo box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_CLOSEUP

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="39a09-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="39a09-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39a09-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="39a09-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="39a09-110">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) содержит идентификатор элемента управления поля со списком.</span><span class="sxs-lookup"><span data-stu-id="39a09-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="39a09-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает код уведомления.</span><span class="sxs-lookup"><span data-stu-id="39a09-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="39a09-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="39a09-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="39a09-113">Обработайте с полем со списком.</span><span class="sxs-lookup"><span data-stu-id="39a09-113">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="39a09-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="39a09-114">Remarks</span></span>

<span data-ttu-id="39a09-115">Если пользователь изменил текущее выделение, поле со списком также отправляет код уведомления [КБН \_ селчанже](cbn-selchange.md) при закрытии раскрывающегося списка.</span><span class="sxs-lookup"><span data-stu-id="39a09-115">If the user changed the current selection, the combo box also sends the [CBN\_SELCHANGE](cbn-selchange.md) notification code when the drop-down list closes.</span></span> <span data-ttu-id="39a09-116">В общем случае нельзя предсказать порядок, в котором будут отправляться коды уведомлений.</span><span class="sxs-lookup"><span data-stu-id="39a09-116">In general, you cannot predict the order in which notification codes will be sent.</span></span> <span data-ttu-id="39a09-117">В частности, \_ код уведомления КБН селчанже может находиться либо до, либо после \_ кода уведомления КБН крупный план.</span><span class="sxs-lookup"><span data-stu-id="39a09-117">In particular, a CBN\_SELCHANGE notification code may occur either before or after a CBN\_CLOSEUP notification code.</span></span>

<span data-ttu-id="39a09-118">Для выполнения определенного процесса каждый раз, когда пользователь выбирает элемент списка, можно обработать код уведомления [КБН \_ СЕЛЧАНЖЕ](cbn-selchange.md) или КБН \_ крупный план.</span><span class="sxs-lookup"><span data-stu-id="39a09-118">To execute a specific process each time the user selects a list item, you can handle either the [CBN\_SELCHANGE](cbn-selchange.md) or CBN\_CLOSEUP notification code.</span></span> <span data-ttu-id="39a09-119">Как правило, вы ждете \_ код уведомления КБН крупный план перед обработкой изменения в текущем выделенном фрагменте.</span><span class="sxs-lookup"><span data-stu-id="39a09-119">Typically, you would wait for the CBN\_CLOSEUP notification code before processing a change in the current selection.</span></span> <span data-ttu-id="39a09-120">Это может быть особенно важно, если требуется значительный объем обработки.</span><span class="sxs-lookup"><span data-stu-id="39a09-120">This can be particularly important if a significant amount of processing is required.</span></span>

<span data-ttu-id="39a09-121">Этот код уведомления не отправляется в поле со списком, имеющее [**\_ простой стиль CBS**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="39a09-121">This notification code is not sent to a combo box that has the [**CBS\_SIMPLE**](combo-box-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="39a09-122">Требования</span><span class="sxs-lookup"><span data-stu-id="39a09-122">Requirements</span></span>



| <span data-ttu-id="39a09-123">Требование</span><span class="sxs-lookup"><span data-stu-id="39a09-123">Requirement</span></span> | <span data-ttu-id="39a09-124">Значение</span><span class="sxs-lookup"><span data-stu-id="39a09-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39a09-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="39a09-125">Minimum supported client</span></span><br/> | <span data-ttu-id="39a09-126">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="39a09-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="39a09-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="39a09-127">Minimum supported server</span></span><br/> | <span data-ttu-id="39a09-128">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="39a09-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="39a09-129">Header</span><span class="sxs-lookup"><span data-stu-id="39a09-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="39a09-130"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="39a09-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39a09-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="39a09-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="39a09-132">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="39a09-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="39a09-133">\_раскрывающийся список КБН</span><span class="sxs-lookup"><span data-stu-id="39a09-133">CBN\_DROPDOWN</span></span>](cbn-dropdown.md)
</dt> <dt>

[<span data-ttu-id="39a09-134">КБН \_ селчанже</span><span class="sxs-lookup"><span data-stu-id="39a09-134">CBN\_SELCHANGE</span></span>](cbn-selchange.md)
</dt> <dt>

<span data-ttu-id="39a09-135">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="39a09-135">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="39a09-136">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="39a09-136">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="39a09-137">[**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="39a09-137">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="39a09-138">**\_команда WM**</span><span class="sxs-lookup"><span data-stu-id="39a09-138">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 


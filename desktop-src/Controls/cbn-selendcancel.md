---
title: Код уведомления CBN_SELENDCANCEL (Winuser. h)
description: Посылается, когда пользователь выбирает элемент, а затем выбирает другой элемент управления или закрывает диалоговое окно. Указывает, что первоначальный выбор пользователя должен игнорироваться. Родительское окно поля со списком получает этот код уведомления через \_ командное сообщение WM.
ms.assetid: ac8d6d9f-4455-42d6-b0f1-5aaa55b8ee42
keywords:
- CBN_SELENDCANCEL кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- CBN_SELENDCANCEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da5b588fbd55af9dfa66a03c7912d4918821168b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803436"
---
# <a name="cbn_selendcancel-notification-code"></a><span data-ttu-id="2b217-106">\_Код уведомления КБН селендканцел</span><span class="sxs-lookup"><span data-stu-id="2b217-106">CBN\_SELENDCANCEL notification code</span></span>

<span data-ttu-id="2b217-107">Посылается, когда пользователь выбирает элемент, а затем выбирает другой элемент управления или закрывает диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="2b217-107">Sent when the user selects an item, but then selects another control or closes the dialog box.</span></span> <span data-ttu-id="2b217-108">Указывает, что первоначальный выбор пользователя должен игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="2b217-108">It indicates the user's initial selection is to be ignored.</span></span> <span data-ttu-id="2b217-109">Родительское окно поля со списком получает этот код уведомления через [**\_ командное сообщение WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="2b217-109">The parent window of the combo box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_SELENDCANCEL

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="2b217-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="2b217-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b217-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2b217-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2b217-112">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) содержит идентификатор элемента управления поля со списком.</span><span class="sxs-lookup"><span data-stu-id="2b217-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="2b217-113">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает код уведомления.</span><span class="sxs-lookup"><span data-stu-id="2b217-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="2b217-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2b217-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2b217-115">Обработайте с полем со списком.</span><span class="sxs-lookup"><span data-stu-id="2b217-115">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2b217-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2b217-116">Remarks</span></span>

<span data-ttu-id="2b217-117">В поле со списком с [**\_ простым**](combo-box-styles.md) стилем CBS \_ код уведомления КБН селендканцел не отправляется.</span><span class="sxs-lookup"><span data-stu-id="2b217-117">In a combo box with the [**CBS\_SIMPLE**](combo-box-styles.md) style, the CBN\_SELENDCANCEL notification code is not sent.</span></span> <span data-ttu-id="2b217-118">Код уведомления [КБН \_ селендок](cbn-selendok.md) отправляется непосредственно перед каждым кодом уведомления [КБН \_ селчанже](cbn-selchange.md) .</span><span class="sxs-lookup"><span data-stu-id="2b217-118">The [CBN\_SELENDOK](cbn-selendok.md) notification code is sent immediately before every [CBN\_SELCHANGE](cbn-selchange.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b217-119">Требования</span><span class="sxs-lookup"><span data-stu-id="2b217-119">Requirements</span></span>



| <span data-ttu-id="2b217-120">Требование</span><span class="sxs-lookup"><span data-stu-id="2b217-120">Requirement</span></span> | <span data-ttu-id="2b217-121">Значение</span><span class="sxs-lookup"><span data-stu-id="2b217-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b217-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2b217-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2b217-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2b217-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2b217-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2b217-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2b217-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2b217-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2b217-126">Header</span><span class="sxs-lookup"><span data-stu-id="2b217-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b217-127"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2b217-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b217-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2b217-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="2b217-129">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="2b217-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2b217-130">КБН \_ селчанже</span><span class="sxs-lookup"><span data-stu-id="2b217-130">CBN\_SELCHANGE</span></span>](cbn-selchange.md)
</dt> <dt>

[<span data-ttu-id="2b217-131">КБН \_ селендок</span><span class="sxs-lookup"><span data-stu-id="2b217-131">CBN\_SELENDOK</span></span>](cbn-selendok.md)
</dt> <dt>

<span data-ttu-id="2b217-132">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="2b217-132">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="2b217-133">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2b217-133">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="2b217-134">[**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2b217-134">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="2b217-135">**\_команда WM**</span><span class="sxs-lookup"><span data-stu-id="2b217-135">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 


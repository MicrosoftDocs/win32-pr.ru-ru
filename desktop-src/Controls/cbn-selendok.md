---
title: Код уведомления CBN_SELENDOK (Winuser. h)
description: Посылается, когда пользователь выбирает элемент списка или выбирает элемент, а затем закрывает список. Указывает, что выбор пользователя должен быть обработан. Родительское окно поля со списком получает этот код уведомления через \_ командное сообщение WM.
ms.assetid: ef0ac46f-2db9-40d6-ba82-7e90d71fdd37
keywords:
- CBN_SELENDOK кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- CBN_SELENDOK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a0b04fcce0ec2b3f6a2bf5b5e04fa4110ad6ceb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654521"
---
# <a name="cbn_selendok-notification-code"></a><span data-ttu-id="58dd6-106">\_Код уведомления КБН селендок</span><span class="sxs-lookup"><span data-stu-id="58dd6-106">CBN\_SELENDOK notification code</span></span>

<span data-ttu-id="58dd6-107">Посылается, когда пользователь выбирает элемент списка или выбирает элемент, а затем закрывает список.</span><span class="sxs-lookup"><span data-stu-id="58dd6-107">Sent when the user selects a list item, or selects an item and then closes the list.</span></span> <span data-ttu-id="58dd6-108">Указывает, что выбор пользователя должен быть обработан.</span><span class="sxs-lookup"><span data-stu-id="58dd6-108">It indicates that the user's selection is to be processed.</span></span> <span data-ttu-id="58dd6-109">Родительское окно поля со списком получает этот код уведомления через [**\_ командное сообщение WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="58dd6-109">The parent window of the combo box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_SELENDOK

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="58dd6-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="58dd6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58dd6-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="58dd6-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="58dd6-112">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) содержит идентификатор элемента управления поля со списком.</span><span class="sxs-lookup"><span data-stu-id="58dd6-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="58dd6-113">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает код уведомления.</span><span class="sxs-lookup"><span data-stu-id="58dd6-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="58dd6-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="58dd6-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="58dd6-115">Обработайте с полем со списком.</span><span class="sxs-lookup"><span data-stu-id="58dd6-115">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="58dd6-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="58dd6-116">Remarks</span></span>

<span data-ttu-id="58dd6-117">В поле со списком с [**\_ простым**](combo-box-styles.md) стилем CBS \_ код уведомления КБН селендок отправляется непосредственно перед каждым кодом уведомления [КБН \_ селчанже](cbn-selchange.md) .</span><span class="sxs-lookup"><span data-stu-id="58dd6-117">In a combo box with the [**CBS\_SIMPLE**](combo-box-styles.md) style, the CBN\_SELENDOK notification code is sent immediately before every [CBN\_SELCHANGE](cbn-selchange.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="58dd6-118">Требования</span><span class="sxs-lookup"><span data-stu-id="58dd6-118">Requirements</span></span>



| <span data-ttu-id="58dd6-119">Требование</span><span class="sxs-lookup"><span data-stu-id="58dd6-119">Requirement</span></span> | <span data-ttu-id="58dd6-120">Значение</span><span class="sxs-lookup"><span data-stu-id="58dd6-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58dd6-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="58dd6-121">Minimum supported client</span></span><br/> | <span data-ttu-id="58dd6-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="58dd6-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="58dd6-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="58dd6-123">Minimum supported server</span></span><br/> | <span data-ttu-id="58dd6-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="58dd6-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="58dd6-125">Header</span><span class="sxs-lookup"><span data-stu-id="58dd6-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="58dd6-126"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="58dd6-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58dd6-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="58dd6-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="58dd6-128">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="58dd6-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="58dd6-129">КБН \_ селчанже</span><span class="sxs-lookup"><span data-stu-id="58dd6-129">CBN\_SELCHANGE</span></span>](cbn-selchange.md)
</dt> <dt>

[<span data-ttu-id="58dd6-130">КБН \_ селендканцел</span><span class="sxs-lookup"><span data-stu-id="58dd6-130">CBN\_SELENDCANCEL</span></span>](cbn-selendcancel.md)
</dt> <dt>

<span data-ttu-id="58dd6-131">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="58dd6-131">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="58dd6-132">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="58dd6-132">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="58dd6-133">[**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="58dd6-133">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="58dd6-134">**\_команда WM**</span><span class="sxs-lookup"><span data-stu-id="58dd6-134">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 


---
title: Код уведомления CBN_SELCHANGE (Winuser. h)
description: Посылается, когда пользователь изменяет текущее выделение в списке поля со списком.
ms.assetid: 2d0d711c-dfc4-485b-97bb-9ccfa7c5864b
keywords:
- CBN_SELCHANGE кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- CBN_SELCHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e921b7856780763923a448e42de072476cc02f6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989377"
---
# <a name="cbn_selchange-notification-code"></a><span data-ttu-id="af28c-104">\_Код уведомления КБН селчанже</span><span class="sxs-lookup"><span data-stu-id="af28c-104">CBN\_SELCHANGE notification code</span></span>

<span data-ttu-id="af28c-105">Посылается, когда пользователь изменяет текущее выделение в списке поля со списком.</span><span class="sxs-lookup"><span data-stu-id="af28c-105">Sent when the user changes the current selection in the list box of a combo box.</span></span> <span data-ttu-id="af28c-106">Пользователь может изменить выбор, щелкнув в списке или используя клавиши со стрелками.</span><span class="sxs-lookup"><span data-stu-id="af28c-106">The user can change the selection by clicking in the list box or by using the arrow keys.</span></span> <span data-ttu-id="af28c-107">Родительское окно поля со списком получает этот код уведомления в виде [**\_ командного сообщения WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="af28c-107">The parent window of the combo box receives this notification code in the form of a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_SELCHANGE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="af28c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="af28c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af28c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="af28c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="af28c-110">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) содержит идентификатор элемента управления поля со списком.</span><span class="sxs-lookup"><span data-stu-id="af28c-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="af28c-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает код уведомления.</span><span class="sxs-lookup"><span data-stu-id="af28c-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="af28c-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="af28c-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="af28c-113">Обработайте с полем со списком.</span><span class="sxs-lookup"><span data-stu-id="af28c-113">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="af28c-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="af28c-114">Remarks</span></span>

<span data-ttu-id="af28c-115">Чтобы получить индекс текущего выделения, отправьте в элемент управления сообщение с параметром [**CB \_**](cb-getcursel.md) .</span><span class="sxs-lookup"><span data-stu-id="af28c-115">To get the index of the current selection, send the [**CB\_GETCURSEL**](cb-getcursel.md) message to the control.</span></span>

<span data-ttu-id="af28c-116">\_Код уведомления КБН селчанже не отправляется, если текущий выбор задается с помощью [**сообщения \_ сеткурсел CB**](cb-setcursel.md) .</span><span class="sxs-lookup"><span data-stu-id="af28c-116">The CBN\_SELCHANGE notification code is not sent when the current selection is set using the [**CB\_SETCURSEL**](cb-setcursel.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="af28c-117">Требования</span><span class="sxs-lookup"><span data-stu-id="af28c-117">Requirements</span></span>



| <span data-ttu-id="af28c-118">Требование</span><span class="sxs-lookup"><span data-stu-id="af28c-118">Requirement</span></span> | <span data-ttu-id="af28c-119">Значение</span><span class="sxs-lookup"><span data-stu-id="af28c-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af28c-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="af28c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="af28c-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="af28c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="af28c-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="af28c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="af28c-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="af28c-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="af28c-124">Header</span><span class="sxs-lookup"><span data-stu-id="af28c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="af28c-125"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="af28c-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af28c-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="af28c-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="af28c-127">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="af28c-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="af28c-128">КБН \_ крупный план</span><span class="sxs-lookup"><span data-stu-id="af28c-128">CBN\_CLOSEUP</span></span>](cbn-closeup.md)
</dt> <dt>

[<span data-ttu-id="af28c-129">КБН \_ дблклк</span><span class="sxs-lookup"><span data-stu-id="af28c-129">CBN\_DBLCLK</span></span>](cbn-dblclk.md)
</dt> <dt>

[<span data-ttu-id="af28c-130">**CB \_**</span><span class="sxs-lookup"><span data-stu-id="af28c-130">**CB\_GETCURSEL**</span></span>](cb-getcursel.md)
</dt> <dt>

[<span data-ttu-id="af28c-131">**\_СЕТКУРСЕЛ CB**</span><span class="sxs-lookup"><span data-stu-id="af28c-131">**CB\_SETCURSEL**</span></span>](cb-setcursel.md)
</dt> <dt>

<span data-ttu-id="af28c-132">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="af28c-132">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="af28c-133">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="af28c-133">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="af28c-134">[**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="af28c-134">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="af28c-135">**\_команда WM**</span><span class="sxs-lookup"><span data-stu-id="af28c-135">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 


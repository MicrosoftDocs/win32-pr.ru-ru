---
title: Код уведомления LBN_SELCHANGE (Winuser. h)
description: Уведомляет приложение о том, что выбор в списке изменился в результате ввода данных пользователем. Родительское окно списка получает этот код уведомления через \_ командное сообщение WM.
ms.assetid: 126d2c47-816e-4179-a870-f5c5a34c5513
keywords:
- LBN_SELCHANGE кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- LBN_SELCHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e029d1753a0fa74f39a59a459d6ede45811a40fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802327"
---
# <a name="lbn_selchange-notification-code"></a><span data-ttu-id="96a5d-105">\_Код уведомления ЛБН селчанже</span><span class="sxs-lookup"><span data-stu-id="96a5d-105">LBN\_SELCHANGE notification code</span></span>

<span data-ttu-id="96a5d-106">Уведомляет приложение о том, что выбор в списке изменился в результате ввода данных пользователем.</span><span class="sxs-lookup"><span data-stu-id="96a5d-106">Notifies the application that the selection in a list box has changed as a result of user input.</span></span> <span data-ttu-id="96a5d-107">Родительское окно списка получает этот код уведомления через [**\_ командное сообщение WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="96a5d-107">The parent window of the list box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
LBN_SELCHANGE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="96a5d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="96a5d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96a5d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="96a5d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="96a5d-110">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) содержит идентификатор поля списка.</span><span class="sxs-lookup"><span data-stu-id="96a5d-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the list box.</span></span> <span data-ttu-id="96a5d-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает код уведомления.</span><span class="sxs-lookup"><span data-stu-id="96a5d-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="96a5d-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="96a5d-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="96a5d-113">Обработайте с списком.</span><span class="sxs-lookup"><span data-stu-id="96a5d-113">Handle to the list box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="96a5d-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="96a5d-114">Remarks</span></span>

<span data-ttu-id="96a5d-115">Этот код уведомления отправляется только в список, в котором имеется стиль [**\_ уведомления фунта**](list-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="96a5d-115">This notification code is sent only by a list box that has the [**LBS\_NOTIFY**](list-box-styles.md) style.</span></span>

<span data-ttu-id="96a5d-116">Этот код уведомления не отправляется, если выбрано сообщение [**\_ сетсел балансировки**](lb-setsel.md)нагрузки, балансировка нагрузки [**\_ сеткурсел**](lb-setcursel.md), [**Балансировка нагрузки \_ селектстринг**](lb-selectstring.md), [**Балансировка нагрузки \_ селитемранже**](lb-selitemrange.md) или [**фунтов \_ селитемранжеекс**](lb-selitemrangeex.md) .</span><span class="sxs-lookup"><span data-stu-id="96a5d-116">This notification code is not sent if the [**LB\_SETSEL**](lb-setsel.md), [**LB\_SETCURSEL**](lb-setcursel.md), [**LB\_SELECTSTRING**](lb-selectstring.md), [**LB\_SELITEMRANGE**](lb-selitemrange.md) or [**LB\_SELITEMRANGEEX**](lb-selitemrangeex.md) message changes the selection.</span></span>

<span data-ttu-id="96a5d-117">Для списка с множественным выбором \_ код уведомления ЛБН селчанже отправляется каждый раз, когда пользователь нажимает клавишу со стрелкой, даже если выделение не изменяется.</span><span class="sxs-lookup"><span data-stu-id="96a5d-117">For a multiple-selection list box, the LBN\_SELCHANGE notification code is sent whenever the user presses an arrow key, even if the selection does not change.</span></span>

## <a name="requirements"></a><span data-ttu-id="96a5d-118">Требования</span><span class="sxs-lookup"><span data-stu-id="96a5d-118">Requirements</span></span>



| <span data-ttu-id="96a5d-119">Требование</span><span class="sxs-lookup"><span data-stu-id="96a5d-119">Requirement</span></span> | <span data-ttu-id="96a5d-120">Значение</span><span class="sxs-lookup"><span data-stu-id="96a5d-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96a5d-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="96a5d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="96a5d-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="96a5d-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="96a5d-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="96a5d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="96a5d-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="96a5d-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="96a5d-125">Header</span><span class="sxs-lookup"><span data-stu-id="96a5d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="96a5d-126"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="96a5d-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96a5d-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="96a5d-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="96a5d-128">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="96a5d-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="96a5d-129">**сеткурсел балансировки нагрузки \_**</span><span class="sxs-lookup"><span data-stu-id="96a5d-129">**LB\_SETCURSEL**</span></span>](lb-setcursel.md)
</dt> <dt>

[<span data-ttu-id="96a5d-130">ЛБН \_ дблклк</span><span class="sxs-lookup"><span data-stu-id="96a5d-130">LBN\_DBLCLK</span></span>](lbn-dblclk.md)
</dt> <dt>

[<span data-ttu-id="96a5d-131">ЛБН \_ селканцел</span><span class="sxs-lookup"><span data-stu-id="96a5d-131">LBN\_SELCANCEL</span></span>](lbn-selcancel.md)
</dt> <dt>

<span data-ttu-id="96a5d-132">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="96a5d-132">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="96a5d-133">**\_команда WM**</span><span class="sxs-lookup"><span data-stu-id="96a5d-133">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 


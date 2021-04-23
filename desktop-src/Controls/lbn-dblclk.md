---
title: Код уведомления LBN_DBLCLK (Winuser. h)
description: Уведомляет приложение о том, что пользователь дважды щелкнул элемент в списке. Родительское окно списка получает этот код уведомления через \_ командное сообщение WM.
ms.assetid: 487282cb-833a-4123-987e-6a417fbd09d4
keywords:
- LBN_DBLCLK кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- LBN_DBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a60623aafb287f2006d9e27da49d0df34c05b05
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803407"
---
# <a name="lbn_dblclk-notification-code"></a><span data-ttu-id="7ec5b-105">\_Код уведомления ЛБН дблклк</span><span class="sxs-lookup"><span data-stu-id="7ec5b-105">LBN\_DBLCLK notification code</span></span>

<span data-ttu-id="7ec5b-106">Уведомляет приложение о том, что пользователь дважды щелкнул элемент в списке.</span><span class="sxs-lookup"><span data-stu-id="7ec5b-106">Notifies the application that the user has double-clicked an item in a list box.</span></span> <span data-ttu-id="7ec5b-107">Родительское окно списка получает этот код уведомления через [**\_ командное сообщение WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="7ec5b-107">The parent window of the list box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
LBN_DBLCLK

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="7ec5b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7ec5b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ec5b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7ec5b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7ec5b-110">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) содержит идентификатор поля списка.</span><span class="sxs-lookup"><span data-stu-id="7ec5b-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the list box.</span></span> <span data-ttu-id="7ec5b-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает код уведомления.</span><span class="sxs-lookup"><span data-stu-id="7ec5b-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="7ec5b-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7ec5b-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7ec5b-113">Обработайте с списком.</span><span class="sxs-lookup"><span data-stu-id="7ec5b-113">Handle to the list box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7ec5b-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7ec5b-114">Remarks</span></span>

<span data-ttu-id="7ec5b-115">Этот код уведомления отправляется только в список, имеющий стиль [**\_ уведомления**](button-styles.md) "L BS".</span><span class="sxs-lookup"><span data-stu-id="7ec5b-115">This notification code is sent only by a list box that has the L [**BS\_NOTIFY**](button-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ec5b-116">Требования</span><span class="sxs-lookup"><span data-stu-id="7ec5b-116">Requirements</span></span>



| <span data-ttu-id="7ec5b-117">Требование</span><span class="sxs-lookup"><span data-stu-id="7ec5b-117">Requirement</span></span> | <span data-ttu-id="7ec5b-118">Значение</span><span class="sxs-lookup"><span data-stu-id="7ec5b-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ec5b-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7ec5b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7ec5b-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7ec5b-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7ec5b-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7ec5b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7ec5b-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7ec5b-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7ec5b-123">Header</span><span class="sxs-lookup"><span data-stu-id="7ec5b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ec5b-124"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7ec5b-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ec5b-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7ec5b-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="7ec5b-126">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="7ec5b-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7ec5b-127">ЛБН \_ селчанже</span><span class="sxs-lookup"><span data-stu-id="7ec5b-127">LBN\_SELCHANGE</span></span>](lbn-selchange.md)
</dt> <dt>

<span data-ttu-id="7ec5b-128">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="7ec5b-128">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="7ec5b-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7ec5b-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="7ec5b-130">[**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7ec5b-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="7ec5b-131">**\_команда WM**</span><span class="sxs-lookup"><span data-stu-id="7ec5b-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 


---
title: Код уведомления BN_DBLCLK (Winuser. h)
description: Посылается, когда пользователь дважды нажимает кнопку.
ms.assetid: 60cc033f-8b84-4aa5-b625-fdee9deb4757
keywords:
- BN_DBLCLK кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- BN_DBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f04c6bf52e213056d85d3a6d038bedb83754a27e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071389"
---
# <a name="bn_dblclk-notification-code"></a><span data-ttu-id="bf4a2-104">\_Код уведомления млрд долл дблклк</span><span class="sxs-lookup"><span data-stu-id="bf4a2-104">BN\_DBLCLK notification code</span></span>

<span data-ttu-id="bf4a2-105">Посылается, когда пользователь дважды нажимает кнопку.</span><span class="sxs-lookup"><span data-stu-id="bf4a2-105">Sent when the user double-clicks a button.</span></span> <span data-ttu-id="bf4a2-106">Этот код уведомления отправляется автоматически для кнопок [**BS \_ усербуттон**](button-styles.md), [**BS \_**](button-styles.md)и [**BS \_ овнердрав**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="bf4a2-106">This notification code is sent automatically for [**BS\_USERBUTTON**](button-styles.md), [**BS\_RADIOBUTTON**](button-styles.md), and [**BS\_OWNERDRAW**](button-styles.md) buttons.</span></span> <span data-ttu-id="bf4a2-107">Другие типы кнопок отправляют млрд долл \_ дблклк только в том случае, если они имеют стиль " [**BS \_**](button-styles.md) ".</span><span class="sxs-lookup"><span data-stu-id="bf4a2-107">Other button types send BN\_DBLCLK only if they have the [**BS\_NOTIFY**](button-styles.md) style.</span></span>

<span data-ttu-id="bf4a2-108">Родительское окно кнопки получает этот код уведомления через [**\_ командное сообщение WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="bf4a2-108">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_DBLCLK

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="bf4a2-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="bf4a2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf4a2-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bf4a2-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bf4a2-111">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) содержит идентификатор элемента управления кнопки.</span><span class="sxs-lookup"><span data-stu-id="bf4a2-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="bf4a2-112">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает код уведомления.</span><span class="sxs-lookup"><span data-stu-id="bf4a2-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="bf4a2-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bf4a2-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bf4a2-114">Маркер кнопки.</span><span class="sxs-lookup"><span data-stu-id="bf4a2-114">A handle to the button.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bf4a2-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bf4a2-115">Remarks</span></span>

<span data-ttu-id="bf4a2-116">МЛРД долл \_ дблклк совпадает с кодом уведомления [млрд долл \_ даублекликкед](bn-doubleclicked.md) .</span><span class="sxs-lookup"><span data-stu-id="bf4a2-116">BN\_DBLCLK is the same as the [BN\_DOUBLECLICKED](bn-doubleclicked.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf4a2-117">Требования</span><span class="sxs-lookup"><span data-stu-id="bf4a2-117">Requirements</span></span>



| <span data-ttu-id="bf4a2-118">Требование</span><span class="sxs-lookup"><span data-stu-id="bf4a2-118">Requirement</span></span> | <span data-ttu-id="bf4a2-119">Значение</span><span class="sxs-lookup"><span data-stu-id="bf4a2-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf4a2-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bf4a2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bf4a2-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bf4a2-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="bf4a2-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bf4a2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bf4a2-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bf4a2-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bf4a2-124">Header</span><span class="sxs-lookup"><span data-stu-id="bf4a2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf4a2-125"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bf4a2-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf4a2-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bf4a2-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="bf4a2-127">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="bf4a2-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="bf4a2-128">\_щелчок млрд долл</span><span class="sxs-lookup"><span data-stu-id="bf4a2-128">BN\_CLICKED</span></span>](bn-clicked.md)
</dt> <dt>

[<span data-ttu-id="bf4a2-129">МЛРД долл \_ даублекликкед</span><span class="sxs-lookup"><span data-stu-id="bf4a2-129">BN\_DOUBLECLICKED</span></span>](bn-doubleclicked.md)
</dt> <dt>

<span data-ttu-id="bf4a2-130">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="bf4a2-130">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="bf4a2-131">**\_команда WM**</span><span class="sxs-lookup"><span data-stu-id="bf4a2-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 


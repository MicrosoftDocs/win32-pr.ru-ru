---
title: Код уведомления LBN_SELCANCEL (Winuser. h)
description: Уведомляет приложение, что пользователь отменил выбор в списке. Родительское окно списка получает этот код уведомления через \_ командное сообщение WM.
ms.assetid: 82e39f22-090e-4dda-8ddc-6a1fe4704fc7
keywords:
- LBN_SELCANCEL кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- LBN_SELCANCEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c192fbdfdb7a351d51993bee89b9b6ec3dab387
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989182"
---
# <a name="lbn_selcancel-notification-code"></a><span data-ttu-id="08989-105">\_Код уведомления ЛБН селканцел</span><span class="sxs-lookup"><span data-stu-id="08989-105">LBN\_SELCANCEL notification code</span></span>

<span data-ttu-id="08989-106">Уведомляет приложение, что пользователь отменил выбор в списке.</span><span class="sxs-lookup"><span data-stu-id="08989-106">Notifies the application that the user has canceled the selection in a list box.</span></span> <span data-ttu-id="08989-107">Родительское окно списка получает этот код уведомления через [**\_ командное сообщение WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="08989-107">The parent window of the list box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
LBN_SELCANCEL

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="08989-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="08989-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08989-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="08989-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="08989-110">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) содержит идентификатор поля списка.</span><span class="sxs-lookup"><span data-stu-id="08989-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the list box.</span></span> <span data-ttu-id="08989-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает код уведомления.</span><span class="sxs-lookup"><span data-stu-id="08989-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="08989-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="08989-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="08989-113">Обработайте с списком.</span><span class="sxs-lookup"><span data-stu-id="08989-113">Handle to the list box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="08989-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="08989-114">Remarks</span></span>

<span data-ttu-id="08989-115">Этот код уведомления отправляется только в список, имеющий стиль [**\_ уведомления**](button-styles.md) "L BS".</span><span class="sxs-lookup"><span data-stu-id="08989-115">This notification code is sent only by a list box that has the L [**BS\_NOTIFY**](button-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="08989-116">Требования</span><span class="sxs-lookup"><span data-stu-id="08989-116">Requirements</span></span>



| <span data-ttu-id="08989-117">Требование</span><span class="sxs-lookup"><span data-stu-id="08989-117">Requirement</span></span> | <span data-ttu-id="08989-118">Значение</span><span class="sxs-lookup"><span data-stu-id="08989-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08989-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="08989-119">Minimum supported client</span></span><br/> | <span data-ttu-id="08989-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="08989-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="08989-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="08989-121">Minimum supported server</span></span><br/> | <span data-ttu-id="08989-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="08989-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="08989-123">Header</span><span class="sxs-lookup"><span data-stu-id="08989-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="08989-124"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="08989-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08989-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="08989-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="08989-126">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="08989-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="08989-127">**сеткурсел балансировки нагрузки \_**</span><span class="sxs-lookup"><span data-stu-id="08989-127">**LB\_SETCURSEL**</span></span>](lb-setcursel.md)
</dt> <dt>

[<span data-ttu-id="08989-128">ЛБН \_ дблклк</span><span class="sxs-lookup"><span data-stu-id="08989-128">LBN\_DBLCLK</span></span>](lbn-dblclk.md)
</dt> <dt>

[<span data-ttu-id="08989-129">ЛБН \_ селчанже</span><span class="sxs-lookup"><span data-stu-id="08989-129">LBN\_SELCHANGE</span></span>](lbn-selchange.md)
</dt> <dt>

<span data-ttu-id="08989-130">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="08989-130">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="08989-131">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="08989-131">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="08989-132">[**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="08989-132">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="08989-133">**\_команда WM**</span><span class="sxs-lookup"><span data-stu-id="08989-133">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 


---
title: Код уведомления STN_CLICKED (Winuser. h)
description: СТНный \_ код уведомления отправляется, когда пользователь щелкает статический элемент управления, который имеет \_ стиль SS notify. Родительское окно элемента управления получает этот код уведомления через \_ командное сообщение WM.
ms.assetid: deeac9e9-c23e-4ffb-a1d7-18782efb7a5c
keywords:
- STN_CLICKED кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- STN_CLICKED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91f63bc496469f6edc26b4f9176f3f9157464bdd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891489"
---
# <a name="stn_clicked-notification-code"></a><span data-ttu-id="b77ed-105">СТН \_ щелчок по коду уведомления</span><span class="sxs-lookup"><span data-stu-id="b77ed-105">STN\_CLICKED notification code</span></span>

<span data-ttu-id="b77ed-106">СТНный \_ код уведомления отправляется, когда пользователь щелкает статический элемент управления, который имеет стиль [**SS \_ Notify**](static-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="b77ed-106">The STN\_CLICKED notification code is sent when the user clicks a static control that has the [**SS\_NOTIFY**](static-control-styles.md) style.</span></span> <span data-ttu-id="b77ed-107">Родительское окно элемента управления получает этот код уведомления через [**\_ командное сообщение WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="b77ed-107">The parent window of the control receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
STN_CLICKED

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="b77ed-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b77ed-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b77ed-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b77ed-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b77ed-110">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) содержит идентификатор статического элемента управления.</span><span class="sxs-lookup"><span data-stu-id="b77ed-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the static control.</span></span> <span data-ttu-id="b77ed-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает код уведомления.</span><span class="sxs-lookup"><span data-stu-id="b77ed-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="b77ed-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b77ed-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b77ed-113">Обработчик статического элемента управления.</span><span class="sxs-lookup"><span data-stu-id="b77ed-113">Handle to the static control.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b77ed-114">Требования</span><span class="sxs-lookup"><span data-stu-id="b77ed-114">Requirements</span></span>



| <span data-ttu-id="b77ed-115">Требование</span><span class="sxs-lookup"><span data-stu-id="b77ed-115">Requirement</span></span> | <span data-ttu-id="b77ed-116">Значение</span><span class="sxs-lookup"><span data-stu-id="b77ed-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b77ed-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b77ed-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b77ed-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b77ed-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b77ed-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b77ed-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b77ed-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b77ed-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b77ed-121">Header</span><span class="sxs-lookup"><span data-stu-id="b77ed-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b77ed-122"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b77ed-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b77ed-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b77ed-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="b77ed-124">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="b77ed-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b77ed-125">СТН \_ дблклк</span><span class="sxs-lookup"><span data-stu-id="b77ed-125">STN\_DBLCLK</span></span>](stn-dblclk.md)
</dt> <dt>

<span data-ttu-id="b77ed-126">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="b77ed-126">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b77ed-127">Статические элементы управления</span><span class="sxs-lookup"><span data-stu-id="b77ed-127">Static Controls</span></span>](static-controls.md)
</dt> <dt>

<span data-ttu-id="b77ed-128">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="b77ed-128">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="b77ed-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b77ed-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="b77ed-130">[**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b77ed-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="b77ed-131">**\_команда WM**</span><span class="sxs-lookup"><span data-stu-id="b77ed-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 


---
title: Код уведомления STN_ENABLE (Winuser. h)
description: '\_Код уведомления о включении СТН отправляется при включении статического элемента управления.'
ms.assetid: daac2ed3-c7cd-46f8-abfa-78754b277ef4
keywords:
- STN_ENABLE кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- STN_ENABLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfc9cc21e884a8a7e907054daa48a21678efa65e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489219"
---
# <a name="stn_enable-notification-code"></a><span data-ttu-id="f31c1-104">СТН \_ включить код уведомления</span><span class="sxs-lookup"><span data-stu-id="f31c1-104">STN\_ENABLE notification code</span></span>

<span data-ttu-id="f31c1-105">\_Код уведомления о включении СТН отправляется при включении статического элемента управления.</span><span class="sxs-lookup"><span data-stu-id="f31c1-105">The STN\_ENABLE notification code is sent when a static control is enabled.</span></span> <span data-ttu-id="f31c1-106">Для получения этого кода уведомления статический элемент управления должен иметь стиль [**SS \_ Notify**](static-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="f31c1-106">The static control must have the [**SS\_NOTIFY**](static-control-styles.md) style to receive this notification code.</span></span> <span data-ttu-id="f31c1-107">Родительское окно элемента управления получает этот код уведомления через [**\_ командное сообщение WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="f31c1-107">The parent window of the control receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
STN_ENABLE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="f31c1-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f31c1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f31c1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f31c1-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f31c1-110">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) содержит идентификатор статического элемента управления.</span><span class="sxs-lookup"><span data-stu-id="f31c1-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the static control.</span></span> <span data-ttu-id="f31c1-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает код уведомления.</span><span class="sxs-lookup"><span data-stu-id="f31c1-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="f31c1-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f31c1-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f31c1-113">Обработчик статического элемента управления.</span><span class="sxs-lookup"><span data-stu-id="f31c1-113">Handle to the static control.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f31c1-114">Требования</span><span class="sxs-lookup"><span data-stu-id="f31c1-114">Requirements</span></span>



| <span data-ttu-id="f31c1-115">Требование</span><span class="sxs-lookup"><span data-stu-id="f31c1-115">Requirement</span></span> | <span data-ttu-id="f31c1-116">Значение</span><span class="sxs-lookup"><span data-stu-id="f31c1-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f31c1-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f31c1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f31c1-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f31c1-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f31c1-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f31c1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f31c1-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f31c1-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f31c1-121">Header</span><span class="sxs-lookup"><span data-stu-id="f31c1-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f31c1-122"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f31c1-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f31c1-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f31c1-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="f31c1-124">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="f31c1-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f31c1-125">\_Отключение СТН</span><span class="sxs-lookup"><span data-stu-id="f31c1-125">STN\_DISABLE</span></span>](stn-disable.md)
</dt> <dt>

<span data-ttu-id="f31c1-126">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="f31c1-126">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f31c1-127">Статические элементы управления</span><span class="sxs-lookup"><span data-stu-id="f31c1-127">Static Controls</span></span>](static-controls.md)
</dt> <dt>

<span data-ttu-id="f31c1-128">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="f31c1-128">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="f31c1-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f31c1-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="f31c1-130">[**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f31c1-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="f31c1-131">**\_команда WM**</span><span class="sxs-lookup"><span data-stu-id="f31c1-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 


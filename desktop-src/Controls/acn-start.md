---
title: Код уведомления ACN_START (Коммктрл. h)
description: Сообщает родительскому окну элемента управления анимации, что началось воспроизведение связанного клипа AVI. Этот код уведомления отправляется в виде \_ командного сообщения WM.
ms.assetid: b4d12225-36f7-4f87-b58a-dac091d14e4c
keywords:
- ACN_START кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- ACN_START
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b0354d8b2b41ea8690be47e70cbc577c064e579
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801540"
---
# <a name="acn_start-notification-code"></a><span data-ttu-id="a0bde-105">\_Код уведомления о запуске АКН</span><span class="sxs-lookup"><span data-stu-id="a0bde-105">ACN\_START notification code</span></span>

<span data-ttu-id="a0bde-106">Сообщает родительскому окну элемента управления анимации, что началось воспроизведение связанного клипа AVI.</span><span class="sxs-lookup"><span data-stu-id="a0bde-106">Notifies an animation control's parent window that the associated AVI clip has started playing.</span></span> <span data-ttu-id="a0bde-107">Этот код уведомления отправляется в виде [**\_ командного сообщения WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="a0bde-107">This notification code is sent in the form of a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
ACN_START 

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="a0bde-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a0bde-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0bde-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a0bde-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a0bde-110">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) содержит идентификатор элемента управления анимацией.</span><span class="sxs-lookup"><span data-stu-id="a0bde-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the animation control's identifier.</span></span> <span data-ttu-id="a0bde-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает код уведомления.</span><span class="sxs-lookup"><span data-stu-id="a0bde-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="a0bde-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a0bde-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a0bde-113">**HWND** , указывающий дескриптор для элемента управления анимации.</span><span class="sxs-lookup"><span data-stu-id="a0bde-113">An **HWND** that specifies the handle to the animation control.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a0bde-114">Требования</span><span class="sxs-lookup"><span data-stu-id="a0bde-114">Requirements</span></span>



| <span data-ttu-id="a0bde-115">Требование</span><span class="sxs-lookup"><span data-stu-id="a0bde-115">Requirement</span></span> | <span data-ttu-id="a0bde-116">Значение</span><span class="sxs-lookup"><span data-stu-id="a0bde-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a0bde-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a0bde-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a0bde-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a0bde-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a0bde-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a0bde-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a0bde-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a0bde-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a0bde-121">Header</span><span class="sxs-lookup"><span data-stu-id="a0bde-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0bde-122"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0bde-122"><dt>Commctrl.h</dt></span></span> </dl> |



 


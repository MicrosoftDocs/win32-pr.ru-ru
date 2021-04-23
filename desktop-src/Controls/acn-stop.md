---
title: Код уведомления ACN_STOP (Коммктрл. h)
description: Уведомляет родительское окно элемента управления анимации о том, что связанный ролик AVI прекратил воспроизведение. Этот код уведомления отправляется в виде \_ командного сообщения WM.
ms.assetid: 2f21a2ec-975f-4592-8b21-956bd5311ef4
keywords:
- ACN_STOP кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- ACN_STOP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cbdb27677439b7f08b489cba9024d44f3ebee6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071331"
---
# <a name="acn_stop-notification-code"></a><span data-ttu-id="0c29c-105">АКН \_ код уведомления о прерывании</span><span class="sxs-lookup"><span data-stu-id="0c29c-105">ACN\_STOP notification code</span></span>

<span data-ttu-id="0c29c-106">Уведомляет родительское окно элемента управления анимации о том, что связанный ролик AVI прекратил воспроизведение.</span><span class="sxs-lookup"><span data-stu-id="0c29c-106">Notifies the parent window of an animation control that the associated AVI clip has stopped playing.</span></span> <span data-ttu-id="0c29c-107">Этот код уведомления отправляется в виде [**\_ командного сообщения WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="0c29c-107">This notification code is sent in the form of a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
ACN_STOP     

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="0c29c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="0c29c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c29c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0c29c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0c29c-110">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) содержит идентификатор элемента управления анимацией.</span><span class="sxs-lookup"><span data-stu-id="0c29c-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the animation control's identifier.</span></span> <span data-ttu-id="0c29c-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает код уведомления.</span><span class="sxs-lookup"><span data-stu-id="0c29c-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="0c29c-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0c29c-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0c29c-113">**HWND** , указывающий дескриптор для элемента управления анимации.</span><span class="sxs-lookup"><span data-stu-id="0c29c-113">An **HWND** that specifies the handle to the animation control.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0c29c-114">Требования</span><span class="sxs-lookup"><span data-stu-id="0c29c-114">Requirements</span></span>



| <span data-ttu-id="0c29c-115">Требование</span><span class="sxs-lookup"><span data-stu-id="0c29c-115">Requirement</span></span> | <span data-ttu-id="0c29c-116">Значение</span><span class="sxs-lookup"><span data-stu-id="0c29c-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0c29c-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0c29c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0c29c-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0c29c-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0c29c-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0c29c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0c29c-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0c29c-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0c29c-121">Header</span><span class="sxs-lookup"><span data-stu-id="0c29c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c29c-122"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c29c-122"><dt>Commctrl.h</dt></span></span> </dl> |



 


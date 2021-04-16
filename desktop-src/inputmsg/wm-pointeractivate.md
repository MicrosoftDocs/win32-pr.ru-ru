---
title: Сообщение WM_POINTERACTIVATE
description: Отправляется в неактивное окно, когда первичный указатель создает WM_POINTERDOWN над окном.
ms.assetid: 4eec37da-227c-4be1-bf0b-99704caa1322
keywords:
- WM_POINTERACTIVATE сообщения и уведомления о входе
topic_type:
- apiref
api_name:
- WM_POINTERACTIVATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: b9bda11b5cb7a27f7744df6e20890a125a66bd88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105719198"
---
# <a name="wm_pointeractivate-message"></a><span data-ttu-id="8e07d-104">Сообщение WM_POINTERACTIVATE</span><span class="sxs-lookup"><span data-stu-id="8e07d-104">WM_POINTERACTIVATE message</span></span>

<span data-ttu-id="8e07d-105">Отправляется в неактивное окно, когда первичный указатель создает [**WM_POINTERDOWN**](wm-pointerdown.md) над окном.</span><span class="sxs-lookup"><span data-stu-id="8e07d-105">Sent to an inactive window when a primary pointer generates a [**WM_POINTERDOWN**](wm-pointerdown.md) over the window.</span></span> <span data-ttu-id="8e07d-106">Пока сообщение остается необработанным, оно перемещается вверх по цепочке родительских окон, пока не достигнет окна верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="8e07d-106">As long as the message remains unhandled, it travels up the parent window chain until it is reaches the top-level window.</span></span> <span data-ttu-id="8e07d-107">Приложения могут отвечать на это сообщение, чтобы указать, нужно ли его активировать.</span><span class="sxs-lookup"><span data-stu-id="8e07d-107">Applications can respond to this message to specify whether they wish to be activated.</span></span>

<span data-ttu-id="8e07d-108">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="8e07d-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_POINTERACTIVATE             0x024B
```



## <a name="parameters"></a><span data-ttu-id="8e07d-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="8e07d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e07d-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8e07d-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8e07d-111">Содержит идентификатор указателя и дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="8e07d-111">Contains the pointer identifier and additional information.</span></span> <span data-ttu-id="8e07d-112">Используйте следующие макросы для получения этих сведений.</span><span class="sxs-lookup"><span data-stu-id="8e07d-112">Use the following macros to retrieve this information.</span></span>

<span data-ttu-id="8e07d-113">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): идентификатор указателя</span><span class="sxs-lookup"><span data-stu-id="8e07d-113">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): pointer identifier</span></span>

<span data-ttu-id="8e07d-114">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(wParam): значение проверки попадания, возвращаемое при обработке сообщения [**WM_NCHITTEST**](../inputdev/wm-nchittest.md) .</span><span class="sxs-lookup"><span data-stu-id="8e07d-114">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(wParam): hit-test value returned from processing the [**WM_NCHITTEST**](../inputdev/wm-nchittest.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="8e07d-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8e07d-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8e07d-116">Содержит маркер окна верхнего уровня активируемого окна.</span><span class="sxs-lookup"><span data-stu-id="8e07d-116">Contains the handle to the top-level window of the window being activated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e07d-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8e07d-117">Return value</span></span>

<span data-ttu-id="8e07d-118">Если приложение обрабатывает это сообщение, оно должно вернуть одно из значений, описанных в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="8e07d-118">If an application processes this message, it should return one of the values described in the Remarks section.</span></span>

<span data-ttu-id="8e07d-119">Если приложение не обрабатывает это сообщение, оно должно вызывать [**дефвиндовпрок**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="8e07d-119">If the application does not process this message, it should call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="8e07d-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8e07d-120">Remarks</span></span>

<span data-ttu-id="8e07d-121">Приложение может обрабатывать это сообщение и возвращать одно из следующих значений, чтобы определить, как система обрабатывает активацию и входные данные активации:</span><span class="sxs-lookup"><span data-stu-id="8e07d-121">An application can handle this message and return one of the following values to determine how the system processes the activation and the activating input:</span></span>

-   <span data-ttu-id="8e07d-122">PA_ACTIVATE</span><span class="sxs-lookup"><span data-stu-id="8e07d-122">PA_ACTIVATE</span></span>
-   <span data-ttu-id="8e07d-123">PA_NOACTIVATE</span><span class="sxs-lookup"><span data-stu-id="8e07d-123">PA_NOACTIVATE</span></span>

<span data-ttu-id="8e07d-124">Важно отметить, что когда пользователь взаимодействует с системой с несколькими одновременными указателями, возможность активации, которую представляет **WM_POINTERACTIVATE** сообщение, доступна приложениям только для первого из этих указателей.</span><span class="sxs-lookup"><span data-stu-id="8e07d-124">It is important to note that, when the user is interacting with the system with multiple simultaneous pointers, the activation opportunity that the **WM_POINTERACTIVATE** message represents is available to applications only for the first of those pointers.</span></span> <span data-ttu-id="8e07d-125">Поэтому приложения должны иметь в виду, что они по-прежнему могут получать входные данные из указателей, когда они неактивны.</span><span class="sxs-lookup"><span data-stu-id="8e07d-125">Applications should, therefore, be aware that they may still receive input from pointers while they are inactive.</span></span>

<span data-ttu-id="8e07d-126">Если приложение не обрабатывает это сообщение, [**дефвиндовпрок**](/windows/win32/api/winuser/nf-winuser-defwindowproca) передает сообщение родительскому окну.</span><span class="sxs-lookup"><span data-stu-id="8e07d-126">If the application does not handle this message, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) passes the message to the parent window.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e07d-127">Требования</span><span class="sxs-lookup"><span data-stu-id="8e07d-127">Requirements</span></span>



| <span data-ttu-id="8e07d-128">Требование</span><span class="sxs-lookup"><span data-stu-id="8e07d-128">Requirement</span></span> | <span data-ttu-id="8e07d-129">Значение</span><span class="sxs-lookup"><span data-stu-id="8e07d-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e07d-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8e07d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="8e07d-131">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="8e07d-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="8e07d-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8e07d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="8e07d-133">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="8e07d-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8e07d-134">Header</span><span class="sxs-lookup"><span data-stu-id="8e07d-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e07d-135"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8e07d-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e07d-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8e07d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e07d-137">Сообщения</span><span class="sxs-lookup"><span data-stu-id="8e07d-137">Messages</span></span>](messages.md)
</dt> </dl>

 


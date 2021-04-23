---
title: Сообщение WM_GESTURENOTIFY (Winuser. h)
description: Дает возможность задать конфигурацию жестов.
ms.assetid: 83c23928-86ce-421d-bb84-5c41a770bf60
keywords:
- WM_GESTURENOTIFY сообщений Windows Touch
topic_type:
- apiref
api_name:
- WM_GESTURENOTIFY
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e900e4b607760df16938080a49f97a3ab0cf2ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136466"
---
# <a name="wm_gesturenotify-message"></a><span data-ttu-id="622a0-104">\_Сообщение ЖЕСТУРЕНОТИФИ WM</span><span class="sxs-lookup"><span data-stu-id="622a0-104">WM\_GESTURENOTIFY message</span></span>

<span data-ttu-id="622a0-105">Дает возможность задать конфигурацию жестов.</span><span class="sxs-lookup"><span data-stu-id="622a0-105">Gives you a chance to set the gesture configuration.</span></span>

## <a name="parameters"></a><span data-ttu-id="622a0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="622a0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="622a0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="622a0-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="622a0-108">Не используется.</span><span class="sxs-lookup"><span data-stu-id="622a0-108">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="622a0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="622a0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="622a0-110">Указатель на [**жестуренотифиструкт**](/windows/win32/api/winuser/ns-winuser-gesturenotifystruct).</span><span class="sxs-lookup"><span data-stu-id="622a0-110">A pointer to a [**GESTURENOTIFYSTRUCT**](/windows/win32/api/winuser/ns-winuser-gesturenotifystruct).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="622a0-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="622a0-111">Return value</span></span>

<span data-ttu-id="622a0-112">Значение должно возвращаться из [дефвиндовпрок](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="622a0-112">A value should be returned from [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="622a0-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="622a0-113">Remarks</span></span>

<span data-ttu-id="622a0-114">Когда получено сообщение **WM \_ жестуренотифи** , приложение может использовать [**сетжестуреконфиг**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig) для указания получаемых жестов.</span><span class="sxs-lookup"><span data-stu-id="622a0-114">When the **WM\_GESTURENOTIFY** message is received, the application can use [**SetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig) to specify the gestures to receive.</span></span> <span data-ttu-id="622a0-115">Это сообщение всегда должно быть собрано с помощью функции [дефвиндовпрок](/windows/win32/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="622a0-115">This message should always be bubbled up using the [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) function.</span></span>

> [!Note]  
> <span data-ttu-id="622a0-116">Обработка сообщения **WM \_ жестуренотифи** изменит конфигурацию жестов на время существования окна, а не только на следующий жест.</span><span class="sxs-lookup"><span data-stu-id="622a0-116">Handling the **WM\_GESTURENOTIFY** message will change the gesture configuration for the lifetime of the Window, not just for the next gesture.</span></span>

 

## <a name="examples"></a><span data-ttu-id="622a0-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="622a0-117">Examples</span></span>

<span data-ttu-id="622a0-118">В следующем примере показано, как включить все жесты.</span><span class="sxs-lookup"><span data-stu-id="622a0-118">The following example shows how to enable all gestures.</span></span> <span data-ttu-id="622a0-119">Дополнительные примеры см. в разделе [**сетжестуреконфиг**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig).</span><span class="sxs-lookup"><span data-stu-id="622a0-119">For more examples, see [**SetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig).</span></span>


```C++
    switch (message)
    {
    case WM_GESTURENOTIFY:
        GESTURECONFIG gc = {0,GC_ALLGESTURES,0};
        BOOL bResult = SetGestureConfig(hWnd,0,1,&gc,sizeof(GESTURECONFIG));
            
        if(!bResult)
        {
            // an error
        }
        return DefWindowProc(hWnd, WM_GESTURENOTIFY, wParam, lParam);
    }
      
```



## <a name="requirements"></a><span data-ttu-id="622a0-120">Требования</span><span class="sxs-lookup"><span data-stu-id="622a0-120">Requirements</span></span>



| <span data-ttu-id="622a0-121">Требование</span><span class="sxs-lookup"><span data-stu-id="622a0-121">Requirement</span></span> | <span data-ttu-id="622a0-122">Значение</span><span class="sxs-lookup"><span data-stu-id="622a0-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="622a0-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="622a0-123">Minimum supported client</span></span><br/> | <span data-ttu-id="622a0-124">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="622a0-124">Windows 7 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="622a0-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="622a0-125">Minimum supported server</span></span><br/> | <span data-ttu-id="622a0-126">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="622a0-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="622a0-127">Header</span><span class="sxs-lookup"><span data-stu-id="622a0-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="622a0-128"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="622a0-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="622a0-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="622a0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="622a0-130">Уведомления</span><span class="sxs-lookup"><span data-stu-id="622a0-130">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="622a0-131">Инструкции по программированию жестов сенсорного ввода Windows</span><span class="sxs-lookup"><span data-stu-id="622a0-131">Windows Touch Gestures Programming Guide</span></span>](guide-multi-touch-gestures.md)
</dt> <dt>

[<span data-ttu-id="622a0-132">**жестуренотифиструкт**</span><span class="sxs-lookup"><span data-stu-id="622a0-132">**GESTURENOTIFYSTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-gesturenotifystruct)
</dt> <dt>

[<span data-ttu-id="622a0-133">**сетжестуреконфиг**</span><span class="sxs-lookup"><span data-stu-id="622a0-133">**SetGestureConfig**</span></span>](/windows/desktop/api/winuser/nf-winuser-setgestureconfig)
</dt> </dl>

 


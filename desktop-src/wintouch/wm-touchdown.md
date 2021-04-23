---
title: Сообщение WM_TOUCH (Winuser. h)
description: Уведомляет окно, когда одна или несколько сенсорных точек, таких как палец или перо, касаются сенсорной поверхности дигитайзера.
ms.assetid: 5dee8bab-34fa-4dd9-a65b-35883757ec80
keywords:
- WM_TOUCH сообщений Windows Touch
topic_type:
- apiref
api_name:
- WM_TOUCH
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b6242d43b661240d946d2883237640d1bc92b3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415812"
---
# <a name="wm_touch-message"></a><span data-ttu-id="14855-104">\_Сообщение касания WM</span><span class="sxs-lookup"><span data-stu-id="14855-104">WM\_TOUCH message</span></span>

<span data-ttu-id="14855-105">Уведомляет окно, когда одна или несколько сенсорных точек, таких как палец или перо, касаются сенсорной поверхности дигитайзера.</span><span class="sxs-lookup"><span data-stu-id="14855-105">Notifies the window when one or more touch points, such as a finger or pen, touches a touch-sensitive digitizer surface.</span></span>

## <a name="parameters"></a><span data-ttu-id="14855-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="14855-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14855-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="14855-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="14855-108">Слово нижнего порядка содержит количество сенсорных точек, связанных с этим сообщением.</span><span class="sxs-lookup"><span data-stu-id="14855-108">The low-order word contains the number of touch points associated with this message.</span></span> <span data-ttu-id="14855-109">Слово высокого порядка зарезервировано для будущего использования.</span><span class="sxs-lookup"><span data-stu-id="14855-109">The high-order word is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="14855-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="14855-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="14855-111">Содержит входной маркер касания, который можно использовать в вызове [**жеттаучинпутинфо**](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo) для получения подробных сведений о сенсорных точках, связанных с этим сообщением.</span><span class="sxs-lookup"><span data-stu-id="14855-111">Contains a touch input handle that can be used in a call to [**GetTouchInputInfo**](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo) to retrieve detailed information about the touch points associated with this message.</span></span>

<span data-ttu-id="14855-112">Этот обработчик действителен только в пределах текущего процесса и не должен передаваться между процессами, за исключением случаев, когда **lParam** используется в вызовах **SendMessage** или @ **Message** .</span><span class="sxs-lookup"><span data-stu-id="14855-112">This handle is valid only within the current process and should not be passed cross-process except as the **LPARAM** in a **SendMessage** or **PostMessage** call.</span></span>

<span data-ttu-id="14855-113">Если приложению больше не требуется этот обработчик, приложение должно вызвать **клосетаучинпусандле** , чтобы освободить память процесса, связанную с этим маркером.</span><span class="sxs-lookup"><span data-stu-id="14855-113">When the application no longer requires this handle, the application must call **CloseTouchInputHandle** to free the process memory associated with this handle.</span></span> <span data-ttu-id="14855-114">Если этого не сделать, это может привести к утечке памяти приложения.</span><span class="sxs-lookup"><span data-stu-id="14855-114">Failing to do so can result in an application memory leak.</span></span>

<span data-ttu-id="14855-115">Обратите внимание, что маркер сенсорного ввода в этом параметре больше не действителен после передачи сообщения в [дефвиндовпрок](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="14855-115">Note that the touch input handle in this parameter is no longer valid after the message has been passed to [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span> <span data-ttu-id="14855-116">[Дефвиндовпрок](/windows/win32/api/winuser/nf-winuser-defwindowproca) закроет и сделает этот маркер недействительным.</span><span class="sxs-lookup"><span data-stu-id="14855-116">[DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) will close and invalidate this handle.</span></span>

<span data-ttu-id="14855-117">Обратите внимание, что маркер сенсорного ввода в этом параметре больше не действителен после пересылки сообщения с помощью [**сообщения**](sendmessage--postmessage--and-related-functions.md), **SendMessage** или одного из вариантов.</span><span class="sxs-lookup"><span data-stu-id="14855-117">Note also that the touch input handle in this parameter is no longer valid after the message has been forwarded using [**PostMessage**](sendmessage--postmessage--and-related-functions.md), **SendMessage**, or one of their variants.</span></span> <span data-ttu-id="14855-118">Эти функции закрывают и не проверяют этот обработчик.</span><span class="sxs-lookup"><span data-stu-id="14855-118">These functions will close and invalidate this handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14855-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="14855-119">Return value</span></span>

<span data-ttu-id="14855-120">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="14855-120">If an application processes this message, it should return zero.</span></span>

<span data-ttu-id="14855-121">Если приложение не обрабатывает сообщение, оно должно вызвать [дефвиндовпрок](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="14855-121">If the application does not process the message, it must call [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span> <span data-ttu-id="14855-122">Это приводит к утечке памяти в приложении, поскольку дескриптор сенсорного ввода не закрыт, а связанная память процесса не освобождается.</span><span class="sxs-lookup"><span data-stu-id="14855-122">Not doing so causes the application to leak memory because the touch input handle is not closed and associated process memory is not freed.</span></span>

## <a name="remarks"></a><span data-ttu-id="14855-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="14855-123">Remarks</span></span>

<span data-ttu-id="14855-124">**WM \_ СЕНСОРные** сообщения не учитывают **хттранспарент** области Windows.</span><span class="sxs-lookup"><span data-stu-id="14855-124">**WM\_TOUCH** messages do not respect **HTTRANSPARENT** regions of windows.</span></span> <span data-ttu-id="14855-125">Если окно возвращает **хттранспарент** в ответ на сообщение **\_ нчиттест WM** , сообщения мыши переходят к родительскому элементу, а сообщения **WM \_ Touch** переходят непосредственно в окно.</span><span class="sxs-lookup"><span data-stu-id="14855-125">If a window returns **HTTRANSPARENT** in response to a **WM\_NCHITTEST** message, mouse messages go to the parent, and **WM\_TOUCH** messages go directly to the window.</span></span>

## <a name="examples"></a><span data-ttu-id="14855-126">Примеры</span><span class="sxs-lookup"><span data-stu-id="14855-126">Examples</span></span>

<span data-ttu-id="14855-127">В следующем коде приведен пример того, как получить подробные данные сенсорного ввода, связанные с этим сообщением.</span><span class="sxs-lookup"><span data-stu-id="14855-127">The following code is an example of how to obtain detailed touch input information associated with this message.</span></span>


```C++
UINT cInputs = LOWORD(wParam);
PTOUCHINPUT pInputs = new TOUCHINPUT[cInputs];
if (NULL != pInputs)
{
    if (GetTouchInputInfo((HTOUCHINPUT)lParam,
                          cInputs,
                          pInputs,
                          sizeof(TOUCHINPUT)))
    {
        // process pInputs
        if (!CloseTouchInputHandle((HTOUCHINPUT)lParam))
        {
            // error handling
        }
    }
    else
    {
        // GetLastError() and error handling
    }
    delete [] pInputs;
}
else
{
    // error handling, presumably out of memory
}
return DefWindowProc(hWnd, message, wParam, lParam);
```



## <a name="requirements"></a><span data-ttu-id="14855-128">Требования</span><span class="sxs-lookup"><span data-stu-id="14855-128">Requirements</span></span>



| <span data-ttu-id="14855-129">Требование</span><span class="sxs-lookup"><span data-stu-id="14855-129">Requirement</span></span> | <span data-ttu-id="14855-130">Значение</span><span class="sxs-lookup"><span data-stu-id="14855-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14855-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="14855-131">Minimum supported client</span></span><br/> | <span data-ttu-id="14855-132">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="14855-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="14855-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="14855-133">Minimum supported server</span></span><br/> | <span data-ttu-id="14855-134">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="14855-134">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="14855-135">Header</span><span class="sxs-lookup"><span data-stu-id="14855-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="14855-136"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="14855-136"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14855-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="14855-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14855-138">Сообщения</span><span class="sxs-lookup"><span data-stu-id="14855-138">Messages</span></span>](messages.md)
</dt> <dt>

[<span data-ttu-id="14855-139">Инструкции по программированию и обработке инерции</span><span class="sxs-lookup"><span data-stu-id="14855-139">Manipulations and Inertia Programming Guide</span></span>](manipulation-and-inertia.md)
</dt> <dt>

[<span data-ttu-id="14855-140">Справочное руководством по программированию ввода Windows Touch</span><span class="sxs-lookup"><span data-stu-id="14855-140">Windows Touch Input Programming Guide</span></span>](guide-multi-touch-input.md)
</dt> </dl>

 


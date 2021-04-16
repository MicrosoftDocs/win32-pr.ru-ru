---
description: Отправляется в приложение для предоставления команд и запроса информации. Окно получает это сообщение через функцию WindowProc.
ms.assetid: c5e9f256-eed2-46cb-bb33-0e640a975f1f
title: Сообщение WM_IME_REQUEST (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d0cea120d088fe1423b1d7dcb822307886675b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650546"
---
# <a name="wm_ime_request-message"></a><span data-ttu-id="d77c0-104">Сообщение WM_IME_REQUEST</span><span class="sxs-lookup"><span data-stu-id="d77c0-104">WM_IME_REQUEST message</span></span>

<span data-ttu-id="d77c0-105">Отправляется в приложение для предоставления команд и запроса информации.</span><span class="sxs-lookup"><span data-stu-id="d77c0-105">Sent to an application to provide commands and request information.</span></span> <span data-ttu-id="d77c0-106">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="d77c0-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,       
  WM_IME_REQUEST,  
  WPARAM wParam,   
  LPARAM lParam    
);
```



## <a name="parameters"></a><span data-ttu-id="d77c0-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="d77c0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d77c0-108">*HWND*</span><span class="sxs-lookup"><span data-stu-id="d77c0-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="d77c0-109">Маркер для окна.</span><span class="sxs-lookup"><span data-stu-id="d77c0-109">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="d77c0-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d77c0-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d77c0-111">Команда</span><span class="sxs-lookup"><span data-stu-id="d77c0-111">Command.</span></span> <span data-ttu-id="d77c0-112">Этот параметр может принимать одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="d77c0-112">This parameter can have one of the following values:</span></span>

<dl> 
<dd><span data-ttu-id="d77c0-113"><a href="imr-candidatewindow.md">IMR_CANDIDATEWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="d77c0-113"><a href="imr-candidatewindow.md">IMR_CANDIDATEWINDOW</a></span></span></dd> 
<dd><span data-ttu-id="d77c0-114"><a href="imr-compositionfont.md">IMR_COMPOSITIONFONT</a></span><span class="sxs-lookup"><span data-stu-id="d77c0-114"><a href="imr-compositionfont.md">IMR_COMPOSITIONFONT</a></span></span></dd> 
<dd><span data-ttu-id="d77c0-115"><a href="imr-compositionwindow.md">IMR_COMPOSITIONWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="d77c0-115"><a href="imr-compositionwindow.md">IMR_COMPOSITIONWINDOW</a></span></span></dd> 
<dd><span data-ttu-id="d77c0-116"><a href="imr-confirmreconvertstring.md">IMR_CONFIRMRECONVERTSTRING</a></span><span class="sxs-lookup"><span data-stu-id="d77c0-116"><a href="imr-confirmreconvertstring.md">IMR_CONFIRMRECONVERTSTRING</a></span></span></dd> 
<dd><span data-ttu-id="d77c0-117"><a href="imr-documentfeed.md">IMR_DOCUMENTFEED</a></span><span class="sxs-lookup"><span data-stu-id="d77c0-117"><a href="imr-documentfeed.md">IMR_DOCUMENTFEED</a></span></span></dd> 
<dd><span data-ttu-id="d77c0-118"><a href="imr-querycharposition.md">IMR_QUERYCHARPOSITION</a></span><span class="sxs-lookup"><span data-stu-id="d77c0-118"><a href="imr-querycharposition.md">IMR_QUERYCHARPOSITION</a></span></span></dd> 
<dd><span data-ttu-id="d77c0-119"><a href="imr-reconvertstring.md">IMR_RECONVERTSTRING</a></span><span class="sxs-lookup"><span data-stu-id="d77c0-119"><a href="imr-reconvertstring.md">IMR_RECONVERTSTRING</a></span></span></dd> 
</dl> 
</dd> 
<dt>

<span data-ttu-id="d77c0-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d77c0-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d77c0-121">Данные, относящиеся к команде.</span><span class="sxs-lookup"><span data-stu-id="d77c0-121">Command-specific data.</span></span> <span data-ttu-id="d77c0-122">Дополнительные сведения см. в описании каждой команды.</span><span class="sxs-lookup"><span data-stu-id="d77c0-122">For more information, see the description for each command.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d77c0-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d77c0-123">Return value</span></span>

<span data-ttu-id="d77c0-124">Возвращает значение, зависящее от команды.</span><span class="sxs-lookup"><span data-stu-id="d77c0-124">Returns a command-specific value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d77c0-125">Требования</span><span class="sxs-lookup"><span data-stu-id="d77c0-125">Requirements</span></span>



| <span data-ttu-id="d77c0-126">Требование</span><span class="sxs-lookup"><span data-stu-id="d77c0-126">Requirement</span></span> | <span data-ttu-id="d77c0-127">Значение</span><span class="sxs-lookup"><span data-stu-id="d77c0-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d77c0-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d77c0-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d77c0-129">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d77c0-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                                                                |
| <span data-ttu-id="d77c0-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d77c0-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d77c0-131">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d77c0-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="d77c0-132">Заголовок</span><span class="sxs-lookup"><span data-stu-id="d77c0-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="d77c0-133"><dt>Winuser. h (включает Windows. h); </dt> <dt>IMM. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d77c0-133"><dt>Winuser.h (include Windows.h); </dt> <dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d77c0-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d77c0-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d77c0-135">Диспетчер метода ввода</span><span class="sxs-lookup"><span data-stu-id="d77c0-135">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="d77c0-136">Сообщения диспетчера методов ввода</span><span class="sxs-lookup"><span data-stu-id="d77c0-136">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> <dt>

[<span data-ttu-id="d77c0-137">IMR_CANDIDATEWINDOW</span><span class="sxs-lookup"><span data-stu-id="d77c0-137">IMR_CANDIDATEWINDOW</span></span>](imr-candidatewindow.md)
</dt> <dt>

[<span data-ttu-id="d77c0-138">IMR_COMPOSITIONFONT</span><span class="sxs-lookup"><span data-stu-id="d77c0-138">IMR_COMPOSITIONFONT</span></span>](imr-compositionfont.md)
</dt> <dt>

[<span data-ttu-id="d77c0-139">IMR_COMPOSITIONWINDOW</span><span class="sxs-lookup"><span data-stu-id="d77c0-139">IMR_COMPOSITIONWINDOW</span></span>](imr-compositionwindow.md)
</dt> <dt>

[<span data-ttu-id="d77c0-140">IMR_CONFIRMRECONVERTSTRING</span><span class="sxs-lookup"><span data-stu-id="d77c0-140">IMR_CONFIRMRECONVERTSTRING</span></span>](imr-confirmreconvertstring.md)
</dt> <dt>

[<span data-ttu-id="d77c0-141">IMR_DOCUMENTFEED</span><span class="sxs-lookup"><span data-stu-id="d77c0-141">IMR_DOCUMENTFEED</span></span>](imr-documentfeed.md)
</dt> <dt>

[<span data-ttu-id="d77c0-142">IMR_QUERYCHARPOSITION</span><span class="sxs-lookup"><span data-stu-id="d77c0-142">IMR_QUERYCHARPOSITION</span></span>](imr-querycharposition.md)
</dt> <dt>

[<span data-ttu-id="d77c0-143">IMR_RECONVERTSTRING</span><span class="sxs-lookup"><span data-stu-id="d77c0-143">IMR_RECONVERTSTRING</span></span>](imr-reconvertstring.md)
</dt> </dl>

 

 

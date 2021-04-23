---
description: Отправляется в приложение для уведомления об изменениях в окне IME. Окно получает это сообщение через функцию WindowProc.
ms.assetid: 20e064b8-2baf-4b4c-8341-36c3e4643eff
title: Сообщение WM_IME_NOTIFY (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca5ab1b2a1fd62d159ab4f216bf9b1bb6892ed69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682725"
---
# <a name="wm_ime_notify-message"></a><span data-ttu-id="6b995-104">Сообщение WM_IME_NOTIFY</span><span class="sxs-lookup"><span data-stu-id="6b995-104">WM_IME_NOTIFY message</span></span>

<span data-ttu-id="6b995-105">Отправляется в приложение для уведомления об изменениях в окне IME.</span><span class="sxs-lookup"><span data-stu-id="6b995-105">Sent to an application to notify it of changes to the IME window.</span></span> <span data-ttu-id="6b995-106">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="6b995-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,       
  WM_IME_NOTIFY,   
  WPARAM wParam,   
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="6b995-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="6b995-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b995-108">*HWND*</span><span class="sxs-lookup"><span data-stu-id="6b995-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="6b995-109">Маркер для окна.</span><span class="sxs-lookup"><span data-stu-id="6b995-109">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="6b995-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6b995-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6b995-111">Команда.</span><span class="sxs-lookup"><span data-stu-id="6b995-111">The command.</span></span> <span data-ttu-id="6b995-112">Этот параметр может иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="6b995-112">This parameter can have one of the following values.</span></span>

<dl>
<dd><span data-ttu-id="6b995-113"><a href="imn-changecandidate.md">IMN_CHANGECANDIDATE</a></span><span class="sxs-lookup"><span data-stu-id="6b995-113"><a href="imn-changecandidate.md">IMN_CHANGECANDIDATE</a></span></span></dd> 
<dd><span data-ttu-id="6b995-114"><a href="imn-closecandidate.md">IMN_CLOSECANDIDATE</a></span><span class="sxs-lookup"><span data-stu-id="6b995-114"><a href="imn-closecandidate.md">IMN_CLOSECANDIDATE</a></span></span></dd> 
<dd><span data-ttu-id="6b995-115"><a href="imn-closestatuswindow.md">IMN_CLOSESTATUSWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="6b995-115"><a href="imn-closestatuswindow.md">IMN_CLOSESTATUSWINDOW</a></span></span></dd> 
<dd><span data-ttu-id="6b995-116"><a href="imn-guideline.md">IMN_GUIDELINE</a></span><span class="sxs-lookup"><span data-stu-id="6b995-116"><a href="imn-guideline.md">IMN_GUIDELINE</a></span></span></dd> 
<dd><span data-ttu-id="6b995-117"><a href="imn-opencandidate.md">IMN_OPENCANDIDATE</a></span><span class="sxs-lookup"><span data-stu-id="6b995-117"><a href="imn-opencandidate.md">IMN_OPENCANDIDATE</a></span></span></dd> 
<dd><span data-ttu-id="6b995-118"><a href="imn-openstatuswindow.md">IMN_OPENSTATUSWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="6b995-118"><a href="imn-openstatuswindow.md">IMN_OPENSTATUSWINDOW</a></span></span></dd> 
<dd><span data-ttu-id="6b995-119"><a href="imn-setcandidatepos.md">IMN_SETCANDIDATEPOS</a></span><span class="sxs-lookup"><span data-stu-id="6b995-119"><a href="imn-setcandidatepos.md">IMN_SETCANDIDATEPOS</a></span></span></dd> 
<dd><span data-ttu-id="6b995-120"><a href="imn-setcompositionfont.md">IMN_SETCOMPOSITIONFONT</a></span><span class="sxs-lookup"><span data-stu-id="6b995-120"><a href="imn-setcompositionfont.md">IMN_SETCOMPOSITIONFONT</a></span></span></dd> 
<dd><span data-ttu-id="6b995-121"><a href="imn-setcompositionwindow.md">IMN_SETCOMPOSITIONWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="6b995-121"><a href="imn-setcompositionwindow.md">IMN_SETCOMPOSITIONWINDOW</a></span></span></dd> 
<dd><span data-ttu-id="6b995-122"><a href="imn-setconversionmode.md">IMN_SETCONVERSIONMODE</a></span><span class="sxs-lookup"><span data-stu-id="6b995-122"><a href="imn-setconversionmode.md">IMN_SETCONVERSIONMODE</a></span></span></dd> 
<dd><span data-ttu-id="6b995-123"><a href="imn-setopenstatus.md">IMN_SETOPENSTATUS</a></span><span class="sxs-lookup"><span data-stu-id="6b995-123"><a href="imn-setopenstatus.md">IMN_SETOPENSTATUS</a></span></span></dd> 
<dd><span data-ttu-id="6b995-124"><a href="imn-setsentencemode.md">IMN_SETSENTENCEMODE</a></span><span class="sxs-lookup"><span data-stu-id="6b995-124"><a href="imn-setsentencemode.md">IMN_SETSENTENCEMODE</a></span></span></dd> 
<dd><span data-ttu-id="6b995-125"><a href="imn-setstatuswindowpos.md">IMN_SETSTATUSWINDOWPOS</a></span><span class="sxs-lookup"><span data-stu-id="6b995-125"><a href="imn-setstatuswindowpos.md">IMN_SETSTATUSWINDOWPOS</a></span></span></dd> 
</dl> 
</dd> 
<dt>

<span data-ttu-id="6b995-126">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6b995-126">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6b995-127">Данные, относящиеся к конкретной команде, с форматом, зависящим от значения параметра *wParam* .</span><span class="sxs-lookup"><span data-stu-id="6b995-127">Command-specific data, with format dependent on the value of the *wParam* parameter.</span></span> <span data-ttu-id="6b995-128">Дополнительные сведения см. в документации по каждой команде.</span><span class="sxs-lookup"><span data-stu-id="6b995-128">For more information, refer to the documentation for each command.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b995-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6b995-129">Return value</span></span>

<span data-ttu-id="6b995-130">Возвращаемое значение зависит от отправленной команды.</span><span class="sxs-lookup"><span data-stu-id="6b995-130">The return value depends on the command sent.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b995-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6b995-131">Remarks</span></span>

<span data-ttu-id="6b995-132">Приложение обрабатывает это сообщение, если оно отвечает за управление окном IME.</span><span class="sxs-lookup"><span data-stu-id="6b995-132">An application processes this message if it is responsible for managing the IME window.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b995-133">Требования</span><span class="sxs-lookup"><span data-stu-id="6b995-133">Requirements</span></span>



| <span data-ttu-id="6b995-134">Требование</span><span class="sxs-lookup"><span data-stu-id="6b995-134">Requirement</span></span> | <span data-ttu-id="6b995-135">Значение</span><span class="sxs-lookup"><span data-stu-id="6b995-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b995-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6b995-136">Minimum supported client</span></span><br/> | <span data-ttu-id="6b995-137">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6b995-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                                                                |
| <span data-ttu-id="6b995-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6b995-138">Minimum supported server</span></span><br/> | <span data-ttu-id="6b995-139">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6b995-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="6b995-140">Заголовок</span><span class="sxs-lookup"><span data-stu-id="6b995-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b995-141"><dt>Winuser. h (включает Windows. h); </dt> <dt>IMM. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6b995-141"><dt>Winuser.h (include Windows.h); </dt> <dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b995-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6b995-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b995-143">Диспетчер метода ввода</span><span class="sxs-lookup"><span data-stu-id="6b995-143">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="6b995-144">Сообщения диспетчера методов ввода</span><span class="sxs-lookup"><span data-stu-id="6b995-144">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> <dt>

[<span data-ttu-id="6b995-145">IMN_CHANGECANDIDATE</span><span class="sxs-lookup"><span data-stu-id="6b995-145">IMN_CHANGECANDIDATE</span></span>](imn-changecandidate.md)
</dt> <dt>

[<span data-ttu-id="6b995-146">IMN_CLOSECANDIDATE</span><span class="sxs-lookup"><span data-stu-id="6b995-146">IMN_CLOSECANDIDATE</span></span>](imn-closecandidate.md)
</dt> <dt>

[<span data-ttu-id="6b995-147">IMN_CLOSESTATUSWINDOW</span><span class="sxs-lookup"><span data-stu-id="6b995-147">IMN_CLOSESTATUSWINDOW</span></span>](imn-closestatuswindow.md)
</dt> <dt>

[<span data-ttu-id="6b995-148">IMN_GUIDELINE</span><span class="sxs-lookup"><span data-stu-id="6b995-148">IMN_GUIDELINE</span></span>](imn-guideline.md)
</dt> <dt>

[<span data-ttu-id="6b995-149">IMN_OPENCANDIDATE</span><span class="sxs-lookup"><span data-stu-id="6b995-149">IMN_OPENCANDIDATE</span></span>](imn-opencandidate.md)
</dt> <dt>

[<span data-ttu-id="6b995-150">IMN_OPENSTATUSWINDOW</span><span class="sxs-lookup"><span data-stu-id="6b995-150">IMN_OPENSTATUSWINDOW</span></span>](imn-openstatuswindow.md)
</dt> <dt>

[<span data-ttu-id="6b995-151">IMN_SETCANDIDATEPOS</span><span class="sxs-lookup"><span data-stu-id="6b995-151">IMN_SETCANDIDATEPOS</span></span>](imn-setcandidatepos.md)
</dt> <dt>

[<span data-ttu-id="6b995-152">IMN_SETCOMPOSITIONFONT</span><span class="sxs-lookup"><span data-stu-id="6b995-152">IMN_SETCOMPOSITIONFONT</span></span>](imn-setcompositionfont.md)
</dt> <dt>

[<span data-ttu-id="6b995-153">IMN_SETCOMPOSITIONWINDOW</span><span class="sxs-lookup"><span data-stu-id="6b995-153">IMN_SETCOMPOSITIONWINDOW</span></span>](imn-setcompositionwindow.md)
</dt> <dt>

[<span data-ttu-id="6b995-154">IMN_SETCONVERSIONMODE</span><span class="sxs-lookup"><span data-stu-id="6b995-154">IMN_SETCONVERSIONMODE</span></span>](imn-setconversionmode.md)
</dt> <dt>

[<span data-ttu-id="6b995-155">IMN_SETOPENSTATUS</span><span class="sxs-lookup"><span data-stu-id="6b995-155">IMN_SETOPENSTATUS</span></span>](imn-setopenstatus.md)
</dt> <dt>

[<span data-ttu-id="6b995-156">IMN_SETSENTENCEMODE</span><span class="sxs-lookup"><span data-stu-id="6b995-156">IMN_SETSENTENCEMODE</span></span>](imn-setsentencemode.md)
</dt> <dt>

[<span data-ttu-id="6b995-157">IMN_SETSTATUSWINDOWPOS</span><span class="sxs-lookup"><span data-stu-id="6b995-157">IMN_SETSTATUSWINDOWPOS</span></span>](imn-setstatuswindowpos.md)
</dt> </dl>

 

 

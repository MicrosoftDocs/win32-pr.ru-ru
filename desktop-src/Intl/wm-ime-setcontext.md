---
description: Отправляется в приложение при активации окна. Окно получает это сообщение через функцию WindowProc.
ms.assetid: ba1e7877-1612-4f2f-aced-0dd982352ad6
title: Сообщение WM_IME_SETCONTEXT (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b36cb1e80127d1a451dabcc457dc364a27878ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263114"
---
# <a name="wm_ime_setcontext-message"></a><span data-ttu-id="b2c1e-104">\_Сообщение SETCONTEXT редактора IME WM \_</span><span class="sxs-lookup"><span data-stu-id="b2c1e-104">WM\_IME\_SETCONTEXT message</span></span>

<span data-ttu-id="b2c1e-105">Отправляется в приложение при активации окна.</span><span class="sxs-lookup"><span data-stu-id="b2c1e-105">Sent to an application when a window is activated.</span></span> <span data-ttu-id="b2c1e-106">Окно получает это сообщение через функцию [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b2c1e-106">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,  
  WM_IME_SETCONTEXT,  
  WPARAM wParam,      
  LPARAM lParam      
);
```



## <a name="parameters"></a><span data-ttu-id="b2c1e-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="b2c1e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2c1e-108">*HWND*</span><span class="sxs-lookup"><span data-stu-id="b2c1e-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="b2c1e-109">Маркер для окна.</span><span class="sxs-lookup"><span data-stu-id="b2c1e-109">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="b2c1e-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b2c1e-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b2c1e-111">**Значение true** , если окно активно, и **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="b2c1e-111">**TRUE** if the window is active, and **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="b2c1e-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b2c1e-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b2c1e-113">Параметры отображения.</span><span class="sxs-lookup"><span data-stu-id="b2c1e-113">Display options.</span></span> <span data-ttu-id="b2c1e-114">Этот параметр может иметь одно или несколько из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="b2c1e-114">This parameter can have one or more of the following values.</span></span>



| <span data-ttu-id="b2c1e-115">Значение</span><span class="sxs-lookup"><span data-stu-id="b2c1e-115">Value</span></span>                                                                                                                                                                                                   | <span data-ttu-id="b2c1e-116">Значение</span><span class="sxs-lookup"><span data-stu-id="b2c1e-116">Meaning</span></span>                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="ISC_SHOWUICOMPOSITIONWINDOW"></span><span id="isc_showuicompositionwindow"></span><dl> <span data-ttu-id="b2c1e-117"><dt>**ISC \_ шовуикомпоситионвиндов**</dt></span><span class="sxs-lookup"><span data-stu-id="b2c1e-117"><dt>**ISC\_SHOWUICOMPOSITIONWINDOW**</dt></span></span> </dl> | <span data-ttu-id="b2c1e-118">Отображение окна "композиция" по пользовательскому интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="b2c1e-118">Show the composition window by user interface window.</span></span><br/>          |
| <span id="ISC_SHOWUIGUIDWINDOW"></span><span id="isc_showuiguidwindow"></span><dl> <span data-ttu-id="b2c1e-119"><dt>**ISC \_ шовуигуидвиндов**</dt></span><span class="sxs-lookup"><span data-stu-id="b2c1e-119"><dt>**ISC\_SHOWUIGUIDWINDOW**</dt></span></span> </dl>                      | <span data-ttu-id="b2c1e-120">Отображение окна "Guide" по пользовательскому интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="b2c1e-120">Show the guide window by user interface window.</span></span><br/>                |
| <span id="ISC_SHOWUISOFTKBD"></span><span id="isc_showuisoftkbd"></span><dl> <span data-ttu-id="b2c1e-121"><dt>**ISC \_ шовуисофткбд**</dt></span><span class="sxs-lookup"><span data-stu-id="b2c1e-121"><dt>**ISC\_SHOWUISOFTKBD**</dt></span></span> </dl>                               | <span data-ttu-id="b2c1e-122">Отображение экранной клавиатуры в окне пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="b2c1e-122">Show the soft keyboard by user interface window.</span></span><br/>               |
| <span id="ISC_SHOWUICANDIDATEWINDOW"></span><span id="isc_showuicandidatewindow"></span><dl> <span data-ttu-id="b2c1e-123"><dt>**ISC \_ шовуикандидатевиндов**</dt></span><span class="sxs-lookup"><span data-stu-id="b2c1e-123"><dt>**ISC\_SHOWUICANDIDATEWINDOW**</dt></span></span> </dl>       | <span data-ttu-id="b2c1e-124">Отображение окна кандидатов с индексом 0 в окне пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="b2c1e-124">Show the candidate window of index 0 by user interface window.</span></span><br/> |
| <dl> <span data-ttu-id="b2c1e-125"><dt>ISC \_ шовуикандидатевиндов << 1</dt></span><span class="sxs-lookup"><span data-stu-id="b2c1e-125"><dt>ISC\_SHOWUICANDIDATEWINDOW << 1</dt></span></span> </dl>                                                                                        | <span data-ttu-id="b2c1e-126">Отображение окна кандидатов с индексом 1 в окне пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="b2c1e-126">Show the candidate window of index 1 by user interface window.</span></span><br/> |
| <dl> <span data-ttu-id="b2c1e-127"><dt>ISC \_ шовуикандидатевиндов << 2</dt></span><span class="sxs-lookup"><span data-stu-id="b2c1e-127"><dt>ISC\_SHOWUICANDIDATEWINDOW << 2</dt></span></span> </dl>                                                                                        | <span data-ttu-id="b2c1e-128">Отображение окна кандидатов с индексом 2 в окне пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="b2c1e-128">Show the candidate window of index 2 by user interface window.</span></span><br/> |
| <dl> <span data-ttu-id="b2c1e-129"><dt>ISC \_ шовуикандидатевиндов << 3</dt></span><span class="sxs-lookup"><span data-stu-id="b2c1e-129"><dt>ISC\_SHOWUICANDIDATEWINDOW << 3</dt></span></span> </dl>                                                                                        | <span data-ttu-id="b2c1e-130">Отображение окна кандидатов с индексом 3 в окне пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="b2c1e-130">Show the candidate window of index 3 by user interface window.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2c1e-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b2c1e-131">Return value</span></span>

<span data-ttu-id="b2c1e-132">Возвращает значение, возвращаемое [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) или [**иммисуимессаже**](/windows/desktop/api/Imm/nf-imm-immisuimessagea).</span><span class="sxs-lookup"><span data-stu-id="b2c1e-132">Returns the value returned by [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) or [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea).</span></span>

## <a name="remarks"></a><span data-ttu-id="b2c1e-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b2c1e-133">Remarks</span></span>

<span data-ttu-id="b2c1e-134">Если приложение создало окно IME, оно должно вызывать [**иммисуимессаже**](/windows/desktop/api/Imm/nf-imm-immisuimessagea).</span><span class="sxs-lookup"><span data-stu-id="b2c1e-134">If the application has created an IME window, it should call [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea).</span></span> <span data-ttu-id="b2c1e-135">В противном случае оно должно передать это сообщение в [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="b2c1e-135">Otherwise, it should pass this message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span>

<span data-ttu-id="b2c1e-136">Если приложение рисует окно композиции, то окно IME по умолчанию не обязательно отображает окно его композиции.</span><span class="sxs-lookup"><span data-stu-id="b2c1e-136">If the application draws the composition window, the default IME window does not have to show its composition window.</span></span> <span data-ttu-id="b2c1e-137">В этом случае приложение должно очистить значение **ISC \_ шовуикомпоситионвиндов** из параметра *lParam* перед передачей сообщения в [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) или [**иммисуимессаже**](/windows/desktop/api/Imm/nf-imm-immisuimessagea).</span><span class="sxs-lookup"><span data-stu-id="b2c1e-137">In this case, the application must clear the **ISC\_SHOWUICOMPOSITIONWINDOW** value from the *lParam* parameter before passing the message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) or [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea).</span></span> <span data-ttu-id="b2c1e-138">Чтобы отобразить определенное окно пользовательского интерфейса, приложение должно удалить соответствующее значение, чтобы редактор IME не отображал его.</span><span class="sxs-lookup"><span data-stu-id="b2c1e-138">To display a certain user interface window, an application should remove the corresponding value so that the IME will not display it.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2c1e-139">Требования</span><span class="sxs-lookup"><span data-stu-id="b2c1e-139">Requirements</span></span>



| <span data-ttu-id="b2c1e-140">Требование</span><span class="sxs-lookup"><span data-stu-id="b2c1e-140">Requirement</span></span> | <span data-ttu-id="b2c1e-141">Значение</span><span class="sxs-lookup"><span data-stu-id="b2c1e-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2c1e-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b2c1e-142">Minimum supported client</span></span><br/> | <span data-ttu-id="b2c1e-143">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b2c1e-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                                                                |
| <span data-ttu-id="b2c1e-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b2c1e-144">Minimum supported server</span></span><br/> | <span data-ttu-id="b2c1e-145">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b2c1e-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="b2c1e-146">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b2c1e-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2c1e-147"><dt>Winuser. h (включает Windows. h); </dt> <dt>IMM. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b2c1e-147"><dt>Winuser.h (include Windows.h); </dt> <dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2c1e-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b2c1e-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2c1e-149">Диспетчер метода ввода</span><span class="sxs-lookup"><span data-stu-id="b2c1e-149">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="b2c1e-150">Сообщения диспетчера методов ввода</span><span class="sxs-lookup"><span data-stu-id="b2c1e-150">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> <dt>

[<span data-ttu-id="b2c1e-151">**иммисуимессаже**</span><span class="sxs-lookup"><span data-stu-id="b2c1e-151">**ImmIsUIMessage**</span></span>](/windows/desktop/api/Imm/nf-imm-immisuimessagea)
</dt> </dl>

 

 

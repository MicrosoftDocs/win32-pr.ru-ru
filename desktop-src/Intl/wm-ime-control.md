---
description: Отправляется приложением для направления окна IME для выполнения запрошенной команды.
ms.assetid: 5d3b7f8a-57c9-41e3-8022-9a3f515fc32e
title: Сообщение WM_IME_CONTROL (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd0adc534883bc0b31984c8d3e9b57a04b555987
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897418"
---
# <a name="wm_ime_control-message"></a><span data-ttu-id="4ad30-103">Сообщение WM_IME_CONTROL</span><span class="sxs-lookup"><span data-stu-id="4ad30-103">WM_IME_CONTROL message</span></span>

<span data-ttu-id="4ad30-104">Отправляется приложением для направления окна IME для выполнения запрошенной команды.</span><span class="sxs-lookup"><span data-stu-id="4ad30-104">Sent by an application to direct the IME window to carry out the requested command.</span></span> <span data-ttu-id="4ad30-105">Приложение использует это сообщение для управления созданным окном IME.</span><span class="sxs-lookup"><span data-stu-id="4ad30-105">The application uses this message to control the IME window that it has created.</span></span> <span data-ttu-id="4ad30-106">Чтобы отправить это сообщение, приложение вызывает функцию [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="4ad30-106">To send this message, the application calls the [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) function with the following parameters.</span></span>


```C++
SendMessage(
  HWND   hwnd,
  WM_IME_CONTROL, 
  WPARAM wParam,
  LPARAM lParam             
);
```



## <a name="parameters"></a><span data-ttu-id="4ad30-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="4ad30-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ad30-108">*HWND*</span><span class="sxs-lookup"><span data-stu-id="4ad30-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="4ad30-109">Обработчик для окна.</span><span class="sxs-lookup"><span data-stu-id="4ad30-109">Handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="4ad30-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4ad30-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4ad30-111">Команда.</span><span class="sxs-lookup"><span data-stu-id="4ad30-111">The command.</span></span> <span data-ttu-id="4ad30-112">Этот параметр может принимать одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="4ad30-112">This parameter can have one of the following values:</span></span>

<dl>
<dd><span data-ttu-id="4ad30-113"><a href="imc-closestatuswindow.md">IMC_CLOSESTATUSWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="4ad30-113"><a href="imc-closestatuswindow.md">IMC_CLOSESTATUSWINDOW</a></span></span></dd> 
<dd><span data-ttu-id="4ad30-114"><a href="imc-getcandidatepos.md">IMC_GETCANDIDATEPOS</a></span><span class="sxs-lookup"><span data-stu-id="4ad30-114"><a href="imc-getcandidatepos.md">IMC_GETCANDIDATEPOS</a></span></span></dd> 
<dd><span data-ttu-id="4ad30-115"><a href="imc-getcompositionfont.md">IMC_GETCOMPOSITIONFONT</a></span><span class="sxs-lookup"><span data-stu-id="4ad30-115"><a href="imc-getcompositionfont.md">IMC_GETCOMPOSITIONFONT</a></span></span></dd> 
<dd><span data-ttu-id="4ad30-116"><a href="imc-getcompositionwindow.md">IMC_GETCOMPOSITIONWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="4ad30-116"><a href="imc-getcompositionwindow.md">IMC_GETCOMPOSITIONWINDOW</a></span></span></dd> 
<dd><span data-ttu-id="4ad30-117"><a href="imc-getstatuswindowpos.md">IMC_GETSTATUSWINDOWPOS</a></span><span class="sxs-lookup"><span data-stu-id="4ad30-117"><a href="imc-getstatuswindowpos.md">IMC_GETSTATUSWINDOWPOS</a></span></span></dd> 
<dd><span data-ttu-id="4ad30-118"><a href="imc-openstatuswindow.md">IMC_OPENSTATUSWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="4ad30-118"><a href="imc-openstatuswindow.md">IMC_OPENSTATUSWINDOW</a></span></span></dd> 
<dd><span data-ttu-id="4ad30-119"><a href="imc-setcandidatepos.md">IMC_SETCANDIDATEPOS</a></span><span class="sxs-lookup"><span data-stu-id="4ad30-119"><a href="imc-setcandidatepos.md">IMC_SETCANDIDATEPOS</a></span></span></dd> 
<dd><span data-ttu-id="4ad30-120"><a href="imc-setcompositionfont.md">IMC_SETCOMPOSITIONFONT</a>></span><span class="sxs-lookup"><span data-stu-id="4ad30-120"><a href="imc-setcompositionfont.md">IMC_SETCOMPOSITIONFONT</a>></span></span></dd> 
<dd><span data-ttu-id="4ad30-121"><a href="imc-setcompositionwindow.md">IMC_SETCOMPOSITIONWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="4ad30-121"><a href="imc-setcompositionwindow.md">IMC_SETCOMPOSITIONWINDOW</a></span></span></dd> 
<dd><span data-ttu-id="4ad30-122"><a href="imc-setstatuswindowpos.md">IMC_SETSTATUSWINDOWPOS</a></span><span class="sxs-lookup"><span data-stu-id="4ad30-122"><a href="imc-setstatuswindowpos.md">IMC_SETSTATUSWINDOWPOS</a></span></span></dd> 
</dl>
</dd>

<dt>

<span data-ttu-id="4ad30-123">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4ad30-123">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4ad30-124">Данные, относящиеся к конкретной команде, с форматом, зависящим от значения параметра *wParam* .</span><span class="sxs-lookup"><span data-stu-id="4ad30-124">Command-specific data, with format dependent on the value of the *wParam* parameter.</span></span> <span data-ttu-id="4ad30-125">Дополнительные сведения см. в документации по каждой команде.</span><span class="sxs-lookup"><span data-stu-id="4ad30-125">For more information, refer to the documentation for each command.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ad30-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4ad30-126">Return value</span></span>

<span data-ttu-id="4ad30-127">Сообщение возвращает значение, зависящее от команды.</span><span class="sxs-lookup"><span data-stu-id="4ad30-127">The message returns a command-specific value.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ad30-128">Требования</span><span class="sxs-lookup"><span data-stu-id="4ad30-128">Requirements</span></span>



| <span data-ttu-id="4ad30-129">Требование</span><span class="sxs-lookup"><span data-stu-id="4ad30-129">Requirement</span></span> | <span data-ttu-id="4ad30-130">Значение</span><span class="sxs-lookup"><span data-stu-id="4ad30-130">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ad30-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4ad30-131">Minimum supported client</span></span><br/> | <span data-ttu-id="4ad30-132">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4ad30-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                                                                |
| <span data-ttu-id="4ad30-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4ad30-133">Minimum supported server</span></span><br/> | <span data-ttu-id="4ad30-134">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4ad30-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="4ad30-135">Заголовок</span><span class="sxs-lookup"><span data-stu-id="4ad30-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ad30-136"><dt>Winuser. h (включает Windows. h); </dt> <dt>IMM. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4ad30-136"><dt>Winuser.h (include Windows.h); </dt> <dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ad30-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4ad30-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ad30-138">Диспетчер метода ввода</span><span class="sxs-lookup"><span data-stu-id="4ad30-138">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="4ad30-139">Сообщения диспетчера методов ввода</span><span class="sxs-lookup"><span data-stu-id="4ad30-139">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> <dt>

[<span data-ttu-id="4ad30-140">IMC_CLOSESTATUSWINDOW</span><span class="sxs-lookup"><span data-stu-id="4ad30-140">IMC_CLOSESTATUSWINDOW</span></span>](imc-closestatuswindow.md)
</dt> <dt>

[<span data-ttu-id="4ad30-141">IMC_GETCANDIDATEPOS</span><span class="sxs-lookup"><span data-stu-id="4ad30-141">IMC_GETCANDIDATEPOS</span></span>](imc-getcandidatepos.md)
</dt> <dt>

[<span data-ttu-id="4ad30-142">IMC_GETCOMPOSITIONFONT</span><span class="sxs-lookup"><span data-stu-id="4ad30-142">IMC_GETCOMPOSITIONFONT</span></span>](imc-getcompositionfont.md)
</dt> <dt>

[<span data-ttu-id="4ad30-143">IMC_GETCOMPOSITIONWINDOW</span><span class="sxs-lookup"><span data-stu-id="4ad30-143">IMC_GETCOMPOSITIONWINDOW</span></span>](imc-getcompositionwindow.md)
</dt> <dt>

[<span data-ttu-id="4ad30-144">IMC_GETSTATUSWINDOWPOS</span><span class="sxs-lookup"><span data-stu-id="4ad30-144">IMC_GETSTATUSWINDOWPOS</span></span>](imc-getstatuswindowpos.md)
</dt> <dt>

[<span data-ttu-id="4ad30-145">IMC_OPENSTATUSWINDOW</span><span class="sxs-lookup"><span data-stu-id="4ad30-145">IMC_OPENSTATUSWINDOW</span></span>](imc-openstatuswindow.md)
</dt> <dt>

[<span data-ttu-id="4ad30-146">IMC_SETCANDIDATEPOS</span><span class="sxs-lookup"><span data-stu-id="4ad30-146">IMC_SETCANDIDATEPOS</span></span>](imc-setcandidatepos.md)
</dt> <dt>

[<span data-ttu-id="4ad30-147">IMC_SETCOMPOSITIONFONT</span><span class="sxs-lookup"><span data-stu-id="4ad30-147">IMC_SETCOMPOSITIONFONT</span></span>](imc-setcompositionfont.md)
</dt> <dt>

[<span data-ttu-id="4ad30-148">IMC_SETCOMPOSITIONWINDOW</span><span class="sxs-lookup"><span data-stu-id="4ad30-148">IMC_SETCOMPOSITIONWINDOW</span></span>](imc-setcompositionwindow.md)
</dt> <dt>

[<span data-ttu-id="4ad30-149">IMC_SETSTATUSWINDOWPOS</span><span class="sxs-lookup"><span data-stu-id="4ad30-149">IMC_SETSTATUSWINDOWPOS</span></span>](imc-setstatuswindowpos.md)
</dt> </dl>

 

 

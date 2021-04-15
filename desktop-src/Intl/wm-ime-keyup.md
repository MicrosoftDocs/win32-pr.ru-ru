---
description: Отправляется в приложение редактором IME для уведомления приложения о выпуске ключа и для сохранения порядка сообщений. Окно получает это сообщение через функцию WindowProc.
ms.assetid: 652f951f-4e9f-407c-844c-b250b6a9e6f5
title: Сообщение WM_IME_KEYUP (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e0eb6c6701510a373573ff6d85d5b50a8541b4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682726"
---
# <a name="wm_ime_keyup-message"></a><span data-ttu-id="22a85-104">\_ \_ Сообщение KEYUP IME</span><span class="sxs-lookup"><span data-stu-id="22a85-104">WM\_IME\_KEYUP message</span></span>

<span data-ttu-id="22a85-105">Отправляется в приложение редактором IME для уведомления приложения о выпуске ключа и для сохранения порядка сообщений.</span><span class="sxs-lookup"><span data-stu-id="22a85-105">Sent to an application by the IME to notify the application of a key release and to keep message order.</span></span> <span data-ttu-id="22a85-106">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="22a85-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,       
  WM_IME_KEYUP,    
  WPARAM wParam,   
  LPARAM lParam    
);
```



## <a name="parameters"></a><span data-ttu-id="22a85-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="22a85-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22a85-108">*HWND*</span><span class="sxs-lookup"><span data-stu-id="22a85-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="22a85-109">Маркер для окна.</span><span class="sxs-lookup"><span data-stu-id="22a85-109">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="22a85-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="22a85-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="22a85-111">Код виртуального ключа для ключа.</span><span class="sxs-lookup"><span data-stu-id="22a85-111">Virtual key code of the key.</span></span>

</dd> <dt>

<span data-ttu-id="22a85-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="22a85-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="22a85-113">Число повторов, код сканирования, флаг расширенного ключа, код контекста, флаг предыдущего состояния ключа и флаг состояния перехода, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="22a85-113">Repeat count, scan code, extended key flag, context code, previous key state flag, and transition state flag, as shown below.</span></span>



| <span data-ttu-id="22a85-114">bit</span><span class="sxs-lookup"><span data-stu-id="22a85-114">Bit</span></span>   | <span data-ttu-id="22a85-115">Значение</span><span class="sxs-lookup"><span data-stu-id="22a85-115">Meaning</span></span>                                                                     |
|-------|-----------------------------------------------------------------------------|
| <span data-ttu-id="22a85-116">0—15</span><span class="sxs-lookup"><span data-stu-id="22a85-116">0-15</span></span>  | <span data-ttu-id="22a85-117">Число повторов.</span><span class="sxs-lookup"><span data-stu-id="22a85-117">Repeat count.</span></span> <span data-ttu-id="22a85-118">Это значение всегда равно 1.</span><span class="sxs-lookup"><span data-stu-id="22a85-118">This value is always 1.</span></span>                                       |
| <span data-ttu-id="22a85-119">16—23</span><span class="sxs-lookup"><span data-stu-id="22a85-119">16-23</span></span> | <span data-ttu-id="22a85-120">Код сканирования.</span><span class="sxs-lookup"><span data-stu-id="22a85-120">Scan code.</span></span>                                                                  |
| <span data-ttu-id="22a85-121">24</span><span class="sxs-lookup"><span data-stu-id="22a85-121">24</span></span>    | <span data-ttu-id="22a85-122">Расширенный ключ.</span><span class="sxs-lookup"><span data-stu-id="22a85-122">Extended key.</span></span> <span data-ttu-id="22a85-123">Это значение равно 1, если это расширенный ключ.</span><span class="sxs-lookup"><span data-stu-id="22a85-123">This value is 1 if it is an extended key.</span></span> <span data-ttu-id="22a85-124">В противном случае — 0.</span><span class="sxs-lookup"><span data-stu-id="22a85-124">Otherwise, it is 0.</span></span> |
| <span data-ttu-id="22a85-125">25-28</span><span class="sxs-lookup"><span data-stu-id="22a85-125">25-28</span></span> | <span data-ttu-id="22a85-126">Не используется.</span><span class="sxs-lookup"><span data-stu-id="22a85-126">Not used.</span></span>                                                                   |
| <span data-ttu-id="22a85-127">29</span><span class="sxs-lookup"><span data-stu-id="22a85-127">29</span></span>    | <span data-ttu-id="22a85-128">Код контекста.</span><span class="sxs-lookup"><span data-stu-id="22a85-128">Context code.</span></span> <span data-ttu-id="22a85-129">Это значение всегда равно 0.</span><span class="sxs-lookup"><span data-stu-id="22a85-129">This value is always 0.</span></span>                                       |
| <span data-ttu-id="22a85-130">30</span><span class="sxs-lookup"><span data-stu-id="22a85-130">30</span></span>    | <span data-ttu-id="22a85-131">Предыдущее состояние ключа.</span><span class="sxs-lookup"><span data-stu-id="22a85-131">Previous key state.</span></span> <span data-ttu-id="22a85-132">Это значение всегда равно 1.</span><span class="sxs-lookup"><span data-stu-id="22a85-132">This value is always 1.</span></span>                                 |
| <span data-ttu-id="22a85-133">31</span><span class="sxs-lookup"><span data-stu-id="22a85-133">31</span></span>    | <span data-ttu-id="22a85-134">Переходное состояние.</span><span class="sxs-lookup"><span data-stu-id="22a85-134">Transition state.</span></span> <span data-ttu-id="22a85-135">Это значение всегда равно 1.</span><span class="sxs-lookup"><span data-stu-id="22a85-135">This value is always 1.</span></span>                                   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22a85-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="22a85-136">Return value</span></span>

<span data-ttu-id="22a85-137">Приложение должно вернуть значение 0, если оно обрабатывает это сообщение.</span><span class="sxs-lookup"><span data-stu-id="22a85-137">An application should return 0 if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="22a85-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="22a85-138">Remarks</span></span>

<span data-ttu-id="22a85-139">Приложение может обработать это сообщение или передать его функции [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  для создания соответствующего сообщения [**WM \_ KEYUP**](../inputdev/wm-keyup.md) .</span><span class="sxs-lookup"><span data-stu-id="22a85-139">An application can process this message or pass it to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  function to generate a matching [**WM\_KEYUP**](../inputdev/wm-keyup.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="22a85-140">Требования</span><span class="sxs-lookup"><span data-stu-id="22a85-140">Requirements</span></span>



| <span data-ttu-id="22a85-141">Требование</span><span class="sxs-lookup"><span data-stu-id="22a85-141">Requirement</span></span> | <span data-ttu-id="22a85-142">Значение</span><span class="sxs-lookup"><span data-stu-id="22a85-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22a85-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="22a85-143">Minimum supported client</span></span><br/> | <span data-ttu-id="22a85-144">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="22a85-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="22a85-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="22a85-145">Minimum supported server</span></span><br/> | <span data-ttu-id="22a85-146">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="22a85-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="22a85-147">Заголовок</span><span class="sxs-lookup"><span data-stu-id="22a85-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="22a85-148"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="22a85-148"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22a85-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="22a85-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22a85-150">Диспетчер метода ввода</span><span class="sxs-lookup"><span data-stu-id="22a85-150">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="22a85-151">Сообщения диспетчера методов ввода</span><span class="sxs-lookup"><span data-stu-id="22a85-151">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> </dl>

 

 

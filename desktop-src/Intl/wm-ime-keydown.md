---
description: Отправляется в приложение редактором IME для уведомления приложения о нажатии клавиши и для сохранения порядка сообщений. Окно получает это сообщение через функцию WindowProc.
ms.assetid: db7075fb-b3d4-4d32-a0db-096d17d67c72
title: Сообщение WM_IME_KEYDOWN (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3089af3c839f70e7f55895ae13158e7b2240605
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263116"
---
# <a name="wm_ime_keydown-message"></a><span data-ttu-id="a4c92-104">\_Сообщение KeyDown редактора IME WM \_</span><span class="sxs-lookup"><span data-stu-id="a4c92-104">WM\_IME\_KEYDOWN message</span></span>

<span data-ttu-id="a4c92-105">Отправляется в приложение редактором IME для уведомления приложения о нажатии клавиши и для сохранения порядка сообщений.</span><span class="sxs-lookup"><span data-stu-id="a4c92-105">Sent to an application by the IME to notify the application of a key press and to keep message order.</span></span> <span data-ttu-id="a4c92-106">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="a4c92-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,        
  WM_IME_KEYDOWN,  
  WPARAM wParam, 
  LPARAM lParam      
);
```



## <a name="parameters"></a><span data-ttu-id="a4c92-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="a4c92-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4c92-108">*HWND*</span><span class="sxs-lookup"><span data-stu-id="a4c92-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="a4c92-109">Маркер для окна.</span><span class="sxs-lookup"><span data-stu-id="a4c92-109">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="a4c92-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a4c92-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a4c92-111">Код виртуального ключа для ключа.</span><span class="sxs-lookup"><span data-stu-id="a4c92-111">Virtual key code of the key.</span></span>

</dd> <dt>

<span data-ttu-id="a4c92-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a4c92-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a4c92-113">Число повторов, код сканирования, флаг расширенного ключа, код контекста, предыдущий флаг состояния ключа и флаг состояния перехода, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="a4c92-113">Repeat count, scan code, extended key flag, context code, previous key state flag, and transition state flag, as shown in the following table.</span></span>



| <span data-ttu-id="a4c92-114">bit</span><span class="sxs-lookup"><span data-stu-id="a4c92-114">Bit</span></span>   | <span data-ttu-id="a4c92-115">Значение</span><span class="sxs-lookup"><span data-stu-id="a4c92-115">Meaning</span></span>                                                                     |
|-------|-----------------------------------------------------------------------------|
| <span data-ttu-id="a4c92-116">0—15</span><span class="sxs-lookup"><span data-stu-id="a4c92-116">0-15</span></span>  | <span data-ttu-id="a4c92-117">Число повторов.</span><span class="sxs-lookup"><span data-stu-id="a4c92-117">Repeat count.</span></span>                                                               |
| <span data-ttu-id="a4c92-118">16—23</span><span class="sxs-lookup"><span data-stu-id="a4c92-118">16-23</span></span> | <span data-ttu-id="a4c92-119">Код сканирования.</span><span class="sxs-lookup"><span data-stu-id="a4c92-119">Scan code.</span></span>                                                                  |
| <span data-ttu-id="a4c92-120">24</span><span class="sxs-lookup"><span data-stu-id="a4c92-120">24</span></span>    | <span data-ttu-id="a4c92-121">Расширенный ключ.</span><span class="sxs-lookup"><span data-stu-id="a4c92-121">Extended key.</span></span> <span data-ttu-id="a4c92-122">Это значение равно 1, если это расширенный ключ.</span><span class="sxs-lookup"><span data-stu-id="a4c92-122">This value is 1 if it is an extended key.</span></span> <span data-ttu-id="a4c92-123">В противном случае — 0.</span><span class="sxs-lookup"><span data-stu-id="a4c92-123">Otherwise, it is 0.</span></span> |
| <span data-ttu-id="a4c92-124">25-28</span><span class="sxs-lookup"><span data-stu-id="a4c92-124">25-28</span></span> | <span data-ttu-id="a4c92-125">Не используется.</span><span class="sxs-lookup"><span data-stu-id="a4c92-125">Not used.</span></span>                                                                   |
| <span data-ttu-id="a4c92-126">29</span><span class="sxs-lookup"><span data-stu-id="a4c92-126">29</span></span>    | <span data-ttu-id="a4c92-127">Код контекста.</span><span class="sxs-lookup"><span data-stu-id="a4c92-127">Context code.</span></span> <span data-ttu-id="a4c92-128">Это значение всегда равно 0.</span><span class="sxs-lookup"><span data-stu-id="a4c92-128">This value is always 0.</span></span>                                       |
| <span data-ttu-id="a4c92-129">30</span><span class="sxs-lookup"><span data-stu-id="a4c92-129">30</span></span>    | <span data-ttu-id="a4c92-130">Предыдущее состояние ключа.</span><span class="sxs-lookup"><span data-stu-id="a4c92-130">Previous key state.</span></span> <span data-ttu-id="a4c92-131">Это значение равно 1, если ключ не работает, или 0, если он работает.</span><span class="sxs-lookup"><span data-stu-id="a4c92-131">This value is 1 if the key is down or 0 if it is up.</span></span>    |
| <span data-ttu-id="a4c92-132">31</span><span class="sxs-lookup"><span data-stu-id="a4c92-132">31</span></span>    | <span data-ttu-id="a4c92-133">Переходное состояние.</span><span class="sxs-lookup"><span data-stu-id="a4c92-133">Transition state.</span></span> <span data-ttu-id="a4c92-134">Это значение всегда равно 0.</span><span class="sxs-lookup"><span data-stu-id="a4c92-134">This value is always 0.</span></span>                                   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4c92-135">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a4c92-135">Return value</span></span>

<span data-ttu-id="a4c92-136">Приложение должно вернуть значение 0, если оно обрабатывает это сообщение.</span><span class="sxs-lookup"><span data-stu-id="a4c92-136">An application should return 0 if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4c92-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a4c92-137">Remarks</span></span>

<span data-ttu-id="a4c92-138">Приложение может обработать это сообщение или передать его функции [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  для создания соответствующего сообщения [**WM \_ KeyDown**](../inputdev/wm-keydown.md) .</span><span class="sxs-lookup"><span data-stu-id="a4c92-138">An application can process this message or pass it to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  function to generate a matching [**WM\_KEYDOWN**](../inputdev/wm-keydown.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4c92-139">Требования</span><span class="sxs-lookup"><span data-stu-id="a4c92-139">Requirements</span></span>



| <span data-ttu-id="a4c92-140">Требование</span><span class="sxs-lookup"><span data-stu-id="a4c92-140">Requirement</span></span> | <span data-ttu-id="a4c92-141">Значение</span><span class="sxs-lookup"><span data-stu-id="a4c92-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4c92-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a4c92-142">Minimum supported client</span></span><br/> | <span data-ttu-id="a4c92-143">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a4c92-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a4c92-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a4c92-144">Minimum supported server</span></span><br/> | <span data-ttu-id="a4c92-145">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a4c92-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a4c92-146">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a4c92-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4c92-147"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a4c92-147"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4c92-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a4c92-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4c92-149">Диспетчер метода ввода</span><span class="sxs-lookup"><span data-stu-id="a4c92-149">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="a4c92-150">Сообщения диспетчера методов ввода</span><span class="sxs-lookup"><span data-stu-id="a4c92-150">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> </dl>

 

 

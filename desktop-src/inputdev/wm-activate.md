---
title: Сообщение WM_ACTIVATE (Winuser. h)
description: Посылается как активируемое окно, так и деактивируемое окно.
ms.assetid: a62bb9f7-f286-4d0d-a1ca-370950c188b2
keywords:
- WM_ACTIVATE ввода сообщений с клавиатуры и мыши
topic_type:
- apiref
api_name:
- WM_ACTIVATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec28662aa2219ee9b3ad2e8cc8efac861d292f6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135642"
---
# <a name="wm_activate-message"></a><span data-ttu-id="128ca-104">\_Сообщение активации WM</span><span class="sxs-lookup"><span data-stu-id="128ca-104">WM\_ACTIVATE message</span></span>

<span data-ttu-id="128ca-105">Посылается как активируемое окно, так и деактивируемое окно.</span><span class="sxs-lookup"><span data-stu-id="128ca-105">Sent to both the window being activated and the window being deactivated.</span></span> <span data-ttu-id="128ca-106">Если в Windows используется одна и та же очередь ввода, сообщение отправляется синхронно, сначала в процедуру окна верхнего уровня, которая деактивируется, а затем в оконную процедуру активируемого окна верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="128ca-106">If the windows use the same input queue, the message is sent synchronously, first to the window procedure of the top-level window being deactivated, then to the window procedure of the top-level window being activated.</span></span> <span data-ttu-id="128ca-107">Если в Windows используются различные входные очереди, сообщение отправляется асинхронно, поэтому окно активируется немедленно.</span><span class="sxs-lookup"><span data-stu-id="128ca-107">If the windows use different input queues, the message is sent asynchronously, so the window is activated immediately.</span></span>


```C++
#define WM_ACTIVATE                     0x0006
```



## <a name="parameters"></a><span data-ttu-id="128ca-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="128ca-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="128ca-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="128ca-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="128ca-110">Слово нижнего порядка указывает, активируется ли окно или деактивируется.</span><span class="sxs-lookup"><span data-stu-id="128ca-110">The low-order word specifies whether the window is being activated or deactivated.</span></span> <span data-ttu-id="128ca-111">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="128ca-111">This parameter can be one of the following values.</span></span> <span data-ttu-id="128ca-112">Слово в высоком порядке указывает на состояние окна, которое активируется или деактивируется.</span><span class="sxs-lookup"><span data-stu-id="128ca-112">The high-order word specifies the minimized state of the window being activated or deactivated.</span></span> <span data-ttu-id="128ca-113">Ненулевое значение указывает, что окно является минимальным.</span><span class="sxs-lookup"><span data-stu-id="128ca-113">A nonzero value indicates the window is minimized.</span></span>



| <span data-ttu-id="128ca-114">Значение</span><span class="sxs-lookup"><span data-stu-id="128ca-114">Value</span></span>                                                                                                                                                                                                                   | <span data-ttu-id="128ca-115">Значение</span><span class="sxs-lookup"><span data-stu-id="128ca-115">Meaning</span></span>                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WA_ACTIVE"></span><span id="wa_active"></span><dl> <span data-ttu-id="128ca-116"><dt>**WA \_ Активный**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="128ca-116"><dt>**WA\_ACTIVE**</dt> <dt>1</dt></span></span> </dl>                | <span data-ttu-id="128ca-117">Активируется каким-либо методом, отличным от щелчка мышью (например, путем вызова функции [**сетактивевиндов**](/windows/win32/api/winuser/nf-winuser-setactivewindow) или с помощью интерфейса клавиатуры для выбора окна).</span><span class="sxs-lookup"><span data-stu-id="128ca-117">Activated by some method other than a mouse click (for example, by a call to the [**SetActiveWindow**](/windows/win32/api/winuser/nf-winuser-setactivewindow) function or by use of the keyboard interface to select the window).</span></span><br/> |
| <span id="WA_CLICKACTIVE"></span><span id="wa_clickactive"></span><dl> <span data-ttu-id="128ca-118"><dt>**WA \_ КЛИККАКТИВЕ**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="128ca-118"><dt>**WA\_CLICKACTIVE**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="128ca-119">Активируется щелчком мыши.</span><span class="sxs-lookup"><span data-stu-id="128ca-119">Activated by a mouse click.</span></span><br/>                                                                                                                                                                     |
| <span id="WA_INACTIVE"></span><span id="wa_inactive"></span><dl> <span data-ttu-id="128ca-120"><dt>**WA \_ Неактивный**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="128ca-120"><dt>**WA\_INACTIVE**</dt> <dt>0</dt></span></span> </dl>          | <span data-ttu-id="128ca-121">Деактивирован.</span><span class="sxs-lookup"><span data-stu-id="128ca-121">Deactivated.</span></span><br/>                                                                                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="128ca-122">*lParam*</span><span class="sxs-lookup"><span data-stu-id="128ca-122">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="128ca-123">Обработчик, который активируется или деактивируется в зависимости от значения параметра *wParam* .</span><span class="sxs-lookup"><span data-stu-id="128ca-123">A handle to the window being activated or deactivated, depending on the value of the *wParam* parameter.</span></span> <span data-ttu-id="128ca-124">Если Нештатное слово *wParam* имеет **\_ неактивное значение WA**, то параметр *lParam* является обработчиком активируемого окна.</span><span class="sxs-lookup"><span data-stu-id="128ca-124">If the low-order word of *wParam* is **WA\_INACTIVE**, *lParam* is the handle to the window being activated.</span></span> <span data-ttu-id="128ca-125">Если младшее слово в параметре *wParam* имеет значение **WA \_ Active** или **WA \_ кликкактиве**, то *lParam* — это маркер деактивируемого окна.</span><span class="sxs-lookup"><span data-stu-id="128ca-125">If the low-order word of *wParam* is **WA\_ACTIVE** or **WA\_CLICKACTIVE**, *lParam* is the handle to the window being deactivated.</span></span> <span data-ttu-id="128ca-126">Этот обработчик может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="128ca-126">This handle can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="128ca-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="128ca-127">Return value</span></span>

<span data-ttu-id="128ca-128">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="128ca-128">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="128ca-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="128ca-129">Remarks</span></span>

<span data-ttu-id="128ca-130">Если окно активируется и не свернется, функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) устанавливает фокус клавиатуры на окно.</span><span class="sxs-lookup"><span data-stu-id="128ca-130">If the window is being activated and is not minimized, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function sets the keyboard focus to the window.</span></span> <span data-ttu-id="128ca-131">Если окно активируется щелчком мыши, оно также получает сообщение [**WM \_ маусеактивате**](wm-mouseactivate.md) .</span><span class="sxs-lookup"><span data-stu-id="128ca-131">If the window is activated by a mouse click, it also receives a [**WM\_MOUSEACTIVATE**](wm-mouseactivate.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="128ca-132">Требования</span><span class="sxs-lookup"><span data-stu-id="128ca-132">Requirements</span></span>



| <span data-ttu-id="128ca-133">Требование</span><span class="sxs-lookup"><span data-stu-id="128ca-133">Requirement</span></span> | <span data-ttu-id="128ca-134">Значение</span><span class="sxs-lookup"><span data-stu-id="128ca-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="128ca-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="128ca-135">Minimum supported client</span></span><br/> | <span data-ttu-id="128ca-136">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="128ca-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="128ca-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="128ca-137">Minimum supported server</span></span><br/> | <span data-ttu-id="128ca-138">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="128ca-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="128ca-139">Заголовок</span><span class="sxs-lookup"><span data-stu-id="128ca-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="128ca-140"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="128ca-140"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="128ca-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="128ca-141">See also</span></span>

<dl> <dt>

<span data-ttu-id="128ca-142">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="128ca-142">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="128ca-143">**дефвиндовпрок**</span><span class="sxs-lookup"><span data-stu-id="128ca-143">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="128ca-144">**сетактивевиндов**</span><span class="sxs-lookup"><span data-stu-id="128ca-144">**SetActiveWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-setactivewindow)
</dt> <dt>

[<span data-ttu-id="128ca-145">**WM \_ маусеактивате**</span><span class="sxs-lookup"><span data-stu-id="128ca-145">**WM\_MOUSEACTIVATE**</span></span>](wm-mouseactivate.md)
</dt> <dt>

[<span data-ttu-id="128ca-146">**WM \_ нкактивате**</span><span class="sxs-lookup"><span data-stu-id="128ca-146">**WM\_NCACTIVATE**</span></span>](/windows/desktop/winmsg/wm-ncactivate)
</dt> <dt>

<span data-ttu-id="128ca-147">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="128ca-147">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="128ca-148">Ввод с клавиатуры</span><span class="sxs-lookup"><span data-stu-id="128ca-148">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 


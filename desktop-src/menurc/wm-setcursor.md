---
title: Сообщение WM_SETCURSOR (Winuser. h)
description: Отправляется в окно, если указатель мыши вызывает перемещение курсора в пределах окна, а ввод с помощью мыши не фиксируется.
ms.assetid: b722689e-925f-40ac-ba4a-55be9dc6a8f8
keywords:
- WM_SETCURSOR меню сообщений и других ресурсов
topic_type:
- apiref
api_name:
- WM_SETCURSOR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e941919b447659e67fdcdd9e4e5f4ff2630f8bf1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071712"
---
# <a name="wm_setcursor-message"></a><span data-ttu-id="bd68b-104">\_Сообщение СЕТКУРСОР WM</span><span class="sxs-lookup"><span data-stu-id="bd68b-104">WM\_SETCURSOR message</span></span>

<span data-ttu-id="bd68b-105">Отправляется в окно, если указатель мыши вызывает перемещение курсора в пределах окна, а ввод с помощью мыши не фиксируется.</span><span class="sxs-lookup"><span data-stu-id="bd68b-105">Sent to a window if the mouse causes the cursor to move within a window and mouse input is not captured.</span></span>


```C++
#define WM_SETCURSOR                    0x0020
```



## <a name="parameters"></a><span data-ttu-id="bd68b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bd68b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd68b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bd68b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bd68b-108">Указатель на окно, содержащее курсор.</span><span class="sxs-lookup"><span data-stu-id="bd68b-108">A handle to the window that contains the cursor.</span></span>

</dd> <dt>

<span data-ttu-id="bd68b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bd68b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bd68b-110">Слово *lParam* с низким приоритетом задает результат проверки попадания для позиции курсора.</span><span class="sxs-lookup"><span data-stu-id="bd68b-110">The low-order word of *lParam* specifies the hit-test result for the cursor position.</span></span> <span data-ttu-id="bd68b-111">Возможные значения см. в разделе возвращаемые значения для [WM_NCHITTEST](../inputdev/wm-nchittest.md) .</span><span class="sxs-lookup"><span data-stu-id="bd68b-111">See the return values for [WM_NCHITTEST](../inputdev/wm-nchittest.md) for possible values.</span></span>

<span data-ttu-id="bd68b-112">Слово *lParam* в высоком порядке указывает на сообщение окна мыши, которое активировало это событие, например [WM_MOUSEMOVE](../inputdev/wm-mousemove.md).</span><span class="sxs-lookup"><span data-stu-id="bd68b-112">The high-order word of *lParam* specifies the mouse window message which triggered this event, such as [WM_MOUSEMOVE](../inputdev/wm-mousemove.md).</span></span> <span data-ttu-id="bd68b-113">Когда окно переходит в режим меню, это значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="bd68b-113">When the window enters menu mode, this value is zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd68b-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bd68b-114">Return value</span></span>

<span data-ttu-id="bd68b-115">Если приложение обрабатывает это сообщение, оно должно возвращать **значение true** , чтобы остановить дальнейшую обработку, или **false** , чтобы продолжить.</span><span class="sxs-lookup"><span data-stu-id="bd68b-115">If an application processes this message, it should return **TRUE** to halt further processing or **FALSE** to continue.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd68b-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bd68b-116">Remarks</span></span>

<span data-ttu-id="bd68b-117">Функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowprocw) передает сообщение **WM \_ сеткурсор** в родительское окно перед обработкой.</span><span class="sxs-lookup"><span data-stu-id="bd68b-117">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowprocw) function passes the **WM\_SETCURSOR** message to a parent window before processing.</span></span> <span data-ttu-id="bd68b-118">Если родительское окно возвращает **значение true**, то дальнейшая обработка прерывается.</span><span class="sxs-lookup"><span data-stu-id="bd68b-118">If the parent window returns **TRUE**, further processing is halted.</span></span> <span data-ttu-id="bd68b-119">Передача сообщения в родительское окно окна позволяет родительскому окну управлять параметром курсора в дочернем окне.</span><span class="sxs-lookup"><span data-stu-id="bd68b-119">Passing the message to a window's parent window gives the parent window control over the cursor's setting in a child window.</span></span> <span data-ttu-id="bd68b-120">Функция **дефвиндовпрок** также использует это сообщение, чтобы установить курсор на стрелку, если она не находится в клиентской области, или на курсор зарегистрированного класса, если он находится в клиентской области.</span><span class="sxs-lookup"><span data-stu-id="bd68b-120">The **DefWindowProc** function also uses this message to set the cursor to an arrow if it is not in the client area, or to the registered class cursor if it is in the client area.</span></span> <span data-ttu-id="bd68b-121">Если неупорядоченное слово параметра *lParam* имеет значение **хтеррор** , а высокое значение *lParam* указывает, что одна из кнопок мыши нажата, **дефвиндовпрок** вызывает функцию [**мессажебип**](/windows/desktop/api/winuser/nf-winuser-messagebeep) .</span><span class="sxs-lookup"><span data-stu-id="bd68b-121">If the low-order word of the *lParam* parameter is **HTERROR** and the high-order word of *lParam* specifies that one of the mouse buttons is pressed, **DefWindowProc** calls the [**MessageBeep**](/windows/desktop/api/winuser/nf-winuser-messagebeep) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd68b-122">Требования</span><span class="sxs-lookup"><span data-stu-id="bd68b-122">Requirements</span></span>



| <span data-ttu-id="bd68b-123">Требование</span><span class="sxs-lookup"><span data-stu-id="bd68b-123">Requirement</span></span> | <span data-ttu-id="bd68b-124">Значение</span><span class="sxs-lookup"><span data-stu-id="bd68b-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd68b-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bd68b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="bd68b-126">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="bd68b-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="bd68b-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bd68b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="bd68b-128">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="bd68b-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bd68b-129">Заголовок</span><span class="sxs-lookup"><span data-stu-id="bd68b-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd68b-130"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bd68b-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd68b-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bd68b-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="bd68b-132">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="bd68b-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="bd68b-133">**дефвиндовпрок**</span><span class="sxs-lookup"><span data-stu-id="bd68b-133">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowprocw)
</dt> <dt>

<span data-ttu-id="bd68b-134">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="bd68b-134">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="bd68b-135">[**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="bd68b-135">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="bd68b-136">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="bd68b-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="bd68b-137">Курсоры</span><span class="sxs-lookup"><span data-stu-id="bd68b-137">Cursors</span></span>](cursors.md)
</dt> </dl>

 


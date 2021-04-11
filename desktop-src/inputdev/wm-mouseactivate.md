---
title: Сообщение WM_MOUSEACTIVATE (Winuser. h)
description: Посылается, когда курсор находится в неактивном окне, и пользователь нажимает кнопку мыши. Родительское окно получает это сообщение, только если дочернее окно передает его функции Дефвиндовпрок.
ms.assetid: 335c0819-a655-4dd1-9511-1f148b87271c
keywords:
- WM_MOUSEACTIVATE ввода сообщений с клавиатуры и мыши
topic_type:
- apiref
api_name:
- WM_MOUSEACTIVATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ba74141f8d519541d1e63327179fff2f27ad403
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135635"
---
# <a name="wm_mouseactivate-message"></a><span data-ttu-id="9ed44-105">\_Сообщение МАУСЕАКТИВАТЕ WM</span><span class="sxs-lookup"><span data-stu-id="9ed44-105">WM\_MOUSEACTIVATE message</span></span>

<span data-ttu-id="9ed44-106">Посылается, когда курсор находится в неактивном окне, и пользователь нажимает кнопку мыши.</span><span class="sxs-lookup"><span data-stu-id="9ed44-106">Sent when the cursor is in an inactive window and the user presses a mouse button.</span></span> <span data-ttu-id="9ed44-107">Родительское окно получает это сообщение, только если дочернее окно передает его функции [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="9ed44-107">The parent window receives this message only if the child window passes it to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span>

<span data-ttu-id="9ed44-108">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="9ed44-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_MOUSEACTIVATE                0x0021
```



## <a name="parameters"></a><span data-ttu-id="9ed44-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="9ed44-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ed44-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9ed44-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9ed44-111">Маркер родительского окна верхнего уровня активируемого окна.</span><span class="sxs-lookup"><span data-stu-id="9ed44-111">A handle to the top-level parent window of the window being activated.</span></span>

</dd> <dt>

<span data-ttu-id="9ed44-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9ed44-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9ed44-113">Слово нижнего порядка указывает значение проверки попадания, возвращаемое функцией [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) в результате обработки сообщения [**WM \_ нчиттест**](wm-nchittest.md) .</span><span class="sxs-lookup"><span data-stu-id="9ed44-113">The low-order word specifies the hit-test value returned by the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function as a result of processing the [**WM\_NCHITTEST**](wm-nchittest.md) message.</span></span> <span data-ttu-id="9ed44-114">Список значений проверки попадания см. в разделе **WM \_ нчиттест**.</span><span class="sxs-lookup"><span data-stu-id="9ed44-114">For a list of hit-test values, see **WM\_NCHITTEST**.</span></span>

<span data-ttu-id="9ed44-115">Слово в высоком порядке указывает идентификатор сообщения мыши, формируемого при нажатии пользователем кнопки мыши.</span><span class="sxs-lookup"><span data-stu-id="9ed44-115">The high-order word specifies the identifier of the mouse message generated when the user pressed a mouse button.</span></span> <span data-ttu-id="9ed44-116">Сообщение мыши либо отбрасывается, либо отправляется в окно в зависимости от возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="9ed44-116">The mouse message is either discarded or posted to the window, depending on the return value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ed44-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9ed44-117">Return value</span></span>

<span data-ttu-id="9ed44-118">Возвращаемое значение указывает, следует ли активировать окно и следует ли отменять идентификатор сообщения мыши.</span><span class="sxs-lookup"><span data-stu-id="9ed44-118">The return value specifies whether the window should be activated and whether the identifier of the mouse message should be discarded.</span></span> <span data-ttu-id="9ed44-119">Это должно быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="9ed44-119">It must be one of the following values.</span></span>



| <span data-ttu-id="9ed44-120">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="9ed44-120">Return code/value</span></span>                                                                                                                                          | <span data-ttu-id="9ed44-121">Описание</span><span class="sxs-lookup"><span data-stu-id="9ed44-121">Description</span></span>                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9ed44-122"><dt>**MA \_ Активация**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="9ed44-122"><dt>**MA\_ACTIVATE**</dt> <dt>1</dt></span></span> </dl>         | <span data-ttu-id="9ed44-123">Активирует окно и не удаляет сообщение мыши.</span><span class="sxs-lookup"><span data-stu-id="9ed44-123">Activates the window, and does not discard the mouse message.</span></span><br/>         |
| <dl> <span data-ttu-id="9ed44-124"><dt>**MA \_ АКТИВАТЕАНДЕАТ**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="9ed44-124"><dt>**MA\_ACTIVATEANDEAT**</dt> <dt>2</dt></span></span> </dl>   | <span data-ttu-id="9ed44-125">Активирует окно и отклоняет сообщение мыши.</span><span class="sxs-lookup"><span data-stu-id="9ed44-125">Activates the window, and discards the mouse message.</span></span><br/>                 |
| <dl> <span data-ttu-id="9ed44-126"><dt>**MA \_ АКТИВИРОВАТЬ**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="9ed44-126"><dt>**MA\_NOACTIVATE**</dt> <dt>3</dt></span></span> </dl>       | <span data-ttu-id="9ed44-127">Не активирует окно и не удаляет сообщение мыши.</span><span class="sxs-lookup"><span data-stu-id="9ed44-127">Does not activate the window, and does not discard the mouse message.</span></span><br/> |
| <dl> <span data-ttu-id="9ed44-128"><dt>**MA \_ НОАКТИВАТЕАНДЕАТ**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="9ed44-128"><dt>**MA\_NOACTIVATEANDEAT**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="9ed44-129">Не активирует окно, но отклоняет сообщение мыши.</span><span class="sxs-lookup"><span data-stu-id="9ed44-129">Does not activate the window, but discards the mouse message.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="9ed44-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9ed44-130">Remarks</span></span>

<span data-ttu-id="9ed44-131">Функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) передает сообщение в родительское окно дочернего окна перед любой обработкой.</span><span class="sxs-lookup"><span data-stu-id="9ed44-131">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function passes the message to a child window's parent window before any processing occurs.</span></span> <span data-ttu-id="9ed44-132">Родительское окно определяет, следует ли активировать дочернее окно.</span><span class="sxs-lookup"><span data-stu-id="9ed44-132">The parent window determines whether to activate the child window.</span></span> <span data-ttu-id="9ed44-133">При активации дочернего окна родительское окно должно возвращать **MA \_** **\_ ноактиватеандеат или MA** , чтобы система больше не обрабатывал сообщение.</span><span class="sxs-lookup"><span data-stu-id="9ed44-133">If it activates the child window, the parent window should return **MA\_NOACTIVATE** or **MA\_NOACTIVATEANDEAT** to prevent the system from processing the message further.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ed44-134">Требования</span><span class="sxs-lookup"><span data-stu-id="9ed44-134">Requirements</span></span>



| <span data-ttu-id="9ed44-135">Требование</span><span class="sxs-lookup"><span data-stu-id="9ed44-135">Requirement</span></span> | <span data-ttu-id="9ed44-136">Значение</span><span class="sxs-lookup"><span data-stu-id="9ed44-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ed44-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9ed44-137">Minimum supported client</span></span><br/> | <span data-ttu-id="9ed44-138">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9ed44-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="9ed44-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9ed44-139">Minimum supported server</span></span><br/> | <span data-ttu-id="9ed44-140">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9ed44-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9ed44-141">Заголовок</span><span class="sxs-lookup"><span data-stu-id="9ed44-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ed44-142"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9ed44-142"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ed44-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9ed44-143">See also</span></span>

<dl> <dt>

<span data-ttu-id="9ed44-144">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="9ed44-144">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9ed44-145">**дефвиндовпрок**</span><span class="sxs-lookup"><span data-stu-id="9ed44-145">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

<span data-ttu-id="9ed44-146">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9ed44-146">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="9ed44-147">[**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9ed44-147">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="9ed44-148">**WM \_ нчиттест**</span><span class="sxs-lookup"><span data-stu-id="9ed44-148">**WM\_NCHITTEST**</span></span>](wm-nchittest.md)
</dt> <dt>

<span data-ttu-id="9ed44-149">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="9ed44-149">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9ed44-150">Ввод с помощью мыши</span><span class="sxs-lookup"><span data-stu-id="9ed44-150">Mouse Input</span></span>](mouse-input.md)
</dt> </dl>

 


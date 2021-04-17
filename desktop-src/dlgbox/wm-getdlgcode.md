---
title: Сообщение WM_GETDLGCODE (Winuser. h)
description: Отправляется в процедуру окна, связанную с элементом управления.
ms.assetid: 96d2caee-be6e-46e9-98b3-bffc3af1c003
keywords:
- WM_GETDLGCODE диалоговых окон сообщений
topic_type:
- apiref
api_name:
- WM_GETDLGCODE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89d6e1ddb3be21e227c4dad404a06113f5c50a49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691880"
---
# <a name="wm_getdlgcode-message"></a><span data-ttu-id="02deb-104">\_Сообщение ЖЕТДЛГКОДЕ WM</span><span class="sxs-lookup"><span data-stu-id="02deb-104">WM\_GETDLGCODE message</span></span>

<span data-ttu-id="02deb-105">Отправляется в процедуру окна, связанную с элементом управления.</span><span class="sxs-lookup"><span data-stu-id="02deb-105">Sent to the window procedure associated with a control.</span></span> <span data-ttu-id="02deb-106">По умолчанию система обрабатывает все вводы с клавиатуры для элемента управления. система интерпретирует определенные типы ввода с клавиатуры как клавиши навигации диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="02deb-106">By default, the system handles all keyboard input to the control; the system interprets certain types of keyboard input as dialog box navigation keys.</span></span> <span data-ttu-id="02deb-107">Чтобы переопределить это поведение по умолчанию, элемент управления может ответить на сообщение **WM \_ жетдлгкоде** , чтобы указать типы входных данных, которые необходимо обработать.</span><span class="sxs-lookup"><span data-stu-id="02deb-107">To override this default behavior, the control can respond to the **WM\_GETDLGCODE** message to indicate the types of input it wants to process itself.</span></span>


```C++
#define WM_GETDLGCODE                   0x0087
```



## <a name="parameters"></a><span data-ttu-id="02deb-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="02deb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02deb-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="02deb-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="02deb-110">Виртуальный ключ, нажатый пользователем и предлагающий Windows выдать это уведомление.</span><span class="sxs-lookup"><span data-stu-id="02deb-110">The virtual key, pressed by the user, that prompted Windows to issue this notification.</span></span> <span data-ttu-id="02deb-111">Обработчик должен выборочно обрабатывайте эти ключи.</span><span class="sxs-lookup"><span data-stu-id="02deb-111">The handler must selectively handle these keys.</span></span> <span data-ttu-id="02deb-112">Например, обработчик может принять и обработать **VK \_ return** , но делегировать **VK \_ вкладку** в окно владельца.</span><span class="sxs-lookup"><span data-stu-id="02deb-112">For instance, the handler might accept and process **VK\_RETURN** but delegate **VK\_TAB** to the owner window.</span></span> <span data-ttu-id="02deb-113">Список значений см. в разделе [**коды виртуальных клавиш**](/windows/desktop/inputdev/virtual-key-codes).</span><span class="sxs-lookup"><span data-stu-id="02deb-113">For a list of values, see [**Virtual-Key Codes**](/windows/desktop/inputdev/virtual-key-codes).</span></span>

</dd> <dt>

<span data-ttu-id="02deb-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="02deb-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="02deb-115">Указатель на структуру [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) (или **значение NULL** , если система выполняет запрос).</span><span class="sxs-lookup"><span data-stu-id="02deb-115">A pointer to an [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) structure (or **NULL** if the system is performing a query).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02deb-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="02deb-116">Return value</span></span>

<span data-ttu-id="02deb-117">Возвращаемое значение — одно или несколько из следующих значений, указывающее тип входных данных, обрабатываемых приложением.</span><span class="sxs-lookup"><span data-stu-id="02deb-117">The return value is one or more of the following values, indicating which type of input the application processes.</span></span>



| <span data-ttu-id="02deb-118">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="02deb-118">Return code/value</span></span>                                                                                                                                                | <span data-ttu-id="02deb-119">Описание</span><span class="sxs-lookup"><span data-stu-id="02deb-119">Description</span></span>                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="02deb-120"><dt>**Длгк \_ Кнопка "**</dt> <dt>0x2000</dt> "</span><span class="sxs-lookup"><span data-stu-id="02deb-120"><dt>**DLGC\_BUTTON**</dt> <dt>0x2000</dt></span></span> </dl>          | <span data-ttu-id="02deb-121">Переключатель.</span><span class="sxs-lookup"><span data-stu-id="02deb-121">Button.</span></span><br/>                                                                                                         |
| <dl> <span data-ttu-id="02deb-122"><dt>**Длгк \_ ДЕФПУШБУТТОН**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="02deb-122"><dt>**DLGC\_DEFPUSHBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>   | <span data-ttu-id="02deb-123">Кнопка отправки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="02deb-123">Default push button.</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="02deb-124"><dt>**Длгк \_ ХАССЕТСЕЛ**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="02deb-124"><dt>**DLGC\_HASSETSEL**</dt> <dt>0x0008</dt></span></span> </dl>       | <span data-ttu-id="02deb-125">[**EM \_ СЕТСЕЛ**](/windows/desktop/Controls/em-setsel) сообщения.</span><span class="sxs-lookup"><span data-stu-id="02deb-125">[**EM\_SETSEL**](/windows/desktop/Controls/em-setsel) messages.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="02deb-126"><dt>**Длгк \_ RADIOBUTTON**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="02deb-126"><dt>**DLGC\_RADIOBUTTON**</dt> <dt>0x0040</dt></span></span> </dl>     | <span data-ttu-id="02deb-127">Переключатель.</span><span class="sxs-lookup"><span data-stu-id="02deb-127">Radio button.</span></span><br/>                                                                                                   |
| <dl> <span data-ttu-id="02deb-128"><dt>**Длгк \_ СТАТИЧЕСКИЙ**</dt> <dt>0x0100</dt></span><span class="sxs-lookup"><span data-stu-id="02deb-128"><dt>**DLGC\_STATIC**</dt> <dt>0x0100</dt></span></span> </dl>          | <span data-ttu-id="02deb-129">Статический элемент управления.</span><span class="sxs-lookup"><span data-stu-id="02deb-129">Static control.</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="02deb-130"><dt>**Длгк \_ УНДЕФПУШБУТТОН**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="02deb-130"><dt>**DLGC\_UNDEFPUSHBUTTON**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="02deb-131">Кнопка отправки, не используемая по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="02deb-131">Non-default push button.</span></span><br/>                                                                                        |
| <dl> <span data-ttu-id="02deb-132"><dt>**Длгк \_ ВАНТАЛЛКЭЙС**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="02deb-132"><dt>**DLGC\_WANTALLKEYS**</dt> <dt>0x0004</dt></span></span> </dl>     | <span data-ttu-id="02deb-133">Все входные данные с клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="02deb-133">All keyboard input.</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="02deb-134"><dt>**Длгк \_ ВАНТАРРОВС**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="02deb-134"><dt>**DLGC\_WANTARROWS**</dt> <dt>0x0001</dt></span></span> </dl>      | <span data-ttu-id="02deb-135">Клавиши направления.</span><span class="sxs-lookup"><span data-stu-id="02deb-135">Direction keys.</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="02deb-136"><dt>**Длгк \_ ВАНТЧАРС**</dt> <dt>0x0080</dt></span><span class="sxs-lookup"><span data-stu-id="02deb-136"><dt>**DLGC\_WANTCHARS**</dt> <dt>0x0080</dt></span></span> </dl>       | <span data-ttu-id="02deb-137">[**WM \_ Сообщения типа CHAR**](/windows/desktop/inputdev/wm-char) .</span><span class="sxs-lookup"><span data-stu-id="02deb-137">[**WM\_CHAR**](/windows/desktop/inputdev/wm-char) messages.</span></span><br/>                                                                      |
| <dl> <span data-ttu-id="02deb-138"><dt>**Длгк \_ ВАНТМЕССАЖЕ**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="02deb-138"><dt>**DLGC\_WANTMESSAGE**</dt> <dt>0x0004</dt></span></span> </dl>     | <span data-ttu-id="02deb-139">Все входные данные с клавиатуры (приложение передает это сообщение в структуру [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) в элемент управления).</span><span class="sxs-lookup"><span data-stu-id="02deb-139">All keyboard input (the application passes this message in the [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) structure to the control).</span></span><br/> |
| <dl> <span data-ttu-id="02deb-140"><dt>**Длгк \_ ВАНТТАБ**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="02deb-140"><dt>**DLGC\_WANTTAB**</dt> <dt>0x0002</dt></span></span> </dl>         | <span data-ttu-id="02deb-141">Клавиша TAB.</span><span class="sxs-lookup"><span data-stu-id="02deb-141">TAB key.</span></span><br/>                                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="02deb-142">Комментарии</span><span class="sxs-lookup"><span data-stu-id="02deb-142">Remarks</span></span>

<span data-ttu-id="02deb-143">Хотя функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) всегда возвращает ноль в ответ на сообщение **\_ жетдлгкоде WM** , процедура окна для предопределенных классов элементов управления возвращает код, соответствующий каждому классу.</span><span class="sxs-lookup"><span data-stu-id="02deb-143">Although the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function always returns zero in response to the **WM\_GETDLGCODE** message, the window procedure for the predefined control classes return a code appropriate for each class.</span></span>

<span data-ttu-id="02deb-144">Сообщение **WM \_ жетдлгкоде** и возвращаемые значения полезны только с пользовательскими элементами управления диалогового окна или стандартными элементами управления, измененными подклассами.</span><span class="sxs-lookup"><span data-stu-id="02deb-144">The **WM\_GETDLGCODE** message and the returned values are useful only with user-defined dialog box controls or standard controls modified by subclassing.</span></span>

## <a name="requirements"></a><span data-ttu-id="02deb-145">Требования</span><span class="sxs-lookup"><span data-stu-id="02deb-145">Requirements</span></span>



| <span data-ttu-id="02deb-146">Требование</span><span class="sxs-lookup"><span data-stu-id="02deb-146">Requirement</span></span> | <span data-ttu-id="02deb-147">Значение</span><span class="sxs-lookup"><span data-stu-id="02deb-147">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02deb-148">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="02deb-148">Minimum supported client</span></span><br/> | <span data-ttu-id="02deb-149">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="02deb-149">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="02deb-150">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="02deb-150">Minimum supported server</span></span><br/> | <span data-ttu-id="02deb-151">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="02deb-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="02deb-152">Заголовок</span><span class="sxs-lookup"><span data-stu-id="02deb-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="02deb-153"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="02deb-153"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02deb-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="02deb-154">See also</span></span>

<dl> <dt>

<span data-ttu-id="02deb-155">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="02deb-155">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="02deb-156">**дефвиндовпрок**</span><span class="sxs-lookup"><span data-stu-id="02deb-156">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="02deb-157">**EM \_ сетсел**</span><span class="sxs-lookup"><span data-stu-id="02deb-157">**EM\_SETSEL**</span></span>](/windows/desktop/Controls/em-setsel)
</dt> <dt>

[<span data-ttu-id="02deb-158">**ОБ**</span><span class="sxs-lookup"><span data-stu-id="02deb-158">**MSG**</span></span>](/windows/win32/api/winuser/ns-winuser-msg)
</dt> <dt>

[<span data-ttu-id="02deb-159">**WM \_ char**</span><span class="sxs-lookup"><span data-stu-id="02deb-159">**WM\_CHAR**</span></span>](/windows/desktop/inputdev/wm-char)
</dt> <dt>

<span data-ttu-id="02deb-160">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="02deb-160">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="02deb-161">Диалоговые окна</span><span class="sxs-lookup"><span data-stu-id="02deb-161">Dialog Boxes</span></span>](dialog-boxes.md)
</dt> </dl>

 


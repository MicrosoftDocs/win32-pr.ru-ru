---
description: Передается в окно с фокусом, когда пользователь выбирает новый язык ввода с помощью сочетания клавиш (указанного в приложении панели управления "клавиатура") или из индикатора на системной панели задач.
ms.assetid: db38c31c-6ae4-4401-82b8-7fd220c1678c
title: Сообщение WM_INPUTLANGCHANGEREQUEST (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1df361c479978083c29281764e65c48b131c22b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105693070"
---
# <a name="wm_inputlangchangerequest-message"></a><span data-ttu-id="0169b-103">\_Сообщение ИНПУТЛАНГЧАНЖЕРЕКУЕСТ WM</span><span class="sxs-lookup"><span data-stu-id="0169b-103">WM\_INPUTLANGCHANGEREQUEST message</span></span>

<span data-ttu-id="0169b-104">Передается в окно с фокусом, когда пользователь выбирает новый язык ввода с помощью сочетания клавиш (указанного в приложении панели управления "клавиатура") или из индикатора на системной панели задач.</span><span class="sxs-lookup"><span data-stu-id="0169b-104">Posted to the window with the focus when the user chooses a new input language, either with the hotkey (specified in the Keyboard control panel application) or from the indicator on the system taskbar.</span></span> <span data-ttu-id="0169b-105">Приложение может принять изменение, передав сообщение функции [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) или отклонить изменение (и предотвратить его выполнение), немедленно выполнив возврат.</span><span class="sxs-lookup"><span data-stu-id="0169b-105">An application can accept the change by passing the message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function or reject the change (and prevent it from taking place) by returning immediately.</span></span>

<span data-ttu-id="0169b-106">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="0169b-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_INPUTLANGCHANGEREQUEST       0x0050
```



## <a name="parameters"></a><span data-ttu-id="0169b-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="0169b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0169b-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0169b-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0169b-109">Новый языковой стандарт ввода.</span><span class="sxs-lookup"><span data-stu-id="0169b-109">The new input locale.</span></span> <span data-ttu-id="0169b-110">Этот параметр может быть сочетанием следующих флагов.</span><span class="sxs-lookup"><span data-stu-id="0169b-110">This parameter can be a combination of the following flags.</span></span>



| <span data-ttu-id="0169b-111">Значение</span><span class="sxs-lookup"><span data-stu-id="0169b-111">Value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="0169b-112">Значение</span><span class="sxs-lookup"><span data-stu-id="0169b-112">Meaning</span></span>                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INPUTLANGCHANGE_BACKWARD"></span><span id="inputlangchange_backward"></span><dl> <span data-ttu-id="0169b-113"><dt>**Инпутлангчанже \_ НАЗАД**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="0169b-113"><dt>**INPUTLANGCHANGE\_BACKWARD**</dt> <dt>0x0004</dt></span></span> </dl>       | <span data-ttu-id="0169b-114">Для выбора предыдущего языка ввода в списке установленных языков ввода используются горячие клавиши.</span><span class="sxs-lookup"><span data-stu-id="0169b-114">A hot key was used to choose the previous input locale in the installed list of input locales.</span></span> <span data-ttu-id="0169b-115">Этот флаг нельзя использовать с \_ флагом пересылки инпутлангчанже.</span><span class="sxs-lookup"><span data-stu-id="0169b-115">This flag cannot be used with the INPUTLANGCHANGE\_FORWARD flag.</span></span><br/> |
| <span id="INPUTLANGCHANGE_FORWARD"></span><span id="inputlangchange_forward"></span><dl> <span data-ttu-id="0169b-116"><dt>**Инпутлангчанже \_ Пересылка**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="0169b-116"><dt>**INPUTLANGCHANGE\_FORWARD**</dt> <dt>0x0002</dt></span></span> </dl>          | <span data-ttu-id="0169b-117">Сочетание клавиш используется для выбора следующего языкового стандарта ввода в списке установленных языков ввода.</span><span class="sxs-lookup"><span data-stu-id="0169b-117">A hot key was used to choose the next input locale in the installed list of input locales.</span></span> <span data-ttu-id="0169b-118">Этот флаг нельзя использовать с \_ флагом обратной инпутлангчанже.</span><span class="sxs-lookup"><span data-stu-id="0169b-118">This flag cannot be used with the INPUTLANGCHANGE\_BACKWARD flag.</span></span><br/>    |
| <span id="INPUTLANGCHANGE_SYSCHARSET"></span><span id="inputlangchange_syscharset"></span><dl> <span data-ttu-id="0169b-119"><dt>**Инпутлангчанже \_ СИСЧАРСЕТ**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="0169b-119"><dt>**INPUTLANGCHANGE\_SYSCHARSET**</dt> <dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="0169b-120">Раскладка клавиатуры нового языка ввода может использоваться с системным набором символов.</span><span class="sxs-lookup"><span data-stu-id="0169b-120">The new input locale's keyboard layout can be used with the system character set.</span></span><br/>                                                                               |



 

</dd> <dt>

<span data-ttu-id="0169b-121">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0169b-121">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0169b-122">Идентификатор локали ввода.</span><span class="sxs-lookup"><span data-stu-id="0169b-122">The input locale identifier.</span></span> <span data-ttu-id="0169b-123">Дополнительные сведения см. в разделе [языки, языковые стандарты и раскладки клавиатуры](../inputdev/about-keyboard-input.md).</span><span class="sxs-lookup"><span data-stu-id="0169b-123">For more information, see [Languages, Locales, and Keyboard Layouts](../inputdev/about-keyboard-input.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0169b-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0169b-124">Return value</span></span>

<span data-ttu-id="0169b-125">Тип: **lResult**</span><span class="sxs-lookup"><span data-stu-id="0169b-125">Type: **LRESULT**</span></span>

<span data-ttu-id="0169b-126">Это сообщение публикуется в приложении, а не отправляется, поэтому возвращаемое значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="0169b-126">This message is posted, not sent, to the application, so the return value is ignored.</span></span> <span data-ttu-id="0169b-127">Чтобы принять изменение, приложение должно передать сообщение в [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="0169b-127">To accept the change, the application should pass the message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span> <span data-ttu-id="0169b-128">Чтобы отклонить изменение, приложение должно вернуть нуль, не вызывая **дефвиндовпрок**.</span><span class="sxs-lookup"><span data-stu-id="0169b-128">To reject the change, the application should return zero without calling **DefWindowProc**.</span></span>

## <a name="remarks"></a><span data-ttu-id="0169b-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0169b-129">Remarks</span></span>

<span data-ttu-id="0169b-130">Когда функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) получает сообщение **WM \_ инпутлангчанжерекуест** , она активирует новый языковой стандарт ввода и уведомляет приложение об изменении, отправляя сообщение [**WM \_ инпутлангчанже**](wm-inputlangchange.md) .</span><span class="sxs-lookup"><span data-stu-id="0169b-130">When the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function receives the **WM\_INPUTLANGCHANGEREQUEST** message, it activates the new input locale and notifies the application of the change by sending the [**WM\_INPUTLANGCHANGE**](wm-inputlangchange.md) message.</span></span>

<span data-ttu-id="0169b-131">Индикатор языка отображается на панели задач только в том случае, если вы установили несколько раскладок клавиатуры и включили индикатор с помощью приложения панели управления "клавиатура".</span><span class="sxs-lookup"><span data-stu-id="0169b-131">The language indicator is present on the taskbar only if you have installed more than one keyboard layout and if you have enabled the indicator using the Keyboard control panel application.</span></span>

## <a name="requirements"></a><span data-ttu-id="0169b-132">Требования</span><span class="sxs-lookup"><span data-stu-id="0169b-132">Requirements</span></span>



| <span data-ttu-id="0169b-133">Требование</span><span class="sxs-lookup"><span data-stu-id="0169b-133">Requirement</span></span> | <span data-ttu-id="0169b-134">Значение</span><span class="sxs-lookup"><span data-stu-id="0169b-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0169b-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0169b-135">Minimum supported client</span></span><br/> | <span data-ttu-id="0169b-136">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0169b-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="0169b-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0169b-137">Minimum supported server</span></span><br/> | <span data-ttu-id="0169b-138">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0169b-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0169b-139">Заголовок</span><span class="sxs-lookup"><span data-stu-id="0169b-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="0169b-140"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0169b-140"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0169b-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0169b-141">See also</span></span>

<dl> <dt>

<span data-ttu-id="0169b-142">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="0169b-142">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0169b-143">**дефвиндовпрок**</span><span class="sxs-lookup"><span data-stu-id="0169b-143">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="0169b-144">**WM \_ инпутлангчанже**</span><span class="sxs-lookup"><span data-stu-id="0169b-144">**WM\_INPUTLANGCHANGE**</span></span>](wm-inputlangchange.md)
</dt> <dt>

<span data-ttu-id="0169b-145">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="0169b-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0169b-146">Windows</span><span class="sxs-lookup"><span data-stu-id="0169b-146">Windows</span></span>](windows.md)
</dt> </dl>

 

 

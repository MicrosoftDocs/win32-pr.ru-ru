---
title: Код уведомления WM_VSCROLL (TrackBar) (Winuser. h)
description: Сообщение WM \_ VSCROLL отправляется владельцу элемента управления "вертикальная прокрутка" при изменении положения ползунка. Окно получает это сообщение через функцию WindowProc.
ms.assetid: E491E210-9605-4ABB-A667-471830DA7C2B
keywords:
- Элементы управления Windows для кода уведомления WM_VSCROLL (TrackBar)
topic_type:
- apiref
api_name:
- WM_HSCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1e13b07fab3335bf99469cd43ed1caa10373a97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136390"
---
# <a name="wm_vscroll-trackbar-notification-code"></a><span data-ttu-id="aa941-105">\_Код уведомления WM VSCROLL (TrackBar)</span><span class="sxs-lookup"><span data-stu-id="aa941-105">WM\_VSCROLL (Trackbar) notification code</span></span>

<span data-ttu-id="aa941-106">Сообщение **WM \_ VSCROLL** отправляется владельцу элемента управления "вертикальная прокрутка" при изменении положения ползунка.</span><span class="sxs-lookup"><span data-stu-id="aa941-106">The **WM\_VSCROLL** message is sent to the owner of a vertical trackbar control when the slider changes position.</span></span>

<span data-ttu-id="aa941-107">Окно получает это сообщение через функцию [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="aa941-107">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
WM_HSCROLL

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="aa941-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="aa941-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa941-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="aa941-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aa941-110">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает текущее положение ползунка, если [**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) — ТБ \_ сумбпоситион или ТБ \_ сумбтракк.</span><span class="sxs-lookup"><span data-stu-id="aa941-110">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the current position of the slider if the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is TB\_THUMBPOSITION or TB\_THUMBTRACK.</span></span> <span data-ttu-id="aa941-111">Для всех остальных кодов уведомлений слово в высоком порядке имеет нулевое значение; Отправьте сообщение [**ТБМ \_ жетпос**](tbm-getpos.md) , чтобы определить положение ползунка.</span><span class="sxs-lookup"><span data-stu-id="aa941-111">For all other notification codes, the high-order word is zero; send the [**TBM\_GETPOS**](tbm-getpos.md) message to determine the slider position.</span></span>

<span data-ttu-id="aa941-112">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) указывает код уведомления, указывающий на взаимодействие пользователя с TrackBar.</span><span class="sxs-lookup"><span data-stu-id="aa941-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies a notification code that indicates the user's interaction with the trackbar.</span></span> <span data-ttu-id="aa941-113">Это слово может принимать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="aa941-113">This word can be one of the following values.</span></span>



| <span data-ttu-id="aa941-114">Значение</span><span class="sxs-lookup"><span data-stu-id="aa941-114">Value</span></span>                                                                                                                                                                  | <span data-ttu-id="aa941-115">Значение</span><span class="sxs-lookup"><span data-stu-id="aa941-115">Meaning</span></span>                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TB_BOTTOM"></span><span id="tb_bottom"></span><dl> <span data-ttu-id="aa941-116"><dt>**\_Нижняя ТБ**</dt></span><span class="sxs-lookup"><span data-stu-id="aa941-116"><dt>**TB\_BOTTOM**</dt></span></span> </dl>                      | <span data-ttu-id="aa941-117">Пользователь нажал на конец ключа ([**VK \_ End**](/windows/desktop/inputdev/virtual-key-codes)).</span><span class="sxs-lookup"><span data-stu-id="aa941-117">The user pressed the END key ([**VK\_END**](/windows/desktop/inputdev/virtual-key-codes)).</span></span><br/>                                                                                          |
| <span id="TB_ENDTRACK"></span><span id="tb_endtrack"></span><dl> <span data-ttu-id="aa941-118"><dt>**\_ЕНДТРАКК ТБ**</dt></span><span class="sxs-lookup"><span data-stu-id="aa941-118"><dt>**TB\_ENDTRACK**</dt></span></span> </dl>                | <span data-ttu-id="aa941-119">Значение TrackBar получило [**WM \_ KEYUP**](/windows/desktop/inputdev/wm-keyup), означающее, что пользователь освободил ключ, который отправил соответствующий виртуальный код клавиши.</span><span class="sxs-lookup"><span data-stu-id="aa941-119">The trackbar received [**WM\_KEYUP**](/windows/desktop/inputdev/wm-keyup), meaning that the user released a key that sent a relevant virtual key code.</span></span> <br/>                                           |
| <span id="TB_LINEDOWN"></span><span id="tb_linedown"></span><dl> <span data-ttu-id="aa941-120"><dt>**\_ЛИНЕДОВН ТБ**</dt></span><span class="sxs-lookup"><span data-stu-id="aa941-120"><dt>**TB\_LINEDOWN**</dt></span></span> </dl>                | <span data-ttu-id="aa941-121">Пользователь нажал клавишу Стрелка вправо ([**VK \_ right**](/windows/desktop/inputdev/virtual-key-codes)) или стрелка вниз ([**VK \_ Down**](/windows/desktop/inputdev/virtual-key-codes)).</span><span class="sxs-lookup"><span data-stu-id="aa941-121">The user pressed the RIGHT ARROW ([**VK\_RIGHT**](/windows/desktop/inputdev/virtual-key-codes)) or DOWN ARROW ([**VK\_DOWN**](/windows/desktop/inputdev/virtual-key-codes)) key.</span></span><br/> |
| <span id="TB_LINEUP"></span><span id="tb_lineup"></span><dl> <span data-ttu-id="aa941-122"><dt>**Разметка \_ ТБ**</dt></span><span class="sxs-lookup"><span data-stu-id="aa941-122"><dt>**TB\_LINEUP**</dt></span></span> </dl>                      | <span data-ttu-id="aa941-123">Пользователь нажал клавишу Стрелка влево ([**VK \_ Left**](/windows/desktop/inputdev/virtual-key-codes)) или стрелка вверх ([**VK \_ up**](/windows/desktop/inputdev/virtual-key-codes)).</span><span class="sxs-lookup"><span data-stu-id="aa941-123">The user pressed the LEFT ARROW ([**VK\_LEFT**](/windows/desktop/inputdev/virtual-key-codes)) or UP ARROW ([**VK\_UP**](/windows/desktop/inputdev/virtual-key-codes)) key.</span></span><br/>             |
| <span id="TB_PAGEDOWN"></span><span id="tb_pagedown"></span><dl> <span data-ttu-id="aa941-124"><dt>**\_PageDown ТБ**</dt></span><span class="sxs-lookup"><span data-stu-id="aa941-124"><dt>**TB\_PAGEDOWN**</dt></span></span> </dl>                | <span data-ttu-id="aa941-125">Пользователь щелкнул канал ниже или справа от ползунка ([**VK \_ Далее**](/windows/desktop/inputdev/virtual-key-codes)).</span><span class="sxs-lookup"><span data-stu-id="aa941-125">The user clicked the channel below or to the right of the slider ([**VK\_NEXT**](/windows/desktop/inputdev/virtual-key-codes)).</span></span><br/>                                                   |
| <span id="TB_PAGEUP"></span><span id="tb_pageup"></span><dl> <span data-ttu-id="aa941-126"><dt>**\_PageUp ТБ**</dt></span><span class="sxs-lookup"><span data-stu-id="aa941-126"><dt>**TB\_PAGEUP**</dt></span></span> </dl>                      | <span data-ttu-id="aa941-127">Пользователь щелкнул канал выше или слева от ползунка ([**VK \_ ранее**](/windows/desktop/inputdev/virtual-key-codes)).</span><span class="sxs-lookup"><span data-stu-id="aa941-127">The user clicked the channel above or to the left of the slider ([**VK\_PRIOR**](/windows/desktop/inputdev/virtual-key-codes)).</span></span><br/>                                                 |
| <span id="TB_THUMBPOSITION"></span><span id="tb_thumbposition"></span><dl> <span data-ttu-id="aa941-128"><dt>**\_СУМБПОСИТИОН ТБ**</dt></span><span class="sxs-lookup"><span data-stu-id="aa941-128"><dt>**TB\_THUMBPOSITION**</dt></span></span> </dl> | <span data-ttu-id="aa941-129">Значение TrackBar, полученное от [**WM \_ лбуттонуп**](/windows/desktop/inputdev/wm-lbuttonup) , после \_ кода уведомления сумбтракк ТБ.</span><span class="sxs-lookup"><span data-stu-id="aa941-129">The trackbar received [**WM\_LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) following a TB\_THUMBTRACK notification code.</span></span><br/>                                                                   |
| <span id="TB_THUMBTRACK"></span><span id="tb_thumbtrack"></span><dl> <span data-ttu-id="aa941-130"><dt>**\_СУМБТРАКК ТБ**</dt></span><span class="sxs-lookup"><span data-stu-id="aa941-130"><dt>**TB\_THUMBTRACK**</dt></span></span> </dl>          | <span data-ttu-id="aa941-131">Пользователь переместил ползунок.</span><span class="sxs-lookup"><span data-stu-id="aa941-131">The user dragged the slider.</span></span><br/>                                                                                                                                                     |
| <span id="TB_TOP"></span><span id="tb_top"></span><dl> <span data-ttu-id="aa941-132"><dt>**\_верхний ТБ**</dt></span><span class="sxs-lookup"><span data-stu-id="aa941-132"><dt>**TB\_TOP**</dt></span></span> </dl>                               | <span data-ttu-id="aa941-133">Пользователь нажал на ДОМАШНЮЮ клавишу ([**VK \_ Home**](/windows/desktop/inputdev/virtual-key-codes)).</span><span class="sxs-lookup"><span data-stu-id="aa941-133">The user pressed the HOME key ([**VK\_HOME**](/windows/desktop/inputdev/virtual-key-codes)).</span></span> <br/>                                                                                     |



 

</dd> <dt>

<span data-ttu-id="aa941-134">*lParam*</span><span class="sxs-lookup"><span data-stu-id="aa941-134">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aa941-135">Маркер для элемента управления TrackBar.</span><span class="sxs-lookup"><span data-stu-id="aa941-135">The handle to the trackbar control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa941-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="aa941-136">Return value</span></span>

<span data-ttu-id="aa941-137">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="aa941-137">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa941-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="aa941-138">Remarks</span></span>

<span data-ttu-id="aa941-139">\_Код СУМБТРАКК ТБ обычно используется приложениями, которые предоставляют отзыв по мере того, как пользователь перетаскивает ползунок.</span><span class="sxs-lookup"><span data-stu-id="aa941-139">The TB\_THUMBTRACK code is typically used by applications that provide feedback as the user drags the scroll box.</span></span>

<span data-ttu-id="aa941-140">Обратите внимание, что сообщение **WM \_ VSCROLL** содержит только 16 бит данных о положении.</span><span class="sxs-lookup"><span data-stu-id="aa941-140">Note that the **WM\_VSCROLL** message carries only 16 bits of position data.</span></span> <span data-ttu-id="aa941-141">Таким же, приложения, которые используют только **WM \_ VSCROLL** (и [**WM \_ HSCROLL**](wm-hscroll--trackbar-.md)) для данных о положении ползунка, имеют практически максимальное значение положения 65 535.</span><span class="sxs-lookup"><span data-stu-id="aa941-141">Thus, applications that rely solely on **WM\_VSCROLL** (and [**WM\_HSCROLL**](wm-hscroll--trackbar-.md)) for slider position data have a practical maximum position value of 65,535.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa941-142">Требования</span><span class="sxs-lookup"><span data-stu-id="aa941-142">Requirements</span></span>



| <span data-ttu-id="aa941-143">Требование</span><span class="sxs-lookup"><span data-stu-id="aa941-143">Requirement</span></span> | <span data-ttu-id="aa941-144">Значение</span><span class="sxs-lookup"><span data-stu-id="aa941-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa941-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="aa941-145">Minimum supported client</span></span><br/> | <span data-ttu-id="aa941-146">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="aa941-146">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="aa941-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="aa941-147">Minimum supported server</span></span><br/> | <span data-ttu-id="aa941-148">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="aa941-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="aa941-149">Header</span><span class="sxs-lookup"><span data-stu-id="aa941-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa941-150"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="aa941-150"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa941-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aa941-151">See also</span></span>

<dl> <dt>

<span data-ttu-id="aa941-152">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="aa941-152">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="aa941-153">**WM \_ HSCROLL**</span><span class="sxs-lookup"><span data-stu-id="aa941-153">**WM\_HSCROLL**</span></span>](wm-hscroll--trackbar-.md)
</dt> </dl>

 


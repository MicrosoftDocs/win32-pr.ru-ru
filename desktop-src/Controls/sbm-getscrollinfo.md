---
title: Сообщение SBM_GETSCROLLINFO (Winuser. h)
description: '\_Для получения параметров полосы прокрутки отправляется сообщение СБМ жетскроллинфо.'
ms.assetid: 3b43430f-b55f-43ec-8558-baf5c953064f
keywords:
- Элементы управления Windows для SBM_GETSCROLLINFO сообщений
topic_type:
- apiref
api_name:
- SBM_GETSCROLLINFO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4cb05b05ba2686d755c5fa34adcff0016433346
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654701"
---
# <a name="sbm_getscrollinfo-message"></a><span data-ttu-id="54c5d-104">\_Сообщение СБМ жетскроллинфо</span><span class="sxs-lookup"><span data-stu-id="54c5d-104">SBM\_GETSCROLLINFO message</span></span>

<span data-ttu-id="54c5d-105">Для получения параметров полосы прокрутки отправляется сообщение **СБМ \_ жетскроллинфо** .</span><span class="sxs-lookup"><span data-stu-id="54c5d-105">The **SBM\_GETSCROLLINFO** message is sent to retrieve the parameters of a scroll bar.</span></span>

<span data-ttu-id="54c5d-106">Приложения не должны отсылать это сообщение напрямую.</span><span class="sxs-lookup"><span data-stu-id="54c5d-106">Applications should not send this message directly.</span></span> <span data-ttu-id="54c5d-107">Вместо этого они должны использовать функцию [**жетскроллинфо**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) .</span><span class="sxs-lookup"><span data-stu-id="54c5d-107">Instead, they should use the [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) function.</span></span> <span data-ttu-id="54c5d-108">Окно получает это сообщение через функцию [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="54c5d-108">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span> <span data-ttu-id="54c5d-109">Приложения, которые реализуют пользовательский элемент управления "полоса прокрутки", должны отвечать на эти сообщения, чтобы функция **жетскроллинфо** работала правильно.</span><span class="sxs-lookup"><span data-stu-id="54c5d-109">Applications which implement a custom scroll bar control must respond to these messages for the **GetScrollInfo** function to work properly.</span></span>

## <a name="parameters"></a><span data-ttu-id="54c5d-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="54c5d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54c5d-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="54c5d-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="54c5d-112">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="54c5d-112">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="54c5d-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="54c5d-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="54c5d-114">Указатель на структуру [**скроллинфо**](/windows/win32/api/winuser/ns-winuser-scrollinfo) .</span><span class="sxs-lookup"><span data-stu-id="54c5d-114">Pointer to a [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) structure.</span></span> <span data-ttu-id="54c5d-115">Перед вызовом [**жетскроллинфо**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)задайте для элемента **кбсизе** структуры значение **sizeof**(**скроллинфо**) и установите элемент **фмаск** , чтобы указать параметры полосы прокрутки для извлечения.</span><span class="sxs-lookup"><span data-stu-id="54c5d-115">Before calling [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo), set the **cbSize** member of the structure to **sizeof**(**SCROLLINFO**), and set the **fMask** member to specify the scroll bar parameters to retrieve.</span></span> <span data-ttu-id="54c5d-116">Перед возвратом сообщение копирует указанные параметры в соответствующие члены структуры.</span><span class="sxs-lookup"><span data-stu-id="54c5d-116">Before returning, the message copies the specified parameters to the appropriate members of the structure.</span></span>

<span data-ttu-id="54c5d-117">Элемент **фмаск** может иметь одно или несколько из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="54c5d-117">The **fMask** member can be one or more of the following values.</span></span>



| <span data-ttu-id="54c5d-118">Значение</span><span class="sxs-lookup"><span data-stu-id="54c5d-118">Value</span></span>                                                                                                                                                      | <span data-ttu-id="54c5d-119">Значение</span><span class="sxs-lookup"><span data-stu-id="54c5d-119">Meaning</span></span>                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span id="SIF_ALL"></span><span id="sif_all"></span><dl> <span data-ttu-id="54c5d-120"><dt>**SIF \_ все**</dt></span><span class="sxs-lookup"><span data-stu-id="54c5d-120"><dt>**SIF\_ALL**</dt></span></span> </dl>                | <span data-ttu-id="54c5d-121">Сочетание страницы SIF \_ , SIF \_ POS, SIF \_ Range и SIF \_ траккпос.</span><span class="sxs-lookup"><span data-stu-id="54c5d-121">Combination of SIF\_PAGE, SIF\_POS, SIF\_RANGE, and SIF\_TRACKPOS.</span></span><br/>       |
| <span id="SIF_PAGE"></span><span id="sif_page"></span><dl> <span data-ttu-id="54c5d-122"><dt>**\_страница SIF**</dt></span><span class="sxs-lookup"><span data-stu-id="54c5d-122"><dt>**SIF\_PAGE**</dt></span></span> </dl>             | <span data-ttu-id="54c5d-123">Копирует страницу прокрутки в элемент Нпаже.</span><span class="sxs-lookup"><span data-stu-id="54c5d-123">Copies the scroll page to the nPage member.</span></span><br/>                              |
| <span id="SIF_POS"></span><span id="sif_pos"></span><dl> <span data-ttu-id="54c5d-124"><dt>**SIF \_ POS**</dt></span><span class="sxs-lookup"><span data-stu-id="54c5d-124"><dt>**SIF\_POS**</dt></span></span> </dl>                | <span data-ttu-id="54c5d-125">Копирует расположение прокрутки в элемент nPos.</span><span class="sxs-lookup"><span data-stu-id="54c5d-125">Copies the scroll position to the nPos member.</span></span> <br/>                          |
| <span id="SIF_RANGE"></span><span id="sif_range"></span><dl> <span data-ttu-id="54c5d-126"><dt>**\_диапазон SIF**</dt></span><span class="sxs-lookup"><span data-stu-id="54c5d-126"><dt>**SIF\_RANGE**</dt></span></span> </dl>          | <span data-ttu-id="54c5d-127">Копирует диапазон прокрутки в элементы Nмин. и Nмакс..</span><span class="sxs-lookup"><span data-stu-id="54c5d-127">Copies the scroll range to the nMin and nMax members.</span></span> <br/>                   |
| <span id="SIF_TRACKPOS"></span><span id="sif_trackpos"></span><dl> <span data-ttu-id="54c5d-128"><dt>**SIF \_ траккпос**</dt></span><span class="sxs-lookup"><span data-stu-id="54c5d-128"><dt>**SIF\_TRACKPOS**</dt></span></span> </dl> | <span data-ttu-id="54c5d-129">Копирует текущую отслеживаемую точку прокрутки в элемент Нтраккпос.</span><span class="sxs-lookup"><span data-stu-id="54c5d-129">Copies the current scroll box tracking position to the nTrackPos member.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54c5d-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="54c5d-130">Return value</span></span>

<span data-ttu-id="54c5d-131">Если сообщение получает какие-либо значения, возвращается значение **true**. в противном случае — **false**.</span><span class="sxs-lookup"><span data-stu-id="54c5d-131">If the message retrieved any values, the return value is **TRUE**; otherwise, it is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="54c5d-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="54c5d-132">Remarks</span></span>

<span data-ttu-id="54c5d-133">Сообщения, указывающие расположение полосы прокрутки, [**WM \_ HSCROLL**](wm-hscroll.md) и [**WM \_ VSCROLL**](wm-vscroll.md), содержат только 16 бит данных о положении.</span><span class="sxs-lookup"><span data-stu-id="54c5d-133">The messages that indicate scroll bar position, [**WM\_HSCROLL**](wm-hscroll.md) and [**WM\_VSCROLL**](wm-vscroll.md), provide only 16 bits of position data.</span></span> <span data-ttu-id="54c5d-134">Однако структура [**скроллинфо**](/windows/win32/api/winuser/ns-winuser-scrollinfo) , используемая **СБМ \_ жетскроллинфо**, [**СБМ \_ сетскроллинфо**](sbm-setscrollinfo.md), [**жетскроллинфо**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)и [**сетскроллинфо**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) , предоставляет 32 бит для расположения данных в полосе прокрутки.</span><span class="sxs-lookup"><span data-stu-id="54c5d-134">However, the [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) structure used by **SBM\_GETSCROLLINFO**, [**SBM\_SETSCROLLINFO**](sbm-setscrollinfo.md), [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo), and [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) provides 32 bits of scroll bar position data.</span></span> <span data-ttu-id="54c5d-135">Эти сообщения и функции можно использовать при обработке сообщений **WM \_ HSCROLL** или **WM \_ VSCROLL** для получения данных о положении полосы прокрутки 32 бит.</span><span class="sxs-lookup"><span data-stu-id="54c5d-135">You can use these messages and functions while processing either the **WM\_HSCROLL** or **WM\_VSCROLL** messages to obtain 32-bit scroll bar position data.</span></span>

<span data-ttu-id="54c5d-136">Чтобы получить 32-разрядную точку прокрутки (Thumb) во время выполнения \_ кода запроса SB сумбтракк [**\_ HSCROLL**](wm-hscroll.md) или [**WM \_ VSCROLL**](wm-vscroll.md) , отправьте **СБМ \_ жетскроллинфо** со \_ значением SIF траккпос в **фмаск** -члене структуры [**скроллинфо**](/windows/win32/api/winuser/ns-winuser-scrollinfo) .</span><span class="sxs-lookup"><span data-stu-id="54c5d-136">To get the 32-bit position of the scroll box (thumb) during a SB\_THUMBTRACK request code in a [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) message, send **SBM\_GETSCROLLINFO** with the SIF\_TRACKPOS value in the **fMask** member of the [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) structure.</span></span> <span data-ttu-id="54c5d-137">Сообщение возвращает точку отслеживания ползунка в элементе **нтраккпос** структуры **скроллинфо** .</span><span class="sxs-lookup"><span data-stu-id="54c5d-137">The message returns the tracking position of the scroll box in the **nTrackPos** member of the **SCROLLINFO** structure.</span></span> <span data-ttu-id="54c5d-138">Это позволяет получить расположение поля прокрутки при его перемещении пользователем.</span><span class="sxs-lookup"><span data-stu-id="54c5d-138">This allows you to get the position of the scroll box as the user moves it.</span></span> <span data-ttu-id="54c5d-139">Кроме того, можно использовать функцию [**жетскроллинфо**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) для получения той же информации.</span><span class="sxs-lookup"><span data-stu-id="54c5d-139">Alternatively, you can use the [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) function to get the same information.</span></span>

## <a name="requirements"></a><span data-ttu-id="54c5d-140">Требования</span><span class="sxs-lookup"><span data-stu-id="54c5d-140">Requirements</span></span>



| <span data-ttu-id="54c5d-141">Требование</span><span class="sxs-lookup"><span data-stu-id="54c5d-141">Requirement</span></span> | <span data-ttu-id="54c5d-142">Значение</span><span class="sxs-lookup"><span data-stu-id="54c5d-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54c5d-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="54c5d-143">Minimum supported client</span></span><br/> | <span data-ttu-id="54c5d-144">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="54c5d-144">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="54c5d-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="54c5d-145">Minimum supported server</span></span><br/> | <span data-ttu-id="54c5d-146">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="54c5d-146">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="54c5d-147">Header</span><span class="sxs-lookup"><span data-stu-id="54c5d-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="54c5d-148"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="54c5d-148"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54c5d-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="54c5d-149">See also</span></span>

<dl> <dt>

<span data-ttu-id="54c5d-150">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="54c5d-150">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="54c5d-151">**жетскроллинфо**</span><span class="sxs-lookup"><span data-stu-id="54c5d-151">**GetScrollInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)
</dt> <dt>

[<span data-ttu-id="54c5d-152">**СБМ \_ сетскроллинфо**</span><span class="sxs-lookup"><span data-stu-id="54c5d-152">**SBM\_SETSCROLLINFO**</span></span>](sbm-setscrollinfo.md)
</dt> <dt>

[<span data-ttu-id="54c5d-153">**скроллинфо**</span><span class="sxs-lookup"><span data-stu-id="54c5d-153">**SCROLLINFO**</span></span>](/windows/win32/api/winuser/ns-winuser-scrollinfo)
</dt> <dt>

[<span data-ttu-id="54c5d-154">**сетскроллинфо**</span><span class="sxs-lookup"><span data-stu-id="54c5d-154">**SetScrollInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)
</dt> </dl>

 


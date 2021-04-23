---
title: Сообщение SBM_SETSCROLLINFO (Winuser. h)
description: Сообщение СБМ \_ сетскроллинфо отправляется для установки параметров полосы прокрутки.
ms.assetid: e0e42a81-67be-4d40-88c8-77398b068617
keywords:
- Элементы управления Windows для SBM_SETSCROLLINFO сообщений
topic_type:
- apiref
api_name:
- SBM_SETSCROLLINFO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e98abbca2d53d4b104caea22954472a17dfd5c1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654603"
---
# <a name="sbm_setscrollinfo-message"></a><span data-ttu-id="1e412-104">\_Сообщение СБМ сетскроллинфо</span><span class="sxs-lookup"><span data-stu-id="1e412-104">SBM\_SETSCROLLINFO message</span></span>

<span data-ttu-id="1e412-105">Сообщение **СБМ \_ сетскроллинфо** отправляется для установки параметров полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="1e412-105">The **SBM\_SETSCROLLINFO** message is sent to set the parameters of a scroll bar.</span></span>

<span data-ttu-id="1e412-106">Приложения не должны отсылать это сообщение напрямую.</span><span class="sxs-lookup"><span data-stu-id="1e412-106">Applications should not send this message directly.</span></span> <span data-ttu-id="1e412-107">Вместо этого они должны использовать функцию [**сетскроллинфо**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) .</span><span class="sxs-lookup"><span data-stu-id="1e412-107">Instead, they should use the [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) function.</span></span> <span data-ttu-id="1e412-108">Окно получает это сообщение через функцию [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="1e412-108">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span> <span data-ttu-id="1e412-109">Приложения, которые реализуют пользовательский элемент управления "полоса прокрутки", должны отвечать на эти сообщения, чтобы функция **сетскроллинфо** работала правильно.</span><span class="sxs-lookup"><span data-stu-id="1e412-109">Applications which implement a custom scroll bar control must respond to these messages for the **SetScrollInfo** function to function properly.</span></span>

## <a name="parameters"></a><span data-ttu-id="1e412-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="1e412-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e412-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1e412-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1e412-112">Указывает, перерисовывается ли полоса прокрутки для отражения новой позицией ползунка.</span><span class="sxs-lookup"><span data-stu-id="1e412-112">Specifies whether the scroll bar is redrawn to reflect the new scroll box position.</span></span> <span data-ttu-id="1e412-113">Если этот параметр имеет **значение true**, полоса прокрутки перерисовывается.</span><span class="sxs-lookup"><span data-stu-id="1e412-113">If this parameter is **TRUE**, the scroll bar is redrawn.</span></span> <span data-ttu-id="1e412-114">Если значение равно **false**, полоса прокрутки не перерисовывается.</span><span class="sxs-lookup"><span data-stu-id="1e412-114">If it is **FALSE**, the scroll bar is not redrawn.</span></span>

</dd> <dt>

<span data-ttu-id="1e412-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1e412-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1e412-116">Указатель на структуру [**скроллинфо**](/windows/win32/api/winuser/ns-winuser-scrollinfo) .</span><span class="sxs-lookup"><span data-stu-id="1e412-116">Pointer to a [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) structure.</span></span> <span data-ttu-id="1e412-117">Перед вызовом [**сетскроллинфо**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)задайте для элемента **кбсизе** структуры значение **sizeof**(**скроллинфо**), установите элемент **фмаск** , чтобы указать заданные параметры, и укажите новые значения параметров в соответствующих элементах.</span><span class="sxs-lookup"><span data-stu-id="1e412-117">Before calling [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo), set the **cbSize** member of the structure to **sizeof**(**SCROLLINFO**), set the **fMask** member to indicate the parameters to set, and specify the new parameter values in the appropriate members.</span></span>

<span data-ttu-id="1e412-118">Элемент **фмаск** может иметь одно или несколько из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="1e412-118">The **fMask** member can be one or more of the following values.</span></span>



| <span data-ttu-id="1e412-119">Значение</span><span class="sxs-lookup"><span data-stu-id="1e412-119">Value</span></span>                                                                                                                                                                           | <span data-ttu-id="1e412-120">Значение</span><span class="sxs-lookup"><span data-stu-id="1e412-120">Meaning</span></span>                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span id="SIF_DISABLENOSCROLL"></span><span id="sif_disablenoscroll"></span><dl> <span data-ttu-id="1e412-121"><dt>**SIF \_ дисабленоскролл**</dt></span><span class="sxs-lookup"><span data-stu-id="1e412-121"><dt>**SIF\_DISABLENOSCROLL**</dt></span></span> </dl> | <span data-ttu-id="1e412-122">Отключает полосу прокрутки вместо ее удаления, если новые параметры полосы прокрутки сделают полосу прокрутки ненужной.</span><span class="sxs-lookup"><span data-stu-id="1e412-122">Disables the scroll bar instead of removing it, if the scroll bar's new parameters make the scroll bar unnecessary.</span></span><br/> |
| <span id="SIF_PAGE"></span><span id="sif_page"></span><dl> <span data-ttu-id="1e412-123"><dt>**\_страница SIF**</dt></span><span class="sxs-lookup"><span data-stu-id="1e412-123"><dt>**SIF\_PAGE**</dt></span></span> </dl>                                  | <span data-ttu-id="1e412-124">Задает для страницы прокрутки значение, указанное в элементе **нпаже** .</span><span class="sxs-lookup"><span data-stu-id="1e412-124">Sets the scroll page to the value specified in the **nPage** member.</span></span><br/>                                                |
| <span id="SIF_POS"></span><span id="sif_pos"></span><dl> <span data-ttu-id="1e412-125"><dt>**SIF \_ POS**</dt></span><span class="sxs-lookup"><span data-stu-id="1e412-125"><dt>**SIF\_POS**</dt></span></span> </dl>                                     | <span data-ttu-id="1e412-126">Задает в качестве расположения прокрутки значение, указанное в элементе **npos** .</span><span class="sxs-lookup"><span data-stu-id="1e412-126">Sets the scroll position to the value specified in the **nPos** member.</span></span> <br/>                                            |
| <span id="SIF_RANGE"></span><span id="sif_range"></span><dl> <span data-ttu-id="1e412-127"><dt>**\_диапазон SIF**</dt></span><span class="sxs-lookup"><span data-stu-id="1e412-127"><dt>**SIF\_RANGE**</dt></span></span> </dl>                               | <span data-ttu-id="1e412-128">Задает для диапазона прокрутки значение, указанное в элементах **nмин.** и **nмакс.** .</span><span class="sxs-lookup"><span data-stu-id="1e412-128">Sets the scroll range to the value specified in the **nMin** and **nMax** members.</span></span> <br/>                                 |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e412-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1e412-129">Return value</span></span>

<span data-ttu-id="1e412-130">Возвращаемое значение является текущей позицией ползунка.</span><span class="sxs-lookup"><span data-stu-id="1e412-130">The return value is the current position of the scroll box.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e412-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1e412-131">Remarks</span></span>

<span data-ttu-id="1e412-132">Сообщения, указывающие расположение полосы прокрутки, [**WM \_ HSCROLL**](wm-hscroll.md) и [**WM \_ VSCROLL**](wm-vscroll.md), содержат только 16 бит данных о положении.</span><span class="sxs-lookup"><span data-stu-id="1e412-132">The messages that indicate scroll bar position, [**WM\_HSCROLL**](wm-hscroll.md) and [**WM\_VSCROLL**](wm-vscroll.md), provide only 16 bits of position data.</span></span> <span data-ttu-id="1e412-133">Однако структура [**скроллинфо**](/windows/win32/api/winuser/ns-winuser-scrollinfo) , используемая [**СБМ \_ жетскроллинфо**](sbm-getscrollinfo.md), **СБМ \_ сетскроллинфо**, [**жетскроллинфо**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)и [**сетскроллинфо**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) , предоставляет 32 бит для расположения данных в полосе прокрутки.</span><span class="sxs-lookup"><span data-stu-id="1e412-133">However, the [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) structure used by [**SBM\_GETSCROLLINFO**](sbm-getscrollinfo.md), **SBM\_SETSCROLLINFO**, [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo), and [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) provides 32 bits of scroll bar position data.</span></span> <span data-ttu-id="1e412-134">Эти сообщения и функции можно использовать при обработке сообщений **WM \_ HSCROLL** или **WM \_ VSCROLL** для получения данных о положении полосы прокрутки 32 бит.</span><span class="sxs-lookup"><span data-stu-id="1e412-134">You can use these messages and functions while processing either the **WM\_HSCROLL** or **WM\_VSCROLL** messages to obtain 32-bit scroll bar position data.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e412-135">Требования</span><span class="sxs-lookup"><span data-stu-id="1e412-135">Requirements</span></span>



| <span data-ttu-id="1e412-136">Требование</span><span class="sxs-lookup"><span data-stu-id="1e412-136">Requirement</span></span> | <span data-ttu-id="1e412-137">Значение</span><span class="sxs-lookup"><span data-stu-id="1e412-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e412-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1e412-138">Minimum supported client</span></span><br/> | <span data-ttu-id="1e412-139">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1e412-139">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1e412-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1e412-140">Minimum supported server</span></span><br/> | <span data-ttu-id="1e412-141">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1e412-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1e412-142">Header</span><span class="sxs-lookup"><span data-stu-id="1e412-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e412-143"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1e412-143"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e412-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1e412-144">See also</span></span>

<dl> <dt>

<span data-ttu-id="1e412-145">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="1e412-145">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1e412-146">**жетскроллинфо**</span><span class="sxs-lookup"><span data-stu-id="1e412-146">**GetScrollInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)
</dt> <dt>

[<span data-ttu-id="1e412-147">**СБМ \_ жетскроллинфо**</span><span class="sxs-lookup"><span data-stu-id="1e412-147">**SBM\_GETSCROLLINFO**</span></span>](sbm-getscrollinfo.md)
</dt> <dt>

[<span data-ttu-id="1e412-148">**скроллинфо**</span><span class="sxs-lookup"><span data-stu-id="1e412-148">**SCROLLINFO**</span></span>](/windows/win32/api/winuser/ns-winuser-scrollinfo)
</dt> <dt>

[<span data-ttu-id="1e412-149">**сетскроллинфо**</span><span class="sxs-lookup"><span data-stu-id="1e412-149">**SetScrollInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)
</dt> </dl>

 


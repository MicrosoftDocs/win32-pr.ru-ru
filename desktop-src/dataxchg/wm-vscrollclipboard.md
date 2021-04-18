---
title: Сообщение WM_VSCROLLCLIPBOARD (Winuser. h)
description: Посылается владельцу буфера обмена в окне средства просмотра буфера обмена, когда в буфере обмена содержатся данные в \_ формате CF овнердисплай, а в вертикальной полосе прокрутки появляется событие.
ms.assetid: 17bd32c4-1b07-42b7-b269-f517e3ec13f3
keywords:
- Обмен данными с сообщениями WM_VSCROLLCLIPBOARD
topic_type:
- apiref
api_name:
- WM_VSCROLLCLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87a9e80aa342065ee88c8e1d7aa44c1fd598e411
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491067"
---
# <a name="wm_vscrollclipboard-message"></a><span data-ttu-id="e43ac-104">\_Сообщение ВСКРОЛЛКЛИПБОАРД WM</span><span class="sxs-lookup"><span data-stu-id="e43ac-104">WM\_VSCROLLCLIPBOARD message</span></span>

<span data-ttu-id="e43ac-105">Посылается владельцу буфера обмена в окне средства просмотра буфера обмена, когда в буфере обмена содержатся данные в формате [**CF \_ овнердисплай**](standard-clipboard-formats.md) , а в вертикальной полосе прокрутки появляется событие.</span><span class="sxs-lookup"><span data-stu-id="e43ac-105">Sent to the clipboard owner by a clipboard viewer window when the clipboard contains data in the [**CF\_OWNERDISPLAY**](standard-clipboard-formats.md) format and an event occurs in the clipboard viewer's vertical scroll bar.</span></span> <span data-ttu-id="e43ac-106">Владелец должен прокручивать изображение в буфере обмена и обновлять значения полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="e43ac-106">The owner should scroll the clipboard image and update the scroll bar values.</span></span>


```C++
#define WM_VSCROLLCLIPBOARD             0x030A
```



## <a name="parameters"></a><span data-ttu-id="e43ac-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="e43ac-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e43ac-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e43ac-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e43ac-109">Маркер окна средства просмотра буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="e43ac-109">A handle to the clipboard viewer window.</span></span>

</dd> <dt>

<span data-ttu-id="e43ac-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e43ac-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e43ac-111">Слово *lParam* в низком порядке указывает на событие полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="e43ac-111">The low-order word of *lParam* specifies a scroll bar event.</span></span> <span data-ttu-id="e43ac-112">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="e43ac-112">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="e43ac-113">Значение</span><span class="sxs-lookup"><span data-stu-id="e43ac-113">Value</span></span>                                                                                                                                                                                                                         | <span data-ttu-id="e43ac-114">Значение</span><span class="sxs-lookup"><span data-stu-id="e43ac-114">Meaning</span></span>                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="SB_BOTTOM"></span><span id="sb_bottom"></span><dl> <span data-ttu-id="e43ac-115"><dt>**SB \_ 7 НИЖНИх**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="e43ac-115"><dt>**SB\_BOTTOM**</dt> <dt>7</dt></span></span> </dl>                      | <span data-ttu-id="e43ac-116">Прокрутите вниз вправо.</span><span class="sxs-lookup"><span data-stu-id="e43ac-116">Scroll to lower right.</span></span><br/>                                                                 |
| <span id="SB_ENDSCROLL"></span><span id="sb_endscroll"></span><dl> <span data-ttu-id="e43ac-117"><dt>**SB \_ ЕНДСКРОЛЛ**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="e43ac-117"><dt>**SB\_ENDSCROLL**</dt> <dt>8</dt></span></span> </dl>             | <span data-ttu-id="e43ac-118">Завершить прокрутку.</span><span class="sxs-lookup"><span data-stu-id="e43ac-118">End scroll.</span></span><br/>                                                                            |
| <span id="SB_LINEDOWN"></span><span id="sb_linedown"></span><dl> <span data-ttu-id="e43ac-119"><dt>**SB \_ ЛИНЕДОВН**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e43ac-119"><dt>**SB\_LINEDOWN**</dt> <dt>1</dt></span></span> </dl>                | <span data-ttu-id="e43ac-120">Прокрутить на одну строку вниз.</span><span class="sxs-lookup"><span data-stu-id="e43ac-120">Scroll one line down.</span></span><br/>                                                                  |
| <span id="SB_LINEUP"></span><span id="sb_lineup"></span><dl> <span data-ttu-id="e43ac-121"><dt>**SB \_**</dt>Отметка <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e43ac-121"><dt>**SB\_LINEUP**</dt> <dt>0</dt></span></span> </dl>                      | <span data-ttu-id="e43ac-122">Прокрутить на одну строку вверх.</span><span class="sxs-lookup"><span data-stu-id="e43ac-122">Scroll one line up.</span></span><br/>                                                                    |
| <span id="SB_PAGEDOWN"></span><span id="sb_pagedown"></span><dl> <span data-ttu-id="e43ac-123"><dt>**SB \_ PAGEDOWN**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="e43ac-123"><dt>**SB\_PAGEDOWN**</dt> <dt>3</dt></span></span> </dl>                | <span data-ttu-id="e43ac-124">Прокрутить на одну страницу вниз.</span><span class="sxs-lookup"><span data-stu-id="e43ac-124">Scroll one page down.</span></span><br/>                                                                  |
| <span id="SB_PAGEUP"></span><span id="sb_pageup"></span><dl> <span data-ttu-id="e43ac-125"><dt>**SB \_ PAGEUP**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e43ac-125"><dt>**SB\_PAGEUP**</dt> <dt>2</dt></span></span> </dl>                      | <span data-ttu-id="e43ac-126">Прокрутка на одну страницу вверх.</span><span class="sxs-lookup"><span data-stu-id="e43ac-126">Scroll one page up.</span></span><br/>                                                                    |
| <span id="SB_THUMBPOSITION"></span><span id="sb_thumbposition"></span><dl> <span data-ttu-id="e43ac-127"><dt>**SB \_ СУМБПОСИТИОН**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="e43ac-127"><dt>**SB\_THUMBPOSITION**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="e43ac-128">Прокрутить к абсолютному положению.</span><span class="sxs-lookup"><span data-stu-id="e43ac-128">Scroll to absolute position.</span></span> <span data-ttu-id="e43ac-129">Текущая позицией задается в виде слова в высоком порядке.</span><span class="sxs-lookup"><span data-stu-id="e43ac-129">The current position is specified by the high-order word.</span></span><br/> |
| <span id="SB_TOP"></span><span id="sb_top"></span><dl> <span data-ttu-id="e43ac-130"><dt>**SB \_ Первые**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="e43ac-130"><dt>**SB\_TOP**</dt> <dt>6</dt></span></span> </dl>                               | <span data-ttu-id="e43ac-131">Прокрутить к верхнему левому краю.</span><span class="sxs-lookup"><span data-stu-id="e43ac-131">Scroll to upper left.</span></span><br/>                                                                  |



 

<span data-ttu-id="e43ac-132">Слово *lParam* с высоким приоритетом задает текущую точку прокрутки, если неупорядоченное слово *lParam* является **SB \_ сумбпоситион**; в противном случае не используется слово с высоким порядком *lParam* .</span><span class="sxs-lookup"><span data-stu-id="e43ac-132">The high-order word of *lParam* specifies the current position of the scroll box if the low-order word of *lParam* is **SB\_THUMBPOSITION**; otherwise, the high-order word of *lParam* is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e43ac-133">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e43ac-133">Return value</span></span>

<span data-ttu-id="e43ac-134">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="e43ac-134">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="e43ac-135">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e43ac-135">Remarks</span></span>

<span data-ttu-id="e43ac-136">Владелец буфера обмена может использовать функцию [**скроллвиндов**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx) для прокрутки изображения в окне средства просмотра буфера обмена и сделать недействительным соответствующий регион.</span><span class="sxs-lookup"><span data-stu-id="e43ac-136">The clipboard owner can use the [**ScrollWindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx) function to scroll the image in the clipboard viewer window and invalidate the appropriate region.</span></span>

## <a name="requirements"></a><span data-ttu-id="e43ac-137">Требования</span><span class="sxs-lookup"><span data-stu-id="e43ac-137">Requirements</span></span>



| <span data-ttu-id="e43ac-138">Требование</span><span class="sxs-lookup"><span data-stu-id="e43ac-138">Requirement</span></span> | <span data-ttu-id="e43ac-139">Значение</span><span class="sxs-lookup"><span data-stu-id="e43ac-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e43ac-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e43ac-140">Minimum supported client</span></span><br/> | <span data-ttu-id="e43ac-141">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e43ac-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e43ac-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e43ac-142">Minimum supported server</span></span><br/> | <span data-ttu-id="e43ac-143">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e43ac-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e43ac-144">Заголовок</span><span class="sxs-lookup"><span data-stu-id="e43ac-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="e43ac-145"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e43ac-145"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e43ac-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e43ac-146">See also</span></span>

<dl> <dt>

<span data-ttu-id="e43ac-147">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="e43ac-147">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="e43ac-148">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e43ac-148">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="e43ac-149">[**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e43ac-149">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="e43ac-150">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="e43ac-150">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e43ac-151">Буфер обмена</span><span class="sxs-lookup"><span data-stu-id="e43ac-151">Clipboard</span></span>](clipboard.md)
</dt> <dt>

<span data-ttu-id="e43ac-152">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="e43ac-152">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="e43ac-153">[**скроллвиндов**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx)</span><span class="sxs-lookup"><span data-stu-id="e43ac-153">[**ScrollWindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx)</span></span>
</dt> </dl>

 


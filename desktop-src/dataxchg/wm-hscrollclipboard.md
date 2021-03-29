---
title: Сообщение WM_HSCROLLCLIPBOARD (Winuser. h)
description: Отправляется в окно просмотра владельцу буфера обмена.
ms.assetid: 73558de6-a822-40f7-9eb2-47ea5afd4e6e
keywords:
- Обмен данными с сообщениями WM_HSCROLLCLIPBOARD
topic_type:
- apiref
api_name:
- WM_HSCROLLCLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a34ee33709601b483258ae0aec4873c47fa69a00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492195"
---
# <a name="wm_hscrollclipboard-message"></a><span data-ttu-id="e5744-104">\_Сообщение ХСКРОЛЛКЛИПБОАРД WM</span><span class="sxs-lookup"><span data-stu-id="e5744-104">WM\_HSCROLLCLIPBOARD message</span></span>

<span data-ttu-id="e5744-105">Отправляется в окно просмотра владельцу буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="e5744-105">Sent to the clipboard owner by a clipboard viewer window.</span></span> <span data-ttu-id="e5744-106">Это происходит, когда буфер обмена содержит данные в формате [**CF \_ овнердисплай**](standard-clipboard-formats.md) и событие возникает в горизонтальной полосе прокрутки окна буфера просмотра.</span><span class="sxs-lookup"><span data-stu-id="e5744-106">This occurs when the clipboard contains data in the [**CF\_OWNERDISPLAY**](standard-clipboard-formats.md) format and an event occurs in the clipboard viewer's horizontal scroll bar.</span></span> <span data-ttu-id="e5744-107">Владелец должен прокручивать изображение в буфере обмена и обновлять значения полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="e5744-107">The owner should scroll the clipboard image and update the scroll bar values.</span></span>


```C++
#define WM_HSCROLLCLIPBOARD             0x030E
```



## <a name="parameters"></a><span data-ttu-id="e5744-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e5744-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5744-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e5744-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e5744-110">Маркер окна средства просмотра буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="e5744-110">A handle to the clipboard viewer window.</span></span>

</dd> <dt>

<span data-ttu-id="e5744-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e5744-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e5744-112">Слово *lParam* в низком порядке указывает на событие полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="e5744-112">The low-order word of *lParam* specifies a scroll bar event.</span></span> <span data-ttu-id="e5744-113">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="e5744-113">This parameter can be one of the following values.</span></span> <span data-ttu-id="e5744-114">Слово *lParam* в высоком порядке задает текущую точку прокрутки, если неупорядоченное слово *lParam* является **SB \_ сумбпоситион**; в противном случае слово с высоким порядком не используется.</span><span class="sxs-lookup"><span data-stu-id="e5744-114">The high-order word of *lParam* specifies the current position of the scroll box if the low-order word of *lParam* is **SB\_THUMBPOSITION**; otherwise, the high-order word is not used.</span></span>



| <span data-ttu-id="e5744-115">Значение</span><span class="sxs-lookup"><span data-stu-id="e5744-115">Value</span></span>                                                                                                                                                                                                                         | <span data-ttu-id="e5744-116">Значение</span><span class="sxs-lookup"><span data-stu-id="e5744-116">Meaning</span></span>                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="SB_ENDSCROLL"></span><span id="sb_endscroll"></span><dl> <span data-ttu-id="e5744-117"><dt>**SB \_ ЕНДСКРОЛЛ**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="e5744-117"><dt>**SB\_ENDSCROLL**</dt> <dt>8</dt></span></span> </dl>             | <span data-ttu-id="e5744-118">Завершить прокрутку.</span><span class="sxs-lookup"><span data-stu-id="e5744-118">End scroll.</span></span><br/>                                                                            |
| <span id="SB_LEFT"></span><span id="sb_left"></span><dl> <span data-ttu-id="e5744-119"><dt>**SB \_ СЛЕВА**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="e5744-119"><dt>**SB\_LEFT**</dt> <dt>6</dt></span></span> </dl>                            | <span data-ttu-id="e5744-120">Прокрутить к верхнему левому краю.</span><span class="sxs-lookup"><span data-stu-id="e5744-120">Scroll to upper left.</span></span><br/>                                                                  |
| <span id="SB_RIGHT"></span><span id="sb_right"></span><dl> <span data-ttu-id="e5744-121"><dt>**SB \_ СПРАВА**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="e5744-121"><dt>**SB\_RIGHT**</dt> <dt>7</dt></span></span> </dl>                         | <span data-ttu-id="e5744-122">Прокрутите вниз вправо.</span><span class="sxs-lookup"><span data-stu-id="e5744-122">Scroll to lower right.</span></span><br/>                                                                 |
| <span id="SB_LINELEFT"></span><span id="sb_lineleft"></span><dl> <span data-ttu-id="e5744-123"><dt>**SB \_ ЛИНЕЛЕФТ**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e5744-123"><dt>**SB\_LINELEFT**</dt> <dt>0</dt></span></span> </dl>                | <span data-ttu-id="e5744-124">Прокрутка влево на одну единицу.</span><span class="sxs-lookup"><span data-stu-id="e5744-124">Scrolls left by one unit.</span></span><br/>                                                              |
| <span id="SB_LINERIGHT"></span><span id="sb_lineright"></span><dl> <span data-ttu-id="e5744-125"><dt>**SB \_ ЛИНЕРИГХТ**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e5744-125"><dt>**SB\_LINERIGHT**</dt> <dt>1</dt></span></span> </dl>             | <span data-ttu-id="e5744-126">Выполняет прокрутку вправо на одну единицу.</span><span class="sxs-lookup"><span data-stu-id="e5744-126">Scrolls right by one unit.</span></span><br/>                                                             |
| <span id="SB_PAGELEFT"></span><span id="sb_pageleft"></span><dl> <span data-ttu-id="e5744-127"><dt>**SB \_ ПАЖЕЛЕФТ**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e5744-127"><dt>**SB\_PAGELEFT**</dt> <dt>2</dt></span></span> </dl>                | <span data-ttu-id="e5744-128">Прокрутка влево по ширине окна.</span><span class="sxs-lookup"><span data-stu-id="e5744-128">Scrolls left by the width of the window.</span></span><br/>                                               |
| <span id="SB_PAGERIGHT"></span><span id="sb_pageright"></span><dl> <span data-ttu-id="e5744-129"><dt>**SB \_ ПАЖЕРИГХТ**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="e5744-129"><dt>**SB\_PAGERIGHT**</dt> <dt>3</dt></span></span> </dl>             | <span data-ttu-id="e5744-130">Прокрутка вправо по ширине окна.</span><span class="sxs-lookup"><span data-stu-id="e5744-130">Scrolls right by the width of the window.</span></span><br/>                                              |
| <span id="SB_THUMBPOSITION"></span><span id="sb_thumbposition"></span><dl> <span data-ttu-id="e5744-131"><dt>**SB \_ СУМБПОСИТИОН**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="e5744-131"><dt>**SB\_THUMBPOSITION**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="e5744-132">Прокрутить к абсолютному положению.</span><span class="sxs-lookup"><span data-stu-id="e5744-132">Scroll to absolute position.</span></span> <span data-ttu-id="e5744-133">Текущая позицией задается в виде слова в высоком порядке.</span><span class="sxs-lookup"><span data-stu-id="e5744-133">The current position is specified by the high-order word.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5744-134">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e5744-134">Return value</span></span>

<span data-ttu-id="e5744-135">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="e5744-135">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5744-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e5744-136">Remarks</span></span>

<span data-ttu-id="e5744-137">Владелец буфера обмена может использовать функцию [**скроллвиндов**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx) для прокрутки изображения в окне средства просмотра буфера обмена и сделать недействительным соответствующий регион.</span><span class="sxs-lookup"><span data-stu-id="e5744-137">The clipboard owner can use the [**ScrollWindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx) function to scroll the image in the clipboard viewer window and invalidate the appropriate region.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5744-138">Требования</span><span class="sxs-lookup"><span data-stu-id="e5744-138">Requirements</span></span>



| <span data-ttu-id="e5744-139">Требование</span><span class="sxs-lookup"><span data-stu-id="e5744-139">Requirement</span></span> | <span data-ttu-id="e5744-140">Значение</span><span class="sxs-lookup"><span data-stu-id="e5744-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5744-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e5744-141">Minimum supported client</span></span><br/> | <span data-ttu-id="e5744-142">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e5744-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e5744-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e5744-143">Minimum supported server</span></span><br/> | <span data-ttu-id="e5744-144">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e5744-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e5744-145">Заголовок</span><span class="sxs-lookup"><span data-stu-id="e5744-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5744-146"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e5744-146"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5744-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e5744-147">See also</span></span>

<dl> <dt>

<span data-ttu-id="e5744-148">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="e5744-148">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="e5744-149">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e5744-149">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="e5744-150">[**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e5744-150">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="e5744-151">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="e5744-151">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e5744-152">Буфер обмена</span><span class="sxs-lookup"><span data-stu-id="e5744-152">Clipboard</span></span>](clipboard.md)
</dt> <dt>

<span data-ttu-id="e5744-153">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="e5744-153">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="e5744-154">[**скроллвиндов**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx)</span><span class="sxs-lookup"><span data-stu-id="e5744-154">[**ScrollWindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx)</span></span>
</dt> </dl>

 


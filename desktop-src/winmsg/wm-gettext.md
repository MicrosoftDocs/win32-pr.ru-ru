---
description: Копирует текст, соответствующий окну, в буфер, предоставленный вызывающим объектом.
ms.assetid: 117c3d6d-24cd-462f-bdb0-b65d8914273a
title: Сообщение WM_GETTEXT (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47f8e2268c1d0ec043e24a001f16abae357bdbdc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815456"
---
# <a name="wm_gettext-message"></a><span data-ttu-id="51c1c-103">\_Сообщение WM gettext</span><span class="sxs-lookup"><span data-stu-id="51c1c-103">WM\_GETTEXT message</span></span>

<span data-ttu-id="51c1c-104">Копирует текст, соответствующий окну, в буфер, предоставленный вызывающим объектом.</span><span class="sxs-lookup"><span data-stu-id="51c1c-104">Copies the text that corresponds to a window into a buffer provided by the caller.</span></span>


```C++
#define WM_GETTEXT                      0x000D
```



## <a name="parameters"></a><span data-ttu-id="51c1c-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="51c1c-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51c1c-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="51c1c-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="51c1c-107">Максимальное число копируемых символов, включая завершающий символ null.</span><span class="sxs-lookup"><span data-stu-id="51c1c-107">The maximum number of characters to be copied, including the terminating null character.</span></span>

<span data-ttu-id="51c1c-108">Приложения ANSI могут уменьшить размер строки в буфере (до минимума половины значения параметра *wParam* ) из-за преобразования из ANSI в Юникод.</span><span class="sxs-lookup"><span data-stu-id="51c1c-108">ANSI applications may have the string in the buffer reduced in size (to a minimum of half that of the *wParam* value) due to conversion from ANSI to Unicode.</span></span>

</dd> <dt>

<span data-ttu-id="51c1c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="51c1c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="51c1c-110">Указатель на буфер, который должен получить текст.</span><span class="sxs-lookup"><span data-stu-id="51c1c-110">A pointer to the buffer that is to receive the text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51c1c-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="51c1c-111">Return value</span></span>

<span data-ttu-id="51c1c-112">Тип: **lResult**</span><span class="sxs-lookup"><span data-stu-id="51c1c-112">Type: **LRESULT**</span></span>

<span data-ttu-id="51c1c-113">Возвращаемое значение — это число скопированных символов, не включая завершающий нуль-символ.</span><span class="sxs-lookup"><span data-stu-id="51c1c-113">The return value is the number of characters copied, not including the terminating null character.</span></span>

## <a name="remarks"></a><span data-ttu-id="51c1c-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="51c1c-114">Remarks</span></span>

<span data-ttu-id="51c1c-115">Функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) копирует текст, связанный с окном, в указанный буфер и возвращает число скопированных символов.</span><span class="sxs-lookup"><span data-stu-id="51c1c-115">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function copies the text associated with the window into the specified buffer and returns the number of characters copied.</span></span> <span data-ttu-id="51c1c-116">Обратите внимание, что для статических элементов управления, не являющихся текстовыми, это позволяет получить текст, с которым был создан элемент управления, т. е. ИДЕНТИФИКАЦИОНный номер.</span><span class="sxs-lookup"><span data-stu-id="51c1c-116">Note, for non-text static controls this gives you the text with which the control was originally created, that is, the ID number.</span></span> <span data-ttu-id="51c1c-117">Тем не менее, он предоставляет идентификатор нетекстового статического элемента управления, как он был создан изначально.</span><span class="sxs-lookup"><span data-stu-id="51c1c-117">However, it gives you the ID of the non-text static control as originally created.</span></span> <span data-ttu-id="51c1c-118">Это значит, что если впоследствии вы использовали **STM- \_ сетимаже** для изменения его исходного идентификатора, он все равно будет возвращен.</span><span class="sxs-lookup"><span data-stu-id="51c1c-118">That is, if you subsequently used a **STM\_SETIMAGE** to change it the original ID would still be returned.</span></span>

<span data-ttu-id="51c1c-119">Для элемента управления "поле ввода" копируемый текст является содержимым элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="51c1c-119">For an edit control, the text to be copied is the content of the edit control.</span></span> <span data-ttu-id="51c1c-120">Для поля со списком текст — это содержимое части элемента управления Edit (или статического текста) поля со списком.</span><span class="sxs-lookup"><span data-stu-id="51c1c-120">For a combo box, the text is the content of the edit control (or static-text) portion of the combo box.</span></span> <span data-ttu-id="51c1c-121">Для кнопки текст — это имя кнопки.</span><span class="sxs-lookup"><span data-stu-id="51c1c-121">For a button, the text is the button name.</span></span> <span data-ttu-id="51c1c-122">Для других окон текст — это заголовок окна.</span><span class="sxs-lookup"><span data-stu-id="51c1c-122">For other windows, the text is the window title.</span></span> <span data-ttu-id="51c1c-123">Чтобы скопировать текст элемента в поле со списком, приложение может использовать сообщение [**фунтовой нагрузки \_**](../controls/lb-gettext.md) .</span><span class="sxs-lookup"><span data-stu-id="51c1c-123">To copy the text of an item in a list box, an application can use the [**LB\_GETTEXT**](../controls/lb-gettext.md) message.</span></span>

<span data-ttu-id="51c1c-124">Когда сообщение **WM \_ gettext** отправляется в статический элемент управления со стилем **\_ значка SS** , маркер значка будет возвращен в первых четырех байтах буфера, на которые указывает *lParam*.</span><span class="sxs-lookup"><span data-stu-id="51c1c-124">When the **WM\_GETTEXT** message is sent to a static control with the **SS\_ICON** style, a handle to the icon will be returned in the first four bytes of the buffer pointed to by *lParam*.</span></span> <span data-ttu-id="51c1c-125">Это справедливо только в том случае, если для задания значка использовалось сообщение [**WM \_ SETTEXT**](wm-settext.md) .</span><span class="sxs-lookup"><span data-stu-id="51c1c-125">This is true only if the [**WM\_SETTEXT**](wm-settext.md) message has been used to set the icon.</span></span>

<span data-ttu-id="51c1c-126">**Расширенное редактирование:** Если размер копируемого текста превышает 64 КБ, используйте сообщение " [**\_ поток EM**](../controls/em-streamout.md) или [**EM \_ жетселтекст**](../controls/em-getseltext.md) ".</span><span class="sxs-lookup"><span data-stu-id="51c1c-126">**Rich Edit:** If the text to be copied exceeds 64K, use either the [**EM\_STREAMOUT**](../controls/em-streamout.md) or [**EM\_GETSELTEXT**](../controls/em-getseltext.md) message.</span></span>

<span data-ttu-id="51c1c-127">Отправка сообщения **WM \_ gettext** в статический элемент управления, не являющийся текстовым, например статический точечный рисунок или элемент управления "статический значок", не возвращает строковое значение.</span><span class="sxs-lookup"><span data-stu-id="51c1c-127">Sending a **WM\_GETTEXT** message to a non-text static control, such as a static bitmap or static icon control, does not return a string value.</span></span> <span data-ttu-id="51c1c-128">Вместо этого он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="51c1c-128">Instead, it returns zero.</span></span> <span data-ttu-id="51c1c-129">Кроме того, в ранних версиях Windows приложения могли отправить сообщение **WM \_ gettext** в статический элемент управления, не являющийся текстовым, для получения идентификатора элемента управления.</span><span class="sxs-lookup"><span data-stu-id="51c1c-129">In addition, in early versions of Windows, applications could send a **WM\_GETTEXT** message to a non-text static control to retrieve the control's ID.</span></span> <span data-ttu-id="51c1c-130">Чтобы получить идентификатор элемента управления, приложения могут использовать [**жетвиндовлонг**](/windows/win32/api/winuser/nf-winuser-getwindowlonga) , передав **\_ идентификатор ГВЛ** в качестве значения индекса или [**жетвиндовлонгптр**](/windows/win32/api/winuser/nf-winuser-getwindowlongptra) с **помощью \_ идентификатора гвлп**.</span><span class="sxs-lookup"><span data-stu-id="51c1c-130">To retrieve a control's ID, applications can use [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga) passing **GWL\_ID** as the index value or [**GetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-getwindowlongptra) using **GWLP\_ID**.</span></span>

## <a name="requirements"></a><span data-ttu-id="51c1c-131">Требования</span><span class="sxs-lookup"><span data-stu-id="51c1c-131">Requirements</span></span>



| <span data-ttu-id="51c1c-132">Требование</span><span class="sxs-lookup"><span data-stu-id="51c1c-132">Requirement</span></span> | <span data-ttu-id="51c1c-133">Значение</span><span class="sxs-lookup"><span data-stu-id="51c1c-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51c1c-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="51c1c-134">Minimum supported client</span></span><br/> | <span data-ttu-id="51c1c-135">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="51c1c-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="51c1c-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="51c1c-136">Minimum supported server</span></span><br/> | <span data-ttu-id="51c1c-137">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="51c1c-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="51c1c-138">Заголовок</span><span class="sxs-lookup"><span data-stu-id="51c1c-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="51c1c-139"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="51c1c-139"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51c1c-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="51c1c-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="51c1c-141">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="51c1c-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="51c1c-142">**дефвиндовпрок**</span><span class="sxs-lookup"><span data-stu-id="51c1c-142">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="51c1c-143">**жетвиндовлонг**</span><span class="sxs-lookup"><span data-stu-id="51c1c-143">**GetWindowLong**</span></span>](/windows/win32/api/winuser/nf-winuser-getwindowlonga)
</dt> <dt>

[<span data-ttu-id="51c1c-144">**жетвиндовлонгптр**</span><span class="sxs-lookup"><span data-stu-id="51c1c-144">**GetWindowLongPtr**</span></span>](/windows/win32/api/winuser/nf-winuser-getwindowlongptra)
</dt> <dt>

[<span data-ttu-id="51c1c-145">**жетвиндовтекст**</span><span class="sxs-lookup"><span data-stu-id="51c1c-145">**GetWindowText**</span></span>](/windows/win32/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[<span data-ttu-id="51c1c-146">**жетвиндовтекстленгс**</span><span class="sxs-lookup"><span data-stu-id="51c1c-146">**GetWindowTextLength**</span></span>](/windows/win32/api/winuser/nf-winuser-getwindowtextlengtha)
</dt> <dt>

[<span data-ttu-id="51c1c-147">**WM \_ жеттекстленгс**</span><span class="sxs-lookup"><span data-stu-id="51c1c-147">**WM\_GETTEXTLENGTH**</span></span>](wm-gettextlength.md)
</dt> <dt>

[<span data-ttu-id="51c1c-148">**WM \_ SETTEXT**</span><span class="sxs-lookup"><span data-stu-id="51c1c-148">**WM\_SETTEXT**</span></span>](wm-settext.md)
</dt> <dt>

<span data-ttu-id="51c1c-149">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="51c1c-149">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="51c1c-150">Windows</span><span class="sxs-lookup"><span data-stu-id="51c1c-150">Windows</span></span>](windows.md)
</dt> <dt>

<span data-ttu-id="51c1c-151">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="51c1c-151">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="51c1c-152">**EM \_ жетселтекст**</span><span class="sxs-lookup"><span data-stu-id="51c1c-152">**EM\_GETSELTEXT**</span></span>](../controls/em-getseltext.md)
</dt> <dt>

[<span data-ttu-id="51c1c-153">**\_потоковая передача EM**</span><span class="sxs-lookup"><span data-stu-id="51c1c-153">**EM\_STREAMOUT**</span></span>](../controls/em-streamout.md)
</dt> <dt>

[<span data-ttu-id="51c1c-154">**\_Балансировка нагрузки**</span><span class="sxs-lookup"><span data-stu-id="51c1c-154">**LB\_GETTEXT**</span></span>](../controls/lb-gettext.md)
</dt> </dl>

 

 

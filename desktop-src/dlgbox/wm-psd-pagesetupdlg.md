---
title: Сообщение WM_PSD_PAGESETUPDLG (Коммдлг. h)
description: Уведомляет процедуру-обработчик Пажепаинсук о том, что диалоговое окно "Параметры страницы" собирается вывести содержимое образца страницы. Процедура-обработчик может использовать это сообщение для выполнения задач инициализации, связанных с рисованием содержимого образца страницы.
ms.assetid: 0d95240b-7d77-4819-8e5c-cc25cd1b30f2
keywords:
- WM_PSD_PAGESETUPDLG диалоговых окон сообщений
topic_type:
- apiref
api_name:
- WM_PSD_PAGESETUPDLG
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9706eff6d015dc31332d9f757c954081f0134b2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104416085"
---
# <a name="wm_psd_pagesetupdlg-message"></a><span data-ttu-id="a2452-105">\_Сообщение WM PSD \_ пажесетупдлг</span><span class="sxs-lookup"><span data-stu-id="a2452-105">WM\_PSD\_PAGESETUPDLG message</span></span>

<span data-ttu-id="a2452-106">Уведомляет процедуру-обработчик [**пажепаинсук**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) о том, что диалоговое окно " **Параметры страницы** " собирается вывести содержимое образца страницы.</span><span class="sxs-lookup"><span data-stu-id="a2452-106">Notifies a [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure that the **Page Setup** dialog box is about to draw the contents of the sample page.</span></span> <span data-ttu-id="a2452-107">Процедура-обработчик может использовать это сообщение для выполнения задач инициализации, связанных с рисованием содержимого образца страницы.</span><span class="sxs-lookup"><span data-stu-id="a2452-107">The hook procedure can use this message to carry out initialization tasks related to drawing the contents of the sample page.</span></span>


```C++
#define WM_USER                  0x0400
#define WM_PSD_PAGESETUPDLG     (WM_USER  )
```



## <a name="parameters"></a><span data-ttu-id="a2452-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a2452-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2452-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a2452-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a2452-110">Слово нижнего порядка задает значение, указывающее размер бумаги.</span><span class="sxs-lookup"><span data-stu-id="a2452-110">The low-order word specifies a value that indicates the paper size.</span></span> <span data-ttu-id="a2452-111">Это значение может быть одним из значений **дмпапер \_** , перечисленных в описании структуры.</span><span class="sxs-lookup"><span data-stu-id="a2452-111">This value can be one of the **DMPAPER\_** values listed in the description of the structure.</span></span> <span data-ttu-id="a2452-112">Слово в высоком порядке Указывает ориентацию бумаги или конверта, а также то, является ли принтер точечной матрицей или ориентации для HPPCLHPPCL (Hewlett Packard Control Language).</span><span class="sxs-lookup"><span data-stu-id="a2452-112">The high-order word specifies the orientation of the paper or envelope, and whether the printer is a dot matrix or HPPCL (Hewlett Packard Printer Control Language) device.</span></span> <span data-ttu-id="a2452-113">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="a2452-113">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="a2452-114">Значение</span><span class="sxs-lookup"><span data-stu-id="a2452-114">Value</span></span>                                                                             | <span data-ttu-id="a2452-115">Значение</span><span class="sxs-lookup"><span data-stu-id="a2452-115">Meaning</span></span>                                            |
|-----------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="a2452-116"><dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="a2452-116"><dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="a2452-117">Бумага в альбомном режиме (матрица точек)</span><span class="sxs-lookup"><span data-stu-id="a2452-117">Paper in landscape mode (dot matrix)</span></span><br/>    |
| <dl> <span data-ttu-id="a2452-118"><dt>0x0003</dt></span><span class="sxs-lookup"><span data-stu-id="a2452-118"><dt>0x0003</dt></span></span> </dl> | <span data-ttu-id="a2452-119">Бумага в альбомном режиме (ориентации для HPPCLHPPCL)</span><span class="sxs-lookup"><span data-stu-id="a2452-119">Paper in landscape mode (HPPCL)</span></span><br/>         |
| <dl> <span data-ttu-id="a2452-120"><dt>0x0005</dt></span><span class="sxs-lookup"><span data-stu-id="a2452-120"><dt>0x0005</dt></span></span> </dl> | <span data-ttu-id="a2452-121">Бумага в книжном режиме (матрица точек)</span><span class="sxs-lookup"><span data-stu-id="a2452-121">Paper in portrait mode (dot matrix)</span></span><br/>     |
| <dl> <span data-ttu-id="a2452-122"><dt>0x0007</dt></span><span class="sxs-lookup"><span data-stu-id="a2452-122"><dt>0x0007</dt></span></span> </dl> | <span data-ttu-id="a2452-123">Бумага в книжном режиме (ориентации для HPPCLHPPCL)</span><span class="sxs-lookup"><span data-stu-id="a2452-123">Paper in portrait mode (HPPCL)</span></span><br/>          |
| <dl> <span data-ttu-id="a2452-124"><dt>0x000b</dt></span><span class="sxs-lookup"><span data-stu-id="a2452-124"><dt>0x000b</dt></span></span> </dl> | <span data-ttu-id="a2452-125">Конверт в альбомном режиме (ориентации для HPPCLHPPCL)</span><span class="sxs-lookup"><span data-stu-id="a2452-125">Envelope in landscape mode (HPPCL)</span></span><br/>      |
| <dl> <span data-ttu-id="a2452-126"><dt>0x000d</dt></span><span class="sxs-lookup"><span data-stu-id="a2452-126"><dt>0x000d</dt></span></span> </dl> | <span data-ttu-id="a2452-127">Конверт в книжной ориентации (матрица точек)</span><span class="sxs-lookup"><span data-stu-id="a2452-127">Envelope in portrait mode (dot matrix)</span></span><br/>  |
| <dl> <span data-ttu-id="a2452-128"><dt>0x0019</dt></span><span class="sxs-lookup"><span data-stu-id="a2452-128"><dt>0x0019</dt></span></span> </dl> | <span data-ttu-id="a2452-129">Конверт в альбомном режиме (матрица точек)</span><span class="sxs-lookup"><span data-stu-id="a2452-129">Envelope in landscape mode (dot matrix)</span></span><br/> |
| <dl> <span data-ttu-id="a2452-130"><dt>0x001f</dt></span><span class="sxs-lookup"><span data-stu-id="a2452-130"><dt>0x001f</dt></span></span> </dl> | <span data-ttu-id="a2452-131">Конверт в книжном режиме (ориентации для HPPCLHPPCL)</span><span class="sxs-lookup"><span data-stu-id="a2452-131">Envelope in portrait mode (HPPCL)</span></span><br/>       |



 

</dd> <dt>

<span data-ttu-id="a2452-132">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a2452-132">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a2452-133">Указатель на структуру [**пажесетупдлг**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) , содержащую сведения, используемые для инициализации диалогового окна « **Параметры страницы** ».</span><span class="sxs-lookup"><span data-stu-id="a2452-133">A pointer to a [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) structure that contains information used to initialize the **Page Setup** dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2452-134">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a2452-134">Return value</span></span>

<span data-ttu-id="a2452-135">Если процедура-обработчик возвращает **значение true**, то диалоговое окно не отправляет никаких сообщений и не рисует его на образце страницы до тех пор, пока системе не потребуется перерисовать образец страницы.</span><span class="sxs-lookup"><span data-stu-id="a2452-135">If the hook procedure returns **TRUE**, the dialog box sends no more messages and does not draw in the sample page until the next time the system needs to redraw the sample page.</span></span>

<span data-ttu-id="a2452-136">Если процедура-обработчик возвращает **значение false**, то диалоговое окно отправляет оставшиеся сообщения последовательности отображения.</span><span class="sxs-lookup"><span data-stu-id="a2452-136">If the hook procedure returns **FALSE**, the dialog box sends the remaining messages of the drawing sequence.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2452-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a2452-137">Remarks</span></span>

<span data-ttu-id="a2452-138">Диалоговое окно **Параметры страницы** содержит изображение образца страницы, показывающее, как выбранные пользователем параметры влияют на внешний вид напечатанных данных.</span><span class="sxs-lookup"><span data-stu-id="a2452-138">The **Page Setup** dialog box includes an image of a sample page that shows how the user's selections affect the appearance of the printed output.</span></span> <span data-ttu-id="a2452-139">При вызове функции [**пажесетупдлг**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) можно предоставить процедуру-обработчик [*пажепаинсук*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) для настройки внешнего вида образца страницы.</span><span class="sxs-lookup"><span data-stu-id="a2452-139">When you call the [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) function, you can provide a [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure to customize the appearance of the sample page.</span></span> <span data-ttu-id="a2452-140">Каждый раз, когда диалоговое окно собирается вывести содержимое образца страницы, диалоговое окно отправляет последовательность сообщений в процедуру-обработчик.</span><span class="sxs-lookup"><span data-stu-id="a2452-140">Whenever the dialog box is about to draw the contents of the sample page, the dialog box sends a sequence of messages to the hook procedure.</span></span>

<span data-ttu-id="a2452-141">Первые три сообщения последовательности (**WM \_ PSD \_ пажесетупдлг**, [**WM \_ PSD \_ фуллпажерект**](wm-psd-fullpagerect.md)или [**WM \_ PSD \_ минмаргинрект**](wm-psd-minmarginrect.md)) предоставляют сведения, которые процедура-ловушка может использовать для рисования содержимого образца страницы.</span><span class="sxs-lookup"><span data-stu-id="a2452-141">The first three messages of a drawing sequence (**WM\_PSD\_PAGESETUPDLG**, [**WM\_PSD\_FULLPAGERECT**](wm-psd-fullpagerect.md), or [**WM\_PSD\_MINMARGINRECT**](wm-psd-minmarginrect.md)) provide information that the hook procedure can use to draw the contents of the sample page.</span></span> <span data-ttu-id="a2452-142">Оставшиеся сообщения ([**WM \_ PSD \_ маргинрект**](wm-psd-marginrect.md), [**WM \_ PSD \_ гриктекстрект**](wm-psd-greektextrect.md), [**WM \_ PSD \_ енвстампрект**](wm-psd-envstamprect.md), [**WM \_ PSD \_ яфуллпажерект**](wm-psd-yafullpagerect.md)) уведомляют процедуру-обработчик о том, что диалоговое окно собирается отобразить определенную часть образца страницы.</span><span class="sxs-lookup"><span data-stu-id="a2452-142">The remaining messages ([**WM\_PSD\_MARGINRECT**](wm-psd-marginrect.md), [**WM\_PSD\_GREEKTEXTRECT**](wm-psd-greektextrect.md), [**WM\_PSD\_ENVSTAMPRECT**](wm-psd-envstamprect.md), [**WM\_PSD\_YAFULLPAGERECT**](wm-psd-yafullpagerect.md)) notify the hook procedure that the dialog box is about to draw a specific portion of the sample page.</span></span> <span data-ttu-id="a2452-143">Это позволяет процедуре-обработчику выборочно рисовать части образца страницы.</span><span class="sxs-lookup"><span data-stu-id="a2452-143">This allows the hook procedure to selectively draw portions of the sample page.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2452-144">Требования</span><span class="sxs-lookup"><span data-stu-id="a2452-144">Requirements</span></span>



| <span data-ttu-id="a2452-145">Требование</span><span class="sxs-lookup"><span data-stu-id="a2452-145">Requirement</span></span> | <span data-ttu-id="a2452-146">Значение</span><span class="sxs-lookup"><span data-stu-id="a2452-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2452-147">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a2452-147">Minimum supported client</span></span><br/> | <span data-ttu-id="a2452-148">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a2452-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a2452-149">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a2452-149">Minimum supported server</span></span><br/> | <span data-ttu-id="a2452-150">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a2452-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a2452-151">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a2452-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2452-152"><dt>Коммдлг. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a2452-152"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2452-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a2452-153">See also</span></span>

<dl> <dt>

<span data-ttu-id="a2452-154">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="a2452-154">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a2452-155">*пажепаинсук*</span><span class="sxs-lookup"><span data-stu-id="a2452-155">*PagePaintHook*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)
</dt> <dt>

<span data-ttu-id="a2452-156">[**пажесетупдлг**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a2452-156">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="a2452-157">**пажесетупдлг**</span><span class="sxs-lookup"><span data-stu-id="a2452-157">**PAGESETUPDLG**</span></span>](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga)
</dt> <dt>

[<span data-ttu-id="a2452-158">**WM \_ PSD \_ енвстампрект**</span><span class="sxs-lookup"><span data-stu-id="a2452-158">**WM\_PSD\_ENVSTAMPRECT**</span></span>](wm-psd-envstamprect.md)
</dt> <dt>

[<span data-ttu-id="a2452-159">**WM \_ PSD \_ фуллпажерект**</span><span class="sxs-lookup"><span data-stu-id="a2452-159">**WM\_PSD\_FULLPAGERECT**</span></span>](wm-psd-fullpagerect.md)
</dt> <dt>

[<span data-ttu-id="a2452-160">**WM \_ PSD \_ гриктекстрект**</span><span class="sxs-lookup"><span data-stu-id="a2452-160">**WM\_PSD\_GREEKTEXTRECT**</span></span>](wm-psd-greektextrect.md)
</dt> <dt>

[<span data-ttu-id="a2452-161">**WM \_ PSD \_ маргинрект**</span><span class="sxs-lookup"><span data-stu-id="a2452-161">**WM\_PSD\_MARGINRECT**</span></span>](wm-psd-marginrect.md)
</dt> <dt>

[<span data-ttu-id="a2452-162">**WM \_ PSD \_ минмаргинрект**</span><span class="sxs-lookup"><span data-stu-id="a2452-162">**WM\_PSD\_MINMARGINRECT**</span></span>](wm-psd-minmarginrect.md)
</dt> <dt>

[<span data-ttu-id="a2452-163">**WM \_ PSD \_ яфуллпажерект**</span><span class="sxs-lookup"><span data-stu-id="a2452-163">**WM\_PSD\_YAFULLPAGERECT**</span></span>](wm-psd-yafullpagerect.md)
</dt> <dt>

<span data-ttu-id="a2452-164">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="a2452-164">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a2452-165">Библиотека общих диалоговых окон</span><span class="sxs-lookup"><span data-stu-id="a2452-165">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 


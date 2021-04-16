---
title: Код уведомления CDN_SHAREVIOLATION (Коммдлг. h)
description: Отсылается диалоговым окном открытия или сохранения в стиле обозревателя, когда пользователь нажимает кнопку ОК и возникает нарушение общего доступа к сети для выбранного файла.
ms.assetid: a62ca550-0997-4379-aaaf-a5bc9414bd69
keywords:
- CDN_SHAREVIOLATION диалоговых окон кода уведомления
topic_type:
- apiref
api_name:
- CDN_SHAREVIOLATION
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acfa3a91e9c84f15984285f99d071fcde24a4d66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105719194"
---
# <a name="cdn_shareviolation-notification-code"></a><span data-ttu-id="aaa78-104">\_Код уведомления ШАРЕВИОЛАТИОН CDN</span><span class="sxs-lookup"><span data-stu-id="aaa78-104">CDN\_SHAREVIOLATION notification code</span></span>

<span data-ttu-id="aaa78-105">\[Начиная с Windows Vista, диалоговые окна " **Открыть** " и " **Сохранить как** " были заменены [диалоговым окном общих элементов](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="aaa78-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="aaa78-106">Рекомендуется использовать API-интерфейс общего элемента, а не эти диалоговые окна из библиотеки общих диалоговых окон.\]</span><span class="sxs-lookup"><span data-stu-id="aaa78-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="aaa78-107">Отсылается диалоговым окном **открытия** или **сохранения в** стиле обозревателя, когда пользователь нажимает кнопку **ОК** и возникает нарушение общего доступа к сети для выбранного файла.</span><span class="sxs-lookup"><span data-stu-id="aaa78-107">Sent by an Explorer-style **Open** or **Save As** dialog box when the user clicks the **OK** button and a network sharing violation occurs for the selected file.</span></span>

<span data-ttu-id="aaa78-108">Процедура обработчика [*офнхукпрок*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) получает это сообщение в виде сообщения [**WM \_ Notify**](../controls/wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="aaa78-108">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_SHAREVIOLATION      (CDN_FIRST - 0x0003)
```



## <a name="parameters"></a><span data-ttu-id="aaa78-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="aaa78-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aaa78-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="aaa78-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aaa78-111">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="aaa78-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="aaa78-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="aaa78-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aaa78-113">Указатель на структуру [**офнотифи**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) .</span><span class="sxs-lookup"><span data-stu-id="aaa78-113">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span> <span data-ttu-id="aaa78-114">Элемент **псзфиле** этой структуры является указателем на имя файла с нарушением общего доступа.</span><span class="sxs-lookup"><span data-stu-id="aaa78-114">The **pszFile** member of this structure is a pointer to the name of the file that had the sharing violation.</span></span> <span data-ttu-id="aaa78-115">Структура **офнотифи** содержит структуру [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) , элемент **кода** которой указывает на сообщение **уведомления \_ шаревиолатион CDN** .</span><span class="sxs-lookup"><span data-stu-id="aaa78-115">The **OFNOTIFY** structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_SHAREVIOLATION** notification message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aaa78-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="aaa78-116">Return value</span></span>

<span data-ttu-id="aaa78-117">Возвращаемое значение показывает, как диалоговое окно должно реагировать на нарушение совместного доступа.</span><span class="sxs-lookup"><span data-stu-id="aaa78-117">The return value indicates how the dialog box should handle the sharing violation.</span></span>

<span data-ttu-id="aaa78-118">Если процедура-обработчик возвращает значение 0, в диалоговом окне отображается стандартное предупреждающее сообщение о нарушении общего доступа.</span><span class="sxs-lookup"><span data-stu-id="aaa78-118">If the hook procedure returns zero, the dialog box displays the standard warning message for a sharing violation.</span></span>

<span data-ttu-id="aaa78-119">Чтобы предотвратить отображение стандартного предупреждающего сообщения, следует вернуть ненулевое значение из процедуры-обработчика и вызвать функцию [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) , чтобы установить одно из следующих **значений \_ мсгресулт DWL** .</span><span class="sxs-lookup"><span data-stu-id="aaa78-119">To prevent the display of the standard warning message, return a nonzero value from the hook procedure and call the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function to set one of the following **DWL\_MSGRESULT** values.</span></span>



| <span data-ttu-id="aaa78-120">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="aaa78-120">Return code/value</span></span>                                                                                                                                           | <span data-ttu-id="aaa78-121">Описание</span><span class="sxs-lookup"><span data-stu-id="aaa78-121">Description</span></span>                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="aaa78-122"><dt>**ОФН \_ ШАРЕФАЛЛСРАУГХ**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="aaa78-122"><dt>**OFN\_SHAREFALLTHROUGH**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="aaa78-123">Заставляет диалоговое окно вернуть имя файла без предупреждения пользователя о нарушении общего доступа.</span><span class="sxs-lookup"><span data-stu-id="aaa78-123">Causes the dialog box to return the file name without warning the user about the sharing violation.</span></span><br/>  |
| <dl> <span data-ttu-id="aaa78-124"><dt>**ОФН \_ ШАРЕНОВАРН**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="aaa78-124"><dt>**OFN\_SHARENOWARN**</dt> <dt>1</dt></span></span> </dl>      | <span data-ttu-id="aaa78-125">Заставляет диалоговое окно отклонять имя файла без предупреждения пользователя о нарушении общего доступа.</span><span class="sxs-lookup"><span data-stu-id="aaa78-125">Causes the dialog box to reject the file name without warning the user about the sharing violation.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="aaa78-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="aaa78-126">Remarks</span></span>

<span data-ttu-id="aaa78-127">Система отправляет это уведомление только в том случае, если диалоговое окно было создано с помощью значения **\_ обозревателя ОФН** .</span><span class="sxs-lookup"><span data-stu-id="aaa78-127">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

<span data-ttu-id="aaa78-128">Система отправляет это уведомление, только если значение **ОФН \_ шареаваре** не было указано при создании диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="aaa78-128">The system sends this notification only if the **OFN\_SHAREAWARE** value was not specified when the dialog box was created.</span></span>

## <a name="requirements"></a><span data-ttu-id="aaa78-129">Требования</span><span class="sxs-lookup"><span data-stu-id="aaa78-129">Requirements</span></span>



| <span data-ttu-id="aaa78-130">Требование</span><span class="sxs-lookup"><span data-stu-id="aaa78-130">Requirement</span></span> | <span data-ttu-id="aaa78-131">Значение</span><span class="sxs-lookup"><span data-stu-id="aaa78-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aaa78-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="aaa78-132">Minimum supported client</span></span><br/> | <span data-ttu-id="aaa78-133">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="aaa78-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="aaa78-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="aaa78-134">Minimum supported server</span></span><br/> | <span data-ttu-id="aaa78-135">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="aaa78-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="aaa78-136">Заголовок</span><span class="sxs-lookup"><span data-stu-id="aaa78-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="aaa78-137"><dt>Коммдлг. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="aaa78-137"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aaa78-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aaa78-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="aaa78-139">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="aaa78-139">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="aaa78-140">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="aaa78-140">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="aaa78-141">**жетсавефиленаме**</span><span class="sxs-lookup"><span data-stu-id="aaa78-141">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="aaa78-142">*офнхукпрок*</span><span class="sxs-lookup"><span data-stu-id="aaa78-142">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="aaa78-143">**офнотифи**</span><span class="sxs-lookup"><span data-stu-id="aaa78-143">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[<span data-ttu-id="aaa78-144">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="aaa78-144">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[<span data-ttu-id="aaa78-145">**SetWindowLong**</span><span class="sxs-lookup"><span data-stu-id="aaa78-145">**SetWindowLong**</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)
</dt> <dt>

<span data-ttu-id="aaa78-146">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="aaa78-146">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="aaa78-147">Библиотека общих диалоговых окон</span><span class="sxs-lookup"><span data-stu-id="aaa78-147">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 


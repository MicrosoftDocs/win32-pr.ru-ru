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
ms.openlocfilehash: 6e79d9c48d3e80d14d83de07c03f7db119ea8e78
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590701"
---
# <a name="cdn_shareviolation-notification-code"></a><span data-ttu-id="9cc47-104">\_Код уведомления ШАРЕВИОЛАТИОН CDN</span><span class="sxs-lookup"><span data-stu-id="9cc47-104">CDN\_SHAREVIOLATION notification code</span></span>

<span data-ttu-id="9cc47-105">\[Начиная с Windows Vista, диалоговые окна " **Открыть** " и " **Сохранить как** " были заменены [диалоговым окном общих элементов](/windows/win32/shell/common-file-dialog).</span><span class="sxs-lookup"><span data-stu-id="9cc47-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="9cc47-106">Рекомендуется использовать API-интерфейс общего элемента, а не эти диалоговые окна из библиотеки общих диалоговых окон.\]</span><span class="sxs-lookup"><span data-stu-id="9cc47-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="9cc47-107">Отсылается диалоговым окном **открытия** или **сохранения в** стиле обозревателя, когда пользователь нажимает кнопку **ОК** и возникает нарушение общего доступа к сети для выбранного файла.</span><span class="sxs-lookup"><span data-stu-id="9cc47-107">Sent by an Explorer-style **Open** or **Save As** dialog box when the user clicks the **OK** button and a network sharing violation occurs for the selected file.</span></span>

<span data-ttu-id="9cc47-108">Процедура обработчика [*офнхукпрок*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) получает это сообщение в виде сообщения [**WM \_ Notify**](../controls/wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="9cc47-108">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_SHAREVIOLATION      (CDN_FIRST - 0x0003)
```



## <a name="parameters"></a><span data-ttu-id="9cc47-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="9cc47-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9cc47-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9cc47-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9cc47-111">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="9cc47-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9cc47-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9cc47-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9cc47-113">Указатель на структуру [**офнотифи**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) .</span><span class="sxs-lookup"><span data-stu-id="9cc47-113">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span> <span data-ttu-id="9cc47-114">Элемент **псзфиле** этой структуры является указателем на имя файла с нарушением общего доступа.</span><span class="sxs-lookup"><span data-stu-id="9cc47-114">The **pszFile** member of this structure is a pointer to the name of the file that had the sharing violation.</span></span> <span data-ttu-id="9cc47-115">Структура **офнотифи** содержит структуру [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) , элемент **кода** которой указывает на сообщение **уведомления \_ шаревиолатион CDN** .</span><span class="sxs-lookup"><span data-stu-id="9cc47-115">The **OFNOTIFY** structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_SHAREVIOLATION** notification message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9cc47-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9cc47-116">Return value</span></span>

<span data-ttu-id="9cc47-117">Возвращаемое значение показывает, как диалоговое окно должно реагировать на нарушение совместного доступа.</span><span class="sxs-lookup"><span data-stu-id="9cc47-117">The return value indicates how the dialog box should handle the sharing violation.</span></span>

<span data-ttu-id="9cc47-118">Если процедура-обработчик возвращает значение 0, в диалоговом окне отображается стандартное предупреждающее сообщение о нарушении общего доступа.</span><span class="sxs-lookup"><span data-stu-id="9cc47-118">If the hook procedure returns zero, the dialog box displays the standard warning message for a sharing violation.</span></span>

<span data-ttu-id="9cc47-119">Чтобы предотвратить отображение стандартного предупреждающего сообщения, следует вернуть ненулевое значение из процедуры-обработчика и вызвать функцию [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) , чтобы установить одно из следующих **значений \_ мсгресулт DWL** .</span><span class="sxs-lookup"><span data-stu-id="9cc47-119">To prevent the display of the standard warning message, return a nonzero value from the hook procedure and call the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function to set one of the following **DWL\_MSGRESULT** values.</span></span>



| <span data-ttu-id="9cc47-120">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="9cc47-120">Return code/value</span></span>                                                                                                                                           | <span data-ttu-id="9cc47-121">Описание:</span><span class="sxs-lookup"><span data-stu-id="9cc47-121">Description</span></span>                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9cc47-122"><dt>**ОФН \_ ШАРЕФАЛЛСРАУГХ**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="9cc47-122"><dt>**OFN\_SHAREFALLTHROUGH**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="9cc47-123">Заставляет диалоговое окно вернуть имя файла без предупреждения пользователя о нарушении общего доступа.</span><span class="sxs-lookup"><span data-stu-id="9cc47-123">Causes the dialog box to return the file name without warning the user about the sharing violation.</span></span><br/>  |
| <dl> <span data-ttu-id="9cc47-124"><dt>**ОФН \_ ШАРЕНОВАРН**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="9cc47-124"><dt>**OFN\_SHARENOWARN**</dt> <dt>1</dt></span></span> </dl>      | <span data-ttu-id="9cc47-125">Заставляет диалоговое окно отклонять имя файла без предупреждения пользователя о нарушении общего доступа.</span><span class="sxs-lookup"><span data-stu-id="9cc47-125">Causes the dialog box to reject the file name without warning the user about the sharing violation.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="9cc47-126">Замечания</span><span class="sxs-lookup"><span data-stu-id="9cc47-126">Remarks</span></span>

<span data-ttu-id="9cc47-127">Система отправляет это уведомление только в том случае, если диалоговое окно было создано с помощью значения **\_ обозревателя ОФН** .</span><span class="sxs-lookup"><span data-stu-id="9cc47-127">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

<span data-ttu-id="9cc47-128">Система отправляет это уведомление, только если значение **ОФН \_ шареаваре** не было указано при создании диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="9cc47-128">The system sends this notification only if the **OFN\_SHAREAWARE** value was not specified when the dialog box was created.</span></span>

## <a name="requirements"></a><span data-ttu-id="9cc47-129">Требования</span><span class="sxs-lookup"><span data-stu-id="9cc47-129">Requirements</span></span>



| <span data-ttu-id="9cc47-130">Требование</span><span class="sxs-lookup"><span data-stu-id="9cc47-130">Requirement</span></span> | <span data-ttu-id="9cc47-131">Значение</span><span class="sxs-lookup"><span data-stu-id="9cc47-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9cc47-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9cc47-132">Minimum supported client</span></span><br/> | <span data-ttu-id="9cc47-133">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9cc47-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="9cc47-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9cc47-134">Minimum supported server</span></span><br/> | <span data-ttu-id="9cc47-135">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9cc47-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9cc47-136">Заголовок</span><span class="sxs-lookup"><span data-stu-id="9cc47-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="9cc47-137"><dt>Коммдлг. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9cc47-137"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9cc47-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9cc47-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="9cc47-139">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="9cc47-139">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9cc47-140">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="9cc47-140">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="9cc47-141">**жетсавефиленаме**</span><span class="sxs-lookup"><span data-stu-id="9cc47-141">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="9cc47-142">*офнхукпрок*</span><span class="sxs-lookup"><span data-stu-id="9cc47-142">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="9cc47-143">**офнотифи**</span><span class="sxs-lookup"><span data-stu-id="9cc47-143">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[<span data-ttu-id="9cc47-144">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="9cc47-144">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[<span data-ttu-id="9cc47-145">**SetWindowLong**</span><span class="sxs-lookup"><span data-stu-id="9cc47-145">**SetWindowLong**</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)
</dt> <dt>

<span data-ttu-id="9cc47-146">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="9cc47-146">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9cc47-147">Библиотека общих диалоговых окон</span><span class="sxs-lookup"><span data-stu-id="9cc47-147">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 


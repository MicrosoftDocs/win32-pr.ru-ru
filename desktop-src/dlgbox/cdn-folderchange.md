---
title: Код уведомления CDN_FOLDERCHANGE (Коммдлг. h)
description: Отправляется диалоговым окном открытия или сохранения в стиле обозревателя при открытии новой папки.
ms.assetid: 864ab80d-cd99-4dd6-8aff-49beed246e53
keywords:
- CDN_FOLDERCHANGE диалоговых окон кода уведомления
topic_type:
- apiref
api_name:
- CDN_FOLDERCHANGE
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c93bd37afa44e7fc5ca81d928974f56bf80d1b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136075"
---
# <a name="cdn_folderchange-notification-code"></a><span data-ttu-id="eec49-104">\_Код уведомления ФОЛДЕРЧАНЖЕ CDN</span><span class="sxs-lookup"><span data-stu-id="eec49-104">CDN\_FOLDERCHANGE notification code</span></span>

<span data-ttu-id="eec49-105">\[Начиная с Windows Vista, диалоговые окна " **Открыть** " и " **Сохранить как** " были заменены [диалоговым окном общих элементов](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="eec49-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="eec49-106">Рекомендуется использовать API-интерфейс общего элемента, а не эти диалоговые окна из библиотеки общих диалоговых окон.\]</span><span class="sxs-lookup"><span data-stu-id="eec49-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="eec49-107">Отправляется диалоговым окном **открытия** или **сохранения в** стиле обозревателя при открытии новой папки.</span><span class="sxs-lookup"><span data-stu-id="eec49-107">Sent by an Explorer-style **Open** or **Save As** dialog box when a new folder is opened.</span></span>

<span data-ttu-id="eec49-108">Процедура обработчика [*офнхукпрок*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) получает это сообщение в виде сообщения [**WM \_ Notify**](../controls/wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="eec49-108">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_FOLDERCHANGE        (CDN_FIRST - 0x0002)
```



## <a name="parameters"></a><span data-ttu-id="eec49-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="eec49-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eec49-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="eec49-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eec49-111">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="eec49-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="eec49-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="eec49-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eec49-113">Указатель на структуру [**офнотифи**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) .</span><span class="sxs-lookup"><span data-stu-id="eec49-113">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span> <span data-ttu-id="eec49-114">Структура **офнотифи** содержит структуру [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) , элемент **кода** которой указывает на сообщение **уведомления \_ фолдерчанже CDN** .</span><span class="sxs-lookup"><span data-stu-id="eec49-114">The **OFNOTIFY** structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_FOLDERCHANGE** notification message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eec49-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="eec49-115">Return value</span></span>

<span data-ttu-id="eec49-116">Возвращаемое значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="eec49-116">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="eec49-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eec49-117">Remarks</span></span>

<span data-ttu-id="eec49-118">Система отправляет это уведомление только в том случае, если диалоговое окно было создано с помощью значения **\_ обозревателя ОФН** .</span><span class="sxs-lookup"><span data-stu-id="eec49-118">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

<span data-ttu-id="eec49-119">Чтобы получить путь к вновь открытой папке, процедура-обработчик может отправить сообщение [**CDM \_ GETFOLDERPATH**](cdm-getfolderpath.md) в диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="eec49-119">To get the path of the newly opened folder, the hook procedure can send the [**CDM\_GETFOLDERPATH**](cdm-getfolderpath.md) message to the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="eec49-120">Требования</span><span class="sxs-lookup"><span data-stu-id="eec49-120">Requirements</span></span>



| <span data-ttu-id="eec49-121">Требование</span><span class="sxs-lookup"><span data-stu-id="eec49-121">Requirement</span></span> | <span data-ttu-id="eec49-122">Значение</span><span class="sxs-lookup"><span data-stu-id="eec49-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eec49-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="eec49-123">Minimum supported client</span></span><br/> | <span data-ttu-id="eec49-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="eec49-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="eec49-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="eec49-125">Minimum supported server</span></span><br/> | <span data-ttu-id="eec49-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="eec49-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="eec49-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="eec49-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="eec49-128"><dt>Коммдлг. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eec49-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eec49-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eec49-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="eec49-130">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="eec49-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="eec49-131">**CDM \_ GETFOLDERPATH**</span><span class="sxs-lookup"><span data-stu-id="eec49-131">**CDM\_GETFOLDERPATH**</span></span>](cdm-getfolderpath.md)
</dt> <dt>

[<span data-ttu-id="eec49-132">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="eec49-132">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="eec49-133">**жетсавефиленаме**</span><span class="sxs-lookup"><span data-stu-id="eec49-133">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="eec49-134">*офнхукпрок*</span><span class="sxs-lookup"><span data-stu-id="eec49-134">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="eec49-135">**офнотифи**</span><span class="sxs-lookup"><span data-stu-id="eec49-135">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

<span data-ttu-id="eec49-136">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="eec49-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="eec49-137">Библиотека общих диалоговых окон</span><span class="sxs-lookup"><span data-stu-id="eec49-137">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 


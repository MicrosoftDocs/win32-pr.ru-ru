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
ms.openlocfilehash: 318aa2ffe4ddd47bcb1472f412f85ab785c5049e
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550079"
---
# <a name="cdn_folderchange-notification-code"></a><span data-ttu-id="07059-104">\_Код уведомления ФОЛДЕРЧАНЖЕ CDN</span><span class="sxs-lookup"><span data-stu-id="07059-104">CDN\_FOLDERCHANGE notification code</span></span>

<span data-ttu-id="07059-105">\[Начиная с Windows Vista, диалоговые окна " **Открыть** " и " **Сохранить как** " были заменены [диалоговым окном общих элементов](../shell/common-file-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="07059-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](../shell/common-file-dialog.md).</span></span> <span data-ttu-id="07059-106">Рекомендуется использовать API-интерфейс общего элемента, а не эти диалоговые окна из библиотеки общих диалоговых окон.\]</span><span class="sxs-lookup"><span data-stu-id="07059-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="07059-107">Отправляется диалоговым окном **открытия** или **сохранения в** стиле обозревателя при открытии новой папки.</span><span class="sxs-lookup"><span data-stu-id="07059-107">Sent by an Explorer-style **Open** or **Save As** dialog box when a new folder is opened.</span></span>

<span data-ttu-id="07059-108">Процедура обработчика [*офнхукпрок*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) получает это сообщение в виде сообщения [**WM \_ Notify**](../controls/wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="07059-108">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_FOLDERCHANGE        (CDN_FIRST - 0x0002)
```



## <a name="parameters"></a><span data-ttu-id="07059-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="07059-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07059-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="07059-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="07059-111">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="07059-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="07059-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="07059-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="07059-113">Указатель на структуру [**офнотифи**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) .</span><span class="sxs-lookup"><span data-stu-id="07059-113">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span> <span data-ttu-id="07059-114">Структура **офнотифи** содержит структуру [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) , элемент **кода** которой указывает на сообщение **уведомления \_ фолдерчанже CDN** .</span><span class="sxs-lookup"><span data-stu-id="07059-114">The **OFNOTIFY** structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_FOLDERCHANGE** notification message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07059-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="07059-115">Return value</span></span>

<span data-ttu-id="07059-116">Возвращаемое значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="07059-116">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="07059-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="07059-117">Remarks</span></span>

<span data-ttu-id="07059-118">Система отправляет это уведомление только в том случае, если диалоговое окно было создано с помощью значения **\_ обозревателя ОФН** .</span><span class="sxs-lookup"><span data-stu-id="07059-118">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

<span data-ttu-id="07059-119">Чтобы получить путь к вновь открытой папке, процедура-обработчик может отправить сообщение [**CDM \_ GETFOLDERPATH**](cdm-getfolderpath.md) в диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="07059-119">To get the path of the newly opened folder, the hook procedure can send the [**CDM\_GETFOLDERPATH**](cdm-getfolderpath.md) message to the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="07059-120">Требования</span><span class="sxs-lookup"><span data-stu-id="07059-120">Requirements</span></span>



| <span data-ttu-id="07059-121">Требование</span><span class="sxs-lookup"><span data-stu-id="07059-121">Requirement</span></span> | <span data-ttu-id="07059-122">Применение</span><span class="sxs-lookup"><span data-stu-id="07059-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07059-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="07059-123">Minimum supported client</span></span><br/> | <span data-ttu-id="07059-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="07059-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="07059-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="07059-125">Minimum supported server</span></span><br/> | <span data-ttu-id="07059-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="07059-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="07059-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="07059-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="07059-128"><dt>Коммдлг. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="07059-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07059-129">См. также</span><span class="sxs-lookup"><span data-stu-id="07059-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="07059-130">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="07059-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="07059-131">**CDM \_ GETFOLDERPATH**</span><span class="sxs-lookup"><span data-stu-id="07059-131">**CDM\_GETFOLDERPATH**</span></span>](cdm-getfolderpath.md)
</dt> <dt>

[<span data-ttu-id="07059-132">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="07059-132">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="07059-133">**жетсавефиленаме**</span><span class="sxs-lookup"><span data-stu-id="07059-133">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="07059-134">*офнхукпрок*</span><span class="sxs-lookup"><span data-stu-id="07059-134">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="07059-135">**офнотифи**</span><span class="sxs-lookup"><span data-stu-id="07059-135">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

<span data-ttu-id="07059-136">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="07059-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="07059-137">Библиотека общих диалоговых окон</span><span class="sxs-lookup"><span data-stu-id="07059-137">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>


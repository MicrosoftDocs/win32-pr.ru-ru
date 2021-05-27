---
title: Код уведомления CDN_HELP (Коммдлг. h)
description: Отсылается диалоговым окном открытия или сохранения в стиле обозревателя, когда пользователь нажимает кнопку «Справка».
ms.assetid: 18ee86b2-3446-4de4-a47a-2e44e677f4f7
keywords:
- CDN_HELP диалоговых окон кода уведомления
topic_type:
- apiref
api_name:
- CDN_HELP
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0abd3519bdc877eca24304b1104a12d51b2dfe4f
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550069"
---
# <a name="cdn_help-notification-code"></a><span data-ttu-id="9fc44-104">\_Код уведомления в СПРАВКЕ CDN</span><span class="sxs-lookup"><span data-stu-id="9fc44-104">CDN\_HELP notification code</span></span>

<span data-ttu-id="9fc44-105">\[Начиная с Windows Vista, диалоговые окна " **Открыть** " и " **Сохранить как** " были заменены [диалоговым окном общих элементов](../shell/common-file-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="9fc44-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](../shell/common-file-dialog.md).</span></span> <span data-ttu-id="9fc44-106">Рекомендуется использовать API-интерфейс общего элемента, а не эти диалоговые окна из библиотеки общих диалоговых окон.\]</span><span class="sxs-lookup"><span data-stu-id="9fc44-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="9fc44-107">Отсылается диалоговым окном **открытия** или **сохранения в** стиле обозревателя, когда пользователь нажимает кнопку « **Справка** ».</span><span class="sxs-lookup"><span data-stu-id="9fc44-107">Sent by an Explorer-style **Open** or **Save As** dialog box when the user clicks the **Help** button.</span></span>

<span data-ttu-id="9fc44-108">Процедура обработчика [*офнхукпрок*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) получает это сообщение в виде сообщения [**WM \_ Notify**](../controls/wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="9fc44-108">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_HELP                (CDN_FIRST - 0x0004)
```



## <a name="parameters"></a><span data-ttu-id="9fc44-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="9fc44-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fc44-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9fc44-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9fc44-111">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="9fc44-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9fc44-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9fc44-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9fc44-113">Указатель на структуру [**офнотифи**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) .</span><span class="sxs-lookup"><span data-stu-id="9fc44-113">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span> <span data-ttu-id="9fc44-114">Структура **офнотифи** содержит структуру [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) , элемент **кода** которой указывает на сообщение с уведомлением в **\_ справке CDN** .</span><span class="sxs-lookup"><span data-stu-id="9fc44-114">The **OFNOTIFY** structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_HELP** notification message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fc44-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9fc44-115">Return value</span></span>

<span data-ttu-id="9fc44-116">Возвращаемое значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="9fc44-116">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="9fc44-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9fc44-117">Remarks</span></span>

<span data-ttu-id="9fc44-118">Система отправляет это уведомление только в том случае, если диалоговое окно было создано с помощью значения **\_ обозревателя ОФН** .</span><span class="sxs-lookup"><span data-stu-id="9fc44-118">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fc44-119">Требования</span><span class="sxs-lookup"><span data-stu-id="9fc44-119">Requirements</span></span>



| <span data-ttu-id="9fc44-120">Требование</span><span class="sxs-lookup"><span data-stu-id="9fc44-120">Requirement</span></span> | <span data-ttu-id="9fc44-121">Применение</span><span class="sxs-lookup"><span data-stu-id="9fc44-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fc44-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9fc44-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9fc44-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9fc44-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="9fc44-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9fc44-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9fc44-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9fc44-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9fc44-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="9fc44-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9fc44-127"><dt>Коммдлг. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9fc44-127"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fc44-128">См. также</span><span class="sxs-lookup"><span data-stu-id="9fc44-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="9fc44-129">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="9fc44-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9fc44-130">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="9fc44-130">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="9fc44-131">**жетсавефиленаме**</span><span class="sxs-lookup"><span data-stu-id="9fc44-131">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="9fc44-132">*офнхукпрок*</span><span class="sxs-lookup"><span data-stu-id="9fc44-132">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="9fc44-133">**офнотифи**</span><span class="sxs-lookup"><span data-stu-id="9fc44-133">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[<span data-ttu-id="9fc44-134">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="9fc44-134">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="9fc44-135">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="9fc44-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9fc44-136">Библиотека общих диалоговых окон</span><span class="sxs-lookup"><span data-stu-id="9fc44-136">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>


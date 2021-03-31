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
ms.openlocfilehash: c73b690b1ac522a985ae121413804c4385e0f2cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136990"
---
# <a name="cdn_help-notification-code"></a><span data-ttu-id="fa978-104">\_Код уведомления в СПРАВКЕ CDN</span><span class="sxs-lookup"><span data-stu-id="fa978-104">CDN\_HELP notification code</span></span>

<span data-ttu-id="fa978-105">\[Начиная с Windows Vista, диалоговые окна " **Открыть** " и " **Сохранить как** " были заменены [диалоговым окном общих элементов](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fa978-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="fa978-106">Рекомендуется использовать API-интерфейс общего элемента, а не эти диалоговые окна из библиотеки общих диалоговых окон.\]</span><span class="sxs-lookup"><span data-stu-id="fa978-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="fa978-107">Отсылается диалоговым окном **открытия** или **сохранения в** стиле обозревателя, когда пользователь нажимает кнопку « **Справка** ».</span><span class="sxs-lookup"><span data-stu-id="fa978-107">Sent by an Explorer-style **Open** or **Save As** dialog box when the user clicks the **Help** button.</span></span>

<span data-ttu-id="fa978-108">Процедура обработчика [*офнхукпрок*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) получает это сообщение в виде сообщения [**WM \_ Notify**](../controls/wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="fa978-108">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_HELP                (CDN_FIRST - 0x0004)
```



## <a name="parameters"></a><span data-ttu-id="fa978-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="fa978-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa978-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fa978-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fa978-111">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="fa978-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="fa978-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fa978-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fa978-113">Указатель на структуру [**офнотифи**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) .</span><span class="sxs-lookup"><span data-stu-id="fa978-113">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span> <span data-ttu-id="fa978-114">Структура **офнотифи** содержит структуру [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) , элемент **кода** которой указывает на сообщение с уведомлением в **\_ справке CDN** .</span><span class="sxs-lookup"><span data-stu-id="fa978-114">The **OFNOTIFY** structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_HELP** notification message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa978-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fa978-115">Return value</span></span>

<span data-ttu-id="fa978-116">Возвращаемое значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="fa978-116">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa978-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fa978-117">Remarks</span></span>

<span data-ttu-id="fa978-118">Система отправляет это уведомление только в том случае, если диалоговое окно было создано с помощью значения **\_ обозревателя ОФН** .</span><span class="sxs-lookup"><span data-stu-id="fa978-118">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa978-119">Требования</span><span class="sxs-lookup"><span data-stu-id="fa978-119">Requirements</span></span>



| <span data-ttu-id="fa978-120">Требование</span><span class="sxs-lookup"><span data-stu-id="fa978-120">Requirement</span></span> | <span data-ttu-id="fa978-121">Значение</span><span class="sxs-lookup"><span data-stu-id="fa978-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa978-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fa978-122">Minimum supported client</span></span><br/> | <span data-ttu-id="fa978-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="fa978-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="fa978-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fa978-124">Minimum supported server</span></span><br/> | <span data-ttu-id="fa978-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="fa978-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fa978-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="fa978-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa978-127"><dt>Коммдлг. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fa978-127"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa978-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fa978-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="fa978-129">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="fa978-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="fa978-130">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="fa978-130">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="fa978-131">**жетсавефиленаме**</span><span class="sxs-lookup"><span data-stu-id="fa978-131">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="fa978-132">*офнхукпрок*</span><span class="sxs-lookup"><span data-stu-id="fa978-132">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="fa978-133">**офнотифи**</span><span class="sxs-lookup"><span data-stu-id="fa978-133">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[<span data-ttu-id="fa978-134">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="fa978-134">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="fa978-135">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="fa978-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="fa978-136">Библиотека общих диалоговых окон</span><span class="sxs-lookup"><span data-stu-id="fa978-136">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 


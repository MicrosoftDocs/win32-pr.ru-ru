---
title: Код уведомления CDN_TYPECHANGE (Коммдлг. h)
description: Отправляется в стиле обозревателя в диалоговом окне Открыть или сохранить как, когда пользователь выбирает новый тип файла в поле со списком типы файлов.
ms.assetid: fb8324db-e435-4ef2-aac5-506a6b7adb2c
keywords:
- CDN_TYPECHANGE диалоговых окон кода уведомления
topic_type:
- apiref
api_name:
- CDN_TYPECHANGE
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64226c1ac15cb6b55c6c2e2de7264d726e6f3a7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490566"
---
# <a name="cdn_typechange-notification-code"></a><span data-ttu-id="1706a-104">\_Код уведомления ТИПЕЧАНЖЕ CDN</span><span class="sxs-lookup"><span data-stu-id="1706a-104">CDN\_TYPECHANGE notification code</span></span>

<span data-ttu-id="1706a-105">\[Начиная с Windows Vista, диалоговые окна " **Открыть** " и " **Сохранить как** " были заменены [диалоговым окном общих элементов](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1706a-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="1706a-106">Рекомендуется использовать API-интерфейс общего элемента, а не эти диалоговые окна из библиотеки общих диалоговых окон.\]</span><span class="sxs-lookup"><span data-stu-id="1706a-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="1706a-107">Отправляется в стиле обозревателя в диалоговом окне **Открыть** или **Сохранить как** , когда пользователь выбирает новый тип файла в поле со списком типы файлов.</span><span class="sxs-lookup"><span data-stu-id="1706a-107">Sent by an Explorer-style **Open** or **Save As** dialog box when the user selects a new file type from the file types combo box.</span></span>

<span data-ttu-id="1706a-108">Процедура обработчика [*офнхукпрок*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) получает это сообщение в виде сообщения [**WM \_ Notify**](../controls/wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="1706a-108">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_TYPECHANGE          (CDN_FIRST - 0x0006)
```



## <a name="parameters"></a><span data-ttu-id="1706a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="1706a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1706a-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1706a-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1706a-111">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="1706a-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1706a-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1706a-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1706a-113">Указатель на структуру [**офнотифи**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) .</span><span class="sxs-lookup"><span data-stu-id="1706a-113">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span>

<span data-ttu-id="1706a-114">Структура [**офнотифи**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) содержит структуру [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) , элемент **кода** которой указывает на сообщение **уведомления \_ типечанже CDN** .</span><span class="sxs-lookup"><span data-stu-id="1706a-114">The [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_TYPECHANGE** notification message.</span></span>

<span data-ttu-id="1706a-115">Структура [**офнотифи**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) также содержит указатель на структуру [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) , член **нфилтериндекс** которой указывает индекс только что выбранного фильтра типа файла.</span><span class="sxs-lookup"><span data-stu-id="1706a-115">The [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure also contains a pointer to an [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure whose **nFilterIndex** member indicates the one-based index of the newly selected file type filter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1706a-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1706a-116">Return value</span></span>

<span data-ttu-id="1706a-117">Это сообщение не имеет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="1706a-117">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1706a-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1706a-118">Remarks</span></span>

<span data-ttu-id="1706a-119">Система отправляет это уведомление только в том случае, если диалоговое окно было создано с помощью значения **\_ обозревателя ОФН** .</span><span class="sxs-lookup"><span data-stu-id="1706a-119">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="1706a-120">Требования</span><span class="sxs-lookup"><span data-stu-id="1706a-120">Requirements</span></span>



| <span data-ttu-id="1706a-121">Требование</span><span class="sxs-lookup"><span data-stu-id="1706a-121">Requirement</span></span> | <span data-ttu-id="1706a-122">Значение</span><span class="sxs-lookup"><span data-stu-id="1706a-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1706a-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1706a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="1706a-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1706a-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="1706a-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1706a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="1706a-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1706a-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1706a-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="1706a-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="1706a-128"><dt>Коммдлг. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1706a-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1706a-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1706a-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="1706a-130">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="1706a-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1706a-131">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="1706a-131">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="1706a-132">**жетсавефиленаме**</span><span class="sxs-lookup"><span data-stu-id="1706a-132">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="1706a-133">*офнхукпрок*</span><span class="sxs-lookup"><span data-stu-id="1706a-133">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="1706a-134">**офнотифи**</span><span class="sxs-lookup"><span data-stu-id="1706a-134">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[<span data-ttu-id="1706a-135">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="1706a-135">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="1706a-136">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="1706a-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1706a-137">Библиотека общих диалоговых окон</span><span class="sxs-lookup"><span data-stu-id="1706a-137">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 


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
ms.openlocfilehash: 5c03fae474f6622e1ccec0c5b52b0dfb473ba438
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590851"
---
# <a name="cdn_help-notification-code"></a><span data-ttu-id="43d36-104">\_Код уведомления в СПРАВКЕ CDN</span><span class="sxs-lookup"><span data-stu-id="43d36-104">CDN\_HELP notification code</span></span>

<span data-ttu-id="43d36-105">\[Начиная с Windows Vista, диалоговые окна " **Открыть** " и " **Сохранить как** " были заменены [диалоговым окном общих элементов](/windows/win32/shell/common-file-dialog).</span><span class="sxs-lookup"><span data-stu-id="43d36-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="43d36-106">Рекомендуется использовать API-интерфейс общего элемента, а не эти диалоговые окна из библиотеки общих диалоговых окон.\]</span><span class="sxs-lookup"><span data-stu-id="43d36-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="43d36-107">Отсылается диалоговым окном **открытия** или **сохранения в** стиле обозревателя, когда пользователь нажимает кнопку « **Справка** ».</span><span class="sxs-lookup"><span data-stu-id="43d36-107">Sent by an Explorer-style **Open** or **Save As** dialog box when the user clicks the **Help** button.</span></span>

<span data-ttu-id="43d36-108">Процедура обработчика [*офнхукпрок*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) получает это сообщение в виде сообщения [**WM \_ Notify**](../controls/wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="43d36-108">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_HELP                (CDN_FIRST - 0x0004)
```



## <a name="parameters"></a><span data-ttu-id="43d36-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="43d36-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43d36-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="43d36-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="43d36-111">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="43d36-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="43d36-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="43d36-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="43d36-113">Указатель на структуру [**офнотифи**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) .</span><span class="sxs-lookup"><span data-stu-id="43d36-113">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span> <span data-ttu-id="43d36-114">Структура **офнотифи** содержит структуру [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) , элемент **кода** которой указывает на сообщение с уведомлением в **\_ справке CDN** .</span><span class="sxs-lookup"><span data-stu-id="43d36-114">The **OFNOTIFY** structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_HELP** notification message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43d36-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="43d36-115">Return value</span></span>

<span data-ttu-id="43d36-116">Возвращаемое значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="43d36-116">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="43d36-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="43d36-117">Remarks</span></span>

<span data-ttu-id="43d36-118">Система отправляет это уведомление только в том случае, если диалоговое окно было создано с помощью значения **\_ обозревателя ОФН** .</span><span class="sxs-lookup"><span data-stu-id="43d36-118">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="43d36-119">Требования</span><span class="sxs-lookup"><span data-stu-id="43d36-119">Requirements</span></span>



| <span data-ttu-id="43d36-120">Требование</span><span class="sxs-lookup"><span data-stu-id="43d36-120">Requirement</span></span> | <span data-ttu-id="43d36-121">Значение</span><span class="sxs-lookup"><span data-stu-id="43d36-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43d36-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="43d36-122">Minimum supported client</span></span><br/> | <span data-ttu-id="43d36-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="43d36-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="43d36-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="43d36-124">Minimum supported server</span></span><br/> | <span data-ttu-id="43d36-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="43d36-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="43d36-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="43d36-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="43d36-127"><dt>Коммдлг. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="43d36-127"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43d36-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="43d36-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="43d36-129">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="43d36-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="43d36-130">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="43d36-130">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="43d36-131">**жетсавефиленаме**</span><span class="sxs-lookup"><span data-stu-id="43d36-131">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="43d36-132">*офнхукпрок*</span><span class="sxs-lookup"><span data-stu-id="43d36-132">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="43d36-133">**офнотифи**</span><span class="sxs-lookup"><span data-stu-id="43d36-133">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[<span data-ttu-id="43d36-134">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="43d36-134">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="43d36-135">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="43d36-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="43d36-136">Библиотека общих диалоговых окон</span><span class="sxs-lookup"><span data-stu-id="43d36-136">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 


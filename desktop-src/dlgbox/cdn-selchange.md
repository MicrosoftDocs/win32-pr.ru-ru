---
title: Код уведомления CDN_SELCHANGE (Коммдлг. h)
description: Отсылается диалоговым окном открытия или сохранения в стиле обозревателя при изменении выбора в списке, отображающем содержимое текущей открытой папки или каталога.
ms.assetid: e622babf-7024-45c5-a8db-f80896f69140
keywords:
- CDN_SELCHANGE диалоговых окон кода уведомления
topic_type:
- apiref
api_name:
- CDN_SELCHANGE
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5a5c7aed47d02fb7c7fcf2232b144e7a99e7c46
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590758"
---
# <a name="cdn_selchange-notification-code"></a><span data-ttu-id="7b7b7-104">\_Код уведомления СЕЛЧАНЖЕ CDN</span><span class="sxs-lookup"><span data-stu-id="7b7b7-104">CDN\_SELCHANGE notification code</span></span>

<span data-ttu-id="7b7b7-105">\[Начиная с Windows Vista, диалоговые окна " **Открыть** " и " **Сохранить как** " были заменены [диалоговым окном общих элементов](/windows/win32/shell/common-file-dialog).</span><span class="sxs-lookup"><span data-stu-id="7b7b7-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="7b7b7-106">Рекомендуется использовать API-интерфейс общего элемента, а не эти диалоговые окна из библиотеки общих диалоговых окон.\]</span><span class="sxs-lookup"><span data-stu-id="7b7b7-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="7b7b7-107">Отсылается диалоговым окном **открытия** или **сохранения** в стиле обозревателя при изменении выбора в списке, отображающем содержимое текущей открытой папки или каталога.</span><span class="sxs-lookup"><span data-stu-id="7b7b7-107">Sent by an Explorer-style **Open** or **Save As** dialog box when the selection changes in the list box that displays the contents of the currently opened folder or directory.</span></span>

<span data-ttu-id="7b7b7-108">Процедура обработчика [*офнхукпрок*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) получает это сообщение в виде сообщения [**WM \_ Notify**](../controls/wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="7b7b7-108">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_SELCHANGE           (CDN_FIRST - 0x0001)
#define CDN_FIRST               (0U-601U)
```



## <a name="parameters"></a><span data-ttu-id="7b7b7-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="7b7b7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b7b7-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7b7b7-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7b7b7-111">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="7b7b7-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7b7b7-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7b7b7-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7b7b7-113">Указатель на структуру [**офнотифи**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) .</span><span class="sxs-lookup"><span data-stu-id="7b7b7-113">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span> <span data-ttu-id="7b7b7-114">Структура **офнотифи** содержит структуру [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) , элемент **кода** которой указывает на сообщение **уведомления \_ селчанже CDN** .</span><span class="sxs-lookup"><span data-stu-id="7b7b7-114">The **OFNOTIFY** structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_SELCHANGE** notification message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b7b7-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7b7b7-115">Return value</span></span>

<span data-ttu-id="7b7b7-116">Возвращаемое значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="7b7b7-116">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b7b7-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="7b7b7-117">Remarks</span></span>

<span data-ttu-id="7b7b7-118">Система отправляет это уведомление только в том случае, если диалоговое окно было создано с помощью значения **\_ обозревателя ОФН** .</span><span class="sxs-lookup"><span data-stu-id="7b7b7-118">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

<span data-ttu-id="7b7b7-119">Чтобы получить имя только что выбранного файла или папки, процедура-обработчик может отправить сообщение CDM- [**\_ FilePath**](cdm-getfilepath.md) или CDM- [**\_ Spec**](cdm-getspec.md) в диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="7b7b7-119">To get the name of the newly selected file or folder, the hook procedure can send the [**CDM\_GETFILEPATH**](cdm-getfilepath.md) or [**CDM\_GETSPEC**](cdm-getspec.md) message to the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b7b7-120">Требования</span><span class="sxs-lookup"><span data-stu-id="7b7b7-120">Requirements</span></span>



| <span data-ttu-id="7b7b7-121">Требование</span><span class="sxs-lookup"><span data-stu-id="7b7b7-121">Requirement</span></span> | <span data-ttu-id="7b7b7-122">Значение</span><span class="sxs-lookup"><span data-stu-id="7b7b7-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b7b7-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7b7b7-123">Minimum supported client</span></span><br/> | <span data-ttu-id="7b7b7-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7b7b7-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="7b7b7-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7b7b7-125">Minimum supported server</span></span><br/> | <span data-ttu-id="7b7b7-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7b7b7-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7b7b7-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="7b7b7-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b7b7-128"><dt>Коммдлг. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7b7b7-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b7b7-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7b7b7-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="7b7b7-130">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="7b7b7-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7b7b7-131">**CDM. \_ FilePath**</span><span class="sxs-lookup"><span data-stu-id="7b7b7-131">**CDM\_GETFILEPATH**</span></span>](cdm-getfilepath.md)
</dt> <dt>

[<span data-ttu-id="7b7b7-132">**CDMая \_ Спецификация**</span><span class="sxs-lookup"><span data-stu-id="7b7b7-132">**CDM\_GETSPEC**</span></span>](cdm-getspec.md)
</dt> <dt>

[<span data-ttu-id="7b7b7-133">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="7b7b7-133">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="7b7b7-134">**жетсавефиленаме**</span><span class="sxs-lookup"><span data-stu-id="7b7b7-134">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="7b7b7-135">*офнхукпрок*</span><span class="sxs-lookup"><span data-stu-id="7b7b7-135">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="7b7b7-136">**офнотифи**</span><span class="sxs-lookup"><span data-stu-id="7b7b7-136">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

<span data-ttu-id="7b7b7-137">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="7b7b7-137">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7b7b7-138">Библиотека общих диалоговых окон</span><span class="sxs-lookup"><span data-stu-id="7b7b7-138">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 


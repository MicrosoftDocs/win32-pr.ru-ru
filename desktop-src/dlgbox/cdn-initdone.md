---
title: Код уведомления CDN_INITDONE (Коммдлг. h)
description: Отсылается диалоговым окном открытия или сохранения в стиле обозревателя, когда система завершает работу элементов управления в диалоговом окне. Система перемещает стандартные элементы управления, чтобы освободить место для элементов управления дочернего диалогового окна.
ms.assetid: 337fccac-5444-442d-92f0-862c5302fa21
keywords:
- CDN_INITDONE диалоговых окон кода уведомления
topic_type:
- apiref
api_name:
- CDN_INITDONE
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b07c25183eced86c3a430621091bed74c53f90d
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590801"
---
# <a name="cdn_initdone-notification-code"></a><span data-ttu-id="be9d4-105">\_Код уведомления ИНИТДОНЕ CDN</span><span class="sxs-lookup"><span data-stu-id="be9d4-105">CDN\_INITDONE notification code</span></span>

<span data-ttu-id="be9d4-106">\[Начиная с Windows Vista, диалоговые окна " **Открыть** " и " **Сохранить как** " были заменены [диалоговым окном общих элементов](/windows/win32/shell/common-file-dialog).</span><span class="sxs-lookup"><span data-stu-id="be9d4-106">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="be9d4-107">Рекомендуется использовать API-интерфейс общего элемента, а не эти диалоговые окна из библиотеки общих диалоговых окон.\]</span><span class="sxs-lookup"><span data-stu-id="be9d4-107">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="be9d4-108">Отсылается диалоговым окном **открытия** или **сохранения** в стиле обозревателя, когда система завершает работу элементов управления в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="be9d4-108">Sent by an Explorer-style **Open** or **Save As** dialog box when the system has finished arranging the controls in the dialog box.</span></span> <span data-ttu-id="be9d4-109">Система перемещает стандартные элементы управления, чтобы освободить место для элементов управления дочернего диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="be9d4-109">The system moves the standard controls to make room for the controls of the child dialog box.</span></span>

<span data-ttu-id="be9d4-110">Процедура обработчика [*офнхукпрок*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) получает это сообщение в виде сообщения [**WM \_ Notify**](../controls/wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="be9d4-110">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_INITDONE            (CDN_FIRST - 0x0000)
```



## <a name="parameters"></a><span data-ttu-id="be9d4-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="be9d4-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be9d4-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="be9d4-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="be9d4-113">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="be9d4-113">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="be9d4-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="be9d4-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="be9d4-115">Указатель на структуру [**офнотифи**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) .</span><span class="sxs-lookup"><span data-stu-id="be9d4-115">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span> <span data-ttu-id="be9d4-116">Структура **офнотифи** содержит структуру [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) , элемент **кода** которой указывает на сообщение **уведомления \_ инитдоне CDN** .</span><span class="sxs-lookup"><span data-stu-id="be9d4-116">The **OFNOTIFY** structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_INITDONE** notification message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be9d4-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="be9d4-117">Return value</span></span>

<span data-ttu-id="be9d4-118">Возвращаемое значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="be9d4-118">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="be9d4-119">Замечания</span><span class="sxs-lookup"><span data-stu-id="be9d4-119">Remarks</span></span>

<span data-ttu-id="be9d4-120">Система отправляет это уведомление только в том случае, если диалоговое окно было создано с помощью значения **\_ обозревателя ОФН** .</span><span class="sxs-lookup"><span data-stu-id="be9d4-120">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="be9d4-121">Требования</span><span class="sxs-lookup"><span data-stu-id="be9d4-121">Requirements</span></span>



| <span data-ttu-id="be9d4-122">Требование</span><span class="sxs-lookup"><span data-stu-id="be9d4-122">Requirement</span></span> | <span data-ttu-id="be9d4-123">Значение</span><span class="sxs-lookup"><span data-stu-id="be9d4-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be9d4-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="be9d4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="be9d4-125">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="be9d4-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="be9d4-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="be9d4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="be9d4-127">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="be9d4-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="be9d4-128">Заголовок</span><span class="sxs-lookup"><span data-stu-id="be9d4-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="be9d4-129"><dt>Коммдлг. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="be9d4-129"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be9d4-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="be9d4-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="be9d4-131">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="be9d4-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="be9d4-132">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="be9d4-132">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="be9d4-133">**жетсавефиленаме**</span><span class="sxs-lookup"><span data-stu-id="be9d4-133">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="be9d4-134">*офнхукпрок*</span><span class="sxs-lookup"><span data-stu-id="be9d4-134">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="be9d4-135">**офнотифи**</span><span class="sxs-lookup"><span data-stu-id="be9d4-135">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[<span data-ttu-id="be9d4-136">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="be9d4-136">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="be9d4-137">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="be9d4-137">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="be9d4-138">Библиотека общих диалоговых окон</span><span class="sxs-lookup"><span data-stu-id="be9d4-138">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 


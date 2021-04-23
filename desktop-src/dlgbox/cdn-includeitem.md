---
title: Код уведомления CDN_INCLUDEITEM (Коммдлг. h)
description: Отправляется диалоговым окном Открыть или сохранить как, чтобы определить, должно ли диалоговое окно отображать элемент в списке элементов в папке оболочки.
ms.assetid: 0972a78d-e058-4bac-85bd-fbd4c3885552
keywords:
- CDN_INCLUDEITEM диалоговых окон кода уведомления
topic_type:
- apiref
api_name:
- CDN_INCLUDEITEM
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a91c61e4a7c2786e67ed28e2c62e5963762659c
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590781"
---
# <a name="cdn_includeitem-notification-code"></a><span data-ttu-id="07954-104">\_Код уведомления ИНКЛУДЕИТЕМ CDN</span><span class="sxs-lookup"><span data-stu-id="07954-104">CDN\_INCLUDEITEM notification code</span></span>

<span data-ttu-id="07954-105">\[Начиная с Windows Vista, диалоговые окна " **Открыть** " и " **Сохранить как** " были заменены [диалоговым окном общих элементов](/windows/win32/shell/common-file-dialog).</span><span class="sxs-lookup"><span data-stu-id="07954-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="07954-106">Рекомендуется использовать API-интерфейс общего элемента, а не эти диалоговые окна из библиотеки общих диалоговых окон.\]</span><span class="sxs-lookup"><span data-stu-id="07954-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="07954-107">Отправляется диалоговым окном **Открыть** или **Сохранить как** , чтобы определить, должно ли диалоговое окно отображать элемент в списке элементов в папке оболочки.</span><span class="sxs-lookup"><span data-stu-id="07954-107">Sent by an **Open** or **Save As** dialog box to determine whether the dialog box should display an item in a shell folder's item list.</span></span> <span data-ttu-id="07954-108">Когда пользователь открывает папку, диалоговое окно отправляет уведомление **\_ инклудеитем CDN** для каждого элемента в папке.</span><span class="sxs-lookup"><span data-stu-id="07954-108">When the user opens a folder, the dialog box sends a **CDN\_INCLUDEITEM** notification for each item in the folder.</span></span> <span data-ttu-id="07954-109">Это уведомление отправляется в диалоговом окне только в том случае, если был установлен флаг **ОФН \_ енаблеинклуденотифи** при создании диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="07954-109">The dialog box sends this notification only if the **OFN\_ENABLEINCLUDENOTIFY** flag was set when the dialog box was created.</span></span>

<span data-ttu-id="07954-110">Процедура обработчика [*офнхукпрок*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) получает это сообщение в виде сообщения [**WM \_ Notify**](../controls/wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="07954-110">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_INCLUDEITEM         (CDN_FIRST - 0x0007)
```



## <a name="parameters"></a><span data-ttu-id="07954-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="07954-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07954-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="07954-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="07954-113">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="07954-113">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="07954-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="07954-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="07954-115">Указатель на структуру [**офнотифекс**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) .</span><span class="sxs-lookup"><span data-stu-id="07954-115">A pointer to an [**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) structure.</span></span>

<span data-ttu-id="07954-116">Структура [**офнотифекс**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) содержит структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , элемент **кода** которой указывает на сообщение **уведомления \_ инклудеитем CDN** .</span><span class="sxs-lookup"><span data-stu-id="07954-116">The [**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_INCLUDEITEM** notification message.</span></span>

<span data-ttu-id="07954-117">Элемент **ПСФ** структуры [**офнотифекс**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) является указателем на интерфейс для папки, элементы которой перечисляются.</span><span class="sxs-lookup"><span data-stu-id="07954-117">The **psf** member of the [**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) structure is a pointer to an interface for the folder whose items are being enumerated.</span></span> <span data-ttu-id="07954-118">Элемент **Пидл** является указателем на список идентификаторов элементов, который определяет элемент относительно папки.</span><span class="sxs-lookup"><span data-stu-id="07954-118">The **pidl** member is a pointer to an item identifier list that identifies the item relative to the folder.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07954-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="07954-119">Return value</span></span>

<span data-ttu-id="07954-120">Если процедура-обработчик [*офнхукпрок*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) возвращает значение 0, это диалоговое окно исключает элемент из списка элементов.</span><span class="sxs-lookup"><span data-stu-id="07954-120">If the [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure returns zero, the dialog box excludes the item from the list of items.</span></span>

<span data-ttu-id="07954-121">Чтобы включить элемент, возвратите ненулевое значение из процедуры-обработчика.</span><span class="sxs-lookup"><span data-stu-id="07954-121">To include the item, return a nonzero value from the hook procedure.</span></span>

## <a name="remarks"></a><span data-ttu-id="07954-122">Замечания</span><span class="sxs-lookup"><span data-stu-id="07954-122">Remarks</span></span>

<span data-ttu-id="07954-123">Диалоговое окно всегда включает элементы, содержащие атрибуты **сфгао \_ FILESYSTEM** и **\_ филесисанцестор сфгао** , независимо от значения, возвращаемого **CDN \_ инклудеитем**.</span><span class="sxs-lookup"><span data-stu-id="07954-123">The dialog box always includes items that have both the **SFGAO\_FILESYSTEM** and **SFGAO\_FILESYSANCESTOR** attributes, regardless of the value returned by **CDN\_INCLUDEITEM**.</span></span>

## <a name="requirements"></a><span data-ttu-id="07954-124">Требования</span><span class="sxs-lookup"><span data-stu-id="07954-124">Requirements</span></span>



| <span data-ttu-id="07954-125">Требование</span><span class="sxs-lookup"><span data-stu-id="07954-125">Requirement</span></span> | <span data-ttu-id="07954-126">Значение</span><span class="sxs-lookup"><span data-stu-id="07954-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07954-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="07954-127">Minimum supported client</span></span><br/> | <span data-ttu-id="07954-128">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="07954-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="07954-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="07954-129">Minimum supported server</span></span><br/> | <span data-ttu-id="07954-130">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="07954-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="07954-131">Заголовок</span><span class="sxs-lookup"><span data-stu-id="07954-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="07954-132"><dt>Коммдлг. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="07954-132"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07954-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="07954-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="07954-134">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="07954-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="07954-135">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="07954-135">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="07954-136">**жетсавефиленаме**</span><span class="sxs-lookup"><span data-stu-id="07954-136">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="07954-137">*офнхукпрок*</span><span class="sxs-lookup"><span data-stu-id="07954-137">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="07954-138">**офнотифекс**</span><span class="sxs-lookup"><span data-stu-id="07954-138">**OFNOTIFYEX**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa)
</dt> <dt>

<span data-ttu-id="07954-139">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="07954-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="07954-140">Библиотека общих диалоговых окон</span><span class="sxs-lookup"><span data-stu-id="07954-140">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 


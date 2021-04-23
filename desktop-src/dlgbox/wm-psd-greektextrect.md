---
title: Сообщение WM_PSD_GREEKTEXTRECT (Коммдлг. h)
description: Уведомляет процедуру-обработчик диалогового окна Параметры страницы, Пажепаинсук, что диалоговое окно собирается нарисовать Греческий текст внутри прямоугольника с примером страницы.
ms.assetid: ad0a200d-5626-4768-b3bd-73d4e3f0d548
keywords:
- WM_PSD_GREEKTEXTRECT диалоговых окон сообщений
topic_type:
- apiref
api_name:
- WM_PSD_GREEKTEXTRECT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd0853720bea8cadc8df40d8fa649f644fd00694
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071827"
---
# <a name="wm_psd_greektextrect-message"></a><span data-ttu-id="e4e78-104">\_Сообщение WM PSD \_ гриктекстрект</span><span class="sxs-lookup"><span data-stu-id="e4e78-104">WM\_PSD\_GREEKTEXTRECT message</span></span>

<span data-ttu-id="e4e78-105">Уведомляет процедуру-обработчик диалогового окна **Параметры страницы** , [*пажепаинсук*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook), что диалоговое окно собирается нарисовать Греческий текст внутри прямоугольника с примером страницы.</span><span class="sxs-lookup"><span data-stu-id="e4e78-105">Notifies the hook procedure of a **Page Setup** dialog box, [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook), that the dialog box is about to draw Greek text inside the margin rectangle of the sample page.</span></span>


```C++
#define WM_USER                  0x0400
#define WM_PSD_GREEKTEXTRECT    (WM_USER+4)
```



## <a name="parameters"></a><span data-ttu-id="e4e78-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e4e78-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4e78-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e4e78-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e4e78-108">Маркер контекста устройства для примера страницы.</span><span class="sxs-lookup"><span data-stu-id="e4e78-108">A handle to the device context for the sample page.</span></span>

</dd> <dt>

<span data-ttu-id="e4e78-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e4e78-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e4e78-110">Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) , содержащую координаты (в пикселях) текстового прямоугольника для греческого текста.</span><span class="sxs-lookup"><span data-stu-id="e4e78-110">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the coordinates, in pixels, of the Greek text rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4e78-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e4e78-111">Return value</span></span>

<span data-ttu-id="e4e78-112">Если процедура-обработчик возвращает **значение true**, то диалоговое окно не рисует текст на греческой части образца страницы.</span><span class="sxs-lookup"><span data-stu-id="e4e78-112">If the hook procedure returns **TRUE**, the dialog box does not draw the Greek text portion of the sample page.</span></span>

<span data-ttu-id="e4e78-113">Если процедура-обработчик возвращает **значение false**, то диалоговое окно рисует текст на греческой части образца страницы.</span><span class="sxs-lookup"><span data-stu-id="e4e78-113">If the hook procedure returns **FALSE**, the dialog box draws the Greek text portion of the sample page.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4e78-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e4e78-114">Remarks</span></span>

<span data-ttu-id="e4e78-115">Диалоговое окно **Параметры страницы** содержит изображение образца страницы, показывающее, как выбранные пользователем параметры влияют на внешний вид напечатанных данных.</span><span class="sxs-lookup"><span data-stu-id="e4e78-115">The **Page Setup** dialog box includes an image of a sample page that shows how the user's selections affect the appearance of the printed output.</span></span> <span data-ttu-id="e4e78-116">При вызове функции [**пажесетупдлг**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) можно предоставить процедуру-обработчик [*пажепаинсук*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) для настройки внешнего вида образца страницы.</span><span class="sxs-lookup"><span data-stu-id="e4e78-116">When you call the [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) function, you can provide a [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure to customize the appearance of the sample page.</span></span> <span data-ttu-id="e4e78-117">Каждый раз, когда диалоговое окно собирается вывести содержимое образца страницы, диалоговое окно отправляет последовательность сообщений в процедуру-обработчик.</span><span class="sxs-lookup"><span data-stu-id="e4e78-117">Whenever the dialog box is about to draw the contents of the sample page, the dialog box sends a sequence of messages to the hook procedure.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4e78-118">Требования</span><span class="sxs-lookup"><span data-stu-id="e4e78-118">Requirements</span></span>



| <span data-ttu-id="e4e78-119">Требование</span><span class="sxs-lookup"><span data-stu-id="e4e78-119">Requirement</span></span> | <span data-ttu-id="e4e78-120">Значение</span><span class="sxs-lookup"><span data-stu-id="e4e78-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4e78-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e4e78-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e4e78-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e4e78-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e4e78-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e4e78-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e4e78-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e4e78-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e4e78-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="e4e78-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4e78-126"><dt>Коммдлг. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e4e78-126"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4e78-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e4e78-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="e4e78-128">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="e4e78-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e4e78-129">*пажепаинсук*</span><span class="sxs-lookup"><span data-stu-id="e4e78-129">*PagePaintHook*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)
</dt> <dt>

<span data-ttu-id="e4e78-130">[**пажесетупдлг**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e4e78-130">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="e4e78-131">**WM \_ PSD \_ пажесетупдлг**</span><span class="sxs-lookup"><span data-stu-id="e4e78-131">**WM\_PSD\_PAGESETUPDLG**</span></span>](wm-psd-pagesetupdlg.md)
</dt> <dt>

<span data-ttu-id="e4e78-132">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="e4e78-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e4e78-133">Библиотека общих диалоговых окон</span><span class="sxs-lookup"><span data-stu-id="e4e78-133">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 


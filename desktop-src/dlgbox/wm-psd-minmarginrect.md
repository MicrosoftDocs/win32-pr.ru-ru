---
title: Сообщение WM_PSD_MINMARGINRECT (Коммдлг. h)
description: Уведомляет процедуру-обработчик Пажепаинсук о координатах прямоугольника поля на странице образца. Диалоговое окно «Параметры страницы» отправляет это сообщение, когда будет выводиться содержимое образца страницы.
ms.assetid: 14977b52-7a6f-4c55-956a-716398a71613
keywords:
- WM_PSD_MINMARGINRECT диалоговых окон сообщений
topic_type:
- apiref
api_name:
- WM_PSD_MINMARGINRECT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22ec7271026ba7557fcbe3fe17cd890d62eadbca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534724"
---
# <a name="wm_psd_minmarginrect-message"></a><span data-ttu-id="17387-105">\_Сообщение WM PSD \_ минмаргинрект</span><span class="sxs-lookup"><span data-stu-id="17387-105">WM\_PSD\_MINMARGINRECT message</span></span>

<span data-ttu-id="17387-106">Уведомляет процедуру-обработчик [*пажепаинсук*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) о координатах прямоугольника поля на странице образца.</span><span class="sxs-lookup"><span data-stu-id="17387-106">Notifies a [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure of the coordinates of the margin rectangle in the sample page.</span></span> <span data-ttu-id="17387-107">Диалоговое окно « **Параметры страницы** » отправляет это сообщение, когда будет выводиться содержимое образца страницы.</span><span class="sxs-lookup"><span data-stu-id="17387-107">A **Page Setup** dialog box sends this message when it is about to draw the contents of the sample page.</span></span>


```C++
#define WM_USER                  0x0400
#define WM_PSD_MINMARGINRECT    (WM_USER+2)
```



## <a name="parameters"></a><span data-ttu-id="17387-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="17387-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17387-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="17387-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="17387-110">Маркер контекста устройства для примера страницы.</span><span class="sxs-lookup"><span data-stu-id="17387-110">A handle to the device context for the sample page.</span></span>

</dd> <dt>

<span data-ttu-id="17387-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="17387-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="17387-112">Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) , содержащую координаты (в пикселях) прямоугольника минимального поля.</span><span class="sxs-lookup"><span data-stu-id="17387-112">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the coordinates, in pixels, of the minimum margin rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17387-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="17387-113">Return value</span></span>

<span data-ttu-id="17387-114">Если процедура-обработчик возвращает **значение true**, то диалоговое окно не отправляет никаких сообщений и не рисует его на образце страницы до тех пор, пока системе не потребуется перерисовать образец страницы.</span><span class="sxs-lookup"><span data-stu-id="17387-114">If the hook procedure returns **TRUE**, the dialog box sends no more messages and does not draw in the sample page until the next time the system needs to redraw the sample page.</span></span>

<span data-ttu-id="17387-115">Если процедура-обработчик возвращает **значение false**, то диалоговое окно отправляет оставшиеся сообщения последовательности отображения.</span><span class="sxs-lookup"><span data-stu-id="17387-115">If the hook procedure returns **FALSE**, the dialog box sends the remaining messages of the drawing sequence.</span></span>

## <a name="remarks"></a><span data-ttu-id="17387-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="17387-116">Remarks</span></span>

<span data-ttu-id="17387-117">Диалоговое окно **Параметры страницы** содержит изображение образца страницы, показывающее, как выбранные пользователем параметры влияют на внешний вид напечатанных данных.</span><span class="sxs-lookup"><span data-stu-id="17387-117">The **Page Setup** dialog box includes an image of a sample page that shows how the user's selections affect the appearance of the printed output.</span></span> <span data-ttu-id="17387-118">При вызове функции [**пажесетупдлг**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) можно предоставить процедуру-обработчик [*пажепаинсук*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) для настройки внешнего вида образца страницы.</span><span class="sxs-lookup"><span data-stu-id="17387-118">When you call the [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) function, you can provide a [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure to customize the appearance of the sample page.</span></span> <span data-ttu-id="17387-119">Каждый раз, когда диалоговое окно собирается вывести содержимое образца страницы, диалоговое окно отправляет последовательность сообщений в процедуру-обработчик.</span><span class="sxs-lookup"><span data-stu-id="17387-119">Whenever the dialog box is about to draw the contents of the sample page, the dialog box sends a sequence of messages to the hook procedure.</span></span>

## <a name="requirements"></a><span data-ttu-id="17387-120">Требования</span><span class="sxs-lookup"><span data-stu-id="17387-120">Requirements</span></span>



| <span data-ttu-id="17387-121">Требование</span><span class="sxs-lookup"><span data-stu-id="17387-121">Requirement</span></span> | <span data-ttu-id="17387-122">Значение</span><span class="sxs-lookup"><span data-stu-id="17387-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17387-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="17387-123">Minimum supported client</span></span><br/> | <span data-ttu-id="17387-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="17387-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="17387-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="17387-125">Minimum supported server</span></span><br/> | <span data-ttu-id="17387-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="17387-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="17387-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="17387-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="17387-128"><dt>Коммдлг. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="17387-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17387-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="17387-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="17387-130">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="17387-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="17387-131">*пажепаинсук*</span><span class="sxs-lookup"><span data-stu-id="17387-131">*PagePaintHook*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)
</dt> <dt>

<span data-ttu-id="17387-132">[**пажесетупдлг**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="17387-132">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="17387-133">**WM \_ PSD \_ пажесетупдлг**</span><span class="sxs-lookup"><span data-stu-id="17387-133">**WM\_PSD\_PAGESETUPDLG**</span></span>](wm-psd-pagesetupdlg.md)
</dt> <dt>

<span data-ttu-id="17387-134">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="17387-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="17387-135">Библиотека общих диалоговых окон</span><span class="sxs-lookup"><span data-stu-id="17387-135">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 


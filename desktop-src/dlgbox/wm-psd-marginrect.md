---
title: Сообщение WM_PSD_MARGINRECT (Коммдлг. h)
description: Уведомляет процедуру-обработчик диалогового окна Параметры страницы, Пажепаинсук, что диалоговое окно собирается отобразить прямоугольник поля образца страницы.
ms.assetid: 81c057ab-6faf-4dd8-8b0c-34a2753e572c
keywords:
- WM_PSD_MARGINRECT диалоговых окон сообщений
topic_type:
- apiref
api_name:
- WM_PSD_MARGINRECT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4718cfbe16db53378544d9fca0ab44ade23ffb3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491859"
---
# <a name="wm_psd_marginrect-message"></a><span data-ttu-id="6a1b8-104">\_Сообщение WM PSD \_ маргинрект</span><span class="sxs-lookup"><span data-stu-id="6a1b8-104">WM\_PSD\_MARGINRECT message</span></span>

<span data-ttu-id="6a1b8-105">Уведомляет процедуру-обработчик диалогового окна **Параметры страницы** , [**пажепаинсук**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook), что диалоговое окно собирается отобразить прямоугольник поля образца страницы.</span><span class="sxs-lookup"><span data-stu-id="6a1b8-105">Notifies the hook procedure of a **Page Setup** dialog box, [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook), that the dialog box is about to draw the margin rectangle of the sample page.</span></span>


```C++
#define WM_USER                  0x0400
#define WM_PSD_MARGINRECT       (WM_USER+3)
```



## <a name="parameters"></a><span data-ttu-id="6a1b8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6a1b8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a1b8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6a1b8-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6a1b8-108">Маркер контекста устройства для примера страницы.</span><span class="sxs-lookup"><span data-stu-id="6a1b8-108">A handle to the device context for the sample page.</span></span>

</dd> <dt>

<span data-ttu-id="6a1b8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6a1b8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6a1b8-110">Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) , содержащую координаты прямоугольника поля в пикселях.</span><span class="sxs-lookup"><span data-stu-id="6a1b8-110">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the coordinates, in pixels, of the margin rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a1b8-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6a1b8-111">Return value</span></span>

<span data-ttu-id="6a1b8-112">Если процедура-обработчик возвращает **значение true**, то диалоговое окно не рисует прямоугольник поля на странице выборки.</span><span class="sxs-lookup"><span data-stu-id="6a1b8-112">If the hook procedure returns **TRUE**, the dialog box does not draw the margin rectangle in the sample page.</span></span>

<span data-ttu-id="6a1b8-113">Если процедура-обработчик возвращает **значение false**, то диалоговое окно рисует прямоугольник поля на странице выборки.</span><span class="sxs-lookup"><span data-stu-id="6a1b8-113">If the hook procedure returns **FALSE**, the dialog box draws the margin rectangle in the sample page.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a1b8-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6a1b8-114">Remarks</span></span>

<span data-ttu-id="6a1b8-115">Диалоговое окно **Параметры страницы** содержит изображение образца страницы, показывающее, как выбранные пользователем параметры влияют на внешний вид напечатанных данных.</span><span class="sxs-lookup"><span data-stu-id="6a1b8-115">The **Page Setup** dialog box includes an image of a sample page that shows how the user's selections affect the appearance of the printed output.</span></span> <span data-ttu-id="6a1b8-116">При вызове функции [**пажесетупдлг**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) можно предоставить процедуру-обработчик [*пажепаинсук*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) для настройки внешнего вида образца страницы.</span><span class="sxs-lookup"><span data-stu-id="6a1b8-116">When you call the [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) function, you can provide a [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure to customize the appearance of the sample page.</span></span> <span data-ttu-id="6a1b8-117">Каждый раз, когда диалоговое окно собирается вывести содержимое образца страницы, диалоговое окно отправляет последовательность сообщений в процедуру-обработчик.</span><span class="sxs-lookup"><span data-stu-id="6a1b8-117">Whenever the dialog box is about to draw the contents of the sample page, the dialog box sends a sequence of messages to the hook procedure.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a1b8-118">Требования</span><span class="sxs-lookup"><span data-stu-id="6a1b8-118">Requirements</span></span>



| <span data-ttu-id="6a1b8-119">Требование</span><span class="sxs-lookup"><span data-stu-id="6a1b8-119">Requirement</span></span> | <span data-ttu-id="6a1b8-120">Значение</span><span class="sxs-lookup"><span data-stu-id="6a1b8-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a1b8-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6a1b8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6a1b8-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6a1b8-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="6a1b8-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6a1b8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6a1b8-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6a1b8-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6a1b8-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="6a1b8-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a1b8-126"><dt>Коммдлг. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6a1b8-126"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a1b8-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6a1b8-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="6a1b8-128">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="6a1b8-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6a1b8-129">*пажепаинсук*</span><span class="sxs-lookup"><span data-stu-id="6a1b8-129">*PagePaintHook*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)
</dt> <dt>

<span data-ttu-id="6a1b8-130">[**пажесетупдлг**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6a1b8-130">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="6a1b8-131">**WM \_ PSD \_ пажесетупдлг**</span><span class="sxs-lookup"><span data-stu-id="6a1b8-131">**WM\_PSD\_PAGESETUPDLG**</span></span>](wm-psd-pagesetupdlg.md)
</dt> <dt>

<span data-ttu-id="6a1b8-132">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="6a1b8-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6a1b8-133">Библиотека общих диалоговых окон</span><span class="sxs-lookup"><span data-stu-id="6a1b8-133">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 


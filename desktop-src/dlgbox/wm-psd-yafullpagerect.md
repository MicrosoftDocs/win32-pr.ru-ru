---
title: Сообщение WM_PSD_YAFULLPAGERECT (Коммдлг. h)
description: Уведомляет процедуру-обработчик диалогового окна Параметры страницы, Пажепаинсук, что диалоговое окно собирается отобразить часть возвращаемого адреса на странице образца конверта.
ms.assetid: 1f6aea69-a1bd-41ea-b508-44b4f5c38757
keywords:
- WM_PSD_YAFULLPAGERECT диалоговых окон сообщений
topic_type:
- apiref
api_name:
- WM_PSD_YAFULLPAGERECT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb325a8d408724cd865f5f9b70cfe7369fe6ffe6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071977"
---
# <a name="wm_psd_yafullpagerect-message"></a><span data-ttu-id="b1cc4-104">\_Сообщение WM PSD \_ яфуллпажерект</span><span class="sxs-lookup"><span data-stu-id="b1cc4-104">WM\_PSD\_YAFULLPAGERECT message</span></span>

<span data-ttu-id="b1cc4-105">Уведомляет процедуру-обработчик диалогового окна **Параметры страницы** , [*пажепаинсук*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook), что диалоговое окно собирается отобразить часть возвращаемого адреса на странице образца конверта.</span><span class="sxs-lookup"><span data-stu-id="b1cc4-105">Notifies the hook procedure of a **Page Setup** dialog box, [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook), that the dialog box is about to draw the return address portion of an envelope sample page.</span></span>


```C++
#define WM_USER                  0x0400
#define WM_PSD_YAFULLPAGERECT   (WM_USER+6)
```



## <a name="parameters"></a><span data-ttu-id="b1cc4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b1cc4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1cc4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b1cc4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b1cc4-108">Маркер контекста устройства для примера страницы.</span><span class="sxs-lookup"><span data-stu-id="b1cc4-108">A handle to the device context for the sample page.</span></span>

</dd> <dt>

<span data-ttu-id="b1cc4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b1cc4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b1cc4-110">Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) , содержащую координаты образца страницы (в пикселях).</span><span class="sxs-lookup"><span data-stu-id="b1cc4-110">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the coordinates, in pixels, of the sample page.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1cc4-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b1cc4-111">Return value</span></span>

<span data-ttu-id="b1cc4-112">Если процедура-обработчик возвращает **значение true**, то диалоговое окно не рисует часть возвращаемого адреса на странице образца конверта.</span><span class="sxs-lookup"><span data-stu-id="b1cc4-112">If the hook procedure returns **TRUE**, the dialog box does not draw the return address portion of an envelope sample page.</span></span>

<span data-ttu-id="b1cc4-113">Если процедура-обработчик возвращает **значение false**, в диалоговом окне выводится часть возвращаемого адреса из образца страницы "Конверт".</span><span class="sxs-lookup"><span data-stu-id="b1cc4-113">If the hook procedure returns **FALSE**, the dialog box draws the return address portion of an envelope sample page.</span></span>

<span data-ttu-id="b1cc4-114">Если тип бумаги не является конвертом, возвращаемое значение не действует.</span><span class="sxs-lookup"><span data-stu-id="b1cc4-114">If the paper type is not an envelope, the return value has no effect.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1cc4-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b1cc4-115">Remarks</span></span>

<span data-ttu-id="b1cc4-116">Диалоговое окно **Параметры страницы** содержит изображение образца страницы, показывающее, как выбранные пользователем параметры влияют на внешний вид напечатанных данных.</span><span class="sxs-lookup"><span data-stu-id="b1cc4-116">The **Page Setup** dialog box includes an image of a sample page that shows how the user's selections affect the appearance of the printed output.</span></span> <span data-ttu-id="b1cc4-117">При вызове функции [**пажесетупдлг**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) можно предоставить процедуру-обработчик [*пажепаинсук*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) для настройки внешнего вида образца страницы.</span><span class="sxs-lookup"><span data-stu-id="b1cc4-117">When you call the [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) function, you can provide a [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure to customize the appearance of the sample page.</span></span> <span data-ttu-id="b1cc4-118">Каждый раз, когда диалоговое окно собирается вывести содержимое образца страницы, диалоговое окно отправляет последовательность сообщений в процедуру-обработчик.</span><span class="sxs-lookup"><span data-stu-id="b1cc4-118">Whenever the dialog box is about to draw the contents of the sample page, the dialog box sends a sequence of messages to the hook procedure.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1cc4-119">Требования</span><span class="sxs-lookup"><span data-stu-id="b1cc4-119">Requirements</span></span>



| <span data-ttu-id="b1cc4-120">Требование</span><span class="sxs-lookup"><span data-stu-id="b1cc4-120">Requirement</span></span> | <span data-ttu-id="b1cc4-121">Значение</span><span class="sxs-lookup"><span data-stu-id="b1cc4-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1cc4-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b1cc4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b1cc4-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b1cc4-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b1cc4-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b1cc4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b1cc4-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b1cc4-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b1cc4-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b1cc4-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1cc4-127"><dt>Коммдлг. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b1cc4-127"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1cc4-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b1cc4-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="b1cc4-129">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="b1cc4-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b1cc4-130">*пажепаинсук*</span><span class="sxs-lookup"><span data-stu-id="b1cc4-130">*PagePaintHook*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)
</dt> <dt>

<span data-ttu-id="b1cc4-131">[**пажесетупдлг**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b1cc4-131">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="b1cc4-132">**WM \_ PSD \_ пажесетупдлг**</span><span class="sxs-lookup"><span data-stu-id="b1cc4-132">**WM\_PSD\_PAGESETUPDLG**</span></span>](wm-psd-pagesetupdlg.md)
</dt> <dt>

<span data-ttu-id="b1cc4-133">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="b1cc4-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b1cc4-134">Библиотека общих диалоговых окон</span><span class="sxs-lookup"><span data-stu-id="b1cc4-134">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 


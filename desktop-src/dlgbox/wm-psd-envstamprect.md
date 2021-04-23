---
title: Сообщение WM_PSD_ENVSTAMPRECT (Коммдлг. h)
description: Уведомляет процедуру-обработчик диалогового окна Параметры страницы, Пажепаинсук, что диалоговое окно собирается отобразить прямоугольник метки конверта страницы образца.
ms.assetid: f193baa0-a084-416e-90c9-9c838758a3d3
keywords:
- WM_PSD_ENVSTAMPRECT диалоговых окон сообщений
topic_type:
- apiref
api_name:
- WM_PSD_ENVSTAMPRECT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf13485ab75f51298ef273c7e02ea0253e4244d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491862"
---
# <a name="wm_psd_envstamprect-message"></a><span data-ttu-id="9f899-104">\_Сообщение WM PSD \_ енвстампрект</span><span class="sxs-lookup"><span data-stu-id="9f899-104">WM\_PSD\_ENVSTAMPRECT message</span></span>

<span data-ttu-id="9f899-105">Уведомляет процедуру-обработчик диалогового окна **Параметры страницы** , [*пажепаинсук*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook), что диалоговое окно собирается отобразить прямоугольник метки конверта страницы образца.</span><span class="sxs-lookup"><span data-stu-id="9f899-105">Notifies the hook procedure of a **Page Setup** dialog box, [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook), that the dialog box is about to draw the envelope-stamp rectangle of the sample page.</span></span>


```C++
#define WM_USER                  0x0400
#define WM_PSD_ENVSTAMPRECT     (WM_USER+5)
```



## <a name="parameters"></a><span data-ttu-id="9f899-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9f899-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f899-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9f899-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9f899-108">Маркер контекста устройства для примера страницы.</span><span class="sxs-lookup"><span data-stu-id="9f899-108">A handle to the device context for the sample page.</span></span>

</dd> <dt>

<span data-ttu-id="9f899-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9f899-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9f899-110">Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) , которая содержит координаты (в пикселях) прямоугольника метки конверта.</span><span class="sxs-lookup"><span data-stu-id="9f899-110">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the coordinates, in pixels, of the envelope-stamp rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f899-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9f899-111">Return value</span></span>

<span data-ttu-id="9f899-112">Если процедура-обработчик возвращает **значение true**, то диалоговое окно не рисует часть метки конверта на странице выборки.</span><span class="sxs-lookup"><span data-stu-id="9f899-112">If the hook procedure returns **TRUE**, the dialog box does not draw the envelope-stamp portion of the sample page.</span></span>

<span data-ttu-id="9f899-113">Если процедура-обработчик возвращает **значение false**, то в диалоговом окне на странице выводится часть метки конверта.</span><span class="sxs-lookup"><span data-stu-id="9f899-113">If the hook procedure returns **FALSE**, the dialog box draws the envelope-stamp portion of the sample page.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f899-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9f899-114">Remarks</span></span>

<span data-ttu-id="9f899-115">Диалоговое окно **Параметры страницы** содержит изображение образца страницы, показывающее, как выбранные пользователем параметры влияют на внешний вид напечатанных данных.</span><span class="sxs-lookup"><span data-stu-id="9f899-115">The **Page Setup** dialog box includes an image of a sample page that shows how the user's selections affect the appearance of the printed output.</span></span> <span data-ttu-id="9f899-116">При вызове функции [**пажесетупдлг**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) можно предоставить процедуру-обработчик [*пажепаинсук*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) для настройки внешнего вида образца страницы.</span><span class="sxs-lookup"><span data-stu-id="9f899-116">When you call the [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) function, you can provide a [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure to customize the appearance of the sample page.</span></span> <span data-ttu-id="9f899-117">Каждый раз, когда диалоговое окно собирается вывести содержимое образца страницы, диалоговое окно отправляет последовательность сообщений в процедуру-обработчик.</span><span class="sxs-lookup"><span data-stu-id="9f899-117">Whenever the dialog box is about to draw the contents of the sample page, the dialog box sends a sequence of messages to the hook procedure.</span></span>

<span data-ttu-id="9f899-118">Процедура-обработчик получает это сообщение, только если выбранный тип бумаги является конвертом.</span><span class="sxs-lookup"><span data-stu-id="9f899-118">A hook procedure receives this message only if the selected paper type is an envelope.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f899-119">Требования</span><span class="sxs-lookup"><span data-stu-id="9f899-119">Requirements</span></span>



| <span data-ttu-id="9f899-120">Требование</span><span class="sxs-lookup"><span data-stu-id="9f899-120">Requirement</span></span> | <span data-ttu-id="9f899-121">Значение</span><span class="sxs-lookup"><span data-stu-id="9f899-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f899-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9f899-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9f899-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9f899-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="9f899-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9f899-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9f899-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9f899-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9f899-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="9f899-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f899-127"><dt>Коммдлг. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9f899-127"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f899-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9f899-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="9f899-129">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="9f899-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9f899-130">*пажепаинсук*</span><span class="sxs-lookup"><span data-stu-id="9f899-130">*PagePaintHook*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)
</dt> <dt>

<span data-ttu-id="9f899-131">[**пажесетупдлг**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9f899-131">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="9f899-132">**WM \_ PSD \_ пажесетупдлг**</span><span class="sxs-lookup"><span data-stu-id="9f899-132">**WM\_PSD\_PAGESETUPDLG**</span></span>](wm-psd-pagesetupdlg.md)
</dt> <dt>

<span data-ttu-id="9f899-133">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="9f899-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9f899-134">Библиотека общих диалоговых окон</span><span class="sxs-lookup"><span data-stu-id="9f899-134">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 


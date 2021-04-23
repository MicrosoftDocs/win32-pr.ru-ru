---
title: Сообщение WM_DWMSENDICONICLIVEPREVIEWBITMAP (Двмапи. h)
description: Указывает окну указать статический точечный рисунок для использования в качестве динамического предварительного просмотра (также известного как предварительный просмотр) этого окна.
ms.assetid: 24bf3b42-a850-4aa5-966a-29baab6b4d21
keywords:
- Сообщение WM_DWMSENDICONICLIVEPREVIEWBITMAP диспетчер окон рабочего стола
topic_type:
- apiref
api_name:
- WM_DWMSENDICONICLIVEPREVIEWBITMAP
api_location:
- Dwmapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21f73076ab313da66171bc8265f7f4e7d068f93e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490893"
---
# <a name="wm_dwmsendiconiclivepreviewbitmap-message"></a><span data-ttu-id="af8b6-104">\_Сообщение ДВМСЕНДИКОНИКЛИВЕПРЕВИЕВБИТМАП WM</span><span class="sxs-lookup"><span data-stu-id="af8b6-104">WM\_DWMSENDICONICLIVEPREVIEWBITMAP message</span></span>

<span data-ttu-id="af8b6-105">Указывает окну указать статический точечный рисунок для использования в качестве *динамического предварительного просмотра* (также известного как *Предварительный просмотр*) этого окна.</span><span class="sxs-lookup"><span data-stu-id="af8b6-105">Instructs a window to provide a static bitmap to use as a *live preview* (also known as a *Peek preview*) of that window.</span></span>

## <a name="parameters"></a><span data-ttu-id="af8b6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="af8b6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af8b6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="af8b6-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="af8b6-108">Не используется.</span><span class="sxs-lookup"><span data-stu-id="af8b6-108">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="af8b6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="af8b6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="af8b6-110">Не используется.</span><span class="sxs-lookup"><span data-stu-id="af8b6-110">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af8b6-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="af8b6-111">Return value</span></span>

<span data-ttu-id="af8b6-112">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="af8b6-112">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="af8b6-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="af8b6-113">Remarks</span></span>

<span data-ttu-id="af8b6-114">*Динамический просмотр* (также называемый *предварительным просмотром*) окна появляется, когда пользователь перемещает указатель мыши над эскизом окна на панели задач или передает фокус в окно ALT + TAB.</span><span class="sxs-lookup"><span data-stu-id="af8b6-114">A *live preview* (also known as a *Peek preview*) of a window appears when a user moves the mouse pointer over the window's thumbnail in the taskbar or gives the thumbnail focus in the ALT+TAB window.</span></span> <span data-ttu-id="af8b6-115">Это представление является полным предварительным просмотром окна и может быть динамическим моментальным снимком или значком.</span><span class="sxs-lookup"><span data-stu-id="af8b6-115">This view is a full-sized preview of the window and can be a live snapshot or an iconic representation.</span></span>

<span data-ttu-id="af8b6-116">Диспетчер окон рабочего стола (DWM) отправляет это сообщение в окно, если выполняются все следующие ситуации:</span><span class="sxs-lookup"><span data-stu-id="af8b6-116">Desktop Window Manager (DWM) sends this message to a window if all of the following situations are true:</span></span>

-   <span data-ttu-id="af8b6-117">В окне был вызван динамический просмотр.</span><span class="sxs-lookup"><span data-stu-id="af8b6-117">Live preview has been invoked on the window.</span></span>
-   <span data-ttu-id="af8b6-118">В окне задан атрибут [**\_ \_ \_ Bitmap двмва**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) .</span><span class="sxs-lookup"><span data-stu-id="af8b6-118">The [**DWMWA\_HAS\_ICONIC\_BITMAP**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) attribute is set on the window.</span></span>
-   <span data-ttu-id="af8b6-119">Для этого окна существует только значок.</span><span class="sxs-lookup"><span data-stu-id="af8b6-119">An iconic representation is the only one that exists for this window.</span></span>

<span data-ttu-id="af8b6-120">Окно, которое получает это сообщение, должно реагировать путем создания полной масштабируемой битовой карты.</span><span class="sxs-lookup"><span data-stu-id="af8b6-120">The window that receives this message should respond by generating a full-scale bitmap.</span></span> <span data-ttu-id="af8b6-121">Затем окно вызывает функцию [**двмсетиконикливепревиевбитмап**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) для задания динамического просмотра.</span><span class="sxs-lookup"><span data-stu-id="af8b6-121">The window then calls the [**DwmSetIconicLivePreviewBitmap**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) function to set the live preview.</span></span> <span data-ttu-id="af8b6-122">Если окно не устанавливает точечный рисунок в течение заданного промежутка времени, DWM использует собственный значок по умолчанию для окна.</span><span class="sxs-lookup"><span data-stu-id="af8b6-122">If the window does not set a bitmap in a given amount of time, DWM uses its own default iconic representation for the window.</span></span>

## <a name="examples"></a><span data-ttu-id="af8b6-123">Примеры</span><span class="sxs-lookup"><span data-stu-id="af8b6-123">Examples</span></span>

<span data-ttu-id="af8b6-124">В следующем примере демонстрируется ответ на сообщение **\_ двмсендиконикливепревиевбитмап WM** .</span><span class="sxs-lookup"><span data-stu-id="af8b6-124">The following example demonstrates a response to the **WM\_DWMSENDICONICLIVEPREVIEWBITMAP** message.</span></span> <span data-ttu-id="af8b6-125">В примере вызывается функция [**двмсетиконикливепревиевбитмап**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) с маркером для настраиваемого, независимого от устройства точечного рисунка, используемого в качестве представления окна.</span><span class="sxs-lookup"><span data-stu-id="af8b6-125">The example calls the [**DwmSetIconicLivePreviewBitmap**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) function with a handle to a customized, device-independent bitmap to use as the window's representation.</span></span>


```C++
        case WM_DWMSENDICONICLIVEPREVIEWBITMAP:
        {
            // This window is being asked to provide a bitmap to show in Peek preview.
            // This indicates the thumbnail in the taskbar is being previewed.
            RECT rectWindow = {0, 0, 0, 0};
            if (GetClientRect(hwnd, &rectWindow))
            {
                nWidth = rectWindow.right - rectWindow.left;
                nHeight = rectWindow.bottom - rectWindow.top;
            }

            hbm = CreateDIB(nWidth, nHeight);
            if (hbm)
            {
                hr = DwmSetIconicLivePreviewBitmap(hwnd, hbm, NULL, DWM_SIT_DISPLAYFRAME);
                DeleteObject(hbm);
            }
        }
        break;
```



<span data-ttu-id="af8b6-126">Полный код см. в разделе [Настройка эскиза значка и пример динамического предварительного просмотра растрового изображения](dwm-sample-customizethumbnail.md) .</span><span class="sxs-lookup"><span data-stu-id="af8b6-126">For the complete code, see the [Customize an Iconic Thumbnail and a Live Preview Bitmap](dwm-sample-customizethumbnail.md) sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="af8b6-127">Требования</span><span class="sxs-lookup"><span data-stu-id="af8b6-127">Requirements</span></span>



| <span data-ttu-id="af8b6-128">Требование</span><span class="sxs-lookup"><span data-stu-id="af8b6-128">Requirement</span></span> | <span data-ttu-id="af8b6-129">Значение</span><span class="sxs-lookup"><span data-stu-id="af8b6-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="af8b6-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="af8b6-130">Minimum supported client</span></span><br/> | <span data-ttu-id="af8b6-131">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="af8b6-131">Windows 7 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="af8b6-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="af8b6-132">Minimum supported server</span></span><br/> | <span data-ttu-id="af8b6-133">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="af8b6-133">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="af8b6-134">Header</span><span class="sxs-lookup"><span data-stu-id="af8b6-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="af8b6-135"><dt>Двмапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="af8b6-135"><dt>Dwmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af8b6-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="af8b6-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af8b6-137">**WM \_ двмсендикониксумбнаил**</span><span class="sxs-lookup"><span data-stu-id="af8b6-137">**WM\_DWMSENDICONICTHUMBNAIL**</span></span>](wm-dwmsendiconicthumbnail.md)
</dt> <dt>

[<span data-ttu-id="af8b6-138">**двминвалидатеиконикбитмапс**</span><span class="sxs-lookup"><span data-stu-id="af8b6-138">**DwmInvalidateIconicBitmaps**</span></span>](/windows/desktop/api/Dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps)
</dt> </dl>

 

 






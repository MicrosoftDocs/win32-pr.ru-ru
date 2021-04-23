---
title: Сообщение WM_DWMSENDICONICTHUMBNAIL (Двмапи. h)
description: Указывает окну указать статический точечный рисунок для использования в качестве эскиза этого окна.
ms.assetid: 476c2542-f4d0-4777-93d3-bf50da26d94f
keywords:
- Сообщение WM_DWMSENDICONICTHUMBNAIL диспетчер окон рабочего стола
topic_type:
- apiref
api_name:
- WM_DWMSENDICONICTHUMBNAIL
api_location:
- Dwmapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ded5b734278973afe35f5ed3d9fbb5b0aec9242b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492657"
---
# <a name="wm_dwmsendiconicthumbnail-message"></a><span data-ttu-id="8e3a2-104">\_Сообщение ДВМСЕНДИКОНИКСУМБНАИЛ WM</span><span class="sxs-lookup"><span data-stu-id="8e3a2-104">WM\_DWMSENDICONICTHUMBNAIL message</span></span>

<span data-ttu-id="8e3a2-105">Указывает окну указать статический точечный рисунок для использования в качестве эскиза этого окна.</span><span class="sxs-lookup"><span data-stu-id="8e3a2-105">Instructs a window to provide a static bitmap to use as a thumbnail representation of that window.</span></span>

## <a name="parameters"></a><span data-ttu-id="8e3a2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8e3a2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e3a2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8e3a2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8e3a2-108">Не используется.</span><span class="sxs-lookup"><span data-stu-id="8e3a2-108">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="8e3a2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8e3a2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8e3a2-110">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) этого значения — это максимальная координата x эскиза.</span><span class="sxs-lookup"><span data-stu-id="8e3a2-110">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) of this value is the maximum x-coordinate of the thumbnail.</span></span> <span data-ttu-id="8e3a2-111">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) — это максимальная координата по оси y.</span><span class="sxs-lookup"><span data-stu-id="8e3a2-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is the maximum y-coordinate.</span></span> <span data-ttu-id="8e3a2-112">Если размер эскиза превышает одно или оба этих значения, DWM не принимает эскиз.</span><span class="sxs-lookup"><span data-stu-id="8e3a2-112">If a thumbnail has a dimension that exceeds one or both of these values, the DWM does not accept the thumbnail.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e3a2-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8e3a2-113">Return value</span></span>

<span data-ttu-id="8e3a2-114">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="8e3a2-114">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e3a2-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8e3a2-115">Remarks</span></span>

<span data-ttu-id="8e3a2-116">DWM отправляет это сообщение в окно, если выполняются все перечисленные ниже ситуации.</span><span class="sxs-lookup"><span data-stu-id="8e3a2-116">DWM sends this message to a window if all of the following situations are true:</span></span>

-   <span data-ttu-id="8e3a2-117">DWM отображает значок окна.</span><span class="sxs-lookup"><span data-stu-id="8e3a2-117">DWM is displaying an iconic representation of the window.</span></span>
-   <span data-ttu-id="8e3a2-118">В окне задан атрибут [**\_ \_ \_ Bitmap двмва**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) .</span><span class="sxs-lookup"><span data-stu-id="8e3a2-118">The [**DWMWA\_HAS\_ICONIC\_BITMAP**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) attribute is set on the window.</span></span>
-   <span data-ttu-id="8e3a2-119">Окно не установило кэшированный точечный рисунок.</span><span class="sxs-lookup"><span data-stu-id="8e3a2-119">The window did not set a cached bitmap.</span></span>
-   <span data-ttu-id="8e3a2-120">Существует место в кэше для другого точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="8e3a2-120">There is room in the cache for another bitmap.</span></span>

<span data-ttu-id="8e3a2-121">Окно, которое получает это сообщение, должно ответить путем создания точечного рисунка, размер которого не превышает размера, запрошенного в параметрах сообщения.</span><span class="sxs-lookup"><span data-stu-id="8e3a2-121">The window that receives this message should respond by generating a bitmap that is not larger than the size that is requested in the message parameters.</span></span> <span data-ttu-id="8e3a2-122">Затем окно вызывает функцию [**двмсетикониксумбнаил**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail) для переопределения эскиза по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8e3a2-122">The window then calls the [**DwmSetIconicThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail) function to override the default thumbnail.</span></span> <span data-ttu-id="8e3a2-123">Если окно не предоставляет точечный рисунок в течение заданного промежутка времени, DWM использует собственный значок по умолчанию для окна.</span><span class="sxs-lookup"><span data-stu-id="8e3a2-123">If the window does not supply a bitmap in a given amount of time, DWM uses its own default iconic representation for the window.</span></span>

<span data-ttu-id="8e3a2-124">Окно должно принадлежать вызывающему процессу.</span><span class="sxs-lookup"><span data-stu-id="8e3a2-124">The window must belong to the calling process.</span></span>

## <a name="examples"></a><span data-ttu-id="8e3a2-125">Примеры</span><span class="sxs-lookup"><span data-stu-id="8e3a2-125">Examples</span></span>

<span data-ttu-id="8e3a2-126">В следующем примере кода показано, как реагировать на сообщение **WM \_ двмсендикониксумбнаил** .</span><span class="sxs-lookup"><span data-stu-id="8e3a2-126">The following code example shows how to respond to the **WM\_DWMSENDICONICTHUMBNAIL** message.</span></span> <span data-ttu-id="8e3a2-127">В примере вызывается [**двмсетикониксумбнаил**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail)с маркером для настраиваемого аппаратно-независимого точечного рисунка, используемого в качестве представления Windows.</span><span class="sxs-lookup"><span data-stu-id="8e3a2-127">The example calls [**DwmSetIconicThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail), with a handle to a customized, device-indepedent bitmap to use as the windows' representation.</span></span>


```C++
        case WM_DWMSENDICONICTHUMBNAIL:
        {    
            // This window is being asked to provide its iconic bitmap. This indicates
            // a thumbnail is being drawn.
            hbm = CreateDIB(HIWORD(lParam), LOWORD(lParam)); 
            if (hbm)
            {
                hr = DwmSetIconicThumbnail(hwnd, hbm, 0);
                DeleteObject(hbm);
            }
        }
        break;
```



<span data-ttu-id="8e3a2-128">Полный пример см. в разделе [Настройка эскиза значка и пример динамического предварительного просмотра растрового изображения](dwm-sample-customizethumbnail.md) .</span><span class="sxs-lookup"><span data-stu-id="8e3a2-128">For the complete example, see the [Customize an Iconic Thumbnail and a Live Preview Bitmap](dwm-sample-customizethumbnail.md) sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e3a2-129">Требования</span><span class="sxs-lookup"><span data-stu-id="8e3a2-129">Requirements</span></span>



| <span data-ttu-id="8e3a2-130">Требование</span><span class="sxs-lookup"><span data-stu-id="8e3a2-130">Requirement</span></span> | <span data-ttu-id="8e3a2-131">Значение</span><span class="sxs-lookup"><span data-stu-id="8e3a2-131">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8e3a2-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8e3a2-132">Minimum supported client</span></span><br/> | <span data-ttu-id="8e3a2-133">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="8e3a2-133">Windows 7 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="8e3a2-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8e3a2-134">Minimum supported server</span></span><br/> | <span data-ttu-id="8e3a2-135">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="8e3a2-135">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="8e3a2-136">Header</span><span class="sxs-lookup"><span data-stu-id="8e3a2-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e3a2-137"><dt>Двмапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e3a2-137"><dt>Dwmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e3a2-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8e3a2-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e3a2-139">**двминвалидатеиконикбитмапс**</span><span class="sxs-lookup"><span data-stu-id="8e3a2-139">**DwmInvalidateIconicBitmaps**</span></span>](/windows/desktop/api/Dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps)
</dt> <dt>

[<span data-ttu-id="8e3a2-140">**WM \_ двмсендиконикливепревиевбитмап**</span><span class="sxs-lookup"><span data-stu-id="8e3a2-140">**WM\_DWMSENDICONICLIVEPREVIEWBITMAP**</span></span>](wm-dwmsendiconiclivepreviewbitmap.md)
</dt> </dl>

 


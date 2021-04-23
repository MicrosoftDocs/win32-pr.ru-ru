---
title: Сообщение WM_CAP_SET_SCALE (VFW. h)
description: В \_ \_ \_ сообщении о масштабировании WM Set Scale можно включить или отключить масштабирование для видеороликов предварительного просмотра.
ms.assetid: f15f1d18-2c5a-40c1-baa1-0d18549bee23
keywords:
- WM_CAP_SET_SCALE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_SET_SCALE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd3bfc5dc463d84c935f994519060c33f89b8c0a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137519"
---
# <a name="wm_cap_set_scale-message"></a><span data-ttu-id="15c77-104">\_Сообщение с \_ заданным \_ масштабом WM Cap</span><span class="sxs-lookup"><span data-stu-id="15c77-104">WM\_CAP\_SET\_SCALE message</span></span>

<span data-ttu-id="15c77-105">В сообщении о **\_ \_ \_ масштабировании WM Set Scale** можно включить или отключить масштабирование для видеороликов предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="15c77-105">The **WM\_CAP\_SET\_SCALE** message enables or disables scaling of the preview video images.</span></span> <span data-ttu-id="15c77-106">Если масштабирование включено, захваченный видеокадр растягивается по размерам окна Capture.</span><span class="sxs-lookup"><span data-stu-id="15c77-106">If scaling is enabled, the captured video frame is stretched to the dimensions of the capture window.</span></span> <span data-ttu-id="15c77-107">Это сообщение можно отправить явно или с помощью макроса [**каппревиевскале**](/windows/desktop/api/Vfw/nf-vfw-cappreviewscale) .</span><span class="sxs-lookup"><span data-stu-id="15c77-107">You can send this message explicitly or by using the [**capPreviewScale**](/windows/desktop/api/Vfw/nf-vfw-cappreviewscale) macro.</span></span>


```C++
WM_CAP_SET_SCALE 
wParam = (WPARAM) (BOOL)f; 
lParam = 0L; 
```



## <a name="parameters"></a><span data-ttu-id="15c77-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="15c77-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15c77-109"><span id="f"></span><span id="F"></span>*ж*</span><span class="sxs-lookup"><span data-stu-id="15c77-109"><span id="f"></span><span id="F"></span>*f*</span></span>
</dt> <dd>

<span data-ttu-id="15c77-110">Флаг масштабирования для предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="15c77-110">Preview scaling flag.</span></span> <span data-ttu-id="15c77-111">Укажите **значение true** для параметра растяжение кадров предварительного просмотра до размера окна записи или **значение false** , чтобы отобразить их в натуральном размере.</span><span class="sxs-lookup"><span data-stu-id="15c77-111">Specify **TRUE** for this parameter to stretch preview frames to the size of the capture window or **FALSE** to display them at their natural size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15c77-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="15c77-112">Return Value</span></span>

<span data-ttu-id="15c77-113">Возвращает **значение true** в случае успеха или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="15c77-113">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="15c77-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="15c77-114">Remarks</span></span>

<span data-ttu-id="15c77-115">Изображения с предварительным просмотром — это немедленное представление захваченных кадров в окне Capture.</span><span class="sxs-lookup"><span data-stu-id="15c77-115">Scaling preview images controls the immediate presentation of captured frames within the capture window.</span></span> <span data-ttu-id="15c77-116">Он не влияет на размер кадров, сохраняемых в файле.</span><span class="sxs-lookup"><span data-stu-id="15c77-116">It has no effect on the size of the frames saved to file.</span></span>

<span data-ttu-id="15c77-117">Масштабирование не оказывает никакого влияния при использовании оверлея для показа видео в буфере кадров.</span><span class="sxs-lookup"><span data-stu-id="15c77-117">Scaling has no effect when using overlay to display video in the frame buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="15c77-118">Требования</span><span class="sxs-lookup"><span data-stu-id="15c77-118">Requirements</span></span>



| <span data-ttu-id="15c77-119">Требование</span><span class="sxs-lookup"><span data-stu-id="15c77-119">Requirement</span></span> | <span data-ttu-id="15c77-120">Значение</span><span class="sxs-lookup"><span data-stu-id="15c77-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="15c77-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="15c77-121">Minimum supported client</span></span><br/> | <span data-ttu-id="15c77-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="15c77-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="15c77-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="15c77-123">Minimum supported server</span></span><br/> | <span data-ttu-id="15c77-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="15c77-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="15c77-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="15c77-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="15c77-126"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="15c77-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15c77-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="15c77-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15c77-128">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="15c77-128">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="15c77-129">Сообщения видеозаписи</span><span class="sxs-lookup"><span data-stu-id="15c77-129">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 






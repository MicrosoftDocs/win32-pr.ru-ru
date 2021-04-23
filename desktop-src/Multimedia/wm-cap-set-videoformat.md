---
title: Сообщение WM_CAP_SET_VIDEOFORMAT (VFW. h)
description: Сообщение WM \_ Cap \_ Set \_ видеоформат устанавливает формат записываемых видеоданных. Это сообщение можно отправить явно или с помощью макроса Капсетвидеоформат.
ms.assetid: 4f9cf90d-7ccb-4fc7-aad5-3d7e082526be
keywords:
- WM_CAP_SET_VIDEOFORMAT сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_SET_VIDEOFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ba6154ec1532bd83f482eb81a0e286795aa3341
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989320"
---
# <a name="wm_cap_set_videoformat-message"></a><span data-ttu-id="35356-105">\_ \_ Сообщение видеоформат установки крепления WM \_</span><span class="sxs-lookup"><span data-stu-id="35356-105">WM\_CAP\_SET\_VIDEOFORMAT message</span></span>

<span data-ttu-id="35356-106">Сообщение **WM \_ Cap \_ Set \_ видеоформат** устанавливает формат записываемых видеоданных.</span><span class="sxs-lookup"><span data-stu-id="35356-106">The **WM\_CAP\_SET\_VIDEOFORMAT** message sets the format of captured video data.</span></span> <span data-ttu-id="35356-107">Это сообщение можно отправить явно или с помощью макроса [**капсетвидеоформат**](/windows/desktop/api/Vfw/nf-vfw-capsetvideoformat) .</span><span class="sxs-lookup"><span data-stu-id="35356-107">You can send this message explicitly or by using the [**capSetVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capsetvideoformat) macro.</span></span>


```C++
WM_CAP_SET_VIDEOFORMAT 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (psVideoFormat); 
```



## <a name="parameters"></a><span data-ttu-id="35356-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="35356-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35356-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*всизе*</span><span class="sxs-lookup"><span data-stu-id="35356-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="35356-110">Размер (в байтах) структуры, на которую ссылается **s**.</span><span class="sxs-lookup"><span data-stu-id="35356-110">Size, in bytes, of the structure referenced by **s**.</span></span>

</dd> <dt>

<span data-ttu-id="35356-111"><span id="psVideoFormat"></span><span id="psvideoformat"></span><span id="PSVIDEOFORMAT"></span>*псвидеоформат*</span><span class="sxs-lookup"><span data-stu-id="35356-111"><span id="psVideoFormat"></span><span id="psvideoformat"></span><span id="PSVIDEOFORMAT"></span>*psVideoFormat*</span></span>
</dt> <dd>

<span data-ttu-id="35356-112">Указатель на структуру [**битмапинфо**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) .</span><span class="sxs-lookup"><span data-stu-id="35356-112">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35356-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="35356-113">Return Value</span></span>

<span data-ttu-id="35356-114">Возвращает **значение true** в случае успеха или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="35356-114">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="35356-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="35356-115">Remarks</span></span>

<span data-ttu-id="35356-116">Так как форматы видео специфичны для конкретного устройства, приложения должны проверить возвращаемое значение этой функции, чтобы определить, принимается ли формат драйвером.</span><span class="sxs-lookup"><span data-stu-id="35356-116">Because video formats are device-specific, applications should check the return value from this function to determine if the format is accepted by the driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="35356-117">Требования</span><span class="sxs-lookup"><span data-stu-id="35356-117">Requirements</span></span>



| <span data-ttu-id="35356-118">Требование</span><span class="sxs-lookup"><span data-stu-id="35356-118">Requirement</span></span> | <span data-ttu-id="35356-119">Значение</span><span class="sxs-lookup"><span data-stu-id="35356-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="35356-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="35356-120">Minimum supported client</span></span><br/> | <span data-ttu-id="35356-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="35356-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="35356-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="35356-122">Minimum supported server</span></span><br/> | <span data-ttu-id="35356-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="35356-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="35356-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="35356-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="35356-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="35356-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35356-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="35356-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35356-127">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="35356-127">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="35356-128">Сообщения видеозаписи</span><span class="sxs-lookup"><span data-stu-id="35356-128">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 


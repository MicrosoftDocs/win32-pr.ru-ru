---
title: Сообщение WM_CAP_GET_VIDEOFORMAT (VFW. h)
description: Сообщение о \_ получении крепления WM \_ \_ видеоформат извлекает копию используемого видеоформата или размер, необходимый для формата видео. Это сообщение можно отправить явно или с помощью макросов Капжетвидеоформат и Капжетвидеоформатсизе.
ms.assetid: ac72dfdb-fe1a-4007-bdce-41e5e67d076a
keywords:
- WM_CAP_GET_VIDEOFORMAT сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_GET_VIDEOFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 072d71366efee550b037d4a20388817954937854
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988622"
---
# <a name="wm_cap_get_videoformat-message"></a><span data-ttu-id="a5f2b-105">\_Сообщение о \_ получении крепления WM \_ видеоформат</span><span class="sxs-lookup"><span data-stu-id="a5f2b-105">WM\_CAP\_GET\_VIDEOFORMAT message</span></span>

<span data-ttu-id="a5f2b-106">Сообщение **о \_ получении крепления WM \_ \_ видеоформат** извлекает копию используемого видеоформата или размер, необходимый для формата видео.</span><span class="sxs-lookup"><span data-stu-id="a5f2b-106">The **WM\_CAP\_GET\_VIDEOFORMAT** message retrieves a copy of the video format in use or the size required for the video format.</span></span> <span data-ttu-id="a5f2b-107">Это сообщение можно отправить явно или с помощью макросов [**капжетвидеоформат**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformat) и [**капжетвидеоформатсизе**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformatsize) .</span><span class="sxs-lookup"><span data-stu-id="a5f2b-107">You can send this message explicitly or by using the [**capGetVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformat) and [**capGetVideoFormatSize**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformatsize) macros.</span></span>


```C++
WM_CAP_GET_VIDEOFORMAT 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (psVideoFormat); 
```



## <a name="parameters"></a><span data-ttu-id="a5f2b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a5f2b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5f2b-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*всизе*</span><span class="sxs-lookup"><span data-stu-id="a5f2b-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="a5f2b-110">Размер (в байтах) структуры, на которую ссылается **s**.</span><span class="sxs-lookup"><span data-stu-id="a5f2b-110">Size, in bytes, of the structure referenced by **s**.</span></span>

</dd> <dt>

<span data-ttu-id="a5f2b-111"><span id="psVideoFormat"></span><span id="psvideoformat"></span><span id="PSVIDEOFORMAT"></span>*псвидеоформат*</span><span class="sxs-lookup"><span data-stu-id="a5f2b-111"><span id="psVideoFormat"></span><span id="psvideoformat"></span><span id="PSVIDEOFORMAT"></span>*psVideoFormat*</span></span>
</dt> <dd>

<span data-ttu-id="a5f2b-112">Указатель на структуру [**битмапинфо**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) .</span><span class="sxs-lookup"><span data-stu-id="a5f2b-112">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure.</span></span> <span data-ttu-id="a5f2b-113">Можно также указать **значение NULL** , чтобы получить необходимое количество байтов.</span><span class="sxs-lookup"><span data-stu-id="a5f2b-113">You can also specify **NULL** to retrieve the number of bytes needed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5f2b-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a5f2b-114">Return Value</span></span>

<span data-ttu-id="a5f2b-115">Возвращает размер (в байтах) формата видео или нуль, если окно записи не подключено к драйверу записи.</span><span class="sxs-lookup"><span data-stu-id="a5f2b-115">Returns the size, in bytes, of the video format or zero if the capture window is not connected to a capture driver.</span></span> <span data-ttu-id="a5f2b-116">Для форматов видео, для которых требуется палитра, также возвращается текущая палитра.</span><span class="sxs-lookup"><span data-stu-id="a5f2b-116">For video formats that require a palette, the current palette is also returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5f2b-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a5f2b-117">Remarks</span></span>

<span data-ttu-id="a5f2b-118">Поскольку формат сжатого видео зависит от требований к размеру, приложения должны сначала получить размер, затем выделить память и, наконец, запросить данные в формате видео.</span><span class="sxs-lookup"><span data-stu-id="a5f2b-118">Because compressed video formats vary in size requirements applications must first retrieve the size, then allocate memory, and finally request the video format data.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5f2b-119">Требования</span><span class="sxs-lookup"><span data-stu-id="a5f2b-119">Requirements</span></span>



| <span data-ttu-id="a5f2b-120">Требование</span><span class="sxs-lookup"><span data-stu-id="a5f2b-120">Requirement</span></span> | <span data-ttu-id="a5f2b-121">Значение</span><span class="sxs-lookup"><span data-stu-id="a5f2b-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a5f2b-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a5f2b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a5f2b-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a5f2b-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="a5f2b-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a5f2b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a5f2b-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a5f2b-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a5f2b-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a5f2b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5f2b-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5f2b-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5f2b-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a5f2b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5f2b-129">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="a5f2b-129">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="a5f2b-130">Сообщения видеозаписи</span><span class="sxs-lookup"><span data-stu-id="a5f2b-130">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 


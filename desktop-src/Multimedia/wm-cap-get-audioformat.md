---
title: Сообщение WM_CAP_GET_AUDIOFORMAT (VFW. h)
description: Сообщение о \_ получении крепления WM \_ \_ аудиоформат получает звуковой формат или размер звукового формата. Это сообщение можно отправить явно или с помощью макросов Капжетаудиоформат и Капжетаудиоформатсизе.
ms.assetid: 25e58863-2b1e-4ed8-9f34-c39617a15bc1
keywords:
- WM_CAP_GET_AUDIOFORMAT сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_GET_AUDIOFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9508972c173c9e189bdc092a63d849adf3be739
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414721"
---
# <a name="wm_cap_get_audioformat-message"></a><span data-ttu-id="ea0e6-105">\_Сообщение о \_ получении крепления WM \_ аудиоформат</span><span class="sxs-lookup"><span data-stu-id="ea0e6-105">WM\_CAP\_GET\_AUDIOFORMAT message</span></span>

<span data-ttu-id="ea0e6-106">Сообщение **о \_ получении крепления WM \_ \_ аудиоформат** получает звуковой формат или размер звукового формата.</span><span class="sxs-lookup"><span data-stu-id="ea0e6-106">The **WM\_CAP\_GET\_AUDIOFORMAT** message obtains the audio format or the size of the audio format.</span></span> <span data-ttu-id="ea0e6-107">Это сообщение можно отправить явно или с помощью макросов [**капжетаудиоформат**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformat) и [**капжетаудиоформатсизе**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformatsize) .</span><span class="sxs-lookup"><span data-stu-id="ea0e6-107">You can send this message explicitly or by using the [**capGetAudioFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformat) and [**capGetAudioFormatSize**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformatsize) macros.</span></span>


```C++
WM_CAP_GET_AUDIOFORMAT 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPWAVEFORMATEX) (psAudioFormat); 
```



## <a name="parameters"></a><span data-ttu-id="ea0e6-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ea0e6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea0e6-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*всизе*</span><span class="sxs-lookup"><span data-stu-id="ea0e6-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="ea0e6-110">Размер (в байтах) структуры, на которую ссылается **s**.</span><span class="sxs-lookup"><span data-stu-id="ea0e6-110">Size, in bytes, of the structure referenced by **s**.</span></span>

</dd> <dt>

<span data-ttu-id="ea0e6-111"><span id="psAudioFormat"></span><span id="psaudioformat"></span><span id="PSAUDIOFORMAT"></span>*псаудиоформат*</span><span class="sxs-lookup"><span data-stu-id="ea0e6-111"><span id="psAudioFormat"></span><span id="psaudioformat"></span><span id="PSAUDIOFORMAT"></span>*psAudioFormat*</span></span>
</dt> <dd>

<span data-ttu-id="ea0e6-112">Указатель на структуру [**вавеформатекс**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="ea0e6-112">Pointer to a [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) structure, or **NULL**.</span></span> <span data-ttu-id="ea0e6-113">Если значение равно **null**, возвращается размер (в байтах), необходимый для хранения структуры.</span><span class="sxs-lookup"><span data-stu-id="ea0e6-113">If the value is **NULL**, the size, in bytes, required to hold the structure is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea0e6-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ea0e6-114">Return Value</span></span>

<span data-ttu-id="ea0e6-115">Возвращает размер звукового формата в байтах.</span><span class="sxs-lookup"><span data-stu-id="ea0e6-115">Returns the size, in bytes, of the audio format.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea0e6-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ea0e6-116">Remarks</span></span>

<span data-ttu-id="ea0e6-117">Так как сжатые аудио форматы зависят от требований к размеру, приложения должны сначала получить размер, затем выделить память и, наконец, запросить данные в звуковом формате.</span><span class="sxs-lookup"><span data-stu-id="ea0e6-117">Because compressed audio formats vary in size requirements applications must first retrieve the size, then allocate memory, and finally request the audio format data.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea0e6-118">Требования</span><span class="sxs-lookup"><span data-stu-id="ea0e6-118">Requirements</span></span>



| <span data-ttu-id="ea0e6-119">Требование</span><span class="sxs-lookup"><span data-stu-id="ea0e6-119">Requirement</span></span> | <span data-ttu-id="ea0e6-120">Значение</span><span class="sxs-lookup"><span data-stu-id="ea0e6-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ea0e6-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ea0e6-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ea0e6-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ea0e6-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ea0e6-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ea0e6-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ea0e6-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ea0e6-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ea0e6-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="ea0e6-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea0e6-126"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea0e6-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea0e6-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ea0e6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea0e6-128">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="ea0e6-128">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="ea0e6-129">Сообщения видеозаписи</span><span class="sxs-lookup"><span data-stu-id="ea0e6-129">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 


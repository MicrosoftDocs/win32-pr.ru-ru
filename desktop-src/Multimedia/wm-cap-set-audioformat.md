---
title: Сообщение WM_CAP_SET_AUDIOFORMAT (VFW. h)
description: '\_ \_ Сообщение аудиоформат, установленное с помощью WM Cap, \_ задает формат аудио, используемый при выполнении потоковой передачи или записи шага. Это сообщение можно отправить явно или с помощью макроса Капсетаудиоформат.'
ms.assetid: 8bffa401-3d36-43bb-9f69-988ebc69b860
keywords:
- WM_CAP_SET_AUDIOFORMAT сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_SET_AUDIOFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c519ed936d2e71d9eee88435a94acc8c567a9a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136214"
---
# <a name="wm_cap_set_audioformat-message"></a><span data-ttu-id="6b3b8-105">\_ \_ Сообщение аудиоформат установки крепления WM \_</span><span class="sxs-lookup"><span data-stu-id="6b3b8-105">WM\_CAP\_SET\_AUDIOFORMAT message</span></span>

<span data-ttu-id="6b3b8-106">Сообщение **\_ \_ \_ аудиоформат, установленное с помощью WM Cap** , задает формат аудио, используемый при выполнении потоковой передачи или записи шага.</span><span class="sxs-lookup"><span data-stu-id="6b3b8-106">The **WM\_CAP\_SET\_AUDIOFORMAT** message sets the audio format to use when performing streaming or step capture.</span></span> <span data-ttu-id="6b3b8-107">Это сообщение можно отправить явно или с помощью макроса [**капсетаудиоформат**](/windows/desktop/api/Vfw/nf-vfw-capsetaudioformat) .</span><span class="sxs-lookup"><span data-stu-id="6b3b8-107">You can send this message explicitly or by using the [**capSetAudioFormat**](/windows/desktop/api/Vfw/nf-vfw-capsetaudioformat) macro.</span></span>


```C++
WM_CAP_SET_AUDIOFORMAT 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPWAVEFORMATEX) (psAudioFormat); 
```



## <a name="parameters"></a><span data-ttu-id="6b3b8-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6b3b8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b3b8-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*всизе*</span><span class="sxs-lookup"><span data-stu-id="6b3b8-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="6b3b8-110">Размер (в байтах) структуры, на которую ссылается **s**.</span><span class="sxs-lookup"><span data-stu-id="6b3b8-110">Size, in bytes, of the structure referenced by **s**.</span></span>

</dd> <dt>

<span data-ttu-id="6b3b8-111"><span id="psAudioFormat"></span><span id="psaudioformat"></span><span id="PSAUDIOFORMAT"></span>*псаудиоформат*</span><span class="sxs-lookup"><span data-stu-id="6b3b8-111"><span id="psAudioFormat"></span><span id="psaudioformat"></span><span id="PSAUDIOFORMAT"></span>*psAudioFormat*</span></span>
</dt> <dd>

<span data-ttu-id="6b3b8-112">Указатель на структуру [**вавеформатекс**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) или [**пкмвавеформат**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat) , определяющую аудио формат.</span><span class="sxs-lookup"><span data-stu-id="6b3b8-112">Pointer to a [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) or [**PCMWAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat) structure that defines the audio format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b3b8-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6b3b8-113">Return Value</span></span>

<span data-ttu-id="6b3b8-114">Возвращает **значение true** в случае успеха или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="6b3b8-114">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b3b8-115">Требования</span><span class="sxs-lookup"><span data-stu-id="6b3b8-115">Requirements</span></span>



| <span data-ttu-id="6b3b8-116">Требование</span><span class="sxs-lookup"><span data-stu-id="6b3b8-116">Requirement</span></span> | <span data-ttu-id="6b3b8-117">Значение</span><span class="sxs-lookup"><span data-stu-id="6b3b8-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6b3b8-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6b3b8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6b3b8-119">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6b3b8-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="6b3b8-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6b3b8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6b3b8-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6b3b8-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6b3b8-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="6b3b8-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b3b8-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b3b8-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b3b8-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6b3b8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b3b8-125">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="6b3b8-125">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="6b3b8-126">Сообщения видеозаписи</span><span class="sxs-lookup"><span data-stu-id="6b3b8-126">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 


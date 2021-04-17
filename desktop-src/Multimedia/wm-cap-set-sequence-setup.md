---
title: Сообщение WM_CAP_SET_SEQUENCE_SETUP (VFW. h)
description: В \_ сообщении о настройке закрепления WM \_ Set \_ Sequence \_ устанавливаются параметры конфигурации, используемые для сбора потоковой передачи. Это сообщение можно отправить явно или с помощью макроса Капкаптуресетсетуп.
ms.assetid: ba9adb26-6627-469b-a836-f4f277ddb7c4
keywords:
- WM_CAP_SET_SEQUENCE_SETUP сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_SET_SEQUENCE_SETUP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54a2129021f31694d9e601ecd97503e2a5f5c925
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535339"
---
# <a name="wm_cap_set_sequence_setup-message"></a><span data-ttu-id="000f0-105">\_ \_ \_ Сообщение настройки установки последовательностей WM Cap \_</span><span class="sxs-lookup"><span data-stu-id="000f0-105">WM\_CAP\_SET\_SEQUENCE\_SETUP message</span></span>

<span data-ttu-id="000f0-106">В сообщении о **\_ настройке закрепления WM \_ Set \_ Sequence \_** устанавливаются параметры конфигурации, используемые для сбора потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="000f0-106">The **WM\_CAP\_SET\_SEQUENCE\_SETUP** message sets the configuration parameters used with streaming capture.</span></span> <span data-ttu-id="000f0-107">Это сообщение можно отправить явно или с помощью макроса [**капкаптуресетсетуп**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) .</span><span class="sxs-lookup"><span data-stu-id="000f0-107">You can send this message explicitly or by using the [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) macro.</span></span>


```C++
WM_CAP_SET_SEQUENCE_SETUP 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPCAPTUREPARMS) (psCapParms); 
```



## <a name="parameters"></a><span data-ttu-id="000f0-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="000f0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="000f0-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*всизе*</span><span class="sxs-lookup"><span data-stu-id="000f0-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="000f0-110">Размер (в байтах) структуры, на которую ссылается **s**.</span><span class="sxs-lookup"><span data-stu-id="000f0-110">Size, in bytes, of the structure referenced by **s**.</span></span>

</dd> <dt>

<span data-ttu-id="000f0-111"><span id="psCapParms"></span><span id="pscapparms"></span><span id="PSCAPPARMS"></span>*пскаппармс*</span><span class="sxs-lookup"><span data-stu-id="000f0-111"><span id="psCapParms"></span><span id="pscapparms"></span><span id="PSCAPPARMS"></span>*psCapParms*</span></span>
</dt> <dd>

<span data-ttu-id="000f0-112">Указатель на структуру [**каптурепармс**](/windows/win32/api/vfw/ns-vfw-captureparms) .</span><span class="sxs-lookup"><span data-stu-id="000f0-112">Pointer to a [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="000f0-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="000f0-113">Return Value</span></span>

<span data-ttu-id="000f0-114">Возвращает **значение true** в случае успеха или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="000f0-114">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="000f0-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="000f0-115">Remarks</span></span>

<span data-ttu-id="000f0-116">Сведения о параметрах, используемых для управления потоковой передачей, см. в разделе Структура [**каптурепармс**](/windows/win32/api/vfw/ns-vfw-captureparms) .</span><span class="sxs-lookup"><span data-stu-id="000f0-116">For information about the parameters used to control streaming capture, see the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="000f0-117">Требования</span><span class="sxs-lookup"><span data-stu-id="000f0-117">Requirements</span></span>



| <span data-ttu-id="000f0-118">Требование</span><span class="sxs-lookup"><span data-stu-id="000f0-118">Requirement</span></span> | <span data-ttu-id="000f0-119">Значение</span><span class="sxs-lookup"><span data-stu-id="000f0-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="000f0-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="000f0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="000f0-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="000f0-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="000f0-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="000f0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="000f0-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="000f0-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="000f0-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="000f0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="000f0-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="000f0-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="000f0-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="000f0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="000f0-127">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="000f0-127">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="000f0-128">Сообщения видеозаписи</span><span class="sxs-lookup"><span data-stu-id="000f0-128">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 






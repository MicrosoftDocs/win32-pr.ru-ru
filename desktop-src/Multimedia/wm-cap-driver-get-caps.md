---
title: Сообщение WM_CAP_DRIVER_GET_CAPS (VFW. h)
description: '\_Сообщение о получении политики авторизации устройств WM Cap \_ \_ \_ возвращает аппаратные возможности драйвера записи, подключенного в настоящее время к окну записи. Это сообщение можно отправить явно или с помощью макроса Капдривержеткапс.'
ms.assetid: 898a800c-1109-47cd-bcc9-cb61d86a4a2e
keywords:
- WM_CAP_DRIVER_GET_CAPS сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_GET_CAPS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 027e530be82c76afebc343ceebe4905daef9b126
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535345"
---
# <a name="wm_cap_driver_get_caps-message"></a><span data-ttu-id="6268c-105">\_Сообщение о \_ \_ получении \_ политик крепления WM</span><span class="sxs-lookup"><span data-stu-id="6268c-105">WM\_CAP\_DRIVER\_GET\_CAPS message</span></span>

<span data-ttu-id="6268c-106">Сообщение **о \_ \_ \_ получении \_ политики авторизации устройств WM Cap** возвращает аппаратные возможности драйвера записи, подключенного в настоящее время к окну записи.</span><span class="sxs-lookup"><span data-stu-id="6268c-106">The **WM\_CAP\_DRIVER\_GET\_CAPS** message returns the hardware capabilities of the capture driver currently connected to a capture window.</span></span> <span data-ttu-id="6268c-107">Это сообщение можно отправить явно или с помощью макроса [**капдривержеткапс**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) .</span><span class="sxs-lookup"><span data-stu-id="6268c-107">You can send this message explicitly or by using the [**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) macro.</span></span>


```C++
WM_CAP_DRIVER_GET_CAPS 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPCAPDRIVERCAPS) (psCaps); 
```



## <a name="parameters"></a><span data-ttu-id="6268c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6268c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6268c-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*всизе*</span><span class="sxs-lookup"><span data-stu-id="6268c-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="6268c-110">Размер (в байтах) структуры, на которую ссылается **s**.</span><span class="sxs-lookup"><span data-stu-id="6268c-110">Size, in bytes, of the structure referenced by **s**.</span></span>

</dd> <dt>

<span data-ttu-id="6268c-111"><span id="psCaps"></span><span id="pscaps"></span><span id="PSCAPS"></span>*пскапс*</span><span class="sxs-lookup"><span data-stu-id="6268c-111"><span id="psCaps"></span><span id="pscaps"></span><span id="PSCAPS"></span>*psCaps*</span></span>
</dt> <dd>

<span data-ttu-id="6268c-112">Указатель на структуру [**капдриверкапс**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) , в которой должны содержаться аппаратные возможности.</span><span class="sxs-lookup"><span data-stu-id="6268c-112">Pointer to the [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) structure to contain the hardware capabilities.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6268c-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6268c-113">Return Value</span></span>

<span data-ttu-id="6268c-114">Возвращает **значение true** в случае успеха или **false** , если окно записи не подключено к драйверу записи.</span><span class="sxs-lookup"><span data-stu-id="6268c-114">Returns **TRUE** if successful or **FALSE** if the capture window is not connected to a capture driver.</span></span>

## <a name="remarks"></a><span data-ttu-id="6268c-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6268c-115">Remarks</span></span>

<span data-ttu-id="6268c-116">Возможности, возвращаемые в [**капдриверкапс**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) , являются постоянными для данного драйвера записи.</span><span class="sxs-lookup"><span data-stu-id="6268c-116">The capabilities returned in [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) are constant for a given capture driver.</span></span> <span data-ttu-id="6268c-117">Приложения должны получить эту информацию один раз при первом подключении драйвера записи к окну записи.</span><span class="sxs-lookup"><span data-stu-id="6268c-117">Applications need to retrieve this information once when the capture driver is first connected to a capture window.</span></span>

## <a name="requirements"></a><span data-ttu-id="6268c-118">Требования</span><span class="sxs-lookup"><span data-stu-id="6268c-118">Requirements</span></span>



| <span data-ttu-id="6268c-119">Требование</span><span class="sxs-lookup"><span data-stu-id="6268c-119">Requirement</span></span> | <span data-ttu-id="6268c-120">Значение</span><span class="sxs-lookup"><span data-stu-id="6268c-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6268c-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6268c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6268c-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6268c-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="6268c-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6268c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6268c-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6268c-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6268c-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="6268c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="6268c-126"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="6268c-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6268c-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6268c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6268c-128">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="6268c-128">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="6268c-129">Сообщения видеозаписи</span><span class="sxs-lookup"><span data-stu-id="6268c-129">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 






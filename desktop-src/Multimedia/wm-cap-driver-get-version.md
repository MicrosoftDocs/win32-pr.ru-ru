---
title: Сообщение WM_CAP_DRIVER_GET_VERSION (VFW. h)
description: '\_ \_ \_ Сообщение о получении версии драйвера WM Cap \_ возвращает сведения о версии драйвера записи, подключенного к окну записи. Это сообщение можно отправить явно или с помощью макроса Капдривержетверсион.'
ms.assetid: 762ebe7e-0d09-46ea-ab17-86061f0bd8f9
keywords:
- WM_CAP_DRIVER_GET_VERSION сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_GET_VERSION
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ced70f2d0159ef4bbad3f2d7a8027c30b2c71a5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661967"
---
# <a name="wm_cap_driver_get_version-message"></a><span data-ttu-id="f582a-105">\_Сообщение о \_ \_ получении \_ версии драйвера WM Cap</span><span class="sxs-lookup"><span data-stu-id="f582a-105">WM\_CAP\_DRIVER\_GET\_VERSION message</span></span>

<span data-ttu-id="f582a-106">Сообщение **о \_ \_ \_ получении \_ версии драйвера WM Cap** возвращает сведения о версии драйвера записи, подключенного к окну записи.</span><span class="sxs-lookup"><span data-stu-id="f582a-106">The **WM\_CAP\_DRIVER\_GET\_VERSION** message returns the version information of the capture driver connected to a capture window.</span></span> <span data-ttu-id="f582a-107">Это сообщение можно отправить явно или с помощью макроса [**капдривержетверсион**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetversion) .</span><span class="sxs-lookup"><span data-stu-id="f582a-107">You can send this message explicitly or by using the [**capDriverGetVersion**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetversion) macro.</span></span>


```C++
WM_CAP_DRIVER_GET_VERSION 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPSTR) (szVer); 
```



## <a name="parameters"></a><span data-ttu-id="f582a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f582a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f582a-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*всизе*</span><span class="sxs-lookup"><span data-stu-id="f582a-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="f582a-110">Размер (в байтах) определяемого приложением буфера, на который ссылается **сзвер**.</span><span class="sxs-lookup"><span data-stu-id="f582a-110">Size, in bytes, of the application-defined buffer referenced by **szVer**.</span></span>

</dd> <dt>

<span data-ttu-id="f582a-111"><span id="szVer"></span><span id="szver"></span><span id="SZVER"></span>*сзвер*</span><span class="sxs-lookup"><span data-stu-id="f582a-111"><span id="szVer"></span><span id="szver"></span><span id="SZVER"></span>*szVer*</span></span>
</dt> <dd>

<span data-ttu-id="f582a-112">Указатель на определенный приложением буфер, используемый для возврата сведений о версии в виде строки, завершающейся нулем.</span><span class="sxs-lookup"><span data-stu-id="f582a-112">Pointer to an application-defined buffer used to return the version information as a null-terminated string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f582a-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f582a-113">Return Value</span></span>

<span data-ttu-id="f582a-114">Возвращает **значение true** в случае успеха или **false** , если окно записи не подключено к драйверу записи.</span><span class="sxs-lookup"><span data-stu-id="f582a-114">Returns **TRUE** if successful or **FALSE** if the capture window is not connected to a capture driver.</span></span>

## <a name="remarks"></a><span data-ttu-id="f582a-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f582a-115">Remarks</span></span>

<span data-ttu-id="f582a-116">Сведения о версии — это текстовая строка, полученная из области ресурсов драйвера.</span><span class="sxs-lookup"><span data-stu-id="f582a-116">The version information is a text string retrieved from the driver's resource area.</span></span> <span data-ttu-id="f582a-117">Для этой строки приложения должны выделить примерно 40 байт.</span><span class="sxs-lookup"><span data-stu-id="f582a-117">Applications should allocate approximately 40 bytes for this string.</span></span> <span data-ttu-id="f582a-118">Если сведения о версии недоступны, возвращается **пустая** строка.</span><span class="sxs-lookup"><span data-stu-id="f582a-118">If version information is not available, a **NULL** string is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="f582a-119">Требования</span><span class="sxs-lookup"><span data-stu-id="f582a-119">Requirements</span></span>



| <span data-ttu-id="f582a-120">Требование</span><span class="sxs-lookup"><span data-stu-id="f582a-120">Requirement</span></span> | <span data-ttu-id="f582a-121">Значение</span><span class="sxs-lookup"><span data-stu-id="f582a-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f582a-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f582a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f582a-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f582a-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="f582a-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f582a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f582a-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f582a-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f582a-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="f582a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f582a-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="f582a-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f582a-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f582a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f582a-129">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="f582a-129">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="f582a-130">Сообщения видеозаписи</span><span class="sxs-lookup"><span data-stu-id="f582a-130">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 






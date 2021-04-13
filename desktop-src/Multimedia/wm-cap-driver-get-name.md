---
title: Сообщение WM_CAP_DRIVER_GET_NAME (VFW. h)
description: '\_ \_ \_ Сообщение Get Name драйвера WM Cap \_ возвращает имя драйвера записи, подключенного к окну Capture (захват). Это сообщение можно отправить явно или с помощью макроса Капдривержетнаме.'
ms.assetid: 84cecaf1-e0ff-424f-8c10-8bfe5cc2e7ea
keywords:
- WM_CAP_DRIVER_GET_NAME сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_GET_NAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 256b5f7913c83ddd278f3f3a05552b3d81070c73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489750"
---
# <a name="wm_cap_driver_get_name-message"></a><span data-ttu-id="e614e-105">\_Сообщение о \_ \_ получении \_ имени драйвера WM Cap</span><span class="sxs-lookup"><span data-stu-id="e614e-105">WM\_CAP\_DRIVER\_GET\_NAME message</span></span>

<span data-ttu-id="e614e-106">Сообщение **\_ \_ \_ Get \_ Name драйвера WM Cap** возвращает имя драйвера записи, подключенного к окну Capture (захват).</span><span class="sxs-lookup"><span data-stu-id="e614e-106">The **WM\_CAP\_DRIVER\_GET\_NAME** message returns the name of the capture driver connected to the capture window.</span></span> <span data-ttu-id="e614e-107">Это сообщение можно отправить явно или с помощью макроса [**капдривержетнаме**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetname) .</span><span class="sxs-lookup"><span data-stu-id="e614e-107">You can send this message explicitly or by using the [**capDriverGetName**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetname) macro.</span></span>


```C++
WM_CAP_DRIVER_GET_NAME 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a><span data-ttu-id="e614e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e614e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e614e-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*всизе*</span><span class="sxs-lookup"><span data-stu-id="e614e-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="e614e-110">Размер (в байтах) буфера, на который ссылается параметр **szName**.</span><span class="sxs-lookup"><span data-stu-id="e614e-110">Size, in bytes, of the buffer referenced by **szName**.</span></span>

</dd> <dt>

<span data-ttu-id="e614e-111"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span><span class="sxs-lookup"><span data-stu-id="e614e-111"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span></span>
</dt> <dd>

<span data-ttu-id="e614e-112">Указатель на определенный приложением буфер, используемый для возврата имени устройства в виде строки, завершающейся нулем.</span><span class="sxs-lookup"><span data-stu-id="e614e-112">Pointer to an application-defined buffer used to return the device name as a null-terminated string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e614e-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e614e-113">Return Value</span></span>

<span data-ttu-id="e614e-114">Возвращает **значение true** в случае успеха или **false** , если окно записи не подключено к драйверу записи.</span><span class="sxs-lookup"><span data-stu-id="e614e-114">Returns **TRUE** if successful or **FALSE** if the capture window is not connected to a capture driver.</span></span>

## <a name="remarks"></a><span data-ttu-id="e614e-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e614e-115">Remarks</span></span>

<span data-ttu-id="e614e-116">Имя — это текстовая строка, полученная из области ресурсов драйвера.</span><span class="sxs-lookup"><span data-stu-id="e614e-116">The name is a text string retrieved from the driver's resource area.</span></span> <span data-ttu-id="e614e-117">Для этой строки приложения должны выделить примерно 80 байт.</span><span class="sxs-lookup"><span data-stu-id="e614e-117">Applications should allocate approximately 80 bytes for this string.</span></span> <span data-ttu-id="e614e-118">Если драйвер не содержит ресурс имени, возвращается полный путь к драйверу, указанному в реестре или в файле SYSTEM.INI.</span><span class="sxs-lookup"><span data-stu-id="e614e-118">If the driver does not contain a name resource, the full path name of the driver listed in the registry or in the SYSTEM.INI file is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="e614e-119">Требования</span><span class="sxs-lookup"><span data-stu-id="e614e-119">Requirements</span></span>



| <span data-ttu-id="e614e-120">Требование</span><span class="sxs-lookup"><span data-stu-id="e614e-120">Requirement</span></span> | <span data-ttu-id="e614e-121">Значение</span><span class="sxs-lookup"><span data-stu-id="e614e-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e614e-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e614e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e614e-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e614e-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="e614e-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e614e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e614e-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e614e-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e614e-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="e614e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e614e-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="e614e-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e614e-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e614e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e614e-129">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="e614e-129">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="e614e-130">Сообщения видеозаписи</span><span class="sxs-lookup"><span data-stu-id="e614e-130">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 






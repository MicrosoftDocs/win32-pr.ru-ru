---
title: Сообщение WM_CAP_FILE_GET_CAPTURE_FILE (VFW. h)
description: '\_ \_ \_ Сообщение о получении файла записи с закреплением WM \_ \_ возвращает имя текущего файла записи. Это сообщение можно отправить явно или с помощью макроса Капфилежеткаптурефиле.'
ms.assetid: 86ce2904-834d-449f-9ef8-5a158c55bbaa
keywords:
- WM_CAP_FILE_GET_CAPTURE_FILE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_FILE_GET_CAPTURE_FILE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7008e0b217f29ad9602afbdc41cc97f9cb7ecaa3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891538"
---
# <a name="wm_cap_file_get_capture_file-message"></a><span data-ttu-id="84c76-105">\_Сообщение о \_ \_ получении \_ файла записи \_ закрепления WM</span><span class="sxs-lookup"><span data-stu-id="84c76-105">WM\_CAP\_FILE\_GET\_CAPTURE\_FILE message</span></span>

<span data-ttu-id="84c76-106">Сообщение **о \_ \_ \_ получении \_ \_ файла записи с закреплением WM** возвращает имя текущего файла записи.</span><span class="sxs-lookup"><span data-stu-id="84c76-106">The **WM\_CAP\_FILE\_GET\_CAPTURE\_FILE** message returns the name of the current capture file.</span></span> <span data-ttu-id="84c76-107">Это сообщение можно отправить явно или с помощью макроса [**капфилежеткаптурефиле**](/windows/desktop/api/Vfw/nf-vfw-capfilegetcapturefile) .</span><span class="sxs-lookup"><span data-stu-id="84c76-107">You can send this message explicitly or by using the [**capFileGetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilegetcapturefile) macro.</span></span>


```C++
WM_CAP_FILE_GET_CAPTURE_FILE 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a><span data-ttu-id="84c76-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="84c76-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84c76-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*всизе*</span><span class="sxs-lookup"><span data-stu-id="84c76-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="84c76-110">Размер (в байтах) определяемого приложением буфера, на который ссылается параметр **szName**.</span><span class="sxs-lookup"><span data-stu-id="84c76-110">Size, in bytes, of the application-defined buffer referenced by **szName**.</span></span>

</dd> <dt>

<span data-ttu-id="84c76-111"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span><span class="sxs-lookup"><span data-stu-id="84c76-111"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span></span>
</dt> <dd>

<span data-ttu-id="84c76-112">Указатель на определенный приложением буфер, используемый для возврата имени файла записи в виде строки, завершающейся нулем.</span><span class="sxs-lookup"><span data-stu-id="84c76-112">Pointer to an application-defined buffer used to return the name of the capture file as a null-terminated string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84c76-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="84c76-113">Return Value</span></span>

<span data-ttu-id="84c76-114">Возвращает **значение true** в случае успеха или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="84c76-114">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="84c76-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="84c76-115">Remarks</span></span>

<span data-ttu-id="84c76-116">Имя файла для отслеживания по умолчанию — C: \\CAPTURE.AVI.</span><span class="sxs-lookup"><span data-stu-id="84c76-116">The default capture filename is C:\\CAPTURE.AVI.</span></span>

## <a name="requirements"></a><span data-ttu-id="84c76-117">Требования</span><span class="sxs-lookup"><span data-stu-id="84c76-117">Requirements</span></span>



| <span data-ttu-id="84c76-118">Требование</span><span class="sxs-lookup"><span data-stu-id="84c76-118">Requirement</span></span> | <span data-ttu-id="84c76-119">Значение</span><span class="sxs-lookup"><span data-stu-id="84c76-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="84c76-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="84c76-120">Minimum supported client</span></span><br/> | <span data-ttu-id="84c76-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="84c76-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="84c76-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="84c76-122">Minimum supported server</span></span><br/> | <span data-ttu-id="84c76-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="84c76-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="84c76-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="84c76-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="84c76-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="84c76-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84c76-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="84c76-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84c76-127">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="84c76-127">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="84c76-128">Сообщения видеозаписи</span><span class="sxs-lookup"><span data-stu-id="84c76-128">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 






---
title: Сообщение WM_CAP_FILE_SET_CAPTURE_FILE (VFW. h)
description: '\_ \_ \_ Сообщение файла записи набора закрепления WM задает \_ \_ имя файла, используемого для записи видео. Это сообщение можно отправить явно или с помощью макроса Капфилесеткаптурефиле.'
ms.assetid: d96e498b-6322-4d48-a5d7-156e95f23740
keywords:
- WM_CAP_FILE_SET_CAPTURE_FILE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_FILE_SET_CAPTURE_FILE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12b3f59edfc9bf01f6bd2af3b9028f8e3315e2de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988173"
---
# <a name="wm_cap_file_set_capture_file-message"></a><span data-ttu-id="1f486-105">\_Сообщение о \_ \_ наборе файлов \_ фиксации \_ WM Cap</span><span class="sxs-lookup"><span data-stu-id="1f486-105">WM\_CAP\_FILE\_SET\_CAPTURE\_FILE message</span></span>

<span data-ttu-id="1f486-106">Сообщение **\_ \_ \_ \_ \_ файла записи набора закрепления WM задает** имя файла, используемого для записи видео.</span><span class="sxs-lookup"><span data-stu-id="1f486-106">The **WM\_CAP\_FILE\_SET\_CAPTURE\_FILE** message names the file used for video capture.</span></span> <span data-ttu-id="1f486-107">Это сообщение можно отправить явно или с помощью макроса [**капфилесеткаптурефиле**](/windows/desktop/api/Vfw/nf-vfw-capfilesetcapturefile) .</span><span class="sxs-lookup"><span data-stu-id="1f486-107">You can send this message explicitly or by using the [**capFileSetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilesetcapturefile) macro.</span></span>


```C++
WM_CAP_FILE_SET_CAPTURE_FILE 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a><span data-ttu-id="1f486-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1f486-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f486-109"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span><span class="sxs-lookup"><span data-stu-id="1f486-109"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span></span>
</dt> <dd>

<span data-ttu-id="1f486-110">Указатель на строку, завершающуюся нулем, которая содержит имя файла записи для использования.</span><span class="sxs-lookup"><span data-stu-id="1f486-110">Pointer to the null-terminated string that contains the name of the capture file to use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f486-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1f486-111">Return Value</span></span>

<span data-ttu-id="1f486-112">Возвращает **значение true** в случае успеха или **false** , если имя файла является недопустимым, или если выполняется потоковая передача или захват одного кадра.</span><span class="sxs-lookup"><span data-stu-id="1f486-112">Returns **TRUE** if successful or **FALSE** if the filename is invalid, or if streaming or single-frame capture is in progress.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f486-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1f486-113">Remarks</span></span>

<span data-ttu-id="1f486-114">Это сообщение сохраняет имя файла во внутренней структуре.</span><span class="sxs-lookup"><span data-stu-id="1f486-114">This message stores the filename in an internal structure.</span></span> <span data-ttu-id="1f486-115">Он не создает, не выделяет или не открывает указанный файл.</span><span class="sxs-lookup"><span data-stu-id="1f486-115">It does not create, allocate, or open the specified file.</span></span> <span data-ttu-id="1f486-116">Имя файла для отслеживания по умолчанию — C: \\CAPTURE.AVI.</span><span class="sxs-lookup"><span data-stu-id="1f486-116">The default capture filename is C:\\CAPTURE.AVI.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f486-117">Требования</span><span class="sxs-lookup"><span data-stu-id="1f486-117">Requirements</span></span>



| <span data-ttu-id="1f486-118">Требование</span><span class="sxs-lookup"><span data-stu-id="1f486-118">Requirement</span></span> | <span data-ttu-id="1f486-119">Значение</span><span class="sxs-lookup"><span data-stu-id="1f486-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="1f486-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1f486-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1f486-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1f486-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="1f486-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1f486-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1f486-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1f486-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="1f486-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="1f486-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f486-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f486-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f486-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1f486-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f486-127">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="1f486-127">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="1f486-128">Сообщения видеозаписи</span><span class="sxs-lookup"><span data-stu-id="1f486-128">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 






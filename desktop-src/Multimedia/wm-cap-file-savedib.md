---
title: Сообщение WM_CAP_FILE_SAVEDIB (VFW. h)
description: '\_Сообщение саведиб с закреплением WM \_ \_ копирует текущий кадр в DIB-файл. Это сообщение можно отправить явно или с помощью макроса Капфилесаведиб.'
ms.assetid: bf6d343b-9236-4e68-bbda-2ed6e197a5cb
keywords:
- WM_CAP_FILE_SAVEDIB сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_FILE_SAVEDIB
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2155febfdac1b3f24133df47ce206c8e5ec33d3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492951"
---
# <a name="wm_cap_file_savedib-message"></a><span data-ttu-id="af56a-105">\_ \_ \_ Сообщение саведиба WM Cap File</span><span class="sxs-lookup"><span data-stu-id="af56a-105">WM\_CAP\_FILE\_SAVEDIB message</span></span>

<span data-ttu-id="af56a-106">Сообщение **\_ \_ \_ саведиб с закреплением WM** копирует текущий кадр в DIB-файл.</span><span class="sxs-lookup"><span data-stu-id="af56a-106">The **WM\_CAP\_FILE\_SAVEDIB** message copies the current frame to a DIB file.</span></span> <span data-ttu-id="af56a-107">Это сообщение можно отправить явно или с помощью макроса [**капфилесаведиб**](/windows/desktop/api/Vfw/nf-vfw-capfilesavedib) .</span><span class="sxs-lookup"><span data-stu-id="af56a-107">You can send this message explicitly or by using the [**capFileSaveDIB**](/windows/desktop/api/Vfw/nf-vfw-capfilesavedib) macro.</span></span>


```C++
WM_CAP_FILE_SAVEDIB 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a><span data-ttu-id="af56a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="af56a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af56a-109"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span><span class="sxs-lookup"><span data-stu-id="af56a-109"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span></span>
</dt> <dd>

<span data-ttu-id="af56a-110">Указатель на строку, завершающуюся нулем, которая содержит имя конечного файла DIB.</span><span class="sxs-lookup"><span data-stu-id="af56a-110">Pointer to the null-terminated string that contains the name of the destination DIB file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af56a-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="af56a-111">Return Value</span></span>

<span data-ttu-id="af56a-112">Возвращает **значение true** в случае успеха или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="af56a-112">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="af56a-113">Если возникает ошибка и функция обратного вызова ошибки устанавливается с помощью сообщения [**\_ \_ \_ \_ об ошибке обратного вызова**](wm-cap-set-callback-error.md) , то вызывается функция обратного вызова ошибки.</span><span class="sxs-lookup"><span data-stu-id="af56a-113">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="remarks"></a><span data-ttu-id="af56a-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="af56a-114">Remarks</span></span>

<span data-ttu-id="af56a-115">Если драйвер записи передает кадры в сжатом формате, этот вызов пытается распаковать кадр перед записью файла.</span><span class="sxs-lookup"><span data-stu-id="af56a-115">If the capture driver supplies frames in a compressed format, this call attempts to decompress the frame before writing the file.</span></span>

## <a name="requirements"></a><span data-ttu-id="af56a-116">Требования</span><span class="sxs-lookup"><span data-stu-id="af56a-116">Requirements</span></span>



| <span data-ttu-id="af56a-117">Требование</span><span class="sxs-lookup"><span data-stu-id="af56a-117">Requirement</span></span> | <span data-ttu-id="af56a-118">Значение</span><span class="sxs-lookup"><span data-stu-id="af56a-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="af56a-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="af56a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="af56a-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="af56a-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="af56a-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="af56a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="af56a-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="af56a-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="af56a-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="af56a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="af56a-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="af56a-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af56a-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="af56a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af56a-126">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="af56a-126">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="af56a-127">Сообщения видеозаписи</span><span class="sxs-lookup"><span data-stu-id="af56a-127">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 






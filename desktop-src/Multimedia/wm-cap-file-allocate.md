---
title: Сообщение WM_CAP_FILE_ALLOCATE (VFW. h)
description: '\_ \_ \_ Сообщение о выделении файла закрепления WM создает (предварительно выделяет) файл записи указанного размера. Это сообщение можно отправить явно или с помощью макроса Капфилеаллок.'
ms.assetid: 31ebe824-4a30-4212-9479-a5cbd8fc1e1d
keywords:
- WM_CAP_FILE_ALLOCATE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_FILE_ALLOCATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d36cec54e5775641118679b24b0d4b3b1767693
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489747"
---
# <a name="wm_cap_file_allocate-message"></a><span data-ttu-id="df8ca-105">\_Сообщение о \_ выделении файла крепления WM \_</span><span class="sxs-lookup"><span data-stu-id="df8ca-105">WM\_CAP\_FILE\_ALLOCATE message</span></span>

<span data-ttu-id="df8ca-106">Сообщение **о \_ \_ \_ выделении файла закрепления WM** создает (предварительно выделяет) файл записи указанного размера.</span><span class="sxs-lookup"><span data-stu-id="df8ca-106">The **WM\_CAP\_FILE\_ALLOCATE** message creates (preallocates) a capture file of a specified size.</span></span> <span data-ttu-id="df8ca-107">Это сообщение можно отправить явно или с помощью макроса [**капфилеаллок**](/windows/desktop/api/Vfw/nf-vfw-capfilealloc) .</span><span class="sxs-lookup"><span data-stu-id="df8ca-107">You can send this message explicitly or by using the [**capFileAlloc**](/windows/desktop/api/Vfw/nf-vfw-capfilealloc) macro.</span></span>


```C++
WM_CAP_FILE_ALLOCATE 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (DWORD) (dwSize); 
```



## <a name="parameters"></a><span data-ttu-id="df8ca-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="df8ca-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df8ca-109"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>*двсизе*</span><span class="sxs-lookup"><span data-stu-id="df8ca-109"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>*dwSize*</span></span>
</dt> <dd>

<span data-ttu-id="df8ca-110">Размер (в байтах) для создания файла записи.</span><span class="sxs-lookup"><span data-stu-id="df8ca-110">Size, in bytes, to create the capture file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df8ca-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="df8ca-111">Return Value</span></span>

<span data-ttu-id="df8ca-112">Возвращает **значение true** в случае успеха или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="df8ca-112">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="df8ca-113">Если возникает ошибка и функция обратного вызова ошибки устанавливается с помощью сообщения [**\_ \_ \_ \_ об ошибке обратного вызова**](wm-cap-set-callback-error.md) , то вызывается функция обратного вызова ошибки.</span><span class="sxs-lookup"><span data-stu-id="df8ca-113">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="remarks"></a><span data-ttu-id="df8ca-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="df8ca-114">Remarks</span></span>

<span data-ttu-id="df8ca-115">Производительность захвата потоковой передачи значительно повышается за счет предварительного выделения файла записи, достаточного для хранения всего видеоклипа и дефрагментации файла записи перед записью клипа.</span><span class="sxs-lookup"><span data-stu-id="df8ca-115">You can improve streaming capture performance significantly by preallocating a capture file large enough to store an entire video clip and by defragmenting the capture file before capturing the clip.</span></span>

## <a name="requirements"></a><span data-ttu-id="df8ca-116">Требования</span><span class="sxs-lookup"><span data-stu-id="df8ca-116">Requirements</span></span>



| <span data-ttu-id="df8ca-117">Требование</span><span class="sxs-lookup"><span data-stu-id="df8ca-117">Requirement</span></span> | <span data-ttu-id="df8ca-118">Значение</span><span class="sxs-lookup"><span data-stu-id="df8ca-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="df8ca-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="df8ca-119">Minimum supported client</span></span><br/> | <span data-ttu-id="df8ca-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="df8ca-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="df8ca-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="df8ca-121">Minimum supported server</span></span><br/> | <span data-ttu-id="df8ca-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="df8ca-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="df8ca-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="df8ca-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="df8ca-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="df8ca-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df8ca-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="df8ca-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df8ca-126">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="df8ca-126">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="df8ca-127">Сообщения видеозаписи</span><span class="sxs-lookup"><span data-stu-id="df8ca-127">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 






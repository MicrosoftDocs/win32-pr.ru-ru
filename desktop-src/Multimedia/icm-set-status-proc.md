---
title: Сообщение ICM_SET_STATUS_PROC (VFW. h)
description: Сообщение о \_ состоянии установки ICM \_ \_ предоставляет функцию обратного вызова состояния с состоянием длительной операции.
ms.assetid: a1bcd840-b94b-487e-91d6-67411a8a3a2d
keywords:
- ICM_SET_STATUS_PROC сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_SET_STATUS_PROC
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53d7ad2745ab53c2e04a1588ddbf1b1e5d755202
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493281"
---
# <a name="icm_set_status_proc-message"></a><span data-ttu-id="0f381-104">\_ \_ Сообщение о состоянии установки ICM \_</span><span class="sxs-lookup"><span data-stu-id="0f381-104">ICM\_SET\_STATUS\_PROC message</span></span>

<span data-ttu-id="0f381-105">Сообщение **о \_ \_ состоянии установки \_ ICM** предоставляет функцию обратного вызова состояния с состоянием длительной операции.</span><span class="sxs-lookup"><span data-stu-id="0f381-105">The **ICM\_SET\_STATUS\_PROC** message provides a status callback function with the status of a lengthy operation.</span></span>


```C++
ICM_SET_STATUS_PROC 
wParam = (DWORD_PTR)icsetstatusProc; 
lParam = sizeof(ICSETSTATUSPROC); 
```



## <a name="parameters"></a><span data-ttu-id="0f381-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0f381-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f381-107"><span id="icsetstatusProc"></span><span id="icsetstatusproc"></span><span id="ICSETSTATUSPROC"></span>*иксетстатуспрок*</span><span class="sxs-lookup"><span data-stu-id="0f381-107"><span id="icsetstatusProc"></span><span id="icsetstatusproc"></span><span id="ICSETSTATUSPROC"></span>*icsetstatusProc*</span></span>
</dt> <dd>

<span data-ttu-id="0f381-108">Указатель на структуру [**иксетстатуспрок**](/windows/desktop/api/Vfw/ns-vfw-icsetstatusproc) .</span><span class="sxs-lookup"><span data-stu-id="0f381-108">Pointer to an [**ICSETSTATUSPROC**](/windows/desktop/api/Vfw/ns-vfw-icsetstatusproc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="0f381-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="0f381-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="0f381-110">Размер **иксетстатуспрок** в байтах.</span><span class="sxs-lookup"><span data-stu-id="0f381-110">Size, in bytes, of **ICSETSTATUSPROC**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f381-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0f381-111">Return Value</span></span>

<span data-ttu-id="0f381-112">Возвращает ИЦЕРР \_ ОК в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="0f381-112">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f381-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0f381-113">Remarks</span></span>

<span data-ttu-id="0f381-114">Поддержка этого сообщения является необязательной, но настоятельно рекомендуется, если сжатие или распаковка занимает больше времени, чем приблизительно в одну десятую секунды.</span><span class="sxs-lookup"><span data-stu-id="0f381-114">Support of this message is optional but strongly recommended if compression or decompression takes longer than approximately one-tenth of a second.</span></span>

<span data-ttu-id="0f381-115">Приложение может периодически отправить это сообщение в функцию обратного вызова состояния во время длительных операций.</span><span class="sxs-lookup"><span data-stu-id="0f381-115">An application can send this message periodically to a status callback function during lengthy operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f381-116">Требования</span><span class="sxs-lookup"><span data-stu-id="0f381-116">Requirements</span></span>



| <span data-ttu-id="0f381-117">Требование</span><span class="sxs-lookup"><span data-stu-id="0f381-117">Requirement</span></span> | <span data-ttu-id="0f381-118">Значение</span><span class="sxs-lookup"><span data-stu-id="0f381-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0f381-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0f381-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0f381-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0f381-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="0f381-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0f381-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0f381-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0f381-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0f381-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="0f381-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f381-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f381-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f381-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0f381-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f381-126">Диспетчер сжатия видео</span><span class="sxs-lookup"><span data-stu-id="0f381-126">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="0f381-127">Сообщения о сжатии видео</span><span class="sxs-lookup"><span data-stu-id="0f381-127">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 






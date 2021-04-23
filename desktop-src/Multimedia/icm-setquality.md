---
title: Сообщение ICM_SETQUALITY (VFW. h)
description: Сообщение ICM \_ сеткуалити предоставляет драйверу сжатия видео с уровнем качества, который будет использоваться во время сжатия.
ms.assetid: 487ff1de-7178-440a-b38d-0b82a30d7297
keywords:
- ICM_SETQUALITY сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_SETQUALITY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a1523996ad336e64d4b34143cc26cd8d0937d5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104416173"
---
# <a name="icm_setquality-message"></a><span data-ttu-id="72776-104">\_Сообщение ICM сеткуалити</span><span class="sxs-lookup"><span data-stu-id="72776-104">ICM\_SETQUALITY message</span></span>

<span data-ttu-id="72776-105">Сообщение **ICM \_ сеткуалити** предоставляет драйверу сжатия видео с уровнем качества, который будет использоваться во время сжатия.</span><span class="sxs-lookup"><span data-stu-id="72776-105">The **ICM\_SETQUALITY** message provides a video compression driver with a quality level to use during compression.</span></span>


```C++
ICM_SETQUALITY 
wParam = (DWORD) (LPVOID) &dwICValue; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="72776-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="72776-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72776-107"><span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*двиквалуе*</span><span class="sxs-lookup"><span data-stu-id="72776-107"><span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*</span></span>
</dt> <dd>

<span data-ttu-id="72776-108">Новое значение качества.</span><span class="sxs-lookup"><span data-stu-id="72776-108">New quality value.</span></span> <span data-ttu-id="72776-109">Значения качества находятся в диапазоне от 0 до 10 000.</span><span class="sxs-lookup"><span data-stu-id="72776-109">Quality values range from 0 to 10,000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72776-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="72776-110">Return Value</span></span>

<span data-ttu-id="72776-111">Возвращает ИЦЕРР \_ ОК, если драйвер поддерживает это сообщение или ИЦЕРР \_ не поддерживается в противном случае.</span><span class="sxs-lookup"><span data-stu-id="72776-111">Returns ICERR\_OK if the driver supports this message or ICERR\_UNSUPPORTED otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="72776-112">Требования</span><span class="sxs-lookup"><span data-stu-id="72776-112">Requirements</span></span>



| <span data-ttu-id="72776-113">Требование</span><span class="sxs-lookup"><span data-stu-id="72776-113">Requirement</span></span> | <span data-ttu-id="72776-114">Значение</span><span class="sxs-lookup"><span data-stu-id="72776-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="72776-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="72776-115">Minimum supported client</span></span><br/> | <span data-ttu-id="72776-116">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="72776-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="72776-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="72776-117">Minimum supported server</span></span><br/> | <span data-ttu-id="72776-118">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="72776-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="72776-119">Заголовок</span><span class="sxs-lookup"><span data-stu-id="72776-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="72776-120"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="72776-120"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72776-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="72776-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72776-122">Диспетчер сжатия видео</span><span class="sxs-lookup"><span data-stu-id="72776-122">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="72776-123">Сообщения о сжатии видео</span><span class="sxs-lookup"><span data-stu-id="72776-123">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 






---
title: Сообщение ICM_GETQUALITY (VFW. h)
description: Сообщение ICM \_ Quality запрашивает драйвер сжатия видео, чтобы вернуть текущий параметр качества.
ms.assetid: 8da99a26-7b2a-4118-89e1-7485915cbdc9
keywords:
- ICM_GETQUALITY сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_GETQUALITY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c4fa2a26e1fe5fa111585ce0a59422a2fe9b072
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989424"
---
# <a name="icm_getquality-message"></a><span data-ttu-id="b3043-104">Сообщение ICM с \_ качеством</span><span class="sxs-lookup"><span data-stu-id="b3043-104">ICM\_GETQUALITY message</span></span>

<span data-ttu-id="b3043-105">Сообщение **ICM \_ Quality** запрашивает драйвер сжатия видео, чтобы вернуть текущий параметр качества.</span><span class="sxs-lookup"><span data-stu-id="b3043-105">The **ICM\_GETQUALITY** message queries a video compression driver to return its current quality setting.</span></span>


```C++
ICM_GETQUALITY 
wParam = (DWORD) (LPVOID) &dwICValue; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="b3043-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b3043-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3043-107"><span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*двиквалуе*</span><span class="sxs-lookup"><span data-stu-id="b3043-107"><span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*</span></span>
</dt> <dd>

<span data-ttu-id="b3043-108">Адрес, который будет содержать текущее значение качества.</span><span class="sxs-lookup"><span data-stu-id="b3043-108">Address to contain the current quality value.</span></span> <span data-ttu-id="b3043-109">Значения качества находятся в диапазоне от 0 до 10 000.</span><span class="sxs-lookup"><span data-stu-id="b3043-109">Quality values range from 0 to 10,000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3043-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b3043-110">Return Value</span></span>

<span data-ttu-id="b3043-111">Возвращает ИЦЕРР \_ ОК, если драйвер поддерживает это сообщение или ИЦЕРР \_ не поддерживается в противном случае.</span><span class="sxs-lookup"><span data-stu-id="b3043-111">Returns ICERR\_OK if the driver supports this message or ICERR\_UNSUPPORTED otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3043-112">Требования</span><span class="sxs-lookup"><span data-stu-id="b3043-112">Requirements</span></span>



| <span data-ttu-id="b3043-113">Требование</span><span class="sxs-lookup"><span data-stu-id="b3043-113">Requirement</span></span> | <span data-ttu-id="b3043-114">Значение</span><span class="sxs-lookup"><span data-stu-id="b3043-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b3043-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b3043-115">Minimum supported client</span></span><br/> | <span data-ttu-id="b3043-116">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b3043-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="b3043-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b3043-117">Minimum supported server</span></span><br/> | <span data-ttu-id="b3043-118">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b3043-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b3043-119">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b3043-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3043-120"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3043-120"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3043-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b3043-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3043-122">Диспетчер сжатия видео</span><span class="sxs-lookup"><span data-stu-id="b3043-122">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="b3043-123">Сообщения о сжатии видео</span><span class="sxs-lookup"><span data-stu-id="b3043-123">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 






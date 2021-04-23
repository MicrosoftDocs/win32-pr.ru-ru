---
title: Сообщение ICM_GETDEFAULTQUALITY (VFW. h)
description: Сообщение ICM \_ жетдефаулткуалити запрашивает драйвер сжатия видео, чтобы предоставить параметр качества по умолчанию. Это сообщение можно отправить явно или с помощью макроса Икжетдефаулткуалити.
ms.assetid: bba7f451-52c2-4684-a7c9-e4b05cb946c5
keywords:
- ICM_GETDEFAULTQUALITY сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_GETDEFAULTQUALITY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4350539851ca720e3538d297f955a56fedfc4a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489591"
---
# <a name="icm_getdefaultquality-message"></a><span data-ttu-id="a97b0-105">\_Сообщение ICM жетдефаулткуалити</span><span class="sxs-lookup"><span data-stu-id="a97b0-105">ICM\_GETDEFAULTQUALITY message</span></span>

<span data-ttu-id="a97b0-106">Сообщение **ICM \_ жетдефаулткуалити** запрашивает драйвер сжатия видео, чтобы предоставить параметр качества по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a97b0-106">The **ICM\_GETDEFAULTQUALITY** message queries a video compression driver to provide its default quality setting.</span></span> <span data-ttu-id="a97b0-107">Это сообщение можно отправить явно или с помощью макроса [**икжетдефаулткуалити**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality) .</span><span class="sxs-lookup"><span data-stu-id="a97b0-107">You can send this message explicitly or by using the [**ICGetDefaultQuality**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality) macro.</span></span>


```C++
ICM_GETDEFAULTQUALITY 
wParam = (DWORD_PTR) (LPVOID) &dwICValue; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="a97b0-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a97b0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a97b0-109"><span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*двиквалуе*</span><span class="sxs-lookup"><span data-stu-id="a97b0-109"><span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*</span></span>
</dt> <dd>

<span data-ttu-id="a97b0-110">Адрес, который будет содержать значение качества по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a97b0-110">Address to contain the default quality value.</span></span> <span data-ttu-id="a97b0-111">Значения качества находятся в диапазоне от 0 до 10 000.</span><span class="sxs-lookup"><span data-stu-id="a97b0-111">Quality values range from 0 to 10,000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a97b0-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a97b0-112">Return Value</span></span>

<span data-ttu-id="a97b0-113">Возвращает ИЦЕРР \_ ОК, если драйвер поддерживает это сообщение или ИЦЕРР \_ не поддерживается в противном случае.</span><span class="sxs-lookup"><span data-stu-id="a97b0-113">Returns ICERR\_OK if the driver supports this message or ICERR\_UNSUPPORTED otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="a97b0-114">Требования</span><span class="sxs-lookup"><span data-stu-id="a97b0-114">Requirements</span></span>



| <span data-ttu-id="a97b0-115">Требование</span><span class="sxs-lookup"><span data-stu-id="a97b0-115">Requirement</span></span> | <span data-ttu-id="a97b0-116">Значение</span><span class="sxs-lookup"><span data-stu-id="a97b0-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a97b0-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a97b0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a97b0-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a97b0-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="a97b0-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a97b0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a97b0-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a97b0-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a97b0-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a97b0-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a97b0-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="a97b0-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a97b0-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a97b0-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a97b0-124">Диспетчер сжатия видео</span><span class="sxs-lookup"><span data-stu-id="a97b0-124">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="a97b0-125">Сообщения о сжатии видео</span><span class="sxs-lookup"><span data-stu-id="a97b0-125">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 






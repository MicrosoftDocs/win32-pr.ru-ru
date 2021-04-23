---
title: Сообщение ICM_GETDEFAULTKEYFRAMERATE (VFW. h)
description: Сообщение ICM \_ жетдефаулткэйфрамерате запрашивает драйвер сжатия видео о его стандартном (или предпочтительном) интервале между кадрами. Это сообщение можно отправить явно или с помощью макроса Икжетдефаултэйфрамерате.
ms.assetid: 2ebe37cc-3ec2-4b52-bd8f-71c44b704647
keywords:
- ICM_GETDEFAULTKEYFRAMERATE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_GETDEFAULTKEYFRAMERATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e64f2796ca1c2de10222330217a0e1deb7883baa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415645"
---
# <a name="icm_getdefaultkeyframerate-message"></a><span data-ttu-id="ec881-105">\_Сообщение ICM жетдефаулткэйфрамерате</span><span class="sxs-lookup"><span data-stu-id="ec881-105">ICM\_GETDEFAULTKEYFRAMERATE message</span></span>

<span data-ttu-id="ec881-106">Сообщение **ICM \_ жетдефаулткэйфрамерате** запрашивает драйвер сжатия видео о его стандартном (или предпочтительном) интервале между кадрами.</span><span class="sxs-lookup"><span data-stu-id="ec881-106">The **ICM\_GETDEFAULTKEYFRAMERATE** message queries a video compression driver for its default (or preferred) key-frame spacing.</span></span> <span data-ttu-id="ec881-107">Это сообщение можно отправить явно или с помощью макроса [**икжетдефаултэйфрамерате**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) .</span><span class="sxs-lookup"><span data-stu-id="ec881-107">You can send this message explicitly or by using the [**ICGetDefaulteyFrameRate**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) macro.</span></span>


```C++
ICM_GETDEFAULTKEYFRAMERATE 
wParam = (DWORD_PTR) (LPVOID) &dwICValue; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="ec881-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ec881-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec881-109"><span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*двиквалуе*</span><span class="sxs-lookup"><span data-stu-id="ec881-109"><span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*</span></span>
</dt> <dd>

<span data-ttu-id="ec881-110">Адрес, который будет содержать предпочтительные интервалы между кадрами.</span><span class="sxs-lookup"><span data-stu-id="ec881-110">Address to contain the preferred key-frame spacing.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec881-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ec881-111">Return Value</span></span>

<span data-ttu-id="ec881-112">Возвращает ИЦЕРР \_ ОК, если драйвер поддерживает это сообщение или ИЦЕРР \_ не поддерживается в противном случае.</span><span class="sxs-lookup"><span data-stu-id="ec881-112">Returns ICERR\_OK if the driver supports this message or ICERR\_UNSUPPORTED otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec881-113">Требования</span><span class="sxs-lookup"><span data-stu-id="ec881-113">Requirements</span></span>



| <span data-ttu-id="ec881-114">Требование</span><span class="sxs-lookup"><span data-stu-id="ec881-114">Requirement</span></span> | <span data-ttu-id="ec881-115">Значение</span><span class="sxs-lookup"><span data-stu-id="ec881-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ec881-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ec881-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ec881-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ec881-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ec881-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ec881-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ec881-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ec881-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ec881-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="ec881-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec881-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec881-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec881-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ec881-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec881-123">Диспетчер сжатия видео</span><span class="sxs-lookup"><span data-stu-id="ec881-123">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="ec881-124">Сообщения о сжатии видео</span><span class="sxs-lookup"><span data-stu-id="ec881-124">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 






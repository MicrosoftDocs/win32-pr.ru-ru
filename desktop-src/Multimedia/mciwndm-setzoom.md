---
title: Сообщение MCIWNDM_SETZOOM (VFW. h)
description: Сообщение МЦИВНДМ \_ сетзум изменяет размер изображения видео в соответствии с коэффициентом масштабирования. Этот Марко корректирует размер МЦивнд окна, сохраняя постоянную пропорцию. Это сообщение можно отправить явно или с помощью макроса МЦивндсетзум.
ms.assetid: c899b678-5ba7-4f0a-9ef9-c5370b3b4ea8
keywords:
- MCIWNDM_SETZOOM сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_SETZOOM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80ecb513735c4e62266892e8ad55c7bf5daca151
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489408"
---
# <a name="mciwndm_setzoom-message"></a><span data-ttu-id="9085f-106">\_Сообщение мЦивндм сетзум</span><span class="sxs-lookup"><span data-stu-id="9085f-106">MCIWNDM\_SETZOOM message</span></span>

<span data-ttu-id="9085f-107">Сообщение **мЦивндм \_ сетзум** изменяет размер изображения видео в соответствии с коэффициентом масштабирования.</span><span class="sxs-lookup"><span data-stu-id="9085f-107">The **MCIWNDM\_SETZOOM** message resizes a video image according to a zoom factor.</span></span> <span data-ttu-id="9085f-108">Этот Марко корректирует размер МЦивнд окна, сохраняя постоянную пропорцию.</span><span class="sxs-lookup"><span data-stu-id="9085f-108">This marco adjusts the size of an MCIWnd window while maintaining a constant aspect ratio.</span></span> <span data-ttu-id="9085f-109">Это сообщение можно отправить явно или с помощью макроса [**мЦивндсетзум**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom) .</span><span class="sxs-lookup"><span data-stu-id="9085f-109">You can send this message explicitly or by using the [**MCIWndSetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom) macro.</span></span>


```C++
MCIWNDM_SETZOOM 
wParam = 0; 
lParam = (LPARAM) (UINT) iZoom; 
```



## <a name="parameters"></a><span data-ttu-id="9085f-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="9085f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9085f-111"><span id="iZoom"></span><span id="izoom"></span><span id="IZOOM"></span>*изум*</span><span class="sxs-lookup"><span data-stu-id="9085f-111"><span id="iZoom"></span><span id="izoom"></span><span id="IZOOM"></span>*iZoom*</span></span>
</dt> <dd>

<span data-ttu-id="9085f-112">Коэффициент масштабирования выражается в процентах от исходного изображения.</span><span class="sxs-lookup"><span data-stu-id="9085f-112">Zoom factor expressed as a percentage of the original image.</span></span> <span data-ttu-id="9085f-113">Укажите 100, чтобы изображение отображалось в созданном размере, 200, чтобы изображение отображалось в два раза больше обычного размера, или 50, чтобы изображение отображалось с половиной его обычного размера.</span><span class="sxs-lookup"><span data-stu-id="9085f-113">Specify 100 to display the image at its authored size, 200 to display the image at twice its normal size, or 50 to display the image at half its normal size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9085f-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9085f-114">Return Value</span></span>

<span data-ttu-id="9085f-115">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="9085f-115">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="9085f-116">Требования</span><span class="sxs-lookup"><span data-stu-id="9085f-116">Requirements</span></span>



| <span data-ttu-id="9085f-117">Требование</span><span class="sxs-lookup"><span data-stu-id="9085f-117">Requirement</span></span> | <span data-ttu-id="9085f-118">Значение</span><span class="sxs-lookup"><span data-stu-id="9085f-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="9085f-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9085f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9085f-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9085f-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="9085f-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9085f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9085f-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9085f-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9085f-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="9085f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9085f-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="9085f-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9085f-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9085f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9085f-126">**мЦивндсетзум**</span><span class="sxs-lookup"><span data-stu-id="9085f-126">**MCIWndSetZoom**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom)
</dt> </dl>

 

 






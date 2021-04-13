---
description: Указывает, является ли поток изображений в источнике видеозаписи независимым от видеопотока.
ms.assetid: DC4ED612-593B-40BF-BB42-946149042D1F
title: Атрибут MF_DEVICESTREAM_INDEPENDENT_IMAGE_STREAM (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 174e62a1bdd178ad2d8dce7fab5bf9ce3104d834
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647239"
---
# <a name="mf_devicestream_independent_image_stream-attribute"></a><span data-ttu-id="956ca-103">\_ \_ Атрибут потока с независимым \_ изображением MF девицестреам \_</span><span class="sxs-lookup"><span data-stu-id="956ca-103">MF\_DEVICESTREAM\_INDEPENDENT\_IMAGE\_STREAM attribute</span></span>

<span data-ttu-id="956ca-104">Указывает, является ли поток изображений в источнике видеозаписи независимым от видеопотока.</span><span class="sxs-lookup"><span data-stu-id="956ca-104">Specifies whether the image stream on a video capture source is independent of the video stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="956ca-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="956ca-105">Data type</span></span>

<span data-ttu-id="956ca-106">**Bool** , сохраненный как **UINT32**</span><span class="sxs-lookup"><span data-stu-id="956ca-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="956ca-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="956ca-107">Remarks</span></span>

<span data-ttu-id="956ca-108">Некоторые USB-камеры видео предоставляют поток, который создает изображения.</span><span class="sxs-lookup"><span data-stu-id="956ca-108">Some USB video cameras expose a stream that produces still images.</span></span> <span data-ttu-id="956ca-109">В некоторых камерах поток изображений просто возвращает следующий кадр из видеопотока.</span><span class="sxs-lookup"><span data-stu-id="956ca-109">In some cameras, the image stream simply returns the next frame from the video stream.</span></span> <span data-ttu-id="956ca-110">В других камерах поток изображений работает независимо от видеопотока.</span><span class="sxs-lookup"><span data-stu-id="956ca-110">In other cameras, the image stream functions independently of the video stream.</span></span> <span data-ttu-id="956ca-111">Если камера имеет независимый поток изображений, источник носителя для устройства записи устанавливает для этого атрибута **значение true** в потоке изображений.</span><span class="sxs-lookup"><span data-stu-id="956ca-111">If the camera has an independent image stream, the media source for the capture device sets this attribute to **TRUE** on the image stream.</span></span>

<span data-ttu-id="956ca-112">Чтобы получить этот атрибут, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="956ca-112">To get this attribute, do the following:</span></span>

1.  <span data-ttu-id="956ca-113">Запросите источник мультимедиа для интерфейса [**имфмедиасаурцеекс**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) .</span><span class="sxs-lookup"><span data-stu-id="956ca-113">Query the media source for the [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) interface.</span></span>
2.  <span data-ttu-id="956ca-114">Вызовите метод [**имфмедиасаурцеекс:: жетстреаматтрибутес**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) , чтобы получить указатель [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) для потока.</span><span class="sxs-lookup"><span data-stu-id="956ca-114">Call [**IMFMediaSourceEx::GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer for the stream.</span></span>
3.  <span data-ttu-id="956ca-115">Вызовите [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) , чтобы получить атрибут.</span><span class="sxs-lookup"><span data-stu-id="956ca-115">Call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) to get the attribute.</span></span>

<span data-ttu-id="956ca-116">Этот атрибут применяется только в том случае, если атрибут [ \_ \_ \_ потока изображений MF девицестреам](mf-devicestream-image-stream.md) имеет **значение true**.</span><span class="sxs-lookup"><span data-stu-id="956ca-116">This attribute applies only when the [MF\_DEVICESTREAM\_IMAGE\_STREAM](mf-devicestream-image-stream.md) attribute is **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="956ca-117">Требования</span><span class="sxs-lookup"><span data-stu-id="956ca-117">Requirements</span></span>



| <span data-ttu-id="956ca-118">Требование</span><span class="sxs-lookup"><span data-stu-id="956ca-118">Requirement</span></span> | <span data-ttu-id="956ca-119">Значение</span><span class="sxs-lookup"><span data-stu-id="956ca-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="956ca-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="956ca-120">Minimum supported client</span></span><br/> | <span data-ttu-id="956ca-121">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="956ca-121">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="956ca-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="956ca-122">Minimum supported server</span></span><br/> | <span data-ttu-id="956ca-123">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="956ca-123">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="956ca-124">Header</span><span class="sxs-lookup"><span data-stu-id="956ca-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="956ca-125"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="956ca-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="956ca-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="956ca-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="956ca-127">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="956ca-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 





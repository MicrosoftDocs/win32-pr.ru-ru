---
description: Указывает, является ли поток в источнике видеозаписи по-прежнему потоком изображения.
ms.assetid: 52251A45-3603-41C7-A869-7F6319BD337F
title: Атрибут MF_DEVICESTREAM_IMAGE_STREAM (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 382ce587574d6ec46509a460dfb964e23dd416d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810486"
---
# <a name="mf_devicestream_image_stream-attribute"></a><span data-ttu-id="ac079-103">\_ \_ Атрибут потока изображений MF девицестреам \_</span><span class="sxs-lookup"><span data-stu-id="ac079-103">MF\_DEVICESTREAM\_IMAGE\_STREAM attribute</span></span>

<span data-ttu-id="ac079-104">Указывает, является ли поток в источнике видеозаписи по-прежнему потоком изображения.</span><span class="sxs-lookup"><span data-stu-id="ac079-104">Specifies whether a stream on a video capture source is a still-image stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="ac079-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="ac079-105">Data type</span></span>

<span data-ttu-id="ac079-106">**Bool** , сохраненный как **UINT32**</span><span class="sxs-lookup"><span data-stu-id="ac079-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="ac079-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ac079-107">Remarks</span></span>

<span data-ttu-id="ac079-108">Некоторые видеокамеры предоставляют поток с изображением по-прежнему, который создает изображения с высоким разрешением.</span><span class="sxs-lookup"><span data-stu-id="ac079-108">Some video cameras expose a still-image stream that produces high-resolution images.</span></span> <span data-ttu-id="ac079-109">Поток изображений может создавать несжатые изображения или изображения в формате JPEG.</span><span class="sxs-lookup"><span data-stu-id="ac079-109">The image stream might produce uncompressed images or JPEG images.</span></span> <span data-ttu-id="ac079-110">Если камера имеет поток изображений, источник носителя для устройства записи устанавливает для этого атрибута **значение true** в потоке изображений.</span><span class="sxs-lookup"><span data-stu-id="ac079-110">If the camera has an image stream, the media source for the capture device sets this attribute to **TRUE** on the image stream.</span></span>

<span data-ttu-id="ac079-111">Чтобы получить этот атрибут, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ac079-111">To get this attribute, do the following:</span></span>

1.  <span data-ttu-id="ac079-112">Запросите источник мультимедиа для интерфейса [**имфмедиасаурцеекс**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) .</span><span class="sxs-lookup"><span data-stu-id="ac079-112">Query the media source for the [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) interface.</span></span>
2.  <span data-ttu-id="ac079-113">Вызовите метод [**имфмедиасаурцеекс:: жетстреаматтрибутес**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) , чтобы получить указатель [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) для потока.</span><span class="sxs-lookup"><span data-stu-id="ac079-113">Call [**IMFMediaSourceEx::GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer for the stream.</span></span>
3.  <span data-ttu-id="ac079-114">Вызовите [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) , чтобы получить атрибут.</span><span class="sxs-lookup"><span data-stu-id="ac079-114">Call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) to get the attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac079-115">Требования</span><span class="sxs-lookup"><span data-stu-id="ac079-115">Requirements</span></span>



| <span data-ttu-id="ac079-116">Требование</span><span class="sxs-lookup"><span data-stu-id="ac079-116">Requirement</span></span> | <span data-ttu-id="ac079-117">Значение</span><span class="sxs-lookup"><span data-stu-id="ac079-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ac079-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ac079-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ac079-119">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ac079-119">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ac079-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ac079-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ac079-121">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ac079-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ac079-122">Header</span><span class="sxs-lookup"><span data-stu-id="ac079-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac079-123"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac079-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac079-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ac079-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac079-125">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ac079-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 





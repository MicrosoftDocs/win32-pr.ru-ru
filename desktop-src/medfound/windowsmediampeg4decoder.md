---
description: Декодер Windows Media MPEG4 версии 1/v2 декодирует видеопотокы версии MPEG4 v1/v2.
ms.assetid: 63b32972-1003-4291-bfdd-cc0cb8d65430
title: Декодер Windows Media MPEG4 версии 1/v2 (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b14cf22e29c1266ac9bb3593375ee4485d79df2
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105713249"
---
# <a name="windows-media-mpeg4-v1v2-decoder"></a><span data-ttu-id="12279-103">Декодер Windows Media MPEG4 версии 1/v2</span><span class="sxs-lookup"><span data-stu-id="12279-103">Windows Media MPEG4 V1/V2 Decoder</span></span>

<span data-ttu-id="12279-104">Декодер Windows Media MPEG4 версии 1/v2 декодирует видеопотокы версии MPEG4 v1/v2.</span><span class="sxs-lookup"><span data-stu-id="12279-104">The Windows Media MPEG4 V1/V2 decoder decodes MPEG4 V1/V2 video streams.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="12279-105">Идентификатор класса</span><span class="sxs-lookup"><span data-stu-id="12279-105">Class Identifier</span></span>

<span data-ttu-id="12279-106">Идентификатор класса (CLSID) для декодера Windows Media MPEG4 v1/v2 представлен константой **CLSID \_ CMpeg4DecMediaObject**.</span><span class="sxs-lookup"><span data-stu-id="12279-106">The class identifier (CLSID) for the Windows Media MPEG4 V1/V2 decoder is represented by the constant **CLSID\_CMpeg4DecMediaObject**.</span></span> <span data-ttu-id="12279-107">Можно создать экземпляр декодера MPEG4 версии 1/v2, вызвав **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="12279-107">You can create an instance of the MPEG4 V1/V2 decoder by calling **CoCreateInstance**.</span></span>

## <a name="formats"></a><span data-ttu-id="12279-108">Форматы</span><span class="sxs-lookup"><span data-stu-id="12279-108">Formats</span></span>

<span data-ttu-id="12279-109">Декодер Windows Media MPEG4 версии 1/v2 поддерживает следующие входные типы носителей.</span><span class="sxs-lookup"><span data-stu-id="12279-109">The Windows Media MPEG4 V1/V2 decoder supports the following input media types.</span></span>

-   <span data-ttu-id="12279-110">МЕДИАСУБТИПЕ \_ MPG4</span><span class="sxs-lookup"><span data-stu-id="12279-110">MEDIASUBTYPE\_MPG4</span></span>
-   <span data-ttu-id="12279-111">МЕДИАСУБТИПЕ \_ MPG4</span><span class="sxs-lookup"><span data-stu-id="12279-111">MEDIASUBTYPE\_mpg4</span></span>
-   <span data-ttu-id="12279-112">МЕДИАСУБТИПЕ \_ MP42</span><span class="sxs-lookup"><span data-stu-id="12279-112">MEDIASUBTYPE\_MP42</span></span>
-   <span data-ttu-id="12279-113">МЕДИАСУБТИПЕ \_ MP42</span><span class="sxs-lookup"><span data-stu-id="12279-113">MEDIASUBTYPE\_mp42</span></span>

<span data-ttu-id="12279-114">Декодер Windows Media MPEG4 версии 1/v2 поддерживает следующие подтипы выходных данных, когда он выступает в качестве объекта мультимедиа DirectX (DMO).</span><span class="sxs-lookup"><span data-stu-id="12279-114">The Windows Media MPEG4 V1/V2 decoder supports the following output media subtypes when it is acting as a DirectX Media Object (DMO).</span></span>

-   <span data-ttu-id="12279-115">МЕДИАСУБТИПЕ \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="12279-115">MEDIASUBTYPE\_YUY2</span></span>
-   <span data-ttu-id="12279-116">МЕДИАСУБТИПЕ \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="12279-116">MEDIASUBTYPE\_UYVY</span></span>
-   <span data-ttu-id="12279-117">МЕДИАСУБТИПЕ \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="12279-117">MEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="12279-118">МЕДИАСУБТИПЕ \_ Rgb24</span><span class="sxs-lookup"><span data-stu-id="12279-118">MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="12279-119">МЕДИАСУБТИПЕ \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="12279-119">MEDIASUBTYPE\_RGB565</span></span>
-   <span data-ttu-id="12279-120">МЕДИАСУБТИПЕ \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="12279-120">MEDIASUBTYPE\_RGB8</span></span>
-   <span data-ttu-id="12279-121">МЕДИАСУБТИПЕ \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="12279-121">MEDIASUBTYPE\_RGB555</span></span>

<span data-ttu-id="12279-122">Декодер Windows Media MPEG4 версии 1/v2 поддерживает следующие подтипы выходных данных, когда он выступает в качестве Media Foundation преобразования (MFT).</span><span class="sxs-lookup"><span data-stu-id="12279-122">The Windows Media MPEG4 V1/V2 decoder supports the following output media subtypes when it is acting as a Media Foundation Transform (MFT).</span></span>

-   <span data-ttu-id="12279-123">Мфвидеоформат \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="12279-123">MFVideoFormat\_YUY2</span></span>
-   <span data-ttu-id="12279-124">Мфвидеоформат \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="12279-124">MFVideoFormat\_UYVY</span></span>
-   <span data-ttu-id="12279-125">Мфвидеоформат \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="12279-125">MFVideoFormat\_RGB32</span></span>
-   <span data-ttu-id="12279-126">Мфвидеоформат \_ Rgb24</span><span class="sxs-lookup"><span data-stu-id="12279-126">MFVideoFormat\_RGB24</span></span>
-   <span data-ttu-id="12279-127">Мфвидеоформат \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="12279-127">MFVideoFormat\_RGB565</span></span>
-   <span data-ttu-id="12279-128">Мфвидеоформат \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="12279-128">MFVideoFormat\_RGB8</span></span>
-   <span data-ttu-id="12279-129">Мфвидеоформат \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="12279-129">MFVideoFormat\_RGB555</span></span>

## <a name="remarks"></a><span data-ttu-id="12279-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="12279-130">Remarks</span></span>

<span data-ttu-id="12279-131">Объект декодера Windows Media MPEG4 версии 1/v2 предоставляет интерфейс [**имедиаобжект**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) , чтобы объект можно было использовать в качестве объекта мультимедиа DirectX (DMO), и он предоставляет интерфейс [**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) , чтобы объект можно было использовать в качестве Media Foundation преобразования (MFT).</span><span class="sxs-lookup"><span data-stu-id="12279-131">The Windows Media MPEG4 V1/V2 decoder object exposes the [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface so that the object can be used as a Media Foundation Transform (MFT).</span></span> <span data-ttu-id="12279-132">Объект имеет тот же идентификатор класса (CLSID), независимо от того, действует ли он как DMO или MFT.</span><span class="sxs-lookup"><span data-stu-id="12279-132">The object has the same class identifier (CLSID) regardless of whether it acts as a DMO or an MFT.</span></span>

<span data-ttu-id="12279-133">Декодеры MPEG4 версии 1 и v2 работают как объекты DMO или MFT в зависимости от того, какие интерфейсы получены и какая версия Windows выполняется.</span><span class="sxs-lookup"><span data-stu-id="12279-133">An MPEG4 V1/V2 decoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="12279-134">В следующей таблице показаны условия, при которых декодер MPEG4 версии 1 и v2 ведет себя как DMO или MFT.</span><span class="sxs-lookup"><span data-stu-id="12279-134">The following table shows the conditions under which an MPEG4 V1/V2 decoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="12279-135">Операционная система</span><span class="sxs-lookup"><span data-stu-id="12279-135">Operating system</span></span>            | <span data-ttu-id="12279-136">Поведение декодера</span><span class="sxs-lookup"><span data-stu-id="12279-136">Decoder behavior</span></span>                                                                                                                                                                |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12279-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="12279-137">Windows XP</span></span>                  | <span data-ttu-id="12279-138">Декодер MPEG4 версии 1 или v2 всегда ведет себя как DMO.</span><span class="sxs-lookup"><span data-stu-id="12279-138">An MPEG4 V1/V2 decoder always behaves as a DMO.</span></span>                                                                                                                                 |
| <span data-ttu-id="12279-139">Windows Vista и Windows 7</span><span class="sxs-lookup"><span data-stu-id="12279-139">Windows Vista and Windows 7</span></span> | <span data-ttu-id="12279-140">По умолчанию декодеры MPEG4 версии 1 и v2 ведет себя как DMO.</span><span class="sxs-lookup"><span data-stu-id="12279-140">By default, an MPEG4 V1/V2 decoder behaves as a DMO.</span></span> <span data-ttu-id="12279-141">Если вы получаете интерфейс [GUID подтипа видео](video-subtype-guids.md) для декодера MPEG4 версии 1/v2, он ведет себя как MFT.</span><span class="sxs-lookup"><span data-stu-id="12279-141">If you obtain an [Video Subtype GUIDs](video-subtype-guids.md) interface on an MPEG4 V1/V2 decoder, it behaves as an MFT.</span></span> |



 

<span data-ttu-id="12279-142">Глобальные уникальные идентификаторы (GUID) для подтипов мультимедиа RGB различаются в зависимости от того, выступает ли декодер в качестве DMO или MFT.</span><span class="sxs-lookup"><span data-stu-id="12279-142">The globally unique identifiers (GUIDs) for RGB media subtypes differ depending on whether a decoder is acting as a DMO or an MFT.</span></span> <span data-ttu-id="12279-143">Идентификаторы GUID для подтипов мультимедиа, отличных от RGB, одинаковы, независимо от того, выступает ли декодер в качестве DMO или MFT.</span><span class="sxs-lookup"><span data-stu-id="12279-143">The GUIDs for non-RGB media subtypes are the same, regardless of whether a decoder is acting as a DMO or an MFT.</span></span> <span data-ttu-id="12279-144">Сведения об идентификаторах GUID, представляющих подтипы видео, см. в разделе [GUID для подтипов видео](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="12279-144">For information about the GUIDs that represent video subtypes, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="12279-145">Требования</span><span class="sxs-lookup"><span data-stu-id="12279-145">Requirements</span></span>



| <span data-ttu-id="12279-146">Требование</span><span class="sxs-lookup"><span data-stu-id="12279-146">Requirement</span></span> | <span data-ttu-id="12279-147">Значение</span><span class="sxs-lookup"><span data-stu-id="12279-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="12279-148">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="12279-148">Minimum supported client</span></span><br/> | <span data-ttu-id="12279-149">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="12279-149">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="12279-150">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="12279-150">Minimum supported server</span></span><br/> | <span data-ttu-id="12279-151">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="12279-151">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="12279-152">Header</span><span class="sxs-lookup"><span data-stu-id="12279-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="12279-153"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="12279-153"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="12279-154">DLL</span><span class="sxs-lookup"><span data-stu-id="12279-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12279-155"><dt>MPG4DECD.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12279-155"><dt>MPG4DECD.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12279-156">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="12279-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12279-157">Объекты кодека</span><span class="sxs-lookup"><span data-stu-id="12279-157">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 

---
description: Декодер Windows Media MPEG-4 v3 декодирует видеопотоки MPEG-4 v3.
ms.assetid: 5143b0cc-c171-46af-8d7f-4d029af71fb4
title: Декодер Windows Media MPEG-4 v3 (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ee98a0a3c4b221da6f2000e32d4c75bc3e3a93b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105713265"
---
# <a name="windows-media-mpeg-4-v3-decoder"></a><span data-ttu-id="37cb1-103">Декодер Windows Media MPEG-4 v3</span><span class="sxs-lookup"><span data-stu-id="37cb1-103">Windows Media MPEG-4 V3 Decoder</span></span>

<span data-ttu-id="37cb1-104">Декодер Windows Media MPEG-4 v3 декодирует видеопотоки MPEG-4 v3.</span><span class="sxs-lookup"><span data-stu-id="37cb1-104">The Windows Media MPEG-4 V3 decoder decodes MPEG-4 V3 video streams.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="37cb1-105">Идентификатор класса</span><span class="sxs-lookup"><span data-stu-id="37cb1-105">Class Identifier</span></span>

<span data-ttu-id="37cb1-106">Идентификатор класса (CLSID) для декодера Windows MPEG-4 v3 представлен константой **CLSID \_ CMpeg43DecMediaObject**.</span><span class="sxs-lookup"><span data-stu-id="37cb1-106">The class identifier (CLSID) for the Windows MPEG-4 V3 decoder is represented by the constant **CLSID\_CMpeg43DecMediaObject**.</span></span> <span data-ttu-id="37cb1-107">Вы можете создать экземпляр декодера MPEG-4 v3, вызвав **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="37cb1-107">You can create an instance of the MPEG-4 V3 decoder by calling **CoCreateInstance**.</span></span>

## <a name="formats"></a><span data-ttu-id="37cb1-108">Форматы</span><span class="sxs-lookup"><span data-stu-id="37cb1-108">Formats</span></span>

<span data-ttu-id="37cb1-109">Декодер Windows Media MPEG-4 v3 поддерживает следующие входные типы носителей.</span><span class="sxs-lookup"><span data-stu-id="37cb1-109">The Windows Media MPEG-4 V3 decoder supports the following input media types.</span></span>

-   <span data-ttu-id="37cb1-110">МЕДИАСУБТИПЕ \_ MP43</span><span class="sxs-lookup"><span data-stu-id="37cb1-110">MEDIASUBTYPE\_MP43</span></span>
-   <span data-ttu-id="37cb1-111">МЕДИАСУБТИПЕ \_ MP43</span><span class="sxs-lookup"><span data-stu-id="37cb1-111">MEDIASUBTYPE\_mp43</span></span>

<span data-ttu-id="37cb1-112">Декодер Windows Media MPEG-4 v3 поддерживает следующие подтипы выходных данных, когда он выступает в качестве объекта мультимедиа DirectX (DMO).</span><span class="sxs-lookup"><span data-stu-id="37cb1-112">The Windows Media MPEG-4 V3 decoder supports the following output media subtypes when it is acting as a DirectX Media Object (DMO).</span></span>

-   <span data-ttu-id="37cb1-113">МЕДИАСУБТИПЕ \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="37cb1-113">MEDIASUBTYPE\_YUY2</span></span>
-   <span data-ttu-id="37cb1-114">МЕДИАСУБТИПЕ \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="37cb1-114">MEDIASUBTYPE\_UYVY</span></span>
-   <span data-ttu-id="37cb1-115">МЕДИАСУБТИПЕ \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="37cb1-115">MEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="37cb1-116">МЕДИАСУБТИПЕ \_ Rgb24</span><span class="sxs-lookup"><span data-stu-id="37cb1-116">MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="37cb1-117">МЕДИАСУБТИПЕ \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="37cb1-117">MEDIASUBTYPE\_RGB565</span></span>
-   <span data-ttu-id="37cb1-118">МЕДИАСУБТИПЕ \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="37cb1-118">MEDIASUBTYPE\_RGB8</span></span>
-   <span data-ttu-id="37cb1-119">МЕДИАСУБТИПЕ \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="37cb1-119">MEDIASUBTYPE\_RGB555</span></span>

<span data-ttu-id="37cb1-120">Декодер Windows Media MPEG-4 v3 поддерживает следующие выходные типы выходных данных, когда он выступает в качестве Media Foundation преобразования (MFT).</span><span class="sxs-lookup"><span data-stu-id="37cb1-120">The Windows Media MPEG-4 V3 decoder supports the following output media subtypes when it is acting as a Media Foundation Transform (MFT).</span></span>

-   <span data-ttu-id="37cb1-121">Мфвидеоформат \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="37cb1-121">MFVideoFormat\_YUY2</span></span>
-   <span data-ttu-id="37cb1-122">Мфвидеоформат \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="37cb1-122">MFVideoFormat\_UYVY</span></span>
-   <span data-ttu-id="37cb1-123">Мфвидеоформат \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="37cb1-123">MFVideoFormat\_RGB32</span></span>
-   <span data-ttu-id="37cb1-124">Мфвидеоформат \_ Rgb24</span><span class="sxs-lookup"><span data-stu-id="37cb1-124">MFVideoFormat\_RGB24</span></span>
-   <span data-ttu-id="37cb1-125">Мфвидеоформат \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="37cb1-125">MFVideoFormat\_RGB565</span></span>
-   <span data-ttu-id="37cb1-126">Мфвидеоформат \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="37cb1-126">MFVideoFormat\_RGB8</span></span>
-   <span data-ttu-id="37cb1-127">Мфвидеоформат \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="37cb1-127">MFVideoFormat\_RGB555</span></span>

## <a name="remarks"></a><span data-ttu-id="37cb1-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="37cb1-128">Remarks</span></span>

<span data-ttu-id="37cb1-129">Объект декодера MPEG-4 v3 Windows Media предоставляет интерфейс [**имедиаобжект**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) , чтобы объект можно было использовать в качестве объекта мультимедиа DirectX (DMO), и он предоставляет интерфейс [**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) , чтобы объект можно было использовать в качестве Media Foundation преобразования (MFT).</span><span class="sxs-lookup"><span data-stu-id="37cb1-129">The Windows Media MPEG-4 V3 decoder object exposes the [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface so that the object can be used as a Media Foundation Transform (MFT).</span></span> <span data-ttu-id="37cb1-130">Объект имеет тот же идентификатор класса (CLSID), независимо от того, действует ли он как DMO или MFT.</span><span class="sxs-lookup"><span data-stu-id="37cb1-130">The object has the same class identifier (CLSID) regardless of whether it acts as a DMO or an MFT.</span></span>

<span data-ttu-id="37cb1-131">Декодер MPEG-4 v3 ведет себя как DMO или MFT в зависимости от того, какие интерфейсы вы получаете и какая версия Windows выполняется.</span><span class="sxs-lookup"><span data-stu-id="37cb1-131">The MPEG-4 V3 decoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="37cb1-132">В следующей таблице показаны условия, при которых декодер MPEG-4 v3 ведет себя как DMO или MFT.</span><span class="sxs-lookup"><span data-stu-id="37cb1-132">The following table shows the conditions under which an MPEG-4 V3 decoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="37cb1-133">Операционная система</span><span class="sxs-lookup"><span data-stu-id="37cb1-133">Operating system</span></span>            | <span data-ttu-id="37cb1-134">Поведение декодера</span><span class="sxs-lookup"><span data-stu-id="37cb1-134">Decoder behavior</span></span>                                                                                                                                                    |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37cb1-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="37cb1-135">Windows XP</span></span>                  | <span data-ttu-id="37cb1-136">Декодер MPEG-4 v3 всегда ведет себя как DMO.</span><span class="sxs-lookup"><span data-stu-id="37cb1-136">The MPEG-4 V3 decoder always behaves as a DMO.</span></span>                                                                                                                      |
| <span data-ttu-id="37cb1-137">Windows Vista и Windows 7</span><span class="sxs-lookup"><span data-stu-id="37cb1-137">Windows Vista and Windows 7</span></span> | <span data-ttu-id="37cb1-138">По умолчанию декодер MPEG-4 v3 ведет себя как DMO.</span><span class="sxs-lookup"><span data-stu-id="37cb1-138">By default, the MPEG-4 V3 decoder behaves as a DMO.</span></span> <span data-ttu-id="37cb1-139">Если вы получаете интерфейс [**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) в декодере MPEG-4 v3, он ведет себя как MFT.</span><span class="sxs-lookup"><span data-stu-id="37cb1-139">If you obtain an [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface on the MPEG-4 V3 decoder, it behaves as an MFT.</span></span> |



 

<span data-ttu-id="37cb1-140">Глобальные уникальные идентификаторы (GUID) для подтипов мультимедиа RGB различаются в зависимости от того, выступает ли декодер в качестве DMO или MFT.</span><span class="sxs-lookup"><span data-stu-id="37cb1-140">The globally unique identifiers (GUIDs) for RGB media subtypes differ depending on whether a decoder is acting as a DMO or an MFT.</span></span> <span data-ttu-id="37cb1-141">Идентификаторы GUID для подтипов мультимедиа, отличных от RGB, одинаковы, независимо от того, выступает ли декодер в качестве DMO или MFT.</span><span class="sxs-lookup"><span data-stu-id="37cb1-141">The GUIDs for non-RGB media subtypes are the same, regardless of whether a decoder is acting as a DMO or an MFT.</span></span> <span data-ttu-id="37cb1-142">Сведения об идентификаторах GUID, представляющих подтипы мультимедиа, см. в разделе [GUID для подтипов видео](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="37cb1-142">For information about the GUIDs that represent media subtypes, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="37cb1-143">Требования</span><span class="sxs-lookup"><span data-stu-id="37cb1-143">Requirements</span></span>



| <span data-ttu-id="37cb1-144">Требование</span><span class="sxs-lookup"><span data-stu-id="37cb1-144">Requirement</span></span> | <span data-ttu-id="37cb1-145">Значение</span><span class="sxs-lookup"><span data-stu-id="37cb1-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="37cb1-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="37cb1-146">Minimum supported client</span></span><br/> | <span data-ttu-id="37cb1-147">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="37cb1-147">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="37cb1-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="37cb1-148">Minimum supported server</span></span><br/> | <span data-ttu-id="37cb1-149">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="37cb1-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="37cb1-150">Header</span><span class="sxs-lookup"><span data-stu-id="37cb1-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="37cb1-151"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="37cb1-151"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="37cb1-152">DLL</span><span class="sxs-lookup"><span data-stu-id="37cb1-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37cb1-153"><dt>MP43DECD.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37cb1-153"><dt>MP43DECD.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37cb1-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="37cb1-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37cb1-155">Объекты кодека</span><span class="sxs-lookup"><span data-stu-id="37cb1-155">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 

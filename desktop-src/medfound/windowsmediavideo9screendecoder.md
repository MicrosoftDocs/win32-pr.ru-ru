---
description: Экранный декодер Windows Media Video 9 декодирует потоки, закодированные кодировщиком экрана Windows Media видео 9.
ms.assetid: 6688a830-7a54-4f58-947e-26013e191b5f
title: Декодер экрана Windows Media Video 9 (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd9dcdce920fa39437edb769fd575a7d7a0d68fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704441"
---
# <a name="windows-media-video-9-screen-decoder"></a><span data-ttu-id="dbf68-103">Декодер экрана Windows Media видео 9</span><span class="sxs-lookup"><span data-stu-id="dbf68-103">Windows Media Video 9 Screen Decoder</span></span>

<span data-ttu-id="dbf68-104">Экранный декодер Windows Media Video 9 декодирует потоки, закодированные [**кодировщиком экрана Windows Media видео 9**](windowsmediavideo9screenencoder.md).</span><span class="sxs-lookup"><span data-stu-id="dbf68-104">The Windows Media Video 9 Screen decoder decodes streams that were encoded by the [**Windows Media Video 9 Screen Encoder**](windowsmediavideo9screenencoder.md).</span></span>

## <a name="class-identifier"></a><span data-ttu-id="dbf68-105">Идентификатор класса</span><span class="sxs-lookup"><span data-stu-id="dbf68-105">Class Identifier</span></span>

<span data-ttu-id="dbf68-106">Идентификатор класса (CLSID) для декодера экрана Windows Media Video 9 представлен константой **CLSID \_ кмсскдекмедиаобжект**.</span><span class="sxs-lookup"><span data-stu-id="dbf68-106">The class identifier (CLSID) for the Windows Media Video 9 Screen decoder is represented by the constant **CLSID\_CMSSCDecMediaObject**.</span></span> <span data-ttu-id="dbf68-107">Можно создать экземпляр декодера, вызвав **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="dbf68-107">You can create an instance of the decoder by calling **CoCreateInstance**.</span></span>

## <a name="input-types"></a><span data-ttu-id="dbf68-108">Типы входных данных</span><span class="sxs-lookup"><span data-stu-id="dbf68-108">Input Types</span></span>

<span data-ttu-id="dbf68-109">Код из четырех символов (FOURCC) для содержимого с видео Windows Media версии 9 — "MSS2".</span><span class="sxs-lookup"><span data-stu-id="dbf68-109">The four-character code (FOURCC) for Windows Media Video Screen Version 9 encoded content is "MSS2".</span></span>

<span data-ttu-id="dbf68-110">Декодер экрана версии 9 поддерживает следующие типы входных данных.</span><span class="sxs-lookup"><span data-stu-id="dbf68-110">The following input types are supported by the Version 9 Screen decoder.</span></span>

-   <span data-ttu-id="dbf68-111">МЕДИАСУБТИПЕ \_ MSS2</span><span class="sxs-lookup"><span data-stu-id="dbf68-111">MEDIASUBTYPE\_MSS2</span></span>

## <a name="output-types"></a><span data-ttu-id="dbf68-112">Типы вывода</span><span class="sxs-lookup"><span data-stu-id="dbf68-112">Output Types</span></span>

<span data-ttu-id="dbf68-113">Декодеры экрана версии 9 поддерживают следующие типы выходных данных, если они используются как объект мультимедиа DirectX (DMO).</span><span class="sxs-lookup"><span data-stu-id="dbf68-113">The following output types are supported by the Version 9 Screen decoder when it is being used as a DirectX Media Object (DMO).</span></span>

-   <span data-ttu-id="dbf68-114">МЕДИАСУБТИПЕ \_ Rgb24</span><span class="sxs-lookup"><span data-stu-id="dbf68-114">MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="dbf68-115">МЕДИАСУБТИПЕ \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="dbf68-115">MEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="dbf68-116">МЕДИАСУБТИПЕ \_ ARGB32</span><span class="sxs-lookup"><span data-stu-id="dbf68-116">MEDIASUBTYPE\_ARGB32</span></span>
-   <span data-ttu-id="dbf68-117">МЕДИАСУБТИПЕ \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="dbf68-117">MEDIASUBTYPE\_RGB565</span></span>
-   <span data-ttu-id="dbf68-118">МЕДИАСУБТИПЕ \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="dbf68-118">MEDIASUBTYPE\_RGB555</span></span>
-   <span data-ttu-id="dbf68-119">МЕДИАСУБТИПЕ \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="dbf68-119">MEDIASUBTYPE\_RGB8</span></span>

<span data-ttu-id="dbf68-120">Декодеры экрана версии 9 поддерживают следующие типы выходных данных, если они используются в качестве Media Foundation преобразования (MFT).</span><span class="sxs-lookup"><span data-stu-id="dbf68-120">The following output types are supported by the Version 9 Screen decoder when it is being used as a Media Foundation Transform (MFT).</span></span>

-   <span data-ttu-id="dbf68-121">Мфвидеоформат \_ Rgb24</span><span class="sxs-lookup"><span data-stu-id="dbf68-121">MFVideoFormat\_RGB24</span></span>
-   <span data-ttu-id="dbf68-122">Мфвидеоформат \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="dbf68-122">MFVideoFormat\_RGB32</span></span>
-   <span data-ttu-id="dbf68-123">Мфвидеоформат \_ ARGB32</span><span class="sxs-lookup"><span data-stu-id="dbf68-123">MFVideoFormat\_ARGB32</span></span>
-   <span data-ttu-id="dbf68-124">Мфвидеоформат \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="dbf68-124">MFVideoFormat\_RGB565</span></span>
-   <span data-ttu-id="dbf68-125">Мфвидеоформат \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="dbf68-125">MFVideoFormat\_RGB555</span></span>
-   <span data-ttu-id="dbf68-126">Мфвидеоформат \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="dbf68-126">MFVideoFormat\_RGB8</span></span>

## <a name="remarks"></a><span data-ttu-id="dbf68-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dbf68-127">Remarks</span></span>

<span data-ttu-id="dbf68-128">Объект декодера экрана предоставляет интерфейс [**имедиаобжект**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) , чтобы объект можно было использовать в качестве объекта мультимедиа DirectX (DMO), и он предоставляет интерфейс [**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) , чтобы объект можно было использовать в качестве Media Foundation преобразования (MFT).</span><span class="sxs-lookup"><span data-stu-id="dbf68-128">A screen decoder object exposes the [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface so that the object can be used as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="dbf68-129">Декодер экрана ведет себя как DMO или MFT в зависимости от того, какие интерфейсы вы получаете и какая версия Windows выполняется.</span><span class="sxs-lookup"><span data-stu-id="dbf68-129">A screen decoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="dbf68-130">В следующей таблице показаны условия, при которых декодер экрана ведет себя как DMO или MFT.</span><span class="sxs-lookup"><span data-stu-id="dbf68-130">The following table shows the conditions under which a screen decoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="dbf68-131">Операционная система</span><span class="sxs-lookup"><span data-stu-id="dbf68-131">Operating system</span></span>            | <span data-ttu-id="dbf68-132">Поведение декодера</span><span class="sxs-lookup"><span data-stu-id="dbf68-132">Decoder behavior</span></span>                                                                                                                                                        |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbf68-133">Windows XP</span><span class="sxs-lookup"><span data-stu-id="dbf68-133">Windows XP</span></span>                  | <span data-ttu-id="dbf68-134">Декодер экрана Windows Media всегда ведет себя как DMO.</span><span class="sxs-lookup"><span data-stu-id="dbf68-134">A Windows Media Screen decoder always behaves as a DMO.</span></span>                                                                                                                 |
| <span data-ttu-id="dbf68-135">Windows Vista и Windows 7</span><span class="sxs-lookup"><span data-stu-id="dbf68-135">Windows Vista and Windows 7</span></span> | <span data-ttu-id="dbf68-136">По умолчанию декодер экрана Windows Media ведет себя как DMO.</span><span class="sxs-lookup"><span data-stu-id="dbf68-136">By default, a Windows Media Screen decoder behaves as a DMO.</span></span> <span data-ttu-id="dbf68-137">При получении интерфейса [**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) на экране декодера он ведет себя как MFT.</span><span class="sxs-lookup"><span data-stu-id="dbf68-137">If you obtain an [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface on a screen decoder, it behaves as an MFT.</span></span> |



 

<span data-ttu-id="dbf68-138">Вы можете использовать один CLSID (CLSID \_ кмсскдекмедиаобжект) для создания декодера экрана версии 7 и декодера экрана версии 9.</span><span class="sxs-lookup"><span data-stu-id="dbf68-138">You can use the same CLSID (CLSID\_CMSSCDecMediaObject) to create the Version 7 Screen decoder and the Version 9 Screen decoder.</span></span> <span data-ttu-id="dbf68-139">Содержимое объекта FOURCC для Windows Media Video Screen с кодировкой 7 — "MSS1".</span><span class="sxs-lookup"><span data-stu-id="dbf68-139">The FOURCC for Windows Media Video Screen Version 7 encoded content is "MSS1".</span></span> <span data-ttu-id="dbf68-140">Декодер экрана версии 7 поддерживает \_ входной тип медиасубтипе MSS1.</span><span class="sxs-lookup"><span data-stu-id="dbf68-140">The Version 7 Screen decoder supports the MEDIASUBTYPE\_MSS1 input type.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbf68-141">Требования</span><span class="sxs-lookup"><span data-stu-id="dbf68-141">Requirements</span></span>



| <span data-ttu-id="dbf68-142">Требование</span><span class="sxs-lookup"><span data-stu-id="dbf68-142">Requirement</span></span> | <span data-ttu-id="dbf68-143">Значение</span><span class="sxs-lookup"><span data-stu-id="dbf68-143">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dbf68-144">Клиент</span><span class="sxs-lookup"><span data-stu-id="dbf68-144">Client</span></span><br/> | <span data-ttu-id="dbf68-145">Windows XP, Windows Vista или Windows 7</span><span class="sxs-lookup"><span data-stu-id="dbf68-145">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="dbf68-146">Header</span><span class="sxs-lookup"><span data-stu-id="dbf68-146">Header</span></span><br/> | <dl> <span data-ttu-id="dbf68-147"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="dbf68-147"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="dbf68-148">DLL</span><span class="sxs-lookup"><span data-stu-id="dbf68-148">DLL</span></span><br/>    | <dl> <span data-ttu-id="dbf68-149"><dt>Wmvsdecd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dbf68-149"><dt>Wmvsdecd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbf68-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dbf68-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbf68-151">Объекты кодека</span><span class="sxs-lookup"><span data-stu-id="dbf68-151">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="dbf68-152">Реализация кодека</span><span class="sxs-lookup"><span data-stu-id="dbf68-152">Codec Implementation</span></span>](codecimplementation.md)
</dt> <dt>

[<span data-ttu-id="dbf68-153">Использование экранного видеокодека Windows Media видео 9</span><span class="sxs-lookup"><span data-stu-id="dbf68-153">Using the Windows Media Video 9 Screen Codec</span></span>](usingthewindowsmediavideo9screencodec.md)
</dt> <dt>

[<span data-ttu-id="dbf68-154">Кодировщик экрана Windows Media видео 9</span><span class="sxs-lookup"><span data-stu-id="dbf68-154">Windows Media Video 9 Screen Encoder</span></span>](windowsmediavideo9screenencoder.md)
</dt> </dl>

 

 

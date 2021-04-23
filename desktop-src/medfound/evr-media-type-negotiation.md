---
description: Согласование типа носителя Евр
ms.assetid: 3a12b80d-7aac-437d-b515-aab37c1e81b2
title: Согласование типа носителя Евр
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bb1f87a24db866c9e80b211b0385c12dcd6b594
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351455"
---
# <a name="evr-media-type-negotiation"></a><span data-ttu-id="fc4b3-103">Согласование типа носителя Евр</span><span class="sxs-lookup"><span data-stu-id="fc4b3-103">EVR Media Type Negotiation</span></span>

<span data-ttu-id="fc4b3-104">В этом разделе описывается проверка типов мультимедиа в расширенном обработчике видео (Евр).</span><span class="sxs-lookup"><span data-stu-id="fc4b3-104">This topic describes how the enhanced video renderer (EVR) validates media types.</span></span>

-   <span data-ttu-id="fc4b3-105">Для фильтра Евр DirectShow происходит согласование типов при подключении контактов фильтра.</span><span class="sxs-lookup"><span data-stu-id="fc4b3-105">For the DirectShow EVR filter, type negotiation occurs when the filter's pins are connected.</span></span>

-   <span data-ttu-id="fc4b3-106">Для приемника мультимедиа Евр типы носителей задаются через интерфейс [**имфмедиатипехандлер**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) в приемниках потоков.</span><span class="sxs-lookup"><span data-stu-id="fc4b3-106">For the EVR media sink, the media types are set through the [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) interface on the stream sinks.</span></span> <span data-ttu-id="fc4b3-107">Обычно загрузчик топологии согласовывает типы носителей, хотя приложение также может задавать типы мультимедиа напрямую.</span><span class="sxs-lookup"><span data-stu-id="fc4b3-107">Typically the topology loader negotiates the media types, although the application can also set the media types directly.</span></span>

<span data-ttu-id="fc4b3-108">Евр не сообщает о каких либо предпочтительных типах носителей.</span><span class="sxs-lookup"><span data-stu-id="fc4b3-108">The EVR does not report any preferred media types.</span></span> <span data-ttu-id="fc4b3-109">Клиент должен протестировать типы мультимедиа до тех пор, пока не найдет допустимый тип.</span><span class="sxs-lookup"><span data-stu-id="fc4b3-109">The client must test media types until it finds an acceptable type.</span></span> <span data-ttu-id="fc4b3-110">Тип носителя для потока ссылок должен быть задан, прежде чем типы можно будет задать для любого из подпотоков.</span><span class="sxs-lookup"><span data-stu-id="fc4b3-110">The media type for the reference stream must be set before the types can be set on any of the substreams.</span></span>

<span data-ttu-id="fc4b3-111">Для потока ссылок Евр микшер возвращает список совместимых форматов для визуализации видео DirectX (ДКСВА).</span><span class="sxs-lookup"><span data-stu-id="fc4b3-111">For the reference stream, the EVR mixer gets a list of compatible DirectX Video Acceleration (DXVA) render target formats.</span></span> <span data-ttu-id="fc4b3-112">В Евр Presenter этот список используется для выбора формата для цепочки подкачки Direct3D.</span><span class="sxs-lookup"><span data-stu-id="fc4b3-112">The EVR presenter uses this list to select the format for the Direct3D swap chain.</span></span> <span data-ttu-id="fc4b3-113">Если не удается найти совместимый формат целевого объекта прорисовки, ЕВР отклоняет тип носителя.</span><span class="sxs-lookup"><span data-stu-id="fc4b3-113">If no compatible render target format can be found, the EVR rejects the media type.</span></span>

<span data-ttu-id="fc4b3-114">Для вложенных потоков микшер Евр запрашивает, поддерживает ли устройство ДКСВА этот формат подпотока в сочетании с форматом целевого объекта прорисовки, выбранным для потока ссылок.</span><span class="sxs-lookup"><span data-stu-id="fc4b3-114">For the substreams, the EVR mixer queries whether the DXVA device supports that substream format in combination with the render target format that was selected for the reference stream.</span></span> <span data-ttu-id="fc4b3-115">В результате доступные форматы подпотока могут изменяться в зависимости от потока ссылок.</span><span class="sxs-lookup"><span data-stu-id="fc4b3-115">As a result, the available substream formats might change depending on the reference stream.</span></span>

<span data-ttu-id="fc4b3-116">Более подробно этот процесс приведен ниже.</span><span class="sxs-lookup"><span data-stu-id="fc4b3-116">Here is the process in more detail.</span></span> <span data-ttu-id="fc4b3-117">Эти сведения не важны для большинства приложений, но они могут оказаться полезными при написании пользовательского микшера или Presenter.</span><span class="sxs-lookup"><span data-stu-id="fc4b3-117">These details are not important for most applications, but might be helpful if you are writing a custom mixer or presenter.</span></span>

<span data-ttu-id="fc4b3-118">Для потока ссылок согласование происходит следующим образом.</span><span class="sxs-lookup"><span data-stu-id="fc4b3-118">For the reference stream, negotiation happens as follows:</span></span>

1.  <span data-ttu-id="fc4b3-119">Евр вызывает [**имфтрансформ:: сетинпуттипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) в микшере.</span><span class="sxs-lookup"><span data-stu-id="fc4b3-119">The EVR calls [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) on the mixer.</span></span>

2.  <span data-ttu-id="fc4b3-120">Микшер преобразует тип носителя в описание ДКСВА 2,0 с помощью структуры [**DXVA2 \_ видеодеск**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) .</span><span class="sxs-lookup"><span data-stu-id="fc4b3-120">The mixer converts the media type to a DXVA 2.0 description, using the [**DXVA2\_VideoDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) structure.</span></span>

3.  <span data-ttu-id="fc4b3-121">Микшер вызывает [**идиректксвидеопроцессорсервице:: жетвидеопроцессордевицегуидс**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids) , чтобы получить список идентификаторов GUID обработчика видео.</span><span class="sxs-lookup"><span data-stu-id="fc4b3-121">The mixer calls [**IDirectXVideoProcessorService::GetVideoProcessorDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids) to get a list of video processor GUIDs.</span></span>

4.  <span data-ttu-id="fc4b3-122">Для каждого идентификатора GUID обработчика видео микшер вызывает [**идиректксвидеопроцессорсервице:: жетвидеопроцессоррендертаржетс**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorrendertargets) , чтобы получить Поддерживаемые форматы целевого объекта прорисовки.</span><span class="sxs-lookup"><span data-stu-id="fc4b3-122">For each video processor GUID, the mixer calls [**IDirectXVideoProcessorService::GetVideoProcessorRenderTargets**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorrendertargets) to get the supported render target formats.</span></span>

5.  <span data-ttu-id="fc4b3-123">Евр вызывает [**имфвидеопресентер::P роцессмессаже**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) в выступающих с \_ сообщением мфвп Message \_ инвалидатемедиатипе.</span><span class="sxs-lookup"><span data-stu-id="fc4b3-123">The EVR calls [**IMFVideoPresenter::ProcessMessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) on the presenter with the MFVP\_MESSAGE\_INVALIDATEMEDIATYPE message.</span></span> <span data-ttu-id="fc4b3-124">Это сообщение приводит к тому, что в выступающем поле выбирается новый формат.</span><span class="sxs-lookup"><span data-stu-id="fc4b3-124">This message causes the presenter to select a new format.</span></span>

6.  <span data-ttu-id="fc4b3-125">Выступающий вызывает [**имфтрансформ:: жетаутпутаваилаблетипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) , чтобы получить список доступных выходных форматов из микшера.</span><span class="sxs-lookup"><span data-stu-id="fc4b3-125">The presenter calls [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) to get a list of available output formats from the mixer.</span></span> <span data-ttu-id="fc4b3-126">Микшер создает этот список из форматов, полученных на шаге 4.</span><span class="sxs-lookup"><span data-stu-id="fc4b3-126">The mixer generates this list from the formats obtained in step 4.</span></span>

7.  <span data-ttu-id="fc4b3-127">Выступающий выбирает формат и вызывает [**имфтрансформ:: сетаутпуттипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) в микшере.</span><span class="sxs-lookup"><span data-stu-id="fc4b3-127">The presenter selects a format and calls [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) on the mixer.</span></span>

<span data-ttu-id="fc4b3-128">Для подпотоков процесс является более простым:</span><span class="sxs-lookup"><span data-stu-id="fc4b3-128">For substreams, the process is simpler:</span></span>

1.  <span data-ttu-id="fc4b3-129">Евр вызывает [**имфтрансформ:: сетинпуттипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) в микшере.</span><span class="sxs-lookup"><span data-stu-id="fc4b3-129">The EVR calls [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) on the mixer.</span></span>

2.  <span data-ttu-id="fc4b3-130">Микшер вызывает [**идиректксвидеопроцессорсервице:: жетвидеопроцессорсубстреамформатс**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorsubstreamformats) , чтобы получить список доступных форматов подпотока.</span><span class="sxs-lookup"><span data-stu-id="fc4b3-130">The mixer calls [**IDirectXVideoProcessorService::GetVideoProcessorSubStreamFormats**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorsubstreamformats) to get a list of available substream formats.</span></span>

3.  <span data-ttu-id="fc4b3-131">Если в этом списке содержится предложенный формат, ЕВР принимает входной тип.</span><span class="sxs-lookup"><span data-stu-id="fc4b3-131">If the proposed format is contained in this list, the EVR accepts the input type.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fc4b3-132">См. также</span><span class="sxs-lookup"><span data-stu-id="fc4b3-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc4b3-133">Улучшенный модуль подготовки видео</span><span class="sxs-lookup"><span data-stu-id="fc4b3-133">Enhanced Video Renderer</span></span>](enhanced-video-renderer.md)
</dt> </dl>

 

 




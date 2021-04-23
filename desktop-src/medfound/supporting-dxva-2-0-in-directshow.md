---
description: В этом разделе описано, как поддерживать ускорение видео DirectX (ДКСВА) 2,0 в фильтре декодера DirectShow.
ms.assetid: 40deaddb-bb17-4a34-8294-5c7dc8a8a457
title: Поддержка ДКСВА 2,0 в DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dda956b60d4905c2392e1a50bd62ee8421b944b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898174"
---
# <a name="supporting-dxva-20-in-directshow"></a><span data-ttu-id="7b481-103">Поддержка ДКСВА 2,0 в DirectShow</span><span class="sxs-lookup"><span data-stu-id="7b481-103">Supporting DXVA 2.0 in DirectShow</span></span>

<span data-ttu-id="7b481-104">В этом разделе описано, как поддерживать ускорение видео DirectX (ДКСВА) 2,0 в фильтре декодера DirectShow.</span><span class="sxs-lookup"><span data-stu-id="7b481-104">This topic describes how to support DirectX Video Acceleration (DXVA) 2.0 in a DirectShow decoder filter.</span></span> <span data-ttu-id="7b481-105">В частности, он описывает взаимодействие между декодером и модулем подготовки видео.</span><span class="sxs-lookup"><span data-stu-id="7b481-105">Specifically, it describes the communication between the decoder and the video renderer.</span></span> <span data-ttu-id="7b481-106">В этом разделе не описывается, как реализовать декодирование ДКСВА.</span><span class="sxs-lookup"><span data-stu-id="7b481-106">This topic does not describe how to implement DXVA decoding.</span></span>

-   [<span data-ttu-id="7b481-107">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="7b481-107">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="7b481-108">Примечания по миграции</span><span class="sxs-lookup"><span data-stu-id="7b481-108">Migration Notes</span></span>](#migration-notes)
-   [<span data-ttu-id="7b481-109">Поиск конфигурации декодера</span><span class="sxs-lookup"><span data-stu-id="7b481-109">Finding a Decoder Configuration</span></span>](#finding-a-decoder-configuration)
-   [<span data-ttu-id="7b481-110">Уведомление модуля подготовки видео</span><span class="sxs-lookup"><span data-stu-id="7b481-110">Notifying the Video Renderer</span></span>](#notifying-the-video-renderer)
-   [<span data-ttu-id="7b481-111">Выделение несжатых буферов</span><span class="sxs-lookup"><span data-stu-id="7b481-111">Allocating Uncompressed Buffers</span></span>](#allocating-uncompressed-buffers)
-   [<span data-ttu-id="7b481-112">Декодирование</span><span class="sxs-lookup"><span data-stu-id="7b481-112">Decoding</span></span>](#decoding)
-   [<span data-ttu-id="7b481-113">См. также</span><span class="sxs-lookup"><span data-stu-id="7b481-113">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="7b481-114">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="7b481-114">Prerequisites</span></span>

<span data-ttu-id="7b481-115">В этом разделе предполагается, что вы знакомы с написанием фильтров DirectShow.</span><span class="sxs-lookup"><span data-stu-id="7b481-115">This topic assumes that you are familiar with writing DirectShow filters.</span></span> <span data-ttu-id="7b481-116">Дополнительные сведения см. в разделе [Создание фильтров DirectShow](../directshow/writing-directshow-filters.md) в документации по пакету SDK для DirectShow.</span><span class="sxs-lookup"><span data-stu-id="7b481-116">For more information, see the topic [Writing DirectShow Filters](../directshow/writing-directshow-filters.md) in the DirectShow SDK documentation.</span></span> <span data-ttu-id="7b481-117">В примерах кода в этом разделе предполагается, что фильтр декодера является производным от класса [**ктрансформфилтер**](../directshow/ctransformfilter.md) со следующим определением класса:</span><span class="sxs-lookup"><span data-stu-id="7b481-117">The code examples in this topic assume that the decoder filter is derived from the [**CTransformFilter**](../directshow/ctransformfilter.md) class, with the following class definition:</span></span>


```C++
class CDecoder : public CTransformFilter
{
public:
    static CUnknown* WINAPI CreateInstance(IUnknown *pUnk, HRESULT *pHr);

    HRESULT CompleteConnect(PIN_DIRECTION direction, IPin *pPin);

    HRESULT InitAllocator(IMemAllocator **ppAlloc);
    HRESULT DecideBufferSize(IMemAllocator *pAlloc, ALLOCATOR_PROPERTIES *pProp);

    // TODO: The implementations of these methods depend on the specific decoder.
    HRESULT CheckInputType(const CMediaType *mtIn);
    HRESULT CheckTransform(const CMediaType *mtIn, const CMediaType *mtOut);
    HRESULT CTransformFilter::GetMediaType(int,CMediaType *);

private:
    CDecoder(HRESULT *pHr);
    ~CDecoder();

    CBasePin * GetPin(int n);

    HRESULT ConfigureDXVA2(IPin *pPin);
    HRESULT SetEVRForDXVA2(IPin *pPin);

    HRESULT FindDecoderConfiguration(
        /* [in] */  IDirectXVideoDecoderService *pDecoderService,
        /* [in] */  const GUID& guidDecoder, 
        /* [out] */ DXVA2_ConfigPictureDecode *pSelectedConfig,
        /* [out] */ BOOL *pbFoundDXVA2Configuration
        );

private:
    IDirectXVideoDecoderService *m_pDecoderService;

    DXVA2_ConfigPictureDecode m_DecoderConfig;
    GUID                      m_DecoderGuid;
    HANDLE                    m_hDevice;

    FOURCC                    m_fccOutputFormat;
};
```



<span data-ttu-id="7b481-118">В оставшейся части этого раздела термин *декодера* относится к фильтру декодера, который получает сжатое видео и выводит несжатое видео.</span><span class="sxs-lookup"><span data-stu-id="7b481-118">In the remainder of this topic, the term *decoder* refers to the decoder filter, which receives compressed video and outputs uncompressed video.</span></span> <span data-ttu-id="7b481-119">Термин *устройство декодера* относится к аппаратному ускорителю, реализованному графическим драйвером.</span><span class="sxs-lookup"><span data-stu-id="7b481-119">The term *decoder device* refers to a hardware video accelerator implemented by the graphics driver.</span></span>

<span data-ttu-id="7b481-120">Ниже приведены основные шаги, которые должен выполнить фильтр декодера для поддержки ДКСВА 2,0:</span><span class="sxs-lookup"><span data-stu-id="7b481-120">Here are the basic steps that a decoder filter must perform to support DXVA 2.0:</span></span>

1.  <span data-ttu-id="7b481-121">Согласование типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="7b481-121">Negotiate a media type.</span></span>
2.  <span data-ttu-id="7b481-122">Найдите конфигурацию декодера ДКСВА.</span><span class="sxs-lookup"><span data-stu-id="7b481-122">Find a DXVA decoder configuration.</span></span>
3.  <span data-ttu-id="7b481-123">Уведомление модуля подготовки отчетов о том, что декодер использует декодирование ДКСВА.</span><span class="sxs-lookup"><span data-stu-id="7b481-123">Notify the video renderer that the decoder is using DXVA decoding.</span></span>
4.  <span data-ttu-id="7b481-124">Предоставьте пользовательский распределитель, который выделяет поверхности Direct3D.</span><span class="sxs-lookup"><span data-stu-id="7b481-124">Provide a custom allocator that allocates Direct3D surfaces.</span></span>

<span data-ttu-id="7b481-125">Эти действия более подробно описаны в оставшейся части этого раздела.</span><span class="sxs-lookup"><span data-stu-id="7b481-125">These steps are described in more detail in the remainder of this topic.</span></span>

## <a name="migration-notes"></a><span data-ttu-id="7b481-126">Примечания по миграции</span><span class="sxs-lookup"><span data-stu-id="7b481-126">Migration Notes</span></span>

<span data-ttu-id="7b481-127">При миграции с ДКСВА 1,0 необходимо учитывать некоторые существенные различия между двумя версиями:</span><span class="sxs-lookup"><span data-stu-id="7b481-127">If you are migrating from DXVA 1.0, you should be aware of some significant differences between the two versions:</span></span>

-   <span data-ttu-id="7b481-128">ДКСВА 2,0 не использует интерфейсы [**иамвидеоакцелератор**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) и [**иамвидеоакцелераторнотифи**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify) , так как декодер может обращаться к API дксва 2,0 напрямую через интерфейс [**идиректксвидеодекодер**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) .</span><span class="sxs-lookup"><span data-stu-id="7b481-128">DXVA 2.0 does not use the [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) and [**IAMVideoAcceleratorNotify**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify) interfaces, because the decoder can access the DXVA 2.0 APIs directly through the [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) interface.</span></span>
-   <span data-ttu-id="7b481-129">Во время согласования типа мультимедиа декодер не использует GUID ускорения видео в качестве подтипа.</span><span class="sxs-lookup"><span data-stu-id="7b481-129">During media type negotiation, the decoder does not use a video acceleration GUID as the subtype.</span></span> <span data-ttu-id="7b481-130">Вместо этого подтип является просто несжатым видеоформатом (например, NV12), как при декодировании программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="7b481-130">Instead, the subtype is just the uncompressed video format (such as NV12), as with software decoding.</span></span>
-   <span data-ttu-id="7b481-131">Процедура настройки сочетания клавиш была изменена.</span><span class="sxs-lookup"><span data-stu-id="7b481-131">The procedure for configuring the accelerator has changed.</span></span> <span data-ttu-id="7b481-132">В ДКСВА 1,0 декодер вызывает **EXECUTE** с помощью структуры **дксва \_ конфигпиктуредекоде** для настройки акцерлатор.</span><span class="sxs-lookup"><span data-stu-id="7b481-132">In DXVA 1.0, the decoder calls **Execute** with a **DXVA\_ConfigPictureDecode** structure to configure the accerlator.</span></span> <span data-ttu-id="7b481-133">В ДКСВА 2,0 декодер использует интерфейс [**идиректксвидеодекодерсервице**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) , как описано в следующем разделе.</span><span class="sxs-lookup"><span data-stu-id="7b481-133">In DXVA 2.0, the decoder uses the [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) interface, as described in the next section.</span></span>
-   <span data-ttu-id="7b481-134">Декодер выделяет несжатые буферы.</span><span class="sxs-lookup"><span data-stu-id="7b481-134">The decoder allocates the uncompressed buffers.</span></span> <span data-ttu-id="7b481-135">Модуль подготовки видео больше не выделяет их.</span><span class="sxs-lookup"><span data-stu-id="7b481-135">The video renderer no longer allocates them.</span></span>
-   <span data-ttu-id="7b481-136">Вместо вызова [**иамвидеоакцелератор::D исплайфраме**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-displayframe) для отображения декодированного кадра декодер доставляет кадр в модуль подготовки, вызывая [**Имеминпутпин:: Receive**](/windows/win32/api/strmif/nf-strmif-imeminputpin-receive), как и при декодировании программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="7b481-136">Instead of calling [**IAMVideoAccelerator::DisplayFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-displayframe) to display the decoded frame, the decoder delivers the frame to the renderer by calling [**IMemInputPin::Receive**](/windows/win32/api/strmif/nf-strmif-imeminputpin-receive), as with software decoding.</span></span>
-   <span data-ttu-id="7b481-137">Декодер больше не отвечает за проверку безопасности буферов данных для обновлений.</span><span class="sxs-lookup"><span data-stu-id="7b481-137">The decoder is no longer responsible for checking when data buffers are safe for updates.</span></span> <span data-ttu-id="7b481-138">Поэтому ДКСВА 2,0 не имеет метода, эквивалентного [**иамвидеоакцелератор:: куерирендерстатус**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-queryrenderstatus).</span><span class="sxs-lookup"><span data-stu-id="7b481-138">Therefore DXVA 2.0 does not have any method equivalent to [**IAMVideoAccelerator::QueryRenderStatus**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-queryrenderstatus).</span></span>
-   <span data-ttu-id="7b481-139">Наложение изображений выполняется модулем подготовки видео с помощью API процессора ДКСВА 2.0 Video.</span><span class="sxs-lookup"><span data-stu-id="7b481-139">Subpicture blending is done by the video renderer, using the DXVA2.0 video processor APIs.</span></span> <span data-ttu-id="7b481-140">Декодеры, которые предоставляют подизображения (например, декодеры DVD), должны отсылать данные субтитров на отдельный выходной ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="7b481-140">Decoders that provide subpictures (for example, DVD decoders) should send subpicture data on a separate output pin.</span></span>

<span data-ttu-id="7b481-141">Для операций декодирования ДКСВА 2,0 использует те же структуры данных, что и ДКСВА 1,0.</span><span class="sxs-lookup"><span data-stu-id="7b481-141">For decoding operations, DXVA 2.0 uses the same data structures as DXVA 1.0.</span></span>

<span data-ttu-id="7b481-142">Расширенный фильтр модуля подготовки видео (Евр) поддерживает ДКСВА 2,0.</span><span class="sxs-lookup"><span data-stu-id="7b481-142">The enhanced video renderer (EVR) filter supports DXVA 2.0.</span></span> <span data-ttu-id="7b481-143">Фильтры рендеринга для микширования видео (VMR-7 и VMR-9) поддерживают только ДКСВА 1,0.</span><span class="sxs-lookup"><span data-stu-id="7b481-143">The Video Mixing Renderer filters (VMR-7 and VMR-9) support DXVA 1.0 only.</span></span>

## <a name="finding-a-decoder-configuration"></a><span data-ttu-id="7b481-144">Поиск конфигурации декодера</span><span class="sxs-lookup"><span data-stu-id="7b481-144">Finding a Decoder Configuration</span></span>

<span data-ttu-id="7b481-145">После того как декодер согласовывает тип выходного носителя, он должен найти совместимую конфигурацию для устройства декодера ДКСВА.</span><span class="sxs-lookup"><span data-stu-id="7b481-145">After the decoder negotiates the output media type, it must find a compatible configuration for the DXVA decoder device.</span></span> <span data-ttu-id="7b481-146">Этот шаг можно выполнить в методе [**кбасеаутпутпин:: комплетеконнект**](../directshow/cbaseoutputpin-completeconnect.md) выходного контакта.</span><span class="sxs-lookup"><span data-stu-id="7b481-146">You can perform this step inside the output pin's [**CBaseOutputPin::CompleteConnect**](../directshow/cbaseoutputpin-completeconnect.md) method.</span></span> <span data-ttu-id="7b481-147">Этот шаг гарантирует, что графический драйвер поддерживает возможности, необходимые для работы декодера, прежде чем декодер зафиксируется с помощью ДКСВА.</span><span class="sxs-lookup"><span data-stu-id="7b481-147">This step ensures that the graphics driver supports the capabilities needed by the decoder, before the decoder commits to using DXVA.</span></span>

<span data-ttu-id="7b481-148">Чтобы найти конфигурацию для устройства декодера, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="7b481-148">To find a configuration for the decoder device, do the following:</span></span>

1.  <span data-ttu-id="7b481-149">Запросите входной ПИН-код модуля подготовки отчетов для интерфейса [**имфжетсервице**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) .</span><span class="sxs-lookup"><span data-stu-id="7b481-149">Query the renderer's input pin for the [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) interface.</span></span>
2.  <span data-ttu-id="7b481-150">Вызовите [**имфжетсервице::-Service**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) , чтобы получить указатель на интерфейс [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) .</span><span class="sxs-lookup"><span data-stu-id="7b481-150">Call [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) to get a pointer to the [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) interface.</span></span> <span data-ttu-id="7b481-151">Идентификатор GUID службы — это \_ Служба ускорения видео (MR) \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="7b481-151">The service GUID is MR\_VIDEO\_ACCELERATION\_SERVICE.</span></span>
3.  <span data-ttu-id="7b481-152">Вызовите [**IDirect3DDeviceManager9:: опендевицехандле**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) , чтобы получить маркер устройства Direct3D визуализатора.</span><span class="sxs-lookup"><span data-stu-id="7b481-152">Call [**IDirect3DDeviceManager9::OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) to get a handle to the renderer's Direct3D device.</span></span>
4.  <span data-ttu-id="7b481-153">Вызовите [**IDirect3DDeviceManager9:: жетвидеосервице**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice) и передайте в него маркер устройства.</span><span class="sxs-lookup"><span data-stu-id="7b481-153">Call [**IDirect3DDeviceManager9::GetVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice) and pass in the device handle.</span></span> <span data-ttu-id="7b481-154">Этот метод возвращает указатель на интерфейс [**идиректксвидеодекодерсервице**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) .</span><span class="sxs-lookup"><span data-stu-id="7b481-154">This method returns a pointer to the [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) interface.</span></span>
5.  <span data-ttu-id="7b481-155">Вызовите [**идиректксвидеодекодерсервице:: жетдекодердевицегуидс**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderdeviceguids).</span><span class="sxs-lookup"><span data-stu-id="7b481-155">Call [**IDirectXVideoDecoderService::GetDecoderDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderdeviceguids).</span></span> <span data-ttu-id="7b481-156">Этот метод возвращает массив идентификаторов GUID устройства декодера.</span><span class="sxs-lookup"><span data-stu-id="7b481-156">This method returns an array of decoder device GUIDs.</span></span>
6.  <span data-ttu-id="7b481-157">Пройдите по массиву идентификаторов GUID декодера, чтобы найти те, которые поддерживает фильтр декодера.</span><span class="sxs-lookup"><span data-stu-id="7b481-157">Loop through the array of decoder GUIDs to find the ones that the decoder filter supports.</span></span> <span data-ttu-id="7b481-158">Например, для декодера MPEG-2 необходимо найти **DXVA2 \_ ModeMPEG2 \_ мокомп**, **DXVA2 \_ ModeMPEG2 \_ идкт** или **DXVA2 \_ ModeMPEG2 \_ ВЛД**.</span><span class="sxs-lookup"><span data-stu-id="7b481-158">For example, for an MPEG-2 decoder, you would look for **DXVA2\_ModeMPEG2\_MOCOMP**, **DXVA2\_ModeMPEG2\_IDCT**, or **DXVA2\_ModeMPEG2\_VLD**.</span></span>

7.  <span data-ttu-id="7b481-159">При обнаружении идентификатора GUID устройства-кандидата передайте GUID в метод [**идиректксвидеодекодерсервице:: жетдекодеррендертаржетс**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderrendertargets) .</span><span class="sxs-lookup"><span data-stu-id="7b481-159">When you find a candidate decoder device GUID, pass the GUID to the [**IDirectXVideoDecoderService::GetDecoderRenderTargets**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderrendertargets) method.</span></span> <span data-ttu-id="7b481-160">Этот метод возвращает массив форматов целевого объекта прорисовки, указанных как значения **D3DFORMAT** .</span><span class="sxs-lookup"><span data-stu-id="7b481-160">This method returns an array of render target formats, specified as **D3DFORMAT** values.</span></span>
8.  <span data-ttu-id="7b481-161">Пройдите по форматам целевого объекта рендеринга и найдите тот, который соответствует выходному формату.</span><span class="sxs-lookup"><span data-stu-id="7b481-161">Loop through the render target formats and look for one that matches your output format.</span></span> <span data-ttu-id="7b481-162">Как правило, устройство декодера поддерживает один формат целевого объекта рендеринга.</span><span class="sxs-lookup"><span data-stu-id="7b481-162">Typically, a decoder device supports a single render target format.</span></span> <span data-ttu-id="7b481-163">Фильтр декодера должен подключаться к модулю подготовки отчетов с помощью этого подтипа.</span><span class="sxs-lookup"><span data-stu-id="7b481-163">The decoder filter should connect to the renderer using this subtype.</span></span> <span data-ttu-id="7b481-164">При первом вызове [**комплетеконнект**](../directshow/cbaseoutputpin-completeconnect.md)декодер может запрограммировать формат целевого объекта прорисовки, а затем вернуть этот формат в качестве предпочтительного выходного типа.</span><span class="sxs-lookup"><span data-stu-id="7b481-164">In the first call to [**CompleteConnect**](../directshow/cbaseoutputpin-completeconnect.md), the decoder can determing the render target format and then return this format as a preferred output type.</span></span>

9.  <span data-ttu-id="7b481-165">Вызовите [**идиректксвидеодекодерсервице:: жетдекодерконфигуратионс**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderconfigurations).</span><span class="sxs-lookup"><span data-stu-id="7b481-165">Call [**IDirectXVideoDecoderService::GetDecoderConfigurations**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderconfigurations).</span></span> <span data-ttu-id="7b481-166">Передайте тот же GUID устройства декодера, а также структуру [**DXVA2 \_ видеодеск**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) , описывающую предложенный формат.</span><span class="sxs-lookup"><span data-stu-id="7b481-166">Pass in the same decoder device GUID, along with a [**DXVA2\_VideoDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) structure that describes the proposed format.</span></span> <span data-ttu-id="7b481-167">Метод возвращает массив структур [**DXVA2 \_ конфигпиктуредекоде**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_configpicturedecode) .</span><span class="sxs-lookup"><span data-stu-id="7b481-167">The method returns an array of [**DXVA2\_ConfigPictureDecode**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_configpicturedecode) structures.</span></span> <span data-ttu-id="7b481-168">Каждая структура описывает одну возможную конфигурацию для устройства декодера.</span><span class="sxs-lookup"><span data-stu-id="7b481-168">Each structure describes one possible configuration for the decoder device.</span></span>

10. <span data-ttu-id="7b481-169">При условии, что предыдущие шаги выполнены успешно, сохраните маркер устройства Direct3D, GUID устройства декодера и структуру конфигурации.</span><span class="sxs-lookup"><span data-stu-id="7b481-169">Assuming that the previous steps are successful, store the Direct3D device handle, the decoder device GUID, and the configuration structure.</span></span> <span data-ttu-id="7b481-170">Этот фильтр будет использовать эти сведения для создания устройства декодера.</span><span class="sxs-lookup"><span data-stu-id="7b481-170">The filter will use this information to create the decoder device.</span></span>

<span data-ttu-id="7b481-171">В следующем коде показано, как найти конфигурацию декодера.</span><span class="sxs-lookup"><span data-stu-id="7b481-171">The following code shows how to find a decoder configuration.</span></span>


```C++
HRESULT CDecoder::ConfigureDXVA2(IPin *pPin)
{
    UINT    cDecoderGuids = 0;
    BOOL    bFoundDXVA2Configuration = FALSE;
    GUID    guidDecoder = GUID_NULL;

    DXVA2_ConfigPictureDecode config;
    ZeroMemory(&config, sizeof(config));

    // Variables that follow must be cleaned up at the end.

    IMFGetService               *pGetService = NULL;
    IDirect3DDeviceManager9     *pDeviceManager = NULL;
    IDirectXVideoDecoderService *pDecoderService = NULL;

    GUID   *pDecoderGuids = NULL; // size = cDecoderGuids
    HANDLE hDevice = INVALID_HANDLE_VALUE;

    // Query the pin for IMFGetService.
    HRESULT hr = pPin->QueryInterface(IID_PPV_ARGS(&pGetService));

    // Get the Direct3D device manager.
    if (SUCCEEDED(hr))
    {
        hr = pGetService->GetService(

            MR_VIDEO_ACCELERATION_SERVICE,
            IID_PPV_ARGS(&pDeviceManager)
            );
    }

    // Open a new device handle.
    if (SUCCEEDED(hr))
    {
        hr = pDeviceManager->OpenDeviceHandle(&hDevice);
    } 

    // Get the video decoder service.
    if (SUCCEEDED(hr))
    {
        hr = pDeviceManager->GetVideoService(
            hDevice, IID_PPV_ARGS(&pDecoderService));
    }

    // Get the decoder GUIDs.
    if (SUCCEEDED(hr))
    {
        hr = pDecoderService->GetDecoderDeviceGuids(
            &cDecoderGuids, &pDecoderGuids);
    }

    if (SUCCEEDED(hr))
    {
        // Look for the decoder GUIDs we want.
        for (UINT iGuid = 0; iGuid < cDecoderGuids; iGuid++)
        {
            // Do we support this mode?
            if (!IsSupportedDecoderMode(pDecoderGuids[iGuid]))
            {
                continue;
            }

            // Find a configuration that we support. 
            hr = FindDecoderConfiguration(pDecoderService, pDecoderGuids[iGuid],
                &config, &bFoundDXVA2Configuration);
            if (FAILED(hr))
            {
                break;
            }

            if (bFoundDXVA2Configuration)
            {
                // Found a good configuration. Save the GUID and exit the loop.
                guidDecoder = pDecoderGuids[iGuid];
                break;
            }
        }
    }

    if (!bFoundDXVA2Configuration)
    {
        hr = E_FAIL; // Unable to find a configuration.
    }

    if (SUCCEEDED(hr))
    {
        // Store the things we will need later.

        SafeRelease(&m_pDecoderService);
        m_pDecoderService = pDecoderService;
        m_pDecoderService->AddRef();

        m_DecoderConfig = config;
        m_DecoderGuid = guidDecoder;
        m_hDevice = hDevice;
    }

    if (FAILED(hr))
    {
        if (hDevice != INVALID_HANDLE_VALUE)
        {
            pDeviceManager->CloseDeviceHandle(hDevice);
        }
    }

    SafeRelease(&pGetService);
    SafeRelease(&pDeviceManager);
    SafeRelease(&pDecoderService);
    return hr;
}
HRESULT CDecoder::FindDecoderConfiguration(
    /* [in] */  IDirectXVideoDecoderService *pDecoderService,
    /* [in] */  const GUID& guidDecoder, 
    /* [out] */ DXVA2_ConfigPictureDecode *pSelectedConfig,
    /* [out] */ BOOL *pbFoundDXVA2Configuration
    )
{
    HRESULT hr = S_OK;
    UINT cFormats = 0;
    UINT cConfigurations = 0;

    D3DFORMAT                   *pFormats = NULL;     // size = cFormats
    DXVA2_ConfigPictureDecode   *pConfig = NULL;      // size = cConfigurations

    // Find the valid render target formats for this decoder GUID.
    hr = pDecoderService->GetDecoderRenderTargets(
        guidDecoder,
        &cFormats,
        &pFormats
        );

    if (SUCCEEDED(hr))
    {
        // Look for a format that matches our output format.
        for (UINT iFormat = 0; iFormat < cFormats;  iFormat++)
        {
            if (pFormats[iFormat] != (D3DFORMAT)m_fccOutputFormat)
            {
                continue;
            }

            // Fill in the video description. Set the width, height, format, 
            // and frame rate.
            DXVA2_VideoDesc videoDesc = {0};

            FillInVideoDescription(&videoDesc); // Private helper function.
            videoDesc.Format = pFormats[iFormat];

            // Get the available configurations.
            hr = pDecoderService->GetDecoderConfigurations(
                guidDecoder,
                &videoDesc,
                NULL, // Reserved.
                &cConfigurations,
                &pConfig
                );

            if (FAILED(hr))
            {
                break;
            }

            // Find a supported configuration.
            for (UINT iConfig = 0; iConfig < cConfigurations; iConfig++)
            {
                if (IsSupportedDecoderConfig(pConfig[iConfig]))
                {
                    // This configuration is good.
                    *pbFoundDXVA2Configuration = TRUE;
                    *pSelectedConfig = pConfig[iConfig];
                    break;
                }
            }

            CoTaskMemFree(pConfig);
            break;

        } // End of formats loop.
    }

    CoTaskMemFree(pFormats);

    // Note: It is possible to return S_OK without finding a configuration.
    return hr;
}
```



<span data-ttu-id="7b481-172">Поскольку этот пример является универсальным, часть логики была помещена в вспомогательные функции, которые необходимо реализовать с помощью декодера.</span><span class="sxs-lookup"><span data-stu-id="7b481-172">Because this example is generic, some of the logic has been placed in helper functions that would need to be implemented by the decoder.</span></span> <span data-ttu-id="7b481-173">В следующем коде показаны объявления для этих функций:</span><span class="sxs-lookup"><span data-stu-id="7b481-173">The following code shows the declarations for these functions:</span></span>


```C++
// Returns TRUE if the decoder supports a given decoding mode.
BOOL IsSupportedDecoderMode(const GUID& mode);

// Returns TRUE if the decoder supports a given decoding configuration.
BOOL IsSupportedDecoderConfig(const DXVA2_ConfigPictureDecode& config);

// Fills in a DXVA2_VideoDesc structure based on the input format.
void FillInVideoDescription(DXVA2_VideoDesc *pDesc);
```



## <a name="notifying-the-video-renderer"></a><span data-ttu-id="7b481-174">Уведомление модуля подготовки видео</span><span class="sxs-lookup"><span data-stu-id="7b481-174">Notifying the Video Renderer</span></span>

<span data-ttu-id="7b481-175">Если декодер находит конфигурацию декодера, следующий шаг заключается в уведомлении модуля подготовки отчетов о том, что декодер будет использовать аппаратное ускорение.</span><span class="sxs-lookup"><span data-stu-id="7b481-175">If the decoder finds a decoder configuration, the next step is to notify the video renderer that the decoder will use hardware acceleration.</span></span> <span data-ttu-id="7b481-176">Этот шаг можно выполнить в методе [**комплетеконнект**](../directshow/cbaseoutputpin-completeconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="7b481-176">You can perform this step inside the [**CompleteConnect**](../directshow/cbaseoutputpin-completeconnect.md) method.</span></span> <span data-ttu-id="7b481-177">Этот шаг должен быть выполнен до выбора распределителя, так как он влияет на выбор распределителя.</span><span class="sxs-lookup"><span data-stu-id="7b481-177">This step must occur before the allocator is selected, because it affects how the allocator is selected.</span></span>

1.  <span data-ttu-id="7b481-178">Запросите входной ПИН-код модуля подготовки отчетов для интерфейса [**имфжетсервице**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) .</span><span class="sxs-lookup"><span data-stu-id="7b481-178">Query the renderer's input pin for the [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) interface.</span></span>
2.  <span data-ttu-id="7b481-179">Вызовите [**имфжетсервице::-Service**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) , чтобы получить указатель на интерфейс [**идиректксвидеомемориконфигуратион**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration) .</span><span class="sxs-lookup"><span data-stu-id="7b481-179">Call [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) to get a pointer to the [**IDirectXVideoMemoryConfiguration**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration) interface.</span></span> <span data-ttu-id="7b481-180">Идентификатор GUID службы — **это \_ \_ \_ Служба ускорения видео (MR**).</span><span class="sxs-lookup"><span data-stu-id="7b481-180">The service GUID is **MR\_VIDEO\_ACCELERATION\_SERVICE**.</span></span>
3.  <span data-ttu-id="7b481-181">Вызовите метод [**идиректксвидеомемориконфигуратион:: жетаваилаблесурфацетипебиндекс**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideomemoryconfiguration-getavailablesurfacetypebyindex) в цикле, увеличивая переменную *двтипеиндекс* с нуля.</span><span class="sxs-lookup"><span data-stu-id="7b481-181">Call [**IDirectXVideoMemoryConfiguration::GetAvailableSurfaceTypeByIndex**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideomemoryconfiguration-getavailablesurfacetypebyindex) in a loop, incrementing the *dwTypeIndex* variable from zero.</span></span> <span data-ttu-id="7b481-182">Останавливаться, когда метод возвращает значение **DXVA2 \_ сурфацетипе \_ декодеррендертаржет** в параметре *пдвтипе* .</span><span class="sxs-lookup"><span data-stu-id="7b481-182">Stop when the method returns the value **DXVA2\_SurfaceType\_DecoderRenderTarget** in the *pdwType* parameter.</span></span> <span data-ttu-id="7b481-183">Этот шаг гарантирует, что модуль подготовки видео поддерживает декодирование с аппаратным ускорением.</span><span class="sxs-lookup"><span data-stu-id="7b481-183">This step ensures that the video renderer supports hardware-accelerated decoding.</span></span> <span data-ttu-id="7b481-184">Этот шаг всегда будет выполняться для фильтра Евр.</span><span class="sxs-lookup"><span data-stu-id="7b481-184">This step will always succeed for the EVR filter.</span></span>
4.  <span data-ttu-id="7b481-185">Если предыдущий шаг выполнен, вызовите [**идиректксвидеомемориконфигуратион:: сетсурфацетипе**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideomemoryconfiguration-setsurfacetype) со значением DXVA2 \_ сурфацетипе \_ декодеррендертаржет.</span><span class="sxs-lookup"><span data-stu-id="7b481-185">If the previous step succeeded, call [**IDirectXVideoMemoryConfiguration::SetSurfaceType**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideomemoryconfiguration-setsurfacetype) with the value DXVA2\_SurfaceType\_DecoderRenderTarget.</span></span> <span data-ttu-id="7b481-186">При вызове **сетсурфацетипе** с этим значением модуль подготовки видео переводится в режим дксва.</span><span class="sxs-lookup"><span data-stu-id="7b481-186">Calling **SetSurfaceType** with this value puts the video renderer into DXVA mode.</span></span> <span data-ttu-id="7b481-187">Если модуль подготовки видео находится в этом режиме, декодер должен предоставить собственный распределитель.</span><span class="sxs-lookup"><span data-stu-id="7b481-187">When the video renderer is in this mode, the decoder must provide its own allocator.</span></span>

<span data-ttu-id="7b481-188">В следующем коде показано, как уведомлять модуль подготовки видео.</span><span class="sxs-lookup"><span data-stu-id="7b481-188">The following code shows how to notify the video renderer.</span></span>


```C++
HRESULT CDecoder::SetEVRForDXVA2(IPin *pPin)
{
    HRESULT hr = S_OK;

    IMFGetService                       *pGetService = NULL;
    IDirectXVideoMemoryConfiguration    *pVideoConfig = NULL;

    // Query the pin for IMFGetService.
    hr = pPin->QueryInterface(__uuidof(IMFGetService), (void**)&pGetService);

    // Get the IDirectXVideoMemoryConfiguration interface.
    if (SUCCEEDED(hr))
    {
        hr = pGetService->GetService(
            MR_VIDEO_ACCELERATION_SERVICE, IID_PPV_ARGS(&pVideoConfig));
    }

    // Notify the EVR. 
    if (SUCCEEDED(hr))
    {
        DXVA2_SurfaceType surfaceType;

        for (DWORD iTypeIndex = 0; ; iTypeIndex++)
        {
            hr = pVideoConfig->GetAvailableSurfaceTypeByIndex(iTypeIndex, &surfaceType);
            
            if (FAILED(hr))
            {
                break;
            }

            if (surfaceType == DXVA2_SurfaceType_DecoderRenderTarget)
            {
                hr = pVideoConfig->SetSurfaceType(DXVA2_SurfaceType_DecoderRenderTarget);
                break;
            }
        }
    }

    SafeRelease(&pGetService);
    SafeRelease(&pVideoConfig);

    return hr;
}
```



<span data-ttu-id="7b481-189">Если декодер находит допустимую конфигурацию и успешно уведомляет модуль подготовки видео, декодер может использовать ДКСВА для декодирования.</span><span class="sxs-lookup"><span data-stu-id="7b481-189">If the decoder finds a valid configuration and successfully notifies the video renderer, the decoder can use DXVA for decoding.</span></span> <span data-ttu-id="7b481-190">Декодер должен реализовать пользовательский распределитель для своего выходного ПИН-кода, как описано в следующем разделе.</span><span class="sxs-lookup"><span data-stu-id="7b481-190">The decoder must implement a custom allocator for its output pin, as described in the next section.</span></span>

## <a name="allocating-uncompressed-buffers"></a><span data-ttu-id="7b481-191">Выделение несжатых буферов</span><span class="sxs-lookup"><span data-stu-id="7b481-191">Allocating Uncompressed Buffers</span></span>

<span data-ttu-id="7b481-192">В ДКСВА 2,0 декодер отвечает за выделение поверхностей Direct3D для использования в качестве несжатых буферов видео.</span><span class="sxs-lookup"><span data-stu-id="7b481-192">In DXVA 2.0, the decoder is responsible for allocating Direct3D surfaces to use as uncompressed video buffers.</span></span> <span data-ttu-id="7b481-193">Поэтому декодер должен реализовать пользовательский распределитель, который будет создавать поверхности.</span><span class="sxs-lookup"><span data-stu-id="7b481-193">Therefore, the decoder must implement a custom allocator that will create the surfaces.</span></span> <span data-ttu-id="7b481-194">Примеры носителей, предоставляемые этим распределителем, будут содержать указатели на поверхности Direct3D.</span><span class="sxs-lookup"><span data-stu-id="7b481-194">The media samples provided by this allocator will hold pointers to the Direct3D surfaces.</span></span> <span data-ttu-id="7b481-195">Евр получает указатель на поверхность, вызывая [**имфжетсервице::-Service**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) на примере носителя.</span><span class="sxs-lookup"><span data-stu-id="7b481-195">The EVR retrieves a pointer to the surface by calling [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) on the media sample.</span></span> <span data-ttu-id="7b481-196">Идентификатор службы — это **\_ \_ Служба буфера MR**.</span><span class="sxs-lookup"><span data-stu-id="7b481-196">The service identifier is **MR\_BUFFER\_SERVICE**.</span></span>

<span data-ttu-id="7b481-197">Чтобы предоставить пользовательский распределитель, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="7b481-197">To provide the custom allocator, perform the following steps:</span></span>

1.  <span data-ttu-id="7b481-198">Определите класс для образцов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="7b481-198">Define a class for the media samples.</span></span> <span data-ttu-id="7b481-199">Этот класс может быть производным от класса [**кмедиасампле**](../directshow/cmediasample.md) .</span><span class="sxs-lookup"><span data-stu-id="7b481-199">This class can derive from the [**CMediaSample**](../directshow/cmediasample.md) class.</span></span> <span data-ttu-id="7b481-200">Внутри этого класса выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="7b481-200">Inside this class, do the following:</span></span>
    -   <span data-ttu-id="7b481-201">Сохранить указатель на поверхность Direct3D.</span><span class="sxs-lookup"><span data-stu-id="7b481-201">Store a pointer to the Direct3D surface.</span></span>
    -   <span data-ttu-id="7b481-202">Реализуйте интерфейс [**имфжетсервице**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) .</span><span class="sxs-lookup"><span data-stu-id="7b481-202">Implement the [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) interface.</span></span> <span data-ttu-id="7b481-203">В методе [**службы**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) , если идентификатор GUID службы — это **\_ \_ Служба буфера MR**, запросите область Direct3D для запрошенного интерфейса.</span><span class="sxs-lookup"><span data-stu-id="7b481-203">In the [**GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) method, if the service GUID is **MR\_BUFFER\_SERVICE**, query the Direct3D surface for the requested interface.</span></span> <span data-ttu-id="7b481-204">В противном случае служба " **услуга** " может вернуть **\_ \_ неподдерживаемую \_ службу MF E**.</span><span class="sxs-lookup"><span data-stu-id="7b481-204">Otherwise, **GetService** can return **MF\_E\_UNSUPPORTED\_SERVICE**.</span></span>
    -   <span data-ttu-id="7b481-205">Переопределите метод [**кмедиасампле::**](../directshow/cmediasample-getpointer.md) noreturn, возвращающий E \_ нотимпл.</span><span class="sxs-lookup"><span data-stu-id="7b481-205">Override the [**CMediaSample::GetPointer**](../directshow/cmediasample-getpointer.md) method to return E\_NOTIMPL.</span></span>
2.  <span data-ttu-id="7b481-206">Определите класс для распределителя.</span><span class="sxs-lookup"><span data-stu-id="7b481-206">Define a class for the allocator.</span></span> <span data-ttu-id="7b481-207">Распределитель может быть производным от класса [**кбасеаллокатор**](../directshow/cbaseallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="7b481-207">The allocator can derive from the [**CBaseAllocator**](../directshow/cbaseallocator.md) class.</span></span> <span data-ttu-id="7b481-208">Внутри этого класса выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="7b481-208">Inside this class, do the following.</span></span>
    -   <span data-ttu-id="7b481-209">Переопределите метод [**кбасеаллокатор:: Alloc**](../directshow/cbaseallocator-alloc.md) .</span><span class="sxs-lookup"><span data-stu-id="7b481-209">Override the [**CBaseAllocator::Alloc**](../directshow/cbaseallocator-alloc.md) method.</span></span> <span data-ttu-id="7b481-210">Внутри этого метода вызовите [**идиректксвидеоакцелератионсервице:: креатесурфаце**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface) , чтобы создать поверхности.</span><span class="sxs-lookup"><span data-stu-id="7b481-210">Inside this method, call [**IDirectXVideoAccelerationService::CreateSurface**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface) to create the surfaces.</span></span> <span data-ttu-id="7b481-211">(Интерфейс [**идиректксвидеодекодерсервице**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) наследует этот метод от [**идиректксвидеоакцелератионсервице**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoaccelerationservice).)</span><span class="sxs-lookup"><span data-stu-id="7b481-211">(The [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) interface inherits this method from [**IDirectXVideoAccelerationService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoaccelerationservice).)</span></span>
    -   <span data-ttu-id="7b481-212">Переопределите метод [**кбасеаллокатор:: Free**](../directshow/cbaseallocator-free.md) , чтобы освободить поверхности.</span><span class="sxs-lookup"><span data-stu-id="7b481-212">Override the [**CBaseAllocator::Free**](../directshow/cbaseallocator-free.md) method to release the surfaces.</span></span>
3.  <span data-ttu-id="7b481-213">В закреплениях вывода фильтра Переопределите метод [**кбасеаутпутпин:: иниталлокатор**](../directshow/cbaseoutputpin-initallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="7b481-213">In your filter's output pin, override the [**CBaseOutputPin::InitAllocator**](../directshow/cbaseoutputpin-initallocator.md) method.</span></span> <span data-ttu-id="7b481-214">Внутри этого метода создайте экземпляр пользовательского распределителя.</span><span class="sxs-lookup"><span data-stu-id="7b481-214">Inside this method, create an instance of your custom allocator.</span></span>
4.  <span data-ttu-id="7b481-215">В фильтре реализуйте метод [**ктрансформфилтер::D еЦидебуфферсизе**](../directshow/ctransformfilter-decidebuffersize.md) .</span><span class="sxs-lookup"><span data-stu-id="7b481-215">In your filter, implement the [**CTransformFilter::DecideBufferSize**](../directshow/ctransformfilter-decidebuffersize.md) method.</span></span> <span data-ttu-id="7b481-216">Параметр *pProperties* указывает количество поверхностей, требуемое для Евр.</span><span class="sxs-lookup"><span data-stu-id="7b481-216">The *pProperties* parameter indicates the number of surfaces that the EVR requires.</span></span> <span data-ttu-id="7b481-217">Добавьте к этому значению число поверхностей, которое требуется вашему декодеру, и вызовите [**имемаллокатор:: SetProperties**](/windows/win32/api/strmif/nf-strmif-imemallocator-setproperties) на распределителье.</span><span class="sxs-lookup"><span data-stu-id="7b481-217">Add to this value the number of surfaces that your decoder requires, and call [**IMemAllocator::SetProperties**](/windows/win32/api/strmif/nf-strmif-imemallocator-setproperties) on the allocator.</span></span>

<span data-ttu-id="7b481-218">В следующем коде показано, как реализовать пример класса мультимедиа:</span><span class="sxs-lookup"><span data-stu-id="7b481-218">The following code shows how to implement the media sample class:</span></span>


```C++
class CDecoderSample : public CMediaSample, public IMFGetService
{
    friend class CDecoderAllocator;

public:

    CDecoderSample(CDecoderAllocator *pAlloc, HRESULT *phr)
        : CMediaSample(NAME("DecoderSample"), (CBaseAllocator*)pAlloc, phr, NULL, 0),
          m_pSurface(NULL),
          m_dwSurfaceId(0)
    { 
    }

    // Note: CMediaSample does not derive from CUnknown, so we cannot use the
    //       DECLARE_IUNKNOWN macro that is used by most of the filter classes.

    STDMETHODIMP QueryInterface(REFIID riid, void **ppv)
    {
        CheckPointer(ppv, E_POINTER);

        if (riid == IID_IMFGetService)
        {
            *ppv = static_cast<IMFGetService*>(this);
            AddRef();
            return S_OK;
        }
        else
        {
            return CMediaSample::QueryInterface(riid, ppv);
        }
    }
    STDMETHODIMP_(ULONG) AddRef()
    {
        return CMediaSample::AddRef();
    }

    STDMETHODIMP_(ULONG) Release()
    {
        // Return a temporary variable for thread safety.
        ULONG cRef = CMediaSample::Release();
        return cRef;
    }

    // IMFGetService::GetService
    STDMETHODIMP GetService(REFGUID guidService, REFIID riid, LPVOID *ppv)
    {
        if (guidService != MR_BUFFER_SERVICE)
        {
            return MF_E_UNSUPPORTED_SERVICE;
        }
        else if (m_pSurface == NULL)
        {
            return E_NOINTERFACE;
        }
        else
        {
            return m_pSurface->QueryInterface(riid, ppv);
        }
    }

    // Override GetPointer because this class does not manage a system memory buffer.
    // The EVR uses the MR_BUFFER_SERVICE service to get the Direct3D surface.
    STDMETHODIMP GetPointer(BYTE ** ppBuffer)
    {
        return E_NOTIMPL;
    }

private:

    // Sets the pointer to the Direct3D surface. 
    void SetSurface(DWORD surfaceId, IDirect3DSurface9 *pSurf)
    {
        SafeRelease(&m_pSurface);

        m_pSurface = pSurf;
        if (m_pSurface)
        {
            m_pSurface->AddRef();
        }

        m_dwSurfaceId = surfaceId;
    }

    IDirect3DSurface9   *m_pSurface;
    DWORD               m_dwSurfaceId;
};
```



<span data-ttu-id="7b481-219">В следующем коде показано, как реализовать метод [**Alloc**](../directshow/cbaseallocator-alloc.md) для распределителя.</span><span class="sxs-lookup"><span data-stu-id="7b481-219">The following code shows how to implement the [**Alloc**](../directshow/cbaseallocator-alloc.md) method on the allocator.</span></span>


```C++
HRESULT CDecoderAllocator::Alloc()
{
    CAutoLock lock(this);

    HRESULT hr = S_OK;

    if (m_pDXVA2Service == NULL)
    {
        return E_UNEXPECTED;
    }

    hr = CBaseAllocator::Alloc();

    // If the requirements have not changed, do not reallocate.
    if (hr == S_FALSE)
    {
        return S_OK;
    }

    if (SUCCEEDED(hr))
    {
        // Free the old resources.
        Free();

        // Allocate a new array of pointers.
        m_ppRTSurfaceArray = new (std::nothrow) IDirect3DSurface9*[m_lCount];
        if (m_ppRTSurfaceArray == NULL)
        {
            hr = E_OUTOFMEMORY;
        }
        else
        {
            ZeroMemory(m_ppRTSurfaceArray, sizeof(IDirect3DSurface9*) * m_lCount);
        }
    }

    // Allocate the surfaces.
    if (SUCCEEDED(hr))
    {
        hr = m_pDXVA2Service->CreateSurface(
            m_dwWidth,
            m_dwHeight,
            m_lCount - 1,
            (D3DFORMAT)m_dwFormat,
            D3DPOOL_DEFAULT,
            0,
            DXVA2_VideoDecoderRenderTarget,
            m_ppRTSurfaceArray,
            NULL
            );
    }

    if (SUCCEEDED(hr))
    {
        for (m_lAllocated = 0; m_lAllocated < m_lCount; m_lAllocated++)
        {
            CDecoderSample *pSample = new (std::nothrow) CDecoderSample(this, &hr);

            if (pSample == NULL)
            {
                hr = E_OUTOFMEMORY;
                break;
            }
            if (FAILED(hr))
            {
                break;
            }
            // Assign the Direct3D surface pointer and the index.
            pSample->SetSurface(m_lAllocated, m_ppRTSurfaceArray[m_lAllocated]);

            // Add to the sample list.
            m_lFree.Add(pSample);
        }
    }

    if (SUCCEEDED(hr))
    {
        m_bChanged = FALSE;
    }
    return hr;
}
```



<span data-ttu-id="7b481-220">Ниже приведен код для метода [**Free**](../directshow/cbaseallocator-free.md) :</span><span class="sxs-lookup"><span data-stu-id="7b481-220">Here is the code for the [**Free**](../directshow/cbaseallocator-free.md) method:</span></span>


```C++
void CDecoderAllocator::Free()
{
    CMediaSample *pSample = NULL;

    do
    {
        pSample = m_lFree.RemoveHead();
        if (pSample)
        {
            delete pSample;
        }
    } while (pSample);

    if (m_ppRTSurfaceArray)
    {
        for (long i = 0; i < m_lAllocated; i++)
        {
            SafeRelease(&m_ppRTSurfaceArray[i]);
        }

        delete [] m_ppRTSurfaceArray;
    }
    m_lAllocated = 0;
}
```



<span data-ttu-id="7b481-221">Дополнительные сведения о реализации пользовательских распределительов см. в разделе, посвященном [пользовательскому распределительу](../directshow/providing-a-custom-allocator.md) документации по пакету SDK для DirectShow.</span><span class="sxs-lookup"><span data-stu-id="7b481-221">For more information about implementing custom allocators, see the topic [Providing a Custom Allocator](../directshow/providing-a-custom-allocator.md) in the DirectShow SDK documentation.</span></span>

## <a name="decoding"></a><span data-ttu-id="7b481-222">Декодирование</span><span class="sxs-lookup"><span data-stu-id="7b481-222">Decoding</span></span>

<span data-ttu-id="7b481-223">Чтобы создать устройство декодера, вызовите метод [**идиректксвидеодекодерсервице:: креатевидеодекодер**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-createvideodecoder).</span><span class="sxs-lookup"><span data-stu-id="7b481-223">To create the decoder device, call [**IDirectXVideoDecoderService::CreateVideoDecoder**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-createvideodecoder).</span></span> <span data-ttu-id="7b481-224">Метод возвращает указатель на интерфейс [**идиректксвидеодекодер**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) устройства декодера.</span><span class="sxs-lookup"><span data-stu-id="7b481-224">The method returns a pointer to the [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) interface of the decoder device.</span></span>

<span data-ttu-id="7b481-225">Для проверки маркера устройства в каждом кадре вызовите [**IDirect3DDeviceManager9:: тестдевице**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-testdevice) .</span><span class="sxs-lookup"><span data-stu-id="7b481-225">On each frame, call [**IDirect3DDeviceManager9::TestDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-testdevice) to test the device handle.</span></span> <span data-ttu-id="7b481-226">Если устройство изменилось, метод возвращает DXVA2 \_ E \_ новое \_ видео \_ устройство.</span><span class="sxs-lookup"><span data-stu-id="7b481-226">If the device has changed, the method returns DXVA2\_E\_NEW\_VIDEO\_DEVICE.</span></span> <span data-ttu-id="7b481-227">Если это происходит, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="7b481-227">If this occurs, do the following:</span></span>

1.  <span data-ttu-id="7b481-228">Закройте обработчик устройства, вызвав [**IDirect3DDeviceManager9:: клоседевицехандле**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-closedevicehandle).</span><span class="sxs-lookup"><span data-stu-id="7b481-228">Close the device handle by calling [**IDirect3DDeviceManager9::CloseDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-closedevicehandle).</span></span>
2.  <span data-ttu-id="7b481-229">Освободите указатели [**идиректксвидеодекодерсервице**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) и [**идиректксвидеодекодер**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) .</span><span class="sxs-lookup"><span data-stu-id="7b481-229">Release the [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) and [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) pointers.</span></span>
3.  <span data-ttu-id="7b481-230">Откройте новый маркер устройства.</span><span class="sxs-lookup"><span data-stu-id="7b481-230">Open a new device handle.</span></span>
4.  <span data-ttu-id="7b481-231">Согласование новой конфигурации декодера, как описано в разделе [Поиск конфигурации декодера](#finding-a-decoder-configuration).</span><span class="sxs-lookup"><span data-stu-id="7b481-231">Negotiate a new decoder configuration, as described in the section [Finding a Decoder Configuration](#finding-a-decoder-configuration).</span></span>
5.  <span data-ttu-id="7b481-232">Создайте новое устройство декодера.</span><span class="sxs-lookup"><span data-stu-id="7b481-232">Create a new decoder device.</span></span>

<span data-ttu-id="7b481-233">Предполагая, что маркер устройства является допустимым, процесс декодирования работает следующим образом:</span><span class="sxs-lookup"><span data-stu-id="7b481-233">Assuming that the device handle is valid, the decoding process works as follows:</span></span>

1.  <span data-ttu-id="7b481-234">Вызовите [**идиректксвидеодекодер:: бегинфраме**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe).</span><span class="sxs-lookup"><span data-stu-id="7b481-234">Call [**IDirectXVideoDecoder::BeginFrame**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe).</span></span>
2.  <span data-ttu-id="7b481-235">Сделайте следующее или несколько раз:</span><span class="sxs-lookup"><span data-stu-id="7b481-235">Do the following one or more times:</span></span>
    1.  <span data-ttu-id="7b481-236">Вызовите [**идиректксвидеодекодер::-buffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer) , чтобы получить буфер декодера дксва.</span><span class="sxs-lookup"><span data-stu-id="7b481-236">Call [**IDirectXVideoDecoder::GetBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer) to get a DXVA decoder buffer.</span></span>
    2.  <span data-ttu-id="7b481-237">Заполните буфер.</span><span class="sxs-lookup"><span data-stu-id="7b481-237">Fill the buffer.</span></span>
    3.  <span data-ttu-id="7b481-238">Вызовите [**идиректксвидеодекодер:: релеасебуффер**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-releasebuffer).</span><span class="sxs-lookup"><span data-stu-id="7b481-238">Call [**IDirectXVideoDecoder::ReleaseBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-releasebuffer).</span></span>
3.  <span data-ttu-id="7b481-239">Вызовите метод [**идиректксвидеодекодер:: Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) , чтобы выполнить операции декодирования в кадре.</span><span class="sxs-lookup"><span data-stu-id="7b481-239">Call [**IDirectXVideoDecoder::Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) to perform the decoding operations on the frame.</span></span>

<span data-ttu-id="7b481-240">ДКСВА 2,0 использует те же структуры данных, что и ДКСВА 1,0, для операций декодирования.</span><span class="sxs-lookup"><span data-stu-id="7b481-240">DXVA 2.0 uses the same data structures as DXVA 1.0 for decoding operations.</span></span> <span data-ttu-id="7b481-241">Для исходного набора профилей ДКСВА (для H. 261, H. 263 и MPEG-2) эти структуры данных описаны в [спецификации дксва 1,0](/windows-hardware/drivers/display/directx-video-acceleration).</span><span class="sxs-lookup"><span data-stu-id="7b481-241">For the original set of DXVA profiles (for H.261, H.263, and MPEG-2), these data structures are described in the [DXVA 1.0 specification](/windows-hardware/drivers/display/directx-video-acceleration).</span></span>

<span data-ttu-id="7b481-242">В каждой паре вызовов [](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe) / [**выполнения**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) бегинфраме можно вызвать метод несколько [](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer) раз, но только один раз для каждого типа буфера дксва.</span><span class="sxs-lookup"><span data-stu-id="7b481-242">Within each pair of [**BeginFrame**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe)/[**Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) calls, you may call [**GetBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer) multiple times, but only once for each type of DXVA buffer.</span></span> <span data-ttu-id="7b481-243">Если вызвать его дважды с тем же типом буфера, данные будут перезаписаны.</span><span class="sxs-lookup"><span data-stu-id="7b481-243">If you call it twice with the same buffer type, you will overwrite the data.</span></span>

<span data-ttu-id="7b481-244">После вызова [**EXECUTE**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute)вызовите [**Имеминпутпин:: Receive**](/windows/win32/api/strmif/nf-strmif-imeminputpin-receive) , чтобы передать кадр в модуль подготовки видео, как при декодировании программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="7b481-244">After calling [**Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute), call [**IMemInputPin::Receive**](/windows/win32/api/strmif/nf-strmif-imeminputpin-receive) to deliver the frame to the video renderer, as with software decoding.</span></span> <span data-ttu-id="7b481-245">Метод **Receive** является асинхронным; После возврата декодер может продолжить декодирование следующего кадра.</span><span class="sxs-lookup"><span data-stu-id="7b481-245">The **Receive** method is asynchronous; after it returns, the decoder can continue decoding the next frame.</span></span> <span data-ttu-id="7b481-246">Драйвер дисплея предотвращает перезапись буфера во время использования буфера всеми командами декодирования.</span><span class="sxs-lookup"><span data-stu-id="7b481-246">The display driver prevents any decoding commands from overwriting the buffer while the buffer is in use.</span></span> <span data-ttu-id="7b481-247">Декодер не должен повторно использовать поверхность для декодирования другого кадра, пока модуль подготовки отчетов не выпустит пример.</span><span class="sxs-lookup"><span data-stu-id="7b481-247">The decoder should not reuse a surface to decode another frame until the renderer has released the sample.</span></span> <span data-ttu-id="7b481-248">Когда модуль подготовки отчетов освобождает пример, распределитель помещает пример обратно в пул доступных образцов.</span><span class="sxs-lookup"><span data-stu-id="7b481-248">When the renderer releases the sample, the allocator puts the sample back into its pool of available samples.</span></span> <span data-ttu-id="7b481-249">Чтобы получить следующий доступный пример, вызовите метод [**кбасеаутпутпин:: жетделиверибуффер**](../directshow/cbaseoutputpin-getdeliverybuffer.md), который, в свою очередь, вызывает [**имемаллокатор::**](/windows/win32/api/strmif/nf-strmif-imemallocator-getbuffer)GetNext.</span><span class="sxs-lookup"><span data-stu-id="7b481-249">To get the next available sample, call [**CBaseOutputPin::GetDeliveryBuffer**](../directshow/cbaseoutputpin-getdeliverybuffer.md), which in turn calls [**IMemAllocator::GetBuffer**](/windows/win32/api/strmif/nf-strmif-imemallocator-getbuffer).</span></span> <span data-ttu-id="7b481-250">Дополнительные сведения см. в разделе Общие сведения о [потоке данных в DirectShow](../directshow/overview-of-data-flow-in-directshow.md) в документации по DirectShow.</span><span class="sxs-lookup"><span data-stu-id="7b481-250">For more information, see the topic [Overview of Data Flow in DirectShow](../directshow/overview-of-data-flow-in-directshow.md) in the DirectShow documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7b481-251">См. также</span><span class="sxs-lookup"><span data-stu-id="7b481-251">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b481-252">Ускорение видео DirectX 2,0</span><span class="sxs-lookup"><span data-stu-id="7b481-252">DirectX Video Acceleration 2.0</span></span>](directx-video-acceleration-2-0.md)
</dt> </dl>

 

 

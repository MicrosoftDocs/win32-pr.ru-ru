---
description: Куерякцепт (вышестоящий)
ms.assetid: 3153e3a4-2227-4fdd-b2b0-218763013d2d
title: Куерякцепт (вышестоящий)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7707c52d36c3d065c4a7277939f724aabdb73e46
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806472"
---
# <a name="queryaccept-upstream"></a><span data-ttu-id="3b451-103">Куерякцепт (вышестоящий)</span><span class="sxs-lookup"><span data-stu-id="3b451-103">QueryAccept (Upstream)</span></span>

<span data-ttu-id="3b451-104">Этот механизм позволяет закреплять входные данные для предложения изменения формата вышестоящего однорангового узла.</span><span class="sxs-lookup"><span data-stu-id="3b451-104">This mechanism enables an input pin to propose a format change to its upstream peer.</span></span> <span data-ttu-id="3b451-105">Нисходящий фильтр должен присоединить к образцу тип мультимедиа, который будет получать вышестоящий фильтр при следующем вызове [**имемаллокатор::-buffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer).</span><span class="sxs-lookup"><span data-stu-id="3b451-105">The downstream filter must attach a media type to the sample that the upstream filter will obtain in its next call to [**IMemAllocator::GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer).</span></span> <span data-ttu-id="3b451-106">Для этого, однако, нисходящий фильтр должен предоставить пользовательский распределитель для соединения.</span><span class="sxs-lookup"><span data-stu-id="3b451-106">In order to do this, however, the downstream filter must provide a custom allocator for the connection.</span></span> <span data-ttu-id="3b451-107">Этот распределитель должен реализовать частный метод, который нисходящий фильтр может использовать для задания типа мультимедиа в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="3b451-107">This allocator must implement a private method that the downstream filter can use to set the media type on the next sample.</span></span>

<span data-ttu-id="3b451-108">Выполняются следующие действия.</span><span class="sxs-lookup"><span data-stu-id="3b451-108">The following steps occur:</span></span>

1.  <span data-ttu-id="3b451-109">Нисходящий фильтр проверяет, использует ли соединение с закреплением пользовательский распределитель.</span><span class="sxs-lookup"><span data-stu-id="3b451-109">The downstream filter checks whether the pin connection uses the filter's custom allocator.</span></span> <span data-ttu-id="3b451-110">Если вышестоящий фильтр владеет распределителем, нисходящий фильтр не может изменить его формат.</span><span class="sxs-lookup"><span data-stu-id="3b451-110">If the upstream filter owns the allocator, the downstream filter cannot change the format.</span></span>
2.  <span data-ttu-id="3b451-111">Нисходящий фильтр вызывает [**Ипин:: куерякцепт**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) в качестве ПИН-кода вышестоящего вывода (см. иллюстрацию, шаг а).</span><span class="sxs-lookup"><span data-stu-id="3b451-111">The downstream filter calls [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) on the upstream output pin (see illustration, step A).</span></span>
3.  <span data-ttu-id="3b451-112">Если `QueryAccept` возвращается значение S \_ , нисходящий фильтр вызывает закрытый метод для своего распределителя, чтобы задать тип мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="3b451-112">If `QueryAccept` returns S\_OK, the downstream filter calls the private method on its allocator in order to set the media type.</span></span> <span data-ttu-id="3b451-113">В этом частном методе распределитель вызывает [**имедиасампле:: сетмедиатипе**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatype) в следующем доступном примере (B).</span><span class="sxs-lookup"><span data-stu-id="3b451-113">Within this private method, the allocator calls [**IMediaSample::SetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatype) on the next available sample (B).</span></span>
4.  <span data-ttu-id="3b451-114">Вышестоящий фильтр вызывает метод **buffer** для получения нового образца (C) и [**Имедиасампле:: жетмедиатипе**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) для получения типа мультимедиа (D).</span><span class="sxs-lookup"><span data-stu-id="3b451-114">The upstream filter calls **GetBuffer** to get a new sample (C) and [**IMediaSample::GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) to get the media type (D).</span></span>
5.  <span data-ttu-id="3b451-115">Когда вышестоящий фильтр доставляет пример, он должен оставить тип носителя, присоединенный к этому примеру.</span><span class="sxs-lookup"><span data-stu-id="3b451-115">When the upstream filter delivers the sample, it should leave the media type attached to that sample.</span></span> <span data-ttu-id="3b451-116">Таким образом, нисходящий фильтр может подтвердить, что тип мультимедиа изменился (E).</span><span class="sxs-lookup"><span data-stu-id="3b451-116">That way, the downstream filter can confirm that the media type has changed (E).</span></span>

<span data-ttu-id="3b451-117">Если вышестоящий фильтр принимает изменение формата, он также должен иметь возможность вернуться к исходному типу носителя, как показано на следующей схеме.</span><span class="sxs-lookup"><span data-stu-id="3b451-117">If the upstream filter accepts the format change, it must also be able to switch back to the original media type, as shown in the following diagram.</span></span>

![куерякцепт (вышестоящий)](images/dynformat4.png)

<span data-ttu-id="3b451-119">В основных примерах такого рода изменений формата используются модули подготовки видео DirectShow.</span><span class="sxs-lookup"><span data-stu-id="3b451-119">The main examples of this kind of format change involve the DirectShow video renderers.</span></span>

-   <span data-ttu-id="3b451-120">Исходный фильтр модуля [подготовки видео](video-renderer-filter.md) может переключаться между типами RGB и YUV во время потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="3b451-120">The original [Video Renderer](video-renderer-filter.md) filter can switch between RGB and YUV types during streaming.</span></span> <span data-ttu-id="3b451-121">При подключении фильтра требуется формат RGB, соответствующий текущим параметрам экрана.</span><span class="sxs-lookup"><span data-stu-id="3b451-121">When the filter connects, it requires an RGB format that matches the current display settings.</span></span> <span data-ttu-id="3b451-122">Это гарантирует, что он может вернуться на GDI, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="3b451-122">This guarantees that it can fall back on GDI if it needs to.</span></span> <span data-ttu-id="3b451-123">После начала потоковой передачи, если доступен DirectDraw, модуль подготовки отчетов запрашивает изменение формата на YUV-тип.</span><span class="sxs-lookup"><span data-stu-id="3b451-123">After streaming begins, if DirectDraw is available, the Video Renderer requests a format change to a YUV type.</span></span> <span data-ttu-id="3b451-124">Позже она может вернуться к RGB, если по какой бы то ни было причине по какой бы то ни было возникать на поверхности DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="3b451-124">Later, it might switch back to RGB if it loses the DirectDraw surface for any reason.</span></span>
-   <span data-ttu-id="3b451-125">Новый фильтр формирователя микширования видео (VMR) будет подключаться к любому формату, поддерживаемому графическим оборудованием, включая типы YUV.</span><span class="sxs-lookup"><span data-stu-id="3b451-125">The newer Video Mixing Renderer (VMR) filter will connect with any format that is supported by the graphics hardware, including YUV types.</span></span> <span data-ttu-id="3b451-126">Однако графическое оборудование может изменить шаг базовой поверхности DirectDraw, чтобы оптимизировать производительность.</span><span class="sxs-lookup"><span data-stu-id="3b451-126">However, the graphics hardware might change the stride of the underlying DirectDraw surface in order to optimize performance.</span></span> <span data-ttu-id="3b451-127">Фильтр VMR использует `QueryAccept` для создания отчета о новом STRIDE, указанном в элементе **Бивидс** структуры **битмапинфохеадер** .</span><span class="sxs-lookup"><span data-stu-id="3b451-127">The VMR filter uses `QueryAccept` to report the new stride, which is specified in the **biWidth** member of the **BITMAPINFOHEADER** structure.</span></span> <span data-ttu-id="3b451-128">Исходный и целевой прямоугольники в структуре **видеоинфохеадер** или **VIDEOINFOHEADER2** указывают область, в которой должно быть декодировано видео.</span><span class="sxs-lookup"><span data-stu-id="3b451-128">The source and target rectangles in the **VIDEOINFOHEADER** or **VIDEOINFOHEADER2** structure identify the region where the video should be decoded.</span></span>

<span data-ttu-id="3b451-129">**Примечание о реализации**</span><span class="sxs-lookup"><span data-stu-id="3b451-129">**Implementation Note**</span></span>

<span data-ttu-id="3b451-130">Маловероятно, что вы напишете фильтр, который должен запрашивать изменения в вышестоящем формате, так как это в основном является функцией модулей подготовки видео.</span><span class="sxs-lookup"><span data-stu-id="3b451-130">It is unlikely that you will write a filter that needs to request upstream format changes, since this is mainly a feature of video renderers.</span></span> <span data-ttu-id="3b451-131">Однако при написании фильтра преобразования видео или видеодекодера фильтр должен правильно реагировать на запросы из модуля подготовки видео.</span><span class="sxs-lookup"><span data-stu-id="3b451-131">However, if you write a video transform filter or a video decoder, your filter must respond correctly to requests from the video renderer.</span></span>

<span data-ttu-id="3b451-132">Фильтр на месте, расположенный между модулем подготовки видео и декодером, должен пройти все `QueryAccept` вызовы вышестоящего.</span><span class="sxs-lookup"><span data-stu-id="3b451-132">A trans-in-place filter that sits between the video renderer and the decoder should pass all `QueryAccept` calls upstream.</span></span> <span data-ttu-id="3b451-133">Сохранять новые сведения о форматировании при поступлении.</span><span class="sxs-lookup"><span data-stu-id="3b451-133">Store the new format information when it arrives.</span></span>

<span data-ttu-id="3b451-134">Фильтр преобразования копий (т. е. нетранзакционный фильтр) должен реализовывать одно из следующих поведений:</span><span class="sxs-lookup"><span data-stu-id="3b451-134">A copy-transform filter (that is, a non-trans-in-place filter) should implement one of the following behaviors:</span></span>

-   <span data-ttu-id="3b451-135">Передает изменения формата в восходящий и сохраняет новые сведения о форматировании при поступлении.</span><span class="sxs-lookup"><span data-stu-id="3b451-135">Pass format changes upstream and store the new format information when it arrives.</span></span> <span data-ttu-id="3b451-136">Фильтр должен использовать пользовательский распределитель, чтобы он мог присоединить формат к вышестоящему примеру.</span><span class="sxs-lookup"><span data-stu-id="3b451-136">Your filter must use a custom allocator so that it can attach the format to the upstream sample.</span></span>
-   <span data-ttu-id="3b451-137">Преобразование формата в фильтр.</span><span class="sxs-lookup"><span data-stu-id="3b451-137">Perform the format conversion inside the filter.</span></span> <span data-ttu-id="3b451-138">Возможно, это проще, чем передать восходящий формат изменения формата.</span><span class="sxs-lookup"><span data-stu-id="3b451-138">This is probably easier than passing the format change upstream.</span></span> <span data-ttu-id="3b451-139">Однако это может быть менее эффективным, чем возможность декодировать фильтр декодера в правильный формат.</span><span class="sxs-lookup"><span data-stu-id="3b451-139">However, it might be less efficient than letting the decoder filter decode into the correct format.</span></span>
-   <span data-ttu-id="3b451-140">В качестве крайней необходимости просто отклоните изменение формата.</span><span class="sxs-lookup"><span data-stu-id="3b451-140">As a last resort, simply reject the format change.</span></span> <span data-ttu-id="3b451-141">(Дополнительные сведения см. в исходном коде метода [**ктрансинплацеаутпутпин:: чеккмедиатипе**](ctransinplaceoutputpin-checkmediatype.md) в библиотеке базовых классов DirectShow.) Отклонение изменения формата может привести к снижению производительности, так как не позволяет модулю визуализации видео использовать наиболее эффективный формат.</span><span class="sxs-lookup"><span data-stu-id="3b451-141">(For more information, refer to the source code for the [**CTransInPlaceOutputPin::CheckMediaType**](ctransinplaceoutputpin-checkmediatype.md) method in the DirectShow base class library.) Rejecting a format change can reduce performance, however, because it prevents the video renderer from using the most efficient format.</span></span>

<span data-ttu-id="3b451-142">В следующем псевдокоде показано, как можно реализовать фильтр преобразования копий (производный от **ктрансформфилтер**), который может переключаться между типами выходных данных YUV и RGB.</span><span class="sxs-lookup"><span data-stu-id="3b451-142">The following pseudo-code shows how you might implement a copy-transform filter (derived from **CTransformFilter**) that can switch between YUV and RGB output types.</span></span> <span data-ttu-id="3b451-143">В этом примере предполагается, что фильтр выполняет само преобразование, а не передает вышестоящее изменение формата.</span><span class="sxs-lookup"><span data-stu-id="3b451-143">This example assumes that the filter does the conversion itself, rather than passing the format change upstream.</span></span>


```C++
HRESULT CMyTransform::CheckInputType(const CMediaType *pmt)
{
    if (pmt is a YUV type that you support) {
        return S_OK;
    }
    else {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }
}

HRESULT CMyTransform::CheckTransform(
    const CMediaType *mtIn, const CMediaType *mtOut)
{
    if (mtOut is a YUV or RGB type that you support)
    {
        if ((mtIn has the same video dimensions as mtOut) &&
            (you support the mtIn-to-mtOut transform))
        {
            return S_OK;
        }
    }
    // otherwise
    return VFW_E_TYPE_NOT_ACCEPTED;
}

// GetMediaType: Return a preferred output type.
HRESULT CMyTransform::GetMediaType(int iPosition, CMediaType *pMediaType)
{
    if (iPosition < 0) {
        return E_INVALIDARG;
    }
    switch (iPosition)
    {
    case 0:
        Copy the input type (YUV) to pMediaType
        return S_OK;
    case 1:
        Construct an RGB type that matches the input type.
        return S_OK;
    default:
        return VFW_S_NO_MORE_ITEMS;
    }
}

// SetMediaType: Override from CTransformFilter. 
HRESULT CMyTransform::SetMediaType(
    PIN_DIRECTION direction, const CMediaType *pmt)
{
    // Capture this information...
    if (direction == PINDIR_OUTPUT)
    {
       m_bYuv = (pmt->subtype == MEDIASUBTYPE_UYVY);
    }
    return S_OK;
}

HRESULT CMyTransform::Transform(
    IMediaSample *pSource, IMediaSample *pDest)
{
    // Look for format changes from downstream.
    CMediaType *pMT = NULL;
    HRESULT hr = pDest->GetMediaType((AM_MEDIA_TYPE**)&pMT);
    if (hr == S_OK)
    {
        hr = m_pOutput->CheckMediaType(pMT);
        if(FAILED(hr))
        {
            DeleteMediaType(pMT);
            return E_FAIL;
        }
        // Notify our own output pin about the new type.
        m_pOutput->SetMediaType(pMT);
        DeleteMediaType(pMT);
    }
    // Process the buffers
    if (m_bYuv) {
        return ProcessFrameYUV(pSource, pDest);
    }
    else {
        return ProcessFrameRGB(pSource, pDest);
    }
}
```



 

 




---
description: Обработка данных в кодировщике
ms.assetid: 7be4c5e7-db2c-4063-8e5c-af6ffb861aa5
title: Обработка данных в кодировщике
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99b7fedef50df61851408d084b511497eacd0288
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711413"
---
# <a name="processing-data-in-the-encoder"></a><span data-ttu-id="a72fe-103">Обработка данных в кодировщике</span><span class="sxs-lookup"><span data-stu-id="a72fe-103">Processing Data in the Encoder</span></span>

<span data-ttu-id="a72fe-104">После согласования типа входных данных и типа вывода для файла MFT кодировщика, как описано в разделе [согласование типов мультимедиа в кодировщике](media-type-negotiation-on-the-encoder.md), можно начать обработку образцов данных мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="a72fe-104">After you have negotiated the input type and output type for the encoder MFT, as described in [Media Type Negotiation on the Encoder](media-type-negotiation-on-the-encoder.md), you can start processing media data samples.</span></span> <span data-ttu-id="a72fe-105">Данные передаются в виде образцов мультимедиа (интерфейс [**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) ), а также получаются из выходных данных в виде образцов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="a72fe-105">The data is passed in form of media samples ([**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface) and also received from the output as media samples.</span></span>

<span data-ttu-id="a72fe-106">Перед отправкой данных кодировщику для обработки необходимо выделить пример носителя и добавить один из нескольких буферов мультимедиа, содержащих данные мультимедиа, которые необходимо закодировать.</span><span class="sxs-lookup"><span data-stu-id="a72fe-106">Before sending data to the encoder for processing, you must allocate a media sample and add one of more media buffers containing media data that needs to be encoded.</span></span> <span data-ttu-id="a72fe-107">Вызовите [**имфтрансформ::P роцессинпут**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) и передайте указатель на выделенный пример носителя.</span><span class="sxs-lookup"><span data-stu-id="a72fe-107">Call [**IMFTransform::ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) and pass a pointer to the allocated media sample.</span></span> <span data-ttu-id="a72fe-108">Помимо примера носителя, для **ProcessInput** также требуется идентификатор входного потока.</span><span class="sxs-lookup"><span data-stu-id="a72fe-108">In addition to the media sample, **ProcessInput** also needs the input stream identifier.</span></span> <span data-ttu-id="a72fe-109">Чтобы получить идентификатор потока, вызовите метод [**имфтрансформ:: жетстреамидс**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamids).</span><span class="sxs-lookup"><span data-stu-id="a72fe-109">To get the stream identifier, call [**IMFTransform::GetStreamIDs**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamids).</span></span> <span data-ttu-id="a72fe-110">Так как кодировщик предназначен только для одного и одного выходных данных, идентификаторы потоков всегда имеют значение 0.</span><span class="sxs-lookup"><span data-stu-id="a72fe-110">Because an encoder is designed to have only one and one output, these stream identifiers always have the value of 0.</span></span>

<span data-ttu-id="a72fe-111">Чтобы получить данные из кодировщика, вызовите [**имфтрансформ::P роцессаутпут**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).</span><span class="sxs-lookup"><span data-stu-id="a72fe-111">To get data from the encoder, call [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).</span></span> <span data-ttu-id="a72fe-112">Перед вызовом [**ProcessOutput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessoutput)необходимо выяснить, выделяет ли кодировщик образцы выходных данных, или необходимо сделать это явным образом.</span><span class="sxs-lookup"><span data-stu-id="a72fe-112">Before you call [**ProcessOutput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessoutput), you need to find out whether the encoder allocates the output media samples or you must do so explicitly.</span></span> <span data-ttu-id="a72fe-113">Для этого вызовите [**имфтрансформ:: жетаутпутстреаминфо**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo).</span><span class="sxs-lookup"><span data-stu-id="a72fe-113">To do this, call [**IMFTransform::GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo).</span></span> <span data-ttu-id="a72fe-114">Это возвращает образец выходных данных выходного носителя в структуре [**\_ \_ \_ сведений о потоке вывода MFT**](/windows/desktop/api/mftransform/ns-mftransform-mft_output_stream_info) .</span><span class="sxs-lookup"><span data-stu-id="a72fe-114">This returns output media sample information in the [**MFT\_OUTPUT\_STREAM\_INFO**](/windows/desktop/api/mftransform/ns-mftransform-mft_output_stream_info) structure.</span></span> <span data-ttu-id="a72fe-115">Если кодировщик выделяет примеры носителей, он возвращает выходной поток MFT, \_ \_ \_ предоставляющий \_ флаг Samples в элементе **dwFlags** , а элемент **кбсизе** содержит ноль.</span><span class="sxs-lookup"><span data-stu-id="a72fe-115">If the encoder allocates media samples, it returns the MFT\_OUTPUT\_STREAM\_PROVIDES\_SAMPLES flag in the **dwFlags** member and the **cbSize** member contains zero.</span></span> <span data-ttu-id="a72fe-116">Если кодировщику требуется выделить выходной буфер, создайте образец выходного носителя и связанный буфер мультимедиа на основе размера, возвращенного в **кбсизе**.</span><span class="sxs-lookup"><span data-stu-id="a72fe-116">If the encoder expects you to allocate the output buffer, create the output media sample and the associated media buffer based on the size returned in **cbSize**.</span></span> <span data-ttu-id="a72fe-117">При вызове [**процесссампле**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample)передайте указатель на созданный образец носителя.</span><span class="sxs-lookup"><span data-stu-id="a72fe-117">When you call [**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample), pass a pointer to the newly created media sample.</span></span> <span data-ttu-id="a72fe-118">Во время сеанса кодирования кодировщик заполняет буферы мультимедиа, на которые указывает образец выходного носителя, кодированными данными.</span><span class="sxs-lookup"><span data-stu-id="a72fe-118">During the encoding session, the encoder fills the media buffers, pointed by the output media sample, with the encoded data.</span></span>

<span data-ttu-id="a72fe-119">Чтобы начать сеанс кодирования, передайте пример входного носителя в кодировщик, вызвав метод [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).</span><span class="sxs-lookup"><span data-stu-id="a72fe-119">To start the encoding session, pass the input media sample to the encoder by calling [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).</span></span> <span data-ttu-id="a72fe-120">Кодировщик начинает обработку, а данные и создает один или несколько примеров выходных носителей, которые необходимо извлечь с помощью [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) , если для \_ преобразования MF E \_ \_ требуется \_ больше \_ входных данных.</span><span class="sxs-lookup"><span data-stu-id="a72fe-120">The encoder starts processing and the data and produces one or more output media samples that must be retrieved by [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) as long as it returns MF\_E\_TRANSFORM\_NEED\_MORE\_INPUT.</span></span> <span data-ttu-id="a72fe-121">При вызове метода **ProcessInput** для передачи большего числа входных данных, если имеются выходные данные для извлечения, то метод **ProcessInput** завершается с помощью MF \_ E \_ нотакцептинг.</span><span class="sxs-lookup"><span data-stu-id="a72fe-121">If you call **ProcessInput** to pass more input as long as there is output data to be retrieved, **ProcessInput** fails with MF\_E\_NOTACCEPTING.</span></span> <span data-ttu-id="a72fe-122">Кодировщик не принимает никаких входных данных, пока клиент не вызовет **ProcessOutput** по крайней мере один раз.</span><span class="sxs-lookup"><span data-stu-id="a72fe-122">The encoder does not accept any more input until the client calls **ProcessOutput** at least once.</span></span>

<span data-ttu-id="a72fe-123">Необходимо задать точные метки времени и длительности для всех пройденных выборок.</span><span class="sxs-lookup"><span data-stu-id="a72fe-123">You should set accurate time stamps and durations for all input samples passed.</span></span> <span data-ttu-id="a72fe-124">Метки времени не являются строго необходимыми, но помогают поддерживать синхронизацию аудио и видео.</span><span class="sxs-lookup"><span data-stu-id="a72fe-124">Time stamps are not strictly required but help maintain audio/video synchronization.</span></span> <span data-ttu-id="a72fe-125">Если у вас нет меток времени для выборки, лучше оставить их, не используя неопределенные значения.</span><span class="sxs-lookup"><span data-stu-id="a72fe-125">If you do not have the time stamps for your samples it is better to leave them out than to use uncertain values.</span></span>

## <a name="encoder-processing-example"></a><span data-ttu-id="a72fe-126">Пример обработки кодировщика</span><span class="sxs-lookup"><span data-stu-id="a72fe-126">Encoder Processing Example</span></span>

<span data-ttu-id="a72fe-127">В следующем примере кода показано, как вызвать [**имфтрансформ::P роцессаутпут**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) , чтобы получить закодированный пример.</span><span class="sxs-lookup"><span data-stu-id="a72fe-127">The following example code shows how to call [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) to get an encoded sample.</span></span> <span data-ttu-id="a72fe-128">Полный контекст этого примера см. в разделе [пример кода кодировщика](encoder-example-code.md).</span><span class="sxs-lookup"><span data-stu-id="a72fe-128">For the complete context of this example, see [Encoder Example Code](encoder-example-code.md).</span></span>


```C++
HRESULT CWmaEncoder::ProcessOutput(IMFSample **ppSample)
{
    if (m_pMFT == NULL)
    {
        return MF_E_NOT_INITIALIZED;
    }

    *ppSample = NULL;

    IMFMediaBuffer* pBufferOut = NULL;
    IMFSample* pSampleOut = NULL;

    DWORD dwStatus;
  
    MFT_OUTPUT_STREAM_INFO mftStreamInfo = { 0 };
    MFT_OUTPUT_DATA_BUFFER mftOutputData = { 0 };

    HRESULT hr = m_pMFT->GetOutputStreamInfo(m_dwOutputID, &mftStreamInfo);
    if (FAILED(hr))
    {
        goto done;
    }

    //create a buffer for the output sample
    hr = MFCreateMemoryBuffer(mftStreamInfo.cbSize, &pBufferOut);
    if (FAILED(hr))
    {
        goto done;
    }

    //Create the output sample
    hr = MFCreateSample(&pSampleOut);
    if (FAILED(hr))
    {
        goto done;
    }

    //Add the output buffer 
    hr = pSampleOut->AddBuffer(pBufferOut);
    if (FAILED(hr))
    {
        goto done;
    }
 
    //Set the output sample
    mftOutputData.pSample = pSampleOut;

    //Set the output id
    mftOutputData.dwStreamID = m_dwOutputID;

    //Generate the output sample
    hr = m_pMFT->ProcessOutput(0, 1, &mftOutputData, &dwStatus);
    if (hr == MF_E_TRANSFORM_NEED_MORE_INPUT)
    {
        hr = S_OK;
        goto done;
    }

    // TODO: Handle MF_E_TRANSFORM_STREAM_CHANGE

    if (FAILED(hr))
    {
        goto done;
    }

    *ppSample = pSampleOut;
    (*ppSample)->AddRef();

done:
    SafeRelease(&pBufferOut);
    SafeRelease(&pSampleOut);
    return hr;
};
```



## <a name="related-topics"></a><span data-ttu-id="a72fe-129">См. также</span><span class="sxs-lookup"><span data-stu-id="a72fe-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a72fe-130">Мультиплексор ASF</span><span class="sxs-lookup"><span data-stu-id="a72fe-130">ASF Multiplexer</span></span>](asf-multiplexer.md)
</dt> <dt>

[<span data-ttu-id="a72fe-131">Создание экземпляра MFT для кодировщика</span><span class="sxs-lookup"><span data-stu-id="a72fe-131">Instantiating an Encoder MFT</span></span>](instantiating-the-encoder-mft.md)
</dt> <dt>

[<span data-ttu-id="a72fe-132">Кодировщики Windows Media</span><span class="sxs-lookup"><span data-stu-id="a72fe-132">Windows Media Encoders</span></span>](windows-media-encoders.md)
</dt> </dl>

 

 




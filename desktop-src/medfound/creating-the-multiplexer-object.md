---
description: Создание объекта мультиплексора
ms.assetid: a5adc40c-abb4-4012-b6f2-eb871eaed7b9
title: Создание объекта мультиплексора
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b28dd7933bdd7c3a8587c96cb490c4e4122ecc04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262810"
---
# <a name="creating-the-multiplexer-object"></a><span data-ttu-id="b84c5-103">Создание объекта мультиплексора</span><span class="sxs-lookup"><span data-stu-id="b84c5-103">Creating the Multiplexer Object</span></span>

<span data-ttu-id="b84c5-104">Мультиплексор ASF — это объект слоя Вмконтаинер, который работает с [объектом данных ASF](asf-file-structure.md) и дает приложению возможность создавать пакеты данных ASF для потоков мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="b84c5-104">The ASF multiplexer is a WMContainer layer object that works with the [ASF Data Object](asf-file-structure.md) and gives an application the ability to generate ASF data packets for media streams.</span></span>

<span data-ttu-id="b84c5-105">Объект мультиплексора предоставляет интерфейс [**имфасфмултиплексер**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmultiplexer) .</span><span class="sxs-lookup"><span data-stu-id="b84c5-105">The multiplexer object exposes the [**IMFASFMultiplexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmultiplexer) interface.</span></span> <span data-ttu-id="b84c5-106">Чтобы создать мультиплексор, вызовите [**мфкреатеасфмултиплексер**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmultiplexer).</span><span class="sxs-lookup"><span data-stu-id="b84c5-106">To create the multiplexer, call [**MFCreateASFMultiplexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmultiplexer).</span></span> <span data-ttu-id="b84c5-107">Эта функция возвращает указатель на пустой объект.</span><span class="sxs-lookup"><span data-stu-id="b84c5-107">This function returns a pointer to an empty object.</span></span> <span data-ttu-id="b84c5-108">Если приложение записывает новый ASF-файл, приложение должно инициализировать мультиплексор с помощью объекта Контентинфо.</span><span class="sxs-lookup"><span data-stu-id="b84c5-108">If the application is writing a new ASF file, the application must initialize the multiplexer with a ContentInfo object.</span></span> <span data-ttu-id="b84c5-109">Для этого вызовите метод [**имфасфмултиплексер:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize).</span><span class="sxs-lookup"><span data-stu-id="b84c5-109">To do this, call [**IMFASFMultiplexer::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize).</span></span> <span data-ttu-id="b84c5-110">Указанный объект Контентинфо представляет объект заголовка ASF нового файла.</span><span class="sxs-lookup"><span data-stu-id="b84c5-110">The specified ContentInfo object represents the ASF Header Object of the new file.</span></span> <span data-ttu-id="b84c5-111">Сведения о создании и инициализации объекта Контентинфо для нового файла см. [в разделе Инициализация объекта Контентинфо нового ASF-файла](initializing-the-contentinfo-object-of-a-new-asf-file.md).</span><span class="sxs-lookup"><span data-stu-id="b84c5-111">For information about creating and initializing the ContentInfo object for a new file, see [Initializing the ContentInfo Object of a New ASF File](initializing-the-contentinfo-object-of-a-new-asf-file.md).</span></span>

<span data-ttu-id="b84c5-112">Метод [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) анализирует объект контентинфо, чтобы получить сведения о конфигурации потока, такие как число потоков, размер пакета, предпроход.</span><span class="sxs-lookup"><span data-stu-id="b84c5-112">The [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) method parses the ContentInfo object to collect stream configuration information such as the number of streams, packet size, preroll.</span></span> <span data-ttu-id="b84c5-113">Кроме того, мультиплексору также могут потребоваться параметры сегмента утечки и единицы расширения полезных данных.</span><span class="sxs-lookup"><span data-stu-id="b84c5-113">Optionally, the multiplexer might also need leaky bucket parameters, and the payload extension units.</span></span> <span data-ttu-id="b84c5-114">Эти сведения необходимы для создания пакетов данных, соответствующих требованиям, определенным в объекте заголовка ASF.</span><span class="sxs-lookup"><span data-stu-id="b84c5-114">This information is required in order to generate data packets that match the requirements defined in the ASF Header Object.</span></span> <span data-ttu-id="b84c5-115">Метод **Initialize** настраивает мультиплексор на основе типа носителя и параметров конфигурации потоков.</span><span class="sxs-lookup"><span data-stu-id="b84c5-115">The **Initialize** method configures the multiplexer based on the media type and configuration settings of the streams.</span></span> <span data-ttu-id="b84c5-116">Например, если поток настроен на наличие расширений полезных данных (см. раздел [Создание и настройка потоков ASF](creating-and-configuring-asf-streams.md)), а затем мультиплексор настроен на добавление этих значений к созданным пакетам данных.</span><span class="sxs-lookup"><span data-stu-id="b84c5-116">For example, if a stream is configured to have payload extensions (see [Creating and Configuring ASF Streams](creating-and-configuring-asf-streams.md)), and then the multiplexer is configured to add those values to the generated data packets.</span></span>

<span data-ttu-id="b84c5-117">Метод [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) также получает маркер для начального объекта данных, который был создан во время создания объекта контентинфо для записи.</span><span class="sxs-lookup"><span data-stu-id="b84c5-117">The [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) method also gets a handle to the initial data object that was created during the creation of the ContentInfo object for writing.</span></span> <span data-ttu-id="b84c5-118">При создании пакета данных мультиплексор добавляет пакеты в объект данных и соответствующим образом обновляет его.</span><span class="sxs-lookup"><span data-stu-id="b84c5-118">During data packet generation, the multiplexer adds packets to the data object and updates it appropriately.</span></span> <span data-ttu-id="b84c5-119">После того как мультиплексор создаст все пакеты данных, он обновляет указанный объект Контентинфо, чтобы были обновлены определенные значения, например количество пакетов данных.</span><span class="sxs-lookup"><span data-stu-id="b84c5-119">After the multiplexer generates all the data packets, it updates the supplied ContentInfo object so that certain values, such as number of data packets, are updated.</span></span>

<span data-ttu-id="b84c5-120">В следующем примере кода показано, как создать мультиплексор и инициализировать его с помощью объекта Контентинфо.</span><span class="sxs-lookup"><span data-stu-id="b84c5-120">The following code example shows how to create a multiplexer and initialize it with a ContentInfo object.</span></span>


```C++
//-------------------------------------------------------------------
// CreateOutputGenerators
//
// Creates the ASF mux and the ASF Content Info object for the 
// output file.
//-------------------------------------------------------------------

HRESULT CreateOutputGenerators(
    IMFASFProfile *pProfile, 
    IMFASFContentInfo **ppContentInfo, 
    IMFASFMultiplexer **ppMux
    )
{
    IMFASFContentInfo *pContentInfo = NULL;
    IMFASFMultiplexer *pMux = NULL;

    // Use the ASF profile to create the ContentInfo object.
    HRESULT hr = MFCreateASFContentInfo(&pContentInfo);

    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->SetProfile(pProfile);
    }

    // Create the ASF Multiplexer object.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateASFMultiplexer(&pMux);
    }
    
    // Initialize it using the new ContentInfo object.
    if (SUCCEEDED(hr))
    {
        hr = pMux->Initialize(pContentInfo);
    }

    // Return the pointers to the caller.
    if (SUCCEEDED(hr))
    {
        *ppContentInfo = pContentInfo;
        (*ppContentInfo)->AddRef();

        *ppMux = pMux;
        (*ppMux)->AddRef();
    }

    SafeRelease(&pContentInfo);
    SafeRelease(&pMux);

    return hr;
}
```



<span data-ttu-id="b84c5-121">Сведения о функции, используемой в законченном приложении, см. в разделе [учебник. копирование потоков ASF из одного файла в другой](tutorial--copying-asf-streams-from-one-file-to-another.md).</span><span class="sxs-lookup"><span data-stu-id="b84c5-121">To see this function used in a complete application, see [Tutorial: Copying ASF Streams from One File to Another](tutorial--copying-asf-streams-from-one-file-to-another.md).</span></span>

## <a name="multiplexer-initialization-and-leaky-bucket-settings"></a><span data-ttu-id="b84c5-122">Параметры инициализации мультиплексора и утечек сегментов</span><span class="sxs-lookup"><span data-stu-id="b84c5-122">Multiplexer Initialization and Leaky Bucket Settings</span></span>

<span data-ttu-id="b84c5-123">Метод [**имфасфмултиплексер:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) настраивает мультиплексор для определения потока данных контейнера утечки.</span><span class="sxs-lookup"><span data-stu-id="b84c5-123">The [**IMFASFMultiplexer::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) method configures the multiplexer to determine the leaky bucket data flow.</span></span> <span data-ttu-id="b84c5-124">Чтобы настроить эти параметры, убедитесь, что для указанного объекта Контентинфо установлены следующие значения свойств.</span><span class="sxs-lookup"><span data-stu-id="b84c5-124">To configure these parameters, make sure that the following property values are set on the specified ContentInfo object.</span></span> <span data-ttu-id="b84c5-125">Дополнительные сведения об установке этих свойств см. [в разделе Задание свойств в объекте контентинфо](setting-properties-in-the-contentinfo-object.md).</span><span class="sxs-lookup"><span data-stu-id="b84c5-125">For information about setting these properties, see [Setting Properties in the ContentInfo Object](setting-properties-in-the-contentinfo-object.md).</span></span>

-   <span data-ttu-id="b84c5-126">[**Мфпкэй \_ Свойство автоматической \_ настройки \_ скорости асфмедиасинк**](mfpkey-asfmediasink-autoadjust-bitrate-property.md) : указывает, нужно ли мультиплексору автоматически настраивать скорость потока данных, чтобы обеспечить его в контейнере утечки.</span><span class="sxs-lookup"><span data-stu-id="b84c5-126">[**MFPKEY\_ASFMEDIASINK\_AUTOADJUST\_BITRATE**](mfpkey-asfmediasink-autoadjust-bitrate-property.md) property: This indicates whether the multiplexer needs to adjust the bit rate automatically, to maintain the data flow in the leaky bucket.</span></span> <span data-ttu-id="b84c5-127">Этот параметр может быть изменен приложением путем вызова [**имфасфмултиплексер:: сетфлагс**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags) и передачи флага **\_ \_ авторегулировки скорости \_ для мультиплексора мфасф** .</span><span class="sxs-lookup"><span data-stu-id="b84c5-127">This setting can be changed by the application by calling [**IMFASFMultiplexer::SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags) and passing the **MFASF\_MULTIPLEXER\_AUTOADJUST\_BITRATE** flag.</span></span>

-   <span data-ttu-id="b84c5-128">[**Мфпкэй \_ \_Базовое свойство \_ сендтиме асфмедиасинк**](mfpkey-asfmediasink-base-sendtime-property.md) : время отправки указывает, когда будут освобождены полезные данные в сегменте утечки.</span><span class="sxs-lookup"><span data-stu-id="b84c5-128">[**MFPKEY\_ASFMEDIASINK\_BASE\_SENDTIME**](mfpkey-asfmediasink-base-sendtime-property.md) property: The send time indicates when the payload inside the leaky bucket will be released.</span></span> <span data-ttu-id="b84c5-129">Время отправки должно быть больше или равно времени презентации, поскольку полезные данные должны иметь время для получения назначения до времени презентации.</span><span class="sxs-lookup"><span data-stu-id="b84c5-129">Send times must be equal to or earlier than the presentation time because the payload must have time to get to the destination before the presentation time.</span></span>

    <span data-ttu-id="b84c5-130">Это значение свойства является первым временем отправки.</span><span class="sxs-lookup"><span data-stu-id="b84c5-130">This property value is the first send time.</span></span> <span data-ttu-id="b84c5-131">Мультиплексор использует это значение для вычисления последующего времени отправки, чтобы обеспечить непрерывную передачу данных через контейнер.</span><span class="sxs-lookup"><span data-stu-id="b84c5-131">The multiplexer uses this value to calculate the subsequent send times to ensure that data flows through the bucket steadily.</span></span> <span data-ttu-id="b84c5-132">Если для мультиплексора установлен флаг **\_ авторегулировки скорости мфасф мультиплексора \_ \_** , то мультиплексор будет корректировать скорость потока, чтобы полезные данные отправлялись, когда окно буфера близко к заполнению.</span><span class="sxs-lookup"><span data-stu-id="b84c5-132">If the **MFASF\_MULTIPLEXER\_AUTOADJUST\_BITRATE** flag has been set on the multiplexer, the multiplexer will adjust the bit rate so that the payload is sent out when the buffer window is close to being full.</span></span> <span data-ttu-id="b84c5-133">Если флаг не установлен, мультиплексор не сможет создать пакеты данных из-за переполнения полосы пропускания.</span><span class="sxs-lookup"><span data-stu-id="b84c5-133">If the flag is not set, the multiplexer fails to generate data packets due to bandwidth overrun.</span></span>

<span data-ttu-id="b84c5-134">Мультиплексор получает сведения о конфигурации потока из профиля ASF, связанного с объектом Контентинфо, указанным в методе [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) .</span><span class="sxs-lookup"><span data-stu-id="b84c5-134">The multiplexer obtains stream configuration information from the ASF profile associated with the ContentInfo object specified in the [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) method.</span></span> <span data-ttu-id="b84c5-135">Сведения о конфигурации потока включают параметры контейнера с утечкой.</span><span class="sxs-lookup"><span data-stu-id="b84c5-135">The stream configuration information includes leaky bucket parameters.</span></span> <span data-ttu-id="b84c5-136">Это значение требуется мультиплексору для создания пакетов данных.</span><span class="sxs-lookup"><span data-stu-id="b84c5-136">This value is required by the multiplexer to generate data packets.</span></span>

<span data-ttu-id="b84c5-137">Чтобы указать параметры контейнера с утечкой, установите значения в атрибуте [**MF \_ асфстреамконфиг \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) в объекте конфигурации потока, который представляет поток в профиле.</span><span class="sxs-lookup"><span data-stu-id="b84c5-137">To specify the leaky bucket parameters, set the values in the [**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) attribute on the stream configuration object that represents the stream in the profile.</span></span> <span data-ttu-id="b84c5-138">Чтобы использовать значение окна буфера, используемое кодировщиком, вызовите [**ивмкодеклеакибуккет:: жетбуфферсизебитс**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md).</span><span class="sxs-lookup"><span data-stu-id="b84c5-138">To use the buffer window value, which is used by the encoder, call [**IWMCodecLeakyBucket::GetBufferSizeBits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md).</span></span> <span data-ttu-id="b84c5-139">Фактическое значение окна буфера известно только после установки типа выходного носителя кодировщика.</span><span class="sxs-lookup"><span data-stu-id="b84c5-139">The actual buffer window value is known only after setting the output media type of the encoder.</span></span> <span data-ttu-id="b84c5-140">Сведения о настройке типа выходных данных мультимедиа см. в разделе [Согласование типа носителя в кодировщике](media-type-negotiation-on-the-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="b84c5-140">For information about setting the output media type, see [Media Type Negotiation on the Encoder](media-type-negotiation-on-the-encoder.md).</span></span>

> [!Note]  
> <span data-ttu-id="b84c5-141">Значения сегментов утечки, используемые кодировщиком, могут отличаться в объекте Контентинфо, предоставленном профилем ASF, который использовался для создания мультиплексора.</span><span class="sxs-lookup"><span data-stu-id="b84c5-141">The leaky bucket values used by the encoder might be different in the ContentInfo object that was provided by the ASF Profile that was used to create the multiplexer.</span></span>

 

<span data-ttu-id="b84c5-142">Метод [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) обновляет объект контентинфо, чтобы правильные значения отражались в окончательном ОБЪЕКТЕ заголовка ASF.</span><span class="sxs-lookup"><span data-stu-id="b84c5-142">The [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) method updates the ContentInfo object so that the correct values are reflected in the final ASF Header Object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b84c5-143">См. также</span><span class="sxs-lookup"><span data-stu-id="b84c5-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b84c5-144">Мультиплексор ASF</span><span class="sxs-lookup"><span data-stu-id="b84c5-144">ASF Multiplexer</span></span>](asf-multiplexer.md)
</dt> <dt>

[<span data-ttu-id="b84c5-145">Создание новых пакетов данных ASF</span><span class="sxs-lookup"><span data-stu-id="b84c5-145">Generating New ASF Data Packets</span></span>](generating-new-asf-data-packets.md)
</dt> </dl>

 

 

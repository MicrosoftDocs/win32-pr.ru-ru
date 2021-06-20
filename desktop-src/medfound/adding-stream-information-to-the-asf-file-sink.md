---
description: Сведения о добавлении потоковых данных в приемник файлов ASF, который приложение может использовать для архивации данных ASF Media в файл.
ms.assetid: 21cbde27-a2ca-4298-9197-43bcaf05588d
title: Добавление потоковой информации в приемник файлов ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de8202de8da5cb8e17534c334e3d39dddb3c4f99
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404365"
---
# <a name="adding-stream-information-to-the-asf-file-sink"></a><span data-ttu-id="ab5d6-103">Добавление потоковой информации в приемник файлов ASF</span><span class="sxs-lookup"><span data-stu-id="ab5d6-103">Adding Stream Information to the ASF File Sink</span></span>

<span data-ttu-id="ab5d6-104">Приемник ASF-файлов — это реализация [**имфмедиасинк**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) , предоставляемая Media Foundation, которую приложение может использовать для архивации данных ASF Media в файл.</span><span class="sxs-lookup"><span data-stu-id="ab5d6-104">The ASF file sink is an implementation of [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) provided by Media Foundation that an application can use to archive ASF media data to a file.</span></span> <span data-ttu-id="ab5d6-105">Сведения об объектной модели приемников ASF Media и общем использовании см. в статье [приемники мультимедиа ASF](asf-media-sinks.md).</span><span class="sxs-lookup"><span data-stu-id="ab5d6-105">For information about ASF Media Sinks' object model and general usage, see [ASF Media Sinks](asf-media-sinks.md).</span></span>

<span data-ttu-id="ab5d6-106">После создания экземпляра приемника файла его необходимо настроить перед созданием топологии.</span><span class="sxs-lookup"><span data-stu-id="ab5d6-106">After instantiating the file sink, it must be configured before building the topology.</span></span> <span data-ttu-id="ab5d6-107">Приемнику файла необходимо узнать о потоках в выходном файле, сведениях о режиме кодирования и метаданных.</span><span class="sxs-lookup"><span data-stu-id="ab5d6-107">The file sink needs to know about the streams in the output file, the encoding mode information, and the metadata.</span></span> <span data-ttu-id="ab5d6-108">В этом разделе описывается процесс добавления потока в приемник файла.</span><span class="sxs-lookup"><span data-stu-id="ab5d6-108">This topic describes the process of adding stream in the file sink.</span></span>

-   [<span data-ttu-id="ab5d6-109">Добавление потоков в приемник файлов ASF</span><span class="sxs-lookup"><span data-stu-id="ab5d6-109">Adding Streams in the ASF File Sink</span></span>](#adding-streams-in-the-asf-file-sink)
-   [<span data-ttu-id="ab5d6-110">Перечисление приемников потоков</span><span class="sxs-lookup"><span data-stu-id="ab5d6-110">Enumerating Stream Sinks</span></span>](#enumerating-stream-sinks)
-   [<span data-ttu-id="ab5d6-111">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="ab5d6-111">Related topics</span></span>](#related-topics)

## <a name="adding-streams-in-the-asf-file-sink"></a><span data-ttu-id="ab5d6-112">Добавление потоков в приемник файлов ASF</span><span class="sxs-lookup"><span data-stu-id="ab5d6-112">Adding Streams in the ASF File Sink</span></span>

<span data-ttu-id="ab5d6-113">Приемник файла должен иметь представление о потоках вывода и их свойствах, чтобы они могли соответствующим образом формировать выходные образцы и добавлять их в выходной файл ASF.</span><span class="sxs-lookup"><span data-stu-id="ab5d6-113">The file sink must know of the output streams and their properties so that it can generate output samples accordingly and add them to the output ASF file.</span></span> <span data-ttu-id="ab5d6-114">Эти параметры записываются в окончательный объект заголовка ASF.</span><span class="sxs-lookup"><span data-stu-id="ab5d6-114">These settings are written to the final ASF Header Object.</span></span>

<span data-ttu-id="ab5d6-115">Чтобы задать сведения о потоке, необходимо иметь ссылку на объект ASF Контентинфо приемника файлов.</span><span class="sxs-lookup"><span data-stu-id="ab5d6-115">To set stream information, you must have a reference to the file sink's ASF ContentInfo object.</span></span> <span data-ttu-id="ab5d6-116">Дополнительные сведения см. [в разделе Создание приемника файлов ASF](creating-the-asf-file-sink.md).</span><span class="sxs-lookup"><span data-stu-id="ab5d6-116">For information, see [Creating the ASF File Sink](creating-the-asf-file-sink.md).</span></span>

<span data-ttu-id="ab5d6-117">Следующая процедура описывает общие шаги настройки потока с помощью объекта профиля ASF.</span><span class="sxs-lookup"><span data-stu-id="ab5d6-117">The following procedure summarizes the general steps for configuring stream by using the ASF profile object.</span></span>

<span data-ttu-id="ab5d6-118">**Настройка потоковой информации в приемнике файлов ASF**</span><span class="sxs-lookup"><span data-stu-id="ab5d6-118">**To configure stream information in the ASF file sink**</span></span>

1.  <span data-ttu-id="ab5d6-119">Создайте объект профиля ASF, вызвав [**мфкреатеасфпрофиле**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile).</span><span class="sxs-lookup"><span data-stu-id="ab5d6-119">Create an ASF profile object by calling [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile).</span></span>
2.  <span data-ttu-id="ab5d6-120">Для каждого потока в выходном файле создайте тип мультимедиа для целевого потока, добавляемого в приемник файла.</span><span class="sxs-lookup"><span data-stu-id="ab5d6-120">For each stream in the output file, create a media type for the target stream to be added in the file sink.</span></span> <span data-ttu-id="ab5d6-121">Тип мультимедиа должен быть совместим с типами выходных данных, поддерживаемыми кодировщиками Windows Media.</span><span class="sxs-lookup"><span data-stu-id="ab5d6-121">The media type must be compatible with the output types supported by the Windows Media encoders.</span></span>

    <span data-ttu-id="ab5d6-122">Дополнительные сведения о добавлении в профиль звуковых потоков см. в разделе Создание звуковых потоков для кодирования ASF.</span><span class="sxs-lookup"><span data-stu-id="ab5d6-122">For information about adding audio streams to the profile, see Creating Audio Streams for ASF Encoding.</span></span>

    <span data-ttu-id="ab5d6-123">Сведения о добавлении потоков видео в профиль см. в разделе Создание видеопотоков для кодирования ASF.</span><span class="sxs-lookup"><span data-stu-id="ab5d6-123">For information about adding video streams to the profile, see Creating Video Streams for ASF Encoding.</span></span>

3.  <span data-ttu-id="ab5d6-124">Создайте потоки на основе типов носителей, созданных на шаге 2, вызвав [**имфасфпрофиле:: креатестреам**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream).</span><span class="sxs-lookup"><span data-stu-id="ab5d6-124">Create streams based on the media types created in step 2 by calling [**IMFASFProfile::CreateStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream).</span></span>
4.  <span data-ttu-id="ab5d6-125">Назначьте номер потока для вновь созданного потока, вызвав указатель интерфейса [**имфасфстреамконфиг**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) , полученный на шаге 3.</span><span class="sxs-lookup"><span data-stu-id="ab5d6-125">Assign a stream number for the newly created stream by calling [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) interface pointer received in step 3.</span></span>
5.  <span data-ttu-id="ab5d6-126">При необходимости настройте поток со следующими сведениями:</span><span class="sxs-lookup"><span data-stu-id="ab5d6-126">Optionally configure the stream with the following information:</span></span>
    -   <span data-ttu-id="ab5d6-127">Параметры сегмента с утечкой путем установки атрибутов: [**MF \_ асфстреамконфиг \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) или [**MF \_ асфстреамконфиг \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="ab5d6-127">Leaky bucket parameters by setting the attributes: [**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) or [**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md)</span></span>
    -   <span data-ttu-id="ab5d6-128">Расширение полезных данных — взаимное исключение путем вызова методов [**имфасфстреамконфиг**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) .</span><span class="sxs-lookup"><span data-stu-id="ab5d6-128">Payload extension, mutual exclusion by calling [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) methods.</span></span>
6.  <span data-ttu-id="ab5d6-129">При необходимости задайте размер пакета данных для профиля, установив атрибуты [**MF \_ асфпрофиле \_ минпаккетсизе**](mf-asfprofile-minpacketsize-attribute.md) и [**MF \_ асфпрофиле \_ макспаккетсизе**](mf-asfprofile-maxpacketsize-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="ab5d6-129">Optionally set data packet size for the profile by setting [**MF\_ASFPROFILE\_MINPACKETSIZE**](mf-asfprofile-minpacketsize-attribute.md) and [**MF\_ASFPROFILE\_MAXPACKETSIZE**](mf-asfprofile-maxpacketsize-attribute.md) attributes.</span></span> <span data-ttu-id="ab5d6-130">Профиль ASF предоставляет интерфейс [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) , к которому приложение может получить ссылку путем вызова **Имфасфпрофиле:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="ab5d6-130">The ASF profile exposes the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface, which an application can get reference to by calling **IMFASFProfile::QueryInterface**.</span></span>
7.  <span data-ttu-id="ab5d6-131">Задайте сведения о кодировке для потока в приемнике файла.</span><span class="sxs-lookup"><span data-stu-id="ab5d6-131">Set encoding information for the stream in the file sink.</span></span> <span data-ttu-id="ab5d6-132">Описывается в разделе [Установка свойств в приемнике файла](setting-properties-in-the-file-sink.md).</span><span class="sxs-lookup"><span data-stu-id="ab5d6-132">Discussed in [Setting Properties in the File Sink](setting-properties-in-the-file-sink.md).</span></span>
8.  <span data-ttu-id="ab5d6-133">Добавьте поток в профиль, вызвав [**имфасфпрофиле:: сетстреам**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream).</span><span class="sxs-lookup"><span data-stu-id="ab5d6-133">Add the stream to the profile by calling [**IMFASFProfile::SetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream).</span></span>
9.  <span data-ttu-id="ab5d6-134">Свяжите профиль с объектом Контентинфо, вызвав [**имфасфконтентинфо:: сетпрофиле**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile).</span><span class="sxs-lookup"><span data-stu-id="ab5d6-134">Associate the profile with the ContentInfo object by calling [**IMFASFContentInfo::SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile).</span></span>

<span data-ttu-id="ab5d6-135">Чтобы изменить существующий поток, приложение может получить ссылку на интерфейс [**имфасфстреамконфиг**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) потока и перенастроить его в соответствии с требованиями.</span><span class="sxs-lookup"><span data-stu-id="ab5d6-135">To modify an existing stream, the application can get a reference to the stream's [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) interface and reconfigure it according to the requirements.</span></span> <span data-ttu-id="ab5d6-136">Чтобы добавить или удалить потоки, приложение должно вызвать [**имфасфпрофиле:: ремовестреам**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removestream).</span><span class="sxs-lookup"><span data-stu-id="ab5d6-136">To add or remove streams, the application must call [**IMFASFProfile::RemoveStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removestream).</span></span> <span data-ttu-id="ab5d6-137">Чтобы применить эти изменения, изменить потоковые изменения или удалить, необходимо снова задать профиль в объекте Контентинфо.</span><span class="sxs-lookup"><span data-stu-id="ab5d6-137">To apply these changes, stream modifications or removal, you must set the profile again in the ContentInfo object.</span></span> <span data-ttu-id="ab5d6-138">При этом существующий профиль, уже связанный с объектом Контентинфо, перезаписывается.</span><span class="sxs-lookup"><span data-stu-id="ab5d6-138">This overwrites the existing profile that is already associated with the ContentInfo object.</span></span>


```C++
//-------------------------------------------------------------------
//  CreateVideoStream
//  Create an video stream and add it to the profile.
//
//  pProfile: A pointer to the ASF profile.
//  wStreamNumber: Stream number to assign for the new stream.
//    pType: A pointer to the source's video media type.
//-------------------------------------------------------------------

HRESULT CreateVideoStream(IMFASFProfile* pProfile, WORD wStreamNumber, IMFMediaType* pType)
{
    if (!pProfile)
    {
        return E_INVALIDARG;
    }
    if (wStreamNumber < 1 || wStreamNumber > 127 )
    {
        return MF_E_INVALIDSTREAMNUMBER;
    }

    HRESULT hr = S_OK;

    
    IMFMediaType* pVideoType = NULL;
    IMFASFStreamConfig* pVideoStream = NULL;

    UINT32 dwBitRate = 0;
        
    //Create a new video type from the source type
    hr = CreateCompressedVideoType(pType, &pVideoType);
    if (FAILED(hr))
    {
        goto done;
    }

    //Create a new stream with the video type
    hr = pProfile->CreateStream(pVideoType, &pVideoStream);
    if (FAILED(hr))
    {
        goto done;
    }
    

    //Set a valid stream number
    hr = pVideoStream->SetStreamNumber(wStreamNumber);
    if (FAILED(hr))
    {
        goto done;
    }

    //Add the stream to the profile
    hr = pProfile->SetStream(pVideoStream);
    if (FAILED(hr))
    {
        goto done;
    }

    wprintf_s(L"Video Stream created. Stream Number: %d .\n", wStreamNumber);

done:

    SafeRelease(&pVideoStream);
    SafeRelease(&pVideoType);

    return hr;
}
```



## <a name="enumerating-stream-sinks"></a><span data-ttu-id="ab5d6-139">Перечисление приемников потоков</span><span class="sxs-lookup"><span data-stu-id="ab5d6-139">Enumerating Stream Sinks</span></span>

<span data-ttu-id="ab5d6-140">Для каждого потока в профиле, о котором известно объект Контентинфо, приемник файлов ASF создает и добавляет приемник потока, который содержит все свойства закодированного потока.</span><span class="sxs-lookup"><span data-stu-id="ab5d6-140">For each stream in the profile that the ContentInfo object is aware of, the ASF file sink creates and adds a stream sink that contains all the properties of the encoded stream.</span></span> <span data-ttu-id="ab5d6-141">Приемник файлов ASF предназначен для хранения фиксированных потоков.</span><span class="sxs-lookup"><span data-stu-id="ab5d6-141">The ASF file sink is designed to contain fixed streams.</span></span> <span data-ttu-id="ab5d6-142">Это означает, что нельзя добавлять или удалять потоки путем вызова [**имфмедиасинк:: аддстреамсинк**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink) или [**Имфмедиасинк:: ремовестреамсинк**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-removestreamsink).</span><span class="sxs-lookup"><span data-stu-id="ab5d6-142">This means that you cannot add or remove streams by calling [**IMFMediaSink::AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink) or [**IMFMediaSink::RemoveStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-removestreamsink).</span></span> <span data-ttu-id="ab5d6-143">Эти вызовы в приемнике файлов завершаются с \_ \_ \_ фиксированным кодом ошибки MF E стреамсинкс.</span><span class="sxs-lookup"><span data-stu-id="ab5d6-143">These calls on the file sink fail with the MF\_E\_STREAMSINKS\_FIXED error code.</span></span> <span data-ttu-id="ab5d6-144">Добавление или удаление потоков в профиле не приводит к автоматическому добавлению или удалению приемников потоков в приемнике файлов.</span><span class="sxs-lookup"><span data-stu-id="ab5d6-144">Adding or removing streams in the profile does not automatically add or remove the stream sinks in the file sink.</span></span> <span data-ttu-id="ab5d6-145">Необходимо удалить существующий экземпляр файла и повторно создать его со сведениями о новом потоке, если потоки в профиле были изменены.</span><span class="sxs-lookup"><span data-stu-id="ab5d6-145">You must discard the existing instance of the file and recreate it with new stream information if your streams in the profile have changed.</span></span>

<span data-ttu-id="ab5d6-146">Следующая процедура обобщает общие шаги для перечисления приемников потоков в приемнике файлов ASF.</span><span class="sxs-lookup"><span data-stu-id="ab5d6-146">The following procedure summarizes the general steps for enumerating stream sinks in the ASF file sink.</span></span>

<span data-ttu-id="ab5d6-147">**Перечисление приемников потоков**</span><span class="sxs-lookup"><span data-stu-id="ab5d6-147">**To enumerate stream sinks**</span></span>

1.  <span data-ttu-id="ab5d6-148">Вызовите [**имфмедиасинк:: жетстреамсинккаунт**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkcount) , чтобы получить общее число приемников потоков в приемнике файлов ASF.</span><span class="sxs-lookup"><span data-stu-id="ab5d6-148">Call [**IMFMediaSink::GetStreamSinkCount**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkcount) to get the total number of stream sinks in the ASF file sink.</span></span>
2.  <span data-ttu-id="ab5d6-149">Пройдите через приемники потоков, Энг получить ссылку на интерфейс [**жетстреамсинкбиндекс**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyindex) приемника потока.</span><span class="sxs-lookup"><span data-stu-id="ab5d6-149">Loop through the stream sinks ang get a reference to the stream sink's [**GetStreamSinkByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyindex) interface.</span></span>

    <span data-ttu-id="ab5d6-150">-или-</span><span class="sxs-lookup"><span data-stu-id="ab5d6-150">-or-</span></span>

    <span data-ttu-id="ab5d6-151">Вызовите метод [**имфмедиасинк:: жетстреамсинкбид**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyid) , чтобы получить приемник потока, указав номер потока.</span><span class="sxs-lookup"><span data-stu-id="ab5d6-151">Call [**IMFMediaSink::GetStreamSinkById**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyid) to get the stream sink by specifying the stream number.</span></span> <span data-ttu-id="ab5d6-152">Каждый приемник потока определяется номером потока, установленным при создании потока в профиле.</span><span class="sxs-lookup"><span data-stu-id="ab5d6-152">Each stream sink is identified with the stream number you set while creating the stream in the profile.</span></span>

<span data-ttu-id="ab5d6-153">При создании частичной топологии для кодирования файла мультимедиа необходимо добавить приемник файла в топологию в качестве узла выходной топологии.</span><span class="sxs-lookup"><span data-stu-id="ab5d6-153">If you are building a partial topology for encoding a media file, you must add the file sink to the topology as an output topology node.</span></span> <span data-ttu-id="ab5d6-154">Это можно сделать, указав каждый приемник Steam в приемнике файлов или установив объект активации приемника файла и идентификаторы приемника потока.</span><span class="sxs-lookup"><span data-stu-id="ab5d6-154">You can do so either by specifying each steam sink in the file sink or by setting the file sink activation object and the stream sink identifiers.</span></span> <span data-ttu-id="ab5d6-155">Дополнительные сведения и пример кода см. в разделе [Создание выходных узлов](creating-output-nodes.md).</span><span class="sxs-lookup"><span data-stu-id="ab5d6-155">For more information and code example, see [Creating Output Nodes](creating-output-nodes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ab5d6-156">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="ab5d6-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ab5d6-157">Приемники мультимедиа ASF</span><span class="sxs-lookup"><span data-stu-id="ab5d6-157">ASF Media Sinks</span></span>](asf-media-sinks.md)
</dt> <dt>

[<span data-ttu-id="ab5d6-158">Поддержка ASF в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ab5d6-158">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 




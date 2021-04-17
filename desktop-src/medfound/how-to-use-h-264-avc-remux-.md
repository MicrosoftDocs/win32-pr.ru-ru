---
description: В этом разделе описывается, когда и как использовать приемника файлов H. 264/AVC Ремукс в формате MFT и MP4.
ms.assetid: 1DD236D9-775B-4417-BC49-BF52A6B3C8AD
title: Когда и как использовать H. 264/AVC Ремукс MFT и Sink MP4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 132c582fa16eae56c4fec8809caa4bd501469e16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105702120"
---
# <a name="when-and-how-to-use-h264avc-remux-mft-and-mp4-sink"></a><span data-ttu-id="ea105-103">Когда и как использовать H. 264/AVC Ремукс MFT и Sink MP4</span><span class="sxs-lookup"><span data-stu-id="ea105-103">When and How to Use H.264/AVC Remux MFT and MP4 Sink</span></span>

<span data-ttu-id="ea105-104">В этом разделе описывается, когда и как использовать приемника файлов H. 264/AVC Ремукс в формате MFT и MP4.</span><span class="sxs-lookup"><span data-stu-id="ea105-104">This topic describes when and how to use a H.264/AVC Remux MFT and MP4 Sink.</span></span>

## <a name="when-to-use-h264avc-remux-mft"></a><span data-ttu-id="ea105-105">Когда следует использовать таблицу MFT Ремукс в H. 264/AVC</span><span class="sxs-lookup"><span data-stu-id="ea105-105">When to use H.264/AVC Remux MFT</span></span>

<span data-ttu-id="ea105-106">Формат файла MPEG-4 требует, чтобы каждый сжатый пример содержал один основной рисунок с числом NAL-единиц в правильном порядке.</span><span class="sxs-lookup"><span data-stu-id="ea105-106">MPEG-4 file format requires that each compressed sample contains one primary picture with NAL units in the correct order.</span></span> <span data-ttu-id="ea105-107">(См. Описание основного и обязательного порядка NAL-единиц в разделе 7.4.1.2.3, **порядок NAL-единиц и кодированных изображений и ассоциаций с единицами доступа** в спецификации H. 264 AVC.) Также требуется, чтобы каждый сжатый пример был связан с меткой времени презентации, отметкой времени декодирования и длительностью выборки.</span><span class="sxs-lookup"><span data-stu-id="ea105-107">(Please refer to the definition of primary picture and mandatory NAL units order in section 7.4.1.2.3, **Order of NAL units and coded pictures and association to access units**, of the H.264 AVC specification.) It also requires each compressed sample is associated with a presentation time stamp, decoding time stamp, and sample duration.</span></span>

<span data-ttu-id="ea105-108">Во многих случаях, когда приложениям нужно записывать видео H. 264/AVC в контейнер файлов MPEG-4, сжатый пример может не удовлетворять приведенным выше требованиям.</span><span class="sxs-lookup"><span data-stu-id="ea105-108">In many scenarios when applications need to record H.264/AVC video in a MPEG-4 file container, the compressed sample may not satisfy the above requirements.</span></span> <span data-ttu-id="ea105-109">Например, один сжатый пример может не содержать полного основного изображения или иметь соответствующую метку времени презентации.</span><span class="sxs-lookup"><span data-stu-id="ea105-109">For example, one compressed sample might not contain a complete primary picture or might not have a correct presentation time stamp associated with it.</span></span> <span data-ttu-id="ea105-110">Вот несколько примеров приложений:</span><span class="sxs-lookup"><span data-stu-id="ea105-110">A few application examples are:</span></span>

-   <span data-ttu-id="ea105-111">Запись в файл звукозаписи H. 264/AVC — простейшее видео в контейнер файлов MPEG-4.</span><span class="sxs-lookup"><span data-stu-id="ea105-111">Write H.264/AVC streaming elementary video into MPEG-4 file container.</span></span>
-   <span data-ttu-id="ea105-112">Запись о камере, записанной камерой H. 264/AVC (простейшее видео в контейнере файлов MPEG-4).</span><span class="sxs-lookup"><span data-stu-id="ea105-112">Record camera captured H.264/AVC elementary video in MPEG-4 file container.</span></span>
-   <span data-ttu-id="ea105-113">Запись видео о видеоконференции H. 264/AVC в контейнере файлов MPEG-4.</span><span class="sxs-lookup"><span data-stu-id="ea105-113">Record H.264/AVC video conference in MPEG-4 file container.</span></span>
-   <span data-ttu-id="ea105-114">Объединение двух видео в формате H. 264/AVC в MPEG-2 TS или MP4 и запись в контейнер файлов MPEG-4 с правильными штампами времени.</span><span class="sxs-lookup"><span data-stu-id="ea105-114">Concatenate two H.264/AVC video in MPEG-2 TS or MP4 and write into MPEG-4 file container with correct time stamps.</span></span>
-   <span data-ttu-id="ea105-115">Ремукс H. 264/AVC Video из формата файлов АВЧД, MPEG-2 TS/PS в формат файлов MPEG-4.</span><span class="sxs-lookup"><span data-stu-id="ea105-115">Remux H.264/AVC video from AVCHD, MPEG-2 TS/PS file format to MPEG-4 file format.</span></span>
-   <span data-ttu-id="ea105-116">Обрезать видеофайл H. 264/AVC без перекодирования.</span><span class="sxs-lookup"><span data-stu-id="ea105-116">Trim H.264/AVC video file without transcoding.</span></span>

<span data-ttu-id="ea105-117">В этом случае приложению необходимо использовать файл MFT ремукс. 264/AVC для преобразования сжатых образцов, не содержащих полного основного изображения, перед их записью в контейнер файлов MPEG-4.</span><span class="sxs-lookup"><span data-stu-id="ea105-117">In this situation, the application needs to use a H.264/AVC remux MFT to convert the compressed samples not containing a complete primary picture before they are written into the MPEG-4 file container.</span></span>

## <a name="how-to-use-h264avc-remux-mft-and-mp4-sink"></a><span data-ttu-id="ea105-118">Как использовать H. 264/AVC Ремукс MFT и Sink MP4</span><span class="sxs-lookup"><span data-stu-id="ea105-118">How to use H.264/AVC Remux MFT and MP4 sink</span></span>

<span data-ttu-id="ea105-119">Задайте для параметра Тип выходного носителя источника значение **мфвидеоформат \_ H264 Single bitrate \_ ES**, указывающее, что каждый пример может не содержать полного основного изображения.</span><span class="sxs-lookup"><span data-stu-id="ea105-119">Set the source output media type to **MFVideoFormat\_H264\_ES**, which indicates each sample might not contain a complete primary picture.</span></span> <span data-ttu-id="ea105-120">Задайте тип входного носителя для приемника MP4 в **мфвидеоформат \_ H264 Single bitrate**.</span><span class="sxs-lookup"><span data-stu-id="ea105-120">Set the input media type of MP4 sink to **MFVideoFormat\_H264**.</span></span> <span data-ttu-id="ea105-121">Таким образом, тип входного носителя MFT ремукс. 264/AVC — **мфвидеоформат \_ H264 Single bitrate \_ ES** , а тип выходных данных — **264 \_ ремукс**, который будет автоматически вставлен в сопоставитель топологии.</span><span class="sxs-lookup"><span data-stu-id="ea105-121">So, the input media type of the H.264/AVC remux MFT is **MFVideoFormat\_H264\_ES** and the output media type of the H.264/AVC remux MFT is **MFVideoFormat\_H264**, which will be automatically inserted into the topology resolver.</span></span>

<span data-ttu-id="ea105-122">Длительность выборки игнорируется с помощью H. 264/AVC ремукс, так как время выборки для образца, не содержащего полное основное изображение, не имеет ясного значения.</span><span class="sxs-lookup"><span data-stu-id="ea105-122">Sample duration is ignored by the H.264/AVC remux, because the sample duration for a sample not containing a complete primary picture does not have clear meaning.</span></span> <span data-ttu-id="ea105-123">Вместо этого длительность выборки вычисляется по частоте кадров.</span><span class="sxs-lookup"><span data-stu-id="ea105-123">Instead, the sample duration is calculated from the frame rate.</span></span> <span data-ttu-id="ea105-124">Частота кадров вычисляется на основе параметра Sequence.</span><span class="sxs-lookup"><span data-stu-id="ea105-124">The frame rate is calculated from the sequence parameter.</span></span> <span data-ttu-id="ea105-125">Если сведения не существуют в параметре последовательности, частота кадров вычисляется на основе параметров входного типа носителя.</span><span class="sxs-lookup"><span data-stu-id="ea105-125">If the information does not exist in the sequence parameter, the frame rate is calculated from the parameters in the input media type.</span></span> <span data-ttu-id="ea105-126">Если сведения о частоте кадров недоступны, используется частота кадров по умолчанию 29,97 кадров/с.</span><span class="sxs-lookup"><span data-stu-id="ea105-126">If frame rate information is not available, the default frame rate of 29.97 fps is used.</span></span>

<span data-ttu-id="ea105-127">H. 264/AVC ремукс MFT линейно интерполирует метки времени декодирования для каждого сжатого изображения в соответствии с частотой кадров.</span><span class="sxs-lookup"><span data-stu-id="ea105-127">H.264/AVC remux MFT linearly interpolates the decoding time stamps (DTS) for each compressed picture according to the frame rate.</span></span> <span data-ttu-id="ea105-128">H. 264/AVC ремукс MFT учитывает метки времени входной презентации (PTS) во входных примерах и передает их в выходные данные, если они существуют.</span><span class="sxs-lookup"><span data-stu-id="ea105-128">H.264/AVC remux MFT honors the input presentation time stamps (PTS) in input samples and passes them to the output if they exist.</span></span> <span data-ttu-id="ea105-129">Он выполняет PTS интерполяцию в соответствии с частотой кадров, предыдущим PTS и порядком вывода изображения через декодированный процесс буферизации изображений (DBP), как указано в **приложении C. 4.5.3 процесс поднятия** в спецификации H. 264 AVC.</span><span class="sxs-lookup"><span data-stu-id="ea105-129">It performs PTS interpolation according to frame rate, the previous PTS, and the picture output order through Decoded Picture Buffering (DBP) bumping process as specified in **Annex C.4.5.3 Bumping process** of the H.264 AVC specification.</span></span> <span data-ttu-id="ea105-130">Каждый пример выходных данных из файла MFT в таблице H. 264/AVC ремукс должен иметь PTS, DTS и длительность выборки.</span><span class="sxs-lookup"><span data-stu-id="ea105-130">Each output sample from the H.264/AVC remux MFT shall have PTS, DTS, and sample duration.</span></span> <span data-ttu-id="ea105-131">H. 264/AVC ремукс MFT также определяет изображения IDR в битовый поток и задает их как чистую точку с помощью атрибута MF [мфсампликстенсион \_ клеанпоинт](mfsampleextension-cleanpoint-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="ea105-131">H.264/AVC remux MFT also identifies the IDR pictures in the bitstream and sets them as clean point with the MF attribute of [MFSampleExtension\_CleanPoint](mfsampleextension-cleanpoint-attribute.md).</span></span>

<span data-ttu-id="ea105-132">В настоящее время Таблица MFT ремукс. 264/AVC может поддерживать не более 64 переупорядоченных кадров.</span><span class="sxs-lookup"><span data-stu-id="ea105-132">Currently the H.264/AVC remux MFT can handle a maximum of 64 reordered frame.</span></span> <span data-ttu-id="ea105-133">Если число переупорядоченных кадров превышает 64 с выходным кадром долгосрочной ссылки, то MFT ремукс. 264/AVC будет интерполирует неверное PTS для этого кадра и выводит кадр в неправильное время.</span><span class="sxs-lookup"><span data-stu-id="ea105-133">If the number of reordered frame exceeds 64 with a long term reference frame present, the H.264/AVC remux MFT will interpolate a wrong PTS for that frame and output that frame at a wrong time.</span></span>

<span data-ttu-id="ea105-134">Чтобы создать экземпляр файла MFT ремукс в формате H. 264/AVC, задайте правильные типы входных и выходных данных в MFT-файле H. 264/AVC ремукс, задайте тип входного носителя для приемника MP4 и устраните топологию.</span><span class="sxs-lookup"><span data-stu-id="ea105-134">To instantiate a H.264/AVC remux MFT, set the correct input and output media types on the H.264/AVC remux MFT, set the input media type for the MP4 sink, and resolve the topology.</span></span>

<span data-ttu-id="ea105-135">В следующем примере кода показано, как инициализировать журнал MFT. 264/AVC ремукс и приемник MP4.</span><span class="sxs-lookup"><span data-stu-id="ea105-135">The following sample code show how to initialize the H.264/AVC remux MFT and MP4 sink.</span></span>

<span data-ttu-id="ea105-136">Для H. 264/AVC ремукс MFT</span><span class="sxs-lookup"><span data-stu-id="ea105-136">For H.264/AVC remux MFT,</span></span>


```C++
hr = CoCreateInstance(
            CLSID_CMSH264RemuxMFT,
            NULL,
            CLSCTX_INPROC_SERVER,
            IID_IMFTransform,
            (void**) &pIMFTransform
            );
```



<span data-ttu-id="ea105-137">Никакая дополнительная настройка не требуется.</span><span class="sxs-lookup"><span data-stu-id="ea105-137">No further configuration is necessary.</span></span>

<span data-ttu-id="ea105-138">Для приемника MP4</span><span class="sxs-lookup"><span data-stu-id="ea105-138">For MP4 sink,</span></span>


```C++
IMFByteStream*  pMFBSOutputFile = NULL;
hr = MFCreateFile(
    MF_ACCESSMODE_READWRITE,
    MF_OPENMODE_DELETE_IF_EXIST,
    MF_FILEFLAGS_NONE,
    m_pszOutputFile,
    &pMFBSOutputFile);
if(FAILED(hr))
{
    Log(L"ERROR>> Failed to create output file for MP4 Sink (hr=0x%x)", hr);
    break;
}

hr = MFCreateMPEG4MediaSink(
    pMFBSOutputFile,
    (guidMajorType == MFMediaType_Video) ? pMediaType : NULL,  // pMediaType comes from the output type of the remux MFT
    (guidMajorType == MFMediaType_Audio) ? pMediaType : NULL,
    &m_pMediaSink);
if(FAILED(hr))
{
    Log(L"ERROR>> Failed to create MP4 Sink (hr=0x%x)", hr);
    break;
}
hr = m_pMediaSink->GetStreamSinkByIndex(0, &pStream);
```



## <a name="related-topics"></a><span data-ttu-id="ea105-139">См. также</span><span class="sxs-lookup"><span data-stu-id="ea105-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea105-140">Поддерживаемые форматы мультимедиа в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ea105-140">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 




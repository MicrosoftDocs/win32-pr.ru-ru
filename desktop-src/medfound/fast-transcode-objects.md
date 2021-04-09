---
description: В этом разделе описано, как использовать API перекодировки для кодирования файла мультимедиа.
ms.assetid: 52b27359-b319-41a0-88e8-d23567420e92
title: Использование API перекодирования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bb97dd61ef75e71a82b522b65b682f861022bcf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143108"
---
# <a name="using-the-transcode-api"></a><span data-ttu-id="1efdb-103">Использование API перекодирования</span><span class="sxs-lookup"><span data-stu-id="1efdb-103">Using the Transcode API</span></span>

<span data-ttu-id="1efdb-104">В этом разделе описано, как использовать API перекодировки для кодирования файла мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="1efdb-104">This topic described how to use the transcode API to encode a media file.</span></span>

-   [<span data-ttu-id="1efdb-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="1efdb-105">Overview</span></span>](#overview)
-   [<span data-ttu-id="1efdb-106">Создание источника мультимедиа</span><span class="sxs-lookup"><span data-stu-id="1efdb-106">Creating a Media Source</span></span>](#creating-a-media-source)
-   [<span data-ttu-id="1efdb-107">Создание профиля перекодирования</span><span class="sxs-lookup"><span data-stu-id="1efdb-107">Creating a Transcode Profile</span></span>](#creating-a-transcode-profile)
    -   [<span data-ttu-id="1efdb-108">Атрибуты звука</span><span class="sxs-lookup"><span data-stu-id="1efdb-108">Audio Attributes</span></span>](#audio-attributes)
    -   [<span data-ttu-id="1efdb-109">Атрибуты видео</span><span class="sxs-lookup"><span data-stu-id="1efdb-109">Video Attributes</span></span>](#video-attributes)
    -   [<span data-ttu-id="1efdb-110">Атрибуты контейнера</span><span class="sxs-lookup"><span data-stu-id="1efdb-110">Container Attributes</span></span>](#container-attributes)
-   [<span data-ttu-id="1efdb-111">Создание топологии перекодирования</span><span class="sxs-lookup"><span data-stu-id="1efdb-111">Creating a Transcode Topology</span></span>](#creating-a-transcode-topology)
-   [<span data-ttu-id="1efdb-112">Выполнение сеанса кодирования</span><span class="sxs-lookup"><span data-stu-id="1efdb-112">Running the Encoding Session</span></span>](#running-the-encoding-session)
-   [<span data-ttu-id="1efdb-113">См. также</span><span class="sxs-lookup"><span data-stu-id="1efdb-113">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="1efdb-114">Обзор</span><span class="sxs-lookup"><span data-stu-id="1efdb-114">Overview</span></span>

<span data-ttu-id="1efdb-115">Перед использованием API перекодирования приложение должно иметь следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="1efdb-115">Before using the transcode API, the application must have the following pieces of information:</span></span>

-   <span data-ttu-id="1efdb-116">Путь или URL-адрес существующего файла мультимедиа, который будет зашифрован повторно.</span><span class="sxs-lookup"><span data-stu-id="1efdb-116">The path or URL to an existing media file that will be re-encoded.</span></span>
-   <span data-ttu-id="1efdb-117">Имя выходного файла.</span><span class="sxs-lookup"><span data-stu-id="1efdb-117">The name of the output file.</span></span>
-   <span data-ttu-id="1efdb-118">Тип контейнера для выходного файла, например MP4 или Advanced Streaming Format (ASF).</span><span class="sxs-lookup"><span data-stu-id="1efdb-118">The container type for the output file, such as MP4 or Advanced Streaming Format (ASF).</span></span>
-   <span data-ttu-id="1efdb-119">Формат кодировки параметра.</span><span class="sxs-lookup"><span data-stu-id="1efdb-119">The encoding format.</span></span> <span data-ttu-id="1efdb-120">Эти сведения включают в себя типы носителей, описывающие закодированные аудио и видеопотоки.</span><span class="sxs-lookup"><span data-stu-id="1efdb-120">This information includes the media types that describe the encoded audio and video streams.</span></span>

<span data-ttu-id="1efdb-121">Чтобы использовать API перекодирования, приложение выполняет следующие действия.</span><span class="sxs-lookup"><span data-stu-id="1efdb-121">To use the transcode API, an application performs the following steps.</span></span>

1.  <span data-ttu-id="1efdb-122">Создайте источник мультимедиа для чтения исходного файла.</span><span class="sxs-lookup"><span data-stu-id="1efdb-122">Create a media source to read the source file.</span></span>
2.  <span data-ttu-id="1efdb-123">Создайте профиль перекодирования.</span><span class="sxs-lookup"><span data-stu-id="1efdb-123">Create a transcode profile.</span></span> <span data-ttu-id="1efdb-124">Добавьте атрибуты, описывающие аудиопоток, поток видео и контейнер файлов.</span><span class="sxs-lookup"><span data-stu-id="1efdb-124">Add attributes that describe the audio stream, video stream, and file container.</span></span>
3.  <span data-ttu-id="1efdb-125">Используйте профиль перекодировки для создания топологии кодирования.</span><span class="sxs-lookup"><span data-stu-id="1efdb-125">Use the transcode profile to create an encoding topology.</span></span> <span data-ttu-id="1efdb-126">(Дополнительные сведения о топологиях см. в разделе [о топологиях](about-topologies.md).)</span><span class="sxs-lookup"><span data-stu-id="1efdb-126">(For more information about topologies, see [About Topologies](about-topologies.md).)</span></span>
4.  <span data-ttu-id="1efdb-127">Задайте топологию для [сеанса мультимедиа](media-session.md).</span><span class="sxs-lookup"><span data-stu-id="1efdb-127">Set the topology on the [Media Session](media-session.md).</span></span>
5.  <span data-ttu-id="1efdb-128">Запустите сеанс мультимедиа и дождитесь события [месессионендед](mesessionended.md) .</span><span class="sxs-lookup"><span data-stu-id="1efdb-128">Start the Media Session and wait for the [MESessionEnded](mesessionended.md) event.</span></span>

<span data-ttu-id="1efdb-129">В оставшейся части этого раздела эти действия описаны более подробно.</span><span class="sxs-lookup"><span data-stu-id="1efdb-129">The remainder of this topic describes these steps in more detail.</span></span>

## <a name="creating-a-media-source"></a><span data-ttu-id="1efdb-130">Создание источника мультимедиа</span><span class="sxs-lookup"><span data-stu-id="1efdb-130">Creating a Media Source</span></span>

<span data-ttu-id="1efdb-131">Источник мультимедиа — это объект, который считывает и анализирует исходный файл.</span><span class="sxs-lookup"><span data-stu-id="1efdb-131">A media source is an object that reads and parses the source file.</span></span> <span data-ttu-id="1efdb-132">Чтобы создать источник мультимедиа, используйте [сопоставитель источника](source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="1efdb-132">To create a media source, use the [Source Resolver](source-resolver.md).</span></span> <span data-ttu-id="1efdb-133">Пример кода можно найти в разделе [Использование сопоставителя источников](using-the-source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="1efdb-133">You can find example code in the topic [Using the Source Resolver](using-the-source-resolver.md).</span></span>

## <a name="creating-a-transcode-profile"></a><span data-ttu-id="1efdb-134">Создание профиля перекодирования</span><span class="sxs-lookup"><span data-stu-id="1efdb-134">Creating a Transcode Profile</span></span>

<span data-ttu-id="1efdb-135">*Профиль* перекодировки описывает формат и параметры, используемые для кодирования выходного файла.</span><span class="sxs-lookup"><span data-stu-id="1efdb-135">A *transcode profile* describes the format and settings that are used to encode the output file.</span></span> <span data-ttu-id="1efdb-136">Профиль перекодировки содержит три набора атрибутов:</span><span class="sxs-lookup"><span data-stu-id="1efdb-136">The transcode profile contains three sets of attributes:</span></span>

-   <span data-ttu-id="1efdb-137">Атрибуты аудио: Опишите целевой формат аудио и параметры звукового кодировщика.</span><span class="sxs-lookup"><span data-stu-id="1efdb-137">Audio attributes: Describe the target audio format and audio encoder settings.</span></span>
-   <span data-ttu-id="1efdb-138">Атрибуты видео: Опишите целевой формат видео и параметры кодировщика видео.</span><span class="sxs-lookup"><span data-stu-id="1efdb-138">Video attributes: Describe the target video format and video encoder settings.</span></span>
-   <span data-ttu-id="1efdb-139">Атрибуты контейнера: Определите тип контейнера файлов, а также некоторые глобальные параметры кодирования.</span><span class="sxs-lookup"><span data-stu-id="1efdb-139">Container attributes: Define the type of file container, as well as some global encoding settings.</span></span>

<span data-ttu-id="1efdb-140">Чтобы создать профиль перекодирования, вызовите функцию [**мфкреатетранскодепрофиле**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) .</span><span class="sxs-lookup"><span data-stu-id="1efdb-140">To create a transcode profile, call the [**MFCreateTranscodeProfile**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) function.</span></span> <span data-ttu-id="1efdb-141">Эта функция возвращает указатель на интерфейс [**имфтранскодепрофиле**](/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile) .</span><span class="sxs-lookup"><span data-stu-id="1efdb-141">This function returns a pointer to the [**IMFTranscodeProfile**](/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile) interface.</span></span> <span data-ttu-id="1efdb-142">Исходный объект профиля пуст; Он не содержит атрибутов.</span><span class="sxs-lookup"><span data-stu-id="1efdb-142">The initial profile object is empty; it contains no attributes.</span></span> <span data-ttu-id="1efdb-143">Следующим шагом является добавление атрибутов, определяющих профиль.</span><span class="sxs-lookup"><span data-stu-id="1efdb-143">The next step is to add the attributes that define the profile.</span></span>

### <a name="audio-attributes"></a><span data-ttu-id="1efdb-144">Атрибуты звука</span><span class="sxs-lookup"><span data-stu-id="1efdb-144">Audio Attributes</span></span>

<span data-ttu-id="1efdb-145">Чтобы добавить атрибуты для аудиопотока, вызовите метод [**имфтранскодепрофиле:: сетаудиоаттрибутес**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes).</span><span class="sxs-lookup"><span data-stu-id="1efdb-145">To add attributes for the audio stream, call [**IMFTranscodeProfile::SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes).</span></span> <span data-ttu-id="1efdb-146">Эти атрибуты указывают, как кодируется звуковой поток.</span><span class="sxs-lookup"><span data-stu-id="1efdb-146">These attributes specify how the audio stream is encoded.</span></span> <span data-ttu-id="1efdb-147">Если выходной файл не будет содержать аудиопоток, пропустите эти атрибуты.</span><span class="sxs-lookup"><span data-stu-id="1efdb-147">If the output file will not contain an audio stream, omit these attributes.</span></span>

<span data-ttu-id="1efdb-148">Атрибуты аудио делятся на две категории:</span><span class="sxs-lookup"><span data-stu-id="1efdb-148">Audio attributes fall into two categories:</span></span>

-   <span data-ttu-id="1efdb-149">Атрибуты, определяющие формат закодированного потока</span><span class="sxs-lookup"><span data-stu-id="1efdb-149">Attributes that specify the format of the encoded stream</span></span>
-   <span data-ttu-id="1efdb-150">Атрибуты, задающих другие параметры кодировки.</span><span class="sxs-lookup"><span data-stu-id="1efdb-150">Attributes that specify other encoding parameters.</span></span>

<span data-ttu-id="1efdb-151">Атрибуты формата — это просто атрибуты типа мультимедиа, как описано в разделе [типы аудио мультимедиа](audio-media-types.md).</span><span class="sxs-lookup"><span data-stu-id="1efdb-151">Format attributes are simply media-type attributes, as described in the section [Audio Media Types](audio-media-types.md).</span></span> <span data-ttu-id="1efdb-152">Точный набор атрибутов формата зависит от кодировщика.</span><span class="sxs-lookup"><span data-stu-id="1efdb-152">The exact set of format attributes depends on the encoder.</span></span> <span data-ttu-id="1efdb-153">(См. раздел [Поддерживаемые форматы мультимедиа в Media Foundation](supported-media-formats-in-media-foundation.md).) Ниже приведен список типовых атрибутов звукового формата.</span><span class="sxs-lookup"><span data-stu-id="1efdb-153">(See [Supported Media Formats in Media Foundation](supported-media-formats-in-media-foundation.md).) Here is a list of typical audio format attributes:</span></span>



| <span data-ttu-id="1efdb-154">Атрибут Format</span><span class="sxs-lookup"><span data-stu-id="1efdb-154">Format Attribute</span></span>                                                                         | <span data-ttu-id="1efdb-155">Описание</span><span class="sxs-lookup"><span data-stu-id="1efdb-155">Description</span></span>                                                      |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="1efdb-156">подтип MF \_ MT \_</span><span class="sxs-lookup"><span data-stu-id="1efdb-156">MF\_MT\_SUBTYPE</span></span>](mf-mt-subtype-attribute.md)                                           | <span data-ttu-id="1efdb-157">Подтип.</span><span class="sxs-lookup"><span data-stu-id="1efdb-157">The subtype.</span></span> <span data-ttu-id="1efdb-158">См. раздел [идентификаторы GUID для звуковых подтипов](audio-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="1efdb-158">See [Audio Subtype GUIDs](audio-subtype-guids.md).</span></span> |
| [<span data-ttu-id="1efdb-159">\_ \_ каналы аудиосигнала MF MT \_ \_</span><span class="sxs-lookup"><span data-stu-id="1efdb-159">MF\_MT\_AUDIO\_NUM\_CHANNELS</span></span>](mf-mt-audio-num-channels-attribute.md)                   | <span data-ttu-id="1efdb-160">Число звуковых каналов.</span><span class="sxs-lookup"><span data-stu-id="1efdb-160">The number of audio channels.</span></span>                                    |
| [<span data-ttu-id="1efdb-161">\_ \_ звуковых образцов MF MT \_ \_ в \_ секунду</span><span class="sxs-lookup"><span data-stu-id="1efdb-161">MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND</span></span>](mf-mt-audio-samples-per-second-attribute.md)      | <span data-ttu-id="1efdb-162">Количество звуковых выборок в секунду.</span><span class="sxs-lookup"><span data-stu-id="1efdb-162">The number of audio samples per second.</span></span>                          |
| [<span data-ttu-id="1efdb-163">\_ \_ Выравнивание звукового \_ блока MF MT \_</span><span class="sxs-lookup"><span data-stu-id="1efdb-163">MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT</span></span>](mf-mt-audio-block-alignment-attribute.md)             | <span data-ttu-id="1efdb-164">Выравнивание блока.</span><span class="sxs-lookup"><span data-stu-id="1efdb-164">The block alignment.</span></span>                                             |
| [<span data-ttu-id="1efdb-165">\_ \_ \_ Среднее \_ число байт \_ в секунду для \_ звука MF MT</span><span class="sxs-lookup"><span data-stu-id="1efdb-165">MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md) | <span data-ttu-id="1efdb-166">Среднее число байтов в секунду (закодированная скорость).</span><span class="sxs-lookup"><span data-stu-id="1efdb-166">The average number of bytes per second (the encoded bit rate).</span></span>   |



 

<span data-ttu-id="1efdb-167">Определены следующие параметры кодировки.</span><span class="sxs-lookup"><span data-stu-id="1efdb-167">The following encoding parameters are defined.</span></span>



| <span data-ttu-id="1efdb-168">Параметр Encoding</span><span class="sxs-lookup"><span data-stu-id="1efdb-168">Encoding Parameter</span></span>                                                             | <span data-ttu-id="1efdb-169">Описание</span><span class="sxs-lookup"><span data-stu-id="1efdb-169">Description</span></span>                                                                |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="1efdb-170">\_ \_ не разграниченияая \_ Вставка \_ кодировщика MF</span><span class="sxs-lookup"><span data-stu-id="1efdb-170">MF\_TRANSCODE\_DONOT\_INSERT\_ENCODER</span></span>](mf-transcode-donot-insert-encoder.md) | <span data-ttu-id="1efdb-171">Предотвращает вставку кодировщиком звукового потока в API-интерфейсе перекодировки.</span><span class="sxs-lookup"><span data-stu-id="1efdb-171">Prevents the transcode API from inserting an encoder for the audio stream.</span></span> |
| [<span data-ttu-id="1efdb-172">MF \_ \_ енкодингпрофиле</span><span class="sxs-lookup"><span data-stu-id="1efdb-172">MF\_TRANSCODE\_ENCODINGPROFILE</span></span>](mf-transcode-encodingprofile.md)             | <span data-ttu-id="1efdb-173">Указывает шаблон соответствия устройства.</span><span class="sxs-lookup"><span data-stu-id="1efdb-173">Specifies the device conformance template.</span></span> <span data-ttu-id="1efdb-174">(Применяется только к файлам ASF.)</span><span class="sxs-lookup"><span data-stu-id="1efdb-174">(Applies only to ASF files.)</span></span>    |
| [<span data-ttu-id="1efdb-175">MF \_ \_ куалитивсспид</span><span class="sxs-lookup"><span data-stu-id="1efdb-175">MF\_TRANSCODE\_QUALITYVSSPEED</span></span>](mf-transcode-qualityvsspeed.md)               | <span data-ttu-id="1efdb-176">Задает компромисс между качеством кодирования и скоростью.</span><span class="sxs-lookup"><span data-stu-id="1efdb-176">Specifies the trade-off between encoding quality and speed.</span></span>                |



 

<span data-ttu-id="1efdb-177">Необходимо задать атрибуты формата.</span><span class="sxs-lookup"><span data-stu-id="1efdb-177">You must set the format attributes.</span></span> <span data-ttu-id="1efdb-178">Параметры кодировки необязательны.</span><span class="sxs-lookup"><span data-stu-id="1efdb-178">The encoding parameters are optional.</span></span>

<span data-ttu-id="1efdb-179">Один из способов найти формат, совместимый с кодировщиком, — вызвать функцию [**мфтранскодежетаудиуутпутаваилаблетипес**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) .</span><span class="sxs-lookup"><span data-stu-id="1efdb-179">One way to find a format that is compatible with the encoder is to call the [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) function.</span></span> <span data-ttu-id="1efdb-180">Требуемый кодировщик указывается подтипом.</span><span class="sxs-lookup"><span data-stu-id="1efdb-180">The desired encoder is specified by subtype.</span></span> <span data-ttu-id="1efdb-181">Функция возвращает коллекцию типов мультимедиа для этого кодировщика.</span><span class="sxs-lookup"><span data-stu-id="1efdb-181">The function returns a collection of media types for that encoder.</span></span> <span data-ttu-id="1efdb-182">Можно выбрать тип из списка и скопировать атрибуты в профиль.</span><span class="sxs-lookup"><span data-stu-id="1efdb-182">You can select a type from the list and copy the attributes to the profile.</span></span> <span data-ttu-id="1efdb-183">Пример кода, в котором используется такой подход, см. [в разделе Учебник. кодирование WMA-файла](tutorial--converting-an-mp3-file-to-a-wma-file.md).</span><span class="sxs-lookup"><span data-stu-id="1efdb-183">For example code that uses this approach, see [Tutorial: Encoding a WMA File](tutorial--converting-an-mp3-file-to-a-wma-file.md).</span></span>

### <a name="video-attributes"></a><span data-ttu-id="1efdb-184">Атрибуты видео</span><span class="sxs-lookup"><span data-stu-id="1efdb-184">Video Attributes</span></span>

<span data-ttu-id="1efdb-185">Чтобы добавить атрибуты для видеопотока, вызовите метод [**имфтранскодепрофиле:: сетвидеоаттрибутес**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes).</span><span class="sxs-lookup"><span data-stu-id="1efdb-185">To add attributes for the video stream, call [**IMFTranscodeProfile::SetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes).</span></span> <span data-ttu-id="1efdb-186">Эти атрибуты указывают, как кодируется поток видео.</span><span class="sxs-lookup"><span data-stu-id="1efdb-186">These attributes specify how the video stream is encoded.</span></span> <span data-ttu-id="1efdb-187">Если выходной файл не будет содержать поток видео, пропустите эти атрибуты.</span><span class="sxs-lookup"><span data-stu-id="1efdb-187">If the output file will not contain a video stream, omit these attributes.</span></span>

<span data-ttu-id="1efdb-188">Как и в случае с звуковыми атрибутами, атрибуты видео делятся на две категории:</span><span class="sxs-lookup"><span data-stu-id="1efdb-188">As with audio attributes, the video attributes fall into two categories:</span></span>

-   <span data-ttu-id="1efdb-189">Атрибуты, определяющие формат закодированного потока</span><span class="sxs-lookup"><span data-stu-id="1efdb-189">Attributes that specify the format of the encoded stream</span></span>
-   <span data-ttu-id="1efdb-190">Атрибуты, задающих другие параметры кодировки.</span><span class="sxs-lookup"><span data-stu-id="1efdb-190">Attributes that specify other encoding parameters.</span></span>

<span data-ttu-id="1efdb-191">Атрибуты формата — это атрибуты типа мультимедиа, как описано в разделе [типы](video-media-types.md)видеоклипов.</span><span class="sxs-lookup"><span data-stu-id="1efdb-191">Format attributes are media-type attributes, as described in the section [Video Media Types](video-media-types.md).</span></span> <span data-ttu-id="1efdb-192">Ниже приведен список стандартных атрибутов формата видео.</span><span class="sxs-lookup"><span data-stu-id="1efdb-192">Here is a list of typical video format attributes:</span></span>



| <span data-ttu-id="1efdb-193">Атрибут Format</span><span class="sxs-lookup"><span data-stu-id="1efdb-193">Format Attribute</span></span>                                                       | <span data-ttu-id="1efdb-194">Описание</span><span class="sxs-lookup"><span data-stu-id="1efdb-194">Description</span></span>                                                      |
|------------------------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="1efdb-195">подтип MF \_ MT \_</span><span class="sxs-lookup"><span data-stu-id="1efdb-195">MF\_MT\_SUBTYPE</span></span>](mf-mt-subtype-attribute.md)                         | <span data-ttu-id="1efdb-196">Подтип.</span><span class="sxs-lookup"><span data-stu-id="1efdb-196">The subtype.</span></span> <span data-ttu-id="1efdb-197">См. раздел [GUID подтипа видео](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="1efdb-197">See [Video Subtype GUIDs](video-subtype-guids.md).</span></span> |
| [<span data-ttu-id="1efdb-198">\_ \_ Частота кадров MF \_ MT</span><span class="sxs-lookup"><span data-stu-id="1efdb-198">MF\_MT\_FRAME\_RATE</span></span>](mf-mt-frame-rate-attribute.md)                  | <span data-ttu-id="1efdb-199">Частота кадров.</span><span class="sxs-lookup"><span data-stu-id="1efdb-199">The frame rate.</span></span>                                                  |
| [<span data-ttu-id="1efdb-200">\_ \_ Размер пакета MF \_ MT</span><span class="sxs-lookup"><span data-stu-id="1efdb-200">MF\_MT\_FRAME\_SIZE</span></span>](mf-mt-frame-size-attribute.md)                  | <span data-ttu-id="1efdb-201">Размер кадра.</span><span class="sxs-lookup"><span data-stu-id="1efdb-201">The frame size.</span></span>                                                  |
| [<span data-ttu-id="1efdb-202">**\_ \_ Средняя скорость MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="1efdb-202">**MF\_MT\_AVG\_BITRATE**</span></span>](mf-mt-avg-bitrate-attribute.md)            | <span data-ttu-id="1efdb-203">Средняя скорость потока.</span><span class="sxs-lookup"><span data-stu-id="1efdb-203">The average bit rate.</span></span>                                            |
| [<span data-ttu-id="1efdb-204">пропорции MF \_ MT \_ пикселей \_ \_</span><span class="sxs-lookup"><span data-stu-id="1efdb-204">MF\_MT\_PIXEL\_ASPECT\_RATIO</span></span>](mf-mt-pixel-aspect-ratio-attribute.md) | <span data-ttu-id="1efdb-205">Пропорция в пикселях.</span><span class="sxs-lookup"><span data-stu-id="1efdb-205">The pixel aspect ratio.</span></span>                                          |



 

<span data-ttu-id="1efdb-206">Определены следующие параметры кодировки.</span><span class="sxs-lookup"><span data-stu-id="1efdb-206">The following encoding parameters are defined.</span></span>



| <span data-ttu-id="1efdb-207">Параметр Encoding</span><span class="sxs-lookup"><span data-stu-id="1efdb-207">Encoding Parameter</span></span>                                                             | <span data-ttu-id="1efdb-208">Описание</span><span class="sxs-lookup"><span data-stu-id="1efdb-208">Description</span></span>                                                                |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="1efdb-209">\_ \_ не разграниченияая \_ Вставка \_ кодировщика MF</span><span class="sxs-lookup"><span data-stu-id="1efdb-209">MF\_TRANSCODE\_DONOT\_INSERT\_ENCODER</span></span>](mf-transcode-donot-insert-encoder.md) | <span data-ttu-id="1efdb-210">Предотвращает вставку кодировщика для видеопотока API перекодировки.</span><span class="sxs-lookup"><span data-stu-id="1efdb-210">Prevents the transcode API from inserting an encoder for the video stream.</span></span> |
| [<span data-ttu-id="1efdb-211">MF \_ \_ енкодингпрофиле</span><span class="sxs-lookup"><span data-stu-id="1efdb-211">MF\_TRANSCODE\_ENCODINGPROFILE</span></span>](mf-transcode-encodingprofile.md)             | <span data-ttu-id="1efdb-212">Указывает шаблон соответствия устройства.</span><span class="sxs-lookup"><span data-stu-id="1efdb-212">Specifies the device conformance template.</span></span> <span data-ttu-id="1efdb-213">(Применяется только к файлам ASF.)</span><span class="sxs-lookup"><span data-stu-id="1efdb-213">(Applies only to ASF files.)</span></span>    |
| [<span data-ttu-id="1efdb-214">MF \_ \_ куалитивсспид</span><span class="sxs-lookup"><span data-stu-id="1efdb-214">MF\_TRANSCODE\_QUALITYVSSPEED</span></span>](mf-transcode-qualityvsspeed.md)               | <span data-ttu-id="1efdb-215">Задает компромисс между качеством кодирования и скоростью.</span><span class="sxs-lookup"><span data-stu-id="1efdb-215">Specifies the trade-off between encoding quality and speed.</span></span>                |



 

<span data-ttu-id="1efdb-216">Необходимо задать атрибуты формата.</span><span class="sxs-lookup"><span data-stu-id="1efdb-216">You must set the format attributes.</span></span> <span data-ttu-id="1efdb-217">Параметры кодировки необязательны.</span><span class="sxs-lookup"><span data-stu-id="1efdb-217">The encoding parameters are optional.</span></span>

### <a name="container-attributes"></a><span data-ttu-id="1efdb-218">Атрибуты контейнера</span><span class="sxs-lookup"><span data-stu-id="1efdb-218">Container Attributes</span></span>

<span data-ttu-id="1efdb-219">Атрибуты контейнера определяют характеристики уровня файла выходного файла.</span><span class="sxs-lookup"><span data-stu-id="1efdb-219">Container attributes define file-level characteristics of the output file.</span></span> <span data-ttu-id="1efdb-220">Чтобы задать атрибуты контейнера, вызовите метод [**имфтранскодепрофиле:: сетконтаинераттрибутес**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes).</span><span class="sxs-lookup"><span data-stu-id="1efdb-220">To set container attributes, call [**IMFTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes).</span></span> <span data-ttu-id="1efdb-221">Определены следующие атрибуты.</span><span class="sxs-lookup"><span data-stu-id="1efdb-221">The following attributes are defined.</span></span>



| <span data-ttu-id="1efdb-222">attribute</span><span class="sxs-lookup"><span data-stu-id="1efdb-222">Attribute</span></span>                                                                          | <span data-ttu-id="1efdb-223">Описание</span><span class="sxs-lookup"><span data-stu-id="1efdb-223">Description</span></span>                                                                                                                                            |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1efdb-224">\_ \_ Настройка профиля для ПЕРЕкодирования MF \_</span><span class="sxs-lookup"><span data-stu-id="1efdb-224">MF\_TRANSCODE\_ADJUST\_PROFILE</span></span>](mf-transcode-adjust-profile.md)                  | <span data-ttu-id="1efdb-225">Определяет параметры потока, используемые для топологии перекодирования.</span><span class="sxs-lookup"><span data-stu-id="1efdb-225">Defines the stream settings to use for the transcode topology.</span></span> <span data-ttu-id="1efdb-226">Можно установить флаги для использования параметров источника входных данных или использовать пользовательские атрибуты потока.</span><span class="sxs-lookup"><span data-stu-id="1efdb-226">You can set the flags to use the input source settings or use custom stream attributes.</span></span> |
| [<span data-ttu-id="1efdb-227">MF \_ \_ контаинертипе</span><span class="sxs-lookup"><span data-stu-id="1efdb-227">MF\_TRANSCODE\_CONTAINERTYPE</span></span>](mf-transcode-containertype.md)                     | <span data-ttu-id="1efdb-228">Задает формат выходного файла, например MP4 или ASF.</span><span class="sxs-lookup"><span data-stu-id="1efdb-228">Specifies the file format of the output file, such as MP4 or ASF.</span></span> <span data-ttu-id="1efdb-229">На основе этого значения в топологию добавляется соответствующий приемник носителя.</span><span class="sxs-lookup"><span data-stu-id="1efdb-229">Based on this value, the appropriate media sink is added to the topology.</span></span>            |
| [<span data-ttu-id="1efdb-230">\_код MF \_ пропустить \_ перенос метаданных \_</span><span class="sxs-lookup"><span data-stu-id="1efdb-230">MF\_TRANSCODE\_SKIP\_METADATA\_TRANSFER</span></span>](mf-transcode-skip-metadata-transfer.md) | <span data-ttu-id="1efdb-231">Указывает, копируются ли метаданные из источника в выходной файл.</span><span class="sxs-lookup"><span data-stu-id="1efdb-231">Specifies whether metadata from the source is copied to the output file.</span></span>                                                                               |
| [<span data-ttu-id="1efdb-232">MF \_ \_ топологимоде</span><span class="sxs-lookup"><span data-stu-id="1efdb-232">MF\_TRANSCODE\_TOPOLOGYMODE</span></span>](mf-transcode-topologymode.md)                       | <span data-ttu-id="1efdb-233">Указывает, можно ли использовать аппаратные кодеки при кодировании.</span><span class="sxs-lookup"><span data-stu-id="1efdb-233">Specifies whether hardware-based codecs may be used during transcoding.</span></span>                                                                                |
| [<span data-ttu-id="1efdb-234">\_Атрибут MFT фиелдофусе \_ Unlock \_</span><span class="sxs-lookup"><span data-stu-id="1efdb-234">MFT\_FIELDOFUSE\_UNLOCK\_Attribute</span></span>](mft-fieldofuse-unlock-attribute.md)          | <span data-ttu-id="1efdb-235">Разблокирует кодек с ограничениями на использование полей.</span><span class="sxs-lookup"><span data-stu-id="1efdb-235">Unlocks a codec that has field-of-use restrictions.</span></span> <span data-ttu-id="1efdb-236">Дополнительные сведения см. в разделе [ограничения использования](field-of-use-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="1efdb-236">For more information, see [Field of Use Restrictions](field-of-use-restrictions.md).</span></span>              |



 

<span data-ttu-id="1efdb-237">Требуется [атрибут \_ \_ КОНТАИНЕРТИПЕ для перекодирования MF](mf-transcode-containertype.md) .</span><span class="sxs-lookup"><span data-stu-id="1efdb-237">The [MF\_TRANSCODE\_CONTAINERTYPE](mf-transcode-containertype.md) attribute is required.</span></span> <span data-ttu-id="1efdb-238">Другие атрибуты контейнера являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="1efdb-238">The other container attributes are optional.</span></span>

## <a name="creating-a-transcode-topology"></a><span data-ttu-id="1efdb-239">Создание топологии перекодирования</span><span class="sxs-lookup"><span data-stu-id="1efdb-239">Creating a Transcode Topology</span></span>

<span data-ttu-id="1efdb-240">Топология перекодирования — это частичная топология, которая содержит источник мультимедиа, соответствующие кодеки и приемник мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="1efdb-240">The transcode topology is a partial topology that contains the media source, the appropriate codecs, and the media sink.</span></span> <span data-ttu-id="1efdb-241">Чтобы создать топологию перекодирования, вызовите функцию [**мфкреатетранскодетопологи**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) .</span><span class="sxs-lookup"><span data-stu-id="1efdb-241">To create the transcode topology, call to the [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) function.</span></span> <span data-ttu-id="1efdb-242">Эта функция принимает в качестве входных данных следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="1efdb-242">This function takes the following parameters as input:</span></span>

-   <span data-ttu-id="1efdb-243">Указатель на интерфейс [**имфмедиасаурце**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="1efdb-243">A pointer to the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface of the media source.</span></span>
-   <span data-ttu-id="1efdb-244">Имя выходного файла.</span><span class="sxs-lookup"><span data-stu-id="1efdb-244">The name of the output file.</span></span>
-   <span data-ttu-id="1efdb-245">Указатель на интерфейс [**имфтранскодепрофиле**](/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile) профиля перекодирования.</span><span class="sxs-lookup"><span data-stu-id="1efdb-245">A pointer to the [**IMFTranscodeProfile**](/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile) interface of the transcode profile.</span></span>

<span data-ttu-id="1efdb-246">Функция возвращает указатель на интерфейс [**имфтопологи**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) .</span><span class="sxs-lookup"><span data-stu-id="1efdb-246">The function returns a pointer to the [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) interface.</span></span>

## <a name="running-the-encoding-session"></a><span data-ttu-id="1efdb-247">Выполнение сеанса кодирования</span><span class="sxs-lookup"><span data-stu-id="1efdb-247">Running the Encoding Session</span></span>

<span data-ttu-id="1efdb-248">После создания топологии можно приступать к кодированию файла.</span><span class="sxs-lookup"><span data-stu-id="1efdb-248">After you create the topology, you are ready to encode the file.</span></span> <span data-ttu-id="1efdb-249">На этом этапе профиль можно отменить.</span><span class="sxs-lookup"><span data-stu-id="1efdb-249">You can discard the profile at this point.</span></span>

1.  <span data-ttu-id="1efdb-250">Вызовите [**мфкреатемедиасессион**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) , чтобы создать сеанс мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="1efdb-250">Call [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) to create the Media Session.</span></span>
2.  <span data-ttu-id="1efdb-251">Вызовите [**имфмедиасессион:: сеттопологи**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) , чтобы задать топологию для сеанса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="1efdb-251">Call [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) to set the topology on the Media Session.</span></span>
3.  <span data-ttu-id="1efdb-252">Вызовите метод [**имфмедиасессион:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) , чтобы начать сеанс кодирования.</span><span class="sxs-lookup"><span data-stu-id="1efdb-252">Call [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) to start the encoding session.</span></span>
4.  <span data-ttu-id="1efdb-253">Дождитесь события [месессионендед](mesessionended.md) .</span><span class="sxs-lookup"><span data-stu-id="1efdb-253">Wait for the [MESessionEnded](mesessionended.md) event.</span></span>
5.  <span data-ttu-id="1efdb-254">Вызовите метод [**имфмедиасессион:: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) , чтобы закрыть сеанс мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="1efdb-254">Call [**IMFMediaSession::Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) to close the Media Session.</span></span>
6.  <span data-ttu-id="1efdb-255">Дождитесь события [месессионклосед](mesessionclosed.md) .</span><span class="sxs-lookup"><span data-stu-id="1efdb-255">Wait for the [MESessionClosed](mesessionclosed.md) event.</span></span>
7.  <span data-ttu-id="1efdb-256">Вызов [**имфмедиасаурце:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).</span><span class="sxs-lookup"><span data-stu-id="1efdb-256">Call [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).</span></span>
8.  <span data-ttu-id="1efdb-257">Вызов [**имфмедиасессион:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).</span><span class="sxs-lookup"><span data-stu-id="1efdb-257">Call [**IMFMediaSession::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).</span></span>

<span data-ttu-id="1efdb-258">Большая часть времени, затраченного на кодирование, выполняется между шагами 3 и 4.</span><span class="sxs-lookup"><span data-stu-id="1efdb-258">Most of the time spent encoding occurs between steps 3 and 4.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1efdb-259">См. также</span><span class="sxs-lookup"><span data-stu-id="1efdb-259">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1efdb-260">API перекодирования</span><span class="sxs-lookup"><span data-stu-id="1efdb-260">Transcode API</span></span>](transcode-api.md)
</dt> <dt>

[<span data-ttu-id="1efdb-261">Сведения о сеансе мультимедиа</span><span class="sxs-lookup"><span data-stu-id="1efdb-261">About the Media Session</span></span>](about-the-media-session.md)
</dt> </dl>

 

 




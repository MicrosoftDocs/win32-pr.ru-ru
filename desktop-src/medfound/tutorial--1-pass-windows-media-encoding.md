---
description: Кодирование означает процесс преобразования цифрового мультимедиа из одного формата в другой. Например, преобразование MP3 Audio в формат Windows Media Audio в соответствии со спецификацией ASF.
ms.assetid: 4fe202d8-c8f5-4e9a-ad40-1aea8f767362
title: Учебник. 1. Передача кодирования мультимедиа Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d670b107f315966a048a2f847183431f9a57bd4
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "103820301"
---
# <a name="tutorial-1-pass-windows-media-encoding"></a><span data-ttu-id="753a2-104">Учебник. 1. Передача кодирования мультимедиа Windows</span><span class="sxs-lookup"><span data-stu-id="753a2-104">Tutorial: 1-Pass Windows Media Encoding</span></span>

<span data-ttu-id="753a2-105">Кодирование означает процесс преобразования цифрового мультимедиа из одного формата в другой.</span><span class="sxs-lookup"><span data-stu-id="753a2-105">Encoding refers to the process of converting digital media from one format into another.</span></span> <span data-ttu-id="753a2-106">Например, преобразование MP3 Audio в формат Windows Media Audio в соответствии со спецификацией ASF.</span><span class="sxs-lookup"><span data-stu-id="753a2-106">For example, converting MP3 audio into Windows Media Audio format as defined by the Advanced Systems Format (ASF) specification.</span></span>

<span data-ttu-id="753a2-107">**Примечание**  .  Спецификация ASF определяет тип контейнера для выходного файла (. WMA или. wmv), который может содержать данные мультимедиа в любом формате, сжатом или несжатом.</span><span class="sxs-lookup"><span data-stu-id="753a2-107">**Note**  The ASF specification defines a container type for the output file (.wma or .wmv) that can contain media data in any format, compressed or uncompressed.</span></span> <span data-ttu-id="753a2-108">Например, контейнер ASF, такой как WMA-файл, может содержать данные мультимедиа в формате MP3.</span><span class="sxs-lookup"><span data-stu-id="753a2-108">For example, an ASF container such as a .wma file can contain media data in MP3 format.</span></span> <span data-ttu-id="753a2-109">Процесс кодирования преобразует фактический формат данных, содержащихся в файле.</span><span class="sxs-lookup"><span data-stu-id="753a2-109">The encoding process converts the actual format of the data contained within the file.</span></span>

<span data-ttu-id="753a2-110">В этом руководстве демонстрируется кодирование источника входных данных (без защиты от DRM) в содержимое Windows Media и запись их в новый файл ASF (. WM \* ) с использованием компонентов ASF уровня конвейера.</span><span class="sxs-lookup"><span data-stu-id="753a2-110">This tutorial demonstrates encoding clear content (non DRM-protected) input source into Windows Media content and writing the data in a new ASF file (.wm\*) by using Pipeline Layer ASF Components.</span></span> <span data-ttu-id="753a2-111">Эти компоненты будут использоваться для создания топологии с частичным кодированием, которая будет управляться экземпляром сеанса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="753a2-111">These components will be used to build a partial encoding topology, which will be controlled by an instance of the Media Session.</span></span>

<span data-ttu-id="753a2-112">В этом руководстве вы создадите консольное приложение, которое принимает входные и выходные имена файлов, а также режим кодирования в качестве аргументов.</span><span class="sxs-lookup"><span data-stu-id="753a2-112">In this tutorial, you will create a console application that takes the input and output filenames, and the encoding mode as arguments.</span></span> <span data-ttu-id="753a2-113">Входной файл может находиться в сжатом или несжатом формате носителя.</span><span class="sxs-lookup"><span data-stu-id="753a2-113">The input file can be in a compressed or an uncompressed media format.</span></span> <span data-ttu-id="753a2-114">Допустимыми режимами кодирования являются "CBR" (Постоянная скорость потока) или "VBR" (переменная скорость).</span><span class="sxs-lookup"><span data-stu-id="753a2-114">The valid encoding modes are "CBR" (constant bit rate) or "VBR" (variable bit rate).</span></span> <span data-ttu-id="753a2-115">Приложение создает источник мультимедиа, который представляет источник, указанный в имени входного файла, и приемник ASF-файлов для архивации закодированного содержимого исходного файла в ASF-файл.</span><span class="sxs-lookup"><span data-stu-id="753a2-115">The application creates a media source to represent the source specified by the input filename, and the ASF file sink to archive the encoded contents of source file into an ASF file.</span></span> <span data-ttu-id="753a2-116">Чтобы обеспечить простоту реализации сценария, выходной файл будет иметь только один звуковой поток и один поток видео.</span><span class="sxs-lookup"><span data-stu-id="753a2-116">To keep the scenario simple to implement, the output file will have only one audio stream and one video stream.</span></span> <span data-ttu-id="753a2-117">Приложение вставляет кодек Windows Media Audio 9,1 Professional для преобразования формата звукового потока и кодек Windows Media Video 9 для видеопотока.</span><span class="sxs-lookup"><span data-stu-id="753a2-117">The application inserts the Windows Media Audio 9.1 Professional codec for the audio stream format conversion and Windows Media Video 9 codec for the video stream.</span></span>

<span data-ttu-id="753a2-118">Для кодирования постоянной скорости потока перед началом сеанса кодирования кодировщику необходимо указать целевую скорость, которую он должен достичь.</span><span class="sxs-lookup"><span data-stu-id="753a2-118">For constant bit rate encoding, before the encoding session begins, the encoder must know the target bit rate that it must achieve.</span></span> <span data-ttu-id="753a2-119">В этом руководстве для режима "CBR" приложение использует скорость потока, доступную в первом выходном типе носителя, который извлекается из кодировщика во время согласования типа носителя в качестве целевой скорости.</span><span class="sxs-lookup"><span data-stu-id="753a2-119">In this tutorial, for "CBR" mode, the application uses the bit rate available with the first output media type that is retrieved from the encoder during media type negotiation as the target bit rate.</span></span> <span data-ttu-id="753a2-120">В этом учебнике в этом руководстве демонстрируется кодирование с переменной скоростью, задавая уровень качества.</span><span class="sxs-lookup"><span data-stu-id="753a2-120">For variable bit rate encoding, this tutorial demonstrates encoding with variable bit rate by setting a quality level.</span></span> <span data-ttu-id="753a2-121">Звуковые потоки кодируются на уровне качества 98 и видеопотоков на уровне качества 95.</span><span class="sxs-lookup"><span data-stu-id="753a2-121">The audio streams are encoded at the quality level of 98 and video streams at the quality level of 95.</span></span>

<span data-ttu-id="753a2-122">Следующая процедура описывает действия по кодированию содержимого мультимедиа Windows в контейнере ASF с помощью 1-проходного режима кодирования.</span><span class="sxs-lookup"><span data-stu-id="753a2-122">The following procedure summarizes the steps for encoding Windows Media content in an ASF container by using a 1-pass encoding mode.</span></span>

1.  <span data-ttu-id="753a2-123">Создайте источник мультимедиа для указанного с помощью сопоставителя источников.</span><span class="sxs-lookup"><span data-stu-id="753a2-123">Create a media source for the specified by using the source resolver.</span></span>
2.  <span data-ttu-id="753a2-124">Перечисление потоков в источнике мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="753a2-124">Enumerate the streams in the media source.</span></span>
3.  <span data-ttu-id="753a2-125">Создайте приемник мультимедиа ASF и добавьте приемники потоков в зависимости от потоков в источнике носителя, который необходимо закодировать.</span><span class="sxs-lookup"><span data-stu-id="753a2-125">Create the ASF media sink and add stream sinks depending on the streams in the media source that need to be encoded.</span></span>
4.  <span data-ttu-id="753a2-126">Настройте приемник мультимедиа с требуемыми свойствами кодировки.</span><span class="sxs-lookup"><span data-stu-id="753a2-126">Configure the media sink with the required encoding properties.</span></span>
5.  <span data-ttu-id="753a2-127">Создайте кодировщики Windows Media для потоков в выходном файле.</span><span class="sxs-lookup"><span data-stu-id="753a2-127">Create the Windows Media encoders for the streams in the output file.</span></span>
6.  <span data-ttu-id="753a2-128">Настройте кодировщики с помощью свойств, установленных в приемнике мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="753a2-128">Configure the encoders with the properties that are set on the media sink.</span></span>
7.  <span data-ttu-id="753a2-129">Создайте неполную топологию кодирования.</span><span class="sxs-lookup"><span data-stu-id="753a2-129">Build a partial encoding topology.</span></span>
8.  <span data-ttu-id="753a2-130">Создайте экземпляр сеанса мультимедиа и задайте топологию для сеанса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="753a2-130">Instantiate the Media Session and set the topology on the Media Session.</span></span>
9.  <span data-ttu-id="753a2-131">Запустите сеанс кодирования, управляя сеансом мультимедиа и получением всех соответствующих событий из сеанса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="753a2-131">Start the encoding session by controlling the Media Session and getting all the relevant events from the Media Session.</span></span>
10. <span data-ttu-id="753a2-132">Для кодирования VBR получите значения свойств кодировки из кодировщика и задайте их в приемнике мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="753a2-132">For VBR encoding, get the encoding property values from the encoder and set them on the media sink.</span></span>
11. <span data-ttu-id="753a2-133">Закройте и завершите сеанс кодирования.</span><span class="sxs-lookup"><span data-stu-id="753a2-133">Close and shutdown the encoding session.</span></span>

<span data-ttu-id="753a2-134">Этот учебник содержит следующие подразделы:</span><span class="sxs-lookup"><span data-stu-id="753a2-134">This tutorial contains the following sections:</span></span>

-   [<span data-ttu-id="753a2-135">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="753a2-135">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="753a2-136">Настройка проекта</span><span class="sxs-lookup"><span data-stu-id="753a2-136">Set up the Project</span></span>](#set-up-the-project)
-   [<span data-ttu-id="753a2-137">Создание источника мультимедиа</span><span class="sxs-lookup"><span data-stu-id="753a2-137">Create the Media Source</span></span>](#create-the-media-source)
-   [<span data-ttu-id="753a2-138">Создание приемника файлов ASF</span><span class="sxs-lookup"><span data-stu-id="753a2-138">Create the ASF File Sink</span></span>](#create-the-asf-file-sink)
    -   [<span data-ttu-id="753a2-139">Создание объекта профиля ASF</span><span class="sxs-lookup"><span data-stu-id="753a2-139">Create the ASF Profile Object</span></span>](#create-the-asf-profile-object)
    -   [<span data-ttu-id="753a2-140">Создание типа сжатого звукового носителя</span><span class="sxs-lookup"><span data-stu-id="753a2-140">Create a Compressed Audio Media Type</span></span>](#create-a-compressed-audio-media-type)
    -   [<span data-ttu-id="753a2-141">Создание типа носителя с сжатым видео</span><span class="sxs-lookup"><span data-stu-id="753a2-141">Create a Compressed Video Media Type</span></span>](#create-a-compressed-video-media-type)
    -   [<span data-ttu-id="753a2-142">Создание объекта Контентинфо ASF</span><span class="sxs-lookup"><span data-stu-id="753a2-142">Create the ASF ContentInfo Object</span></span>](#create-the-asf-contentinfo-object)
    -   [<span data-ttu-id="753a2-143">Создание приемника файлов ASF</span><span class="sxs-lookup"><span data-stu-id="753a2-143">Create the ASF File Sink</span></span>](#create-the-asf-file-sink)
-   [<span data-ttu-id="753a2-144">Создание топологии частичной кодировки</span><span class="sxs-lookup"><span data-stu-id="753a2-144">Build the Partial Encoding Topology</span></span>](#build-the-partial-encoding-topology)
    -   [<span data-ttu-id="753a2-145">Создание исходного узла топологии для источника мультимедиа</span><span class="sxs-lookup"><span data-stu-id="753a2-145">Create the Source Topology Node for the Media Source</span></span>](#create-the-source-topology-node-for-the-media-source)
    -   [<span data-ttu-id="753a2-146">Создайте экземпляры требуемых кодировщиков и создавайте узлы преобразования.</span><span class="sxs-lookup"><span data-stu-id="753a2-146">Instantiate the Required Encoders and Create the Transform Nodes</span></span>](#instantiate-the-required-encoders-and-create-the-transform-nodes)
    -   [<span data-ttu-id="753a2-147">Создание выходных узлов топологии для приемника файлов</span><span class="sxs-lookup"><span data-stu-id="753a2-147">Create the Output Topology Nodes for the File Sink</span></span>](#create-the-output-topology-nodes-for-the-file-sink)
    -   [<span data-ttu-id="753a2-148">Подключение узлов источника, преобразования и приемника</span><span class="sxs-lookup"><span data-stu-id="753a2-148">Connect the Source, Transform, and Sink Nodes</span></span>](#connect-the-source-transform-and-sink-nodes)
-   [<span data-ttu-id="753a2-149">Обработка сеанса кодирования</span><span class="sxs-lookup"><span data-stu-id="753a2-149">Handling the Encoding Session</span></span>](#handling-the-encoding-session)
-   [<span data-ttu-id="753a2-150">Обновление свойств кодировки в приемнике файла</span><span class="sxs-lookup"><span data-stu-id="753a2-150">Update Encoding Properties in the File Sink</span></span>](#update-encoding-properties-in-the-file-sink)
-   [<span data-ttu-id="753a2-151">Реализация Main</span><span class="sxs-lookup"><span data-stu-id="753a2-151">Implement Main</span></span>](#implement-main)
-   [<span data-ttu-id="753a2-152">Проверка выходного файла</span><span class="sxs-lookup"><span data-stu-id="753a2-152">Test the Output File</span></span>](#test-the-output-file)
-   [<span data-ttu-id="753a2-153">Распространенные коды ошибок и советы по отладке</span><span class="sxs-lookup"><span data-stu-id="753a2-153">Common Error Codes and Debugging Tips</span></span>](#common-error-codes-and-debugging-tips)
-   [<span data-ttu-id="753a2-154">См. также</span><span class="sxs-lookup"><span data-stu-id="753a2-154">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="753a2-155">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="753a2-155">Prerequisites</span></span>

<span data-ttu-id="753a2-156">В этом учебнике предполагается следующее:</span><span class="sxs-lookup"><span data-stu-id="753a2-156">This tutorial assumes the following:</span></span>

-   <span data-ttu-id="753a2-157">Вы знакомы со [структурой файлов ASF](asf-file-structure.md), [компоненты ASF уровня конвейера](pipeline-layer-asf-components.md) , предоставляемые Media Foundation для работы с объектами ASF.</span><span class="sxs-lookup"><span data-stu-id="753a2-157">You are familiar with the [ASF File Structure](asf-file-structure.md), the [Pipeline Layer ASF Components](pipeline-layer-asf-components.md) provided by Media Foundation to work with ASF Objects.</span></span> <span data-ttu-id="753a2-158">К этим компонентам относятся следующие объекты:</span><span class="sxs-lookup"><span data-stu-id="753a2-158">These components include the following objects:</span></span>
    -   [<span data-ttu-id="753a2-159">Источники мультимедиа</span><span class="sxs-lookup"><span data-stu-id="753a2-159">Media Sources</span></span>](media-sources.md)

        <span data-ttu-id="753a2-160">**Примечание**  .  Если вы выполняете преобразование (преобразуя файл более высокой разрядной скорости в файл с меньшей скоростью, не изменяя форматы), вы будете использовать [источник медиа ASF](asf-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="753a2-160">**Note**  If you are performing transrating (converting a higher bit-rate file to a lower bit-rate file without changing formats), you will use the [ASF Media Source](asf-media-source.md).</span></span>

    -   [<span data-ttu-id="753a2-161">Кодировщики Windows Media</span><span class="sxs-lookup"><span data-stu-id="753a2-161">Windows Media Encoders</span></span>](windows-media-encoders.md)
    -   [<span data-ttu-id="753a2-162">Приемники мультимедиа ASF</span><span class="sxs-lookup"><span data-stu-id="753a2-162">ASF Media Sinks</span></span>](asf-media-sinks.md)
    -   [<span data-ttu-id="753a2-163">Объект Контентинфо ASF</span><span class="sxs-lookup"><span data-stu-id="753a2-163">ASF ContentInfo Object</span></span>](asf-contentinfo-object.md)
    -   [<span data-ttu-id="753a2-164">Профиль ASF</span><span class="sxs-lookup"><span data-stu-id="753a2-164">ASF Profile</span></span>](asf-profile.md)

-   <span data-ttu-id="753a2-165">Вы знакомы с кодировщиками Windows Media, а также с различными типами кодировок, в частности с [постоянным кодированием битовой скорости](constant-bit-rate-encoding.md) и [кодированием битовой переменной на основе качества](quality-based-variable-bit-rate--vbr--encoding.md).</span><span class="sxs-lookup"><span data-stu-id="753a2-165">You are familiar with Windows Media encoders, and the various encoding types, particularly [Constant Bit Rate Encoding](constant-bit-rate-encoding.md) and [Quality-Based Variable Bit Rate Encoding](quality-based-variable-bit-rate--vbr--encoding.md).</span></span>
-   <span data-ttu-id="753a2-166">Вы знакомы с операциями MFT кодировщика.</span><span class="sxs-lookup"><span data-stu-id="753a2-166">You are familiar with encoder MFT operations.</span></span> <span data-ttu-id="753a2-167">В частности, создание экземпляра кодировщика и установка входных и выходных типов в кодировщике.</span><span class="sxs-lookup"><span data-stu-id="753a2-167">Specifically, creating an instance of the encoder and setting input and output types on the encoder.</span></span>
-   <span data-ttu-id="753a2-168">Вы знакомы с объектами топологии и созданием топологии кодирования.</span><span class="sxs-lookup"><span data-stu-id="753a2-168">You are familiar with topology objects and how to build an encoding topology.</span></span> <span data-ttu-id="753a2-169">Дополнительные сведения о топологиях и узлах топологии см. в разделе [Создание топологий](creating-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="753a2-169">For more information about topologies and topology nodes, see [Creating Topologies](creating-topologies.md).</span></span>
-   <span data-ttu-id="753a2-170">Вы знакомы с моделью событий [сеанса мультимедиа](media-session.md)и операциями управления потоком.</span><span class="sxs-lookup"><span data-stu-id="753a2-170">You are familiar with [Media Session](media-session.md)'s event model and the flow control operations.</span></span> <span data-ttu-id="753a2-171">Дополнительные сведения см. в разделе [события сеанса мультимедиа](media-session-events.md).</span><span class="sxs-lookup"><span data-stu-id="753a2-171">For information, see [Media Session Events](media-session-events.md).</span></span>

## <a name="set-up-the-project"></a><span data-ttu-id="753a2-172">Настройка проекта</span><span class="sxs-lookup"><span data-stu-id="753a2-172">Set up the Project</span></span>

1.  <span data-ttu-id="753a2-173">Включите в исходный файл следующие заголовки:</span><span class="sxs-lookup"><span data-stu-id="753a2-173">Include the following headers in your source file:</span></span>

    ```C++
    #include <new>
    #include <mfidl.h>            // Media Foundation interfaces
    #include <mfapi.h>            // Media Foundation platform APIs
    #include <mferror.h>        // Media Foundation error codes
    #include <wmcontainer.h>    // ASF-specific components
    #include <wmcodecdsp.h>        // Windows Media DSP interfaces
    #include <Dmo.h>            // DMO objects
    #include <uuids.h>            // Definition for FORMAT_VideoInfo
    #include <propvarutil.h>
    
    ```

    

2.  <span data-ttu-id="753a2-174">Ссылка на следующие файлы библиотеки:</span><span class="sxs-lookup"><span data-stu-id="753a2-174">Link to the following library files:</span></span>

    ```C++
    // The required link libraries 
    #pragma comment(lib, "mfplat")
    #pragma comment(lib, "mf")
    #pragma comment(lib, "mfuuid")
    #pragma comment(lib, "msdmo")
    #pragma comment(lib, "strmiids")
    #pragma comment(lib, "propsys")
    
    ```

    

3.  <span data-ttu-id="753a2-175">Объявите функцию [саферелеасе](saferelease.md) .</span><span class="sxs-lookup"><span data-stu-id="753a2-175">Declare the [SafeRelease](saferelease.md) function.</span></span>

    ```C++
    template <class T> void SafeRelease(T **ppT)
    {
        if (*ppT)
        {
            (*ppT)->Release();
            *ppT = NULL;
        }
    }
    ```

    

4.  <span data-ttu-id="753a2-176">Объявите \_ перечисление режима кодирования для определения типов кодирования CBR и VBR.</span><span class="sxs-lookup"><span data-stu-id="753a2-176">Declare the ENCODING\_MODE enumeration to define CBR and VBR encoding types.</span></span>

    ```C++
    // Encoding mode
    typedef enum ENCODING_MODE {
      NONE  = 0x00000000,
      CBR   = 0x00000001,
      VBR   = 0x00000002,
    } ;
    
    ```

    

5.  <span data-ttu-id="753a2-177">Определите константу окна буфера для видеопотока.</span><span class="sxs-lookup"><span data-stu-id="753a2-177">Define a constant for buffer window for a video stream.</span></span>

    ```C++
    // Video buffer window
    const INT32 VIDEO_WINDOW_MSEC = 3000;
    
    ```

    

## <a name="create-the-media-source"></a><span data-ttu-id="753a2-178">Создание источника мультимедиа</span><span class="sxs-lookup"><span data-stu-id="753a2-178">Create the Media Source</span></span>

<span data-ttu-id="753a2-179">Создайте источник носителя для источника входных данных.</span><span class="sxs-lookup"><span data-stu-id="753a2-179">Create a media source for the input source.</span></span> <span data-ttu-id="753a2-180">Media Foundation предоставляет встроенные источники мультимедиа для различных форматов мультимедиа: MP3, MP4/3GP, AVI/WAVE.</span><span class="sxs-lookup"><span data-stu-id="753a2-180">Media Foundation provides built-in media sources for various media formats: MP3, MP4/3GP, AVI/WAVE.</span></span> <span data-ttu-id="753a2-181">Сведения о форматах, поддерживаемых Media Foundation, см. [в разделе Поддерживаемые форматы мультимедиа в Media Foundation](supported-media-formats-in-media-foundation.md).</span><span class="sxs-lookup"><span data-stu-id="753a2-181">For information about the formats supported by Media Foundation, see [Supported Media Formats in Media Foundation](supported-media-formats-in-media-foundation.md).</span></span>

<span data-ttu-id="753a2-182">Чтобы создать источник мультимедиа, используйте [сопоставитель источника](source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="753a2-182">To create the media source, use the [Source Resolver](source-resolver.md).</span></span> <span data-ttu-id="753a2-183">Этот объект анализирует URL-адрес, указанный для исходного файла, и создает соответствующий источник мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="753a2-183">This object analyzes the URL that was specified for the source file and creates the appropriate media source.</span></span>

<span data-ttu-id="753a2-184">Выполните следующие вызовы:</span><span class="sxs-lookup"><span data-stu-id="753a2-184">Make the following calls:</span></span>

-   [<span data-ttu-id="753a2-185">**мфкреатесаурцересолвер**</span><span class="sxs-lookup"><span data-stu-id="753a2-185">**MFCreateSourceResolver**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesourceresolver)
-   [<span data-ttu-id="753a2-186">**Имфсаурцересолвер:: Креатеобжектфромурл**</span><span class="sxs-lookup"><span data-stu-id="753a2-186">**IMFSourceResolver::CreateObjectFromURL**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl)

    <span data-ttu-id="753a2-187">Дополнительные сведения об этих вызовах см. [в разделе Использование сопоставителя источников](using-the-source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="753a2-187">For more information about these calls, see [Using the Source Resolver](using-the-source-resolver.md).</span></span>

    <span data-ttu-id="753a2-188">Если входной файл имеет формат ASF и вы хотите преобразовать его в другой файл с битовой скоростью без изменения формата, то исходный поисковый компьютер создает экземпляр [источника мультимедиа ASF](asf-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="753a2-188">If your input file is in ASF format and you want to convert it to a different bit-rate file without changing formats, the source solver creates an instance of the [ASF Media Source](asf-media-source.md).</span></span>

<span data-ttu-id="753a2-189">В следующем примере кода показана функция Креатемедиасаурце, которая создает источник мультимедиа для указанного файла.</span><span class="sxs-lookup"><span data-stu-id="753a2-189">The following code example shows a function CreateMediaSource that creates a media source for the specified file.</span></span>


```C++
//  Create a media source from a URL.
HRESULT CreateMediaSource(PCWSTR sURL, IMFMediaSource **ppSource)
{
    MF_OBJECT_TYPE ObjectType = MF_OBJECT_INVALID;

    IMFSourceResolver* pSourceResolver = NULL;
    IUnknown* pSource = NULL;

    // Create the source resolver.
    HRESULT hr = MFCreateSourceResolver(&pSourceResolver);
    if (FAILED(hr))
    {
        goto done;
    }

    // Use the source resolver to create the media source.

    // Note: For simplicity this sample uses the synchronous method to create 
    // the media source. However, creating a media source can take a noticeable
    // amount of time, especially for a network source. For a more responsive 
    // UI, use the asynchronous BeginCreateObjectFromURL method.

    hr = pSourceResolver->CreateObjectFromURL(
        sURL,                       // URL of the source.
        MF_RESOLUTION_MEDIASOURCE,  // Create a source object.
        NULL,                       // Optional property store.
        &ObjectType,        // Receives the created object type. 
        &pSource            // Receives a pointer to the media source.
        );
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the IMFMediaSource interface from the media source.
    hr = pSource->QueryInterface(IID_PPV_ARGS(ppSource));

done:
    SafeRelease(&pSourceResolver);
    SafeRelease(&pSource);
    return hr;
}
```



## <a name="create-the-asf-file-sink"></a><span data-ttu-id="753a2-190">Создание приемника файлов ASF</span><span class="sxs-lookup"><span data-stu-id="753a2-190">Create the ASF File Sink</span></span>

<span data-ttu-id="753a2-191">Создайте экземпляр приемника файлов ASF, который будет архивировать закодированные данные мультимедиа в файл ASF в конце сеанса кодирования.</span><span class="sxs-lookup"><span data-stu-id="753a2-191">Create an instance of the ASF file sink that will archive encoded media data to an ASF file at the end of the encoding session.</span></span>

<span data-ttu-id="753a2-192">В этом руководстве вы создадите объект активации для приемника файлов ASF.</span><span class="sxs-lookup"><span data-stu-id="753a2-192">In this tutorial, you will create an activation object for the ASF file sink.</span></span> <span data-ttu-id="753a2-193">Чтобы создать необходимые приемники потоков, приемнику файла необходимы следующие сведения.</span><span class="sxs-lookup"><span data-stu-id="753a2-193">The file sink needs the following information in order to create the required stream sinks.</span></span>

-   <span data-ttu-id="753a2-194">Потоки, которые должны быть закодированы и записаны в окончательный файл.</span><span class="sxs-lookup"><span data-stu-id="753a2-194">The streams to be encoded and written in the final file.</span></span>
-   <span data-ttu-id="753a2-195">Свойства кодировки, используемые для кодирования мультимедийного содержимого, такие как тип кодирования, число проходов кодирования и связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="753a2-195">The encoding properties that are used to encode the media content, such as, type of encoding, number of encoding passes, and the related properties.</span></span>
-   <span data-ttu-id="753a2-196">Глобальные свойства файла, указывающие на приемник мультимедиа, следует ли автоматически настраивать параметры сегмента утечки (скорость и размер буфера).</span><span class="sxs-lookup"><span data-stu-id="753a2-196">The global file properties that indicate to the media sink whether it should adjust the leaky bucket parameters (bit rate and buffer size) automatically.</span></span>

<span data-ttu-id="753a2-197">Сведения о потоке настраиваются в объекте профиля ASF, а свойства Encoding и Global задаются в хранилище свойств, управляемом объектом ASF Контентинфо.</span><span class="sxs-lookup"><span data-stu-id="753a2-197">The stream information is configured in the ASF Profile object and the encoding and global properties are set in a property store managed by the ASF ContentInfo Object.</span></span>

<span data-ttu-id="753a2-198">Общие сведения о приемнике файлов ASF см. в статье [приемники мультимедиа ASF](asf-media-sinks.md).</span><span class="sxs-lookup"><span data-stu-id="753a2-198">For an overview of the ASF file sink, see [ASF Media Sinks](asf-media-sinks.md).</span></span>

### <a name="create-the-asf-profile-object"></a><span data-ttu-id="753a2-199">Создание объекта профиля ASF</span><span class="sxs-lookup"><span data-stu-id="753a2-199">Create the ASF Profile Object</span></span>

<span data-ttu-id="753a2-200">Чтобы приемник файлов ASF написал закодированные данные мультимедиа в файл ASF, приемнику необходимо получить сведения о количестве потоков и типе потоков, для которых создаются приемники потоков.</span><span class="sxs-lookup"><span data-stu-id="753a2-200">For the ASF file sink to write encoded media data into an ASF file, the sink needs to know the number of streams and the type of streams for which to create stream sinks.</span></span> <span data-ttu-id="753a2-201">В этом учебнике вы извлечете эти сведения из источника мультимедиа и создадите соответствующие выходные потоки.</span><span class="sxs-lookup"><span data-stu-id="753a2-201">In this tutorial you will extract that information from the media source and create corresponding output streams.</span></span> <span data-ttu-id="753a2-202">Ограничьте выходные потоки одним звуковым потоком и одним видеопотоком.</span><span class="sxs-lookup"><span data-stu-id="753a2-202">Restrict your output streams to one audio stream and one video stream.</span></span> <span data-ttu-id="753a2-203">Для каждого выбранного потока в источнике Создайте целевой поток и добавьте его в профиль.</span><span class="sxs-lookup"><span data-stu-id="753a2-203">For each selected stream in the source, create a target stream and add it to the profile.</span></span>

<span data-ttu-id="753a2-204">Для реализации этого шага необходимы следующие объекты.</span><span class="sxs-lookup"><span data-stu-id="753a2-204">To implement this step, you need the following objects.</span></span>

-   [<span data-ttu-id="753a2-205">Профиль ASF</span><span class="sxs-lookup"><span data-stu-id="753a2-205">ASF Profile</span></span>](asf-profile.md)
-   <span data-ttu-id="753a2-206">Дескриптор представления для источника мультимедиа</span><span class="sxs-lookup"><span data-stu-id="753a2-206">Presentation Descriptor for the media source</span></span>
-   <span data-ttu-id="753a2-207">Дескрипторы потоков для выбранных потоков в источнике мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="753a2-207">Stream descriptors for the selected streams in the media source.</span></span>
-   <span data-ttu-id="753a2-208">Типы носителей для выбранных потоков.</span><span class="sxs-lookup"><span data-stu-id="753a2-208">Media Types for the selected streams.</span></span>

<span data-ttu-id="753a2-209">Ниже описан процесс создания профиля ASF и целевых потоков.</span><span class="sxs-lookup"><span data-stu-id="753a2-209">The following steps describe the process of creating the ASF profile and the target streams.</span></span>

<span data-ttu-id="753a2-210">**Создание профиля ASF**</span><span class="sxs-lookup"><span data-stu-id="753a2-210">**To create the ASF profile**</span></span>

1.  <span data-ttu-id="753a2-211">Вызовите [**мфкреатеасфпрофиле**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) , чтобы создать пустой объект профиля.</span><span class="sxs-lookup"><span data-stu-id="753a2-211">Call [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) to create an empty profile object.</span></span>
2.  <span data-ttu-id="753a2-212">Вызовите [**имфмедиасаурце:: креатепресентатиондескриптор**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) , чтобы создать дескриптор представления для источника мультимедиа, созданного на шаге, описанном в разделе "Создание источника мультимедиа" этого руководства.</span><span class="sxs-lookup"><span data-stu-id="753a2-212">Call [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) to create the presentation descriptor for the media source created in the step described in the "Create the Media Source" section of this tutorial.</span></span>
3.  <span data-ttu-id="753a2-213">Вызовите [**имфпресентатиондескриптор:: жетстреамдескрипторкаунт**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount) , чтобы получить количество потоков в источнике мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="753a2-213">Call [**IMFPresentationDescriptor::GetStreamDescriptorCount**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount) to get the number of streams in the media source.</span></span>
4.  <span data-ttu-id="753a2-214">Вызовите [**имфпресентатиондескриптор:: жетстреамдескрипторбиндекс**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) для каждого потока в источнике мультимедиа и получите дескриптор потока потока.</span><span class="sxs-lookup"><span data-stu-id="753a2-214">Call [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) for each stream in the media source, get the stream's stream descriptor.</span></span>
5.  <span data-ttu-id="753a2-215">Вызовите [**имфстреамдескриптор:: жетмедиатипехандлер**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) , а затем [**Имфмедиатипехандлер:: жетмедиатипебиндекс**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) и получите первый тип носителя для потока.</span><span class="sxs-lookup"><span data-stu-id="753a2-215">Call [**IMFStreamDescriptor::GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) followed by [**IMFMediaTypeHandler::GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) and get the first media type for the stream.</span></span>

    <span data-ttu-id="753a2-216">**Примечание**   .   Чтобы избежать сложных вызовов, предположим, что для каждого потока существует только один тип мультимедиа и выбирается первый тип носителя потока.</span><span class="sxs-lookup"><span data-stu-id="753a2-216">**Note**   To avoid complex calls, assume that only one media type exists per stream and select the first media type of the stream.</span></span> <span data-ttu-id="753a2-217">Для сложных потоков необходимо перечислить каждый тип носителя из обработчика типа мультимедиа и выбрать тип носителя для кодирования.</span><span class="sxs-lookup"><span data-stu-id="753a2-217">For complex streams, you need to enumerate each media type from the media type handler and choose the media type that you would like to encode.</span></span>

6.  <span data-ttu-id="753a2-218">Вызовите метод I [**имфмедиатипе:: жетмажортипе**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype) , чтобы получить основной тип потока, чтобы определить, содержит ли поток аудио или видео.</span><span class="sxs-lookup"><span data-stu-id="753a2-218">Call I [**IMFMediaType::GetMajorType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype) to get the major type of the stream to determine whether the stream is contains audio or video.</span></span>
7.  <span data-ttu-id="753a2-219">В зависимости от основного типа потока Создайте типы целевых носителей.</span><span class="sxs-lookup"><span data-stu-id="753a2-219">Depending on the major type of the stream, create target media types.</span></span> <span data-ttu-id="753a2-220">Эти типы носителей будут содержать сведения о формате, которые будут использоваться кодировщиком во время сеанса кодирования.</span><span class="sxs-lookup"><span data-stu-id="753a2-220">These media types will hold format information that the encoder will use during the encoding session.</span></span> <span data-ttu-id="753a2-221">В следующих разделах этого руководства описывается процесс создания типов целевых носителей.</span><span class="sxs-lookup"><span data-stu-id="753a2-221">The following sections of this tutorial describe the process of creating the target media types.</span></span>
    -   <span data-ttu-id="753a2-222">Создание типа сжатого звукового носителя</span><span class="sxs-lookup"><span data-stu-id="753a2-222">Create a Compressed Audio Media Type</span></span>
    -   <span data-ttu-id="753a2-223">Создание типа носителя с сжатым видео</span><span class="sxs-lookup"><span data-stu-id="753a2-223">Create a Compressed Video Media Type</span></span>
8.  <span data-ttu-id="753a2-224">Создайте поток на основе типа целевого носителя, настройте поток в соответствии с требованиями приложения и добавьте поток в профиль.</span><span class="sxs-lookup"><span data-stu-id="753a2-224">Create a stream based on the target media type, configure the stream according to the application's requirements, and add the stream to the profile.</span></span> <span data-ttu-id="753a2-225">Дополнительные сведения см. в разделе [Добавление потоковых данных в приемник файлов ASF](adding-stream-information-to-the-asf-file-sink.md).</span><span class="sxs-lookup"><span data-stu-id="753a2-225">For more information, see [Adding Stream Information to the ASF File Sink](adding-stream-information-to-the-asf-file-sink.md).</span></span>

    1.  <span data-ttu-id="753a2-226">Вызовите [**имфасфпрофиле:: креатестреам**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream) и передайте целевой тип носителя, чтобы создать выходной поток.</span><span class="sxs-lookup"><span data-stu-id="753a2-226">Call [**IMFASFProfile::CreateStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream) and pass the target media type to create the output stream.</span></span> <span data-ttu-id="753a2-227">Метод получает интерфейс Имфасфстреамконфиг объекта потока.</span><span class="sxs-lookup"><span data-stu-id="753a2-227">The method retrieves the IMFASFStreamConfig interface of the stream object.</span></span>
    2.  <span data-ttu-id="753a2-228">Настройте поток.</span><span class="sxs-lookup"><span data-stu-id="753a2-228">Configure the stream.</span></span>
        -   <span data-ttu-id="753a2-229">Вызовите метод [**имфасфстреамконфиг:: сетстреамнумбер**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-setstreamnumber) , чтобы присвоить номер потоку.</span><span class="sxs-lookup"><span data-stu-id="753a2-229">Call [**IMFASFStreamConfig::SetStreamNumber**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-setstreamnumber) to assign a number to the stream.</span></span> <span data-ttu-id="753a2-230">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="753a2-230">This setting is mandatory.</span></span>
        -   <span data-ttu-id="753a2-231">При необходимости настройте параметры контейнера утечки, расширение полезных данных, взаимное исключение для каждого потока, вызвав методы [**имфасфстреамконфиг**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) и соответствующие атрибуты конфигурации потока.</span><span class="sxs-lookup"><span data-stu-id="753a2-231">Optionally configure the leaky bucket parameters, payload extension, mutual exclusion on each stream by calling [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) methods and relevant stream configuration attributes.</span></span>
    3.  <span data-ttu-id="753a2-232">Добавьте свойства кодировки уровня потока с помощью объекта ASF Контентинфо.</span><span class="sxs-lookup"><span data-stu-id="753a2-232">Add the stream level encoding properties by using the ASF ContentInfo object.</span></span> <span data-ttu-id="753a2-233">Дополнительные сведения об этом шаге см. в подразделе «Создание объекта ASF Контентинфо» этого руководства.</span><span class="sxs-lookup"><span data-stu-id="753a2-233">For more information about this step, see the "Create the ASF ContentInfo Object" section in this tutorial.</span></span>
    4.  <span data-ttu-id="753a2-234">Вызовите [**имфасфпрофиле:: сетстреам**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream) , чтобы добавить поток в профиль.</span><span class="sxs-lookup"><span data-stu-id="753a2-234">Call [**IMFASFProfile::SetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream) to add the stream to the profile.</span></span>

    <span data-ttu-id="753a2-235">В следующем примере кода создается выходной поток звука.</span><span class="sxs-lookup"><span data-stu-id="753a2-235">The following code example creates an output audio stream.</span></span>

    ```C++
    //-------------------------------------------------------------------
    //  CreateAudioStream
    //  Create an audio stream and add it to the profile.
    //
    //  pProfile: A pointer to the ASF profile.
    //  wStreamNumber: Stream number to assign for the new stream.
    //-------------------------------------------------------------------

    HRESULT CreateAudioStream(IMFASFProfile* pProfile, WORD wStreamNumber)
    {
        if (!pProfile)
        {
            return E_INVALIDARG;
        }
        if (wStreamNumber < 1 || wStreamNumber > 127 )
        {
            return MF_E_INVALIDSTREAMNUMBER;
        }

        IMFMediaType* pAudioType = NULL;
        IMFASFStreamConfig* pAudioStream = NULL;
        
        //Create an output type from the encoder
        HRESULT hr = GetOutputTypeFromWMAEncoder(&pAudioType);
        if (FAILED(hr))
        {
            goto done;
        }
        
        //Create a new stream with the audio type
        hr = pProfile->CreateStream(pAudioType, &pAudioStream);
        if (FAILED(hr))
        {
            goto done;
        }

        //Set stream number
        hr = pAudioStream->SetStreamNumber(wStreamNumber);
        if (FAILED(hr))
        {
            goto done;
        }
        
        //Add the stream to the profile
        hr = pProfile->SetStream(pAudioStream);
        if (FAILED(hr))
        {
            goto done;
        }

        wprintf_s(L"Audio Stream created. Stream Number: %d.\n", wStreamNumber);

    done:
        SafeRelease(&pAudioStream);
        SafeRelease(&pAudioType);
        return hr;
    }
    ```

    

    <span data-ttu-id="753a2-236">В следующем примере кода создается выходной поток видео.</span><span class="sxs-lookup"><span data-stu-id="753a2-236">The following code example creates an output video stream.</span></span>

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

    

<span data-ttu-id="753a2-237">В следующем примере кода создаются выходные потоки в зависимости от потоков в источнике.</span><span class="sxs-lookup"><span data-stu-id="753a2-237">The following code example creates output streams depending on the streams in the source.</span></span>


```C++
    //For each stream in the source, add target stream information in the profile
    for (DWORD iStream = 0; iStream < dwSrcStream; iStream++)
    {
        hr = pPD->GetStreamDescriptorByIndex(
            iStream, &fSelected, &pStreamDesc);
        if (FAILED(hr))
        {
            goto done;
        }

        if (!fSelected)
        {
            continue;
        }

        //Get the media type handler
        hr = pStreamDesc->GetMediaTypeHandler(&pHandler);
        if (FAILED(hr))
        {
            goto done;
        }

        //Get the first media type 
        hr = pHandler->GetMediaTypeByIndex(0, &pMediaType);
        if (FAILED(hr))
        {
            goto done;
        }

        //Get the major type
        hr = pMediaType->GetMajorType(&guidMajor);
        if (FAILED(hr))
        {
            goto done;
        }

        // If this is a video stream, create the target video stream
        if (guidMajor == MFMediaType_Video)
        {
            //The stream level encoding properties will be set in this call
            hr = CreateVideoStream(pProfile, wStreamID, pMediaType);

            if (FAILED(hr))
            {
                goto done;
            }
        }
        
        // If this is an audio stream, create the target audio stream
        if (guidMajor == MFMediaType_Audio)
        {
            //The stream level encoding properties will be set in this call
            hr = CreateAudioStream(pProfile, wStreamID);

            if (FAILED(hr))
            {
                goto done;
            }
        }

        //Get stream's encoding property
        hr = pContentInfo->GetEncodingConfigurationPropertyStore(wStreamID, &pContentInfoProps);
        if (FAILED(hr))
        {
            goto done;
        }

        //Set the stream-level encoding properties
        hr = SetEncodingProperties(guidMajor, pContentInfoProps);       
        if (FAILED(hr))
        {
            goto done;
        }


        SafeRelease(&pMediaType);
        SafeRelease(&pStreamDesc);
        SafeRelease(&pContentInfoProps);
        wStreamID++;
    }
```



### <a name="create-a-compressed-audio-media-type"></a><span data-ttu-id="753a2-238">Создание типа сжатого звукового носителя</span><span class="sxs-lookup"><span data-stu-id="753a2-238">Create a Compressed Audio Media Type</span></span>

<span data-ttu-id="753a2-239">Если в выходной файл необходимо включить аудиопоток, создайте тип аудио, указав характеристики закодированного типа, задав необходимые атрибуты.</span><span class="sxs-lookup"><span data-stu-id="753a2-239">If you want to include an audio stream in the output file, create an audio type by specifying the characteristics of the encoded type by setting the required attributes.</span></span> <span data-ttu-id="753a2-240">Чтобы убедиться, что тип аудио совместим с кодировщиком Windows Media Audio, создайте экземпляр файла MFT кодировщика, задайте свойства кодировки и получите тип мультимедиа, вызвав [**имфтрансформ:: жетаутпутаваилаблетипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype).</span><span class="sxs-lookup"><span data-stu-id="753a2-240">To make sure that the audio type is compatible with the Windows Media audio encoder, instantiate the encoder MFT, set the encoding properties, and get a media type by calling [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype).</span></span> <span data-ttu-id="753a2-241">Получите требуемый тип выходных данных, перебирая все доступные типы, получая атрибуты каждого типа мультимедиа и выбрав тип, ближайший к вашим требованиям.</span><span class="sxs-lookup"><span data-stu-id="753a2-241">Get the required output type by looping through all the available types, getting the attributes of each media type, and selecting the type that is closest to your requirements.</span></span> <span data-ttu-id="753a2-242">В этом руководстве вы получите первый доступный тип из списка типов выходных носителей, поддерживаемых кодировщиком.</span><span class="sxs-lookup"><span data-stu-id="753a2-242">In this tutorial, get the first available type from the list of output media types supported by the encoder.</span></span>

<span data-ttu-id="753a2-243">**Примечание**  .  В Windows 7 Media Foundation предоставляет новую функцию [**мфтранскодежетаудиуутпутаваилаблетипес**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) , которая получает список совместимых типов аудио.</span><span class="sxs-lookup"><span data-stu-id="753a2-243">**Note**  For Windows 7, Media Foundation provides a new function, [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) that retrieves a list of the compatible audio types.</span></span> <span data-ttu-id="753a2-244">Эта функция получает только типы носителей для кодирования CBR.</span><span class="sxs-lookup"><span data-stu-id="753a2-244">This function only gets media types for CBR encoding.</span></span>

<span data-ttu-id="753a2-245">Для полного звукового типа должны быть заданы следующие атрибуты:</span><span class="sxs-lookup"><span data-stu-id="753a2-245">A complete audio type must have the following attributes set:</span></span>

-   [<span data-ttu-id="753a2-246">**\_ \_ основной тип MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="753a2-246">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md)
-   [<span data-ttu-id="753a2-247">**подтип MF \_ MT \_**</span><span class="sxs-lookup"><span data-stu-id="753a2-247">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)
-   [<span data-ttu-id="753a2-248">**\_ \_ каналы аудиосигнала MF MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="753a2-248">**MF\_MT\_AUDIO\_NUM\_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)
-   [<span data-ttu-id="753a2-249">**\_ \_ звуковых образцов MF MT \_ \_ в \_ секунду**</span><span class="sxs-lookup"><span data-stu-id="753a2-249">**MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)
-   [<span data-ttu-id="753a2-250">**\_ \_ Выравнивание звукового \_ блока MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="753a2-250">**MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT**</span></span>](mf-mt-audio-block-alignment-attribute.md)
-   [<span data-ttu-id="753a2-251">**\_ \_ \_ Среднее \_ число байт \_ в секунду для \_ звука MF MT**</span><span class="sxs-lookup"><span data-stu-id="753a2-251">**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md)
-   [<span data-ttu-id="753a2-252">**\_ \_ звуковый бит MF MT \_ \_ на \_ выборку**</span><span class="sxs-lookup"><span data-stu-id="753a2-252">**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**</span></span>](mf-mt-audio-bits-per-sample-attribute.md)

<span data-ttu-id="753a2-253">В следующем примере кода создается сжатый тип звука путем получения совместимого типа из кодировщика Windows Media Audio.</span><span class="sxs-lookup"><span data-stu-id="753a2-253">The following code example creates a compressed audio type by getting a compatible type from the Windows Media Audio encoder.</span></span> <span data-ttu-id="753a2-254">Реализация для Сетенкодингпропертиес показана в разделе "Создание объекта Контентинфо ASF" этого руководства.</span><span class="sxs-lookup"><span data-stu-id="753a2-254">The implementation for SetEncodingProperties is shown in the "Create the ASF ContentInfo Object" section of this tutorial.</span></span>


```C++
//-------------------------------------------------------------------
//  GetOutputTypeFromWMAEncoder
//  Gets a compatible output type from the Windows Media audio encoder.
//
//  ppAudioType: Receives a pointer to the media type.
//-------------------------------------------------------------------

HRESULT GetOutputTypeFromWMAEncoder(IMFMediaType** ppAudioType)
{
    if (!ppAudioType)
    {
        return E_POINTER;
    }

    IMFTransform* pMFT = NULL;
    IMFMediaType* pType = NULL;
    IPropertyStore* pProps = NULL;

    //We need to find a suitable output media type
    //We need to create the encoder to get the available output types
    //and discard the instance.

    CLSID *pMFTCLSIDs = NULL;   // Pointer to an array of CLISDs. 
    UINT32 cCLSID = 0;            // Size of the array.

    MFT_REGISTER_TYPE_INFO tinfo;
    
    tinfo.guidMajorType = MFMediaType_Audio;
    tinfo.guidSubtype = MFAudioFormat_WMAudioV9;

    // Look for an encoder.
    HRESULT hr = MFTEnum(
        MFT_CATEGORY_AUDIO_ENCODER,
        0,                  // Reserved
        NULL,                // Input type to match. None.
        &tinfo,             // WMV encoded type.
        NULL,               // Attributes to match. (None.)
        &pMFTCLSIDs,        // Receives a pointer to an array of CLSIDs.
        &cCLSID             // Receives the size of the array.
        );
    if (FAILED(hr))
    {
        goto done;
    }

    // MFTEnum can return zero matches.
    if (cCLSID == 0)
    {
        hr = MF_E_TOPO_CODEC_NOT_FOUND;
        goto done;
    }
    else
    {
        // Create the MFT decoder
        hr = CoCreateInstance(pMFTCLSIDs[0], NULL,
            CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pMFT));

        if (FAILED(hr))
        {
            goto done;
        }

    }

    // Get the encoder's property store

    hr = pMFT->QueryInterface(IID_PPV_ARGS(&pProps));
    if (FAILED(hr))
    {
        goto done;
    }
    
    //Set encoding properties
    hr = SetEncodingProperties(MFMediaType_Audio, pProps);
    if (FAILED(hr))
    {
        goto done;
    }

    //Get the first output type
    //You can loop through the available output types to choose 
    //the one that meets your target requirements
    hr = pMFT->GetOutputAvailableType(0, 0, &pType);
    if (FAILED(hr))
    {
        goto done;
    }

    //Return to the caller
    *ppAudioType = pType;
    (*ppAudioType)->AddRef();
    
done:
    SafeRelease(&pProps);
    SafeRelease(&pType);
    SafeRelease(&pMFT);
    CoTaskMemFree(pMFTCLSIDs);
    return hr;
}
```



### <a name="create-a-compressed-video-media-type"></a><span data-ttu-id="753a2-255">Создание типа носителя с сжатым видео</span><span class="sxs-lookup"><span data-stu-id="753a2-255">Create a Compressed Video Media Type</span></span>

<span data-ttu-id="753a2-256">Если вы хотите включить в выходной файл поток видео, создайте тип видео с полным кодированием.</span><span class="sxs-lookup"><span data-stu-id="753a2-256">If you want to include a video stream in the output file, create a complete-encoded video type.</span></span> <span data-ttu-id="753a2-257">Полный тип носителя должен включать требуемую скорость потока и частные данные кодека.</span><span class="sxs-lookup"><span data-stu-id="753a2-257">The complete media type must include the desired bit rate and codec private data.</span></span>

<span data-ttu-id="753a2-258">Существует два способа создания носителя с полным типом видео.</span><span class="sxs-lookup"><span data-stu-id="753a2-258">There are two ways you can create a complete video media type.</span></span>

-   <span data-ttu-id="753a2-259">Создайте пустой тип мультимедиа и скопируйте атрибуты типа мультимедиа из исходного видеотипа и перезапишите атрибут [**\_ \_ подтипа MF MT**](mf-mt-subtype-attribute.md) с помощью константы GUID мфвидеоформат \_ WMV3.</span><span class="sxs-lookup"><span data-stu-id="753a2-259">Create an empty media type and copy the media type attributes from the source video type and overwrite the [**MF\_MT\_SUBTYPE**](mf-mt-subtype-attribute.md) attribute with the GUID constant MFVideoFormat\_WMV3.</span></span>

    <span data-ttu-id="753a2-260">Для полного типа видео должны быть заданы следующие атрибуты:</span><span class="sxs-lookup"><span data-stu-id="753a2-260">A complete video type must have the following attributes set:</span></span>

    -   <span data-ttu-id="753a2-261">\_ \_ основной тип MF \_ MT</span><span class="sxs-lookup"><span data-stu-id="753a2-261">MF\_MT\_MAJOR\_TYPE</span></span>
    -   <span data-ttu-id="753a2-262">подтип MF \_ MT \_</span><span class="sxs-lookup"><span data-stu-id="753a2-262">MF\_MT\_SUBTYPE</span></span>
    -   <span data-ttu-id="753a2-263">\_ \_ Частота кадров MF \_ MT</span><span class="sxs-lookup"><span data-stu-id="753a2-263">MF\_MT\_FRAME\_RATE</span></span>
    -   <span data-ttu-id="753a2-264">\_ \_ Размер пакета MF \_ MT</span><span class="sxs-lookup"><span data-stu-id="753a2-264">MF\_MT\_FRAME\_SIZE</span></span>
    -   <span data-ttu-id="753a2-265">\_ \_ режим чересстрочную РАЗВЕРТКи MF \_</span><span class="sxs-lookup"><span data-stu-id="753a2-265">MF\_MT\_INTERLACE\_MODE</span></span>
    -   <span data-ttu-id="753a2-266">пропорции MF \_ MT \_ пикселей \_ \_</span><span class="sxs-lookup"><span data-stu-id="753a2-266">MF\_MT\_PIXEL\_ASPECT\_RATIO</span></span>
    -   <span data-ttu-id="753a2-267">\_ \_ Средняя скорость MF \_ MT</span><span class="sxs-lookup"><span data-stu-id="753a2-267">MF\_MT\_AVG\_BITRATE</span></span>
    -   <span data-ttu-id="753a2-268">\_ \_ данные пользователя MF \_ MT</span><span class="sxs-lookup"><span data-stu-id="753a2-268">MF\_MT\_USER\_DATA</span></span>

    <span data-ttu-id="753a2-269">В следующем примере кода создается сжатый тип видео из типа видео источника.</span><span class="sxs-lookup"><span data-stu-id="753a2-269">The following code example creates a compressed video type from the source's video type.</span></span>

    ```C++
    //-------------------------------------------------------------------
    //  CreateCompressedVideoType
    //  Creates an output type from source's video media type.
    //
    //    pType: A pointer to the source's video media type.
    //  ppVideoType: Receives a pointer to the media type.
    //-------------------------------------------------------------------

    HRESULT CreateCompressedVideoType(
            IMFMediaType* pType, 
            IMFMediaType** ppVideoType)
    {
        if (!pType)
        {
            return E_INVALIDARG;
        }
        if (!ppVideoType)
        {
            return E_POINTER;
        }
        
        HRESULT hr = S_OK;
        MFRatio fps = { 0 };
        MFRatio par = { 0 };
        UINT32 width = 0, height = 0;
        UINT32 interlace = MFVideoInterlace_Unknown;
        UINT32 fSamplesIndependent = 0;
        UINT32 cBitrate = 0;

        IMFMediaType* pMediaType = NULL;

        GUID guidMajor = GUID_NULL;

        hr = pType->GetMajorType(&guidMajor);
        if (FAILED(hr))
        {
            goto done;
        }

        if (guidMajor != MFMediaType_Video )
        {
            hr = MF_E_INVALID_FORMAT;
            goto done;
        }

        hr = MFCreateMediaType(&pMediaType);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pType->CopyAllItems(pMediaType);
        if (FAILED(hr))
        {
            goto done;
        }

        //Fill the missing attributes
        //1. Frame rate
        hr = MFGetAttributeRatio(pMediaType, MF_MT_FRAME_RATE, (UINT32*)&fps.Numerator, (UINT32*)&fps.Denominator);
        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            fps.Numerator = 30000;
            fps.Denominator = 1001;

            hr = MFSetAttributeRatio(pMediaType, MF_MT_FRAME_RATE, fps.Numerator, fps.Denominator);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        ////2. Frame size
        hr = MFGetAttributeSize(pMediaType, MF_MT_FRAME_SIZE, &width, &height);
        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            width = 1280;
            height = 720;
                
            hr = MFSetAttributeSize(pMediaType, MF_MT_FRAME_SIZE, width, height);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        ////3. Interlace mode
        
        if (FAILED(pMediaType->GetUINT32(MF_MT_INTERLACE_MODE, &interlace)))
        {
            hr = pMediaType->SetUINT32(MF_MT_INTERLACE_MODE, MFVideoInterlace_Progressive);
            if (FAILED(hr))
            {
                goto done;
            }

        }

        ////4. Pixel aspect Ratio
        hr = MFGetAttributeRatio(pMediaType, MF_MT_PIXEL_ASPECT_RATIO, (UINT32*)&par.Numerator, (UINT32*)&par.Denominator);
        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            par.Numerator = par.Denominator = 1;
            hr = MFSetAttributeRatio(pMediaType, MF_MT_PIXEL_ASPECT_RATIO, (UINT32)par.Numerator, (UINT32)par.Denominator);
            if (FAILED(hr))
            {
                goto done;
            }

        }

        //6. bit rate
        if (FAILED(pMediaType->GetUINT32(MF_MT_AVG_BITRATE, &cBitrate)))
        {
            hr = pMediaType->SetUINT32(MF_MT_AVG_BITRATE, 1000000);
            if (FAILED(hr))
            {
                goto done;
            }

        }

        hr = pMediaType->SetGUID(MF_MT_SUBTYPE, MFVideoFormat_WMV3);
        if (FAILED(hr))
        {
            goto done;
        }

        // Return the pointer to the caller.
        *ppVideoType = pMediaType;
        (*ppVideoType)->AddRef();


    done:
        SafeRelease(&pMediaType);
        return hr;
    }
    
    ```

    

-   <span data-ttu-id="753a2-270">Получите совместимый тип мультимедиа от кодировщика видео Windows Media, задав свойства кодировки и вызвав [**имфтрансформ:: жетаутпутаваилаблетипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype).</span><span class="sxs-lookup"><span data-stu-id="753a2-270">Get a compatible media type from the Windows Media video encoder by setting the encoding properties and then calling [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype).</span></span> <span data-ttu-id="753a2-271">Этот метод возвращает частичный тип.</span><span class="sxs-lookup"><span data-stu-id="753a2-271">This method returns the partial type.</span></span> <span data-ttu-id="753a2-272">Убедитесь, что разделяемый тип преобразован в полный тип, добавив следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="753a2-272">Make sure you convert the partial type to a complete type by adding the following information:</span></span>

    -   <span data-ttu-id="753a2-273">Установите скорость воспроизведения видео в атрибуте [**" \_ \_ Средняя \_ скорость" MF MT**](mf-mt-avg-bitrate-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="753a2-273">Set the video bit rate in the [**MF\_MT\_AVG\_BITRATE**](mf-mt-avg-bitrate-attribute.md) attribute.</span></span>
    -   <span data-ttu-id="753a2-274">Добавьте частные данные кодека, задав [**атрибут \_ \_ \_ данных пользователя MF MT**](mf-mt-user-data-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="753a2-274">Add codec private data by setting the [**MF\_MT\_USER\_DATA**](mf-mt-user-data-attribute.md) attribute.</span></span> <span data-ttu-id="753a2-275">Подробные инструкции см. в разделе "данные частного кодека" раздела [Настройка кодировщика WMV](configuring-a-wmv-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="753a2-275">For detailed instructions, see "Private Codec Data" in [Configuring a WMV Encoder](configuring-a-wmv-encoder.md).</span></span>

    <span data-ttu-id="753a2-276">Так как [**ивмкодекприватедата:: жетприватедата**](../wmformat/iwmcodecprivatedata-getprivatedata.md) проверяет скорость потока перед возвратом частных данных кодека, перед получением частных данных кодека необходимо установить скорость.</span><span class="sxs-lookup"><span data-stu-id="753a2-276">Because [**IWMCodecPrivateData::GetPrivateData**](../wmformat/iwmcodecprivatedata-getprivatedata.md) checks the bit rate before returning the codec private data, make sure that you set the bit rate before getting the codec private data.</span></span>

    <span data-ttu-id="753a2-277">В следующем примере кода создается сжатый тип видео путем получения совместимого типа из кодировщика видео Windows Media.</span><span class="sxs-lookup"><span data-stu-id="753a2-277">The following code example creates a compressed video type by getting a compatible type from the Windows Media Video encoder.</span></span> <span data-ttu-id="753a2-278">Он также создает несжатый тип видео и задает его в качестве входных данных кодировщика.</span><span class="sxs-lookup"><span data-stu-id="753a2-278">It also creates an uncompressed video type and sets it as the encoder's input.</span></span> <span data-ttu-id="753a2-279">Это реализуется в вспомогательной функции Креатеункомпресседвидеотипе.</span><span class="sxs-lookup"><span data-stu-id="753a2-279">This is implemented in the helper function CreateUncompressedVideoType.</span></span> <span data-ttu-id="753a2-280">Жетаутпуттипефромвмвенкодер преобразует возвращаемый разделяемый тип в полный тип путем добавления частных данных кодека.</span><span class="sxs-lookup"><span data-stu-id="753a2-280">GetOutputTypeFromWMVEncoder converts the returned partial type into a complete type by adding codec private data.</span></span> <span data-ttu-id="753a2-281">Реализация для Сетенкодингпропертиес показана в разделе "Создание объекта Контентинфо ASF" этого руководства.</span><span class="sxs-lookup"><span data-stu-id="753a2-281">The implementation for SetEncodingProperties is shown in the "Create the ASF ContentInfo Object" section of this tutorial.</span></span>

    ```C++
    //-------------------------------------------------------------------
    //  GetOutputTypeFromWMVEncoder
    //  Gets a compatible output type from the Windows Media video encoder.
    //
    //  pType: A pointer to the source video stream's media type.
    //  ppVideoType: Receives a pointer to the media type.
    //-------------------------------------------------------------------

    HRESULT GetOutputTypeFromWMVEncoder(IMFMediaType* pType, IMFMediaType** ppVideoType)
    {
        if (!ppVideoType)
        {
            return E_POINTER;
        }

        IMFTransform* pMFT = NULL;
        IPropertyStore* pProps = NULL;
        IMFMediaType* pInputType = NULL;
        IMFMediaType* pOutputType = NULL;
        
        UINT32 cBitrate = 0;

        //We need to find a suitable output media type
        //We need to create the encoder to get the available output types
        //and discard the instance.

        CLSID *pMFTCLSIDs = NULL;   // Pointer to an array of CLISDs. 
        UINT32 cCLSID = 0;          // Size of the array.

        MFT_REGISTER_TYPE_INFO tinfo;
        
        tinfo.guidMajorType = MFMediaType_Video;
        tinfo.guidSubtype = MFVideoFormat_WMV3;

        // Look for an encoder.
        HRESULT hr = MFTEnum(
            MFT_CATEGORY_VIDEO_ENCODER,
            0,                  // Reserved
            NULL,               // Input type to match. None.
            &tinfo,             // WMV encoded type.
            NULL,               // Attributes to match. (None.)
            &pMFTCLSIDs,        // Receives a pointer to an array of CLSIDs.
            &cCLSID             // Receives the size of the array.
            );
        if (FAILED(hr))
        {
            goto done;
        }

        // MFTEnum can return zero matches.
        if (cCLSID == 0)
        {
            hr = MF_E_TOPO_CODEC_NOT_FOUND;
            goto done;
        }
        else
        {
            //Create the MFT decoder
            hr = CoCreateInstance(pMFTCLSIDs[0], NULL,
                CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pMFT));
            if (FAILED(hr))
            {
                goto done;
            }

        }
        
        //Get the video encoder property store
        hr = pMFT->QueryInterface(IID_PPV_ARGS(&pProps));
        if (FAILED(hr))
        {
            goto done;
        }

        //Set encoding properties
        hr = SetEncodingProperties(MFMediaType_Video, pProps);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = CreateUncompressedVideoType(pType, &pInputType);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pMFT->SetInputType(0, pInputType, 0);

        //Get the first output type
        //You can loop through the available output types to choose 
        //the one that meets your target requirements
        hr =  pMFT->GetOutputAvailableType(0, 0, &pOutputType);
        if (FAILED(hr))
        {
            goto done;
        }
        
        hr = pType->GetUINT32(MF_MT_AVG_BITRATE, &cBitrate);
        if (FAILED(hr))
        {
            goto done;
        }

        //Now set the bit rate
        hr = pOutputType->SetUINT32(MF_MT_AVG_BITRATE, cBitrate);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = AddPrivateData(pMFT, pOutputType);
        if (FAILED(hr))
        {
            goto done;
        }

        //Return to the caller
        *ppVideoType = pOutputType;
        (*ppVideoType)->AddRef();
        
    done:
        SafeRelease(&pProps);
        SafeRelease(&pOutputType);
        SafeRelease(&pInputType);
        SafeRelease(&pMFT);
        CoTaskMemFree(pMFTCLSIDs);
        return hr;
    }
    ```

    

    <span data-ttu-id="753a2-282">В следующем примере кода создается несжатый тип видео.</span><span class="sxs-lookup"><span data-stu-id="753a2-282">The following code example creates an uncompressed video type.</span></span>

    ```C++
    //-------------------------------------------------------------------
    //  CreateUncompressedVideoType
    //  Creates an uncompressed video type.
    //
    //    pType: A pointer to the source's video media type.
    //  ppVideoType: Receives a pointer to the media type.
    //-------------------------------------------------------------------

    HRESULT CreateUncompressedVideoType(IMFMediaType* pType, IMFMediaType** ppMediaType)
    {
        if (!pType)
        {
            return E_INVALIDARG;
        }
        if (!ppMediaType)
        {
            return E_POINTER;
        }
        
        MFRatio fps = { 0 };
        MFRatio par = { 0 };
        UINT32 width = 0, height = 0;
        UINT32 interlace = MFVideoInterlace_Unknown;
        UINT32 cBitrate = 0;

        IMFMediaType* pMediaType = NULL;

        GUID guidMajor = GUID_NULL;

        HRESULT hr = pType->GetMajorType(&guidMajor);
        if (FAILED(hr))
        {
            goto done;
        }

        if (guidMajor != MFMediaType_Video )
        {
            hr = MF_E_INVALID_FORMAT;
            goto done;
        }

        hr = MFGetAttributeRatio(pType, MF_MT_FRAME_RATE, (UINT32*)&fps.Numerator, (UINT32*)&fps.Denominator);
        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            fps.Numerator = 30000;
            fps.Denominator = 1001;

        }
        hr = MFGetAttributeSize(pType, MF_MT_FRAME_SIZE, &width, &height);
        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            width = 1280;
            height = 720;

        }

        interlace = MFGetAttributeUINT32(pType, MF_MT_INTERLACE_MODE, MFVideoInterlace_Progressive);

        hr = MFGetAttributeRatio(pType, MF_MT_PIXEL_ASPECT_RATIO, (UINT32*)&par.Numerator, (UINT32*)&par.Denominator);
        if (FAILED(hr))
        {
            par.Numerator = par.Denominator = 1;
        }

        cBitrate = MFGetAttributeUINT32(pType, MF_MT_AVG_BITRATE, 1000000);

        hr = MFCreateMediaType(&pMediaType);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = pMediaType->SetGUID(MF_MT_MAJOR_TYPE, guidMajor);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = pMediaType->SetGUID(MF_MT_SUBTYPE, MFVideoFormat_RGB32);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = MFSetAttributeRatio(pMediaType, MF_MT_FRAME_RATE, fps.Numerator, fps.Denominator);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = MFSetAttributeSize(pMediaType, MF_MT_FRAME_SIZE, width, height);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = pMediaType->SetUINT32(MF_MT_INTERLACE_MODE, 2);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pMediaType->SetUINT32(MF_MT_ALL_SAMPLES_INDEPENDENT, TRUE);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pMediaType->SetUINT32(MF_MT_AVG_BITRATE, cBitrate);
        if (FAILED(hr))
        {
            goto done;
        }

        // Return the pointer to the caller.
        *ppMediaType = pMediaType;
        (*ppMediaType)->AddRef();


    done:
        SafeRelease(&pMediaType);
        return hr;
    }
    ```

    

    <span data-ttu-id="753a2-283">В следующем примере кода частные данные кодека добавляются в указанный тип видеоматериала.</span><span class="sxs-lookup"><span data-stu-id="753a2-283">The following code example adds codec private data to the specified video media type.</span></span>

    ```C++
    //
    // AddPrivateData
    // Appends the private codec data to a media type.
    //
    // pMFT: The video encoder
    // pTypeOut: A video type from the encoder's type list.
    //
    // The function modifies pTypeOut by adding the codec data.
    //

    HRESULT AddPrivateData(IMFTransform *pMFT, IMFMediaType *pTypeOut)
    {
        HRESULT hr = S_OK;
        ULONG cbData = 0;
        BYTE *pData = NULL;

        IWMCodecPrivateData *pPrivData = NULL;

        DMO_MEDIA_TYPE mtOut = { 0 };

        // Convert the type to a DMO type.
        hr = MFInitAMMediaTypeFromMFMediaType(
            pTypeOut, 
            FORMAT_VideoInfo, 
            (AM_MEDIA_TYPE*)&mtOut
            );
        
        if (SUCCEEDED(hr))
        {
            hr = pMFT->QueryInterface(IID_PPV_ARGS(&pPrivData));
        }

        if (SUCCEEDED(hr))
        {
            hr = pPrivData->SetPartialOutputType(&mtOut);
        }

        //
        // Get the private codec data
        //

        // First get the buffer size.
        if (SUCCEEDED(hr))
        {
            hr = pPrivData->GetPrivateData(NULL, &cbData);
        }

        if (SUCCEEDED(hr))
        {
            pData = new BYTE[cbData];

            if (pData == NULL)
            {
                hr = E_OUTOFMEMORY;
            }
        }

        // Now get the data.
        if (SUCCEEDED(hr))
        {
            hr = pPrivData->GetPrivateData(pData, &cbData);
        }

        // Add the data to the media type.
        if (SUCCEEDED(hr))
        {
            hr = pTypeOut->SetBlob(MF_MT_USER_DATA, pData, cbData);
        }

        delete [] pData;
        MoFreeMediaType(&mtOut);
        SafeRelease(&pPrivData);
        return hr;
    }
    ```

    

### <a name="create-the-asf-contentinfo-object"></a><span data-ttu-id="753a2-284">Создание объекта Контентинфо ASF</span><span class="sxs-lookup"><span data-stu-id="753a2-284">Create the ASF ContentInfo Object</span></span>

<span data-ttu-id="753a2-285">Объект ASF Контентинфо является компонентом уровня Вмконтаинер, который в основном предназначен для хранения сведений об объекте заголовка ASF.</span><span class="sxs-lookup"><span data-stu-id="753a2-285">The ASF ContentInfo object is a WMContainer level component that is primarily designed to store ASF Header Object information.</span></span> <span data-ttu-id="753a2-286">Приемник ASF-файлов реализует объект Контентинфо для хранения сведений (в хранилище свойств), которые будут использоваться для записи объекта заголовка ASF закодированного файла.</span><span class="sxs-lookup"><span data-stu-id="753a2-286">The ASF file sink, implements the ContentInfo object in order to store information (in a property store) that will be used to write the ASF Header Object of the encoded file.</span></span> <span data-ttu-id="753a2-287">Для этого необходимо создать и настроить следующий набор данных для объекта Контентинфо перед началом сеанса кодирования.</span><span class="sxs-lookup"><span data-stu-id="753a2-287">To do so, you must create and configure the following set of information on the ContentInfo object before starting the encoding session.</span></span>

1.  <span data-ttu-id="753a2-288">Вызовите [**мфкреатеасфконтентинфо**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) , чтобы создать пустой объект контентинфо.</span><span class="sxs-lookup"><span data-stu-id="753a2-288">Call [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) to create an empty ContentInfo object.</span></span>

    <span data-ttu-id="753a2-289">В следующем примере кода создается пустой объект Контентинфо.</span><span class="sxs-lookup"><span data-stu-id="753a2-289">The following code example creates an empty ContentInfo object.</span></span>

    ```C++
        // Create an empty ContentInfo object
        hr = MFCreateASFContentInfo(&pContentInfo);
        if (FAILED(hr))
        {
            goto done;
        }
    
    ```

    

2.  <span data-ttu-id="753a2-290">Вызовите [**имфасфконтентинфо:: жетенкодингконфигуратионпропертисторе**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) , чтобы получить хранилище свойств уровня потока для приемника файла.</span><span class="sxs-lookup"><span data-stu-id="753a2-290">Call [**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) to get the file sink's stream-level property store.</span></span> <span data-ttu-id="753a2-291">В этом вызове необходимо передать номер потока, назначенный для потока, при создании профиля ASF.</span><span class="sxs-lookup"><span data-stu-id="753a2-291">In this call, you need to pass the stream number that you assigned for the stream while creating the ASF profile.</span></span>
3.  <span data-ttu-id="753a2-292">Задайте [Свойства кодировки](configuring-the-encoder.md) на уровне потока в хранилище свойств потока для приемника файла.</span><span class="sxs-lookup"><span data-stu-id="753a2-292">Set the stream-level [Encoding Properties](configuring-the-encoder.md) in the file sink's stream property store.</span></span> <span data-ttu-id="753a2-293">Дополнительные сведения см. в разделе "свойства кодировки потока" раздела [Задание свойств в приемнике файла](setting-properties-in-the-file-sink.md).</span><span class="sxs-lookup"><span data-stu-id="753a2-293">For more information, see "Stream Encoding Properties" in [Setting Properties in the File Sink](setting-properties-in-the-file-sink.md).</span></span>

    <span data-ttu-id="753a2-294">В следующем примере кода устанавливаются свойства уровня потока в хранилище свойств приемника файла.</span><span class="sxs-lookup"><span data-stu-id="753a2-294">The following code example sets the stream level properties in the file sink's property store.</span></span>

    ```C++
            //Get stream's encoding property
            hr = pContentInfo->GetEncodingConfigurationPropertyStore(wStreamID, &pContentInfoProps);
            if (FAILED(hr))
            {
                goto done;
            }

            //Set the stream-level encoding properties
            hr = SetEncodingProperties(guidMajor, pContentInfoProps);       
            if (FAILED(hr))
            {
                goto done;
            }

    
    ```

    

    <span data-ttu-id="753a2-295">В следующем примере кода показана реализация для Сетенкодингпропертиес.</span><span class="sxs-lookup"><span data-stu-id="753a2-295">The following code example shows the implementation for SetEncodingProperties.</span></span> <span data-ttu-id="753a2-296">Эта функция задает свойства кодирования на уровне потока для CBR и VBR.</span><span class="sxs-lookup"><span data-stu-id="753a2-296">This function sets stream level encoding properties for CBR and VBR.</span></span>

    ```C++
    //-------------------------------------------------------------------
    //  SetEncodingProperties
    //  Create a media source from a URL.
    //
    //  guidMT:  Major type of the stream, audio or video
    //  pProps:  A pointer to the property store in which 
    //           to set the required encoding properties.
    //-------------------------------------------------------------------

    HRESULT SetEncodingProperties (const GUID guidMT, IPropertyStore* pProps)
    {
        if (!pProps)
        {
            return E_INVALIDARG;
        }

        if (EncodingMode == NONE)
        {
            return MF_E_NOT_INITIALIZED;
        }
       
        HRESULT hr = S_OK;

        PROPVARIANT var;

        switch (EncodingMode)
        {
            case CBR:
                // Set VBR to false.
                hr = InitPropVariantFromBoolean(FALSE, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_VBRENABLED, var);
                if (FAILED(hr))
                {
                    goto done;
                }

                // Set the video buffer window.
                if (guidMT == MFMediaType_Video)
                {
                    hr = InitPropVariantFromInt32(VIDEO_WINDOW_MSEC, &var);
                    if (FAILED(hr))
                    {
                        goto done;
                    }

                    hr = pProps->SetValue(MFPKEY_VIDEOWINDOW, var);    
                    if (FAILED(hr))
                    {
                        goto done;
                    }
                }
                break;

            case VBR:
                //Set VBR to true.
                hr = InitPropVariantFromBoolean(TRUE, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_VBRENABLED, var);
                if (FAILED(hr))
                {
                    goto done;
                }

                // Number of encoding passes is 1.

                hr = InitPropVariantFromInt32(1, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_PASSESUSED, var);
                if (FAILED(hr))
                {
                    goto done;
                }

                // Set the quality level.

                if (guidMT == MFMediaType_Audio)
                {
                    hr = InitPropVariantFromUInt32(98, &var);
                    if (FAILED(hr))
                    {
                        goto done;
                    }

                    hr = pProps->SetValue(MFPKEY_DESIRED_VBRQUALITY, var);    
                    if (FAILED(hr))
                    {
                        goto done;
                    }
                }
                else if (guidMT == MFMediaType_Video)
                {
                    hr = InitPropVariantFromUInt32(95, &var);
                    if (FAILED(hr))
                    {
                        goto done;
                    }

                    hr = pProps->SetValue(MFPKEY_VBRQUALITY, var);    
                    if (FAILED(hr))
                    {
                        goto done;
                    }
                }
                break;

            default:
                hr = E_UNEXPECTED;
                break;
        }    

    done:
        PropVariantClear(&var);
        return hr;
    }
    ```

    

4.  <span data-ttu-id="753a2-297">Вызовите [**имфасфконтентинфо:: жетенкодингконфигуратионпропертисторе**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) , чтобы получить глобальное хранилище свойств приемника файла.</span><span class="sxs-lookup"><span data-stu-id="753a2-297">Call [**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) to get the file sink's global property store.</span></span> <span data-ttu-id="753a2-298">В этом вызове необходимо передать 0 в первом параметре.</span><span class="sxs-lookup"><span data-stu-id="753a2-298">In this call, you need to pass 0 in the first parameter.</span></span> <span data-ttu-id="753a2-299">Дополнительные сведения см. в разделе "свойства глобального приемника файлов" раздела [Настройка свойств в приемнике файла](setting-properties-in-the-file-sink.md).</span><span class="sxs-lookup"><span data-stu-id="753a2-299">For more information, see "Global File Sink Properties" in [Setting Properties in the File Sink](setting-properties-in-the-file-sink.md).</span></span>
5.  <span data-ttu-id="753a2-300">Установите для параметра [**мфпкэй \_ АСФМЕДИАСИНК \_ Автокорректировка \_ скорость**](mfpkey-asfmediasink-autoadjust-bitrate-property.md) значение Variant \_ true, чтобы значения сегмента утечки в мультиплексоре ASF были правильно настроены.</span><span class="sxs-lookup"><span data-stu-id="753a2-300">Set the [**MFPKEY\_ASFMEDIASINK\_AUTOADJUST\_BITRATE**](mfpkey-asfmediasink-autoadjust-bitrate-property.md) to VARIANT\_TRUE to ensure the leaky bucket values in the ASF multiplexer are adjusted properly.</span></span> <span data-ttu-id="753a2-301">Сведения об этом свойстве см. в разделе "Инициализация мультиплексора и параметры сегмента утечки" раздела [Создание объекта мультиплексора](creating-the-multiplexer-object.md).</span><span class="sxs-lookup"><span data-stu-id="753a2-301">For information about this property, see "Multiplexer Initialization and Leaky Bucket Settings" in [Creating the Multiplexer Object](creating-the-multiplexer-object.md).</span></span>

    <span data-ttu-id="753a2-302">В следующем примере кода устанавливаются свойства уровня потока в хранилище свойств приемника файла.</span><span class="sxs-lookup"><span data-stu-id="753a2-302">The following code example sets the stream level properties in the file sink's property store.</span></span>

    ```C++
        //Now we need to set global properties that will be set on the media sink
        hr = pContentInfo->GetEncodingConfigurationPropertyStore(0, &pContentInfoProps);
        if (FAILED(hr))
        {
            goto done;
        }

        //Auto adjust Bitrate
        var.vt = VT_BOOL;
        var.boolVal = VARIANT_TRUE;

        hr = pContentInfoProps->SetValue(MFPKEY_ASFMEDIASINK_AUTOADJUST_BITRATE, var);
        
        //Initialize with the profile
        hr = pContentInfo->SetProfile(pProfile);
        if (FAILED(hr))
        {
            goto done;
        }
    ```

    

    > [!Note]  
    > <span data-ttu-id="753a2-303">Существуют и другие свойства, которые можно задать на глобальном уровне для приемника файла.</span><span class="sxs-lookup"><span data-stu-id="753a2-303">There are other properties that you can set at the global level for the file sink.</span></span> <span data-ttu-id="753a2-304">Дополнительные сведения см. в разделе "Настройка объекта Контентинфо с помощью параметров кодировщика" раздела [Настройка свойств в объекте контентинфо](setting-properties-in-the-contentinfo-object.md).</span><span class="sxs-lookup"><span data-stu-id="753a2-304">For more information, see "Configuring the ContentInfo Object with Encoder Settings" in [Setting Properties in the ContentInfo Object](setting-properties-in-the-contentinfo-object.md).</span></span>

     

<span data-ttu-id="753a2-305">Вы будете использовать настроенный ASF Контентинфо для создания объекта активации для приемника файлов ASF (описывается в следующем разделе).</span><span class="sxs-lookup"><span data-stu-id="753a2-305">You will use the configured ASF ContentInfo to create an activation object for the ASF file sink (described in the next section).</span></span>

<span data-ttu-id="753a2-306">При создании необработанного приемника файла ([**мфкреатеасфмедиасинкактивате**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate)), который использует объект активации, можно использовать настроенный объект контентинфо для создания экземпляра приемника ASF Media (описывается в следующем разделе).</span><span class="sxs-lookup"><span data-stu-id="753a2-306">If you are creating an out-of-process file sink ([**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate)), that is by using an activation object, you can use the configured ContentInfo object to instantiate the ASF media sink (described in the next section).</span></span> <span data-ttu-id="753a2-307">Если создается внутрипроцессный приемник файлов ([**мфкреатеасфмедиасинк**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink)), вместо создания пустого объекта контентинфо, как описано в шаге 1, получите ссылку на интерфейс [**имфасфконтентинфо**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) , вызвав **имфмедиасинк:: QueryInterface** в приемнике файла.</span><span class="sxs-lookup"><span data-stu-id="753a2-307">If you are creating an in-process file sink ([**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink)), instead of creating the empty ContentInfo object as described in step 1, get a reference to the [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) interface by calling **IMFMediaSink::QueryInterface** on the file sink.</span></span> <span data-ttu-id="753a2-308">Затем необходимо настроить объект Контентинфо, как описано в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="753a2-308">You must then configure the ContentInfo object as described in this section.</span></span>

### <a name="create-the-asf-file-sink"></a><span data-ttu-id="753a2-309">Создание приемника файлов ASF</span><span class="sxs-lookup"><span data-stu-id="753a2-309">Create the ASF File Sink</span></span>

<span data-ttu-id="753a2-310">На этом этапе работы с руководством вы будете использовать настроенный файл ASF Контентинфо, созданный на предыдущем шаге, для создания объекта активации для приемника файлов ASF путем вызова функции [**мфкреатеасфмедиасинкактивате**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate) .</span><span class="sxs-lookup"><span data-stu-id="753a2-310">In this step of the tutorial, you will use the configured ASF ContentInfo, which you created in the previous step, to create an activation object for the ASF file sink by calling the [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate) function.</span></span> <span data-ttu-id="753a2-311">Дополнительные сведения см. [в разделе Создание приемника файлов ASF](creating-the-asf-file-sink.md).</span><span class="sxs-lookup"><span data-stu-id="753a2-311">For more information, see [Creating the ASF File Sink](creating-the-asf-file-sink.md).</span></span>

<span data-ttu-id="753a2-312">В следующем примере кода создается объект активации для приемника файла.</span><span class="sxs-lookup"><span data-stu-id="753a2-312">The following code example creates the activation object for the file sink.</span></span>


```C++
    //Create the activation object for the  file sink
    hr = MFCreateASFMediaSinkActivate(sURL, pContentInfo, &pActivate);
    if (FAILED(hr))
    {
        goto done;
    }

```



## <a name="build-the-partial-encoding-topology"></a><span data-ttu-id="753a2-313">Создание топологии частичной кодировки</span><span class="sxs-lookup"><span data-stu-id="753a2-313">Build the Partial Encoding Topology</span></span>

<span data-ttu-id="753a2-314">Далее предстоит создать топологию с частичным кодированием, создав узлы топологии для источника мультимедиа, необходимые кодировщики Windows Media и приемник ASF-файлов.</span><span class="sxs-lookup"><span data-stu-id="753a2-314">Next, you will build a partial encoding topology by creating topology nodes for the media source, the required Windows Media encoders, and the ASF file sink.</span></span> <span data-ttu-id="753a2-315">После добавления узлов топологии вы подключаете узлы источника, преобразования и приемника.</span><span class="sxs-lookup"><span data-stu-id="753a2-315">After adding the topology nodes, you will connect the source, transform, and the sink nodes.</span></span> <span data-ttu-id="753a2-316">Перед добавлением узлов топологии необходимо создать пустой объект Topology, вызвав [**мфкреатетопологи**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology).</span><span class="sxs-lookup"><span data-stu-id="753a2-316">Before adding topology nodes, you must create an empty topology object by calling [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology).</span></span>

### <a name="create-the-source-topology-node-for-the-media-source"></a><span data-ttu-id="753a2-317">Создание исходного узла топологии для источника мультимедиа</span><span class="sxs-lookup"><span data-stu-id="753a2-317">Create the Source Topology Node for the Media Source</span></span>

<span data-ttu-id="753a2-318">На этом шаге вы создадите узел топологии источника для источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="753a2-318">In this step, you will create the source topology node for the media source.</span></span>

<span data-ttu-id="753a2-319">Для создания этого узла необходимы следующие ссылки:</span><span class="sxs-lookup"><span data-stu-id="753a2-319">To create this node you need the following references:</span></span>

-   <span data-ttu-id="753a2-320">Указатель на источник мультимедиа, созданный на шаге, описанном в разделе "Создание источника мультимедиа" этого руководства.</span><span class="sxs-lookup"><span data-stu-id="753a2-320">A pointer to the media source that you created in the step described in the "Create the Media Source" section of this tutorial.</span></span>
-   <span data-ttu-id="753a2-321">Указатель на дескриптор представления для источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="753a2-321">A pointer to the presentation descriptor for the media source.</span></span> <span data-ttu-id="753a2-322">Ссылку на интерфейс Имфпресентатиондескриптор источника мультимедиа можно получить, вызвав [**имфмедиасаурце:: креатепресентатиондескриптор**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span><span class="sxs-lookup"><span data-stu-id="753a2-322">You can get a reference to IMFPresentationDescriptor interface of the media source by calling [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span></span>
-   <span data-ttu-id="753a2-323">Указатель на дескриптор потока для каждого потока в источнике мультимедиа, для которого был создан целевой поток на шаге, описанном в разделе "Создание объекта профиля ASF" этого руководства.</span><span class="sxs-lookup"><span data-stu-id="753a2-323">A pointer to the stream descriptor for each stream in the media source for which you have created a target stream in the step described in the "Create the ASF Profile Object" section of this tutorial.</span></span>

<span data-ttu-id="753a2-324">Дополнительные сведения о создании исходных узлов и пример кода см. в разделе [Создание исходных узлов](creating-source-nodes.md).</span><span class="sxs-lookup"><span data-stu-id="753a2-324">For more information about creating source nodes and code example, see [Creating Source Nodes](creating-source-nodes.md).</span></span>

<span data-ttu-id="753a2-325">В следующем примере кода создается частичная топология путем добавления исходного узла и требуемых узлов преобразования.</span><span class="sxs-lookup"><span data-stu-id="753a2-325">The following code example creates a partial topology by adding the source node and the required transform nodes.</span></span> <span data-ttu-id="753a2-326">Этот код вызывает вспомогательные функции Аддсаурценоде и Аддтрансформаутпутнодес.</span><span class="sxs-lookup"><span data-stu-id="753a2-326">This code calls the helper functions AddSourceNode, and AddTransformOutputNodes.</span></span> <span data-ttu-id="753a2-327">Эти функции включены далее в этом руководстве.</span><span class="sxs-lookup"><span data-stu-id="753a2-327">These functions are included later in this tutorial.</span></span>


```C++
//-------------------------------------------------------------------
//  BuildPartialTopology
//  Create a partial encoding topology by adding the source and the sink.
//
//  pSource:  A pointer to the media source to enumerate the source streams.
//  pSinkActivate: A pointer to the activation object for ASF file sink.
//  ppTopology:  Receives a pointer to the topology.
//-------------------------------------------------------------------

HRESULT BuildPartialTopology(
       IMFMediaSource *pSource, 
       IMFActivate* pSinkActivate,
       IMFTopology** ppTopology)
{
    if (!pSource || !pSinkActivate)
    {
        return E_INVALIDARG;
    }
    if (!ppTopology)
    {
        return E_POINTER;
    }

    HRESULT hr = S_OK;

    IMFPresentationDescriptor* pPD = NULL;
    IMFStreamDescriptor *pStreamDesc = NULL;
    IMFMediaTypeHandler* pMediaTypeHandler = NULL;
    IMFMediaType* pSrcType = NULL;

    IMFTopology* pTopology = NULL;
    IMFTopologyNode* pSrcNode = NULL;
    IMFTopologyNode* pEncoderNode = NULL;
    IMFTopologyNode* pOutputNode = NULL;


    DWORD cElems = 0;
    DWORD dwSrcStream = 0;
    DWORD StreamID = 0;
    GUID guidMajor = GUID_NULL;
    BOOL fSelected = FALSE;


    //Create the topology that represents the encoding pipeline
    hr = MFCreateTopology (&pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

        
    hr = pSource->CreatePresentationDescriptor(&pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pPD->GetStreamDescriptorCount(&dwSrcStream);
    if (FAILED(hr))
    {
        goto done;
    }

    for (DWORD iStream = 0; iStream < dwSrcStream; iStream++)
    {
        hr = pPD->GetStreamDescriptorByIndex(
            iStream, &fSelected, &pStreamDesc);
        if (FAILED(hr))
        {
            goto done;
        }

        if (!fSelected)
        {
            continue;
        }

        hr = AddSourceNode(pTopology, pSource, pPD, pStreamDesc, &pSrcNode);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pStreamDesc->GetMediaTypeHandler (&pMediaTypeHandler);
        if (FAILED(hr))
        {
            goto done;
        }
        
        hr = pStreamDesc->GetStreamIdentifier(&StreamID);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pMediaTypeHandler->GetMediaTypeByIndex(0, &pSrcType);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pSrcType->GetMajorType(&guidMajor);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = AddTransformOutputNodes(pTopology, pSinkActivate, pSrcType, &pEncoderNode);
        if (FAILED(hr))
        {
            goto done;
        }

        //now we have the transform node, connect it to the source node
        hr = pSrcNode->ConnectOutput(0, pEncoderNode, 0);
        if (FAILED(hr))
        {
            goto done;
        }
                

        SafeRelease(&pStreamDesc);
        SafeRelease(&pMediaTypeHandler);
        SafeRelease(&pSrcType);
        SafeRelease(&pEncoderNode);
        SafeRelease(&pOutputNode);
        guidMajor = GUID_NULL;
    }

    *ppTopology = pTopology;
   (*ppTopology)->AddRef();


    wprintf_s(L"Partial Topology Built.\n");

done:
    SafeRelease(&pStreamDesc);
    SafeRelease(&pMediaTypeHandler);
    SafeRelease(&pSrcType);
    SafeRelease(&pEncoderNode);
    SafeRelease(&pOutputNode);
    SafeRelease(&pTopology);

    return hr;
}
```



<span data-ttu-id="753a2-328">В следующем примере кода создается и добавляется узел топологии источника в топологию кодирования.</span><span class="sxs-lookup"><span data-stu-id="753a2-328">The following code example creates and adds the source topology node to the encoding topology.</span></span> <span data-ttu-id="753a2-329">Он принимает указатели на ранее созданный объект Topology, источник мультимедиа для перечисления исходных потоков, дескриптор представления источника мультимедиа и дескриптор потока источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="753a2-329">It takes pointers to a previously topology object, the media source to enumerate the source streams, the media source's presentation descriptor, and the media source's stream descriptor.</span></span> <span data-ttu-id="753a2-330">Вызывающий объект получает указатель на узел исходной топологии.</span><span class="sxs-lookup"><span data-stu-id="753a2-330">The caller receives a pointer to the source topology node.</span></span>


```C++
// Add a source node to a topology.
HRESULT AddSourceNode(
    IMFTopology *pTopology,           // Topology.
    IMFMediaSource *pSource,          // Media source.
    IMFPresentationDescriptor *pPD,   // Presentation descriptor.
    IMFStreamDescriptor *pSD,         // Stream descriptor.
    IMFTopologyNode **ppNode)         // Receives the node pointer.
{
    IMFTopologyNode *pNode = NULL;

    // Create the node.
    HRESULT hr = MFCreateTopologyNode(MF_TOPOLOGY_SOURCESTREAM_NODE, &pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the attributes.
    hr = pNode->SetUnknown(MF_TOPONODE_SOURCE, pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pNode->SetUnknown(MF_TOPONODE_PRESENTATION_DESCRIPTOR, pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pNode->SetUnknown(MF_TOPONODE_STREAM_DESCRIPTOR, pSD);
    if (FAILED(hr))
    {
        goto done;
    }
    
    // Add the node to the topology.
    hr = pTopology->AddNode(pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the pointer to the caller.
    *ppNode = pNode;
    (*ppNode)->AddRef();

done:
    SafeRelease(&pNode);
    return hr;
}
```



### <a name="instantiate-the-required-encoders-and-create-the-transform-nodes"></a><span data-ttu-id="753a2-331">Создайте экземпляры требуемых кодировщиков и создавайте узлы преобразования.</span><span class="sxs-lookup"><span data-stu-id="753a2-331">Instantiate the Required Encoders and Create the Transform Nodes</span></span>

<span data-ttu-id="753a2-332">Media Foundation конвейер не вставляет необходимые кодировщики Windows Media для потоков, которые необходимо кодировать, автоматически.</span><span class="sxs-lookup"><span data-stu-id="753a2-332">The Media Foundation pipeline does not automatically insert the required Windows Media encoders for the streams that it must encode.</span></span> <span data-ttu-id="753a2-333">Приложение должно добавить кодировщики вручную.</span><span class="sxs-lookup"><span data-stu-id="753a2-333">The application must add the encoders manually.</span></span> <span data-ttu-id="753a2-334">Для этого перечислите потоки в профиле ASF, которые были созданы на шаге, описанном в разделе "Создание объекта профиля ASF" этого руководства.</span><span class="sxs-lookup"><span data-stu-id="753a2-334">To do so, enumerate the streams in the ASF profile that you created in the step described in the "Create the ASF Profile Object" section of this tutorial.</span></span> <span data-ttu-id="753a2-335">Для каждого потока в источнике и соответствующего потока в профиле создайте экземпляр требуемых кодировщиков.</span><span class="sxs-lookup"><span data-stu-id="753a2-335">For each stream in the source and the corresponding stream in the profile, instantiate the required encoders.</span></span> <span data-ttu-id="753a2-336">Для этого шага требуется указатель на объект активации для приемника файла, созданного на шаге, описанном в подразделе "Создание приемника файлов ASF" этого руководства.</span><span class="sxs-lookup"><span data-stu-id="753a2-336">For this step, you need a pointer to the activation object for the file sink that you created in the step described in the "Create the ASF File Sink" section of this tutorial.</span></span>

<span data-ttu-id="753a2-337">Общие сведения о создании кодировщиков с помощью объектов активации см. в разделе [использование объектов активации кодировщика](using-an-encoder-s-activation-objects.md).</span><span class="sxs-lookup"><span data-stu-id="753a2-337">For an overview on creating encoders through activation objects, see [Using an Encoder's Activation Objects](using-an-encoder-s-activation-objects.md).</span></span>

<span data-ttu-id="753a2-338">Следующая процедура описывает шаги, необходимые для создания экземпляра требуемых кодировщиков.</span><span class="sxs-lookup"><span data-stu-id="753a2-338">The following procedure describes the steps required to instantiate the required encoders.</span></span>

1.  <span data-ttu-id="753a2-339">Получите ссылку на объект Контентинфо приемника, вызвав [**имфактивате:: активатеобжект**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) в приемнике файла, и затем запросите [**имфасфконтентинфо**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) из приемника файла, вызвав **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="753a2-339">Get a reference to the sink's ContentInfo object by calling [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) on the file sink activate and then querying for [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) from the file sink by calling **QueryInterface**.</span></span>
2.  <span data-ttu-id="753a2-340">Получите профиль ASF, связанный с объектом Контентинфо, вызвав [**имфасфконтентинфо:: onprofile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile).</span><span class="sxs-lookup"><span data-stu-id="753a2-340">Get the ASF profile associated with the ContentInfo object by calling [**IMFASFContentInfo::GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile).</span></span>
3.  <span data-ttu-id="753a2-341">Перечисление потоков в профиле.</span><span class="sxs-lookup"><span data-stu-id="753a2-341">Enumerate the streams in the profile.</span></span> <span data-ttu-id="753a2-342">Для этого потребуется число потоков и ссылка на интерфейс [**имфасфстреамконфиг**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) каждого потока.</span><span class="sxs-lookup"><span data-stu-id="753a2-342">For this you will need the stream count and a reference to each stream's [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) interface.</span></span>

    <span data-ttu-id="753a2-343">Вызовите следующие методы:</span><span class="sxs-lookup"><span data-stu-id="753a2-343">Call the following methods:</span></span>

    -   [<span data-ttu-id="753a2-344">**Имфасфпрофиле:: Жетстреамкаунт**</span><span class="sxs-lookup"><span data-stu-id="753a2-344">**IMFASFProfile::GetStreamCount**</span></span>](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount)
    -   [<span data-ttu-id="753a2-345">**Имфасфпрофиле:: Stream**</span><span class="sxs-lookup"><span data-stu-id="753a2-345">**IMFASFProfile::GetStream**</span></span>](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream)

4.  <span data-ttu-id="753a2-346">Для каждого потока получает основной тип и свойства кодировки потока из объекта Контентинфо.</span><span class="sxs-lookup"><span data-stu-id="753a2-346">For each stream get the major type and the stream's encoding properties from the ContentInfo object.</span></span>

    <span data-ttu-id="753a2-347">Вызовите следующие методы:</span><span class="sxs-lookup"><span data-stu-id="753a2-347">Call the following methods:</span></span>

    -   [<span data-ttu-id="753a2-348">**Имфасфстреамконфиг:: Жетмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="753a2-348">**IMFASFStreamConfig::GetMediaType**</span></span>](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getmediatype)
    -   [<span data-ttu-id="753a2-349">**Имфмедиатипе:: Жетмажортипе**</span><span class="sxs-lookup"><span data-stu-id="753a2-349">**IMFMediaType::GetMajorType**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype)
    -   [<span data-ttu-id="753a2-350">**Имфасфконтентинфо:: Жетенкодингконфигуратионпропертисторе**</span><span class="sxs-lookup"><span data-stu-id="753a2-350">**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**</span></span>](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore)

        <span data-ttu-id="753a2-351">Для этого вызова требуется номер потока, полученный вызовом [**имфасфпрофиле:: Stream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) .</span><span class="sxs-lookup"><span data-stu-id="753a2-351">For this call you need the stream number retrieved by the [**IMFASFProfile::GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) call.</span></span>

5.  <span data-ttu-id="753a2-352">В зависимости от типа потока, аудио или видео создайте экземпляр объекта активации для кодировщика, вызвав [**мфкреатевмаенкодерактивате**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) или [**мфкреатевмвенкодерактивате**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate).</span><span class="sxs-lookup"><span data-stu-id="753a2-352">Depending on the type of the stream, audio or video, instantiate the activation object for the encoder by calling [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) or [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate).</span></span>

    <span data-ttu-id="753a2-353">Для вызова этих функций необходимы следующие ссылки:</span><span class="sxs-lookup"><span data-stu-id="753a2-353">To call these functions, you need the following references:</span></span>

    -   <span data-ttu-id="753a2-354">Указатель на тип мультимедиа потока, полученный с помощью [**имфасфстреамконфиг:: жетмедиатипе**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getmediatype) на предыдущем шаге.</span><span class="sxs-lookup"><span data-stu-id="753a2-354">A pointer to the stream's media type retrieved by [**IMFASFStreamConfig::GetMediaType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getmediatype) in the previous step.</span></span>
    -   <span data-ttu-id="753a2-355">Указатель на хранилище свойств кодирования потока, полученное с помощью [**имфасфконтентинфо:: жетенкодингконфигуратионпропертисторе**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore).</span><span class="sxs-lookup"><span data-stu-id="753a2-355">A pointer to the stream's encoding property store retrieved by [**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore).</span></span> <span data-ttu-id="753a2-356">Передавая указатель на хранилище свойств, свойства потока, заданные в приемнике файла, копируются в файл MFT кодировщика.</span><span class="sxs-lookup"><span data-stu-id="753a2-356">By passing a pointer to the property store, the stream properties set in the file sink are copied on the encoder MFT.</span></span>

6.  <span data-ttu-id="753a2-357">Обновите параметр контейнера с утечкой для аудиопотока.</span><span class="sxs-lookup"><span data-stu-id="753a2-357">Update the leaky bucket parameter for the audio stream.</span></span>

    <span data-ttu-id="753a2-358">[**Мфкреатевмаенкодерактивате**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) задает тип выходных данных для основного файла MFT кодировщика для аудиокодека Windows Media Audio.</span><span class="sxs-lookup"><span data-stu-id="753a2-358">[**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) sets the output type on the underlying encoder MFT for the Windows Media audio codec.</span></span> <span data-ttu-id="753a2-359">После того как выходной тип носителя установлен, кодировщик получает среднюю скорость потока из выходного типа носителя, вычисляет скорость поразрядного окна буфера и устанавливает значения сегментов утечки, которые будут использоваться во время сеанса кодирования.</span><span class="sxs-lookup"><span data-stu-id="753a2-359">After the output media type is set, the encoder gets the average bit rate from the output media type, calculates the buffer window rage bit rate, and sets the leaky bucket values that will be used during the encoding session.</span></span> <span data-ttu-id="753a2-360">Эти значения можно обновить в приемнике файлов, запросив кодировщика или задавая пользовательские значения.</span><span class="sxs-lookup"><span data-stu-id="753a2-360">You can update these values in the file sink by either querying the encoder or setting custom values.</span></span> <span data-ttu-id="753a2-361">Чтобы обновить значения, требуется следующий набор данных:</span><span class="sxs-lookup"><span data-stu-id="753a2-361">To update values you need the following set of information:</span></span>

    -   <span data-ttu-id="753a2-362">Средняя скорость потока: средняя скорость по скорости от среднего числа [**\_ байт MF \_ в \_ \_ \_ \_ секунду**](mf-mt-audio-avg-bytes-per-second-attribute.md) , заданных для типа выходного носителя, выбранного при согласовании типа носителя.</span><span class="sxs-lookup"><span data-stu-id="753a2-362">Average bit rate: Get the average bit rate from the [**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**](mf-mt-audio-avg-bytes-per-second-attribute.md) attribute set on the output media type that is selected during media type negotiation.</span></span>
    -   <span data-ttu-id="753a2-363">Окно буфера. его можно извлечь, вызвав [**ивмкодеклеакибуккет:: жетбуфферсизебитс**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md).</span><span class="sxs-lookup"><span data-stu-id="753a2-363">Buffer window: you can retrieve it by calling [**IWMCodecLeakyBucket::GetBufferSizeBits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md).</span></span>
    -   <span data-ttu-id="753a2-364">Начальный размер буфера: значение 0.</span><span class="sxs-lookup"><span data-stu-id="753a2-364">Initial buffer size: Set to 0.</span></span>

    <span data-ttu-id="753a2-365">Создайте массив значений типа DWORD и задайте значение в свойстве [**мфпкэй \_ асфстреамсинк \_ исправлен \_ леакибуккет**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) приемника аудиопотока.</span><span class="sxs-lookup"><span data-stu-id="753a2-365">Create an array of DWORDs and set the value in the [**MFPKEY\_ASFSTREAMSINK\_CORRECTED\_LEAKYBUCKET**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) property of the audio stream sink.</span></span> <span data-ttu-id="753a2-366">Если не указать обновленные значения, сеанс мультимедиа задает их соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="753a2-366">If you do not provide the updated values, the Media Session sets them appropriately.</span></span>

    <span data-ttu-id="753a2-367">Дополнительные сведения см. [в разделе Модель буфера для сегмента утечки](the-leaky-bucket-buffer-model.md).</span><span class="sxs-lookup"><span data-stu-id="753a2-367">For more information, see [The Leaky Bucket Buffer Model](the-leaky-bucket-buffer-model.md).</span></span>

<span data-ttu-id="753a2-368">Объекты активации, созданные на шаге 5, должны быть добавлены в топологию как узлы топологии преобразования.</span><span class="sxs-lookup"><span data-stu-id="753a2-368">The activation objects created in step 5 must be added to the topology as transform topology nodes.</span></span> <span data-ttu-id="753a2-369">Дополнительные сведения и пример кода см. в разделе «Создание узла преобразования из объекта активации» раздела [Создание узлов преобразования](creating-transform-nodes.md).</span><span class="sxs-lookup"><span data-stu-id="753a2-369">For more information and code example, see "Creating a Transform Node from an Activation Object" in [Creating Transform Nodes](creating-transform-nodes.md).</span></span>

<span data-ttu-id="753a2-370">В следующем примере кода создается и добавляется требуемый кодировщик.</span><span class="sxs-lookup"><span data-stu-id="753a2-370">The following code example creates and adds the required encoder activates.</span></span> <span data-ttu-id="753a2-371">Он принимает указатели на ранее созданный объект Topology, объект активации приемника файла и тип носителя исходного потока.</span><span class="sxs-lookup"><span data-stu-id="753a2-371">It takes pointers to a previously created topology object, the file sink's activation object and the source stream's media type.</span></span> <span data-ttu-id="753a2-372">Он также вызывает Аддаутпутноде (см. Следующий пример кода), который создает и добавляет узел приемника в топологию кодирования.</span><span class="sxs-lookup"><span data-stu-id="753a2-372">It also calls AddOutputNode (see next code example) that creates and adds the sink node to the encoding topology.</span></span> <span data-ttu-id="753a2-373">Вызывающий объект получает указатель на узел исходной топологии.</span><span class="sxs-lookup"><span data-stu-id="753a2-373">It The caller receives a pointer to the source topology node.</span></span>


```C++
//-------------------------------------------------------------------
//  AddTransformOutputNodes
//  Creates and adds the sink node to the encoding topology.
//  Creates and adds the required encoder activates.

//  pTopology:  A pointer to the topology.
//  pSinkActivate:  A pointer to the file sink's activation object.
//  pSourceType: A pointer to the source stream's media type.
//  ppNode:  Receives a pointer to the topology node.
//-------------------------------------------------------------------

HRESULT AddTransformOutputNodes(
    IMFTopology* pTopology,
    IMFActivate* pSinkActivate,
    IMFMediaType* pSourceType,
    IMFTopologyNode **ppNode    // Receives the node pointer.
    )
{
    if (!pTopology || !pSinkActivate || !pSourceType)
    {
        return E_INVALIDARG;
    }

    IMFTopologyNode* pEncNode = NULL;
    IMFTopologyNode* pOutputNode = NULL;
    IMFASFContentInfo* pContentInfo = NULL;
    IMFASFProfile* pProfile = NULL;
    IMFASFStreamConfig* pStream = NULL;
    IMFMediaType* pMediaType = NULL;
    IPropertyStore* pProps = NULL;
    IMFActivate *pEncoderActivate = NULL;
    IMFMediaSink *pSink = NULL; 

    GUID guidMT = GUID_NULL;
    GUID guidMajor = GUID_NULL;

    DWORD cStreams = 0;
    WORD wStreamNumber = 0;

    HRESULT hr = S_OK;
        
    hr = pSourceType->GetMajorType(&guidMajor);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the node.
    hr = MFCreateTopologyNode(MF_TOPOLOGY_TRANSFORM_NODE, &pEncNode);
    if (FAILED(hr))
    {
        goto done;
    }
    
    //Activate the sink
    hr = pSinkActivate->ActivateObject(__uuidof(IMFMediaSink), (void**)&pSink);
    if (FAILED(hr))
    {
        goto done;
    }
    //find the media type in the sink
    //Get content info from the sink
    hr = pSink->QueryInterface(__uuidof(IMFASFContentInfo), (void**)&pContentInfo);
    if (FAILED(hr))
    {
        goto done;
    }
    

    hr = pContentInfo->GetProfile(&pProfile);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pProfile->GetStreamCount(&cStreams);
    if (FAILED(hr))
    {
        goto done;
    }

    for(DWORD index = 0; index < cStreams ; index++)
    {
        hr = pProfile->GetStream(index, &wStreamNumber, &pStream);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = pStream->GetMediaType(&pMediaType);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = pMediaType->GetMajorType(&guidMT);
        if (FAILED(hr))
        {
            goto done;
        }
        if (guidMT!=guidMajor)
        {
            SafeRelease(&pStream);
            SafeRelease(&pMediaType);
            guidMT = GUID_NULL;

            continue;
        }
        //We need to activate the encoder
        hr = pContentInfo->GetEncodingConfigurationPropertyStore(wStreamNumber, &pProps);
        if (FAILED(hr))
        {
            goto done;
        }

        if (guidMT == MFMediaType_Audio)
        {
             hr = MFCreateWMAEncoderActivate(pMediaType, pProps, &pEncoderActivate);
            if (FAILED(hr))
            {
                goto done;
            }
            wprintf_s(L"Audio Encoder created. Stream Number: %d .\n", wStreamNumber);

            break;
        }
        if (guidMT == MFMediaType_Video)
        {
            hr = MFCreateWMVEncoderActivate(pMediaType, pProps, &pEncoderActivate);
            if (FAILED(hr))
            {
                goto done;
            }
            wprintf_s(L"Video Encoder created. Stream Number: %d .\n", wStreamNumber);

            break;
        }
    }

    // Set the object pointer.
    hr = pEncNode->SetObject(pEncoderActivate);
    if (FAILED(hr))
    {
        goto done;
    }

    // Add the node to the topology.
    hr = pTopology->AddNode(pEncNode);
    if (FAILED(hr))
    {
        goto done;
    }

    //Add the output node to this node.
    hr = AddOutputNode(pTopology, pSinkActivate, wStreamNumber, &pOutputNode);
    if (FAILED(hr))
    {
        goto done;
    }

    //now we have the output node, connect it to the transform node
    hr = pEncNode->ConnectOutput(0, pOutputNode, 0);
    if (FAILED(hr))
    {
        goto done;
    }

   // Return the pointer to the caller.
    *ppNode = pEncNode;
    (*ppNode)->AddRef();


done:
    SafeRelease(&pEncNode);
    SafeRelease(&pOutputNode);
    SafeRelease(&pEncoderActivate);
    SafeRelease(&pMediaType);
    SafeRelease(&pProps);
    SafeRelease(&pStream);
    SafeRelease(&pProfile);
    SafeRelease(&pContentInfo);
    SafeRelease(&pSink);
    return hr;
}
```



### <a name="create-the-output-topology-nodes-for-the-file-sink"></a><span data-ttu-id="753a2-374">Создание выходных узлов топологии для приемника файлов</span><span class="sxs-lookup"><span data-stu-id="753a2-374">Create the Output Topology Nodes for the File Sink</span></span>

<span data-ttu-id="753a2-375">На этом шаге вы создадите узел выходной топологии для приемника файлов ASF.</span><span class="sxs-lookup"><span data-stu-id="753a2-375">In this step, you will create the output topology node for the ASF file sink.</span></span>

<span data-ttu-id="753a2-376">Для создания этого узла необходимы следующие ссылки:</span><span class="sxs-lookup"><span data-stu-id="753a2-376">To create this node you need the following references:</span></span>

-   <span data-ttu-id="753a2-377">Указатель на объект активации, созданный на шаге, описанном в подразделе "Создание приемника файлов ASF" этого руководства.</span><span class="sxs-lookup"><span data-stu-id="753a2-377">A pointer to the activation object that you created in the step described in the "Create the ASF File Sink" section of this tutorial.</span></span>
-   <span data-ttu-id="753a2-378">Номера потоков для обнаружения приемников потока, добавляемых в приемник файла.</span><span class="sxs-lookup"><span data-stu-id="753a2-378">The stream numbers to identify the stream sinks added to the file sink.</span></span> <span data-ttu-id="753a2-379">Номера потоков соответствуют идентификации потока, установленного во время создания потока.</span><span class="sxs-lookup"><span data-stu-id="753a2-379">The stream numbers match the stream's identification that was set during stream creation.</span></span>

<span data-ttu-id="753a2-380">Дополнительные сведения о создании выходных узлов и пример кода см. в разделе «Создание выходного узла из объекта активации» раздела [Создание выходных узлов](creating-output-nodes.md).</span><span class="sxs-lookup"><span data-stu-id="753a2-380">For more information about creating output nodes and code example, see "Creating an Output Node from an Activation Object" in [Creating Output Nodes](creating-output-nodes.md).</span></span>

<span data-ttu-id="753a2-381">Если вы не используете объект активации для приемника файла, необходимо перечислить приемники потока в приемнике файлов ASF и установить каждый приемник потока в качестве выходного узла в топологии.</span><span class="sxs-lookup"><span data-stu-id="753a2-381">If you are not using activation object for the file sink, you must enumerate the stream sinks in the ASF file sink and set each stream sink as the output node in the topology.</span></span> <span data-ttu-id="753a2-382">Дополнительные сведения о перечислении приемников потоков см. в разделе "Перечисление приемников потоков" статьи [Добавление потоковых данных в приемник файлов ASF](adding-stream-information-to-the-asf-file-sink.md).</span><span class="sxs-lookup"><span data-stu-id="753a2-382">For information about stream sink enumeration, see "Enumerating Stream Sinks" in [Adding Stream Information to the ASF File Sink](adding-stream-information-to-the-asf-file-sink.md).</span></span>

<span data-ttu-id="753a2-383">В следующем примере кода создается и добавляется узел приемника в топологию кодирования.</span><span class="sxs-lookup"><span data-stu-id="753a2-383">The following code example creates and adds the sink node to the encoding topology.</span></span> <span data-ttu-id="753a2-384">Он принимает указатели на ранее созданный объект Topology, объект активации приемника файла и идентификационный номер потока.</span><span class="sxs-lookup"><span data-stu-id="753a2-384">It takes pointers to a previously created topology object, the file sink's activation object and the stream's identification number.</span></span> <span data-ttu-id="753a2-385">Вызывающий объект получает указатель на узел исходной топологии.</span><span class="sxs-lookup"><span data-stu-id="753a2-385">It The caller receives a pointer to the source topology node.</span></span>


```C++
// Add an output node to a topology.
HRESULT AddOutputNode(
    IMFTopology *pTopology,     // Topology.
    IMFActivate *pActivate,     // Media sink activation object.
    DWORD dwId,                 // Identifier of the stream sink.
    IMFTopologyNode **ppNode)   // Receives the node pointer.
{
    IMFTopologyNode *pNode = NULL;

    // Create the node.
    HRESULT hr = MFCreateTopologyNode(MF_TOPOLOGY_OUTPUT_NODE, &pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the object pointer.
    hr = pNode->SetObject(pActivate);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the stream sink ID attribute.
    hr = pNode->SetUINT32(MF_TOPONODE_STREAMID, dwId);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pNode->SetUINT32(MF_TOPONODE_NOSHUTDOWN_ON_REMOVE, FALSE);
    if (FAILED(hr))
    {
        goto done;
    }

    // Add the node to the topology.
    hr = pTopology->AddNode(pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the pointer to the caller.
    *ppNode = pNode;
    (*ppNode)->AddRef();

done:
    SafeRelease(&pNode);
    return hr;
}
```



<span data-ttu-id="753a2-386">В следующем примере кода перечисляются приемники потока для заданного приемника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="753a2-386">The following code example enumerates the stream sinks for a given media sink.</span></span>


```C++
//-------------------------------------------------------------------
//  EnumerateStreamSinks
//  Enumerates the stream sinks within the specified media sink.
//
//  pSink:  A pointer to the media sink.
//-------------------------------------------------------------------
HRESULT EnumerateStreamSinks (IMFMediaSink* pSink)
{
    if (!pSink)
    {
        return E_INVALIDARG;
    }
    
    IMFStreamSink* pStreamSink = NULL;
    DWORD cStreamSinks = 0;

    HRESULT hr = pSink->GetStreamSinkCount(&cStreamSinks);
    if (FAILED(hr))
    {
        goto done;
    }

    for(DWORD index = 0; index < cStreamSinks; index++)
    {
        hr = pSink->GetStreamSinkByIndex (index, &pStreamSink);
        if (FAILED(hr))
        {
            goto done;
        }

        //Use the stream sink
        //Not shown.
    }
done:
    SafeRelease(&pStreamSink);

    return hr;
}
```



### <a name="connect-the-source-transform-and-sink-nodes"></a><span data-ttu-id="753a2-387">Подключение узлов источника, преобразования и приемника</span><span class="sxs-lookup"><span data-stu-id="753a2-387">Connect the Source, Transform, and Sink Nodes</span></span>

<span data-ttu-id="753a2-388">На этом шаге вы подключаете исходный узел к узлу преобразования, который ссылается на кодировку, которая активируется на шаге, описанном в разделе "создание экземпляров необходимых кодировщиков и создание узлов преобразования" этого руководства.</span><span class="sxs-lookup"><span data-stu-id="753a2-388">In this step, you will connect the source node to the transform node referencing the encoding activates that you created in the step described in the "Instantiate the Required Encoders and Create the Transform Nodes" section of this tutorial.</span></span> <span data-ttu-id="753a2-389">Узел преобразования будет подключен к выходному узлу, содержащему объект активации для приемника файла.</span><span class="sxs-lookup"><span data-stu-id="753a2-389">The transform node will be connected to the output node containing the activation object for the file sink.</span></span>

## <a name="handling-the-encoding-session"></a><span data-ttu-id="753a2-390">Обработка сеанса кодирования</span><span class="sxs-lookup"><span data-stu-id="753a2-390">Handling the Encoding Session</span></span>

<span data-ttu-id="753a2-391">На этом шаге выполняются следующие действия.</span><span class="sxs-lookup"><span data-stu-id="753a2-391">In the step, you will perform the following steps:</span></span>

1.  <span data-ttu-id="753a2-392">Вызовите [**мфкреатемедиасессион**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) , чтобы создать сеанс кодирования.</span><span class="sxs-lookup"><span data-stu-id="753a2-392">Call [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) to create an encoding session.</span></span>
2.  <span data-ttu-id="753a2-393">Вызовите [**имфмедиасессион:: сеттопологи**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) , чтобы задать топологию кодирования для сеанса.</span><span class="sxs-lookup"><span data-stu-id="753a2-393">Call [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) to set the encoding topology on the session.</span></span> <span data-ttu-id="753a2-394">Если вызов завершается, сеанс мультимедиа оценивает узлы топологии и вставляет дополнительные объекты преобразования, такие как декодер, который преобразует указанный сжатый источник в несжатые образцы в поток в качестве входных данных для кодировщика.</span><span class="sxs-lookup"><span data-stu-id="753a2-394">If the call completes, the Media Session evaluates the topology nodes and inserts additional transform objects such as a decoder that converts the specified compressed source to uncompressed samples to feed as input to the encoder.</span></span>
3.  <span data-ttu-id="753a2-395">Вызовите [**имфмедиасессион:: четный**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent) , чтобы запросить события, вызванные сеансом мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="753a2-395">Call [**IMFMediaSession::GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent) to request for the events raised by the Media Session.</span></span>

    <span data-ttu-id="753a2-396">В цикле событий вы начнете и закроете сеанс кодирования в зависимости от событий, вызванных сеансом мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="753a2-396">In the event loop you will start and close the encoding session depending on the events raised by the Media Session.</span></span> <span data-ttu-id="753a2-397">Вызов [**имфмедиасессион:: сеттопологи**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) приводит к тому, что сеанс мультимедиа вызывает событие [месессионтопологистатус](mesessiontopologystatus.md) с \_ \_ установленным флагом подключения MF топостатус.</span><span class="sxs-lookup"><span data-stu-id="753a2-397">The [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) call results in Media Session raising the [MESessionTopologyStatus](mesessiontopologystatus.md) event with the MF\_TOPOSTATUS\_READY flag set.</span></span> <span data-ttu-id="753a2-398">Все события создаются асинхронно, и приложение может получать эти события синхронно или асинхронно.</span><span class="sxs-lookup"><span data-stu-id="753a2-398">All events are generated asynchronously and an application can retrieve these events synchronously or asynchronously.</span></span> <span data-ttu-id="753a2-399">Поскольку приложение в этом руководстве является консольным приложением и блокирует потоки пользовательского интерфейса, мы будем получать события из сеанса мультимедиа синхронно.</span><span class="sxs-lookup"><span data-stu-id="753a2-399">Because the application in this tutorial is a console application and blocking user interface threads is not a concern, we will get the events from Media Session synchronously.</span></span>

    <span data-ttu-id="753a2-400">Для асинхронного получения событий приложение должно реализовать интерфейс [**имфасинккаллбакк**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .</span><span class="sxs-lookup"><span data-stu-id="753a2-400">To get the events asynchronously, your application must implement the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span> <span data-ttu-id="753a2-401">Дополнительные сведения и пример реализации этого интерфейса см. в разделе "обработка событий сеанса" раздела [Воспроизведение мультимедийных файлов с помощью Media Foundation](how-to-play-unprotected-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="753a2-401">For more information and an example implementation of this interface, see "Handling Session Events" in [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md).</span></span>

<span data-ttu-id="753a2-402">В цикле событий для получения событий сеанса мультимедиа дождитесь события [месессионтопологистатус](mesessiontopologystatus.md) , которое возникает при завершении [**Имфмедиасессион:: сеттопологи**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) и разрешении топологии.</span><span class="sxs-lookup"><span data-stu-id="753a2-402">In the event loop for getting Media Session events, wait for the [MESessionTopologyStatus](mesessiontopologystatus.md) event that is raised when the [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) completes and the topology is resolved.</span></span> <span data-ttu-id="753a2-403">После получения события Месессионтопологистатус запустите сеанс кодирования, вызвав [**имфмедиасессион:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span><span class="sxs-lookup"><span data-stu-id="753a2-403">Upon getting the MESessionTopologyStatus event, start the encoding session by calling [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span></span> <span data-ttu-id="753a2-404">Сеанс мультимедиа создает событие [миндофпресентатион](meendofpresentation.md) при завершении всех операций кодирования.</span><span class="sxs-lookup"><span data-stu-id="753a2-404">The Media Session generates the [MEEndOfPresentation](meendofpresentation.md) event when all of the encoding operations are complete.</span></span> <span data-ttu-id="753a2-405">Это событие должно быть обработано для кодирования VBR и рассматривается в следующем разделе "Обновление свойств кодировки в приемнике файлов для кодирования VBR" этого руководства.</span><span class="sxs-lookup"><span data-stu-id="753a2-405">This event must be handled for VBR encoding and is discussed in the next section "Update Encoding Properties on the File Sink for VBR Encoding" of this tutorial.</span></span>

<span data-ttu-id="753a2-406">Сеанс мультимедиа создает объект заголовка ASF и завершает файл после завершения сеанса кодирования, а затем вызывает событие [месессионклосед](mesessionclosed.md) .</span><span class="sxs-lookup"><span data-stu-id="753a2-406">The Media Session generates the ASF Header Object and finalizes the file when the encoding session completes and then raises the [MESessionClosed](mesessionclosed.md) event.</span></span> <span data-ttu-id="753a2-407">Это событие должно быть обработано путем выполнения правильных операций завершения работы в сеансе мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="753a2-407">This event must be handled by performing proper shutdown operations on the Media Session.</span></span> <span data-ttu-id="753a2-408">Чтобы начать операцию завершения работы, вызовите метод [**имфмедиасессион:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).</span><span class="sxs-lookup"><span data-stu-id="753a2-408">To begin the shutdown operations, call [**IMFMediaSession::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).</span></span> <span data-ttu-id="753a2-409">После закрытия сеанса кодирования нельзя задать другую топологию для кодирования в том же экземпляре сеанса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="753a2-409">After the encoding session is closed, you cannot set another topology for encoding on the same Media Session instance.</span></span> <span data-ttu-id="753a2-410">Для кодирования другого файла текущий сеанс мультимедиа должен быть закрыт и освобожден, а новая топология должна быть установлена во вновь созданном сеансе мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="753a2-410">To encode another file, the current Media Session must be closed and released and the new topology must be set on a newly created Media Session.</span></span> <span data-ttu-id="753a2-411">В следующем примере кода создается сеанс мультимедиа, задается топология кодирования и обрабатываются события сеанса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="753a2-411">The following code example creates the Media Session, sets the encoding topology and handles the Media Session events.</span></span>

<span data-ttu-id="753a2-412">В следующем примере кода создается сеанс мультимедиа, задается топология кодирования и осуществляется управление сеансом кодирования путем обработки событий из сеанса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="753a2-412">The following code example creates the Media Session, sets the encoding topology, and controls the encoding session by handling events from the Media Session.</span></span>


```C++
//-------------------------------------------------------------------
//  Encode
//  Controls the encoding session and handles events from the media session.
//
//  pTopology:  A pointer to the encoding topology.
//-------------------------------------------------------------------

HRESULT Encode(IMFTopology *pTopology)
{
    if (!pTopology)
    {
        return E_INVALIDARG;
    }
    
    IMFMediaSession *pSession = NULL;
    IMFMediaEvent* pEvent = NULL;
    IMFTopology* pFullTopology = NULL;
    IUnknown* pTopoUnk = NULL;


    MediaEventType meType = MEUnknown;  // Event type

    HRESULT hr = S_OK;
    HRESULT hrStatus = S_OK;            // Event status
                
    MF_TOPOSTATUS TopoStatus = MF_TOPOSTATUS_INVALID; // Used with MESessionTopologyStatus event.    
        

    hr = MFCreateMediaSession(NULL, &pSession);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSession->SetTopology(MFSESSION_SETTOPOLOGY_IMMEDIATE, pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    //Get media session events synchronously
    while (1)
    {
        hr = pSession->GetEvent(0, &pEvent);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pEvent->GetType(&meType);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pEvent->GetStatus(&hrStatus);
        if (FAILED(hr))
        {
            goto done;
        }
        if (FAILED(hrStatus))
        {
            hr = hrStatus;
            goto done;
        }

       switch(meType)
        {
            case MESessionTopologyStatus:
                {
                    // Get the status code.
                    MF_TOPOSTATUS status = (MF_TOPOSTATUS)MFGetAttributeUINT32(
                                             pEvent, MF_EVENT_TOPOLOGY_STATUS, MF_TOPOSTATUS_INVALID);

                    if (status == MF_TOPOSTATUS_READY)
                    {
                        PROPVARIANT var;
                        PropVariantInit(&var);
                        wprintf_s(L"Topology resolved and set on the media session.\n");

                        hr = pSession->Start(NULL, &var);
                        if (FAILED(hr))
                        {
                            goto done;
                        }

                    }
                    if (status == MF_TOPOSTATUS_STARTED_SOURCE)
                    {
                        wprintf_s(L"Encoding started.\n");
                        break;
                    }
                    if (status == MF_TOPOSTATUS_ENDED)
                    {
                        wprintf_s(L"Encoding complete.\n");
                        hr = pSession->Close();
                        if (FAILED(hr))
                        {
                            goto done;
                        }

                        break;
                    }
                }
                break;


            case MESessionEnded:
                wprintf_s(L"Encoding complete.\n");
                hr = pSession->Close();
                if (FAILED(hr))
                {
                    goto done;
                }
                break;

            case MEEndOfPresentation:
                {
                    if (EncodingMode == VBR)
                    {
                        hr = pSession->GetFullTopology(MFSESSION_GETFULLTOPOLOGY_CURRENT, 0, &pFullTopology);
                        if (FAILED(hr))
                        {
                            goto done;
                        }
                        hr = PostEncodingUpdate(pFullTopology);
                        if (FAILED(hr))
                        {
                            goto done;
                        }
                        wprintf_s(L"Updated sinks for VBR. \n");
                    }
                }
                break;

            case MESessionClosed:
                wprintf_s(L"Encoding session closed.\n");

                hr = pSession->Shutdown();
                goto done;
        }
        if (FAILED(hr))
        {
            goto done;
        }

        SafeRelease(&pEvent);

    }
done:
    SafeRelease(&pEvent);
    SafeRelease(&pSession);
    SafeRelease(&pFullTopology);
    SafeRelease(&pTopoUnk);
    return hr;
}
```



## <a name="update-encoding-properties-in-the-file-sink"></a><span data-ttu-id="753a2-413">Обновление свойств кодировки в приемнике файла</span><span class="sxs-lookup"><span data-stu-id="753a2-413">Update Encoding Properties in the File Sink</span></span>

<span data-ttu-id="753a2-414">Некоторые свойства кодировки, такие как скорость кодирования и точные значения сегментов утечки, неизвестны до завершения кодирования, особенно для кодирования VBR.</span><span class="sxs-lookup"><span data-stu-id="753a2-414">Certain encoding properties such as the encoding bit rate and the accurate leaky bucket values are not known until the encoding is complete, especially for VBR encoding.</span></span> <span data-ttu-id="753a2-415">Чтобы получить правильные значения, приложение должно подождать события [миндофпресентатион](meendofpresentation.md) , указывающего на то, что сеанс кодирования завершен.</span><span class="sxs-lookup"><span data-stu-id="753a2-415">To get the correct values the application must wait for the [MEEndOfPresentation](meendofpresentation.md) event that indicates that the encoding session is complete.</span></span> <span data-ttu-id="753a2-416">Значения контейнеров утечки необходимо обновить в приемнике, чтобы объект заголовка ASF мог отражать точные значения.</span><span class="sxs-lookup"><span data-stu-id="753a2-416">The leaky bucket values must be updated in the sink so that the ASF Header Object can reflect the accurate values.</span></span>

<span data-ttu-id="753a2-417">Следующая процедура описывает шаги, необходимые для прохода по узлам в топологии кодирования, чтобы получить узел приемника файлов и задать необходимые свойства сегмента утечки.</span><span class="sxs-lookup"><span data-stu-id="753a2-417">The following procedure describes the steps required to traverse the nodes in the encoding topology to get the file sink node and set the required leaky bucket properties.</span></span>

<span data-ttu-id="753a2-418">**Обновление значений свойств кодировки POST в приемнике файлов ASF**</span><span class="sxs-lookup"><span data-stu-id="753a2-418">**To update the post encoding property values on the ASF file sink**</span></span>

1.  <span data-ttu-id="753a2-419">Вызовите метод [**имфтопологи:: жетаутпутнодеколлектион**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-getoutputnodecollection) , чтобы получить коллекцию выходных узлов из топологии кодирования.</span><span class="sxs-lookup"><span data-stu-id="753a2-419">Call [**IMFTopology::GetOutputNodeCollection**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-getoutputnodecollection) to get the output node collection from the encoding topology.</span></span>
2.  <span data-ttu-id="753a2-420">Для каждого узла получите указатель на приемник потока в узле, вызвав [**имфтопологиноде:: GetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getobject).</span><span class="sxs-lookup"><span data-stu-id="753a2-420">For each node, get a pointer to the stream sink in the node by calling [**IMFTopologyNode::GetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getobject).</span></span> <span data-ttu-id="753a2-421">Запрос интерфейса [**имфстреамсинк**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) для указателя [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) , возвращаемого методом **имфтопологиноде:: GetObject**.</span><span class="sxs-lookup"><span data-stu-id="753a2-421">Query for the [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) interface on the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) pointer returned by **IMFTopologyNode::GetObject**.</span></span>
3.  <span data-ttu-id="753a2-422">Для каждого приемника потока получите нисходящий узел (кодировщик), вызвав [**имфтопологиноде:: input**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getinput).</span><span class="sxs-lookup"><span data-stu-id="753a2-422">For each stream sink get the downstream node (encoder) by calling [**IMFTopologyNode::GetInput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getinput).</span></span>
4.  <span data-ttu-id="753a2-423">Запросите узел, чтобы получить указатель [**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) из узла кодировщика.</span><span class="sxs-lookup"><span data-stu-id="753a2-423">Query the node to get the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) pointer from the encoder node.</span></span>
5.  <span data-ttu-id="753a2-424">Запросите у кодировщика указатель [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore) , чтобы получить хранилище свойств кодирования из кодировщика.</span><span class="sxs-lookup"><span data-stu-id="753a2-424">Query the encoder for the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer to get the encoding property store from the encoder.</span></span>
6.  <span data-ttu-id="753a2-425">Запросите приемник потока для указателя [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore) , чтобы получить хранилище свойств приемника потока.</span><span class="sxs-lookup"><span data-stu-id="753a2-425">Query the stream sink for the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer to get the stream sink's property store.</span></span>
7.  <span data-ttu-id="753a2-426">Вызовите метод [**ипропертисторе:: GetValue**](/windows/win32/api/propsys/nn-propsys-ipropertystore) , чтобы получить требуемые значения свойств из хранилища свойств кодировщика и скопировать их в хранилище свойств приемника потока, вызвав **Ипропертисторе:: SetValue**.</span><span class="sxs-lookup"><span data-stu-id="753a2-426">Call [**IPropertyStore::GetValue**](/windows/win32/api/propsys/nn-propsys-ipropertystore) to get the required property values from the encoder's property store and copy them to the stream sink's property store by calling **IPropertyStore::SetValue**.</span></span>

<span data-ttu-id="753a2-427">В следующей таблице показаны значения свойств кодировки POST, которые должны быть заданы в приемнике потока для видеопотока.</span><span class="sxs-lookup"><span data-stu-id="753a2-427">The following table shows the post encoding property values that must be set on the stream sink for the video stream.</span></span>



| <span data-ttu-id="753a2-428">Тип кодировки</span><span class="sxs-lookup"><span data-stu-id="753a2-428">Encoding type</span></span>                                                                                  | <span data-ttu-id="753a2-429">Имя свойства (GetValue)</span><span class="sxs-lookup"><span data-stu-id="753a2-429">Property name (GetValue)</span></span>                                                                        | <span data-ttu-id="753a2-430">Имя свойства (SetValue)</span><span class="sxs-lookup"><span data-stu-id="753a2-430">Property name (SetValue)</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="753a2-431">Кодирование постоянной скорости потока</span><span class="sxs-lookup"><span data-stu-id="753a2-431">Constant Bit Rate Encoding</span></span>](constant-bit-rate-encoding.md)                                   | <span data-ttu-id="753a2-432">МФПКЭЙ \_ бавг</span><span class="sxs-lookup"><span data-stu-id="753a2-432">MFPKEY\_BAVG</span></span><br/> <span data-ttu-id="753a2-433">МФПКЭЙ \_ равг</span><span class="sxs-lookup"><span data-stu-id="753a2-433">MFPKEY\_RAVG</span></span><br/>                                                 | <span data-ttu-id="753a2-434">МФПКЭЙ \_ stat \_ бавг</span><span class="sxs-lookup"><span data-stu-id="753a2-434">MFPKEY\_STAT\_BAVG</span></span><br/> <span data-ttu-id="753a2-435">МФПКЭЙ \_ stat \_ равг</span><span class="sxs-lookup"><span data-stu-id="753a2-435">MFPKEY\_STAT\_RAVG</span></span><br/>                                                             |
| [<span data-ttu-id="753a2-436">Кодирование скорости переменной с учетом качества</span><span class="sxs-lookup"><span data-stu-id="753a2-436">Quality-Based Variable Bit Rate Encoding</span></span>](quality-based-variable-bit-rate--vbr--encoding.md) | <span data-ttu-id="753a2-437">МФПКЭЙ \_ бавг</span><span class="sxs-lookup"><span data-stu-id="753a2-437">MFPKEY\_BAVG</span></span><br/> <span data-ttu-id="753a2-438">МФПКЭЙ \_ равг</span><span class="sxs-lookup"><span data-stu-id="753a2-438">MFPKEY\_RAVG</span></span><br/> <span data-ttu-id="753a2-439">МФПКЭЙ \_ бмакс</span><span class="sxs-lookup"><span data-stu-id="753a2-439">MFPKEY\_BMAX</span></span><br/> <span data-ttu-id="753a2-440">МФПКЭЙ \_ рмакс</span><span class="sxs-lookup"><span data-stu-id="753a2-440">MFPKEY\_RMAX</span></span><br/> | <span data-ttu-id="753a2-441">МФПКЭЙ \_ stat \_ бавг</span><span class="sxs-lookup"><span data-stu-id="753a2-441">MFPKEY\_STAT\_BAVG</span></span><br/> <span data-ttu-id="753a2-442">МФПКЭЙ \_ stat \_ равг</span><span class="sxs-lookup"><span data-stu-id="753a2-442">MFPKEY\_STAT\_RAVG</span></span><br/> <span data-ttu-id="753a2-443">МФПКЭЙ \_ stat \_ бмакс</span><span class="sxs-lookup"><span data-stu-id="753a2-443">MFPKEY\_STAT\_BMAX</span></span><br/> <span data-ttu-id="753a2-444">МФПКЭЙ \_ stat \_ рмакс</span><span class="sxs-lookup"><span data-stu-id="753a2-444">MFPKEY\_STAT\_RMAX</span></span><br/> |



 

<span data-ttu-id="753a2-445">В следующем примере кода задаются значения свойств после кодирования.</span><span class="sxs-lookup"><span data-stu-id="753a2-445">The following code example sets the post-encoding property values.</span></span>


```C++
//-------------------------------------------------------------------
//  PostEncodingUpdate
//  Updates the file sink with encoding properties set on the encoder
//  during the encoding session.
    //1. Get the output nodes
    //2. For each node, get the downstream node
    //3. For the downstream node, get the MFT
    //4. Get the property store
    //5. Get the required values
    //6. Set them on the stream sink
//
//  pTopology: A pointer to the full topology retrieved from the media session.
//-------------------------------------------------------------------

HRESULT PostEncodingUpdate(IMFTopology *pTopology)
{
    if (!pTopology)
    {
        return E_INVALIDARG;
    }

    HRESULT hr = S_OK;

    IMFCollection* pOutputColl = NULL;
    IUnknown* pNodeUnk = NULL;
    IMFMediaType* pType = NULL;
    IMFTopologyNode* pNode = NULL;
    IUnknown* pSinkUnk = NULL;
    IMFStreamSink* pStreamSink = NULL;
    IMFTopologyNode* pEncoderNode = NULL;
    IUnknown* pEncoderUnk = NULL;
    IMFTransform* pEncoder = NULL;
    IPropertyStore* pStreamSinkProps = NULL;
    IPropertyStore* pEncoderProps = NULL;

    GUID guidMajorType = GUID_NULL;

    PROPVARIANT var;
    PropVariantInit( &var );

    DWORD cElements = 0;

    hr = pTopology->GetOutputNodeCollection( &pOutputColl);
    if (FAILED(hr))
    {
        goto done;
    }


    hr = pOutputColl->GetElementCount(&cElements);
    if (FAILED(hr))
    {
        goto done;
    }


    for(DWORD index = 0; index < cElements; index++)
    {
        hr = pOutputColl->GetElement(index, &pNodeUnk);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pNodeUnk->QueryInterface(IID_IMFTopologyNode, (void**)&pNode);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pNode->GetInputPrefType(0, &pType);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pType->GetMajorType( &guidMajorType );
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pNode->GetObject(&pSinkUnk);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pSinkUnk->QueryInterface(IID_IMFStreamSink, (void**)&pStreamSink);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pNode->GetInput( 0, &pEncoderNode, NULL );
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pEncoderNode->GetObject(&pEncoderUnk);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pEncoderUnk->QueryInterface(IID_IMFTransform, (void**)&pEncoder);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pStreamSink->QueryInterface(IID_IPropertyStore, (void**)&pStreamSinkProps);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pEncoder->QueryInterface(IID_IPropertyStore, (void**)&pEncoderProps);
        if (FAILED(hr))
        {
            goto done;
        }

        if( guidMajorType == MFMediaType_Video )
        {            
            hr = pEncoderProps->GetValue( MFPKEY_BAVG, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_BAVG, var );
            if (FAILED(hr))
            {
                goto done;
            }

            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_RAVG, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_RAVG, var);
            if (FAILED(hr))
            {
                goto done;
            }

            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_BMAX, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_BMAX, var);
            if (FAILED(hr))
            {
                goto done;
            }

            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_RMAX, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_RMAX, var);
            if (FAILED(hr))
            {
                goto done;
            }
        }
        else if( guidMajorType == MFMediaType_Audio )
        {      
            hr = pEncoderProps->GetValue( MFPKEY_STAT_BAVG, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_BAVG, var );
            if (FAILED(hr))
            {
                goto done;
            }
            
            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_STAT_RAVG, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_RAVG, var );
            if (FAILED(hr))
            {
                goto done;
            }
            
            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_STAT_BMAX, &var);
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_BMAX, var);
            if (FAILED(hr))
            {
                goto done;
            }

            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_STAT_RMAX, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_RMAX, var );         
            if (FAILED(hr))
            {
                goto done;
            }

            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_WMAENC_AVGBYTESPERSEC, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_WMAENC_AVGBYTESPERSEC, var );         
            if (FAILED(hr))
            {
                goto done;
            }
        } 
        PropVariantClear( &var ); 
   }
done:
    SafeRelease (&pOutputColl);
    SafeRelease (&pNodeUnk);
    SafeRelease (&pType);
    SafeRelease (&pNode);
    SafeRelease (&pSinkUnk);
    SafeRelease (&pStreamSink);
    SafeRelease (&pEncoderNode);
    SafeRelease (&pEncoderUnk);
    SafeRelease (&pEncoder);
    SafeRelease (&pStreamSinkProps);
    SafeRelease (&pEncoderProps);

    return hr;
   
}
```



## <a name="implement-main"></a><span data-ttu-id="753a2-446">Реализация Main</span><span class="sxs-lookup"><span data-stu-id="753a2-446">Implement Main</span></span>

<span data-ttu-id="753a2-447">В следующем примере кода показана основная функция консольного приложения.</span><span class="sxs-lookup"><span data-stu-id="753a2-447">The following code example shows the main function of your console application.</span></span>


```C++
int wmain(int argc, wchar_t* argv[])
{
    HeapSetInformation(NULL, HeapEnableTerminationOnCorruption, NULL, 0);

    if (argc != 4)
    {
        wprintf_s(L"Usage: %s inputaudio.mp3, %s output.wm*, %Encoding Type: CBR, VBR\n");
        return 0;
    }


    HRESULT             hr = S_OK;

    IMFMediaSource* pSource = NULL;
    IMFTopology* pTopology = NULL;
    IMFActivate* pFileSinkActivate = NULL;

    hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | COINIT_DISABLE_OLE1DDE);
    if (FAILED(hr))
    {
        goto done;
    }

    //Set the requested encoding mode
    if (wcscmp(argv[3], L"CBR")==0)
    {
        EncodingMode = CBR;
    }
    else if (wcscmp(argv[3], L"VBR")==0)
    {
        EncodingMode = VBR;
    }
    else
    {
        EncodingMode = CBR;
    }

    // Start up Media Foundation platform.
    hr = MFStartup(MF_VERSION);
    if (FAILED(hr))
    {
        goto done;
    }

    //Create the media source
    hr = CreateMediaSource(argv[1], &pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    //Create the file sink activate
    hr = CreateMediaSink(argv[2], pSource, &pFileSinkActivate);
    if (FAILED(hr))
    {
        goto done;
    }

    //Build the encoding topology.
    hr = BuildPartialTopology(pSource, pFileSinkActivate, &pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    //Instantiate the media session and start encoding
    hr = Encode(pTopology);
    if (FAILED(hr))
    {
        goto done;
    }


done:
    // Clean up.
    SafeRelease(&pSource);
    SafeRelease(&pTopology);
    SafeRelease(&pFileSinkActivate);

    MFShutdown();
    CoUninitialize();

    if (FAILED(hr))
    {
        wprintf_s(L"Could not create the output file due to 0x%X\n", hr);
    }
    return 0;
}
```



## <a name="test-the-output-file"></a><span data-ttu-id="753a2-448">Проверка выходного файла</span><span class="sxs-lookup"><span data-stu-id="753a2-448">Test the Output File</span></span>

<span data-ttu-id="753a2-449">В следующем списке приводится список флажков для проверки закодированного файла.</span><span class="sxs-lookup"><span data-stu-id="753a2-449">The following list describes a check list for testing the encoded file.</span></span> <span data-ttu-id="753a2-450">Эти значения можно проверить в диалоговом окне Свойства файла, которое можно отобразить, щелкнув закодированный файл правой кнопкой мыши и выбрав пункт **Свойства** в контекстном меню.</span><span class="sxs-lookup"><span data-stu-id="753a2-450">These values can be checked in the file properties dialog box that you can display by right-clicking the encoded file and selecting **Properties** from the context menu.</span></span>

-   <span data-ttu-id="753a2-451">Путь к закодированному файлу является точным.</span><span class="sxs-lookup"><span data-stu-id="753a2-451">The path of the encoded file is accurate.</span></span>
-   <span data-ttu-id="753a2-452">Размер файла превышает 0 КБ, а длительность воспроизведения совпадает с длительностью исходного файла.</span><span class="sxs-lookup"><span data-stu-id="753a2-452">The size of the file is more than zero KB and the play duration matches the source file's duration.</span></span>
-   <span data-ttu-id="753a2-453">Для видеопотока проверьте ширину и высоту кадра, а также частоту кадров.</span><span class="sxs-lookup"><span data-stu-id="753a2-453">For the video stream, check the frame width and height, frame rate.</span></span> <span data-ttu-id="753a2-454">Эти значения должны соответствовать значениям, указанным в профиле ASF, созданном на шаге "Создание объекта профиля ASF".</span><span class="sxs-lookup"><span data-stu-id="753a2-454">These values should match the values that you specified in the ASF profile that you created in the step described in the section "Create the ASF Profile Object".</span></span>
-   <span data-ttu-id="753a2-455">Для аудиопотока скорость потока должна быть близко к значению, указанному на целевом типе носителя.</span><span class="sxs-lookup"><span data-stu-id="753a2-455">For the audio stream, the bit rate must be close to the value you specified on the target media type.</span></span>
-   <span data-ttu-id="753a2-456">Откройте файл в проигрывателе Windows Media и проверьте качество кодирования.</span><span class="sxs-lookup"><span data-stu-id="753a2-456">Open the file in Windows Media Player and check the quality of the encoding.</span></span>
-   <span data-ttu-id="753a2-457">Откройте файл ASF в Асфвиевер, чтобы увидеть структуру файла ASF.</span><span class="sxs-lookup"><span data-stu-id="753a2-457">Open the ASF file in ASFViewer to see the structure of an ASF file.</span></span> <span data-ttu-id="753a2-458">Это средство можно загрузить с [веб-сайта Майкрософт](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea).</span><span class="sxs-lookup"><span data-stu-id="753a2-458">This tool can be downloaded from this [Microsoft website](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea).</span></span>

## <a name="common-error-codes-and-debugging-tips"></a><span data-ttu-id="753a2-459">Распространенные коды ошибок и советы по отладке</span><span class="sxs-lookup"><span data-stu-id="753a2-459">Common Error Codes and Debugging Tips</span></span>

<span data-ttu-id="753a2-460">В следующем списке описаны распространенные коды ошибок, которые могут быть получены, и советы по отладке.</span><span class="sxs-lookup"><span data-stu-id="753a2-460">The following list describes the common error codes that your might receive and the debugging tips.</span></span>

-   <span data-ttu-id="753a2-461">Вызов [**имфсаурцересолвер:: креатеобжектфромурл**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) приостанавливается к приложению.</span><span class="sxs-lookup"><span data-stu-id="753a2-461">The call to [**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) stalls the application.</span></span>

    <span data-ttu-id="753a2-462">Убедитесь, что вы инициализируи Media Foundationную платформу, вызвав [**мфстартуп**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup).</span><span class="sxs-lookup"><span data-stu-id="753a2-462">Make sure that you have initialized the Media Foundation platform by calling [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup).</span></span> <span data-ttu-id="753a2-463">Эта функция устанавливает асинхронную платформу, используемую всеми методами, которые запускают асинхронные операции, такие как [**имфсаурцересолвер:: креатеобжектфромурл**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl), внутренне.</span><span class="sxs-lookup"><span data-stu-id="753a2-463">This function sets up the asynchronous platform that is used by all methods that start asynchronous operations, such as [**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl), internally.</span></span>

-   <span data-ttu-id="753a2-464">[**Имфсаурцересолвер:: креатеобжектфромурл**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) возвращает значение HRESULT 0x80070002 "системе не удается найти указанный файл.</span><span class="sxs-lookup"><span data-stu-id="753a2-464">[**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) returns HRESULT 0x80070002 "The system cannot find the file specified.</span></span>

    <span data-ttu-id="753a2-465">Убедитесь, что имя входного файла, указанное пользователем в первом аргументе, существует.</span><span class="sxs-lookup"><span data-stu-id="753a2-465">Make sure that the input file name specified by the user in the first argument exists.</span></span>

-   <span data-ttu-id="753a2-466">HRESULT 0x80070020 "процесс не может получить доступ к файлу, так как он используется другим процессом.</span><span class="sxs-lookup"><span data-stu-id="753a2-466">HRESULT 0x80070020 "The process cannot access the file because it is being used by another process.</span></span> <span data-ttu-id="753a2-467">"</span><span class="sxs-lookup"><span data-stu-id="753a2-467">"</span></span>

    <span data-ttu-id="753a2-468">Убедитесь, что входные и выходные файлы в настоящее время не используются другим ресурсом в системе.</span><span class="sxs-lookup"><span data-stu-id="753a2-468">Make sure that the input and the output files are not currently in use by another resource in the system.</span></span>

-   <span data-ttu-id="753a2-469">Вызовы методов [**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) возвращают MF \_ E \_ инвалидмедиатипе.</span><span class="sxs-lookup"><span data-stu-id="753a2-469">Calls to [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) methods return MF\_E\_INVALIDMEDIATYPE.</span></span>

    <span data-ttu-id="753a2-470">Убедитесь, что выполнены следующие условия.</span><span class="sxs-lookup"><span data-stu-id="753a2-470">Make sure that the following conditions are true:</span></span>

    -   <span data-ttu-id="753a2-471">Указанный тип входных данных или тип выхода совместим с типами мультимедиа, поддерживаемыми кодировщиком.</span><span class="sxs-lookup"><span data-stu-id="753a2-471">The input type or the output type that you specified is compatible with media types that the encoder supports.</span></span>
    -   <span data-ttu-id="753a2-472">Указанные типы носителей завершены.</span><span class="sxs-lookup"><span data-stu-id="753a2-472">The media types that you specified are complete.</span></span> <span data-ttu-id="753a2-473">Для выполнения типов мультимедиа ознакомьтесь с необходимыми атрибутами в подразделах "Создание типа сжатого аудио носителя" и "Создание сжатого видеоматериала" этого руководства.</span><span class="sxs-lookup"><span data-stu-id="753a2-473">For media types to be complete, see the required attributes in the "Create a Compressed Audio Media Type" and "Create a Compressed Video Media Type" sections of this tutorial.</span></span>
    -   <span data-ttu-id="753a2-474">Убедитесь, что задана Целевая скорость по отношению к частичному типу носителя, к которому добавляются частные данные кодека.</span><span class="sxs-lookup"><span data-stu-id="753a2-474">Make sure that you have set the target bit rate on the partial media type to which you are adding the codec private data.</span></span>

-   <span data-ttu-id="753a2-475">Сеанс мультимедиа возвращает \_ \_ из состояния события MF E неподдерживаемый \_ \_ тип D3D.</span><span class="sxs-lookup"><span data-stu-id="753a2-475">The Media Session returns MF\_E\_UNSUPPORTED\_D3D\_TYPE in the event status.</span></span>

    <span data-ttu-id="753a2-476">Эта ошибка возвращается, если тип носителя источника указывает смешанный режим чередования, который не поддерживается кодировщиком видео Windows Media.</span><span class="sxs-lookup"><span data-stu-id="753a2-476">This error is returned when the source's media type indicates a mixed interlace mode that is not supported by Windows Media Video encoder.</span></span> <span data-ttu-id="753a2-477">Если для типа сжатого видео выбрано значение использовать прогрессивный режим, то конвейер должен использовать преобразование «de-чередование».</span><span class="sxs-lookup"><span data-stu-id="753a2-477">If your compressed video media type is set to use progressive mode, the pipeline must use a de-interlacing transform.</span></span> <span data-ttu-id="753a2-478">Поскольку конвейеру не удается найти совпадение (обозначено этим кодом ошибки), необходимо вручную вставить дезагруженный обработчик видео (перекодировать видеопроцессор) между узлами декодера и кодировщика.</span><span class="sxs-lookup"><span data-stu-id="753a2-478">Because the pipeline is unable to find a match (indicated by this error code), you must insert a de-interlacer (transcode video processor) between the decoder and encoder nodes manually.</span></span>

-   <span data-ttu-id="753a2-479">Сеанс мультимедиа возвращает E \_ INVALIDARG в состоянии события.</span><span class="sxs-lookup"><span data-stu-id="753a2-479">The Media Session returns E\_INVALIDARG in the event status.</span></span>

    <span data-ttu-id="753a2-480">Эта ошибка возвращается в том случае, если атрибуты типа носителя источника несовместимы с атрибутами выходного типа носителя, заданного в кодировщике Windows Media.</span><span class="sxs-lookup"><span data-stu-id="753a2-480">This error is returned when the source's media type attributes are not compatible with the attributes of the output media type set on the Windows Media encoder.</span></span>

-   <span data-ttu-id="753a2-481">[**Ивмкодекприватедата:: жетприватедата**](../wmformat/iwmcodecprivatedata-getprivatedata.md) возвращает значение HRESULT 0x80040203 "при попытке вычислить строку запроса произошла синтаксическая ошибка"</span><span class="sxs-lookup"><span data-stu-id="753a2-481">[**IWMCodecPrivateData::GetPrivateData**](../wmformat/iwmcodecprivatedata-getprivatedata.md) returns HRESULT 0x80040203 "A syntax error occurred trying to evaluate a query string"</span></span>

    <span data-ttu-id="753a2-482">Убедитесь, что тип входных данных задан в файле MFT кодировщика.</span><span class="sxs-lookup"><span data-stu-id="753a2-482">Make sure that the input type is set on the encoder MFT.</span></span>

## <a name="related-topics"></a><span data-ttu-id="753a2-483">См. также</span><span class="sxs-lookup"><span data-stu-id="753a2-483">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="753a2-484">Компоненты ASF уровня конвейера</span><span class="sxs-lookup"><span data-stu-id="753a2-484">Pipeline Layer ASF Components</span></span>](pipeline-layer-asf-components.md)
</dt> </dl>

 

 

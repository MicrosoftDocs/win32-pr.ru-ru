---
description: В этом учебнике демонстрируется запись нового звукового файла (WMA) путем извлечения мультимедийного содержимого из файла звукозаписи (. wav) и его сжатия в формате ASF.
ms.assetid: f310c6ed-52e7-4828-9d4c-2f7ced9080c5
title: Учебник. запись файла WMA с помощью объектов Вмконтаинер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d156b75ced6cde2953ec90362ed13b0cc53bb83c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898705"
---
# <a name="tutorial-writing-a-wma-file-by-using-wmcontainer-objects"></a><span data-ttu-id="7e3e8-103">Учебник. запись файла WMA с помощью объектов Вмконтаинер</span><span class="sxs-lookup"><span data-stu-id="7e3e8-103">Tutorial: Writing a WMA File by Using WMContainer Objects</span></span>

<span data-ttu-id="7e3e8-104">В этом учебнике демонстрируется запись нового звукового файла (WMA) путем извлечения мультимедийного содержимого из файла звукозаписи (. wav) и его сжатия в формате ASF.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-104">This tutorial demonstrates writing a new audio file (.wma) by extracting media content from an uncompressed audio file (.wav) and then compressing it in ASF format.</span></span> <span data-ttu-id="7e3e8-105">Для преобразования используется режим кодирования с [постоянным битом скорости](constant-bit-rate-encoding.md) (CBR).</span><span class="sxs-lookup"><span data-stu-id="7e3e8-105">The encoding mode used for the conversion is [Constant Bit Rate Encoding](constant-bit-rate-encoding.md) (CBR).</span></span> <span data-ttu-id="7e3e8-106">В этом режиме перед сеансом кодирования приложение указывает целевую скорость, которую должен достичь кодировщик.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-106">In this mode, before the encoding session, the application specifies a target bit rate that the encoder must achieve.</span></span>

<span data-ttu-id="7e3e8-107">В этом руководстве вы создадите консольное приложение, которое принимает входные и выходные имена файлов в качестве аргументов.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-107">In this tutorial, you will create a console application that takes the input and output filenames as arguments.</span></span> <span data-ttu-id="7e3e8-108">Приложение получает примеры несжатого носителя из приложения для анализа волнового файла, которое предоставляется в этом руководстве.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-108">The application gets the uncompressed media samples from a wave file parsing application, which is provided with this tutorial.</span></span> <span data-ttu-id="7e3e8-109">Эти примеры отправляются в кодировщик для преобразования в формат Windows Media Audio 9.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-109">These samples are sent to the encoder for conversion to Windows Media Audio 9 format.</span></span> <span data-ttu-id="7e3e8-110">Кодировщик настраивается для кодирования CBR и использует первую скорость потока, доступную во время согласования типа носителя, в качестве целевой скорости.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-110">The encoder is configured for CBR encoding and uses the first bit rate available during media type negotiation as the target bit rate.</span></span> <span data-ttu-id="7e3e8-111">Закодированные образцы отправляются мультиплексору для пакетирования в формате ASF.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-111">The encoded samples are sent to the multiplexer for packetization in ASF data format.</span></span> <span data-ttu-id="7e3e8-112">Эти пакеты будут записаны в байтовый поток, представляющий объект данных ASF.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-112">These packets will be written to a byte stream that represents the ASF Data Object.</span></span> <span data-ttu-id="7e3e8-113">После того как раздел данных будет готов, вы создадите звуковой файл ASF и запишете новый объект заголовка ASF, который объединяет все данные заголовка, а затем добавляет байтовый поток данных ASF.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-113">After the data section is ready, you will create an ASF audio file and write the new ASF Header Object that consolidates all the header information and then append the ASF Data Object byte stream.</span></span>

<span data-ttu-id="7e3e8-114">Этот учебник содержит следующие подразделы:</span><span class="sxs-lookup"><span data-stu-id="7e3e8-114">This tutorial contains the following sections:</span></span>

-   [<span data-ttu-id="7e3e8-115">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="7e3e8-115">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="7e3e8-116">Терминология</span><span class="sxs-lookup"><span data-stu-id="7e3e8-116">Terminology</span></span>](#terminology)
-   [<span data-ttu-id="7e3e8-117">1. Настройка проекта</span><span class="sxs-lookup"><span data-stu-id="7e3e8-117">1. Set up the Project</span></span>](#1-set-up-the-project)
-   [<span data-ttu-id="7e3e8-118">2. объявление вспомогательных функций</span><span class="sxs-lookup"><span data-stu-id="7e3e8-118">2. Declare Helper Functions</span></span>](#2-declare-helper-functions)
-   [<span data-ttu-id="7e3e8-119">3. Открытие звукового файла</span><span class="sxs-lookup"><span data-stu-id="7e3e8-119">3. Open an Audio File</span></span>](#3-open-an-audio-file)
-   [<span data-ttu-id="7e3e8-120">4. Настройка кодировщика</span><span class="sxs-lookup"><span data-stu-id="7e3e8-120">4. Configure the Encoder</span></span>](#4-configure-the-encoder)
-   [<span data-ttu-id="7e3e8-121">5. Создайте объект ASF Контентинфо.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-121">5. Create the ASF ContentInfo object.</span></span>](#5-create-the-asf-contentinfo-object)
-   [<span data-ttu-id="7e3e8-122">6. Создание мультиплексора ASF</span><span class="sxs-lookup"><span data-stu-id="7e3e8-122">6. Create the ASF Multiplexer</span></span>](#6-create-the-asf-multiplexer)
-   [<span data-ttu-id="7e3e8-123">7. Генерация новых пакетов данных ASF</span><span class="sxs-lookup"><span data-stu-id="7e3e8-123">7. Generate New ASF Data Packets</span></span>](#7-generate-new-asf-data-packets)
-   [<span data-ttu-id="7e3e8-124">8. запись файла ASF</span><span class="sxs-lookup"><span data-stu-id="7e3e8-124">8. Write the ASF File</span></span>](#8-write-the-asf-file)
-   [<span data-ttu-id="7e3e8-125">9. определение функции Entry-Point</span><span class="sxs-lookup"><span data-stu-id="7e3e8-125">9. Define the Entry-Point Function</span></span>](#9-define-the-entry-point-function)
-   [<span data-ttu-id="7e3e8-126">См. также</span><span class="sxs-lookup"><span data-stu-id="7e3e8-126">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="7e3e8-127">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="7e3e8-127">Prerequisites</span></span>

<span data-ttu-id="7e3e8-128">В этом учебнике предполагается следующее:</span><span class="sxs-lookup"><span data-stu-id="7e3e8-128">This tutorial assumes the following:</span></span>

-   <span data-ttu-id="7e3e8-129">Вы знакомы со структурой файла ASF и компонентами, предоставляемыми Media Foundation для работы с объектами ASF.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-129">You are familiar with the structure of an ASF file and the components provided by Media Foundation to work with ASF Objects.</span></span> <span data-ttu-id="7e3e8-130">К таким компонентам относятся Контентинфо, Splitter, мультиплексор и объекты профиля.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-130">These components include ContentInfo, splitter, multiplexer, and profile objects.</span></span> <span data-ttu-id="7e3e8-131">Дополнительные сведения см. в разделе [компоненты ASF вмконтаинер](wmcontainer-asf-components.md).</span><span class="sxs-lookup"><span data-stu-id="7e3e8-131">For more information, see [WMContainer ASF Components](wmcontainer-asf-components.md).</span></span>
-   <span data-ttu-id="7e3e8-132">Вы знакомы с кодировщиками Windows Media и различными типами кодировок, особенно CBR.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-132">You are familiar with Windows Media encoders, and the various encoding types, particularly CBR.</span></span> <span data-ttu-id="7e3e8-133">Дополнительные сведения см. в разделе [кодировщики Windows Media](windows-media-encoders.md) .</span><span class="sxs-lookup"><span data-stu-id="7e3e8-133">For more information, see [Windows Media Encoders](windows-media-encoders.md) .</span></span>
-   <span data-ttu-id="7e3e8-134">Вы знакомы с [буферами мультимедиа](media-buffers.md) и потоками байтов: в частности, операции с файлами с использованием потока байтов и запись содержимого буфера мультимедиа в байтовый поток.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-134">You are familiar with [Media Buffers](media-buffers.md) and byte streams: Specifically, file operations using a byte stream, and writing the contents of a media buffer to a byte stream.</span></span>

## <a name="terminology"></a><span data-ttu-id="7e3e8-135">Терминология</span><span class="sxs-lookup"><span data-stu-id="7e3e8-135">Terminology</span></span>

<span data-ttu-id="7e3e8-136">В этом учебнике используются следующие термины:</span><span class="sxs-lookup"><span data-stu-id="7e3e8-136">This tutorial uses the following terms:</span></span>

-   <span data-ttu-id="7e3e8-137">Тип исходного носителя: объект типа мультимедиа, предоставляет интерфейс [**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) , описывающий содержимое входного файла.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-137">Source media type: Media type object, exposes [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface, which describes the contents of the input file.</span></span>
-   <span data-ttu-id="7e3e8-138">Звуковой профиль: объект Profile, предоставляет интерфейс [**имфасфпрофиле**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) , который содержит только звуковые потоки выходного файла.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-138">Audio profile: Profile object, exposes [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) interface, which contains only audio streams of the output file.</span></span>
-   <span data-ttu-id="7e3e8-139">Пример Stream: пример носителя, предоставляющий интерфейс [**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , представляет данные носителя входного файла, полученные из кодировщика в сжатом состоянии.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-139">Stream sample: Media sample, exposes [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface, represents the input file's media data obtained from the encoder in a compressed state.</span></span>
-   <span data-ttu-id="7e3e8-140">Объект Контентинфо: [ASF контентинфо](asf-contentinfo-object.md), предоставляет интерфейс [**имфасфконтентинфо**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) , который представляет объект заголовка ASF выходного файла.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-140">ContentInfo object: [ASF ContentInfo Object](asf-contentinfo-object.md), exposes [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) interface, which represents the ASF Header Object of the output file.</span></span>
-   <span data-ttu-id="7e3e8-141">Поток байтов данных: объект потока байтов, предоставляет интерфейс [**имфбитестреам**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) , представляющий всю часть объекта данных ASF в выходном файле.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-141">Data byte stream: Byte stream object, exposes [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) interface, which represents the entire ASF Data Object portion of the output file.</span></span>
-   <span data-ttu-id="7e3e8-142">Пример пакета данных: носитель, предоставляющий интерфейс [**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , созданный [мультиплексором ASF](asf-multiplexer.md); представляет пакет данных ASF, который будет записан в поток байтов данных.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-142">Data packet: Media sample, exposes [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface, generated by the [ASF Multiplexer](asf-multiplexer.md); represents an ASF data packet that will be written to the data byte stream.</span></span>
-   <span data-ttu-id="7e3e8-143">Выходной поток байтов: объект потока байтов, предоставляющий интерфейс [**имфбитестреам**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) , который содержит содержимое выходного файла.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-143">Output byte stream: Byte stream object, exposes [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) interface, which contains the contents of the output file.</span></span>

## <a name="1-set-up-the-project"></a><span data-ttu-id="7e3e8-144">1. Настройка проекта</span><span class="sxs-lookup"><span data-stu-id="7e3e8-144">1. Set up the Project</span></span>

1.  <span data-ttu-id="7e3e8-145">Включите в исходный файл следующие заголовки:</span><span class="sxs-lookup"><span data-stu-id="7e3e8-145">Include the following headers in your source file:</span></span>

    ```C++
    #include <new>
    #include <stdio.h>       // Standard I/O
    #include <windows.h>     // Windows headers
    #include <mfapi.h>       // Media Foundation platform
    #include <wmcontainer.h> // ASF interfaces
    #include <mferror.h>     // Media Foundation error codes
    ```

    

2.  <span data-ttu-id="7e3e8-146">Ссылка на следующие файлы библиотеки:</span><span class="sxs-lookup"><span data-stu-id="7e3e8-146">Link to the following library files:</span></span>

    -   <span data-ttu-id="7e3e8-147">мфплат. lib</span><span class="sxs-lookup"><span data-stu-id="7e3e8-147">mfplat.lib</span></span>
    -   <span data-ttu-id="7e3e8-148">MF. lib</span><span class="sxs-lookup"><span data-stu-id="7e3e8-148">mf.lib</span></span>
    -   <span data-ttu-id="7e3e8-149">мфууид. lib</span><span class="sxs-lookup"><span data-stu-id="7e3e8-149">mfuuid.lib</span></span>

3.  <span data-ttu-id="7e3e8-150">Объявите функцию [саферелеасе](saferelease.md) .</span><span class="sxs-lookup"><span data-stu-id="7e3e8-150">Declare the [SafeRelease](saferelease.md) function.</span></span>
4.  <span data-ttu-id="7e3e8-151">Включите класс Квмаенкодер в проект.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-151">Include the CWmaEncoder class in your project.</span></span> <span data-ttu-id="7e3e8-152">Полный исходный код этого класса см. в разделе [пример кода кодировщика](encoder-example-code.md).</span><span class="sxs-lookup"><span data-stu-id="7e3e8-152">For the complete source code of this class, see [Encoder Example Code](encoder-example-code.md).</span></span>

## <a name="2-declare-helper-functions"></a><span data-ttu-id="7e3e8-153">2. объявление вспомогательных функций</span><span class="sxs-lookup"><span data-stu-id="7e3e8-153">2. Declare Helper Functions</span></span>

<span data-ttu-id="7e3e8-154">В этом руководстве используются следующие вспомогательные функции для чтения и записи из байтового потока.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-154">This tutorial uses the following helper functions to read and write from a byte stream.</span></span>

-   <span data-ttu-id="7e3e8-155">`AppendToByteStream`: Добавляет содержимое одного потока байтов в другой поток байтов.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-155">`AppendToByteStream`: Appends the contents of one byte stream to another byte stream.</span></span>
-   <span data-ttu-id="7e3e8-156">Вритебуффертобитестреам: записывает данные из буфера мультимедиа в байтовый поток.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-156">WriteBufferToByteStream: Writes data from a media buffer to a byte stream.</span></span>

<span data-ttu-id="7e3e8-157">Дополнительные сведения см. в разделе [**имфбитестреам:: Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write).</span><span class="sxs-lookup"><span data-stu-id="7e3e8-157">For more information, see [**IMFByteStream::Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write).</span></span> <span data-ttu-id="7e3e8-158">В следующем коде показаны эти вспомогательные функции:</span><span class="sxs-lookup"><span data-stu-id="7e3e8-158">The following code shows these helper functions:</span></span>


```C++
//-------------------------------------------------------------------
// AppendToByteStream
//
// Reads the contents of pSrc and writes them to pDest.
//-------------------------------------------------------------------

HRESULT AppendToByteStream(IMFByteStream *pSrc, IMFByteStream *pDest)
{
    HRESULT hr = S_OK;

    const DWORD READ_SIZE = 1024;

    BYTE buffer[READ_SIZE];

    while (1)
    {
        ULONG cbRead;

        hr = pSrc->Read(buffer, READ_SIZE, &cbRead);

        if (FAILED(hr)) { break; }

        if (cbRead == 0)
        {
            break;
        }

        hr = pDest->Write(buffer, cbRead, &cbRead);

        if (FAILED(hr)) { break; }
    }

    return hr;
}
```




```C++
//-------------------------------------------------------------------
// WriteBufferToByteStream
//
// Writes data from a media buffer to a byte stream.
//-------------------------------------------------------------------

HRESULT WriteBufferToByteStream(
    IMFByteStream *pStream,   // Pointer to the byte stream.
    IMFMediaBuffer *pBuffer,  // Pointer to the media buffer.
    DWORD *pcbWritten         // Receives the number of bytes written.
    )
{
    HRESULT hr = S_OK;
    DWORD cbData = 0;
    DWORD cbWritten = 0;
    BYTE *pMem = NULL;

    hr = pBuffer->Lock(&pMem, NULL, &cbData);

    if (SUCCEEDED(hr))
    {
        hr = pStream->Write(pMem, cbData, &cbWritten);
    }

    if (SUCCEEDED(hr))
    {
        if (pcbWritten)
        {
            *pcbWritten = cbWritten;
        }
    }

    if (pMem)
    {
        pBuffer->Unlock();
    }
    return hr;
}
```



## <a name="3-open-an-audio-file"></a><span data-ttu-id="7e3e8-159">3. Открытие звукового файла</span><span class="sxs-lookup"><span data-stu-id="7e3e8-159">3. Open an Audio File</span></span>

<span data-ttu-id="7e3e8-160">В этом учебнике предполагается, что приложение создаст несжатый звук для кодирования.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-160">This tutorial assumes that your application will generate uncompressed audio for encoding.</span></span> <span data-ttu-id="7e3e8-161">Для этой цели в этом учебнике объявляются две функции:</span><span class="sxs-lookup"><span data-stu-id="7e3e8-161">For that purpose, two functions are declared in this tutorial:</span></span>


```C++
HRESULT OpenAudioFile(PCWSTR pszURL, IMFMediaType **ppAudioFormat);
HRESULT GetNextAudioSample(BOOL *pbEOS, IMFSample **ppSample);
```



<span data-ttu-id="7e3e8-162">Реализация этих функций остается в модуле чтения.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-162">The implementation of these functions is left to the reader.</span></span>

-   <span data-ttu-id="7e3e8-163">`OpenAudioFile`Функция должна открыть файл мультимедиа, заданный параметром *псзурл* , и вернуть указатель на тип носителя, описывающий аудиопоток.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-163">The `OpenAudioFile` function should open the media file specified by *pszURL* and return a pointer to a media type that describes an audio stream.</span></span>
-   <span data-ttu-id="7e3e8-164">`GetNextAudioSample`Функция должна считывать несжатый звуковой файл PCM из файла, открытого с помощью `OpenAudioFile` .</span><span class="sxs-lookup"><span data-stu-id="7e3e8-164">The `GetNextAudioSample` function should read uncompressed PCM audio from the file that was opened by `OpenAudioFile`.</span></span> <span data-ttu-id="7e3e8-165">По достижении конца файла *пбеос* получает значение **true**.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-165">When the end of the file is reached, *pbEOS* receives the value **TRUE**.</span></span> <span data-ttu-id="7e3e8-166">В противном случае *ппсампле* получает пример мультимедиа, содержащий буфер аудио.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-166">Otherwise, *ppSample* receives a media sample that contains the audio buffer.</span></span>

## <a name="4-configure-the-encoder"></a><span data-ttu-id="7e3e8-167">4. Настройка кодировщика</span><span class="sxs-lookup"><span data-stu-id="7e3e8-167">4. Configure the Encoder</span></span>

<span data-ttu-id="7e3e8-168">Затем создайте кодировщик, настройте его для создания примеров потока в кодировке CBR и согласования входных и выходных типов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-168">Next, create the encoder, configure it to produce CBR-encoded stream samples, and negotiate the input and the output media types.</span></span>

<span data-ttu-id="7e3e8-169">В Media Foundation кодировщики (предоставляют интерфейс [**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) ) реализуются как [преобразования Media Foundation](media-foundation-transforms.md) (MFT).</span><span class="sxs-lookup"><span data-stu-id="7e3e8-169">In Media Foundation, encoders (expose the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface) are implemented as [Media Foundation Transforms](media-foundation-transforms.md) (MFT).</span></span>

<span data-ttu-id="7e3e8-170">В этом руководстве кодировщик реализуется в `CWmaEncoder` классе, который предоставляет оболочку для MFT.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-170">In this tutorial, the encoder is implemented in the `CWmaEncoder` class that provides a wrapper for the MFT.</span></span> <span data-ttu-id="7e3e8-171">Полный исходный код этого класса см. в разделе [пример кода кодировщика](encoder-example-code.md).</span><span class="sxs-lookup"><span data-stu-id="7e3e8-171">For the complete source code of this class, see [Encoder Example Code](encoder-example-code.md).</span></span>

> [!Note]  
> <span data-ttu-id="7e3e8-172">При необходимости можно указать тип кодировки CBR.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-172">You can optionally specify the encoding type as CBR.</span></span> <span data-ttu-id="7e3e8-173">По умолчанию кодировщик настроен на использование кодировки CBR.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-173">By default, the encoder is configured to use CBR encoding.</span></span> <span data-ttu-id="7e3e8-174">Дополнительные сведения см. в статье [кодирование постоянной скорости потока](constant-bit-rate-encoding.md).</span><span class="sxs-lookup"><span data-stu-id="7e3e8-174">For more information, see [Constant Bit Rate Encoding](constant-bit-rate-encoding.md).</span></span> <span data-ttu-id="7e3e8-175">Вы можете задать дополнительные свойства в зависимости от типа кодировки. Дополнительные сведения о свойствах, характерных для режима кодирования, см. в разделе [кодирование переменной с переменным качеством](quality-based-variable-bit-rate--vbr--encoding.md), [кодирование неограниченной переменной скорости](unconstrained-variable-bit-rate--vbr--encoding.md)и [кодирование переменной с ограничением пиковой](peak-constrained-variable-bit-rate--vbr--encoding.md)скорости.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-175">You can set additional properties depending on the type of encoding, for information about the properties that are specific to an encoding mode, see [Quality-Based Variable Bit Rate Encoding](quality-based-variable-bit-rate--vbr--encoding.md), [Unconstrained Variable Bit Rate Encoding](unconstrained-variable-bit-rate--vbr--encoding.md), and [Peak-Constrained Variable Bit Rate Encoding](peak-constrained-variable-bit-rate--vbr--encoding.md).</span></span>

 


```C++
    CWmaEncoder* pEncoder = NULL; //Pointer to the Encoder object.

    hr = OpenAudioFile(sInputFileName, &pInputType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Initialize the WMA encoder wrapper.

    pEncoder = new (std::nothrow) CWmaEncoder();
    if (pEncoder == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    hr = pEncoder->Initialize();
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pEncoder->SetEncodingType(EncodeMode_CBR);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pEncoder->SetInputType(pInputType);
    if (FAILED(hr))
    {
        goto done;
    }
```



## <a name="5-create-the-asf-contentinfo-object"></a><span data-ttu-id="7e3e8-176">5. Создайте объект ASF Контентинфо.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-176">5. Create the ASF ContentInfo object.</span></span>

<span data-ttu-id="7e3e8-177">[Объект ASF контентинфо](asf-contentinfo-object.md) содержит сведения о различных объектах заголовка выходного файла.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-177">The [ASF ContentInfo Object](asf-contentinfo-object.md) contains information about the various header objects of the output file.</span></span>

<span data-ttu-id="7e3e8-178">Сначала создайте профиль ASF для аудиопотока:</span><span class="sxs-lookup"><span data-stu-id="7e3e8-178">First, create an ASF profile for the audio stream:</span></span>

1.  <span data-ttu-id="7e3e8-179">Вызовите [**мфкреатеасфпрофиле**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) , чтобы создать пустой объект профиля ASF.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-179">Call [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) to create an empty ASF profile object.</span></span> <span data-ttu-id="7e3e8-180">Профиль ASF предоставляет интерфейс [**имфасфпрофиле**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) .</span><span class="sxs-lookup"><span data-stu-id="7e3e8-180">The ASF profile exposes the [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) interface.</span></span> <span data-ttu-id="7e3e8-181">Дополнительные сведения см. в разделе [Создание и настройка потоков ASF](creating-and-configuring-asf-streams.md).</span><span class="sxs-lookup"><span data-stu-id="7e3e8-181">For more information, see [Creating and Configuring ASF Streams](creating-and-configuring-asf-streams.md).</span></span>
2.  <span data-ttu-id="7e3e8-182">Получите закодированный аудио формат из `CWmaEncoder` объекта.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-182">Get the encoded audio format from the `CWmaEncoder` object.</span></span>
3.  <span data-ttu-id="7e3e8-183">Вызовите метод [**имфасфпрофиле:: креатестреам**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream) , чтобы создать новый поток для профиля ASF.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-183">Call [**IMFASFProfile::CreateStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream) to create a new stream for the ASF profile.</span></span> <span data-ttu-id="7e3e8-184">Передайте указатель на интерфейс [**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) , который представляет формат потока.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-184">Pass in a pointer to the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface, which represents the stream format.</span></span>
4.  <span data-ttu-id="7e3e8-185">Вызовите метод [**имфасфстреамконфиг:: сетстреамнумбер**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-setstreamnumber) , чтобы назначить идентификатор потока.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-185">Call [**IMFASFStreamConfig::SetStreamNumber**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-setstreamnumber) to assign a stream identifier.</span></span>
5.  <span data-ttu-id="7e3e8-186">Задайте параметры "сегмент утечки", установив атрибут [**MF \_ асфстреамконфиг \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) в объекте потока.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-186">Set the "leaky bucket" parameters by setting the [**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) attribute on the stream object.</span></span>
6.  <span data-ttu-id="7e3e8-187">Вызовите [**имфасфпрофиле:: сетстреам**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream) , чтобы добавить новый поток в профиль.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-187">Call [**IMFASFProfile::SetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream) to add the new stream to the profile.</span></span>

<span data-ttu-id="7e3e8-188">Теперь создайте объект ASF Контентинфо следующим образом:</span><span class="sxs-lookup"><span data-stu-id="7e3e8-188">Now create the ASF ContentInfo object as follows:</span></span>

1.  <span data-ttu-id="7e3e8-189">Вызовите [**мфкреатеасфконтентинфо**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) , чтобы создать пустой объект контентинфо.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-189">Call [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) to create an empty ContentInfo object.</span></span>
2.  <span data-ttu-id="7e3e8-190">Вызовите [**имфасфконтентинфо:: сетпрофиле**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) , чтобы задать профиль ASF.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-190">Call [**IMFASFContentInfo::SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) to set the ASF profile.</span></span>

<span data-ttu-id="7e3e8-191">В следующем коде показаны следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-191">The following code shows these steps:</span></span>


```C++
HRESULT CreateASFContentInfo(
    CWmaEncoder* pEncoder,
    IMFASFContentInfo** ppContentInfo
    )
{
    HRESULT hr = S_OK;
    
    IMFASFProfile* pProfile = NULL;
    IMFMediaType* pMediaType = NULL;
    IMFASFStreamConfig* pStream = NULL;
    IMFASFContentInfo* pContentInfo = NULL;

    // Create the ASF profile object.

    hr = MFCreateASFProfile(&pProfile); 
    if (FAILED(hr))
    {
        goto done;
    }

    // Create a stream description for the encoded audio.

    hr = pEncoder->GetOutputType(&pMediaType); 
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pProfile->CreateStream(pMediaType, &pStream); 
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pStream->SetStreamNumber(DEFAULT_STREAM_NUMBER); 
    if (FAILED(hr))
    {
        goto done;
    }

    // Set "leaky bucket" values.

    LeakyBucket bucket;

    hr = pEncoder->GetLeakyBucket1(&bucket);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pStream->SetBlob(
        MF_ASFSTREAMCONFIG_LEAKYBUCKET1, 
        (UINT8*)&bucket, 
        sizeof(bucket)
        );

    if (FAILED(hr))
    {
        goto done;
    }

    //Add the stream to the profile

    hr = pProfile->SetStream(pStream);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the ASF ContentInfo object.

    hr = MFCreateASFContentInfo(&pContentInfo); 
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pContentInfo->SetProfile(pProfile); 
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the pointer to the caller.

    *ppContentInfo = pContentInfo;
    (*ppContentInfo)->AddRef();

done:
    SafeRelease(&pProfile);
    SafeRelease(&pStream);
    SafeRelease(&pMediaType);
    SafeRelease(&pContentInfo);
    return hr;
}
```



## <a name="6-create-the-asf-multiplexer"></a><span data-ttu-id="7e3e8-192">6. Создание мультиплексора ASF</span><span class="sxs-lookup"><span data-stu-id="7e3e8-192">6. Create the ASF Multiplexer</span></span>

<span data-ttu-id="7e3e8-193">[Мультиплексор ASF](asf-multiplexer.md) создает пакеты данных ASF.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-193">The [ASF Multiplexer](asf-multiplexer.md) generates ASF data packets.</span></span>

1.  <span data-ttu-id="7e3e8-194">Вызовите [**мфкреатеасфмултиплексер**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmultiplexer) , чтобы создать мультиплексор ASF.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-194">Call [**MFCreateASFMultiplexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmultiplexer) to create the ASF multiplexer.</span></span>
2.  <span data-ttu-id="7e3e8-195">Вызовите метод [**имфасфмултиплексер:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) для инициализации мультиплексора.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-195">Call [**IMFASFMultiplexer::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) to initialize the multiplexer.</span></span> <span data-ttu-id="7e3e8-196">Передайте указатель на объект сведений о содержимом ASF, который был создан в предыдущем разделе.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-196">Pass in a pointer to the ASF Content Info object, which was created in the previous section.</span></span>
3.  <span data-ttu-id="7e3e8-197">Вызовите [**имфасфмултиплексер:: сетфлагс**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags) , чтобы задать флаг **\_ \_ авторегулировки скорости \_ для мфасф мультиплексора** .</span><span class="sxs-lookup"><span data-stu-id="7e3e8-197">Call [**IMFASFMultiplexer::SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags) to set the **MFASF\_MULTIPLEXER\_AUTOADJUST\_BITRATE** flag.</span></span> <span data-ttu-id="7e3e8-198">При использовании этого параметра мультиплексор автоматически корректирует скорость передачи содержимого ASF в соответствии с характеристиками мультиплексированных потоков.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-198">When this setting is used, the multiplexer automatically adjusts the bit rate of the ASF content to match the characteristics of the streams being multiplexed.</span></span>


```C++
HRESULT CreateASFMux( 
    IMFASFContentInfo* pContentInfo,
    IMFASFMultiplexer** ppMultiplexer
    )
{
    HRESULT hr = S_OK;
    
    IMFMediaType* pMediaType = NULL;
    IMFASFMultiplexer *pMultiplexer = NULL;

    // Create and initialize the ASF Multiplexer object.

    hr = MFCreateASFMultiplexer(&pMultiplexer);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pMultiplexer->Initialize(pContentInfo);
    if (FAILED(hr))
    {
        goto done;
    }

    // Enable automatic bit-rate adjustment.

    hr = pMultiplexer->SetFlags(MFASF_MULTIPLEXER_AUTOADJUST_BITRATE);
    if (FAILED(hr))
    {
        goto done;
    }

    *ppMultiplexer = pMultiplexer;
    (*ppMultiplexer)->AddRef();

done:
    SafeRelease(&pMultiplexer);
    return hr;
}
```



## <a name="7-generate-new-asf-data-packets"></a><span data-ttu-id="7e3e8-199">7. Генерация новых пакетов данных ASF</span><span class="sxs-lookup"><span data-stu-id="7e3e8-199">7. Generate New ASF Data Packets</span></span>

<span data-ttu-id="7e3e8-200">Затем создайте пакеты данных ASF для нового файла.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-200">Next, generate ASF data packets for the new file.</span></span> <span data-ttu-id="7e3e8-201">Эти пакеты данных будут составлять окончательный объект данных ASF для нового файла.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-201">These data packets will constitute the final ASF Data Object for the new file.</span></span> <span data-ttu-id="7e3e8-202">Чтобы создать новые пакеты данных ASF, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-202">To generate new ASF data packets:</span></span>

1.  <span data-ttu-id="7e3e8-203">Вызовите [**мфкреатетемпфиле**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatetempfile) , чтобы создать временный байтовый поток для хранения пакетов данных ASF.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-203">Call [**MFCreateTempFile**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatetempfile) to create a temporary byte stream to hold the ASF data packets.</span></span>
2.  <span data-ttu-id="7e3e8-204">Вызовите функцию, определяемую приложением, `GetNextAudioSample` чтобы получить несжатые звуковые данные для кодировщика.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-204">Call the application-defined `GetNextAudioSample` function to get uncompressed audio data for the encoder.</span></span>
3.  <span data-ttu-id="7e3e8-205">Передача несжатого звука в кодировщик для сжатия.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-205">Pass the uncompressed audio to the encoder for compression.</span></span> <span data-ttu-id="7e3e8-206">Дополнительные сведения см. [в разделе Обработка данных в кодировщике](processing-data-in-the-encoder.md) .</span><span class="sxs-lookup"><span data-stu-id="7e3e8-206">For more information, see [Processing Data in the Encoder](processing-data-in-the-encoder.md)</span></span>
4.  <span data-ttu-id="7e3e8-207">Вызовите [**имфасфмултиплексер::P роцесссампле**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) , чтобы отправить сжатые аудио примеры в мультиплексор ASF для пакетирования.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-207">Call [**IMFASFMultiplexer::ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) to send the compressed audio samples to the ASF multiplexer for packetization.</span></span>
5.  <span data-ttu-id="7e3e8-208">Получите пакеты ASF из мультиплексора и запишите их во временный байтовый поток.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-208">Get the ASF packets from the multiplexer and write them to the temporary byte stream.</span></span> <span data-ttu-id="7e3e8-209">Дополнительные сведения см. в разделе [Создание новых пакетов данных ASF](generating-new-asf-data-packets.md).</span><span class="sxs-lookup"><span data-stu-id="7e3e8-209">For more information, see [Generating New ASF Data Packets](generating-new-asf-data-packets.md).</span></span>
6.  <span data-ttu-id="7e3e8-210">При достижении конца исходного потока остановите кодировщик и извлекайте оставшиеся сжатые образцы из кодировщика.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-210">When you reach the end of the source stream, drain the encoder and pull the remaining compressed samples from the encoder.</span></span> <span data-ttu-id="7e3e8-211">Дополнительные сведения о стоке MFT см. в разделе [Базовая модель обработки MFT](basic-mft-processing-model.md).</span><span class="sxs-lookup"><span data-stu-id="7e3e8-211">For more information about draining an MFT, see [Basic MFT Processing Model](basic-mft-processing-model.md).</span></span>
7.  <span data-ttu-id="7e3e8-212">После отправки всех образцов в мультиплексор вызовите [**имфасфмултиплексер:: Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-flush) и извлекают оставшиеся пакеты ASF из мультиплексора.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-212">After all samples are sent to the multiplexer, call [**IMFASFMultiplexer::Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-flush) and pull the remaining ASF packets from the multiplexer.</span></span>
8.  <span data-ttu-id="7e3e8-213">Вызовите [**имфасфмултиплексер:: end**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end).</span><span class="sxs-lookup"><span data-stu-id="7e3e8-213">Call [**IMFASFMultiplexer::End**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end).</span></span>

<span data-ttu-id="7e3e8-214">Следующий код создает пакеты данных ASF.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-214">The following code generates ASF data packets.</span></span> <span data-ttu-id="7e3e8-215">Функция возвращает указатель на байтовый поток, содержащий объект данных ASF.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-215">The function returns a pointer to a byte stream that contains the ASF Data Object.</span></span>


```C++
HRESULT EncodeData(
    CWmaEncoder* pEncoder, 
    IMFASFContentInfo* pContentInfo,
    IMFASFMultiplexer* pMux, 
    IMFByteStream** ppDataStream) 
{
    HRESULT hr = S_OK;

    IMFByteStream* pStream = NULL;
    IMFSample* pInputSample = NULL;
    IMFSample* pWmaSample = NULL;

    BOOL bEOF = FALSE;

   // Create a temporary file to hold the data stream.
   hr = MFCreateTempFile(
        MF_ACCESSMODE_READWRITE, 
        MF_OPENMODE_DELETE_IF_EXIST,
        MF_FILEFLAGS_NONE,
        &pStream
        );

   if (FAILED(hr))
   {
       goto done;
   }

    BOOL bNeedInput = TRUE;

    while (TRUE)
    {
        if (bNeedInput)
        {
            hr = GetNextAudioSample(&bEOF, &pInputSample);
            if (FAILED(hr))
            {
                goto done;
            }

            if (bEOF)
            {
                // Reached the end of the input file.
                break;
            }

            // Encode the uncompressed audio sample.
            hr = pEncoder->ProcessInput(pInputSample);
            if (FAILED(hr))
            {
                goto done;
            }

            bNeedInput = FALSE;
        }

        if (bNeedInput == FALSE)
        {
            // Get data from the encoder.

            hr = pEncoder->ProcessOutput(&pWmaSample);
            if (FAILED(hr))
            {
                goto done;
            }

            // pWmaSample can be NULL if the encoder needs more input.

            if (pWmaSample)
            {
                hr = pMux->ProcessSample(DEFAULT_STREAM_NUMBER, pWmaSample, 0);
                if (FAILED(hr))
                {
                    goto done;
                }

                //Collect the data packets and write them to a stream
                hr = GenerateASFDataPackets(pMux, pStream);
                if (FAILED(hr))
                {
                    goto done;
                }
            }
            else
            {
                bNeedInput = TRUE;
            }
        }
        
        SafeRelease(&pInputSample);
        SafeRelease(&pWmaSample);
    }

    // Drain the MFT and pull any remaining samples from the encoder.

    hr = pEncoder->Drain();
    if (FAILED(hr))
    {
        goto done;
    }

    while (TRUE)
    {
        hr = pEncoder->ProcessOutput(&pWmaSample);
        if (FAILED(hr))
        {
            goto done;
        }

        if (pWmaSample == NULL)
        {
            break;
        }

        hr = pMux->ProcessSample(DEFAULT_STREAM_NUMBER, pWmaSample, 0);
        if (FAILED(hr))
        {
            goto done;
        }

        //Collect the data packets and write them to a stream
        hr = GenerateASFDataPackets(pMux, pStream);
        if (FAILED(hr))
        {
            goto done;
        }

        SafeRelease(&pWmaSample);
    }

    // Flush the mux and get any pending ASF data packets.
    hr = pMux->Flush();
    if (FAILED(hr))
    {
        goto done;
    }

    hr = GenerateASFDataPackets(pMux, pStream);
    if (FAILED(hr))
    {
        goto done;
    }
    
    // Update the ContentInfo object
    hr = pMux->End(pContentInfo);
    if (FAILED(hr))
    {
        goto done;
    }

    //Return stream to the caller that contains the ASF encoded data.
    *ppDataStream = pStream;
    (*ppDataStream)->AddRef();

done:
    SafeRelease(&pStream);
    SafeRelease(&pInputSample);
    SafeRelease(&pWmaSample);
    return hr;
}
```



<span data-ttu-id="7e3e8-216">Код для `GenerateASFDataPackets` функции показан в разделе [Создание новых пакетов данных ASF](generating-new-asf-data-packets.md).</span><span class="sxs-lookup"><span data-stu-id="7e3e8-216">Code for the `GenerateASFDataPackets` function is shown in the topic [Generating New ASF Data Packets](generating-new-asf-data-packets.md).</span></span>

## <a name="8-write-the-asf-file"></a><span data-ttu-id="7e3e8-217">8. запись файла ASF</span><span class="sxs-lookup"><span data-stu-id="7e3e8-217">8. Write the ASF File</span></span>

<span data-ttu-id="7e3e8-218">Затем запишите заголовок ASF в буфер мультимедиа, вызвав [**имфасфконтентинфо:: женератехеадер**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader).</span><span class="sxs-lookup"><span data-stu-id="7e3e8-218">Next, write the ASF header to a media buffer by calling [**IMFASFContentInfo::GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader).</span></span> <span data-ttu-id="7e3e8-219">Этот метод преобразует данные, хранящиеся в объекте Контентинфо, в двоичные данные в формате файла заголовка ASF.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-219">This method converts data stored in the ContentInfo object into binary data in ASF Header Object format.</span></span> <span data-ttu-id="7e3e8-220">Дополнительные сведения см. [в разделе Создание нового объекта заголовка ASF](generating-a-new-asf-header-object.md).</span><span class="sxs-lookup"><span data-stu-id="7e3e8-220">For more information, see [Generating a New ASF Header Object](generating-a-new-asf-header-object.md).</span></span>

<span data-ttu-id="7e3e8-221">После создания нового объекта заголовка ASF создайте поток байтов для выходного файла.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-221">After the new ASF Header Object has been generated, create a byte stream for the output file.</span></span> <span data-ttu-id="7e3e8-222">Сначала запишите объект заголовка в выходной поток байтов.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-222">First write the Header Object to the output byte stream.</span></span> <span data-ttu-id="7e3e8-223">Используйте объект заголовка с объектом данных, содержащимся в потоке байтов данных.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-223">Follow the Header Object with the Data Object contained in the data byte stream.</span></span>


```C++
HRESULT WriteASFFile( 
     IMFASFContentInfo *pContentInfo, 
     IMFByteStream *pDataStream,
     PCWSTR pszFile
     )
{
    HRESULT hr = S_OK;
    
    IMFMediaBuffer* pHeaderBuffer = NULL;
    IMFByteStream* pWmaStream = NULL;

    DWORD cbHeaderSize = 0;
    DWORD cbWritten = 0;

    //Create output file
    hr = MFCreateFile(MF_ACCESSMODE_WRITE, MF_OPENMODE_DELETE_IF_EXIST,
        MF_FILEFLAGS_NONE, pszFile, &pWmaStream);

    if (FAILED(hr))
    {
        goto done;
    }


    // Get the size of the ASF Header Object.
    hr = pContentInfo->GenerateHeader (NULL, &cbHeaderSize);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create a media buffer.
    hr = MFCreateMemoryBuffer(cbHeaderSize, &pHeaderBuffer);
    if (FAILED(hr))
    {
        goto done;
    }

    // Populate the media buffer with the ASF Header Object.
    hr = pContentInfo->GenerateHeader(pHeaderBuffer, &cbHeaderSize);
    if (FAILED(hr))
    {
        goto done;
    }

    // Write the ASF header to the output file.
    hr = WriteBufferToByteStream(pWmaStream, pHeaderBuffer, &cbWritten);
    if (FAILED(hr))
    {
        goto done;
    }

    // Append the data stream to the file.

    hr = pDataStream->SetCurrentPosition(0);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = AppendToByteStream(pDataStream, pWmaStream);

done:
    SafeRelease(&pHeaderBuffer);
    SafeRelease(&pWmaStream);
    return hr;
}
```



## <a name="9-define-the-entry-point-function"></a><span data-ttu-id="7e3e8-224">9. определение функции Entry-Point</span><span class="sxs-lookup"><span data-stu-id="7e3e8-224">9. Define the Entry-Point Function</span></span>

<span data-ttu-id="7e3e8-225">Теперь можно объединить предыдущие шаги в законченное приложение.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-225">Now you can put the previous steps together into a complete application.</span></span> <span data-ttu-id="7e3e8-226">Перед использованием любого объекта Media Foundation инициализируйте Media Foundationную платформу, вызвав [**мфстартуп**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup).</span><span class="sxs-lookup"><span data-stu-id="7e3e8-226">Before using any of the Media Foundation objects, initialize the Media Foundation platform by calling [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup).</span></span> <span data-ttu-id="7e3e8-227">По завершении вызовите [**мфшутдовн**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).</span><span class="sxs-lookup"><span data-stu-id="7e3e8-227">When you are done, call [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).</span></span> <span data-ttu-id="7e3e8-228">Дополнительные сведения см. в разделе [инициализация Media Foundation](initializing-media-foundation.md).</span><span class="sxs-lookup"><span data-stu-id="7e3e8-228">For more information, see [Initializing Media Foundation](initializing-media-foundation.md).</span></span>

<span data-ttu-id="7e3e8-229">В следующем коде показано полное консольное приложение.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-229">The following code shows the complete console application.</span></span> <span data-ttu-id="7e3e8-230">Аргумент командной строки задает имя файла для преобразования и имя нового звукового файла.</span><span class="sxs-lookup"><span data-stu-id="7e3e8-230">The command-line argument specifies the name of the file to convert and the name of the new audio file.</span></span>


```C++
int wmain(int argc, WCHAR* argv[])
{
    HeapSetInformation(NULL, HeapEnableTerminationOnCorruption, NULL, 0);

    if (argc != 3)
    {
        wprintf_s(L"Usage: %s input.wmv, %s output.wma");
        return 0;
    }

    const WCHAR* sInputFileName = argv[1];    // Source file name
    const WCHAR* sOutputFileName = argv[2];  // Output file name
    
    IMFMediaType* pInputType = NULL;
    IMFASFContentInfo* pContentInfo = NULL;
    IMFASFMultiplexer* pMux = NULL;
    IMFByteStream* pDataStream = NULL;

    CWmaEncoder* pEncoder = NULL; //Pointer to the Encoder object.

    HRESULT hr = CoInitializeEx(
        NULL, COINIT_APARTMENTTHREADED | COINIT_DISABLE_OLE1DDE);

    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFStartup(MF_VERSION);
    if (FAILED(hr))
    {
        goto done;
    }

    CWmaEncoder* pEncoder = NULL; //Pointer to the Encoder object.

    hr = OpenAudioFile(sInputFileName, &pInputType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Initialize the WMA encoder wrapper.

    pEncoder = new (std::nothrow) CWmaEncoder();
    if (pEncoder == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    hr = pEncoder->Initialize();
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pEncoder->SetEncodingType(EncodeMode_CBR);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pEncoder->SetInputType(pInputType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the WMContainer objects.
    hr = CreateASFContentInfo(pEncoder, &pContentInfo);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = CreateASFMux(pContentInfo, &pMux);
    if (FAILED(hr))
    {
        goto done;
    }

    // Convert uncompressed data to ASF format.
    hr = EncodeData(pEncoder, pContentInfo, pMux, &pDataStream);
    if (FAILED(hr))
    {
        goto done;
    }

    // Write the ASF objects to the output file.
    hr = WriteASFFile(pContentInfo, pDataStream, sOutputFileName);

done:
    SafeRelease(&pInputType);
    SafeRelease(&pContentInfo);
    SafeRelease(&pMux);
    SafeRelease(&pDataStream);
    delete pEncoder;

    MFShutdown();
    CoUninitialize();

    if (FAILED(hr))
    {
        wprintf_s(L"Error: 0x%X\n", hr);
    }

    return 0;
} 
```



## <a name="related-topics"></a><span data-ttu-id="7e3e8-231">См. также</span><span class="sxs-lookup"><span data-stu-id="7e3e8-231">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e3e8-232">Компоненты ASF Вмконтаинер</span><span class="sxs-lookup"><span data-stu-id="7e3e8-232">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)
</dt> <dt>

[<span data-ttu-id="7e3e8-233">Поддержка ASF в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7e3e8-233">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 




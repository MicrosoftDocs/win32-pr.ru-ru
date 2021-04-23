---
description: В этом учебнике показано, как использовать средство чтения исходного кода для декодирования звука из файла мультимедиа и записи звука в ВОЛНовый файл.
ms.assetid: ed40e201-c6ed-444f-bdaa-a5f33d1cc068
title: Учебник. декодирование аудио
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 539eb6d9f48419b62fa1c379c636abaf2bb0a63a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104556246"
---
# <a name="tutorial-decoding-audio"></a><span data-ttu-id="2bd52-103">Учебник. декодирование аудио</span><span class="sxs-lookup"><span data-stu-id="2bd52-103">Tutorial: Decoding Audio</span></span>

<span data-ttu-id="2bd52-104">В этом учебнике показано, как использовать [средство чтения исходного кода](source-reader.md) для декодирования звука из файла мультимедиа и записи звука в волновый файл.</span><span class="sxs-lookup"><span data-stu-id="2bd52-104">This tutorial shows how to use the [Source Reader](source-reader.md) to decode audio from a media file and write the audio to a WAVE file.</span></span> <span data-ttu-id="2bd52-105">Учебник основан на образце [аудиоклипа](audio-clip-sample.md) .</span><span class="sxs-lookup"><span data-stu-id="2bd52-105">The tutorial is based on the [Audio Clip](audio-clip-sample.md) sample.</span></span>

-   [<span data-ttu-id="2bd52-106">Обзор</span><span class="sxs-lookup"><span data-stu-id="2bd52-106">Overview</span></span>](#overview)
-   [<span data-ttu-id="2bd52-107">Файлы заголовков и библиотек</span><span class="sxs-lookup"><span data-stu-id="2bd52-107">Header and Library Files</span></span>](#header-and-library-files)
-   [<span data-ttu-id="2bd52-108">Реализация wmain</span><span class="sxs-lookup"><span data-stu-id="2bd52-108">Implement wmain</span></span>](#implement-wmain)
-   [<span data-ttu-id="2bd52-109">Запись файла WAVE</span><span class="sxs-lookup"><span data-stu-id="2bd52-109">Write the WAVE File</span></span>](#write-the-wave-file)
-   [<span data-ttu-id="2bd52-110">Настройка модуля чтения исходного кода</span><span class="sxs-lookup"><span data-stu-id="2bd52-110">Configure the Source Reader</span></span>](#configure-the-source-reader)
-   [<span data-ttu-id="2bd52-111">Запись заголовка ВОЛНового файла</span><span class="sxs-lookup"><span data-stu-id="2bd52-111">Write the WAVE File Header</span></span>](#write-the-wave-file-header)
-   [<span data-ttu-id="2bd52-112">Вычисление максимального размера данных</span><span class="sxs-lookup"><span data-stu-id="2bd52-112">Calculate the Maximum Data Size</span></span>](#calculate-the-maximum-data-size)
-   [<span data-ttu-id="2bd52-113">Декодирование звука</span><span class="sxs-lookup"><span data-stu-id="2bd52-113">Decode the Audio</span></span>](#decode-the-audio)
-   [<span data-ttu-id="2bd52-114">Финализировать заголовок файла</span><span class="sxs-lookup"><span data-stu-id="2bd52-114">Finalize the File Header</span></span>](#finalize-the-file-header)
-   [<span data-ttu-id="2bd52-115">См. также</span><span class="sxs-lookup"><span data-stu-id="2bd52-115">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="2bd52-116">Обзор</span><span class="sxs-lookup"><span data-stu-id="2bd52-116">Overview</span></span>

<span data-ttu-id="2bd52-117">В этом руководстве вы создадите консольное приложение, которое принимает два аргумента командной строки: имя входного файла, содержащего аудиопоток, и имя выходного файла.</span><span class="sxs-lookup"><span data-stu-id="2bd52-117">In this tutorial, you will create a console application that takes two command-line arguments: The name of an input file that contains an audio stream, and the output file name.</span></span> <span data-ttu-id="2bd52-118">Приложение считывает из входного файла пять секунд звуковых данных и записывает звук в выходной файл в виде ВОЛНовых данных.</span><span class="sxs-lookup"><span data-stu-id="2bd52-118">The application reads five seconds of audio data from the input file and writes the audio to the output file as WAVE data.</span></span>

<span data-ttu-id="2bd52-119">Для получения раскодированных звуковых данных приложение использует объект модуля чтения исходного кода.</span><span class="sxs-lookup"><span data-stu-id="2bd52-119">To get the decoded audio data, the application uses the source reader object.</span></span> <span data-ttu-id="2bd52-120">Модуль чтения исходного кода предоставляет интерфейс [**имфсаурцереадер**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) .</span><span class="sxs-lookup"><span data-stu-id="2bd52-120">The source reader exposes the [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) interface.</span></span> <span data-ttu-id="2bd52-121">Для записи декодированного звука в ВОЛНовый файл приложения используют функции ввода-вывода Windows.</span><span class="sxs-lookup"><span data-stu-id="2bd52-121">To write the decoded audio to the WAVE file, the applications uses Windows I/O functions.</span></span> <span data-ttu-id="2bd52-122">Этот процесс показан на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="2bd52-122">The following image illustrates this process.</span></span>

![Схема, показывающая средство чтения исходного кода, которое получает звуковые данные из исходного файла.](images/audio-clip-tutorial.gif)

<span data-ttu-id="2bd52-124">В простейшей форме файл WAVE имеет следующую структуру:</span><span class="sxs-lookup"><span data-stu-id="2bd52-124">In its simplest form, a WAVE file has the following structure:</span></span>



| <span data-ttu-id="2bd52-125">Тип данных</span><span class="sxs-lookup"><span data-stu-id="2bd52-125">Data Type</span></span>                              | <span data-ttu-id="2bd52-126">Размер (байт)</span><span class="sxs-lookup"><span data-stu-id="2bd52-126">Size (Bytes)</span></span> | <span data-ttu-id="2bd52-127">Значение</span><span class="sxs-lookup"><span data-stu-id="2bd52-127">Value</span></span>                                                                 |
|----------------------------------------|--------------|-----------------------------------------------------------------------|
| <span data-ttu-id="2bd52-128">**FOURCC**</span><span class="sxs-lookup"><span data-stu-id="2bd52-128">**FOURCC**</span></span>                             | <span data-ttu-id="2bd52-129">4</span><span class="sxs-lookup"><span data-stu-id="2bd52-129">4</span></span>            | <span data-ttu-id="2bd52-130">Metallica</span><span class="sxs-lookup"><span data-stu-id="2bd52-130">'RIFF'</span></span>                                                                |
| <span data-ttu-id="2bd52-131">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="2bd52-131">**DWORD**</span></span>                              | <span data-ttu-id="2bd52-132">4</span><span class="sxs-lookup"><span data-stu-id="2bd52-132">4</span></span>            | <span data-ttu-id="2bd52-133">Общий размер файла, не включая первые 8 байт</span><span class="sxs-lookup"><span data-stu-id="2bd52-133">Total file size, not including the first 8 bytes</span></span>                      |
| <span data-ttu-id="2bd52-134">**FOURCC**</span><span class="sxs-lookup"><span data-stu-id="2bd52-134">**FOURCC**</span></span>                             | <span data-ttu-id="2bd52-135">4</span><span class="sxs-lookup"><span data-stu-id="2bd52-135">4</span></span>            | <span data-ttu-id="2bd52-136">ЗВУКОВ</span><span class="sxs-lookup"><span data-stu-id="2bd52-136">'WAVE'</span></span>                                                                |
| <span data-ttu-id="2bd52-137">**FOURCC**</span><span class="sxs-lookup"><span data-stu-id="2bd52-137">**FOURCC**</span></span>                             | <span data-ttu-id="2bd52-138">4</span><span class="sxs-lookup"><span data-stu-id="2bd52-138">4</span></span>            | <span data-ttu-id="2bd52-139">FMT</span><span class="sxs-lookup"><span data-stu-id="2bd52-139">'fmt '</span></span>                                                                |
| <span data-ttu-id="2bd52-140">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="2bd52-140">**DWORD**</span></span>                              | <span data-ttu-id="2bd52-141">4</span><span class="sxs-lookup"><span data-stu-id="2bd52-141">4</span></span>            | <span data-ttu-id="2bd52-142">Размер данных [**вавеформатекс**](/previous-versions/dd757713(v=vs.85)) , приведенных ниже.</span><span class="sxs-lookup"><span data-stu-id="2bd52-142">Size of the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) data that follows.</span></span> |
| <span data-ttu-id="2bd52-143">[**вавеформатекс**](/previous-versions/dd757713(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2bd52-143">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span></span> | <span data-ttu-id="2bd52-144">Различается</span><span class="sxs-lookup"><span data-stu-id="2bd52-144">Varies</span></span>       | <span data-ttu-id="2bd52-145">Заголовок звукового формата.</span><span class="sxs-lookup"><span data-stu-id="2bd52-145">Audio format header.</span></span>                                                  |
| <span data-ttu-id="2bd52-146">**FOURCC**</span><span class="sxs-lookup"><span data-stu-id="2bd52-146">**FOURCC**</span></span>                             | <span data-ttu-id="2bd52-147">4</span><span class="sxs-lookup"><span data-stu-id="2bd52-147">4</span></span>            | <span data-ttu-id="2bd52-148">Data</span><span class="sxs-lookup"><span data-stu-id="2bd52-148">'data'</span></span>                                                                |
| <span data-ttu-id="2bd52-149">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="2bd52-149">**DWORD**</span></span>                              | <span data-ttu-id="2bd52-150">4</span><span class="sxs-lookup"><span data-stu-id="2bd52-150">4</span></span>            | <span data-ttu-id="2bd52-151">Размер звуковых данных.</span><span class="sxs-lookup"><span data-stu-id="2bd52-151">Size of the audio data.</span></span>                                               |
| <span data-ttu-id="2bd52-152">**ДВУХБАЙТОВЫХ**\[\]</span><span class="sxs-lookup"><span data-stu-id="2bd52-152">**BYTE**\[\]</span></span>                           | <span data-ttu-id="2bd52-153">Различается</span><span class="sxs-lookup"><span data-stu-id="2bd52-153">Varies</span></span>       | <span data-ttu-id="2bd52-154">Звуковые данные.</span><span class="sxs-lookup"><span data-stu-id="2bd52-154">Audio data.</span></span>                                                           |



 

> [!Note]  
> <span data-ttu-id="2bd52-155">**FourCC** — это **двойное слово** , сформированное путем сцепления четырех символов ASCII.</span><span class="sxs-lookup"><span data-stu-id="2bd52-155">A **FOURCC** is a **DWORD** formed by concatenating four ASCII characters.</span></span>

 

<span data-ttu-id="2bd52-156">Эту базовую структуру можно расширить, добавив метаданные файла и другую информацию, которая выходит за рамки данного руководства.</span><span class="sxs-lookup"><span data-stu-id="2bd52-156">This basic structure can be extended by adding file metadata and other information, which is beyond the scope of this tutorial.</span></span>

## <a name="header-and-library-files"></a><span data-ttu-id="2bd52-157">Файлы заголовков и библиотек</span><span class="sxs-lookup"><span data-stu-id="2bd52-157">Header and Library Files</span></span>

<span data-ttu-id="2bd52-158">Включите в проект следующие файлы заголовков:</span><span class="sxs-lookup"><span data-stu-id="2bd52-158">Include the following header files in your project:</span></span>


```C++
#define WINVER _WIN32_WINNT_WIN7

#include <windows.h>
#include <mfapi.h>
#include <mfidl.h>
#include <mfreadwrite.h>
#include <stdio.h>
#include <mferror.h>
```



<span data-ttu-id="2bd52-159">Ссылка на следующие библиотеки:</span><span class="sxs-lookup"><span data-stu-id="2bd52-159">Link to the following libraries:</span></span>

-   <span data-ttu-id="2bd52-160">мфплат. lib</span><span class="sxs-lookup"><span data-stu-id="2bd52-160">mfplat.lib</span></span>
-   <span data-ttu-id="2bd52-161">мфреадврите. lib</span><span class="sxs-lookup"><span data-stu-id="2bd52-161">mfreadwrite.lib</span></span>
-   <span data-ttu-id="2bd52-162">мфууид. lib</span><span class="sxs-lookup"><span data-stu-id="2bd52-162">mfuuid.lib</span></span>

## <a name="implement-wmain"></a><span data-ttu-id="2bd52-163">Реализация wmain</span><span class="sxs-lookup"><span data-stu-id="2bd52-163">Implement wmain</span></span>

<span data-ttu-id="2bd52-164">В следующем коде показана функция точки входа для приложения.</span><span class="sxs-lookup"><span data-stu-id="2bd52-164">The following code shows the entry-point function for the application.</span></span>


```C++
int wmain(int argc, wchar_t* argv[])
{
    HeapSetInformation(NULL, HeapEnableTerminationOnCorruption, NULL, 0);

    if (argc != 3)
    {
        printf("arguments: input_file output_file.wav\n");
        return 1;
    }

    const WCHAR *wszSourceFile = argv[1];
    const WCHAR *wszTargetFile = argv[2];

    const LONG MAX_AUDIO_DURATION_MSEC = 5000; // 5 seconds

    HRESULT hr = S_OK;

    IMFSourceReader *pReader = NULL;
    HANDLE hFile = INVALID_HANDLE_VALUE;

    // Initialize the COM library.
    hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | COINIT_DISABLE_OLE1DDE);

    // Initialize the Media Foundation platform.
    if (SUCCEEDED(hr))
    {
        hr = MFStartup(MF_VERSION);
    }

    // Create the source reader to read the input file.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateSourceReaderFromURL(wszSourceFile, NULL, &pReader);
        if (FAILED(hr))
        {
            printf("Error opening input file: %S\n", wszSourceFile, hr);
        }
    }

    // Open the output file for writing.
    if (SUCCEEDED(hr))
    {
        hFile = CreateFile(wszTargetFile, GENERIC_WRITE, FILE_SHARE_READ, NULL,
            CREATE_ALWAYS, 0, NULL);

        if (hFile == INVALID_HANDLE_VALUE)
        {
            hr = HRESULT_FROM_WIN32(GetLastError());
            printf("Cannot create output file: %S\n", wszTargetFile, hr);
        }
    }

    // Write the WAVE file.
    if (SUCCEEDED(hr))
    {
        hr = WriteWaveFile(pReader, hFile, MAX_AUDIO_DURATION_MSEC);
    }

    if (FAILED(hr))
    {
        printf("Failed, hr = 0x%X\n", hr);
    }

    // Clean up.
    if (hFile != INVALID_HANDLE_VALUE)
    {
        CloseHandle(hFile);
    }

    SafeRelease(&pReader);
    MFShutdown();
    CoUninitialize();

    return SUCCEEDED(hr) ? 0 : 1;
};
```



<span data-ttu-id="2bd52-165">Эта функция выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="2bd52-165">This function does the following:</span></span>

1.  <span data-ttu-id="2bd52-166">Вызывает [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) для инициализации библиотеки COM.</span><span class="sxs-lookup"><span data-stu-id="2bd52-166">Calls [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) to initialize the COM library.</span></span>
2.  <span data-ttu-id="2bd52-167">Вызывает [**мфстартуп**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) для инициализации платформы Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="2bd52-167">Calls [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) to initialize the Media Foundation platform.</span></span>
3.  <span data-ttu-id="2bd52-168">Вызывает [**мфкреатесаурцереадерфромурл**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl) для создания модуля чтения исходного кода.</span><span class="sxs-lookup"><span data-stu-id="2bd52-168">Calls [**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl) to create the source reader.</span></span> <span data-ttu-id="2bd52-169">Эта функция принимает имя входного файла и получает указатель интерфейса [**имфсаурцереадер**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) .</span><span class="sxs-lookup"><span data-stu-id="2bd52-169">This function takes the name of the input file and receives an [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) interface pointer.</span></span>
4.  <span data-ttu-id="2bd52-170">Создает выходной файл, вызывая функцию **CreateFile** , которая возвращает маркер файла.</span><span class="sxs-lookup"><span data-stu-id="2bd52-170">Creates the output file by calling the **CreateFile** function, which returns a file handle.</span></span>
5.  <span data-ttu-id="2bd52-171">Вызывает определяемую приложением функцию [вритевавфиле](#write-the-wave-file) .</span><span class="sxs-lookup"><span data-stu-id="2bd52-171">Calls the application-defined [WriteWavFile](#write-the-wave-file) function.</span></span> <span data-ttu-id="2bd52-172">Эта функция декодирует аудио и записывает звуковой файл.</span><span class="sxs-lookup"><span data-stu-id="2bd52-172">This function decodes the audio and writes the WAVE file.</span></span>
6.  <span data-ttu-id="2bd52-173">Освобождает указатель [**имфсаурцереадер**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) и дескриптор файла.</span><span class="sxs-lookup"><span data-stu-id="2bd52-173">Releases the [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) pointer and the file handle.</span></span>
7.  <span data-ttu-id="2bd52-174">Вызывает [**мфшутдовн**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) для завершения работы платформы Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="2bd52-174">Calls [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) to shut down the Media Foundation platform.</span></span>
8.  <span data-ttu-id="2bd52-175">Вызывает [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) для освобождения библиотеки COM.</span><span class="sxs-lookup"><span data-stu-id="2bd52-175">Calls [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) to release the COM library.</span></span>

## <a name="write-the-wave-file"></a><span data-ttu-id="2bd52-176">Запись файла WAVE</span><span class="sxs-lookup"><span data-stu-id="2bd52-176">Write the WAVE File</span></span>

<span data-ttu-id="2bd52-177">Большая часть работы происходит в `WriteWavFile` функции, которая вызывается из `wmain` .</span><span class="sxs-lookup"><span data-stu-id="2bd52-177">Most of the work happens in the `WriteWavFile` function, which is called from `wmain`.</span></span>


```C++
//-------------------------------------------------------------------
// WriteWaveFile
//
// Writes a WAVE file by getting audio data from the source reader.
//
//-------------------------------------------------------------------

HRESULT WriteWaveFile(
    IMFSourceReader *pReader,   // Pointer to the source reader.
    HANDLE hFile,               // Handle to the output file.
    LONG msecAudioData          // Maximum amount of audio data to write, in msec.
    )
{
    HRESULT hr = S_OK;

    DWORD cbHeader = 0;         // Size of the WAVE file header, in bytes.
    DWORD cbAudioData = 0;      // Total bytes of PCM audio data written to the file.
    DWORD cbMaxAudioData = 0;

    IMFMediaType *pAudioType = NULL;    // Represents the PCM audio format.

    // Configure the source reader to get uncompressed PCM audio from the source file.

    hr = ConfigureAudioStream(pReader, &pAudioType);

    // Write the WAVE file header.
    if (SUCCEEDED(hr))
    {
        hr = WriteWaveHeader(hFile, pAudioType, &cbHeader);
    }

    // Calculate the maximum amount of audio to decode, in bytes.
    if (SUCCEEDED(hr))
    {
        cbMaxAudioData = CalculateMaxAudioDataSize(pAudioType, cbHeader, msecAudioData);

        // Decode audio data to the file.
        hr = WriteWaveData(hFile, pReader, cbMaxAudioData, &cbAudioData);
    }

    // Fix up the RIFF headers with the correct sizes.
    if (SUCCEEDED(hr))
    {
        hr = FixUpChunkSizes(hFile, cbHeader, cbAudioData);
    }

    SafeRelease(&pAudioType);
    return hr;
}
```



<span data-ttu-id="2bd52-178">Эта функция вызывает ряд других определяемых приложением функций:</span><span class="sxs-lookup"><span data-stu-id="2bd52-178">This function calls a series of other application-defined functions:</span></span>

1.  <span data-ttu-id="2bd52-179">Функция [конфигуреаудиостреам](#configure-the-source-reader) Инициализирует модуль чтения исходного кода.</span><span class="sxs-lookup"><span data-stu-id="2bd52-179">The [ConfigureAudioStream](#configure-the-source-reader) function initializes the source reader.</span></span> <span data-ttu-id="2bd52-180">Эта функция получает указатель на интерфейс [**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) , который используется для получения описания раскодированного аудио формата, включая частоту выборки, число каналов и глубину бит (бит на выборку).</span><span class="sxs-lookup"><span data-stu-id="2bd52-180">This function receives a pointer to the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface, which is used to get a description of the decoded audio format, including sample rate, number of channels, and bit depth (bits per sample).</span></span>
2.  <span data-ttu-id="2bd52-181">Функция Вритевавехеадер записывает первую часть ВОЛНового файла, включая заголовок и начало фрагмента данных.</span><span class="sxs-lookup"><span data-stu-id="2bd52-181">The WriteWaveHeader function writes the first part of the WAVE file, including the header and the start of the 'data' chunk.</span></span>
3.  <span data-ttu-id="2bd52-182">Функция Калкулатемаксаудиодатасизе вычисляет максимальный объем аудиоданных для записи в файл в байтах.</span><span class="sxs-lookup"><span data-stu-id="2bd52-182">The CalculateMaxAudioDataSize function calculates the maximum amount of audio to write to the file, in bytes.</span></span>
4.  <span data-ttu-id="2bd52-183">Функция Вритеваведата записывает звуковые данные PCM в файл.</span><span class="sxs-lookup"><span data-stu-id="2bd52-183">The WriteWaveData function writes the PCM audio data to the file.</span></span>
5.  <span data-ttu-id="2bd52-184">Функция Фиксупчунксизес записывает сведения о размере файла, которые отображаются после значений "Metallica" и "Data" **FourCC** в волном файле.</span><span class="sxs-lookup"><span data-stu-id="2bd52-184">The FixUpChunkSizes function writes the file-size information that appears after the 'RIFF' and 'data' **FOURCC** values in the WAVE file.</span></span> <span data-ttu-id="2bd52-185">(Эти значения неизвестны до `WriteWaveData` завершения.)</span><span class="sxs-lookup"><span data-stu-id="2bd52-185">(These values are not known until `WriteWaveData` completes.)</span></span>

<span data-ttu-id="2bd52-186">Эти функции показаны в остальных разделах этого руководства.</span><span class="sxs-lookup"><span data-stu-id="2bd52-186">These functions are shown in the remaining sections of this tutorial.</span></span>

## <a name="configure-the-source-reader"></a><span data-ttu-id="2bd52-187">Настройка модуля чтения исходного кода</span><span class="sxs-lookup"><span data-stu-id="2bd52-187">Configure the Source Reader</span></span>

<span data-ttu-id="2bd52-188">`ConfigureAudioStream`Функция настраивает модуль чтения исходного кода для декодирования звукового потока в исходном файле.</span><span class="sxs-lookup"><span data-stu-id="2bd52-188">The `ConfigureAudioStream` function configures the source reader to decode the audio stream in the source file.</span></span> <span data-ttu-id="2bd52-189">Он также возвращает сведения о формате декодированного звука.</span><span class="sxs-lookup"><span data-stu-id="2bd52-189">It also returns information about the format of the decoded audio.</span></span>

<span data-ttu-id="2bd52-190">В Media Foundation форматы мультимедиа описываются с помощью объектов *типа мультимедиа* .</span><span class="sxs-lookup"><span data-stu-id="2bd52-190">In Media Foundation, media formats are described using *media type* objects.</span></span> <span data-ttu-id="2bd52-191">Объект типа мультимедиа предоставляет интерфейс [**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) , который наследует интерфейс [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="2bd52-191">A media type object exposes the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface, which inherits the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span> <span data-ttu-id="2bd52-192">По сути, тип носителя — это коллекция свойств, описывающих формат.</span><span class="sxs-lookup"><span data-stu-id="2bd52-192">Essentially, a media type is a collection of properties that describe the format.</span></span> <span data-ttu-id="2bd52-193">Дополнительные сведения см. в разделе [типы носителей](media-types.md).</span><span class="sxs-lookup"><span data-stu-id="2bd52-193">For more information, see [Media Types](media-types.md).</span></span>


```C++
//-------------------------------------------------------------------
// ConfigureAudioStream
//
// Selects an audio stream from the source file, and configures the
// stream to deliver decoded PCM audio.
//-------------------------------------------------------------------

HRESULT ConfigureAudioStream(
    IMFSourceReader *pReader,   // Pointer to the source reader.
    IMFMediaType **ppPCMAudio   // Receives the audio format.
    )
{
    IMFMediaType *pUncompressedAudioType = NULL;
    IMFMediaType *pPartialType = NULL;

    // Select the first audio stream, and deselect all other streams.
    HRESULT hr = pReader->SetStreamSelection(
        (DWORD)MF_SOURCE_READER_ALL_STREAMS, FALSE);

    if (SUCCEEDED(hr))
    {
        hr = pReader->SetStreamSelection(
            (DWORD)MF_SOURCE_READER_FIRST_AUDIO_STREAM, TRUE);
    }

    // Create a partial media type that specifies uncompressed PCM audio.
    hr = MFCreateMediaType(&pPartialType);

    if (SUCCEEDED(hr))
    {
        hr = pPartialType->SetGUID(MF_MT_MAJOR_TYPE, MFMediaType_Audio);
    }

    if (SUCCEEDED(hr))
    {
        hr = pPartialType->SetGUID(MF_MT_SUBTYPE, MFAudioFormat_PCM);
    }

    // Set this type on the source reader. The source reader will
    // load the necessary decoder.
    if (SUCCEEDED(hr))
    {
        hr = pReader->SetCurrentMediaType(
            (DWORD)MF_SOURCE_READER_FIRST_AUDIO_STREAM,
            NULL, pPartialType);
    }

    // Get the complete uncompressed format.
    if (SUCCEEDED(hr))
    {
        hr = pReader->GetCurrentMediaType(
            (DWORD)MF_SOURCE_READER_FIRST_AUDIO_STREAM,
            &pUncompressedAudioType);
    }

    // Ensure the stream is selected.
    if (SUCCEEDED(hr))
    {
        hr = pReader->SetStreamSelection(
            (DWORD)MF_SOURCE_READER_FIRST_AUDIO_STREAM,
            TRUE);
    }

    // Return the PCM format to the caller.
    if (SUCCEEDED(hr))
    {
        *ppPCMAudio = pUncompressedAudioType;
        (*ppPCMAudio)->AddRef();
    }

    SafeRelease(&pUncompressedAudioType);
    SafeRelease(&pPartialType);
    return hr;
}
```



<span data-ttu-id="2bd52-194">`ConfigureAudioStream`Функция выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="2bd52-194">The `ConfigureAudioStream` function does the following:</span></span>

1.  <span data-ttu-id="2bd52-195">Вызывает метод [**имфсаурцереадер:: сетстреамселектион**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setstreamselection) , чтобы выбрать аудиопоток и отменить выбор всех остальных потоков.</span><span class="sxs-lookup"><span data-stu-id="2bd52-195">Calls the [**IMFSourceReader::SetStreamSelection**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setstreamselection) method to select the audio stream and deselect all other streams.</span></span> <span data-ttu-id="2bd52-196">Этот шаг может повысить производительность, так как предотвращает удержание модуля чтения исходного кода на видеокадры, которые не используются приложением.</span><span class="sxs-lookup"><span data-stu-id="2bd52-196">This step can improve performance, because it prevents the source reader from holding onto video frames that the application does not use.</span></span>
2.  <span data-ttu-id="2bd52-197">Создает *частичный* тип носителя, указывающий звук PCM.</span><span class="sxs-lookup"><span data-stu-id="2bd52-197">Creates a *partial* media type that specifies PCM audio.</span></span> <span data-ttu-id="2bd52-198">Функция создает разделяемый тип следующим образом:</span><span class="sxs-lookup"><span data-stu-id="2bd52-198">The function creates the partial type as follows:</span></span>
    1.  <span data-ttu-id="2bd52-199">Вызывает [**мфкреатемедиатипе**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype) для создания пустого объекта типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="2bd52-199">Calls [**MFCreateMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype) to create an empty media type object.</span></span>
    2.  <span data-ttu-id="2bd52-200">Устанавливает атрибут [**\_ \_ основного \_ типа MF MT**](mf-mt-major-type-attribute.md) в **мфмедиатипе \_ Audio**.</span><span class="sxs-lookup"><span data-stu-id="2bd52-200">Sets the [**MF\_MT\_MAJOR\_TYPE**](mf-mt-major-type-attribute.md) attribute to **MFMediaType\_Audio**.</span></span>
    3.  <span data-ttu-id="2bd52-201">Устанавливает атрибут [**\_ \_ подтипа MF MT**](mf-mt-subtype-attribute.md) в **мфаудиоформат \_ PCM**.</span><span class="sxs-lookup"><span data-stu-id="2bd52-201">Sets the [**MF\_MT\_SUBTYPE**](mf-mt-subtype-attribute.md) attribute to **MFAudioFormat\_PCM**.</span></span>
3.  <span data-ttu-id="2bd52-202">Вызывает [**имфсаурцереадер:: сеткуррентмедиатипе**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype) для установки разделяемого типа в модуле чтения исходного кода.</span><span class="sxs-lookup"><span data-stu-id="2bd52-202">Calls [**IMFSourceReader::SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype) to set the partial type on the source reader.</span></span> <span data-ttu-id="2bd52-203">Если исходный файл содержит закодированный звук, модуль чтения исходного кода автоматически загружает необходимый звуковой декодер.</span><span class="sxs-lookup"><span data-stu-id="2bd52-203">If the source file contains encoded audio, the source reader automatically loads the necessary audio decoder.</span></span>
4.  <span data-ttu-id="2bd52-204">Вызывает [**имфсаурцереадер:: жеткуррентмедиатипе**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype) , чтобы получить фактический тип носителя PCM.</span><span class="sxs-lookup"><span data-stu-id="2bd52-204">Calls [**IMFSourceReader::GetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype) to get the actual PCM media type.</span></span> <span data-ttu-id="2bd52-205">Этот метод возвращает тип носителя со всеми заполненными сведениями о формате, например скорость дискретизации и число каналов.</span><span class="sxs-lookup"><span data-stu-id="2bd52-205">This method returns a media type with all of the format details filled in, such as the audio sample rate and the number of channels.</span></span>
5.  <span data-ttu-id="2bd52-206">Вызывает [**имфсаурцереадер:: сетстреамселектион**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setstreamselection) для включения аудиопотока.</span><span class="sxs-lookup"><span data-stu-id="2bd52-206">Calls [**IMFSourceReader::SetStreamSelection**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setstreamselection) to enable the audio stream.</span></span>

## <a name="write-the-wave-file-header"></a><span data-ttu-id="2bd52-207">Запись заголовка ВОЛНового файла</span><span class="sxs-lookup"><span data-stu-id="2bd52-207">Write the WAVE File Header</span></span>

<span data-ttu-id="2bd52-208">`WriteWaveHeader`Функция записывает заголовок волнового файла.</span><span class="sxs-lookup"><span data-stu-id="2bd52-208">The `WriteWaveHeader` function writes the WAVE file header.</span></span>

<span data-ttu-id="2bd52-209">Единственным Media Foundation API, вызываемым из этой функции, является [**мфкреатевавеформатексфроммфмедиатипе**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatewaveformatexfrommfmediatype), который преобразует тип мультимедиа в структуру [**вавеформатекс**](/previous-versions/dd757713(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="2bd52-209">The only Media Foundation API called from this function is [**MFCreateWaveFormatExFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatewaveformatexfrommfmediatype), which converts the media type to a [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span>


```C++
//-------------------------------------------------------------------
// WriteWaveHeader
//
// Write the WAVE file header.
//
// Note: This function writes placeholder values for the file size
// and data size, as these values will need to be filled in later.
//-------------------------------------------------------------------

HRESULT WriteWaveHeader(
    HANDLE hFile,               // Output file.
    IMFMediaType *pMediaType,   // PCM audio format.
    DWORD *pcbWritten           // Receives the size of the header.
    )
{
    HRESULT hr = S_OK;
    UINT32 cbFormat = 0;

    WAVEFORMATEX *pWav = NULL;

    *pcbWritten = 0;

    // Convert the PCM audio format into a WAVEFORMATEX structure.
    hr = MFCreateWaveFormatExFromMFMediaType(pMediaType, &pWav, &cbFormat);

    // Write the 'RIFF' header and the start of the 'fmt ' chunk.
    if (SUCCEEDED(hr))
    {
        DWORD header[] = {
            // RIFF header
            FCC('RIFF'),
            0,
            FCC('WAVE'),
            // Start of 'fmt ' chunk
            FCC('fmt '),
            cbFormat
        };

        DWORD dataHeader[] = { FCC('data'), 0 };

        hr = WriteToFile(hFile, header, sizeof(header));

        // Write the WAVEFORMATEX structure.
        if (SUCCEEDED(hr))
        {
            hr = WriteToFile(hFile, pWav, cbFormat);
        }

        // Write the start of the 'data' chunk

        if (SUCCEEDED(hr))
        {
            hr = WriteToFile(hFile, dataHeader, sizeof(dataHeader));
        }

        if (SUCCEEDED(hr))
        {
            *pcbWritten = sizeof(header) + cbFormat + sizeof(dataHeader);
        }
    }


    CoTaskMemFree(pWav);
    return hr;
}
```



<span data-ttu-id="2bd52-210">`WriteToFile`Функция — это простая вспомогательная функция, которая заключает в оболочку функцию Windows **WriteFile** и возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2bd52-210">The `WriteToFile` function is a simple helper function that wraps the Windows **WriteFile** function and returns an **HRESULT** value.</span></span>


```C++
//-------------------------------------------------------------------
//
// Writes a block of data to a file
//
// hFile: Handle to the file.
// p: Pointer to the buffer to write.
// cb: Size of the buffer, in bytes.
//
//-------------------------------------------------------------------

HRESULT WriteToFile(HANDLE hFile, void* p, DWORD cb)
{
    DWORD cbWritten = 0;
    HRESULT hr = S_OK;

    BOOL bResult = WriteFile(hFile, p, cb, &cbWritten, NULL);
    if (!bResult)
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
    }
    return hr;
}
```



## <a name="calculate-the-maximum-data-size"></a><span data-ttu-id="2bd52-211">Вычисление максимального размера данных</span><span class="sxs-lookup"><span data-stu-id="2bd52-211">Calculate the Maximum Data Size</span></span>

<span data-ttu-id="2bd52-212">Так как размер файла хранится в виде 4-байтового значения в заголовке файла, файл звукозаписи ограничивается максимальным размером в 0xFFFFFFFF байт — примерно 4 ГБ.</span><span class="sxs-lookup"><span data-stu-id="2bd52-212">Because the file size is stored as a 4-byte value in the file header, a WAVE file is limited to a maximum size of 0xFFFFFFFF bytes—approximately 4 GB.</span></span> <span data-ttu-id="2bd52-213">Это значение включает размер заголовка файла.</span><span class="sxs-lookup"><span data-stu-id="2bd52-213">This value includes the size of the file header.</span></span> <span data-ttu-id="2bd52-214">Звук PCM имеет постоянную скорость, поэтому вы можете вычислить максимальный размер данных из аудио формата следующим образом:</span><span class="sxs-lookup"><span data-stu-id="2bd52-214">PCM audio has a constant bit rate, so you can calculate the maximum data size from the audio format, as follows:</span></span>


```C++
//-------------------------------------------------------------------
// CalculateMaxAudioDataSize
//
// Calculates how much audio to write to the WAVE file, given the
// audio format and the maximum duration of the WAVE file.
//-------------------------------------------------------------------

DWORD CalculateMaxAudioDataSize(
    IMFMediaType *pAudioType,    // The PCM audio format.
    DWORD cbHeader,              // The size of the WAVE file header.
    DWORD msecAudioData          // Maximum duration, in milliseconds.
    )
{
    UINT32 cbBlockSize = 0;         // Audio frame size, in bytes.
    UINT32 cbBytesPerSecond = 0;    // Bytes per second.

    // Get the audio block size and number of bytes/second from the audio format.

    cbBlockSize = MFGetAttributeUINT32(pAudioType, MF_MT_AUDIO_BLOCK_ALIGNMENT, 0);
    cbBytesPerSecond = MFGetAttributeUINT32(pAudioType, MF_MT_AUDIO_AVG_BYTES_PER_SECOND, 0);

    // Calculate the maximum amount of audio data to write.
    // This value equals (duration in seconds x bytes/second), but cannot
    // exceed the maximum size of the data chunk in the WAVE file.

        // Size of the desired audio clip in bytes:
    DWORD cbAudioClipSize = (DWORD)MulDiv(cbBytesPerSecond, msecAudioData, 1000);

    // Largest possible size of the data chunk:
    DWORD cbMaxSize = MAXDWORD - cbHeader;

    // Maximum size altogether.
    cbAudioClipSize = min(cbAudioClipSize, cbMaxSize);

    // Round to the audio block size, so that we do not write a partial audio frame.
    cbAudioClipSize = (cbAudioClipSize / cbBlockSize) * cbBlockSize;

    return cbAudioClipSize;
}
```



<span data-ttu-id="2bd52-215">Чтобы избежать частичных звуковых кадров, размер округляется до выравнивания блока, который хранится в атрибуте [**\_ \_ \_ \_ выравнивания звукового блока MF MT**](mf-mt-audio-block-alignment-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="2bd52-215">To avoid partial audio frames, the size is rounded to the block alignment, which is stored in the [**MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT**](mf-mt-audio-block-alignment-attribute.md) attribute.</span></span>

## <a name="decode-the-audio"></a><span data-ttu-id="2bd52-216">Декодирование звука</span><span class="sxs-lookup"><span data-stu-id="2bd52-216">Decode the Audio</span></span>

<span data-ttu-id="2bd52-217">`WriteWaveData`Функция считывает декодированный звук из исходного файла и выполняет запись в волновый файл.</span><span class="sxs-lookup"><span data-stu-id="2bd52-217">The `WriteWaveData` function reads decoded audio from the source file and writes to the WAVE file.</span></span>


```C++
//-------------------------------------------------------------------
// WriteWaveData
//
// Decodes PCM audio data from the source file and writes it to
// the WAVE file.
//-------------------------------------------------------------------

HRESULT WriteWaveData(
    HANDLE hFile,               // Output file.
    IMFSourceReader *pReader,   // Source reader.
    DWORD cbMaxAudioData,       // Maximum amount of audio data (bytes).
    DWORD *pcbDataWritten       // Receives the amount of data written.
    )
{
    HRESULT hr = S_OK;
    DWORD cbAudioData = 0;
    DWORD cbBuffer = 0;
    BYTE *pAudioData = NULL;

    IMFSample *pSample = NULL;
    IMFMediaBuffer *pBuffer = NULL;

    // Get audio samples from the source reader.
    while (true)
    {
        DWORD dwFlags = 0;

        // Read the next sample.
        hr = pReader->ReadSample(
            (DWORD)MF_SOURCE_READER_FIRST_AUDIO_STREAM,
            0, NULL, &dwFlags, NULL, &pSample );

        if (FAILED(hr)) { break; }

        if (dwFlags & MF_SOURCE_READERF_CURRENTMEDIATYPECHANGED)
        {
            printf("Type change - not supported by WAVE file format.\n");
            break;
        }
        if (dwFlags & MF_SOURCE_READERF_ENDOFSTREAM)
        {
            printf("End of input file.\n");
            break;
        }

        if (pSample == NULL)
        {
            printf("No sample\n");
            continue;
        }

        // Get a pointer to the audio data in the sample.

        hr = pSample->ConvertToContiguousBuffer(&pBuffer);

        if (FAILED(hr)) { break; }


        hr = pBuffer->Lock(&pAudioData, NULL, &cbBuffer);

        if (FAILED(hr)) { break; }


        // Make sure not to exceed the specified maximum size.
        if (cbMaxAudioData - cbAudioData < cbBuffer)
        {
            cbBuffer = cbMaxAudioData - cbAudioData;
        }

        // Write this data to the output file.
        hr = WriteToFile(hFile, pAudioData, cbBuffer);

        if (FAILED(hr)) { break; }

        // Unlock the buffer.
        hr = pBuffer->Unlock();
        pAudioData = NULL;

        if (FAILED(hr)) { break; }

        // Update running total of audio data.
        cbAudioData += cbBuffer;

        if (cbAudioData >= cbMaxAudioData)
        {
            break;
        }

        SafeRelease(&pSample);
        SafeRelease(&pBuffer);
    }

    if (SUCCEEDED(hr))
    {
        printf("Wrote %d bytes of audio data.\n", cbAudioData);

        *pcbDataWritten = cbAudioData;
    }

    if (pAudioData)
    {
        pBuffer->Unlock();
    }

    SafeRelease(&pBuffer);
    SafeRelease(&pSample);
    return hr;
}
```



<span data-ttu-id="2bd52-218">`WriteWaveData`Функция выполняет следующие функции в цикле:</span><span class="sxs-lookup"><span data-stu-id="2bd52-218">The `WriteWaveData` function does the following in a loop:</span></span>

1.  <span data-ttu-id="2bd52-219">Вызывает [**имфсаурцереадер:: реадсампле**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) для чтения звука из исходного файла.</span><span class="sxs-lookup"><span data-stu-id="2bd52-219">Calls [**IMFSourceReader::ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) to read audio from the source file.</span></span> <span data-ttu-id="2bd52-220">Параметр *dwFlags* получает побитовое **или** из перечисления [**\_ \_ \_ флагов считывания источника MF**](/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_flag) .</span><span class="sxs-lookup"><span data-stu-id="2bd52-220">The *dwFlags* parameter receives a bitwise **OR** of flags from the [**MF\_SOURCE\_READER\_FLAG**](/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_flag) enumeration.</span></span> <span data-ttu-id="2bd52-221">Параметр *псампле* получает указатель на интерфейс [**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , который используется для доступа к звуковым данным.</span><span class="sxs-lookup"><span data-stu-id="2bd52-221">The *pSample* parameter receives a pointer to the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface, which is used to access the audio data.</span></span> <span data-ttu-id="2bd52-222">В некоторых случаях вызов **реадсампле** не создает данные, в этом случае указатель **Имфсампле** имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="2bd52-222">In some cases a call to **ReadSample** does not generate data, in which case the **IMFSample** pointer is **NULL**.</span></span>
2.  <span data-ttu-id="2bd52-223">Проверяет *dwFlags* для следующих флагов:</span><span class="sxs-lookup"><span data-stu-id="2bd52-223">Checks *dwFlags* for the following flags:</span></span>
    -   <span data-ttu-id="2bd52-224">**MF \_ SOURCE \_ реадерф \_ куррентмедиатипечанжед**.</span><span class="sxs-lookup"><span data-stu-id="2bd52-224">**MF\_SOURCE\_READERF\_CURRENTMEDIATYPECHANGED**.</span></span> <span data-ttu-id="2bd52-225">Этот флаг указывает на изменение формата в исходном файле.</span><span class="sxs-lookup"><span data-stu-id="2bd52-225">This flag indicates a format change in the source file.</span></span> <span data-ttu-id="2bd52-226">Файлы WAVE не поддерживают изменения формата.</span><span class="sxs-lookup"><span data-stu-id="2bd52-226">WAVE files do not support format changes.</span></span>
    -   <span data-ttu-id="2bd52-227">**MF \_ SOURCE \_ реадерф \_ ENDOFSTREAM**.</span><span class="sxs-lookup"><span data-stu-id="2bd52-227">**MF\_SOURCE\_READERF\_ENDOFSTREAM**.</span></span> <span data-ttu-id="2bd52-228">Этот флаг указывает конец потока.</span><span class="sxs-lookup"><span data-stu-id="2bd52-228">This flag indicates the end of the stream.</span></span>
3.  <span data-ttu-id="2bd52-229">Вызывает [**имфсампле:: конверттоконтигуаусбуффер**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-converttocontiguousbuffer) для получения указателя на объект буфера.</span><span class="sxs-lookup"><span data-stu-id="2bd52-229">Calls [**IMFSample::ConvertToContiguousBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-converttocontiguousbuffer) to get a pointer to a buffer object.</span></span>
4.  <span data-ttu-id="2bd52-230">Вызывает [**имфмедиабуффер:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) для получения указателя на буферную память.</span><span class="sxs-lookup"><span data-stu-id="2bd52-230">Calls [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) to get a pointer to the buffer memory.</span></span>
5.  <span data-ttu-id="2bd52-231">Записывает звуковые данные в выходной файл.</span><span class="sxs-lookup"><span data-stu-id="2bd52-231">Writes the audio data to the output file.</span></span>
6.  <span data-ttu-id="2bd52-232">Вызывает метод [**имфмедиабуффер:: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) для разблокировки объекта буфера.</span><span class="sxs-lookup"><span data-stu-id="2bd52-232">Calls [**IMFMediaBuffer::Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) to unlock the buffer object.</span></span>

<span data-ttu-id="2bd52-233">Функция выходит из цикла, когда происходит любое из следующих условий:</span><span class="sxs-lookup"><span data-stu-id="2bd52-233">The function breaks out of the loop when any of the following occur:</span></span>

-   <span data-ttu-id="2bd52-234">Изменяется формат потока.</span><span class="sxs-lookup"><span data-stu-id="2bd52-234">The stream format changes.</span></span>
-   <span data-ttu-id="2bd52-235">Достигнут конец потока.</span><span class="sxs-lookup"><span data-stu-id="2bd52-235">The end of the stream is reached.</span></span>
-   <span data-ttu-id="2bd52-236">Максимальный объем звуковых данных записывается в выходной файл.</span><span class="sxs-lookup"><span data-stu-id="2bd52-236">The maximum amount of audio data is written to the output file.</span></span>
-   <span data-ttu-id="2bd52-237">Возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="2bd52-237">An error occurs.</span></span>

## <a name="finalize-the-file-header"></a><span data-ttu-id="2bd52-238">Финализировать заголовок файла</span><span class="sxs-lookup"><span data-stu-id="2bd52-238">Finalize the File Header</span></span>

<span data-ttu-id="2bd52-239">Значения размера, хранящиеся в заголовке WAVE, неизвестны до завершения предыдущей функции.</span><span class="sxs-lookup"><span data-stu-id="2bd52-239">The size values that are stored in the WAVE header are not known until the previous function completes.</span></span> <span data-ttu-id="2bd52-240">`FixUpChunkSizes`Заполнит следующие значения:</span><span class="sxs-lookup"><span data-stu-id="2bd52-240">The `FixUpChunkSizes` fills in these values:</span></span>


```C++
//-------------------------------------------------------------------
// FixUpChunkSizes
//
// Writes the file-size information into the WAVE file header.
//
// WAVE files use the RIFF file format. Each RIFF chunk has a data
// size, and the RIFF header has a total file size.
//-------------------------------------------------------------------

HRESULT FixUpChunkSizes(
    HANDLE hFile,           // Output file.
    DWORD cbHeader,         // Size of the 'fmt ' chuck.
    DWORD cbAudioData       // Size of the 'data' chunk.
    )
{
    HRESULT hr = S_OK;

    LARGE_INTEGER ll;
    ll.QuadPart = cbHeader - sizeof(DWORD);

    if (0 == SetFilePointerEx(hFile, ll, NULL, FILE_BEGIN))
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
    }

    // Write the data size.

    if (SUCCEEDED(hr))
    {
        hr = WriteToFile(hFile, &cbAudioData, sizeof(cbAudioData));
    }

    if (SUCCEEDED(hr))
    {
        // Write the file size.
        ll.QuadPart = sizeof(FOURCC);

        if (0 == SetFilePointerEx(hFile, ll, NULL, FILE_BEGIN))
        {
            hr = HRESULT_FROM_WIN32(GetLastError());
        }
    }

    if (SUCCEEDED(hr))
    {
        DWORD cbRiffFileSize = cbHeader + cbAudioData - 8;

        // NOTE: The "size" field in the RIFF header does not include
        // the first 8 bytes of the file. (That is, the size of the
        // data that appears after the size field.)

        hr = WriteToFile(hFile, &cbRiffFileSize, sizeof(cbRiffFileSize));
    }

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="2bd52-241">См. также</span><span class="sxs-lookup"><span data-stu-id="2bd52-241">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2bd52-242">Типы звуковых носителей</span><span class="sxs-lookup"><span data-stu-id="2bd52-242">Audio Media Types</span></span>](audio-media-types.md)
</dt> <dt>

[<span data-ttu-id="2bd52-243">Модуль чтения исходного кода</span><span class="sxs-lookup"><span data-stu-id="2bd52-243">Source Reader</span></span>](source-reader.md)
</dt> <dt>

[<span data-ttu-id="2bd52-244">**имфсаурцереадер**</span><span class="sxs-lookup"><span data-stu-id="2bd52-244">**IMFSourceReader**</span></span>](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader)
</dt> </dl>

 

 

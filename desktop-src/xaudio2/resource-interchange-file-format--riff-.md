---
description: В этом обзоре описывается формат файла обмена ресурсами (Metallica), который используется в WAV-файлах. Metallica — типичный формат, из которого будут загружены звуковые данные для XAudio2.
ms.assetid: b543e949-223c-ddd3-7527-a41f3709a0c1
title: Формат RIFF (Resource Interchange File Format)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d61eb45eff8db119eb73209b53b595f1cf6d243
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105713046"
---
# <a name="resource-interchange-file-format-riff"></a><span data-ttu-id="e6764-104">Формат RIFF (Resource Interchange File Format)</span><span class="sxs-lookup"><span data-stu-id="e6764-104">Resource Interchange File Format (RIFF)</span></span>

<span data-ttu-id="e6764-105">В этом обзоре описывается формат файла обмена ресурсами (Metallica), который используется в WAV-файлах.</span><span class="sxs-lookup"><span data-stu-id="e6764-105">This overview describes the Resource Interchange File Format (RIFF), which is used in .wav files.</span></span> <span data-ttu-id="e6764-106">Metallica — типичный формат, из которого будут загружены звуковые данные для XAudio2.</span><span class="sxs-lookup"><span data-stu-id="e6764-106">RIFF is the typical format from which audio data for XAudio2 will be loaded.</span></span>

## <a name="riff"></a><span data-ttu-id="e6764-107">RIFF</span><span class="sxs-lookup"><span data-stu-id="e6764-107">RIFF</span></span>

<span data-ttu-id="e6764-108">Файл Metallica состоит из нескольких дискретных разделов данных, называемых *фрагментами*.</span><span class="sxs-lookup"><span data-stu-id="e6764-108">A RIFF file is composed of multiple discrete sections of data called *chunks*.</span></span>

## <a name="fourcc-identifiers"></a><span data-ttu-id="e6764-109">Идентификаторы FOURCC</span><span class="sxs-lookup"><span data-stu-id="e6764-109">FOURCC Identifiers</span></span>

<span data-ttu-id="e6764-110">Тип данных в блоке обозначается идентификатором с четырьмя символами (FOURCC).</span><span class="sxs-lookup"><span data-stu-id="e6764-110">The type of data in a chunk is indicated by a four-character code (FOURCC) identifier.</span></span> <span data-ttu-id="e6764-111">FOURCC — это 32-разрядное целое число без знака, созданное путем сцепления четырех символов ASCII, используемых для обнаружения типов блоков в файле Metallica.</span><span class="sxs-lookup"><span data-stu-id="e6764-111">A FOURCC is a 32-bit unsigned integer created by concatenating four ASCII characters used to identify chunk types in a RIFF file.</span></span> <span data-ttu-id="e6764-112">Например, FOURCC «ABCD» представлена в системе с прямым порядком байтов как 0x64636261.</span><span class="sxs-lookup"><span data-stu-id="e6764-112">For example, the FOURCC "abcd" is represented on a little-endian system as 0x64636261.</span></span> <span data-ttu-id="e6764-113">Фаурккс может содержать пробелы, поэтому "ABC" является допустимым набором FOURCC.</span><span class="sxs-lookup"><span data-stu-id="e6764-113">FOURCCs can contain space characters, so " abc" is a valid FOURCC.</span></span> <span data-ttu-id="e6764-114">В аудиофайлах используются коды FOURCC для обнаружения фрагментов звукового формата, блоков звуковых данных и других блоков, относящихся к звуковому формату.</span><span class="sxs-lookup"><span data-stu-id="e6764-114">Audio files use FOURCC codes to identify audio format chunks, audio data chunks, and any other chunks specific to the audio format.</span></span>

<span data-ttu-id="e6764-115">В следующей таблице показаны идентификаторы FOURCC, которые могут быть ожидаемыми в звуковых форматах, поддерживаемых XAudio2.</span><span class="sxs-lookup"><span data-stu-id="e6764-115">The following table shows the FOURCC identifiers that can be expected in the audio formats supported by XAudio2.</span></span> 

| <span data-ttu-id="e6764-116">Формат</span><span class="sxs-lookup"><span data-stu-id="e6764-116">Format</span></span> | <span data-ttu-id="e6764-117">Идентификаторы FOURCC</span><span class="sxs-lookup"><span data-stu-id="e6764-117">FOURCC identifiers</span></span>                     | <span data-ttu-id="e6764-118">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="e6764-118">Additional information</span></span>                                                                               |
|--------|----------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6764-119">PCM</span><span class="sxs-lookup"><span data-stu-id="e6764-119">PCM</span></span>    | <span data-ttu-id="e6764-120">"Metallica", "fmt", "Data"</span><span class="sxs-lookup"><span data-stu-id="e6764-120">"RIFF", "fmt" , "data"</span></span>                 |                                                                                                      |
| <span data-ttu-id="e6764-121">СЖАТИЯ</span><span class="sxs-lookup"><span data-stu-id="e6764-121">ADPCM</span></span>  | <span data-ttu-id="e6764-122">"Metallica", "fmt", "Data", "СМПЛ", "всмпл"</span><span class="sxs-lookup"><span data-stu-id="e6764-122">"RIFF", "fmt", "data", "smpl", "wsmpl"</span></span> | <span data-ttu-id="e6764-123">Описание идентификаторов FOURCC, связанных с ADPCM, см. в разделе [Общие сведения о ADPCM](adpcm-overview.md) .</span><span class="sxs-lookup"><span data-stu-id="e6764-123">See [ADPCM Overview](adpcm-overview.md) for a description of the ADPCM-specific FOURCC identifiers.</span></span> |



 

<span data-ttu-id="e6764-124">Идентификаторы FOURCC "Metallica", "fmt" и "Data" являются общими для всех поддерживаемых форматов.</span><span class="sxs-lookup"><span data-stu-id="e6764-124">The FOURCC identifiers "RIFF", "fmt", and "data" are common to all of the supported formats.</span></span> <span data-ttu-id="e6764-125">В следующей таблице описаны идентификаторы FOURCC, которые находятся во всех поддерживаемых форматах.</span><span class="sxs-lookup"><span data-stu-id="e6764-125">The following table describes the FOURCC identifiers that are found in all of the supported formats.</span></span> 

| <span data-ttu-id="e6764-126">Идентификатор FOURCC</span><span class="sxs-lookup"><span data-stu-id="e6764-126">FOURCC identifier</span></span> | <span data-ttu-id="e6764-127">Описание</span><span class="sxs-lookup"><span data-stu-id="e6764-127">Description</span></span>                                                                                                                                                                                                                        |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6764-128">"RIFF"</span><span class="sxs-lookup"><span data-stu-id="e6764-128">"RIFF"</span></span>            | <span data-ttu-id="e6764-129">Стандартный блок Metallica, содержащий тип файла со значением "WAVE" или "КСВМА" в первых четырех байтах раздела данных, а также другие фрагменты в файле в оставшейся части его раздела данных.</span><span class="sxs-lookup"><span data-stu-id="e6764-129">Standard RIFF chunk containing a file type with the value of "WAVE" or "XWMA" in the first four bytes of its data section and the other chunks in the file in the remainder of its data section.</span></span>                                   |
| <span data-ttu-id="e6764-130">"fmt"</span><span class="sxs-lookup"><span data-stu-id="e6764-130">"fmt"</span></span>             | <span data-ttu-id="e6764-131">Содержит заголовок формата для звукового файла.</span><span class="sxs-lookup"><span data-stu-id="e6764-131">Contains the format header for the audio file.</span></span> <span data-ttu-id="e6764-132">Данные в этом блоке соответствуют одной из следующих структур: **вавеформатекс**, **вавеформатекстенсибле адпкмвавеформат**.</span><span class="sxs-lookup"><span data-stu-id="e6764-132">The data in this chunk corresponds to one of the following structures: **WAVEFORMATEX**, **WAVEFORMATEXTENSIBLE ADPCMWAVEFORMAT**.</span></span>                                                  |
| <span data-ttu-id="e6764-133">"data"</span><span class="sxs-lookup"><span data-stu-id="e6764-133">"data"</span></span>            | <span data-ttu-id="e6764-134">Содержит звуковые данные для звукового файла.</span><span class="sxs-lookup"><span data-stu-id="e6764-134">Contains audio data for the audio file.</span></span> <span data-ttu-id="e6764-135">В XAudio2 содержимое фрагмента данных считывается в буфер и передается в исходный голоса в качестве элемента **паудиодата** в структуре [**\_ буфера XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) .</span><span class="sxs-lookup"><span data-stu-id="e6764-135">In XAudio2, the contents of the data chunk will be read into a buffer and passed to a source voice as the **pAudioData** member of an [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structure.</span></span> |



 

## <a name="chunks"></a><span data-ttu-id="e6764-136">Блоки</span><span class="sxs-lookup"><span data-stu-id="e6764-136">Chunks</span></span>

<span data-ttu-id="e6764-137">Файл Metallica состоит из фрагмента Metallica, содержащего ноль или более других фрагментов.</span><span class="sxs-lookup"><span data-stu-id="e6764-137">A RIFF file consists of a RIFF chunk containing zero or more other chunks.</span></span>

-   <span data-ttu-id="e6764-138">Блок Metallica имеет следующий вид:</span><span class="sxs-lookup"><span data-stu-id="e6764-138">The RIFF chunk has the following form:</span></span>

    <span data-ttu-id="e6764-139">"Metallica", размер файла, Тип_файла, Data</span><span class="sxs-lookup"><span data-stu-id="e6764-139">"RIFF", fileSize, fileType, data</span></span>

    <span data-ttu-id="e6764-140">Где "Metallica" — это литеральный код FOURCC "Metallica", *Размер файла* является 4-байтовым значением, определяющим размер данных в файле, а *filetype* — FourCC, которая определяет конкретный тип файла.</span><span class="sxs-lookup"><span data-stu-id="e6764-140">Where "RIFF" is the literal FOURCC code "RIFF", *fileSize* is a 4-byte value giving the size of the data in the file, and *fileType* is a FOURCC that identifies the specific file type.</span></span> <span data-ttu-id="e6764-141">Значение *Размер файла* включает размер *filetype* FourCC плюс размер данных, приведенных ниже, но не включает размер "Metallica" FourCC или размер *Размер файла*.</span><span class="sxs-lookup"><span data-stu-id="e6764-141">The value of *fileSize* includes the size of *fileType* FOURCC plus the size of the data that follows, but does not include the size of the "RIFF" FOURCC or the size of *fileSize*.</span></span> <span data-ttu-id="e6764-142">Данные состоят из фрагментов в любом порядке.</span><span class="sxs-lookup"><span data-stu-id="e6764-142">The data consists of chunks in any order.</span></span>

-   <span data-ttu-id="e6764-143">Другие фрагменты имеют следующую форму:</span><span class="sxs-lookup"><span data-stu-id="e6764-143">Other chunks have the following form:</span></span>

    ```
    chunkID, chunkSize, data
    ```

    

    <span data-ttu-id="e6764-144">Где *чункид* — это объект FourCC, определяющий данные, содержащиеся в блоке, *ChunkSize* — 4-байтовый размер, указывающий объем раздела данных в фрагменте, а данные — ноль или больше байтов данных.</span><span class="sxs-lookup"><span data-stu-id="e6764-144">Where *chunkID* is a FOURCC that identifies the data contained in the chunk, *chunkSize* is a 4-byte value giving the size of the data section of the chunk, and data is zero or more bytes of data.</span></span> <span data-ttu-id="e6764-145">Данные всегда дополняются до ближайшей границы слова.</span><span class="sxs-lookup"><span data-stu-id="e6764-145">The data is always padded to the nearest WORD boundary.</span></span> <span data-ttu-id="e6764-146">*ChunkSize* предоставляет размер допустимых данных в блоке.</span><span class="sxs-lookup"><span data-stu-id="e6764-146">*chunkSize* gives the size of the valid data in the chunk.</span></span> <span data-ttu-id="e6764-147">Он не включает в себя заполнение, размер *чункид* или размер *ChunkSize*.</span><span class="sxs-lookup"><span data-stu-id="e6764-147">It does not include the padding, the size of *chunkID*, or the size of *chunkSize*.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e6764-148">См. также</span><span class="sxs-lookup"><span data-stu-id="e6764-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6764-149">Начало работы</span><span class="sxs-lookup"><span data-stu-id="e6764-149">Getting Started</span></span>](getting-started.md)
</dt> <dt>

[<span data-ttu-id="e6764-150">Руководство: воспроизведение звука при помощи XAudio2</span><span class="sxs-lookup"><span data-stu-id="e6764-150">How to: Play a Sound with XAudio2</span></span>](how-to--play-a-sound-with-xaudio2.md)
</dt> <dt>

[<span data-ttu-id="e6764-151">Справочник по программированию в XAudio2</span><span class="sxs-lookup"><span data-stu-id="e6764-151">XAudio2 Programming Reference</span></span>](programming-reference.md)
</dt> </dl>

 

 




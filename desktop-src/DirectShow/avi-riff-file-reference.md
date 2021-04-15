---
description: Справочник по файлу AVI Metallica
ms.assetid: 2d8cf5be-1252-4b58-89b1-f5c53ea17d0e
title: Справочник по файлу AVI Metallica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83f28a7254ac9eb927381e313603ffd2bd0d050c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495663"
---
# <a name="avi-riff-file-reference"></a><span data-ttu-id="55ec1-103">Справочник по файлу AVI Metallica</span><span class="sxs-lookup"><span data-stu-id="55ec1-103">AVI RIFF File Reference</span></span>

<span data-ttu-id="55ec1-104">Формат AVI-файла Microsoft — это спецификация файлов Metallica, которая используется в приложениях, записывающих, редактирующих и воспроизводящих звуковые видеопоследовательности.</span><span class="sxs-lookup"><span data-stu-id="55ec1-104">The Microsoft AVI file format is a RIFF file specification used with applications that capture, edit, and play back audio-video sequences.</span></span> <span data-ttu-id="55ec1-105">Как правило, AVI-файлы содержат несколько потоков различных типов данных.</span><span class="sxs-lookup"><span data-stu-id="55ec1-105">In general, AVI files contain multiple streams of different types of data.</span></span> <span data-ttu-id="55ec1-106">Большинство последовательностей AVI используют потоки аудио и видео.</span><span class="sxs-lookup"><span data-stu-id="55ec1-106">Most AVI sequences use both audio and video streams.</span></span> <span data-ttu-id="55ec1-107">Простой вариант для последовательности AVI использует видеоданные и не требует наличия звукового потока.</span><span class="sxs-lookup"><span data-stu-id="55ec1-107">A simple variation for an AVI sequence uses video data and does not require an audio stream.</span></span>

<span data-ttu-id="55ec1-108">В этом разделе не описываются расширения формата AVI для файлов Опендмл.</span><span class="sxs-lookup"><span data-stu-id="55ec1-108">This section does not describe the OpenDML AVI file format extensions.</span></span> <span data-ttu-id="55ec1-109">Дополнительные сведения об этих расширениях см. в разделе *расширения формата AVI-файлов опендмл*, опубликованные в Подкомитете формат файла Опендмл AVI M – JPEG.</span><span class="sxs-lookup"><span data-stu-id="55ec1-109">For further information on these extensions, see *OpenDML AVI File Format Extensions*, published by the OpenDML AVI M-JPEG File Format Subcommittee.</span></span>

## <a name="fourccs"></a><span data-ttu-id="55ec1-110">фаурккс</span><span class="sxs-lookup"><span data-stu-id="55ec1-110">FOURCCs</span></span>

<span data-ttu-id="55ec1-111">FOURCC (код из четырех символов) — это 32-разрядное целое число без знака, созданное путем сцепления четырех символов ASCII.</span><span class="sxs-lookup"><span data-stu-id="55ec1-111">A FOURCC (four-character code) is a 32-bit unsigned integer created by concatenating four ASCII characters.</span></span> <span data-ttu-id="55ec1-112">Например, FOURCC ' ABCD ' представлена в Little-Endian системе как 0x64636261.</span><span class="sxs-lookup"><span data-stu-id="55ec1-112">For example, the FOURCC 'abcd' is represented on a Little-Endian system as 0x64636261.</span></span> <span data-ttu-id="55ec1-113">Фаурккс может содержать пробелы, поэтому "ABC" является допустимым набором FOURCC.</span><span class="sxs-lookup"><span data-stu-id="55ec1-113">FOURCCs can contain space characters, so ' abc' is a valid FOURCC.</span></span> <span data-ttu-id="55ec1-114">Формат AVI использует коды FOURCC для обнаружения типов потоков, фрагментов данных, записей индекса и других сведений.</span><span class="sxs-lookup"><span data-stu-id="55ec1-114">The AVI file format uses FOURCC codes to identify stream types, data chunks, index entries, and other information.</span></span>

## <a name="riff-file-format"></a><span data-ttu-id="55ec1-115">Формат файла Metallica</span><span class="sxs-lookup"><span data-stu-id="55ec1-115">RIFF File Format</span></span>

<span data-ttu-id="55ec1-116">Формат AVI-файла основан на формате документа Metallica (формат файла обмена ресурсами).</span><span class="sxs-lookup"><span data-stu-id="55ec1-116">The AVI file format is based on the RIFF (resource interchange file format) document format.</span></span> <span data-ttu-id="55ec1-117">Файл Metallica состоит из заголовка Metallica, за которым следует ноль или более *списков* и *блоков*.</span><span class="sxs-lookup"><span data-stu-id="55ec1-117">A RIFF file consists of a RIFF header followed by zero or more *lists* and *chunks*.</span></span>

-   <span data-ttu-id="55ec1-118">Заголовок Metallica имеет следующую форму:</span><span class="sxs-lookup"><span data-stu-id="55ec1-118">The RIFF header has the following form:</span></span>

    `'RIFF' fileSize fileType (data)`

    <span data-ttu-id="55ec1-119">где "Metallica" является литеральным кодом FOURCC "Metallica", `fileSize` является 4-байтовым значением, определяющим размер данных в файле, и является типом `fileType` FourCC, идентифицирующим конкретный тип файла.</span><span class="sxs-lookup"><span data-stu-id="55ec1-119">where 'RIFF' is the literal FOURCC code 'RIFF', `fileSize` is a 4-byte value giving the size of the data in the file, and `fileType` is a FOURCC that identifies the specific file type.</span></span> <span data-ttu-id="55ec1-120">Значение `fileSize` включает размер объекта `fileType` FourCC плюс размер данных, приведенных ниже, но не включает размер "Metallica" FourCC или размер `fileSize` .</span><span class="sxs-lookup"><span data-stu-id="55ec1-120">The value of `fileSize` includes the size of the `fileType` FOURCC plus the size of the data that follows, but does not include the size of the 'RIFF' FOURCC or the size of `fileSize`.</span></span> <span data-ttu-id="55ec1-121">Файловые данные состоят из фрагментов и списков в любом порядке.</span><span class="sxs-lookup"><span data-stu-id="55ec1-121">The file data consists of chunks and lists, in any order.</span></span>

-   <span data-ttu-id="55ec1-122">Фрагмент имеет следующий вид:</span><span class="sxs-lookup"><span data-stu-id="55ec1-122">A chunk has the following form:</span></span>

    `ckID ckSize ckData`

    <span data-ttu-id="55ec1-123">где `ckID` — это FourCC, идентифицирующая данные, содержащиеся в блоке, `ckSize` — это 4-байтовый параметр, определяющий размер данных в `ckData` , а `ckData` также ноль или более байтов данных.</span><span class="sxs-lookup"><span data-stu-id="55ec1-123">where `ckID` is a FOURCC that identifies the data contained in the chunk, `ckSize` is a 4-byte value giving the size of the data in `ckData`, and `ckData` is zero or more bytes of data.</span></span> <span data-ttu-id="55ec1-124">Данные всегда дополняются до ближайшей границы **слова** .</span><span class="sxs-lookup"><span data-stu-id="55ec1-124">The data is always padded to nearest **WORD** boundary.</span></span> <span data-ttu-id="55ec1-125">`ckSize` Предоставляет размер допустимых данных в блоке; Он не включает в себя заполнение, размер `ckID` или размер `ckSize` .</span><span class="sxs-lookup"><span data-stu-id="55ec1-125">`ckSize` gives the size of the valid data in the chunk; it does not include the padding, the size of `ckID`, or the size of `ckSize`.</span></span>

-   <span data-ttu-id="55ec1-126">Список имеет следующий вид:</span><span class="sxs-lookup"><span data-stu-id="55ec1-126">A list has the following form:</span></span>

    `'LIST' listSize listType listData`

    <span data-ttu-id="55ec1-127">где "LIST" является строковым кодом FOURCC "LIST", `listSize` является 4-байтовым значением, определяющим размер списка, `listType` является кодом FourCC и `listData` состоит из фрагментов или списков в любом порядке.</span><span class="sxs-lookup"><span data-stu-id="55ec1-127">where 'LIST' is the literal FOURCC code 'LIST', `listSize` is a 4-byte value giving the size of the list, `listType` is a FOURCC code, and `listData` consists of chunks or lists, in any order.</span></span> <span data-ttu-id="55ec1-128">Значение параметра `listSize` включает размер `listType` плюс размер `listData` ; он не включает в себя "List" FourCC или размер `listSize` .</span><span class="sxs-lookup"><span data-stu-id="55ec1-128">The value of `listSize` includes the size of `listType` plus the size of `listData`; it does not include the 'LIST' FOURCC or the size of `listSize`.</span></span>

<span data-ttu-id="55ec1-129">Оставшаяся часть этого раздела использует следующую нотацию для описания фрагментов Metallica:</span><span class="sxs-lookup"><span data-stu-id="55ec1-129">The remainder of this section uses the following notation to describe RIFF chunks:</span></span>

`ckID ( ckData )`

<span data-ttu-id="55ec1-130">где размер фрагмента данных является неявным.</span><span class="sxs-lookup"><span data-stu-id="55ec1-130">where the chunk size is implicit.</span></span> <span data-ttu-id="55ec1-131">С помощью этой нотации список можно представить следующим образом:</span><span class="sxs-lookup"><span data-stu-id="55ec1-131">Using this notation, a list can be represented as:</span></span>

`'LIST' ( listType ( listData ) )`

<span data-ttu-id="55ec1-132">Необязательные элементы помещаются в квадратные скобки: `[ optional element ]`</span><span class="sxs-lookup"><span data-stu-id="55ec1-132">Optional elements are placed in brackets: `[ optional element ]`</span></span>

## <a name="avi-riff-form"></a><span data-ttu-id="55ec1-133">Форма AVI Metallica</span><span class="sxs-lookup"><span data-stu-id="55ec1-133">AVI RIFF Form</span></span>

<span data-ttu-id="55ec1-134">Файлы AVI идентифицируются с помощью FOURCC "AVI" в заголовке Metallica.</span><span class="sxs-lookup"><span data-stu-id="55ec1-134">AVI files are identified by the FOURCC 'AVI ' in the RIFF header.</span></span> <span data-ttu-id="55ec1-135">Все файлы AVI содержат два фрагмента обязательных СПИСКОВ, которые определяют формат потоков и потоковых данных соответственно.</span><span class="sxs-lookup"><span data-stu-id="55ec1-135">All AVI files include two mandatory LIST chunks, which define the format of the streams and the stream data, respectively.</span></span> <span data-ttu-id="55ec1-136">Файл AVI также может содержать фрагмент индекса, который задает расположение фрагментов данных в файле.</span><span class="sxs-lookup"><span data-stu-id="55ec1-136">An AVI file might also include an index chunk, which gives the location of the data chunks within the file.</span></span> <span data-ttu-id="55ec1-137">Файл AVI со следующими компонентами имеет следующий вид:</span><span class="sxs-lookup"><span data-stu-id="55ec1-137">An AVI file with these components has the following form:</span></span>


```C++
RIFF ('AVI '
      LIST ('hdrl' ... )
      LIST ('movi' ... )
      ['idx1' (<AVI Index>) ]
     )
```



<span data-ttu-id="55ec1-138">Список "хдрл" определяет формат данных и является первым обязательным блоком списка.</span><span class="sxs-lookup"><span data-stu-id="55ec1-138">The 'hdrl' list defines the format of the data and is the first required LIST chunk.</span></span> <span data-ttu-id="55ec1-139">Список "Мови" содержит данные для последовательности AVI и второй обязательный блок списка.</span><span class="sxs-lookup"><span data-stu-id="55ec1-139">The 'movi' list contains the data for the AVI sequence and is the second required LIST chunk.</span></span> <span data-ttu-id="55ec1-140">Список "idx1" содержит индекс.</span><span class="sxs-lookup"><span data-stu-id="55ec1-140">The 'idx1' list contains the index.</span></span> <span data-ttu-id="55ec1-141">Файлы AVI должны иметь соответствующие три компонента в правильной последовательности.</span><span class="sxs-lookup"><span data-stu-id="55ec1-141">AVI files must keep these three components in the proper sequence.</span></span>

> [!Note]  
> <span data-ttu-id="55ec1-142">Расширения Опендмл определяют другой тип индекса, идентифицируемый FOURCC "индкс".</span><span class="sxs-lookup"><span data-stu-id="55ec1-142">The OpenDML extensions define another type of index, identified by the FOURCC 'indx'.</span></span>

 

<span data-ttu-id="55ec1-143">Списки "хдрл" и "Мови" используют для своих данных подблоки.</span><span class="sxs-lookup"><span data-stu-id="55ec1-143">The 'hdrl' and 'movi' lists use subchunks for their data.</span></span> <span data-ttu-id="55ec1-144">В следующем примере показана форма AVI Metallica, развернутая с блоками, необходимыми для выполнения этих списков:</span><span class="sxs-lookup"><span data-stu-id="55ec1-144">The following example shows the AVI RIFF form expanded with the chunks needed to complete these lists:</span></span>


```C++
RIFF ('AVI '
      LIST ('hdrl'
            'avih'(<Main AVI Header>)
            LIST ('strl'
                  'strh'(<Stream header>)
                  'strf'(<Stream format>)
                  [ 'strd'(<Additional header data>) ]
                  [ 'strn'(<Stream name>) ]
                  ...
                 )
             ...
           )
      LIST ('movi'
            {SubChunk | LIST ('rec '
                              SubChunk1
                              SubChunk2
                              ...
                             )
               ...
            }
            ...
           )
      ['idx1' (<AVI Index>) ]
     )
```



## <a name="avi-main-header"></a><span data-ttu-id="55ec1-145">Основной заголовок AVI</span><span class="sxs-lookup"><span data-stu-id="55ec1-145">AVI Main Header</span></span>

<span data-ttu-id="55ec1-146">Список "хдрл" начинается с основного заголовка AVI, который содержится в блоке "авих".</span><span class="sxs-lookup"><span data-stu-id="55ec1-146">The 'hdrl' list begins with the main AVI header, which is contained in an 'avih' chunk.</span></span> <span data-ttu-id="55ec1-147">Основной заголовок содержит глобальные сведения для всего файла AVI, например число потоков в файле, а также ширину и высоту последовательности AVI.</span><span class="sxs-lookup"><span data-stu-id="55ec1-147">The main header contains global information for the entire AVI file, such as the number of streams within the file and the width and height of the AVI sequence.</span></span> <span data-ttu-id="55ec1-148">Основной фрагмент заголовка состоит из структуры [**авимаинхеадер**](/previous-versions/windows/desktop/api/Aviriff/ns-aviriff-avimainheader) .</span><span class="sxs-lookup"><span data-stu-id="55ec1-148">The main header chunk consists of an [**AVIMAINHEADER**](/previous-versions/windows/desktop/api/Aviriff/ns-aviriff-avimainheader) structure.</span></span>

## <a name="avi-stream-headers"></a><span data-ttu-id="55ec1-149">Заголовки потока AVI</span><span class="sxs-lookup"><span data-stu-id="55ec1-149">AVI Stream Headers</span></span>

<span data-ttu-id="55ec1-150">Один или несколько списков "СТРЛ" следуют за главным заголовком.</span><span class="sxs-lookup"><span data-stu-id="55ec1-150">One or more 'strl' lists follow the main header.</span></span> <span data-ttu-id="55ec1-151">Для каждого потока данных требуется список "СТРЛ".</span><span class="sxs-lookup"><span data-stu-id="55ec1-151">A 'strl' list is required for each data stream.</span></span> <span data-ttu-id="55ec1-152">Каждый список "СТРЛ" содержит сведения о одном потоке в файле и должен содержать фрагмент заголовка потока ("стрх") и фрагмент формата потока ("стрф").</span><span class="sxs-lookup"><span data-stu-id="55ec1-152">Each 'strl' list contains information about one stream in the file, and must contain a stream header chunk ('strh') and a stream format chunk ('strf').</span></span> <span data-ttu-id="55ec1-153">Кроме того, список "СТРЛ" может содержать фрагмент данных заголовка потока ("стрд") и фрагмент имени потока ("стрн").</span><span class="sxs-lookup"><span data-stu-id="55ec1-153">In addition, a 'strl' list might contain a stream-header data chunk ('strd') and a stream name chunk ('strn').</span></span>

<span data-ttu-id="55ec1-154">Блок заголовка потока ("стрх") состоит из структуры [**авистреамхеадер**](/previous-versions/windows/desktop/api/avifmt/ns-avifmt-avistreamheader) .</span><span class="sxs-lookup"><span data-stu-id="55ec1-154">The stream header chunk ('strh') consists of an [**AVISTREAMHEADER**](/previous-versions/windows/desktop/api/avifmt/ns-avifmt-avistreamheader) structure.</span></span>

<span data-ttu-id="55ec1-155">Блок формата потока ("стрф") должен следовать за фрагментом заголовка потока.</span><span class="sxs-lookup"><span data-stu-id="55ec1-155">A stream format chunk ('strf') must follow the stream header chunk.</span></span> <span data-ttu-id="55ec1-156">Блок формата потока описывает формат данных в потоке.</span><span class="sxs-lookup"><span data-stu-id="55ec1-156">The stream format chunk describes the format of the data in the stream.</span></span> <span data-ttu-id="55ec1-157">Данные, содержащиеся в этом фрагменте, зависят от типа потока.</span><span class="sxs-lookup"><span data-stu-id="55ec1-157">The data contained in this chunk depends on the stream type.</span></span> <span data-ttu-id="55ec1-158">Для видеопотоков информация является структурой [**битмапинфо**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) , включая сведения о палитре, если это уместно.</span><span class="sxs-lookup"><span data-stu-id="55ec1-158">For video streams, the information is a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure, including palette information if appropriate.</span></span> <span data-ttu-id="55ec1-159">Для звуковых потоков эта информация является структурой [**вавеформатекс**](/previous-versions/dd757713(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="55ec1-159">For audio streams, the information is a [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span>

<span data-ttu-id="55ec1-160">Если имеется фрагмент данных заголовка потока ("стрд"), он следует за блоком формата потока.</span><span class="sxs-lookup"><span data-stu-id="55ec1-160">If the stream-header data ('strd') chunk is present, it follows the stream format chunk.</span></span> <span data-ttu-id="55ec1-161">Формат и содержимое этого фрагмента определяется драйвером кодека.</span><span class="sxs-lookup"><span data-stu-id="55ec1-161">The format and content of this chunk are defined by the codec driver.</span></span> <span data-ttu-id="55ec1-162">Как правило, драйверы используют эти сведения для настройки.</span><span class="sxs-lookup"><span data-stu-id="55ec1-162">Typically, drivers use this information for configuration.</span></span> <span data-ttu-id="55ec1-163">Приложениям, считывающим и записывающим файлы AVI, не нужно интерпретировать эти сведения. они просто переносят их в драйвер и из него в виде блока памяти.</span><span class="sxs-lookup"><span data-stu-id="55ec1-163">Applications that read and write AVI files do not need to interpret this information; they simple transfer it to and from the driver as a memory block.</span></span>

<span data-ttu-id="55ec1-164">Необязательный блок "стрн" содержит текстовую строку, завершающуюся нулем, описывающую поток.</span><span class="sxs-lookup"><span data-stu-id="55ec1-164">The optional 'strn' chunk contains a null-terminated text string describing the stream.</span></span>

<span data-ttu-id="55ec1-165">Заголовки потока в списке "хдрл" связаны с потоковых данных в списке "Мови" в соответствии с порядком фрагментов "СТРЛ".</span><span class="sxs-lookup"><span data-stu-id="55ec1-165">The stream headers in the 'hdrl' list are associated with the stream data in the 'movi' list according to the order of the 'strl' chunks.</span></span> <span data-ttu-id="55ec1-166">Первый блок "СТРЛ" применяется к потоку 0, второй — к потоку 1 и т. д.</span><span class="sxs-lookup"><span data-stu-id="55ec1-166">The first 'strl' chunk applies to stream 0, the second applies to stream 1, and so forth.</span></span>

## <a name="stream-data-movi-list"></a><span data-ttu-id="55ec1-167">Потоковые данные (список "Мови")</span><span class="sxs-lookup"><span data-stu-id="55ec1-167">Stream Data ('movi' List)</span></span>

<span data-ttu-id="55ec1-168">После сведений о заголовке находится список "Мови", содержащий фактические данные в потоках, то есть видеоматериалы и образцы аудио.</span><span class="sxs-lookup"><span data-stu-id="55ec1-168">Following the header information is a 'movi' list that contains the actual data in the streams—that is, the video frames and audio samples.</span></span> <span data-ttu-id="55ec1-169">Фрагменты данных могут находиться непосредственно в списке "Мови" или быть сгруппированы в списках "REC".</span><span class="sxs-lookup"><span data-stu-id="55ec1-169">The data chunks can reside directly in the 'movi' list, or they might be grouped within 'rec ' lists.</span></span> <span data-ttu-id="55ec1-170">Группирование "REC" подразумевает, что сгруппированные фрагменты должны считываться с диска все сразу и предназначены для файлов, которые чередуются для воспроизведения с компакт-диска.</span><span class="sxs-lookup"><span data-stu-id="55ec1-170">The 'rec ' grouping implies that the grouped chunks should be read from disk all at once, and is intended for files that are interleaved to play from CD-ROM.</span></span>

<span data-ttu-id="55ec1-171">Объект FOURCC, определяющий каждый блок данных, состоит из двузначного номера потока, за которым следует код из двух символов, определяющий тип данных в фрагменте.</span><span class="sxs-lookup"><span data-stu-id="55ec1-171">The FOURCC that identifies each data chunk consists of a two-digit stream number followed by a two-character code that defines the type of information in the chunk.</span></span>



| <span data-ttu-id="55ec1-172">Код из двух символов</span><span class="sxs-lookup"><span data-stu-id="55ec1-172">Two-character code</span></span> | <span data-ttu-id="55ec1-173">Описание</span><span class="sxs-lookup"><span data-stu-id="55ec1-173">Description</span></span>              |
|--------------------|--------------------------|
| <span data-ttu-id="55ec1-174">db</span><span class="sxs-lookup"><span data-stu-id="55ec1-174">db</span></span>                 | <span data-ttu-id="55ec1-175">Несжатый кадр видео</span><span class="sxs-lookup"><span data-stu-id="55ec1-175">Uncompressed video frame</span></span> |
| <span data-ttu-id="55ec1-176">dc</span><span class="sxs-lookup"><span data-stu-id="55ec1-176">dc</span></span>                 | <span data-ttu-id="55ec1-177">Сжатый кадр видео</span><span class="sxs-lookup"><span data-stu-id="55ec1-177">Compressed video frame</span></span>   |
| <span data-ttu-id="55ec1-178">пк</span><span class="sxs-lookup"><span data-stu-id="55ec1-178">pc</span></span>                 | <span data-ttu-id="55ec1-179">Изменение палитры</span><span class="sxs-lookup"><span data-stu-id="55ec1-179">Palette change</span></span>           |
| <span data-ttu-id="55ec1-180">WB</span><span class="sxs-lookup"><span data-stu-id="55ec1-180">wb</span></span>                 | <span data-ttu-id="55ec1-181">Звуковые данные</span><span class="sxs-lookup"><span data-stu-id="55ec1-181">Audio data</span></span>               |



 

<span data-ttu-id="55ec1-182">Например, если поток 0 содержит звук, фрагменты данных для этого потока будут иметь FOURCC ' 00wb '.</span><span class="sxs-lookup"><span data-stu-id="55ec1-182">For example, if stream 0 contains audio, the data chunks for that stream would have the FOURCC '00wb'.</span></span> <span data-ttu-id="55ec1-183">Если поток 1 содержит видео, фрагменты данных для этого потока будут иметь FOURCC ' 01db ' или ' 01dc '.</span><span class="sxs-lookup"><span data-stu-id="55ec1-183">If stream 1 contains video, the data chunks for that stream would have the FOURCC '01db' or '01dc'.</span></span> <span data-ttu-id="55ec1-184">Фрагменты данных видео также могут определять новые записи палитры для обновления палитры во время последовательности AVI.</span><span class="sxs-lookup"><span data-stu-id="55ec1-184">Video data chunks can also define new palette entries to update the palette during an AVI sequence.</span></span> <span data-ttu-id="55ec1-185">Каждый блок изменения палитры ("кскспк") содержит структуру [**авипалчанже**](/previous-versions/windows/desktop/api/avifmt/ns-avifmt-avipalchange) .</span><span class="sxs-lookup"><span data-stu-id="55ec1-185">Each palette-change chunk ('xxpc') contains an [**AVIPALCHANGE**](/previous-versions/windows/desktop/api/avifmt/ns-avifmt-avipalchange) structure.</span></span> <span data-ttu-id="55ec1-186">Если поток содержит изменения палитры, установите флаг **ависф \_ Video \_ Палчанжес** в элемент **dwFlags** структуры [**авистреамхеадер**](/previous-versions/windows/desktop/api/avifmt/ns-avifmt-avistreamheader) для этого потока.</span><span class="sxs-lookup"><span data-stu-id="55ec1-186">If a stream contains palette changes, set the **AVISF\_VIDEO\_PALCHANGES** flag in the **dwFlags** member of the [**AVISTREAMHEADER**](/previous-versions/windows/desktop/api/avifmt/ns-avifmt-avistreamheader) structure for that stream.</span></span>

<span data-ttu-id="55ec1-187">Текстовые потоки могут использовать произвольные коды из двух символов.</span><span class="sxs-lookup"><span data-stu-id="55ec1-187">Text streams can use arbitrary two-character codes.</span></span>

## <a name="avi-index-entries"></a><span data-ttu-id="55ec1-188">Записи индекса AVI</span><span class="sxs-lookup"><span data-stu-id="55ec1-188">AVI Index Entries</span></span>

<dl> <dt>

<span data-ttu-id="55ec1-189"><span id="AVI_1.0_index"></span><span id="avi_1.0_index"></span><span id="AVI_1.0_INDEX"></span>Индекс AVI 1,0</span><span class="sxs-lookup"><span data-stu-id="55ec1-189"><span id="AVI_1.0_index"></span><span id="avi_1.0_index"></span><span id="AVI_1.0_INDEX"></span>AVI 1.0 index</span></span>
</dt> <dd>

<span data-ttu-id="55ec1-190">Необязательный фрагмент индекса ("idx1") может следовать за списком "Мови".</span><span class="sxs-lookup"><span data-stu-id="55ec1-190">An optional index ('idx1') chunk can follow the 'movi' list.</span></span> <span data-ttu-id="55ec1-191">Индекс содержит список фрагментов данных и их расположение в файле.</span><span class="sxs-lookup"><span data-stu-id="55ec1-191">The index contains a list of the data chunks and their location in the file.</span></span> <span data-ttu-id="55ec1-192">Он состоит из структуры [**авиолдиндекс**](/previous-versions/windows/desktop/api/Aviriff/ns-aviriff-avioldindex) с записями для каждого фрагмента данных, включая фрагменты «REC».</span><span class="sxs-lookup"><span data-stu-id="55ec1-192">It consists of an [**AVIOLDINDEX**](/previous-versions/windows/desktop/api/Aviriff/ns-aviriff-avioldindex) structure with entries for each data chunk, including 'rec ' chunks.</span></span> <span data-ttu-id="55ec1-193">Если файл содержит индекс, установите флаг **Авиф \_ хасиндекс** в элементе **dwFlags** структуры [**авимаинхеадер**](/previous-versions/windows/desktop/api/Aviriff/ns-aviriff-avimainheader) .</span><span class="sxs-lookup"><span data-stu-id="55ec1-193">If the file contains an index, set the **AVIF\_HASINDEX** flag in the **dwFlags** member of the [**AVIMAINHEADER**](/previous-versions/windows/desktop/api/Aviriff/ns-aviriff-avimainheader) structure.</span></span>

</dd> <dt>

<span data-ttu-id="55ec1-194"><span id="AVI_2.0_index"></span><span id="avi_2.0_index"></span><span id="AVI_2.0_INDEX"></span>Индекс AVI 2,0</span><span class="sxs-lookup"><span data-stu-id="55ec1-194"><span id="AVI_2.0_index"></span><span id="avi_2.0_index"></span><span id="AVI_2.0_INDEX"></span>AVI 2.0 index</span></span>
</dt> <dd>

<span data-ttu-id="55ec1-195">Индекс AVI 2,0 может отображаться как один блок.</span><span class="sxs-lookup"><span data-stu-id="55ec1-195">An AVI 2.0 index can appear as a single chunk.</span></span> <span data-ttu-id="55ec1-196">Кроме того, сегменты индекса могут быть чередованием в блоке "Мови".</span><span class="sxs-lookup"><span data-stu-id="55ec1-196">Alternatively, index segments can be interleaved within the 'movi' chunk.</span></span> <span data-ttu-id="55ec1-197">Если сегменты индекса размещаются в блоке "Мови", супер-индекс содержит индекс сегментов индекса.</span><span class="sxs-lookup"><span data-stu-id="55ec1-197">If the index segments are placed in the 'movi' chunk, a super index contains an index of the index segments.</span></span> <span data-ttu-id="55ec1-198">Структура [**авиметаиндекс**](/previous-versions/windows/desktop/api/aviriff/ns-aviriff-avimetaindex) является базовой структурой для сегментов индекса и Super index.</span><span class="sxs-lookup"><span data-stu-id="55ec1-198">The [**AVIMETAINDEX**](/previous-versions/windows/desktop/api/aviriff/ns-aviriff-avimetaindex) structure is the base structure for both the index segments and the super index.</span></span> <span data-ttu-id="55ec1-199">Дополнительные сведения см. в разделе *расширения формата AVI-файлов опендмл*, опубликованного в Подкомитете формат файла Опендмл AVI M – JPEG.</span><span class="sxs-lookup"><span data-stu-id="55ec1-199">For more information, see the *OpenDML AVI File Format Extensions*, published by the OpenDML AVI M-JPEG File Format Subcommittee.</span></span> <span data-ttu-id="55ec1-200">(Этот ресурс может быть недоступен в некоторых языках и странах.)</span><span class="sxs-lookup"><span data-stu-id="55ec1-200">(This resource may not be available in some languages and countries.)</span></span>

</dd> </dl>

## <a name="other-data-chunks"></a><span data-ttu-id="55ec1-201">Другие фрагменты данных</span><span class="sxs-lookup"><span data-stu-id="55ec1-201">Other Data Chunks</span></span>

<span data-ttu-id="55ec1-202">Данные могут быть согласованы в файле AVI путем вставки нежелательных блоков по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="55ec1-202">Data can be aligned in an AVI file by inserting 'JUNK' chunks as needed.</span></span> <span data-ttu-id="55ec1-203">Приложения должны игнорировать содержимое нежелательного фрагмента.</span><span class="sxs-lookup"><span data-stu-id="55ec1-203">Applications should ignore the contents of a 'JUNK' chunk.</span></span>

## <a name="related-topics"></a><span data-ttu-id="55ec1-204">См. также</span><span class="sxs-lookup"><span data-stu-id="55ec1-204">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55ec1-205">Формат файла AVI</span><span class="sxs-lookup"><span data-stu-id="55ec1-205">AVI File Format</span></span>](avi-file-format.md)
</dt> </dl>

 

 

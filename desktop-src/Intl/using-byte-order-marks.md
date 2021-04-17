---
description: Всегда добавляйте префикс к текстовому файлу Юникода с меткой порядка байтов, которая информирует приложение о получении файла о том, что файл является упорядоченным по байтам.
ms.assetid: d9f1ef5c-6367-4183-9c07-01c73cb4debc
title: Использование меток порядка байтов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b72d2ec366020f4c82c418e654e1c7fa0b4c8c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651202"
---
# <a name="using-byte-order-marks"></a><span data-ttu-id="418dd-103">Использование меток порядка байтов</span><span class="sxs-lookup"><span data-stu-id="418dd-103">Using Byte Order Marks</span></span>

<span data-ttu-id="418dd-104">Всегда добавляйте префикс к текстовому файлу Юникода с меткой порядка байтов, которая информирует приложение о получении файла о том, что файл является упорядоченным по байтам.</span><span class="sxs-lookup"><span data-stu-id="418dd-104">Always prefix a Unicode plain text file with a byte order mark, which informs an application receiving the file that the file is byte-ordered.</span></span> <span data-ttu-id="418dd-105">Доступные метки порядка байтов перечислены в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="418dd-105">Available byte order marks are listed in the following table.</span></span> <span data-ttu-id="418dd-106">Поскольку обычный текст в Юникоде представляет собой последовательность из 16-разрядных значений кода, он учитывает порядок байтов, используемый при написании текста.</span><span class="sxs-lookup"><span data-stu-id="418dd-106">Because Unicode plain text is a sequence of 16-bit code values, it is sensitive to the byte ordering used when the text is written.</span></span>

> [!Note]  
> <span data-ttu-id="418dd-107">Метка порядка байтов не является управляющим символом, который выбирает порядок байтов текста.</span><span class="sxs-lookup"><span data-stu-id="418dd-107">A byte order mark is not a control character that selects the byte order of the text.</span></span>

 



| <span data-ttu-id="418dd-108">Метка порядка байтов</span><span class="sxs-lookup"><span data-stu-id="418dd-108">Byte order mark</span></span> | <span data-ttu-id="418dd-109">Описание</span><span class="sxs-lookup"><span data-stu-id="418dd-109">Description</span></span>           |
|-----------------|-----------------------|
| <span data-ttu-id="418dd-110">EF BB BF</span><span class="sxs-lookup"><span data-stu-id="418dd-110">EF BB BF</span></span>        | <span data-ttu-id="418dd-111">UTF-8</span><span class="sxs-lookup"><span data-stu-id="418dd-111">UTF-8</span></span>                 |
| <span data-ttu-id="418dd-112">FF FE</span><span class="sxs-lookup"><span data-stu-id="418dd-112">FF FE</span></span>           | <span data-ttu-id="418dd-113">UTF-16, с прямым порядком байтов</span><span class="sxs-lookup"><span data-stu-id="418dd-113">UTF-16, little endian</span></span> |
| <span data-ttu-id="418dd-114">FE FF</span><span class="sxs-lookup"><span data-stu-id="418dd-114">FE FF</span></span>           | <span data-ttu-id="418dd-115">UTF-16, обратный порядок байтов</span><span class="sxs-lookup"><span data-stu-id="418dd-115">UTF-16, big endian</span></span>    |
| <span data-ttu-id="418dd-116">FF FE 00 00</span><span class="sxs-lookup"><span data-stu-id="418dd-116">FF FE 00 00</span></span>     | <span data-ttu-id="418dd-117">UTF-32, с прямым порядком байтов</span><span class="sxs-lookup"><span data-stu-id="418dd-117">UTF-32, little endian</span></span> |
| <span data-ttu-id="418dd-118">00 00 FE FF</span><span class="sxs-lookup"><span data-stu-id="418dd-118">00 00 FE FF</span></span>     | <span data-ttu-id="418dd-119">UTF-32, с обратным порядком байтов</span><span class="sxs-lookup"><span data-stu-id="418dd-119">UTF-32, big-endian</span></span>    |



 

> [!Note]  
> <span data-ttu-id="418dd-120">Корпорация Майкрософт использует UTF-16 с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="418dd-120">Microsoft uses UTF-16, little endian byte order.</span></span>

 

<span data-ttu-id="418dd-121">В идеале весь текст в Юникоде следует только одному набору правил порядка следования байтов.</span><span class="sxs-lookup"><span data-stu-id="418dd-121">Ideally, all Unicode text follows only one set of byte ordering rules.</span></span> <span data-ttu-id="418dd-122">Однако это невозможно, поскольку микропроцессоры отличаются размещением наименее значимого байта.</span><span class="sxs-lookup"><span data-stu-id="418dd-122">This is not possible, however, because microprocessors differ in the placement of the least significant byte.</span></span> <span data-ttu-id="418dd-123">Процессоры Intel и MIPS сначала размещаются на наименее значащий байт, тогда как процессоры Motorola (и все файлы в формате Юникод с обратным байтом) располагают его последними.</span><span class="sxs-lookup"><span data-stu-id="418dd-123">Intel and MIPS processors position the least significant byte first, whereas Motorola processors (and all byte-reversed Unicode files) position it last.</span></span> <span data-ttu-id="418dd-124">При использовании только одного набора правил порядка байтов пользователи одного типа микропроцессора вынуждены менять порядок байтов каждый раз, когда текстовый файл считывается или записывается, даже если файл никогда не передается в другую операционную систему на основе другого микропроцессора.</span><span class="sxs-lookup"><span data-stu-id="418dd-124">With only a single set of byte ordering rules, users of one type of microprocessor are forced to swap the byte order every time a plain text file is read from or written to, even if the file is never transferred to another operating system based on a different microprocessor.</span></span>

<span data-ttu-id="418dd-125">Предпочтительное место для указания порядка байтов находится в заголовке файла, но текстовые файлы не имеют заголовков.</span><span class="sxs-lookup"><span data-stu-id="418dd-125">The preferred place to specify byte order is in a file header, but text files do not have headers.</span></span> <span data-ttu-id="418dd-126">Поэтому в Юникоде определен символ (U + FEFF) и несимвольный (U + ФФФЕ) в качестве меток порядка байтов.</span><span class="sxs-lookup"><span data-stu-id="418dd-126">Therefore, Unicode has defined a character (U+FEFF) and a noncharacter (U+FFFE) as byte order marks.</span></span> <span data-ttu-id="418dd-127">Они представляют собой зеркально отображаемые байтовые изображения.</span><span class="sxs-lookup"><span data-stu-id="418dd-127">They are mirror byte images of each other.</span></span>

<span data-ttu-id="418dd-128">Поскольку последовательность U + FEFF превышена в начале обычного текстового файла в формате, отличном от Юникода, она может служить неявным маркером или сигнатурой для того, чтобы идентификатор файла определялся как файл Юникода.</span><span class="sxs-lookup"><span data-stu-id="418dd-128">Since the sequence U+FEFF is exceedingly rare at the beginning of a regular non-Unicode text file, it can serve as an implicit marker or signature to identify the file as a Unicode file.</span></span> <span data-ttu-id="418dd-129">Приложения, считывающие текстовые файлы в Юникоде и не в Юникоде, должны использовать эту последовательность в качестве индикатора того, что файл, скорее всего, является файлом Юникода.</span><span class="sxs-lookup"><span data-stu-id="418dd-129">Applications that read both Unicode and non-Unicode text files should use the presence of this sequence as an indicator that the file is most likely a Unicode file.</span></span> <span data-ttu-id="418dd-130">Сравните этот метод с использованием маркера MS-DOS EOF для завершения текстовых файлов.</span><span class="sxs-lookup"><span data-stu-id="418dd-130">Compare this technique to using the MS-DOS EOF marker to terminate text files.</span></span>

<span data-ttu-id="418dd-131">Когда приложение обнаруживает U + FEFF в начале текстового файла, оно обычно обрабатывает файл как файл Юникода, хотя он может выполнять дальнейшие эвристические проверки.</span><span class="sxs-lookup"><span data-stu-id="418dd-131">When an application finds U+FEFF at the beginning of a text file, it typically processes the file as a Unicode file, although it can perform further heuristic checks for verification.</span></span> <span data-ttu-id="418dd-132">Такая проверка может быть настолько простой, как тестирование, чтобы выяснить, является ли изменение в байтах нижнего порядка большим, чем изменение в байтах с высоким порядковым номером.</span><span class="sxs-lookup"><span data-stu-id="418dd-132">Such a check can be as simple as testing to find out if the variation in the low-order bytes is much higher than the variation in the high-order bytes.</span></span> <span data-ttu-id="418dd-133">Например, если текст ASCII преобразуется в текст в Юникоде, каждый второй байт равен 0.</span><span class="sxs-lookup"><span data-stu-id="418dd-133">For example, if ASCII text is converted to Unicode text, every second byte is 0.</span></span> <span data-ttu-id="418dd-134">Кроме того, при проверке того, что символы перевода строки и возврата каретки (U + 000A; и U + 000D), а также для четного или нечетного размера файла, могут дать строгий показатель природы файла.</span><span class="sxs-lookup"><span data-stu-id="418dd-134">Also, checking both for the linefeed and carriage return characters (U+000A and U+000D) and for even or odd file size can provide a strong indicator of the nature of the file.</span></span>

<span data-ttu-id="418dd-135">Когда приложение обнаруживает U + ФФФЕ в начале текстового файла, оно интерпретирует его как файл с обратным байтом в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="418dd-135">When an application finds U+FFFE at the beginning of a text file, it interprets it to mean that the file is a byte-reversed Unicode file.</span></span> <span data-ttu-id="418dd-136">Приложение может либо поменять порядок байтов, либо предупредить пользователя о том, что произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="418dd-136">The application can either swap the order of the bytes or alert the user that an error has occurred.</span></span>

<span data-ttu-id="418dd-137">Поскольку символ метки порядка байтов Юникода не найден ни в одной кодовой странице, он исчезает, если данные преобразуются в ANSI.</span><span class="sxs-lookup"><span data-stu-id="418dd-137">Since the Unicode byte order mark character is not found in any code page, it disappears if data is converted to ANSI.</span></span> <span data-ttu-id="418dd-138">В отличие от других символов Юникода, он не заменяется символом по умолчанию при преобразовании.</span><span class="sxs-lookup"><span data-stu-id="418dd-138">Unlike other Unicode characters, it is not replaced by a default character when it is converted.</span></span> <span data-ttu-id="418dd-139">Если метка порядка байтов находится в середине файла, она не интерпретируется как символ Юникода и не влияет на вывод текста.</span><span class="sxs-lookup"><span data-stu-id="418dd-139">If a byte order mark is found in the middle of a file, it is not interpreted as a Unicode character and has no effect on text output.</span></span>

> [!Note]  
> <span data-ttu-id="418dd-140">Значение Юникода U + FFFF недопустимо в текстовых файлах и не может передаваться между приложениями.</span><span class="sxs-lookup"><span data-stu-id="418dd-140">The Unicode value U+FFFF is illegal in plain text files and cannot be passed between applications.</span></span> <span data-ttu-id="418dd-141">Он зарезервирован для частного использования приложения.</span><span class="sxs-lookup"><span data-stu-id="418dd-141">It is reserved for the private use of an application.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="418dd-142">См. также</span><span class="sxs-lookup"><span data-stu-id="418dd-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="418dd-143">Использование специальных символов в Юникоде</span><span class="sxs-lookup"><span data-stu-id="418dd-143">Using Special Characters in Unicode</span></span>](using-special-characters-in-unicode.md)
</dt> </dl>

 

 




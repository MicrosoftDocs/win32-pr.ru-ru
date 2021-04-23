---
description: В этой статье описывается, как диспетчер графов фильтров находит фильтр источника по заданному имени файла.
ms.assetid: bc0d5719-6325-40fe-8261-ad00b91f272c
title: Регистрация пользовательского типа файла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e98c01555497ac628fff452f464c826475edbb8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105672998"
---
# <a name="registering-a-custom-file-type"></a><span data-ttu-id="81f2b-103">Регистрация пользовательского типа файла</span><span class="sxs-lookup"><span data-stu-id="81f2b-103">Registering a Custom File Type</span></span>

<span data-ttu-id="81f2b-104">В этой статье описывается, как диспетчер графов фильтров находит фильтр источника по заданному имени файла.</span><span class="sxs-lookup"><span data-stu-id="81f2b-104">This article describes how the Filter Graph Manager locates a source filter, given a file name.</span></span> <span data-ttu-id="81f2b-105">Этот механизм можно использовать для регистрации собственных пользовательских типов файлов.</span><span class="sxs-lookup"><span data-stu-id="81f2b-105">You can use this mechanism to register your own custom file types.</span></span> <span data-ttu-id="81f2b-106">После регистрации типа файла DirectShow автоматически загрузит правильный фильтр источника всякий раз, когда приложение вызывает [**играфбуилдер:: renderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) или [**Играфбуилдер:: аддсаурцефилтер**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter).</span><span class="sxs-lookup"><span data-stu-id="81f2b-106">Once the file type is registered, DirectShow will automatically load the correct source filter whenever an application calls [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) or [**IGraphBuilder::AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter).</span></span>

-   [<span data-ttu-id="81f2b-107">Обзор</span><span class="sxs-lookup"><span data-stu-id="81f2b-107">Overview</span></span>](#overview)
-   [<span data-ttu-id="81f2b-108">Протоколы</span><span class="sxs-lookup"><span data-stu-id="81f2b-108">Protocols</span></span>](#protocols)
-   [<span data-ttu-id="81f2b-109">Расширения файлов</span><span class="sxs-lookup"><span data-stu-id="81f2b-109">File Extensions</span></span>](#file-extensions)
-   [<span data-ttu-id="81f2b-110">Проверить байты</span><span class="sxs-lookup"><span data-stu-id="81f2b-110">Check Bytes</span></span>](#check-bytes)
-   [<span data-ttu-id="81f2b-111">Загрузка фильтра источника</span><span class="sxs-lookup"><span data-stu-id="81f2b-111">Loading the Source Filter</span></span>](#loading-the-source-filter)
-   [<span data-ttu-id="81f2b-112">Пользовательские типы файлов в проигрывателе Windows Media</span><span class="sxs-lookup"><span data-stu-id="81f2b-112">Custom File Types in Windows Media Player</span></span>](#custom-file-types-in-windows-media-player)
-   [<span data-ttu-id="81f2b-113">См. также</span><span class="sxs-lookup"><span data-stu-id="81f2b-113">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="81f2b-114">Обзор</span><span class="sxs-lookup"><span data-stu-id="81f2b-114">Overview</span></span>

<span data-ttu-id="81f2b-115">Чтобы указать фильтр источника по заданному имени файла, диспетчер графа фильтров пытается выполнить следующие действия в указанном порядке:</span><span class="sxs-lookup"><span data-stu-id="81f2b-115">To locate a source filter from a given file name, the Filter Graph Manager attempts to do the following, in order:</span></span>

1.  <span data-ttu-id="81f2b-116">Соответствует протоколу, если он есть.</span><span class="sxs-lookup"><span data-stu-id="81f2b-116">Match the protocol, if any.</span></span>
2.  <span data-ttu-id="81f2b-117">Соответствует расширению файла.</span><span class="sxs-lookup"><span data-stu-id="81f2b-117">Match the file extension.</span></span>
3.  <span data-ttu-id="81f2b-118">Совпадение с шаблонами байтов в файле, называемыми *Check bytes*.</span><span class="sxs-lookup"><span data-stu-id="81f2b-118">Match patterns of bytes within the file, called *check bytes*.</span></span>

## <a name="protocols"></a><span data-ttu-id="81f2b-119">Протоколы</span><span class="sxs-lookup"><span data-stu-id="81f2b-119">Protocols</span></span>

<span data-ttu-id="81f2b-120">Такие имена протоколов, как FTP или HTTP, регистрируются в</span><span class="sxs-lookup"><span data-stu-id="81f2b-120">Protocol names such as "ftp" or "http" are registered under the</span></span>

<span data-ttu-id="81f2b-121">**\_корневой узел классов hKey \_**</span><span class="sxs-lookup"><span data-stu-id="81f2b-121">**HKEY\_CLASSES\_ROOT**</span></span>

<span data-ttu-id="81f2b-122">(ключ) со следующей структурой:</span><span class="sxs-lookup"><span data-stu-id="81f2b-122">key, with the following structure:</span></span>


```C++
HKEY_CLASSES_ROOT
    <protocol>
        Source Filter = <Source filter CLSID>
        Extensions
            <.ext1> = <Source filter CLSID>
            <.ext2> = <Source filter CLSID>
```



<span data-ttu-id="81f2b-123">Если имя или URL-адрес файла содержит двоеточие (":"), диспетчер графа фильтров пытается использовать часть, предшествующую ":", в качестве имени протокола.</span><span class="sxs-lookup"><span data-stu-id="81f2b-123">If the file name or URL contains a colon (':'), the Filter Graph Manager attempts to use the portion before the ':' as a protocol name.</span></span> <span data-ttu-id="81f2b-124">Например, если имя — "myprot://myfile.ext", выполняется поиск раздела реестра с именем **мипрот**.</span><span class="sxs-lookup"><span data-stu-id="81f2b-124">For example, if the name is "myprot://myfile.ext", it searches for a registry key named **myprot**.</span></span> <span data-ttu-id="81f2b-125">Если этот ключ существует и содержит подраздел с именем Extensions, диспетчер графов фильтров ищет в этом подразделе записи, соответствующие расширению файла.</span><span class="sxs-lookup"><span data-stu-id="81f2b-125">If this key exists and contains a subkey named "Extensions", the Filter Graph Manager searches within that subkey for entries that match the file extension.</span></span> <span data-ttu-id="81f2b-126">Значение ключа должно быть идентификатором GUID в строковом формате. Например, " {00000000-0000-0000-0000-000000000000} ".</span><span class="sxs-lookup"><span data-stu-id="81f2b-126">The value of the key must be a GUID in string form; for example, "{00000000-0000-0000-0000-000000000000}".</span></span> <span data-ttu-id="81f2b-127">Если диспетчер графов фильтров не может сопоставить что-либо в подразделе **Extensions** , он ищет подраздел с именем **Source Filter**, который также должен быть идентификатором GUID в строковом формате.</span><span class="sxs-lookup"><span data-stu-id="81f2b-127">If the Filter Graph Manager cannot match anything within the **Extensions** subkey, it looks for a subkey named **Source Filter**, which must also be a GUID in string form.</span></span>

<span data-ttu-id="81f2b-128">Если диспетчер графов фильтров находит соответствующий GUID, он использует его в качестве идентификатора CLSID для фильтра источника и пытается загрузить фильтр.</span><span class="sxs-lookup"><span data-stu-id="81f2b-128">If the Filter Graph Manager finds a matching GUID, it uses this as the CLSID of the source filter, and attempts to load the filter.</span></span> <span data-ttu-id="81f2b-129">Если совпадение не найдено, используется фильтр [источника файлов (URL-адрес)](file-source--url--filter.md) , который считает имя файла URL-адресом.</span><span class="sxs-lookup"><span data-stu-id="81f2b-129">If it does not find a match, it uses the [File Source (URL)](file-source--url--filter.md) filter, which treats the file name as a URL.</span></span>

<span data-ttu-id="81f2b-130">Существует два исключения из этого алгоритма:</span><span class="sxs-lookup"><span data-stu-id="81f2b-130">There are two exceptions to this algorithm:</span></span>

-   <span data-ttu-id="81f2b-131">Чтобы исключить буквы драйверов, строки с одним символом не считаются протоколами.</span><span class="sxs-lookup"><span data-stu-id="81f2b-131">To exclude driver letters, single-character strings are not considered protocols.</span></span>
-   <span data-ttu-id="81f2b-132">Если строка имеет значение "file:" или "file://", она не рассматривается как протокол.</span><span class="sxs-lookup"><span data-stu-id="81f2b-132">If the string is "file:" or "file://", it is not treated as a protocol.</span></span>

## <a name="file-extensions"></a><span data-ttu-id="81f2b-133">Расширения файлов</span><span class="sxs-lookup"><span data-stu-id="81f2b-133">File Extensions</span></span>

<span data-ttu-id="81f2b-134">Если в имени файла нет протокола, диспетчер графа фильтров ищет в реестре записи с ключевыми **\_ \_ \\ \\ расширениями \\ класса hKey root Media Types**.*Ext* \\ , где.*Ext* — это расширение файла.</span><span class="sxs-lookup"><span data-stu-id="81f2b-134">If there is no protocol in the file name, the Filter Graph Manager looks in the registry for entries with the key **HKEY\_CLASSES\_ROOT\\Media Type\\Extensions\\**.*ext*\\, where .*ext* is the file extension.</span></span> <span data-ttu-id="81f2b-135">Если этот ключ существует, **Фильтр источника** значения содержит идентификатор CLSID исходного фильтра в виде строки.</span><span class="sxs-lookup"><span data-stu-id="81f2b-135">If this key exists, the value **Source Filter** contains the CLSID of the source filter, in string form.</span></span> <span data-ttu-id="81f2b-136">При необходимости ключ может иметь значения для **типа мультимедиа** и подтип, который предоставляет основной тип и идентификатор GUID **подтипа.**</span><span class="sxs-lookup"><span data-stu-id="81f2b-136">Optionally, the key can have values for **Media Type** and **Subtype**, which give the major type and subtype GUIDs.</span></span>

## <a name="check-bytes"></a><span data-ttu-id="81f2b-137">Проверить байты</span><span class="sxs-lookup"><span data-stu-id="81f2b-137">Check Bytes</span></span>

<span data-ttu-id="81f2b-138">Некоторые типы файлов могут определяться конкретными шаблонами битов, происходящими по конкретным смещениям байтов в файле.</span><span class="sxs-lookup"><span data-stu-id="81f2b-138">Some file types can be identified by specific patterns of bits occurring at specific byte offsets in the file.</span></span> <span data-ttu-id="81f2b-139">Диспетчер графов фильтров ищет в реестре ключи в следующем формате:</span><span class="sxs-lookup"><span data-stu-id="81f2b-139">The Filter Graph Manager looks in the registry for keys with the following form:</span></span>

<span data-ttu-id="81f2b-140">**HKey \_ \_Корневой \\ \\ элемент класса MediaType**{ *основной тип* } \\ { *подтип* }</span><span class="sxs-lookup"><span data-stu-id="81f2b-140">**HKEY\_CLASSES\_ROOT\\MediaType\\**{ *major type* }\\{ *subtype* }</span></span>

<span data-ttu-id="81f2b-141">где *основной тип* и *подтип* являются идентификаторами GUID, определяющими тип мультимедиа для потока байтов.</span><span class="sxs-lookup"><span data-stu-id="81f2b-141">where *major type* and *subtype* are GUIDs that define the media type for the byte stream.</span></span> <span data-ttu-id="81f2b-142">Каждый ключ содержит один или несколько подразделов, обычно именуемых 1, 2 и т. д., которые определяют байты проверки; и подраздела с именем **Исходный фильтр** , который предоставляет CLSID исходного фильтра в виде строки.</span><span class="sxs-lookup"><span data-stu-id="81f2b-142">Each key contains one or more subkeys, usually named 1, 2, and so on, which define the check bytes; and a subkey named **Source Filter** that gives the CLSID of the source filter, in string form.</span></span> <span data-ttu-id="81f2b-143">Подразделы Check-Byte — это строки, содержащие одно или несколько четырех чисел, которые называются:</span><span class="sxs-lookup"><span data-stu-id="81f2b-143">The check-byte subkeys are strings that contain one or more quads of numbers called:</span></span>

<span data-ttu-id="81f2b-144">*СМЕЩ*, *CB*, *Mask*, *Val*</span><span class="sxs-lookup"><span data-stu-id="81f2b-144">*offset*, *cb*, *mask*, *val*</span></span>

<span data-ttu-id="81f2b-145">Чтобы сопоставить этот файл, диспетчер графа фильтров считывает значения CB в байтах, начиная с смещения числа байтов.</span><span class="sxs-lookup"><span data-stu-id="81f2b-145">To match the file, the Filter Graph Manager reads cb bytes, starting from byte number offset.</span></span> <span data-ttu-id="81f2b-146">Затем он выполняет операцию побитового и относительно значения в маске.</span><span class="sxs-lookup"><span data-stu-id="81f2b-146">It then performs a bitwise-AND against the value in mask.</span></span> <span data-ttu-id="81f2b-147">Если результат равен Val, то файл будет соответствовать этому четырем.</span><span class="sxs-lookup"><span data-stu-id="81f2b-147">If the result equals val, the file is a match for that quad.</span></span> <span data-ttu-id="81f2b-148">Значения Mask и Val задаются в шестнадцатеричном формате.</span><span class="sxs-lookup"><span data-stu-id="81f2b-148">The values mask and val are given in hex.</span></span> <span data-ttu-id="81f2b-149">Пустая запись для Mask обрабатывается как строка из 1 длинного значения CB.</span><span class="sxs-lookup"><span data-stu-id="81f2b-149">A blank entry for mask is treated as a string of 1s of length cb.</span></span> <span data-ttu-id="81f2b-150">Отрицательное значение смещения указывает смещение от конца файла.</span><span class="sxs-lookup"><span data-stu-id="81f2b-150">A negative value for offset indicates an offset from the end of the file.</span></span> <span data-ttu-id="81f2b-151">Чтобы сопоставить ключ, файл должен соответствовать всем четырем из этих четырех подразделов.</span><span class="sxs-lookup"><span data-stu-id="81f2b-151">To match the key, the file must match all of the quads in any of the subkeys.</span></span>

<span data-ttu-id="81f2b-152">Например, предположим, что реестр содержит следующие ключи в **\\ типе носителя HKCR**:</span><span class="sxs-lookup"><span data-stu-id="81f2b-152">For example, assume the registry contains the following keys under **HKCR\\Media Type**:</span></span>


```C++
{e436eb83-524f-11ce-9f53-0020af0ba770}
    {7364696D-0000-0010-8000-00AA00389B71}
        0                    "0,4,,52494646,8,4,,524D4944"
        1                    "0,4,,4D546864"
        Source Filter        "{E436EBB5-524F-11CE-9F53-0020AF0BA770}"
```



<span data-ttu-id="81f2b-153">Первый ключ соответствует \_ потоку типа MEDIATYPE.</span><span class="sxs-lookup"><span data-stu-id="81f2b-153">The first key corresponds to the major type MEDIATYPE\_Stream.</span></span> <span data-ttu-id="81f2b-154">Подраздел ниже, соответствующий подтипу MEDIATYPE \_ MIDI.</span><span class="sxs-lookup"><span data-stu-id="81f2b-154">The subkey below that corresponds to the subtype MEDIATYPE\_Midi.</span></span> <span data-ttu-id="81f2b-155">Значение для подраздела фильтра источника — CLSID \_ асинкреадер, CLSID фильтра [File Source (Async)](file-source--async--filter.md) .</span><span class="sxs-lookup"><span data-stu-id="81f2b-155">The value for the Source Filter subkey is CLSID\_AsyncReader, the CLSID of the [File Source (Async)](file-source--async--filter.md) filter.</span></span>

<span data-ttu-id="81f2b-156">Каждая запись может иметь несколько четверок; Все они должны совпадать.</span><span class="sxs-lookup"><span data-stu-id="81f2b-156">Each entry can have multiple quadruples; all of them must match.</span></span> <span data-ttu-id="81f2b-157">В следующем примере первые 4 байта файла должны быть 0xAB, 0xCD, 0x12, 0x34; и последние 4 байта файла должны быть 0xAB, 0xAB, 0x00, 0xAB:</span><span class="sxs-lookup"><span data-stu-id="81f2b-157">In the following example, the first 4 bytes of the file must be 0xAB, 0xCD, 0x12, 0x34; and the last 4 bytes of the file must be 0xAB, 0xAB, 0x00, 0xAB:</span></span>


```C++
    0, 4, , ABCD1234,  -4, 4, , ABAB00AB 
```



<span data-ttu-id="81f2b-158">Кроме того, в одном типе носителя может присутствовать несколько записей.</span><span class="sxs-lookup"><span data-stu-id="81f2b-158">Also, there can be multiple entries listed under a single media type.</span></span> <span data-ttu-id="81f2b-159">Достаточно совпадений с любым из них.</span><span class="sxs-lookup"><span data-stu-id="81f2b-159">A match to any of them is sufficient.</span></span> <span data-ttu-id="81f2b-160">Эта схема обеспечивает набор альтернативных масок. Например, WAV-файлы, которые могут иметь или не иметь заголовок Metallica.</span><span class="sxs-lookup"><span data-stu-id="81f2b-160">This scheme allows for a set of alternative masks; for instance, .wav files that might or might not have a RIFF header.</span></span>

> [!Note]  
> <span data-ttu-id="81f2b-161">Эта схема похожа на ту, которая используется функцией [**жетклассфиле**](/windows/win32/api/objbase/nf-objbase-getclassfile) .</span><span class="sxs-lookup"><span data-stu-id="81f2b-161">This scheme is similar to the one used by the [**GetClassFile**](/windows/win32/api/objbase/nf-objbase-getclassfile) function.</span></span>

 

## <a name="loading-the-source-filter"></a><span data-ttu-id="81f2b-162">Загрузка фильтра источника</span><span class="sxs-lookup"><span data-stu-id="81f2b-162">Loading the Source Filter</span></span>

<span data-ttu-id="81f2b-163">Предполагая, что диспетчер графов фильтров находит соответствующий фильтр источника для файла, он добавляет этот фильтр к графу, запрашивает фильтр для интерфейса [**ифилесаурцефилтер**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) и вызывает [**Ифилесаурцефилтер:: Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load).</span><span class="sxs-lookup"><span data-stu-id="81f2b-163">Assuming that the Filter Graph Manager finds a matching source filter for the file, it adds that filter to the graph, queries the filter for the [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) interface, and calls [**IFileSourceFilter::Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load).</span></span> <span data-ttu-id="81f2b-164">Аргументы метода **Load** — это имя файла и тип носителя, как определено в реестре.</span><span class="sxs-lookup"><span data-stu-id="81f2b-164">The arguments to the **Load** method are the file name and the media type, as determined from the registry.</span></span>

<span data-ttu-id="81f2b-165">Если диспетчер графов фильтров не может найти что-либо из реестра, по умолчанию используется фильтр асинхронного файла.</span><span class="sxs-lookup"><span data-stu-id="81f2b-165">If the Filter Graph Manager cannot find anything from the registry, it defaults to using the Async File Source filter.</span></span> <span data-ttu-id="81f2b-166">В этом случае он задает тип носителя **\_ Stream**, **медиасубтипе \_ None**.</span><span class="sxs-lookup"><span data-stu-id="81f2b-166">In that case, it sets the media type to **MEDIATYPE\_Stream**, **MEDIASUBTYPE\_None**.</span></span>

## <a name="custom-file-types-in-windows-media-player"></a><span data-ttu-id="81f2b-167">Пользовательские типы файлов в проигрывателе Windows Media</span><span class="sxs-lookup"><span data-stu-id="81f2b-167">Custom File Types in Windows Media Player</span></span>

<span data-ttu-id="81f2b-168">Проигрыватель Windows Media использует дополнительный набор записей реестра.</span><span class="sxs-lookup"><span data-stu-id="81f2b-168">Windows Media Player uses an additional set of registry entries.</span></span> <span data-ttu-id="81f2b-169">Дополнительные сведения см. в разделе [параметры реестра для расширения имени файла](../wmp/file-name-extension-registry-settings.md) в пакете SDK проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="81f2b-169">For more information, see [File Name Extension Registry Settings](../wmp/file-name-extension-registry-settings.md) in the Windows Media Player SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="81f2b-170">См. также</span><span class="sxs-lookup"><span data-stu-id="81f2b-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81f2b-171">Написание фильтров DirectShow</span><span class="sxs-lookup"><span data-stu-id="81f2b-171">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 

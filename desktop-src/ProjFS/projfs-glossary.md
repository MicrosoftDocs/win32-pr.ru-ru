---
title: Глоссарий файловой системы Windows
description: Специальные термины, используемые в Прожфс.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: c6eac8faa83e2c898e4b1a3ada5c24ef81151b22
ms.sourcegitcommit: a48b68a75323edfb902eb04fbe6d0ecba6988c21
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/21/2020
ms.locfileid: "105719113"
---
# <a name="windows-projected-file-system-glossary"></a><span data-ttu-id="96123-103">Глоссарий файловой системы Windows</span><span class="sxs-lookup"><span data-stu-id="96123-103">Windows Projected File System glossary</span></span>

<span data-ttu-id="96123-104">Специальные термины, используемые в Прожфс.</span><span class="sxs-lookup"><span data-stu-id="96123-104">Special terms used in ProjFS.</span></span>

<dl>
<dt>

<span data-ttu-id="96123-105"><span id="projfs.glossary_backing_store"></span><span id="PROJFS.GLOSSARY_BACKING_STORE"></span>**Резервное хранилище**</span><span class="sxs-lookup"><span data-stu-id="96123-105"><span id="projfs.glossary_backing_store"></span><span id="PROJFS.GLOSSARY_BACKING_STORE"></span>**backing store**</span></span>
</dt>
<dd>

<span data-ttu-id="96123-106">Иерархические данные, поддерживаемые поставщиком, которые проецируются в файловую систему как файлы и каталоги.</span><span class="sxs-lookup"><span data-stu-id="96123-106">Provider-maintained hierarchical data that is projected into the file system as files and directories.</span></span>
</dd>

<dt>

<span data-ttu-id="96123-107"><span id="projfs.glossary_dirty_placeholder"></span><span id="PROJFS.GLOSSARY_DIRTY_PLACEHOLDER"></span>**заполнитель "грязный"**</span><span class="sxs-lookup"><span data-stu-id="96123-107"><span id="projfs.glossary_dirty_placeholder"></span><span id="PROJFS.GLOSSARY_DIRTY_PLACEHOLDER"></span>**dirty placeholder**</span></span>
</dt>
<dd>

<span data-ttu-id="96123-108">Файл или каталог, который был локально изменен и больше не является кэшем своего состояния в хранилище поставщика.</span><span class="sxs-lookup"><span data-stu-id="96123-108">A file or directory that has been locally modified and is no longer a cache of its state in the provider's store.</span></span>  <span data-ttu-id="96123-109">См. сведения о [состоянии кэша в корне виртуализации](cache-state.md).</span><span class="sxs-lookup"><span data-stu-id="96123-109">See [Cache State in the Virtualization Root](cache-state.md).</span></span>
</dd>

<dt>

<span data-ttu-id="96123-110"><span id="projfs.glossary_full_file_directory"></span><span id="PROJFS.GLOSSARY_FULL_FILE_DIRECTORY"></span>**полный файл или каталог**</span><span class="sxs-lookup"><span data-stu-id="96123-110"><span id="projfs.glossary_full_file_directory"></span><span id="PROJFS.GLOSSARY_FULL_FILE_DIRECTORY"></span>**full file/directory**</span></span>
</dt>
<dd>

<span data-ttu-id="96123-111">Файл или каталог, созданный в локальной файловой системе, или файл, который был изменен, что делает его недоступным для кэша своего состояния в резервном хранилище.</span><span class="sxs-lookup"><span data-stu-id="96123-111">A file or directory that was created in the local file system, or a file that has been modified, making it no longer a cache of its state in the backing store.</span></span>  <span data-ttu-id="96123-112">См. сведения о [состоянии кэша в корне виртуализации](cache-state.md).</span><span class="sxs-lookup"><span data-stu-id="96123-112">See [Cache State in the Virtualization Root](cache-state.md).</span></span>
</dd>

<dt>

<span data-ttu-id="96123-113"><span id="projfs.glossary_hydrated_placeholder"></span><span id="PROJFS.GLOSSARY_HYDRATED_PLACEHOLDER"></span>**заполнитель заархивированного текста**</span><span class="sxs-lookup"><span data-stu-id="96123-113"><span id="projfs.glossary_hydrated_placeholder"></span><span id="PROJFS.GLOSSARY_HYDRATED_PLACEHOLDER"></span>**hydrated placeholder**</span></span>
</dt>
<dd>

<span data-ttu-id="96123-114">Файл, содержимое и метаданные которого были кэшированы на диск.</span><span class="sxs-lookup"><span data-stu-id="96123-114">A file whose content and metadata have been cached to disk.</span></span>  <span data-ttu-id="96123-115">См. сведения о [состоянии кэша в корне виртуализации](cache-state.md).</span><span class="sxs-lookup"><span data-stu-id="96123-115">See [Cache State in the Virtualization Root](cache-state.md).</span></span>
</dd>

<dt>

<span data-ttu-id="96123-116"><span id="projfs.glossary_placeholder"></span><span id="PROJFS.GLOSSARY_PLACEHOLDER"></span>**заполнителе**</span><span class="sxs-lookup"><span data-stu-id="96123-116"><span id="projfs.glossary_placeholder"></span><span id="PROJFS.GLOSSARY_PLACEHOLDER"></span>**placeholder**</span></span>
</dt>
<dd>

<span data-ttu-id="96123-117">Файл или каталог, который не полностью указан на диске.</span><span class="sxs-lookup"><span data-stu-id="96123-117">A file or directory that is not fully present on disk.</span></span>  <span data-ttu-id="96123-118">См. сведения о [состоянии кэша в корне виртуализации](cache-state.md).</span><span class="sxs-lookup"><span data-stu-id="96123-118">See [Cache State in the Virtualization Root](cache-state.md).</span></span>
</dd>

<dt>

<span data-ttu-id="96123-119"><span id="projfs.glossary_tombstone"></span><span id="PROJFS.GLOSSARY_TOMBSTONE"></span>**отметки полного удаления**</span><span class="sxs-lookup"><span data-stu-id="96123-119"><span id="projfs.glossary_tombstone"></span><span id="PROJFS.GLOSSARY_TOMBSTONE"></span>**tombstone**</span></span>
</dt>
<dd>

<span data-ttu-id="96123-120">Специальный скрытый заполнитель, представляющий элемент, который был удален из локальной файловой системы.</span><span class="sxs-lookup"><span data-stu-id="96123-120">A special hidden placeholder that represents an item that has been deleted from the local file system.</span></span>  <span data-ttu-id="96123-121">См. сведения о [состоянии кэша в корне виртуализации](cache-state.md).</span><span class="sxs-lookup"><span data-stu-id="96123-121">See [Cache State in the Virtualization Root](cache-state.md).</span></span>
</dd>

<dt>

<span data-ttu-id="96123-122"><span id="projfs.glossary_virtual_file_directory"></span><span id="PROJFS.GLOSSARY_virtual_file_directory"></span>**виртуальный файл или каталог**</span><span class="sxs-lookup"><span data-stu-id="96123-122"><span id="projfs.glossary_virtual_file_directory"></span><span id="PROJFS.GLOSSARY_virtual_file_directory"></span>**virtual file/directory**</span></span>
</dt>
<dd>

<span data-ttu-id="96123-123">Файл или каталог, который физически не существует на диске, но проецируется на результаты перечисления.</span><span class="sxs-lookup"><span data-stu-id="96123-123">A file or directory that does not physically exist on disk, but is projected into enumeration results.</span></span>  <span data-ttu-id="96123-124">См. сведения о [состоянии кэша в корне виртуализации](cache-state.md).</span><span class="sxs-lookup"><span data-stu-id="96123-124">See [Cache State in the Virtualization Root](cache-state.md).</span></span>
</dd>

<dt>

<span data-ttu-id="96123-125"><span id="projfs.glossary_virtualization_instance"></span><span id="PROJFS.GLOSSARY_VIRTUALIZATION_INSTANCE"></span>**экземпляр виртуализации**</span><span class="sxs-lookup"><span data-stu-id="96123-125"><span id="projfs.glossary_virtualization_instance"></span><span id="PROJFS.GLOSSARY_VIRTUALIZATION_INSTANCE"></span>**virtualization instance**</span></span>
</dt>
<dd>

<span data-ttu-id="96123-126">Объект в памяти, который управляет взаимодействием между поставщиком и Прожфс для набора файлов и каталогов, расположенных в определенном корне виртуализации.</span><span class="sxs-lookup"><span data-stu-id="96123-126">An in-memory object that manages communication between the provider and ProjFS for the set of files and directories located under a particular virtualization root.</span></span>
</dd>

<dt>

<span data-ttu-id="96123-127"><span id="projfs.glossary_virtualization_root"></span><span id="PROJFS.GLOSSARY_VIRTUALIZATION_ROOT"></span>**корень виртуализации**</span><span class="sxs-lookup"><span data-stu-id="96123-127"><span id="projfs.glossary_virtualization_root"></span><span id="PROJFS.GLOSSARY_VIRTUALIZATION_ROOT"></span>**virtualization root**</span></span>
</dt>
<dd>

<span data-ttu-id="96123-128">Каталог в файловой системе, в которой проецируется данные поставщика.</span><span class="sxs-lookup"><span data-stu-id="96123-128">A directory in the file system under which the provider's data is projected.</span></span>
</dd>

</dl>

<!--
<dt>

<span id="projfs.glossary_"></span><span id="PROJFS.GLOSSARY_"></span>**TERM**
</dt>
<dd>

DEFINITION
</dd>
-->
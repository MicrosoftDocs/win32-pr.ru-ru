---
description: В этом разделе содержатся справочные сведения о COM-интерфейсах, используемых для чтения и записи из файлов DirectX. x. Не рекомендуется.
ms.assetid: 66e3476a-4ee8-48ac-aab8-6653793e0ef3
title: Файловые интерфейсы X
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a6e47325a4912faeb919cb60571de3cccbbe265
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537604"
---
# <a name="x-file-interfaces"></a><span data-ttu-id="46744-104">Файловые интерфейсы X</span><span class="sxs-lookup"><span data-stu-id="46744-104">X File Interfaces</span></span>

<span data-ttu-id="46744-105">В этом разделе содержатся справочные сведения о COM-интерфейсах, используемых для чтения и записи из файлов DirectX. x.</span><span class="sxs-lookup"><span data-stu-id="46744-105">This section contains reference information for the COM interfaces used to read to and write from DirectX .x files.</span></span> <span data-ttu-id="46744-106">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="46744-106">Deprecated.</span></span>

-   [<span data-ttu-id="46744-107">**идиректксфиле**</span><span class="sxs-lookup"><span data-stu-id="46744-107">**IDirectXFile**</span></span>](idirectxfile.md)
-   [<span data-ttu-id="46744-108">**идиректксфилебинари**</span><span class="sxs-lookup"><span data-stu-id="46744-108">**IDirectXFileBinary**</span></span>](idirectxfilebinary.md)
-   [<span data-ttu-id="46744-109">**идиректксфиледата**</span><span class="sxs-lookup"><span data-stu-id="46744-109">**IDirectXFileData**</span></span>](idirectxfiledata.md)
-   [<span data-ttu-id="46744-110">**идиректксфиледатареференце**</span><span class="sxs-lookup"><span data-stu-id="46744-110">**IDirectXFileDataReference**</span></span>](idirectxfiledatareference.md)
-   [<span data-ttu-id="46744-111">**идиректксфилинумобжект**</span><span class="sxs-lookup"><span data-stu-id="46744-111">**IDirectXFileEnumObject**</span></span>](idirectxfileenumobject.md)
-   [<span data-ttu-id="46744-112">**идиректксфилеобжект**</span><span class="sxs-lookup"><span data-stu-id="46744-112">**IDirectXFileObject**</span></span>](idirectxfileobject.md)
-   [<span data-ttu-id="46744-113">**идиректксфилесавеобжект**</span><span class="sxs-lookup"><span data-stu-id="46744-113">**IDirectXFileSaveObject**</span></span>](idirectxfilesaveobject.md)

<span data-ttu-id="46744-114">В следующих таблицах показано отношение между интерфейсами файла. x.</span><span class="sxs-lookup"><span data-stu-id="46744-114">The following tables illustrate the relationship between the .x file interfaces.</span></span>



| <span data-ttu-id="46744-115">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="46744-115">Interface</span></span>             | <span data-ttu-id="46744-116">Является производным от</span><span class="sxs-lookup"><span data-stu-id="46744-116">Derives from</span></span>           | <span data-ttu-id="46744-117">Является производным от</span><span class="sxs-lookup"><span data-stu-id="46744-117">Derives from</span></span> |
|-----------------------|------------------------|--------------|
|                       | <span data-ttu-id="46744-118">идиректксфиле</span><span class="sxs-lookup"><span data-stu-id="46744-118">IDirectXFile</span></span>           | <span data-ttu-id="46744-119">IUnknown</span><span class="sxs-lookup"><span data-stu-id="46744-119">IUnknown</span></span>     |
| <span data-ttu-id="46744-120">идиректксфилебинари</span><span class="sxs-lookup"><span data-stu-id="46744-120">IDirectXFileBinary</span></span>    | <span data-ttu-id="46744-121">идиректксфилеобжект</span><span class="sxs-lookup"><span data-stu-id="46744-121">IDirectXFileObject</span></span>     | <span data-ttu-id="46744-122">IUnknown</span><span class="sxs-lookup"><span data-stu-id="46744-122">IUnknown</span></span>     |
| <span data-ttu-id="46744-123">идиректксфиледата</span><span class="sxs-lookup"><span data-stu-id="46744-123">IDirectXFileData</span></span>      | <span data-ttu-id="46744-124">идиректксфилеобжект</span><span class="sxs-lookup"><span data-stu-id="46744-124">IDirectXFileObject</span></span>     | <span data-ttu-id="46744-125">IUnknown</span><span class="sxs-lookup"><span data-stu-id="46744-125">IUnknown</span></span>     |
| <span data-ttu-id="46744-126">идиректксфилереференце</span><span class="sxs-lookup"><span data-stu-id="46744-126">IDirectXFileReference</span></span> | <span data-ttu-id="46744-127">идиректксфилеобжект</span><span class="sxs-lookup"><span data-stu-id="46744-127">IDirectXFileObject</span></span>     | <span data-ttu-id="46744-128">IUnknown</span><span class="sxs-lookup"><span data-stu-id="46744-128">IUnknown</span></span>     |
|                       | <span data-ttu-id="46744-129">идиректксфилесавеобжект</span><span class="sxs-lookup"><span data-stu-id="46744-129">IDirectXFileSaveObject</span></span> | <span data-ttu-id="46744-130">IUnknown</span><span class="sxs-lookup"><span data-stu-id="46744-130">IUnknown</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="46744-131">См. также</span><span class="sxs-lookup"><span data-stu-id="46744-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46744-132">Ссылка на X-файл (устаревшая)</span><span class="sxs-lookup"><span data-stu-id="46744-132">X File Reference (Legacy)</span></span>](dx9-graphics-reference-x-file.md)
</dt> </dl>

 

 




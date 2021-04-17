---
description: Константы службы VDS
ms.assetid: a3a8b549-51bc-48eb-9215-04c7311e03a3
title: Константы службы VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9979cd4416b5305c61f6275612422b1f4cfe43a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674290"
---
# <a name="vds-constants"></a><span data-ttu-id="4d00c-103">Константы службы VDS</span><span class="sxs-lookup"><span data-stu-id="4d00c-103">VDS Constants</span></span>

<span data-ttu-id="4d00c-104">\[Начиная с Windows 8 и Windows Server 2012, интерфейс COM [службы виртуальных дисков](virtual-disk-service-portal.md) заменяется [API управления хранилищами Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="4d00c-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="4d00c-105">Константы службы VDS классифицируются следующим образом:</span><span class="sxs-lookup"><span data-stu-id="4d00c-105">VDS constants are categorized as follows:</span></span>

-   [<span data-ttu-id="4d00c-106">Константы состояния объекта</span><span class="sxs-lookup"><span data-stu-id="4d00c-106">Object Status Constants</span></span>](#object-status-constants)
-   [<span data-ttu-id="4d00c-107">Константы для указания automagic</span><span class="sxs-lookup"><span data-stu-id="4d00c-107">Automagic Hints Constants</span></span>](#automagic-hints-constants)
-   [<span data-ttu-id="4d00c-108">Прочие константы</span><span class="sxs-lookup"><span data-stu-id="4d00c-108">Miscellaneous Constants</span></span>](#miscellaneous-constants)

### <a name="object-status-constants"></a><span data-ttu-id="4d00c-109">Константы состояния объекта</span><span class="sxs-lookup"><span data-stu-id="4d00c-109">Object Status Constants</span></span>



| <span data-ttu-id="4d00c-110">Константа</span><span class="sxs-lookup"><span data-stu-id="4d00c-110">Constant</span></span>           | <span data-ttu-id="4d00c-111">Значение</span><span class="sxs-lookup"><span data-stu-id="4d00c-111">Value</span></span> |
|--------------------|-------|
| <span data-ttu-id="4d00c-112">СОСТОЯНИЕ \_ неизвестно</span><span class="sxs-lookup"><span data-stu-id="4d00c-112">STATUS\_UNKNOWN</span></span>    | <span data-ttu-id="4d00c-113">0</span><span class="sxs-lookup"><span data-stu-id="4d00c-113">0</span></span>     |
| <span data-ttu-id="4d00c-114">СОСТОЯНИЕ в \_ сети</span><span class="sxs-lookup"><span data-stu-id="4d00c-114">STATUS\_ONLINE</span></span>     | <span data-ttu-id="4d00c-115">1</span><span class="sxs-lookup"><span data-stu-id="4d00c-115">1</span></span>     |
| <span data-ttu-id="4d00c-116">СОСТОЯНИЕ \_ не \_ Готово</span><span class="sxs-lookup"><span data-stu-id="4d00c-116">STATUS\_NOT\_READY</span></span> | <span data-ttu-id="4d00c-117">2</span><span class="sxs-lookup"><span data-stu-id="4d00c-117">2</span></span>     |
| <span data-ttu-id="4d00c-118">СОСТОЯНИЕ \_ без \_ носителя</span><span class="sxs-lookup"><span data-stu-id="4d00c-118">STATUS\_NO\_MEDIA</span></span>  | <span data-ttu-id="4d00c-119">3</span><span class="sxs-lookup"><span data-stu-id="4d00c-119">3</span></span>     |
| <span data-ttu-id="4d00c-120">СОСТОЯНИЕ " \_ вне сети"</span><span class="sxs-lookup"><span data-stu-id="4d00c-120">STATUS\_OFFLINE</span></span>    | <span data-ttu-id="4d00c-121">4</span><span class="sxs-lookup"><span data-stu-id="4d00c-121">4</span></span>     |
| <span data-ttu-id="4d00c-122">СОСТОЯНИЕ " \_ Ошибка"</span><span class="sxs-lookup"><span data-stu-id="4d00c-122">STATUS\_FAILED</span></span>     | <span data-ttu-id="4d00c-123">5</span><span class="sxs-lookup"><span data-stu-id="4d00c-123">5</span></span>     |
| <span data-ttu-id="4d00c-124">\_отсутствует состояние</span><span class="sxs-lookup"><span data-stu-id="4d00c-124">STATUS\_MISSING</span></span>    | <span data-ttu-id="4d00c-125">6</span><span class="sxs-lookup"><span data-stu-id="4d00c-125">6</span></span>     |



 

### <a name="automagic-hints-constants"></a><span data-ttu-id="4d00c-126">Константы для указания automagic</span><span class="sxs-lookup"><span data-stu-id="4d00c-126">Automagic Hints Constants</span></span>



| <span data-ttu-id="4d00c-127">Константа</span><span class="sxs-lookup"><span data-stu-id="4d00c-127">Constant</span></span>                               | <span data-ttu-id="4d00c-128">Значение</span><span class="sxs-lookup"><span data-stu-id="4d00c-128">Value</span></span>   |
|----------------------------------------|---------|
| <span data-ttu-id="4d00c-129">\_мостлиреадс указание \_ VDS</span><span class="sxs-lookup"><span data-stu-id="4d00c-129">VDS\_HINT\_MOSTLYREADS</span></span>                 | <span data-ttu-id="4d00c-130">0x0002L</span><span class="sxs-lookup"><span data-stu-id="4d00c-130">0x0002L</span></span> |
| <span data-ttu-id="4d00c-131">\_оптимизефорсекуентиалреадс указание \_ VDS</span><span class="sxs-lookup"><span data-stu-id="4d00c-131">VDS\_HINT\_OPTIMIZEFORSEQUENTIALREADS</span></span>  | <span data-ttu-id="4d00c-132">0x0004L</span><span class="sxs-lookup"><span data-stu-id="4d00c-132">0x0004L</span></span> |
| <span data-ttu-id="4d00c-133">\_оптимизефорсекуентиалвритес указание \_ VDS</span><span class="sxs-lookup"><span data-stu-id="4d00c-133">VDS\_HINT\_OPTIMIZEFORSEQUENTIALWRITES</span></span> | <span data-ttu-id="4d00c-134">0x0008L</span><span class="sxs-lookup"><span data-stu-id="4d00c-134">0x0008L</span></span> |
| <span data-ttu-id="4d00c-135">\_ремапенаблед указание \_ VDS</span><span class="sxs-lookup"><span data-stu-id="4d00c-135">VDS\_HINT\_REMAPENABLED</span></span>                | <span data-ttu-id="4d00c-136">0x0020L</span><span class="sxs-lookup"><span data-stu-id="4d00c-136">0x0020L</span></span> |
| <span data-ttu-id="4d00c-137">\_вритесраугхкачинженаблед указание \_ VDS</span><span class="sxs-lookup"><span data-stu-id="4d00c-137">VDS\_HINT\_WRITETHROUGHCACHINGENABLED</span></span>  | <span data-ttu-id="4d00c-138">0x0040L</span><span class="sxs-lookup"><span data-stu-id="4d00c-138">0x0040L</span></span> |
| <span data-ttu-id="4d00c-139">\_хардваречекксуменаблед указание \_ VDS</span><span class="sxs-lookup"><span data-stu-id="4d00c-139">VDS\_HINT\_HARDWARECHECKSUMENABLED</span></span>     | <span data-ttu-id="4d00c-140">0x0080L</span><span class="sxs-lookup"><span data-stu-id="4d00c-140">0x0080L</span></span> |
| <span data-ttu-id="4d00c-141">\_исянкабле указание \_ VDS</span><span class="sxs-lookup"><span data-stu-id="4d00c-141">VDS\_HINT\_ISYANKABLE</span></span>                  | <span data-ttu-id="4d00c-142">0x0100L</span><span class="sxs-lookup"><span data-stu-id="4d00c-142">0x0100L</span></span> |



 

### <a name="miscellaneous-constants"></a><span data-ttu-id="4d00c-143">Прочие константы</span><span class="sxs-lookup"><span data-stu-id="4d00c-143">Miscellaneous Constants</span></span>



| <span data-ttu-id="4d00c-144">Константа</span><span class="sxs-lookup"><span data-stu-id="4d00c-144">Constant</span></span>                     | <span data-ttu-id="4d00c-145">Значение</span><span class="sxs-lookup"><span data-stu-id="4d00c-145">Value</span></span>      |
|------------------------------|------------|
| <span data-ttu-id="4d00c-146">\_Минимальный приоритет повторного создания VDS \_ \_</span><span class="sxs-lookup"><span data-stu-id="4d00c-146">VDS\_REBUILD\_PRIORITY\_MIN</span></span>  | <span data-ttu-id="4d00c-147">0x0001L</span><span class="sxs-lookup"><span data-stu-id="4d00c-147">0x0001L</span></span>    |
| <span data-ttu-id="4d00c-148">\_ \_ сведения о LUN VDS для ver \_</span><span class="sxs-lookup"><span data-stu-id="4d00c-148">VER\_VDS\_LUN\_INFORMATION</span></span>   | <span data-ttu-id="4d00c-149">1</span><span class="sxs-lookup"><span data-stu-id="4d00c-149">1</span></span>          |
| <span data-ttu-id="4d00c-150">Максимальная \_ \_ Длина ComputerName</span><span class="sxs-lookup"><span data-stu-id="4d00c-150">MAX\_COMPUTERNAME\_LENGTH</span></span>    | <span data-ttu-id="4d00c-151">15</span><span class="sxs-lookup"><span data-stu-id="4d00c-151">15</span></span>         |
| <span data-ttu-id="4d00c-152">Максимальная \_ \_ Длина PROVIDERNAME</span><span class="sxs-lookup"><span data-stu-id="4d00c-152">MAX\_PROVIDERNAME\_LENGTH</span></span>    | <span data-ttu-id="4d00c-153">200</span><span class="sxs-lookup"><span data-stu-id="4d00c-153">200</span></span>        |
| <span data-ttu-id="4d00c-154">Максимальная \_ \_ Длина VERSIONSTRING</span><span class="sxs-lookup"><span data-stu-id="4d00c-154">MAX\_VERSIONSTRING\_LENGTH</span></span>   | <span data-ttu-id="4d00c-155">16</span><span class="sxs-lookup"><span data-stu-id="4d00c-155">16</span></span>         |
| <span data-ttu-id="4d00c-156">\_prop буква диска \_</span><span class="sxs-lookup"><span data-stu-id="4d00c-156">DRIVE\_LETTER\_PROP</span></span>          | <span data-ttu-id="4d00c-157">Н/Д</span><span class="sxs-lookup"><span data-stu-id="4d00c-157">N/A</span></span>        |
| <span data-ttu-id="4d00c-158">МАКСИМАЛЬНЫЙ \_ \_ Размер имени \_ FS</span><span class="sxs-lookup"><span data-stu-id="4d00c-158">MAX\_FS\_NAME\_SIZE</span></span>          | <span data-ttu-id="4d00c-159">8</span><span class="sxs-lookup"><span data-stu-id="4d00c-159">8</span></span>          |
| <span data-ttu-id="4d00c-160">Недопустимый \_ \_ idx члена</span><span class="sxs-lookup"><span data-stu-id="4d00c-160">INVALID\_MEMBER\_IDX</span></span>         | <span data-ttu-id="4d00c-161">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="4d00c-161">0xFFFFFFFF</span></span> |
| <span data-ttu-id="4d00c-162">\_ \_ Длина имени раздела \_ GPT</span><span class="sxs-lookup"><span data-stu-id="4d00c-162">GPT\_PARTITION\_NAME\_LENGTH</span></span> | <span data-ttu-id="4d00c-163">36</span><span class="sxs-lookup"><span data-stu-id="4d00c-163">36</span></span>         |
| <span data-ttu-id="4d00c-164">МАКСИМАЛЬНЫЙ \_ путь</span><span class="sxs-lookup"><span data-stu-id="4d00c-164">MAX\_PATH</span></span>                    | <span data-ttu-id="4d00c-165">260</span><span class="sxs-lookup"><span data-stu-id="4d00c-165">260</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="4d00c-166">См. также</span><span class="sxs-lookup"><span data-stu-id="4d00c-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d00c-167">Ссылка на службу VDS</span><span class="sxs-lookup"><span data-stu-id="4d00c-167">VDS Reference</span></span>](vds-reference.md)
</dt> </dl>

 

 

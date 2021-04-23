---
description: Хотя существует несколько технических ограничений на тип и размер данных, которые приложение может хранить в реестре, для повышения эффективности работы системы существует ряд практических рекомендаций.
ms.assetid: fa85ff87-3d72-4f71-856a-f43df7d19aa8
title: Место для хранения реестра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90b776498528d6c7deaacd92f9e010758b5d57c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663494"
---
# <a name="registry-storage-space"></a><span data-ttu-id="75a64-103">Место для хранения реестра</span><span class="sxs-lookup"><span data-stu-id="75a64-103">Registry Storage Space</span></span>

<span data-ttu-id="75a64-104">Хотя существует несколько технических ограничений на тип и размер данных, которые приложение может хранить в реестре, для повышения эффективности работы системы существует ряд практических рекомендаций.</span><span class="sxs-lookup"><span data-stu-id="75a64-104">Although there are few technical limits to the type and size of data an application can store in the registry, certain practical guidelines exist to promote system efficiency.</span></span> <span data-ttu-id="75a64-105">Приложение должно хранить данные конфигурации и инициализации в реестре и хранить другие типы данных в другом расположении.</span><span class="sxs-lookup"><span data-stu-id="75a64-105">An application should store configuration and initialization data in the registry, and store other kinds of data elsewhere.</span></span>

<span data-ttu-id="75a64-106">Как правило, данные, состоящие более чем из одного или двух килобайтов (K), должны храниться в виде файла и ссылаться на них с помощью ключа в реестре, а не хранить как значение.</span><span class="sxs-lookup"><span data-stu-id="75a64-106">Generally, data consisting of more than one or two kilobytes (K) should be stored as a file and referred to by using a key in the registry rather than being stored as a value.</span></span> <span data-ttu-id="75a64-107">Вместо дублирования больших фрагментов данных в реестре приложение должно сохранить данные в виде файла и ссылаться на файл.</span><span class="sxs-lookup"><span data-stu-id="75a64-107">Instead of duplicating large pieces of data in the registry, an application should save the data as a file and refer to the file.</span></span> <span data-ttu-id="75a64-108">Исполняемый двоичный код никогда не должен храниться в реестре.</span><span class="sxs-lookup"><span data-stu-id="75a64-108">Executable binary code should never be stored in the registry.</span></span>

<span data-ttu-id="75a64-109">Запись значения использует гораздо меньше пространства реестра, чем ключ.</span><span class="sxs-lookup"><span data-stu-id="75a64-109">A value entry uses much less registry space than a key.</span></span> <span data-ttu-id="75a64-110">Чтобы сэкономить место, приложение должно сгруппировать аналогичные данные в виде структуры и сохранить структуру как значение, а не хранить каждый из членов структуры как отдельный ключ.</span><span class="sxs-lookup"><span data-stu-id="75a64-110">To save space, an application should group similar data together as a structure and store the structure as a value rather than storing each of the structure members as a separate key.</span></span> <span data-ttu-id="75a64-111">(Хранение данных в двоичной форме позволяет приложению хранить данные в одном значении, которое в противном случае было бы состоять из нескольких несовместимых типов).</span><span class="sxs-lookup"><span data-stu-id="75a64-111">(Storing the data in binary form allows an application to store data in one value that would otherwise be made up of several incompatible types.)</span></span>

<span data-ttu-id="75a64-112">Представления файлов реестра сопоставлены в памяти выгружаемого пула.</span><span class="sxs-lookup"><span data-stu-id="75a64-112">Views of the registry files are mapped in paged pool memory.</span></span>

<span data-ttu-id="75a64-113">**Windows server 2008 для 32-bit, Windows Vista с пакетом обновления 1 (SP1) для 32-bit, Windows Vista, Windows Server 2003, Windows XP:** Представления файлов реестра сопоставлены в адресном пространстве кэша компьютера.</span><span class="sxs-lookup"><span data-stu-id="75a64-113">**Windows Server 2008 for 32-bit, Windows Vista with SP1 for 32-bit, Windows Vista, Windows Server 2003, Windows XP:** Views of the registry files are mapped in the computer cache address space.</span></span> <span data-ttu-id="75a64-114">Таким образом, независимо от размера данных реестра, он не занимает больше 4 мегабайт (МБ).</span><span class="sxs-lookup"><span data-stu-id="75a64-114">Therefore, regardless of the size of the registry data, it is not charged more than 4 megabytes (MB).</span></span>

<span data-ttu-id="75a64-115">Максимальный размер куста реестра составляет 2 ГБ, за исключением системного куста.</span><span class="sxs-lookup"><span data-stu-id="75a64-115">The maximum size of a registry hive is 2 GB, except for the system hive.</span></span>

<span data-ttu-id="75a64-116">**Windows server 2003 с пакетом обновления 1 (SP1), Windows server 2003 и Windows XP:** Нет явных ограничений на общий объем пространства, который может использоваться Hive в выгружаемого пула памяти и на диске, хотя системные квоты могут повлиять на фактический максимальный размер.</span><span class="sxs-lookup"><span data-stu-id="75a64-116">**Windows Server 2003 with SP1, Windows Server 2003 and Windows XP:** There are no explicit limits on the total amount of space that may be consumed by hives in paged pool memory and in disk space, although system quotas may affect the actual maximum size.</span></span> <span data-ttu-id="75a64-117">Максимальный размер куста реестра ограничен 2 ГБ, начиная с Windows Server 2003 с пакетом обновления 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="75a64-117">The maximum size of a registry hive was limited to 2 GB starting with Windows Server 2003 with Service Pack 2 (SP2).</span></span>

<span data-ttu-id="75a64-118">Максимальный размер системного куста ограничен физической памятью, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="75a64-118">The maximum size of the system hive is limited by physical memory as shown in the following table.</span></span> 

| <span data-ttu-id="75a64-119">Система</span><span class="sxs-lookup"><span data-stu-id="75a64-119">System</span></span>                      | <span data-ttu-id="75a64-120">Максимальный размер системного куста</span><span class="sxs-lookup"><span data-stu-id="75a64-120">Maximum size of the system hive</span></span>                                                                                                                                                                                                            |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75a64-121">системы на базе x86</span><span class="sxs-lookup"><span data-stu-id="75a64-121">x86-based systems</span></span>           | <span data-ttu-id="75a64-122">50% физической памяти, до 400 МБ. **Windows server 2003 с пакетом обновления 2 (SP2), Windows server 2003 с пакетом обновления 1 (SP1), Windows server 2003 и Windows XP:** 25% физической памяти, до 200 МБ.</span><span class="sxs-lookup"><span data-stu-id="75a64-122">50 percent of physical memory, up to 400 MB.**Windows Server 2003 with SP2, Windows Server 2003 with SP1, Windows Server 2003 and Windows XP:** 25 percent of physical memory, up to 200 MB.</span></span><br/>                                    |
| <span data-ttu-id="75a64-123">системы на базе x64</span><span class="sxs-lookup"><span data-stu-id="75a64-123">x64-based systems</span></span>           | <span data-ttu-id="75a64-124">50% физической памяти, до 1,5 ГБ. **Windows Server 2003 с пакетом обновления 2 (SP2):** 25% системной памяти, до 200 МБ.</span><span class="sxs-lookup"><span data-stu-id="75a64-124">50 percent of physical memory, up to 1.5 GB.**Windows Server 2003 with SP2:** 25 percent of system memory, up to 200 MB.</span></span><br/> <span data-ttu-id="75a64-125">**Windows server 2003 с пакетом обновления 1 (SP1), Windows server 2003 и Windows XP 64-bit Edition:** 32 МБ.</span><span class="sxs-lookup"><span data-stu-id="75a64-125">**Windows Server 2003 with SP1, Windows Server 2003 and Windows XP 64-Bit Edition:** 32 MB.</span></span><br/> |
| <span data-ttu-id="75a64-126">Системы на базе Intel Itanium</span><span class="sxs-lookup"><span data-stu-id="75a64-126">Intel Itanium-based systems</span></span> | <span data-ttu-id="75a64-127">50% физической памяти, до 1 ГБ. **Windows server 2008, Windows Vista, Windows server 2003 с пакетом обновления 2 (SP2), Windows server 2003 с пакетом обновления 1 (SP1), Windows server 2003 и Windows XP 64-bit Edition:** 32 МБ.</span><span class="sxs-lookup"><span data-stu-id="75a64-127">50 percent of physical memory, up to 1 GB.**Windows Server 2008, Windows Vista, Windows Server 2003 with SP2, Windows Server 2003 with SP1, Windows Server 2003 and Windows XP 64-Bit Edition:** 32 MB.</span></span><br/>                         |



 

## <a name="windows-2000"></a><span data-ttu-id="75a64-128">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="75a64-128">Windows 2000</span></span>

<span data-ttu-id="75a64-129">Данные реестра хранятся в выгружаемом пуле, области физической памяти, используемой для системных данных, которые могут быть записаны на диск, когда они не используются.</span><span class="sxs-lookup"><span data-stu-id="75a64-129">Registry data is stored in the paged pool, an area of physical memory used for system data that can be written to disk when not in use.</span></span> <span data-ttu-id="75a64-130">Значение **регистрисизелимит** устанавливает максимальный объем выгружаемого пула, который может использоваться данными реестра из всех приложений.</span><span class="sxs-lookup"><span data-stu-id="75a64-130">The **RegistrySizeLimit** value establishes the maximum amount of paged pool that can be consumed by registry data from all applications.</span></span> <span data-ttu-id="75a64-131">Это значение находится в следующем разделе реестра:</span><span class="sxs-lookup"><span data-stu-id="75a64-131">This value is located in the following registry key:</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Control
```

<span data-ttu-id="75a64-132">По умолчанию предельный размер реестра составляет 25 процентов выгружаемого пула.</span><span class="sxs-lookup"><span data-stu-id="75a64-132">By default, the registry size limit is 25 percent of the paged pool.</span></span> <span data-ttu-id="75a64-133">(Размер выгружаемого пула по умолчанию составляет 32 МБ, поэтому это 8 МБ). Система гарантирует, что минимальное значение **регистрисизелимит** — 4 МБ, а максимальное — примерно 80% от значения **пажедпулсизе** .</span><span class="sxs-lookup"><span data-stu-id="75a64-133">(The default size of the paged pool is 32 MB, so this is 8 MB.) The system ensures that the minimum value of **RegistrySizeLimit** is 4 MB and the maximum is approximately 80 percent of the **PagedPoolSize** value.</span></span> <span data-ttu-id="75a64-134">Если значение этой записи превышает 80% от размера выгружаемого пула, система устанавливает максимальный размер реестра, равный 80% от размера выгружаемого пула.</span><span class="sxs-lookup"><span data-stu-id="75a64-134">If the value of this entry is greater than 80 percent of the size of the paged pool, the system sets the maximum size of the registry to 80 percent of the size of the paged pool.</span></span> <span data-ttu-id="75a64-135">Это предотвращает использование пространства реестра, необходимого для процессов.</span><span class="sxs-lookup"><span data-stu-id="75a64-135">This prevents the registry from consuming space needed by processes.</span></span> <span data-ttu-id="75a64-136">Обратите внимание, что установка этого значения не приводит к выделению места в выгружаемом пуле и не гарантирует, что при необходимости пространство будет доступно.</span><span class="sxs-lookup"><span data-stu-id="75a64-136">Note that setting this value does not allocate space in the paged pool, nor does it assure that the space will be available if needed.</span></span>

<span data-ttu-id="75a64-137">Размер выгружаемого пула определяется значением **пажедпулсизе** в следующем разделе реестра:</span><span class="sxs-lookup"><span data-stu-id="75a64-137">The paged pool size is determined by the **PagedPoolSize** value in the following registry key:</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Control
            SessionManager
               MemoryManagement
```

<span data-ttu-id="75a64-138">Пример определения текущего и максимального размера реестра см. [в разделе Определение размера реестра](determining-the-registry-size.md).</span><span class="sxs-lookup"><span data-stu-id="75a64-138">For an example of how to determine the current and maximum sizes of the registry, see [Determining the Registry Size](determining-the-registry-size.md).</span></span>

<span data-ttu-id="75a64-139">Максимальный размер выгружаемого пула составляет примерно 300 470 МБ, поэтому ограничение размера реестра составляет 240-376 МБ.</span><span class="sxs-lookup"><span data-stu-id="75a64-139">The maximum paged pool is approximately 300,470 MB so the registry size limit is 240-376 MB.</span></span> <span data-ttu-id="75a64-140">Однако если используется параметр/3GB, максимальный размер выгружаемого пула составляет 192 МБ, поэтому в реестре может быть не более 153,6 МБ.</span><span class="sxs-lookup"><span data-stu-id="75a64-140">However, if the /3GB switch is used, the maximum paged pool size is 192 MB, so the registry can be a maximum of 153.6 MB.</span></span>

 

 





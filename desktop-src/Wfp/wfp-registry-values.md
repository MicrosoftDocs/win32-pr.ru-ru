---
description: 'Значения реестра WFP находятся в следующем разделе реестра: HKLM \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Winlogon.'
ms.assetid: d4da7f24-1e5d-4ea2-98e8-049e7eaefae1
title: Значения реестра WFP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31cb8db23800ebbead68f34eaf0fa9fffd772f01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664347"
---
# <a name="wfp-registry-values"></a><span data-ttu-id="f8d23-103">Значения реестра WFP</span><span class="sxs-lookup"><span data-stu-id="f8d23-103">WFP Registry Values</span></span>

<span data-ttu-id="f8d23-104">\[Значения реестра WFP не поддерживаются в Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="f8d23-104">\[WFP registry values are not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="f8d23-105">WFP использует несколько значений реестра для настройки параметров.</span><span class="sxs-lookup"><span data-stu-id="f8d23-105">WFP uses several registry values for customization settings.</span></span> <span data-ttu-id="f8d23-106">Значения реестра WFP находятся в следующем разделе реестра:</span><span class="sxs-lookup"><span data-stu-id="f8d23-106">The WFP registry values are located in the following registry key:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows NT
            CurrentVersion
               Winlogon
```

<span data-ttu-id="f8d23-107">Ниже приведены значения реестра WFP.</span><span class="sxs-lookup"><span data-stu-id="f8d23-107">The following are the WFP registry values.</span></span>

<dl> <dt>

<span data-ttu-id="f8d23-108"><span id="SFCDllCacheDir"></span><span id="sfcdllcachedir"></span><span id="SFCDLLCACHEDIR"></span>**сфкдллкачедир**</span><span class="sxs-lookup"><span data-stu-id="f8d23-108"><span id="SFCDllCacheDir"></span><span id="sfcdllcachedir"></span><span id="SFCDLLCACHEDIR"></span>**SFCDllCacheDir**</span></span>
</dt> <dd>

<span data-ttu-id="f8d23-109">Расположение кэша.</span><span class="sxs-lookup"><span data-stu-id="f8d23-109">Location of the cache.</span></span> <span data-ttu-id="f8d23-110">Это должен быть локальный путь.</span><span class="sxs-lookup"><span data-stu-id="f8d23-110">This must be a local path.</span></span> <span data-ttu-id="f8d23-111">Значение по умолчанию —% SystemRoot% \\ system32 \\ Dllcache.</span><span class="sxs-lookup"><span data-stu-id="f8d23-111">The default value is %systemroot%\\system32\\dllcache.</span></span>

</dd> <dt>

<span data-ttu-id="f8d23-112"><span id="SFCQuota"></span><span id="sfcquota"></span><span id="SFCQUOTA"></span>**SFCQuota**</span><span class="sxs-lookup"><span data-stu-id="f8d23-112"><span id="SFCQuota"></span><span id="sfcquota"></span><span id="SFCQUOTA"></span>**SFCQuota**</span></span>
</dt> <dd>

<span data-ttu-id="f8d23-113">Параметры квоты.</span><span class="sxs-lookup"><span data-stu-id="f8d23-113">Quota options.</span></span> <span data-ttu-id="f8d23-114">Этот параметр реестра может принимать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="f8d23-114">This registry value can be one of the following values.</span></span>



| <span data-ttu-id="f8d23-115">Значение</span><span class="sxs-lookup"><span data-stu-id="f8d23-115">Value</span></span>                  | <span data-ttu-id="f8d23-116">Значение</span><span class="sxs-lookup"><span data-stu-id="f8d23-116">Meaning</span></span>                                                  |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="f8d23-117">\_Квота SFC \_ все \_ файлы</span><span class="sxs-lookup"><span data-stu-id="f8d23-117">SFC\_QUOTA\_ALL\_FILES</span></span> | <span data-ttu-id="f8d23-118">Размер кэша DLL не ограничен.</span><span class="sxs-lookup"><span data-stu-id="f8d23-118">Size of the DLL cache is unlimited.</span></span> <span data-ttu-id="f8d23-119">Это значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f8d23-119">This is the default.</span></span> |
| <span data-ttu-id="f8d23-120">Другие значения</span><span class="sxs-lookup"><span data-stu-id="f8d23-120">Other values</span></span>           | <span data-ttu-id="f8d23-121">Размер кэша DLL в файлах.</span><span class="sxs-lookup"><span data-stu-id="f8d23-121">Size of the DLL cache, in files.</span></span>                         |



 

</dd> <dt>

<span data-ttu-id="f8d23-122"><span id="SFCScan"></span><span id="sfcscan"></span><span id="SFCSCAN"></span>**сфкскан**</span><span class="sxs-lookup"><span data-stu-id="f8d23-122"><span id="SFCScan"></span><span id="sfcscan"></span><span id="SFCSCAN"></span>**SFCScan**</span></span>
</dt> <dd>

<span data-ttu-id="f8d23-123">Параметры проверки.</span><span class="sxs-lookup"><span data-stu-id="f8d23-123">Scan options.</span></span> <span data-ttu-id="f8d23-124">Этот параметр реестра может принимать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="f8d23-124">This registry value can be one of the following values.</span></span>



| <span data-ttu-id="f8d23-125">Значение</span><span class="sxs-lookup"><span data-stu-id="f8d23-125">Value</span></span>             | <span data-ttu-id="f8d23-126">Значение</span><span class="sxs-lookup"><span data-stu-id="f8d23-126">Meaning</span></span>                                                   |
|-------------------|-----------------------------------------------------------|
| <span data-ttu-id="f8d23-127">\_Проверка \_ обычного сканирования</span><span class="sxs-lookup"><span data-stu-id="f8d23-127">SFC\_SCAN\_NORMAL</span></span> | <span data-ttu-id="f8d23-128">Не проверять защищенные файлы при загрузке.</span><span class="sxs-lookup"><span data-stu-id="f8d23-128">Do not scan protected files at boot.</span></span> <span data-ttu-id="f8d23-129">Это значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f8d23-129">This is the default.</span></span> |
| <span data-ttu-id="f8d23-130">\_сканирование SFC \_ всегда</span><span class="sxs-lookup"><span data-stu-id="f8d23-130">SFC\_SCAN\_ALWAYS</span></span> | <span data-ttu-id="f8d23-131">Проверять защищенные файлы при каждой загрузке.</span><span class="sxs-lookup"><span data-stu-id="f8d23-131">Scan protected files at every boot.</span></span>                       |
| <span data-ttu-id="f8d23-132">\_Проверка SFC \_</span><span class="sxs-lookup"><span data-stu-id="f8d23-132">SFC\_SCAN\_ONCE</span></span>   | <span data-ttu-id="f8d23-133">Проверять защищенные файлы при следующей загрузке.</span><span class="sxs-lookup"><span data-stu-id="f8d23-133">Scan protected files at the next boot.</span></span>                    |



 

</dd> </dl>

 

 




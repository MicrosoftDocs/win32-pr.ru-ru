---
description: Если для этой системной политики на уровне компьютера задано значение больше 0, установщик Windows сохраняет старые версии файлов в кэше при применении исправления к приложению.
ms.assetid: 986cd521-6907-420d-a2e9-5e0da0069834
title: макспатчкачесизе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8d9930f4a52d3ea0126a19d4dfadae359321f56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497700"
---
# <a name="maxpatchcachesize"></a><span data-ttu-id="f0a3c-103">макспатчкачесизе</span><span class="sxs-lookup"><span data-stu-id="f0a3c-103">MaxPatchCacheSize</span></span>

<span data-ttu-id="f0a3c-104">Если для этой [системной политики](system-policy.md) на уровне компьютера задано значение больше 0, установщик Windows сохраняет старые версии файлов в кэше при применении исправления к приложению.</span><span class="sxs-lookup"><span data-stu-id="f0a3c-104">If this per-machine [system policy](system-policy.md) is set to a value greater than 0, Windows Installer saves older versions of files in a cache when a patch is applied to an application.</span></span> <span data-ttu-id="f0a3c-105">Кэширование может повысить производительность будущих установок, которые в противном случае должны получить старые файлы из исходного источника приложения.</span><span class="sxs-lookup"><span data-stu-id="f0a3c-105">Caching can increase the performance of future installations that otherwise need to obtain the old files from a original application source.</span></span>

<span data-ttu-id="f0a3c-106">Значение политики Макспатчкачесизе — это максимальный процент дискового пространства, который установщик может использовать для кэша старых файлов.</span><span class="sxs-lookup"><span data-stu-id="f0a3c-106">The value of the MaxPatchCacheSize policy is the maximum percentage of disk space that the installer can use for the cache of old files.</span></span> <span data-ttu-id="f0a3c-107">Например, значение 20 указывает, что используется не более 20%.</span><span class="sxs-lookup"><span data-stu-id="f0a3c-107">For example, a value of 20 specifies no more than 20% be used.</span></span> <span data-ttu-id="f0a3c-108">Если общий размер кэша достигает указанного процента места на диске, дополнительные файлы не сохраняются в кэше.</span><span class="sxs-lookup"><span data-stu-id="f0a3c-108">If the total size of the cache reaches the specified percentage of disk space, no additional files are saved to the cache.</span></span> <span data-ttu-id="f0a3c-109">Политика не влияет на уже сохраненные файлы.</span><span class="sxs-lookup"><span data-stu-id="f0a3c-109">The policy does not affect files that have already been saved.</span></span>

<span data-ttu-id="f0a3c-110">Если значение политики Макспатчкачесизе равно 0, дополнительные файлы не сохраняются.</span><span class="sxs-lookup"><span data-stu-id="f0a3c-110">If the value of the MaxPatchCacheSize policy is set to 0, no additional files are saved.</span></span>

<span data-ttu-id="f0a3c-111">Если политика Макспатчкачесизе не задана, по умолчанию используется значение 10, а для сохранения старых файлов можно использовать не более 10% места на диске.</span><span class="sxs-lookup"><span data-stu-id="f0a3c-111">If the MaxPatchCacheSize policy is not set, the default value is 10 and a maximum of 10% of the disk space can be used to save old files.</span></span>

## <a name="registry-key"></a><span data-ttu-id="f0a3c-112">Ключ реестра</span><span class="sxs-lookup"><span data-stu-id="f0a3c-112">Registry Key</span></span>

<span data-ttu-id="f0a3c-113">**HKey \_ \_** \\ **Политики программного обеспечения** локального компьютера \\  \\  \\  \\ **установщик** Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="f0a3c-113">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="f0a3c-114">Тип данных</span><span class="sxs-lookup"><span data-stu-id="f0a3c-114">Data Type</span></span>

<span data-ttu-id="f0a3c-115">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="f0a3c-115">**REG\_DWORD**</span></span>

## <a name="related-topics"></a><span data-ttu-id="f0a3c-116">См. также</span><span class="sxs-lookup"><span data-stu-id="f0a3c-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0a3c-117">Не поддерживается в установщик Windows 2,0 и более ранних версиях</span><span class="sxs-lookup"><span data-stu-id="f0a3c-117">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




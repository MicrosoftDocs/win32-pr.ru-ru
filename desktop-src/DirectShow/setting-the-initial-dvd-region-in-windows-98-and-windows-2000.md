---
description: Настройка начального региона DVD
ms.assetid: b8238cb4-a101-4998-866f-4cf9ebd5d277
title: Настройка начального региона DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d3f5181b804a9d83c04eed0abc70095bf9f1cf2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536443"
---
# <a name="setting-the-initial-dvd-region"></a><span data-ttu-id="42cd3-103">Настройка начального региона DVD</span><span class="sxs-lookup"><span data-stu-id="42cd3-103">Setting the Initial DVD Region</span></span>

<span data-ttu-id="42cd3-104">Изготовитель системы должен выбрать начальный регион для DVD-дисковода на своих ПК.</span><span class="sxs-lookup"><span data-stu-id="42cd3-104">It is the responsibility of the system manufacturer to select an initial DVD region for the DVD drive in their PCs.</span></span>

> [!Note]  
> <span data-ttu-id="42cd3-105">Для задания региона можно использовать только зашифрованные диски.</span><span class="sxs-lookup"><span data-stu-id="42cd3-105">Only encrypted discs can be used to set the region.</span></span>

 

### <a name="windows-2000-and-later"></a><span data-ttu-id="42cd3-106">Windows 2000 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="42cd3-106">Windows 2000 and Later</span></span>

<span data-ttu-id="42cd3-107">Начиная с Windows 2000, регион DVD по умолчанию выбирается в зависимости от языкового стандарта, для которого настроена виртуальная машина.</span><span class="sxs-lookup"><span data-stu-id="42cd3-107">Starting in Windows 2000, the default DVD region is selected based upon the locale that the machine is set up for.</span></span> <span data-ttu-id="42cd3-108">Windows 2000 всегда будет устанавливать начальный регион для DVD-дисковода, используя этот регион по умолчанию, а также регион диска, если диск находится в дисководе.</span><span class="sxs-lookup"><span data-stu-id="42cd3-108">Windows 2000 will always set the initial region for a DVD drive using this default region as well as the disc's region, if there is a disc is in the drive.</span></span> <span data-ttu-id="42cd3-109">Изготовителю системы не нужно ничего делать, чтобы задать начальный регион для DVD-дисков Windows 2000 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="42cd3-109">The system manufacturer does not have to do anything to set the initial region for Windows 2000 or later DVD drives.</span></span>

<span data-ttu-id="42cd3-110">Если на дисках RPC1 нет диска во время загрузки, то регион по умолчанию устанавливается на основе только языкового стандарта компьютера.</span><span class="sxs-lookup"><span data-stu-id="42cd3-110">For RPC1 drives, if there is no disc in the drive during boot up then the default region is set based only on the locale of the machine.</span></span> <span data-ttu-id="42cd3-111">Если во время загрузки в дисководе есть DVD-диск, регион по умолчанию выбирается в качестве региона диска, если он соответствует региону диска. в противном случае наименьший регион на диске выбирается в качестве начальной области диска.</span><span class="sxs-lookup"><span data-stu-id="42cd3-111">If there is a DVD disc in the drive during boot up, the default region is selected to be the drive's region, provided it matches a region of the disc; otherwise the lowest region on the disc is picked as the initial region of the drive.</span></span> <span data-ttu-id="42cd3-112">Пользователь (или производитель системы) имеет одно оставшееся изменение, в случае неправильного значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="42cd3-112">The user (or system manufacturer) has one remaining change allowed, in case the default was not correct.</span></span>

<span data-ttu-id="42cd3-113">Для дисков RPC2, если во время установки Windows 2000 обнаружит, что на диске не задан регион, будет предпринята попытка выбрать регион, как описано выше, но только при наличии диска в накопителе.</span><span class="sxs-lookup"><span data-stu-id="42cd3-113">For RPC2 drives, if during the setup process Windows 2000 finds that the drive does not have any region set, it will try to pick a region as above, but only if there is a disc in the drive.</span></span> <span data-ttu-id="42cd3-114">(Диски RPC1 будут выбирать регион без диска на диске).</span><span class="sxs-lookup"><span data-stu-id="42cd3-114">(RPC1 drives will choose the region without any disc in drive).</span></span> <span data-ttu-id="42cd3-115">После настройки региона для дисков RPC2 он не изменяется при повторной установке или чистой установке операционной системы.</span><span class="sxs-lookup"><span data-stu-id="42cd3-115">Once a region is set for RPC2 drives, it is not auto-changed by either a re-installation or a clean installation of the Operating System.</span></span>

<span data-ttu-id="42cd3-116">Изготовитель оборудования может задать раздел реестра, содержащий регион DVD-диска по умолчанию для системы.</span><span class="sxs-lookup"><span data-stu-id="42cd3-116">The OEM can set a registry key containing the default DVD region for the system.</span></span> <span data-ttu-id="42cd3-117">При первой загрузке для региона диска будет задано это значение.</span><span class="sxs-lookup"><span data-stu-id="42cd3-117">On first boot, the drive region will be set to this value.</span></span> <span data-ttu-id="42cd3-118">Раздел реестра в Windows 2000 и более поздней версии — HKLM \\ System \\ CurrentControlSet \\ Control \\ класс \\ <CDROM GUID> \\ <instance number> \\ дефаултдвдрегион (Binary).</span><span class="sxs-lookup"><span data-stu-id="42cd3-118">The registry key on Windows 2000 and later is HKLM\\System\\CurrentControlSet\\Control\\Class\\<CDROM GUID>\\ <instance number>\\DefaultDVDRegion(binary) .</span></span>

## <a name="related-topics"></a><span data-ttu-id="42cd3-119">См. также</span><span class="sxs-lookup"><span data-stu-id="42cd3-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42cd3-120">Поддержка смены региона DVD в Windows</span><span class="sxs-lookup"><span data-stu-id="42cd3-120">DVD Region Change Support in Windows</span></span>](dvd-region-change-support-in-windows.md)
</dt> </dl>

 

 




---
description: Источники сведений о регионе DVD
ms.assetid: f4874aa7-c58a-49a3-9474-c621cc19156b
title: Источники сведений о регионе DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ac426f995323bfd30d3430dccb4044c5f71a119
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998929"
---
# <a name="sources-of-dvd-region-information"></a><span data-ttu-id="c193a-103">Источники сведений о регионе DVD</span><span class="sxs-lookup"><span data-stu-id="c193a-103">Sources of DVD Region Information</span></span>

<span data-ttu-id="c193a-104">Существует три источника информации о регионе DVD, которые позволяют определить регион для воспроизведения DVD на компьютере под управлением Windows.</span><span class="sxs-lookup"><span data-stu-id="c193a-104">There are three sources of DVD region information that work together to determine the region for DVD playback on a Windows PC.</span></span>

-   <span data-ttu-id="c193a-105">Название DVD-диска.</span><span class="sxs-lookup"><span data-stu-id="c193a-105">DVD Title.</span></span> <span data-ttu-id="c193a-106">Большинство заголовков DVD-дисков отмечены для определенного региона.</span><span class="sxs-lookup"><span data-stu-id="c193a-106">Most DVD titles are marked for a specific region.</span></span> <span data-ttu-id="c193a-107">Некоторые заголовки можно воспроизводить только в одном регионе. Некоторые из них можно воспроизвести в нескольких регионах, а другие могут играть все регионы.</span><span class="sxs-lookup"><span data-stu-id="c193a-107">Some titles can be played in only one region, some can be played in multiple regions, and others can be played all regions.</span></span> <span data-ttu-id="c193a-108">Регионы с 1 по 6 были определены в исходной спецификации DVD-Video.</span><span class="sxs-lookup"><span data-stu-id="c193a-108">Regions 1 through 6 were defined in the original DVD-Video specification.</span></span> <span data-ttu-id="c193a-109">Регион 7 в настоящее время не определен.</span><span class="sxs-lookup"><span data-stu-id="c193a-109">Region 7 is currently undefined.</span></span> <span data-ttu-id="c193a-110">Регион 8 был добавлен в 1999 для специальных мест, например в самолете.</span><span class="sxs-lookup"><span data-stu-id="c193a-110">Region 8 was added in 1999 for special venues, such as airplanes.</span></span> <span data-ttu-id="c193a-111">Диски DVD-ROM (без видеозоны) не должны содержать код региона.</span><span class="sxs-lookup"><span data-stu-id="c193a-111">DVD-ROM discs (those with no video zone) should not contain any region coding.</span></span>
-   <span data-ttu-id="c193a-112">Дисковод DVD-дисков.</span><span class="sxs-lookup"><span data-stu-id="c193a-112">DVD-ROM Drive.</span></span> <span data-ttu-id="c193a-113">Существует два типа дисководов DVD-дисков: RPC Phase 1 (RPC1) и RPC Phase 2 (RPC2).</span><span class="sxs-lookup"><span data-stu-id="c193a-113">There are two types of DVD-ROM drives: RPC Phase 1 (RPC1) drives and RPC Phase 2 (RPC2) drives.</span></span> <span data-ttu-id="c193a-114">Диски RPC1 не поддерживают встроенную аппаратную поддержку для управления регионами.</span><span class="sxs-lookup"><span data-stu-id="c193a-114">RPC1 drives do not have built-in hardware support for region management.</span></span> <span data-ttu-id="c193a-115">Для этих дисков Windows хранит сведения о количестве изменений в регионе, и регион можно изменить только один раз.</span><span class="sxs-lookup"><span data-stu-id="c193a-115">For these drives, Windows maintains the region change count information and the region can be changed only once.</span></span> <span data-ttu-id="c193a-116">RPC2 диски сохраняют сведения о количестве изменений в регионе на оборудовании, а общий регион таких дисков можно изменить до 5 раз.</span><span class="sxs-lookup"><span data-stu-id="c193a-116">RPC2 drives maintain the region change count information in hardware and in general the region of such drives can be changed up to 5 times.</span></span>
-   <span data-ttu-id="c193a-117">DVD-декодер.</span><span class="sxs-lookup"><span data-stu-id="c193a-117">DVD Decoder.</span></span> <span data-ttu-id="c193a-118">Некоторые декодеры DVD, оборудование или программное обеспечение задаются для определенного региона.</span><span class="sxs-lookup"><span data-stu-id="c193a-118">Some DVD decoders, hardware or software, are set for a specific region.</span></span> <span data-ttu-id="c193a-119">Как правило, пользователь не может изменить регион декодера.</span><span class="sxs-lookup"><span data-stu-id="c193a-119">In general, the user cannot change the decoder's region.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c193a-120">См. также</span><span class="sxs-lookup"><span data-stu-id="c193a-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c193a-121">Поддержка смены региона DVD в Windows</span><span class="sxs-lookup"><span data-stu-id="c193a-121">DVD Region Change Support in Windows</span></span>](dvd-region-change-support-in-windows.md)
</dt> </dl>

 

 




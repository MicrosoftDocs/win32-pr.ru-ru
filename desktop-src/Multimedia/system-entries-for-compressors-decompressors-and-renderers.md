---
title: Системные записи для сжатия, декомпрессоров и модулей подготовки отчетов
description: Системные записи для сжатия, декомпрессоров и модулей подготовки отчетов
ms.assetid: b27bbd5b-a218-49bb-b179-b24ce39869a1
keywords:
- Видео для Windows (VFW), системные записи программы сжатия
- VFW (видео для Windows), системные записи программы сжатия
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b46d9c6fd8974511698bcb687c580e68be3757ee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778836"
---
# <a name="system-entries-for-compressors-decompressors-and-renderers"></a><span data-ttu-id="76bce-105">Системные записи для сжатия, декомпрессоров и модулей подготовки отчетов</span><span class="sxs-lookup"><span data-stu-id="76bce-105">System Entries for Compressors, Decompressors, and Renderers</span></span>

<span data-ttu-id="76bce-106">Система использует записи в реестре для поиска драйверов ВКМ.</span><span class="sxs-lookup"><span data-stu-id="76bce-106">The system uses entries in the registry to find VCM drivers.</span></span> <span data-ttu-id="76bce-107">Эти записи представлены в виде кодов символов 2 4, разделенных точкой.</span><span class="sxs-lookup"><span data-stu-id="76bce-107">These entries are in the form of two four-character codes separated by a period.</span></span> <span data-ttu-id="76bce-108">Первый код из четырех символов определяется системой и может быть одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="76bce-108">The first four-character code is defined by the system and can be one of the following:</span></span>



| <span data-ttu-id="76bce-109">Код из четырех символов</span><span class="sxs-lookup"><span data-stu-id="76bce-109">Four-character code</span></span> | <span data-ttu-id="76bce-110">Описание</span><span class="sxs-lookup"><span data-stu-id="76bce-110">Description</span></span>                               |
|---------------------|-------------------------------------------|
| <span data-ttu-id="76bce-111">VIDC</span><span class="sxs-lookup"><span data-stu-id="76bce-111">"VIDC"</span></span>              | <span data-ttu-id="76bce-112">Обозначает программы сжатия и Декомпрессоры.</span><span class="sxs-lookup"><span data-stu-id="76bce-112">Identifies compressors and decompressors.</span></span> |
| <span data-ttu-id="76bce-113">НАПРЯЖЕНИЯ</span><span class="sxs-lookup"><span data-stu-id="76bce-113">"VIDS"</span></span>              | <span data-ttu-id="76bce-114">Определяет модули подготовки видео-потоков.</span><span class="sxs-lookup"><span data-stu-id="76bce-114">Identifies video-stream renderers.</span></span>        |
| <span data-ttu-id="76bce-115">"ТКСТС"</span><span class="sxs-lookup"><span data-stu-id="76bce-115">"TXTS"</span></span>              | <span data-ttu-id="76bce-116">Определяет модули подготовки текстового потока.</span><span class="sxs-lookup"><span data-stu-id="76bce-116">Identifies text-stream renderers.</span></span>         |
| <span data-ttu-id="76bce-117">"АУДС"</span><span class="sxs-lookup"><span data-stu-id="76bce-117">"AUDS"</span></span>              | <span data-ttu-id="76bce-118">Идентифицирует обработчики аудио-потоков.</span><span class="sxs-lookup"><span data-stu-id="76bce-118">Identifies audio-stream handlers.</span></span>         |



 

<span data-ttu-id="76bce-119">Пользовательские модули подготовки отчетов могут определять собственные коды из четырех символов.</span><span class="sxs-lookup"><span data-stu-id="76bce-119">Custom renderers can define their own four-character codes.</span></span>

<span data-ttu-id="76bce-120">Второй код из четырех символов определяется драйвером.</span><span class="sxs-lookup"><span data-stu-id="76bce-120">The second four-character code is defined by the driver.</span></span> <span data-ttu-id="76bce-121">Как правило, второй код из четырех символов соответствует типу данных, которые могут быть обработаны драйвером.</span><span class="sxs-lookup"><span data-stu-id="76bce-121">Typically, the second four-character code corresponds to the type of data the driver can handle.</span></span>

<span data-ttu-id="76bce-122">При открытии драйвера ВКМ приложение определяет тип драйвера и тип необходимого обработчика данных.</span><span class="sxs-lookup"><span data-stu-id="76bce-122">When opening a VCM driver, an application specifies the type of driver and the type of data handler it needs.</span></span> <span data-ttu-id="76bce-123">Как правило, эти сведения поступают из заголовка потока.</span><span class="sxs-lookup"><span data-stu-id="76bce-123">Typically, this information comes from the stream header.</span></span> <span data-ttu-id="76bce-124">Система пытается открыть указанный обработчик данных, но если он завершается неудачно, система выполняет поиск драйвера с требуемым обработчиком в реестре.</span><span class="sxs-lookup"><span data-stu-id="76bce-124">The system tries to open the specified data handler, but if it fails, the system searches the registry for a driver that has the required handler.</span></span>

<span data-ttu-id="76bce-125">При поиске драйвера система пытается сопоставить коды из четырех символов, указанных для типа драйвера и обработчика данных, с указанными в записи драйвера.</span><span class="sxs-lookup"><span data-stu-id="76bce-125">When searching for the driver, the system tries to match the four-character codes specified for the driver type and data handler with those specified in the driver entry.</span></span> <span data-ttu-id="76bce-126">Например, если приложение указывает программу сжатия МССК, система выполняет поиск записи Driver в реестре VIDC. МССК.</span><span class="sxs-lookup"><span data-stu-id="76bce-126">For example, if an application specifies the compressor MSSQ, the system searches the registry for the driver entry VIDC.MSSQ.</span></span> <span data-ttu-id="76bce-127">Если не удается найти совпадение, открывается каждый драйвер, соответствующий типу драйвера, и определяется тип данных, который может обработано приложением.</span><span class="sxs-lookup"><span data-stu-id="76bce-127">If it cannot find a match, it opens each driver corresponding to the driver type and locates one that can handle the type of data your application specifies.</span></span> <span data-ttu-id="76bce-128">В предыдущем примере, если система не смогла найти VIDC. МССК, она откроет все драйверы с кодом "VIDC" с четырьмя символами и найдет один из них, который может справиться с данными.</span><span class="sxs-lookup"><span data-stu-id="76bce-128">In the previous example, if the system could not find VIDC.MSSQ, it would open all drivers with the "VIDC" four-character code and locate one that can handle the data.</span></span>

 

 





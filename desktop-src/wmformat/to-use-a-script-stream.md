---
title: Использование потока скрипта
description: Использование потока скрипта
ms.assetid: 502b1f66-213d-41d8-992a-9bef4f6209f9
keywords:
- Пакет Windows Media Format SDK, скриптовые потоки
- Расширенный системный формат (ASF), скриптовые потоки
- ASF (Расширенный системный формат), скриптовые потоки
- потоки скриптов, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82dee2c4a9789406c21b18c58a5f281a768fc713
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332555"
---
# <a name="to-use-a-script-stream"></a><span data-ttu-id="6190d-107">Использование потока скрипта</span><span class="sxs-lookup"><span data-stu-id="6190d-107">To Use a Script Stream</span></span>

<span data-ttu-id="6190d-108">В этом разделе описывается отправка данных скрипта в модуль записи для включения в файл.</span><span class="sxs-lookup"><span data-stu-id="6190d-108">This section describes how to send script data to the writer for inclusion in a file.</span></span> <span data-ttu-id="6190d-109">Дополнительные сведения о включении в профили потоков скриптов см. в разделе [Настройка произвольных типов потоков](configuring-arbitrary-stream-types.md).</span><span class="sxs-lookup"><span data-stu-id="6190d-109">For information about including script streams in profiles, see [Configuring Arbitrary Stream Types](configuring-arbitrary-stream-types.md).</span></span>

<span data-ttu-id="6190d-110">Каждый скрипт состоит из двух строк: строки *типа* и строки *аргумента* .</span><span class="sxs-lookup"><span data-stu-id="6190d-110">Each script consists of two strings, a *type* string and an *argument* string.</span></span>

<span data-ttu-id="6190d-111">Перед отправкой в модуль записи необходимо отформатировать данные скрипта.</span><span class="sxs-lookup"><span data-stu-id="6190d-111">The script data must be formatted before it is sent to the writer.</span></span> <span data-ttu-id="6190d-112">Строки должны быть объединены, разделены символом **null** и заканчиваться символом **null** .</span><span class="sxs-lookup"><span data-stu-id="6190d-112">The strings should be concatenated, separated by a **NULL** character, and terminated with a **NULL** character.</span></span> <span data-ttu-id="6190d-113">В следующем примере показан законный сценарий:</span><span class="sxs-lookup"><span data-stu-id="6190d-113">The following example shows a legitimate script:</span></span>



|     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| <span data-ttu-id="6190d-114">U</span><span class="sxs-lookup"><span data-stu-id="6190d-114">U</span></span>   | <span data-ttu-id="6190d-115">R</span><span class="sxs-lookup"><span data-stu-id="6190d-115">R</span></span>   | <span data-ttu-id="6190d-116">L</span><span class="sxs-lookup"><span data-stu-id="6190d-116">L</span></span>   | <span data-ttu-id="6190d-117">\\0</span><span class="sxs-lookup"><span data-stu-id="6190d-117">\\0</span></span> | <span data-ttu-id="6190d-118">h</span><span class="sxs-lookup"><span data-stu-id="6190d-118">h</span></span>   | <span data-ttu-id="6190d-119">t</span><span class="sxs-lookup"><span data-stu-id="6190d-119">t</span></span>   | <span data-ttu-id="6190d-120">t</span><span class="sxs-lookup"><span data-stu-id="6190d-120">t</span></span>   | <span data-ttu-id="6190d-121">p</span><span class="sxs-lookup"><span data-stu-id="6190d-121">p</span></span>   | <span data-ttu-id="6190d-122">:</span><span class="sxs-lookup"><span data-stu-id="6190d-122">:</span></span>   | /   | /   | <span data-ttu-id="6190d-123">w</span><span class="sxs-lookup"><span data-stu-id="6190d-123">w</span></span>   | <span data-ttu-id="6190d-124">w</span><span class="sxs-lookup"><span data-stu-id="6190d-124">w</span></span>   | <span data-ttu-id="6190d-125">w</span><span class="sxs-lookup"><span data-stu-id="6190d-125">w</span></span>   | <span data-ttu-id="6190d-126">.</span><span class="sxs-lookup"><span data-stu-id="6190d-126">.</span></span>   | <span data-ttu-id="6190d-127">а</span><span class="sxs-lookup"><span data-stu-id="6190d-127">a</span></span>   | <span data-ttu-id="6190d-128">d</span><span class="sxs-lookup"><span data-stu-id="6190d-128">d</span></span>   | <span data-ttu-id="6190d-129">а</span><span class="sxs-lookup"><span data-stu-id="6190d-129">a</span></span>   | <span data-ttu-id="6190d-130">t</span><span class="sxs-lookup"><span data-stu-id="6190d-130">t</span></span>   | <span data-ttu-id="6190d-131">u</span><span class="sxs-lookup"><span data-stu-id="6190d-131">u</span></span>   | <span data-ttu-id="6190d-132">m</span><span class="sxs-lookup"><span data-stu-id="6190d-132">m</span></span>   | <span data-ttu-id="6190d-133">.</span><span class="sxs-lookup"><span data-stu-id="6190d-133">.</span></span>   | <span data-ttu-id="6190d-134">c</span><span class="sxs-lookup"><span data-stu-id="6190d-134">c</span></span>   | <span data-ttu-id="6190d-135">o</span><span class="sxs-lookup"><span data-stu-id="6190d-135">o</span></span>   | <span data-ttu-id="6190d-136">m</span><span class="sxs-lookup"><span data-stu-id="6190d-136">m</span></span>   | <span data-ttu-id="6190d-137">\\0</span><span class="sxs-lookup"><span data-stu-id="6190d-137">\\0</span></span> |



 

<span data-ttu-id="6190d-138">Каждая пара команд сценария должна быть написана как образец для модуля записи.</span><span class="sxs-lookup"><span data-stu-id="6190d-138">Each pair of script commands should be written as a sample to the writer.</span></span> <span data-ttu-id="6190d-139">Дополнительные сведения о написании образцов см. [в разделе Создание образцов](to-write-samples.md).</span><span class="sxs-lookup"><span data-stu-id="6190d-139">For more information about writing samples, see [To Write Samples](to-write-samples.md).</span></span>

<span data-ttu-id="6190d-140">При воспроизведении ASF-файла команды сценария будут доставляться модулем чтения (или синхронным средством чтения) в порядке времени презентации.</span><span class="sxs-lookup"><span data-stu-id="6190d-140">When the ASF file is played, the script commands will be delivered by the reader (or synchronous reader) in presentation time order.</span></span> <span data-ttu-id="6190d-141">Приложение может проанализировать две строки и ответить на команду скрипта.</span><span class="sxs-lookup"><span data-stu-id="6190d-141">It is the responsibility of the application to parse the two strings and respond to the script command.</span></span>

> [!Note]  
> <span data-ttu-id="6190d-142">При использовании DRM для шифрования файла ни одна из команд сценария не может иметь время презентации, равное 0.</span><span class="sxs-lookup"><span data-stu-id="6190d-142">When using DRM to encrypt a file, no script command can have a presentation time of 0.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="6190d-143">См. также</span><span class="sxs-lookup"><span data-stu-id="6190d-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6190d-144">**Использование команд сценария**</span><span class="sxs-lookup"><span data-stu-id="6190d-144">**Using Script Commands**</span></span>](using-script-commands.md)
</dt> </dl>

 

 





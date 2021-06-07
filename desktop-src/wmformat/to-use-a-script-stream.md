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
ms.openlocfilehash: 09782855bd3000d711f134c5889733e49e020c44
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444735"
---
# <a name="to-use-a-script-stream"></a><span data-ttu-id="e699a-107">Использование потока скрипта</span><span class="sxs-lookup"><span data-stu-id="e699a-107">To Use a Script Stream</span></span>

<span data-ttu-id="e699a-108">В этом разделе описывается отправка данных скрипта в модуль записи для включения в файл.</span><span class="sxs-lookup"><span data-stu-id="e699a-108">This section describes how to send script data to the writer for inclusion in a file.</span></span> <span data-ttu-id="e699a-109">Дополнительные сведения о включении в профили потоков скриптов см. в разделе [Настройка произвольных типов потоков](configuring-arbitrary-stream-types.md).</span><span class="sxs-lookup"><span data-stu-id="e699a-109">For information about including script streams in profiles, see [Configuring Arbitrary Stream Types](configuring-arbitrary-stream-types.md).</span></span>

<span data-ttu-id="e699a-110">Каждый скрипт состоит из двух строк: строки *типа* и строки *аргумента* .</span><span class="sxs-lookup"><span data-stu-id="e699a-110">Each script consists of two strings, a *type* string and an *argument* string.</span></span>

<span data-ttu-id="e699a-111">Перед отправкой в модуль записи необходимо отформатировать данные скрипта.</span><span class="sxs-lookup"><span data-stu-id="e699a-111">The script data must be formatted before it is sent to the writer.</span></span> <span data-ttu-id="e699a-112">Строки должны быть объединены, разделены символом **null** и заканчиваться символом **null** .</span><span class="sxs-lookup"><span data-stu-id="e699a-112">The strings should be concatenated, separated by a **NULL** character, and terminated with a **NULL** character.</span></span> <span data-ttu-id="e699a-113">В следующем примере показан законный сценарий:</span><span class="sxs-lookup"><span data-stu-id="e699a-113">The following example shows a legitimate script:</span></span>



| &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; |   &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp;  | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp;  | &nbsp; |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| <span data-ttu-id="e699a-114">U</span><span class="sxs-lookup"><span data-stu-id="e699a-114">U</span></span>   | <span data-ttu-id="e699a-115">R</span><span class="sxs-lookup"><span data-stu-id="e699a-115">R</span></span>   | <span data-ttu-id="e699a-116">L</span><span class="sxs-lookup"><span data-stu-id="e699a-116">L</span></span>   | &nbsp; | <span data-ttu-id="e699a-117">h</span><span class="sxs-lookup"><span data-stu-id="e699a-117">h</span></span>   | <span data-ttu-id="e699a-118">t</span><span class="sxs-lookup"><span data-stu-id="e699a-118">t</span></span>   | <span data-ttu-id="e699a-119">t</span><span class="sxs-lookup"><span data-stu-id="e699a-119">t</span></span>   | <span data-ttu-id="e699a-120">p</span><span class="sxs-lookup"><span data-stu-id="e699a-120">p</span></span>   | <span data-ttu-id="e699a-121">:</span><span class="sxs-lookup"><span data-stu-id="e699a-121">:</span></span>   | /   | /   | <span data-ttu-id="e699a-122">w</span><span class="sxs-lookup"><span data-stu-id="e699a-122">w</span></span>   | <span data-ttu-id="e699a-123">w</span><span class="sxs-lookup"><span data-stu-id="e699a-123">w</span></span>   | <span data-ttu-id="e699a-124">w</span><span class="sxs-lookup"><span data-stu-id="e699a-124">w</span></span>   | <span data-ttu-id="e699a-125">.</span><span class="sxs-lookup"><span data-stu-id="e699a-125">.</span></span>   | <span data-ttu-id="e699a-126">а</span><span class="sxs-lookup"><span data-stu-id="e699a-126">a</span></span>   | <span data-ttu-id="e699a-127">d</span><span class="sxs-lookup"><span data-stu-id="e699a-127">d</span></span>   | <span data-ttu-id="e699a-128">а</span><span class="sxs-lookup"><span data-stu-id="e699a-128">a</span></span>   | <span data-ttu-id="e699a-129">t</span><span class="sxs-lookup"><span data-stu-id="e699a-129">t</span></span>   | <span data-ttu-id="e699a-130">u</span><span class="sxs-lookup"><span data-stu-id="e699a-130">u</span></span>   | <span data-ttu-id="e699a-131">М</span><span class="sxs-lookup"><span data-stu-id="e699a-131">m</span></span>   | <span data-ttu-id="e699a-132">.</span><span class="sxs-lookup"><span data-stu-id="e699a-132">.</span></span>   | <span data-ttu-id="e699a-133">с</span><span class="sxs-lookup"><span data-stu-id="e699a-133">c</span></span>   | <span data-ttu-id="e699a-134">o</span><span class="sxs-lookup"><span data-stu-id="e699a-134">o</span></span>   | <span data-ttu-id="e699a-135">М</span><span class="sxs-lookup"><span data-stu-id="e699a-135">m</span></span>   | &nbsp; |



 

<span data-ttu-id="e699a-136">Каждая пара команд сценария должна быть написана как образец для модуля записи.</span><span class="sxs-lookup"><span data-stu-id="e699a-136">Each pair of script commands should be written as a sample to the writer.</span></span> <span data-ttu-id="e699a-137">Дополнительные сведения о написании образцов см. [в разделе Создание образцов](to-write-samples.md).</span><span class="sxs-lookup"><span data-stu-id="e699a-137">For more information about writing samples, see [To Write Samples](to-write-samples.md).</span></span>

<span data-ttu-id="e699a-138">При воспроизведении ASF-файла команды сценария будут доставляться модулем чтения (или синхронным средством чтения) в порядке времени презентации.</span><span class="sxs-lookup"><span data-stu-id="e699a-138">When the ASF file is played, the script commands will be delivered by the reader (or synchronous reader) in presentation time order.</span></span> <span data-ttu-id="e699a-139">Приложение может проанализировать две строки и ответить на команду скрипта.</span><span class="sxs-lookup"><span data-stu-id="e699a-139">It is the responsibility of the application to parse the two strings and respond to the script command.</span></span>

> [!Note]  
> <span data-ttu-id="e699a-140">При использовании DRM для шифрования файла ни одна из команд сценария не может иметь время презентации, равное 0.</span><span class="sxs-lookup"><span data-stu-id="e699a-140">When using DRM to encrypt a file, no script command can have a presentation time of 0.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="e699a-141">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="e699a-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e699a-142">**Использование команд сценария**</span><span class="sxs-lookup"><span data-stu-id="e699a-142">**Using Script Commands**</span></span>](using-script-commands.md)
</dt> </dl>

 

 





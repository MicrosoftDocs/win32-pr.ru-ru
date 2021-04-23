---
description: Средство logman можно использовать для получения сведений трассировки для приложений VSS, использующих автоматическое восстановление системы (ASR).
ms.assetid: 872609c8-a123-40a8-96ca-58f34d37f3d8
title: Использование средств трассировки с приложениями ASR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c13eee1c62cd6636eebe5bcfd35bd5abb119645
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692393"
---
# <a name="using-tracing-tools-with-asr-applications"></a><span data-ttu-id="165f6-103">Использование средств трассировки с приложениями ASR</span><span class="sxs-lookup"><span data-stu-id="165f6-103">Using Tracing Tools with ASR Applications</span></span>

<span data-ttu-id="165f6-104">Средство logman можно использовать для получения сведений трассировки для приложений VSS, использующих [Автоматическое восстановление системы (ASR)](using-vss-automated-system-recovery-for-disaster-recovery.md).</span><span class="sxs-lookup"><span data-stu-id="165f6-104">You can use the Logman tool to collect tracing information for VSS applications that use [Automated System Recovery (ASR)](using-vss-automated-system-recovery-for-disaster-recovery.md).</span></span> <span data-ttu-id="165f6-105">Logman (logman.exe) — это контроллер трассировки для событий трассировки и счетчиков производительности.</span><span class="sxs-lookup"><span data-stu-id="165f6-105">Logman (logman.exe) is a trace controller for trace events and performance counters.</span></span> <span data-ttu-id="165f6-106">Он входит в состав Windows XP и более поздних версий Windows.</span><span class="sxs-lookup"><span data-stu-id="165f6-106">It is included in Windows XP and later versions of Windows.</span></span> <span data-ttu-id="165f6-107">Или, при желании, можно использовать средство tracelog для получения одних и тех же данных трассировки ASR.</span><span class="sxs-lookup"><span data-stu-id="165f6-107">Or, if you prefer, you can use the Tracelog tool to collect the same ASR tracing information.</span></span> <span data-ttu-id="165f6-108">Tracelog входит в комплект драйверов Windows (WDK).</span><span class="sxs-lookup"><span data-stu-id="165f6-108">Tracelog is included in the Windows Driver Kit (WDK).</span></span>

<span data-ttu-id="165f6-109">Сведения об использовании средств трассировки с VSS см. в статье [использование средств трассировки с помощью VSS](using-tracing-tools-with-vss.md).</span><span class="sxs-lookup"><span data-stu-id="165f6-109">To use tracing tools with VSS, see [Using Tracing Tools with VSS](using-tracing-tools-with-vss.md).</span></span>

## <a name="using-logman"></a><span data-ttu-id="165f6-110">Использование программы Logman</span><span class="sxs-lookup"><span data-stu-id="165f6-110">Using Logman</span></span>

<span data-ttu-id="165f6-111">В следующей процедуре описывается использование программы Logman с приложением ASR.</span><span class="sxs-lookup"><span data-stu-id="165f6-111">The following procedure describes how to use Logman with your ASR application.</span></span>

<span data-ttu-id="165f6-112">**Использование программы Logman с приложением ASR**</span><span class="sxs-lookup"><span data-stu-id="165f6-112">**To use Logman with your ASR application**</span></span>

1.  <span data-ttu-id="165f6-113">Чтобы начать трассировку, используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="165f6-113">Use the following command to start tracing:</span></span>

    <span data-ttu-id="165f6-114">**Logman Start ASR-o** *x: \\ \* \* \* ASR. ETL-ETS-p {6407345b-94f2-44c8-b3db-4e076be46816} 0xFF 0xFF*\*</span><span class="sxs-lookup"><span data-stu-id="165f6-114">**logman start asr -o** *x:\\*\*\*asr.etl -ets -p {6407345b-94f2-44c8-b3db-4e076be46816} 0xff 0xff*\*</span></span>

    > [!Note]  
    > <span data-ttu-id="165f6-115">Замените "x: \\ " на путь к каталогу, в котором должен храниться файл журнала трассировки.</span><span class="sxs-lookup"><span data-stu-id="165f6-115">Replace "x:\\" with the path to the directory where you would like the trace log file to be stored.</span></span> <span data-ttu-id="165f6-116">Для лучшей производительности файл журнала трассировки должен находиться на томе, который не является частью теневой копии.</span><span class="sxs-lookup"><span data-stu-id="165f6-116">For best performance, the trace log file should be located on a volume that is not part of the shadow copy.</span></span>

     

2.  <span data-ttu-id="165f6-117">Чтобы прерывать трассировку, используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="165f6-117">Use the following command to stop tracing:</span></span>

    <span data-ttu-id="165f6-118">**средство logman останавливает ASR-ETS**</span><span class="sxs-lookup"><span data-stu-id="165f6-118">**logman stop asr -ets**</span></span>

<span data-ttu-id="165f6-119">Файл журнала трассировки — *x: \\* ASR. ETL.</span><span class="sxs-lookup"><span data-stu-id="165f6-119">The trace log file is *x:\\* asr.etl.</span></span>

<span data-ttu-id="165f6-120">Дополнительные сведения о средстве Logman см. в разделе [Logman](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc753820(v=ws.11)).</span><span class="sxs-lookup"><span data-stu-id="165f6-120">For more information about the Logman tool, see [Logman](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc753820(v=ws.11)).</span></span>

## <a name="using-tracelog"></a><span data-ttu-id="165f6-121">Использование tracelog</span><span class="sxs-lookup"><span data-stu-id="165f6-121">Using Tracelog</span></span>

<span data-ttu-id="165f6-122">В следующей процедуре описывается использование tracelog.</span><span class="sxs-lookup"><span data-stu-id="165f6-122">The following procedure describes how to use Tracelog.</span></span>

<span data-ttu-id="165f6-123">**Использование tracelog**</span><span class="sxs-lookup"><span data-stu-id="165f6-123">**To use Tracelog**</span></span>

1.  <span data-ttu-id="165f6-124">Создайте текстовый файл с именем ASR. CTL, который содержит только следующий текст:</span><span class="sxs-lookup"><span data-stu-id="165f6-124">Create a text file named asr.ctl that contains only the following text:</span></span>

    <span data-ttu-id="165f6-125">**6407345b-94f2-44c8-b3db-4e076be46816 ASR**</span><span class="sxs-lookup"><span data-stu-id="165f6-125">**6407345b-94f2-44c8-b3db-4e076be46816 asr**</span></span>

2.  <span data-ttu-id="165f6-126">Чтобы начать трассировку, используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="165f6-126">Use the following command to start tracing:</span></span>

    <span data-ttu-id="165f6-127">**tracelog-Start ASR-f** *x: \\ \* \* \* ASR. ETL-GUID ASR. CTL-флаг 0xFF-Level 0xFF*\*</span><span class="sxs-lookup"><span data-stu-id="165f6-127">**tracelog -start asr -f** *x:\\*\*\*asr.etl -guid asr.ctl -flag 0xff -level 0xff*\*</span></span>

    > [!Note]  
    > <span data-ttu-id="165f6-128">Замените "x: \\ " на путь к каталогу, в котором должен храниться файл журнала трассировки.</span><span class="sxs-lookup"><span data-stu-id="165f6-128">Replace "x:\\" with the path to the directory where you would like the trace log file to be stored.</span></span> <span data-ttu-id="165f6-129">Для лучшей производительности файл журнала трассировки должен находиться на томе, который не является частью теневой копии.</span><span class="sxs-lookup"><span data-stu-id="165f6-129">For best performance, the trace log file should be located on a volume that is not part of the shadow copy.</span></span>

     

3.  <span data-ttu-id="165f6-130">Чтобы прерывать трассировку, используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="165f6-130">Use the following command to stop tracing:</span></span>

    <span data-ttu-id="165f6-131">**tracelog — завершение ASR**</span><span class="sxs-lookup"><span data-stu-id="165f6-131">**tracelog -stop asr**</span></span>

<span data-ttu-id="165f6-132">Файл журнала трассировки — *x: \\* ASR. ETL.</span><span class="sxs-lookup"><span data-stu-id="165f6-132">The trace log file is *x:\\* asr.etl.</span></span>

<span data-ttu-id="165f6-133">Дополнительные сведения о средстве tracelog см. в разделе [tracelog](https://msdn.microsoft.com/library/ms797927.aspx).</span><span class="sxs-lookup"><span data-stu-id="165f6-133">For more information about the Tracelog tool, see [Tracelog](https://msdn.microsoft.com/library/ms797927.aspx).</span></span>

 

 

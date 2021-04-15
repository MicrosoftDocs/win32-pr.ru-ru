---
description: Добавление источника
ms.assetid: 8c5d1050-a696-4a5d-be68-806420d0cd78
title: Добавление источника
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee583cd8971c183f2e03b92f68e2d6ba555c41db
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105655609"
---
# <a name="adding-a-source"></a><span data-ttu-id="b6132-103">Добавление источника</span><span class="sxs-lookup"><span data-stu-id="b6132-103">Adding a Source</span></span>

<span data-ttu-id="b6132-104">\[Этот API не поддерживается и может быть изменен или недоступен в будущем.\]</span><span class="sxs-lookup"><span data-stu-id="b6132-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="b6132-105">Создайте исходный объект так же, как вы создаете другие объекты временной шкалы.</span><span class="sxs-lookup"><span data-stu-id="b6132-105">Create a source object the same way you create other timeline objects.</span></span> <span data-ttu-id="b6132-106">Однако перед вставкой его на временную шкалу необходимо указать по крайней мере следующие свойства источника.</span><span class="sxs-lookup"><span data-stu-id="b6132-106">Before inserting it into the timeline, however, you must specify at least the following properties on the source.</span></span>

-   <span data-ttu-id="b6132-107">Время начала и окончания работы относительно временной шкалы.</span><span class="sxs-lookup"><span data-stu-id="b6132-107">The start and stop times, relative to the timeline.</span></span> <span data-ttu-id="b6132-108">Вызовите метод [**иамтимелинеобж:: сетстартстоп**](iamtimelineobj-setstartstop.md) .</span><span class="sxs-lookup"><span data-stu-id="b6132-108">Call the [**IAMTimelineObj::SetStartStop**](iamtimelineobj-setstartstop.md) method.</span></span>
-   <span data-ttu-id="b6132-109">Файл мультимедиа, используемый в качестве источника.</span><span class="sxs-lookup"><span data-stu-id="b6132-109">The media file to use as a source.</span></span> <span data-ttu-id="b6132-110">Вызовите метод [**иамтимелинесрк:: сетмедианаме**](iamtimelinesrc-setmedianame.md) со строкой расширенных символов, представляющей имя файла.</span><span class="sxs-lookup"><span data-stu-id="b6132-110">Call the [**IAMTimelineSrc::SetMediaName**](iamtimelinesrc-setmedianame.md) method with a wide-character string representing the name of the file.</span></span>
-   <span data-ttu-id="b6132-111">Время начала и окончания воспроизведения, заданное относительно исходного файла.</span><span class="sxs-lookup"><span data-stu-id="b6132-111">The media start and stop times, which are relative to the original file.</span></span> <span data-ttu-id="b6132-112">Вызовите метод [**иамтимелинесрк:: сетмедиатимес**](iamtimelinesrc-setmediatimes.md) .</span><span class="sxs-lookup"><span data-stu-id="b6132-112">Call the [**IAMTimelineSrc::SetMediaTimes**](iamtimelinesrc-setmediatimes.md) method.</span></span> <span data-ttu-id="b6132-113">Дополнительные сведения о времени мультимедиа см. [в разделе время в службах редактирования DirectShow](time-in-directshow-editing-services.md).</span><span class="sxs-lookup"><span data-stu-id="b6132-113">For more information about media times, see [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).</span></span>

<span data-ttu-id="b6132-114">В следующем примере исходный ролик запускается в файл в четыре секунды.</span><span class="sxs-lookup"><span data-stu-id="b6132-114">In the following example, the source clip starts four seconds into the file.</span></span> <span data-ttu-id="b6132-115">Длительность носителя составляет 10 секунд, вдвое больше, чем длительность длительности временной шкалы. Это означает, что источник воспроизводится с удвоенной обычной скоростью.</span><span class="sxs-lookup"><span data-stu-id="b6132-115">The media duration is 10 seconds, twice the length of the timeline duration, meaning the source will play at twice normal speed.</span></span> <span data-ttu-id="b6132-116">Константные единицы определяются как 10000000 (10 ^ 7) и равны одной секунде.</span><span class="sxs-lookup"><span data-stu-id="b6132-116">The constant UNITS is defined as 10000000 (10^7) and equals one second.</span></span>


```C++
pSourceObj->SetStartStop(0, 50000000)
BSTR bstrFile = SysAllocStringLen(OLESTR("C:\\example.avi"), 15);
pSource->SetMediaName(bstrFile); 
SysFreeString(bstrFile);
pSource->SetMediaTimes(40000000, 140000000);
```



> [!Note]  
> <span data-ttu-id="b6132-117">В настоящее время DES не может одновременно визуализировать более 75 источников, которые были сжаты с помощью кодеков для сжатия видео (ВКМ).</span><span class="sxs-lookup"><span data-stu-id="b6132-117">Currently, DES cannot simultaneously render more than 75 sources that were compressed with Video Compression Manager (VCM) codecs.</span></span> <span data-ttu-id="b6132-118">Кроме того, если проект в целом содержит более 75 таких источников, необходимо использовать динамическое переподключение или DES не может выполнить предварительный просмотр проекта.</span><span class="sxs-lookup"><span data-stu-id="b6132-118">Also, if the project as a whole contains more than 75 such sources, you must use dynamic reconnection or DES cannot preview the project.</span></span> <span data-ttu-id="b6132-119">Дополнительные сведения см. в разделе [**ирендеренгине:: сетдинамикреконнектлевел**](irenderengine-setdynamicreconnectlevel.md).</span><span class="sxs-lookup"><span data-stu-id="b6132-119">For more information, see [**IRenderEngine::SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md).</span></span>

 

<span data-ttu-id="b6132-120">Дополнительные сведения об источниках см. [в разделе Работа с источниками](working-with-sources.md).</span><span class="sxs-lookup"><span data-stu-id="b6132-120">For more information about sources, see [Working with Sources](working-with-sources.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b6132-121">См. также</span><span class="sxs-lookup"><span data-stu-id="b6132-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6132-122">Создание временной шкалы</span><span class="sxs-lookup"><span data-stu-id="b6132-122">Constructing a Timeline</span></span>](constructing-a-timeline.md)
</dt> </dl>

 

 




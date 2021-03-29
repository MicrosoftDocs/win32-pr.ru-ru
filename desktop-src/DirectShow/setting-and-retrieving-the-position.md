---
description: Установка и получение расположения
ms.assetid: 06b0e2d7-9539-41ad-a631-7e8da556feeb
title: Установка и получение расположения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 776a32eb6193ef456d693b5a133c87d800a0b64e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805207"
---
# <a name="setting-and-retrieving-the-position"></a><span data-ttu-id="0349c-103">Установка и получение расположения</span><span class="sxs-lookup"><span data-stu-id="0349c-103">Setting and Retrieving the Position</span></span>

<span data-ttu-id="0349c-104">Граф фильтра поддерживает два значения позиции: текущая позиция и позиция окончания.</span><span class="sxs-lookup"><span data-stu-id="0349c-104">The filter graph maintains two position values, current position and stop position.</span></span> <span data-ttu-id="0349c-105">Они определяются следующим образом.</span><span class="sxs-lookup"><span data-stu-id="0349c-105">These are defined as follows:</span></span>

-   <span data-ttu-id="0349c-106">При выполнении графа текущее расположение является текущей позицией воспроизведения относительно начала источника.</span><span class="sxs-lookup"><span data-stu-id="0349c-106">When the graph is running, the current position is the current playback position, relative to the beginning of the source.</span></span> <span data-ttu-id="0349c-107">Когда работа графа остановлена или приостановлена, текущей позицией является точка, с которой начинается потоковая передача при следующей команде Run.</span><span class="sxs-lookup"><span data-stu-id="0349c-107">When the graph is stopped or paused, the current position is the point where streaming will begin on the next run command.</span></span>
-   <span data-ttu-id="0349c-108">Позиция окончания — это точка, в которой поток будет завершен.</span><span class="sxs-lookup"><span data-stu-id="0349c-108">The stop position is the point where the stream will end.</span></span> <span data-ttu-id="0349c-109">Когда граф достигает позиции окончания, больше не выполняется потоковая передача данных, а диспетчер графа фильтров публикует событие [**EC \_ Complete**](ec-complete.md) .</span><span class="sxs-lookup"><span data-stu-id="0349c-109">When the graph reaches the stop position, no more data is streamed, and the filter graph manager posts an [**EC\_COMPLETE**](ec-complete.md) event.</span></span> <span data-ttu-id="0349c-110">(Однако диаграмма не переключается автоматически на остановленное состояние.</span><span class="sxs-lookup"><span data-stu-id="0349c-110">(The graph does not automatically switch to a stopped state, however.</span></span> <span data-ttu-id="0349c-111">Дополнительные сведения см. [в разделе реагирование на события](responding-to-events.md).)</span><span class="sxs-lookup"><span data-stu-id="0349c-111">For more information, see [Responding to Events](responding-to-events.md).)</span></span>

<span data-ttu-id="0349c-112">Чтобы получить эти значения, вызовите метод [**имедиасикинг:: Disposition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions) .</span><span class="sxs-lookup"><span data-stu-id="0349c-112">To retrieve these values, call the [**IMediaSeeking::GetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions) method.</span></span> <span data-ttu-id="0349c-113">Возвращаемые значения всегда относятся к исходному источнику мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="0349c-113">The returned values are always relative to the original media source.</span></span> <span data-ttu-id="0349c-114">По умолчанию значения находятся в ссылочных единицах времени.</span><span class="sxs-lookup"><span data-stu-id="0349c-114">By default, the values are in reference time units.</span></span> <span data-ttu-id="0349c-115">В некоторых случаях можно изменить единицы времени; Дополнительные сведения см. в разделе [форматы времени для команд Seek](time-formats-for-seek-commands.md).</span><span class="sxs-lookup"><span data-stu-id="0349c-115">In some cases, you can change the time units; for more information, see [Time Formats For Seek Commands](time-formats-for-seek-commands.md).</span></span>

<span data-ttu-id="0349c-116">Чтобы перейти к новой позиции или задать новую точку окончания, вызовите метод [**имедиасикинг:: сетпоситионс**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) , как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="0349c-116">To seek to a new position or set a new stop position, call the [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) method, as shown in the following example:</span></span>


```C++
#define ONE_SECOND 10000000
REFERENCE_TIME rtNow  = 2 * ONE_SECOND, 
               rtStop = 5 * ONE_SECOND;

hr = pSeek->SetPositions(
    &rtNow,  AM_SEEKING_AbsolutePositioning, 
    &rtStop, AM_SEEKING_AbsolutePositioning
    );
```



> [!Note]  
> <span data-ttu-id="0349c-117">Одна секунда — 10 000 000 единиц времени ссылки.</span><span class="sxs-lookup"><span data-stu-id="0349c-117">One second is 10,000,000 units of reference time.</span></span> <span data-ttu-id="0349c-118">Для удобства в примере это значение определяется как одна \_ секунда.</span><span class="sxs-lookup"><span data-stu-id="0349c-118">For convenience, the example defines this value as ONE\_SECOND.</span></span> <span data-ttu-id="0349c-119">При использовании библиотеки базового класса DirectShow константные единицы имеют одинаковое значение.</span><span class="sxs-lookup"><span data-stu-id="0349c-119">If you are using the DirectShow base-class library, the constant UNITS has the same value.</span></span>

 

<span data-ttu-id="0349c-120">Параметр *ртнов* задает новую текущую точку.</span><span class="sxs-lookup"><span data-stu-id="0349c-120">The *rtNow* parameter specifies the new current position.</span></span> <span data-ttu-id="0349c-121">Второй параметр — это флаг, определяющий способ интерпретации *ртнов*.</span><span class="sxs-lookup"><span data-stu-id="0349c-121">The second parameter is a flag that defines how to interpret *rtNow*.</span></span> <span data-ttu-id="0349c-122">В этом примере \_ флаг абсолутепоситионинг для поиска \_ указывает, что *ртнов* указывает абсолютное положение в источнике.</span><span class="sxs-lookup"><span data-stu-id="0349c-122">In this example, the AM\_SEEKING\_AbsolutePositioning flag indicates that *rtNow* specifies an absolute position in the source.</span></span> <span data-ttu-id="0349c-123">Таким образом, граф фильтра будет выполнять поиск в положении, равном двум секундам от начала потока.</span><span class="sxs-lookup"><span data-stu-id="0349c-123">Therefore, the filter graph will seek to a position two seconds from the start of the stream.</span></span> <span data-ttu-id="0349c-124">Параметр *ртстоп* задает время окончания.</span><span class="sxs-lookup"><span data-stu-id="0349c-124">The *rtStop* parameter gives the stop time.</span></span> <span data-ttu-id="0349c-125">Последний параметр указывает, что *ртстоп* также является абсолютной позицией.</span><span class="sxs-lookup"><span data-stu-id="0349c-125">The last parameter specifies that *rtStop* is also an absolute position.</span></span>

<span data-ttu-id="0349c-126">Чтобы задать расположение относительно предыдущего значения положения, используйте \_ \_ флаг AM релативепоситионинг.</span><span class="sxs-lookup"><span data-stu-id="0349c-126">To specify a position relative to the previous position value, use the AM\_SEEKING\_RelativePositioning flag.</span></span> <span data-ttu-id="0349c-127">Чтобы оставить одно из значений в неизменном виде, используйте флаг AM для \_ поиска по \_ положению.</span><span class="sxs-lookup"><span data-stu-id="0349c-127">To leave one of the position values unchanged, use the AM\_SEEKING\_NoPositioning flag.</span></span> <span data-ttu-id="0349c-128">В этом случае соответствующий параметр времени может иметь **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="0349c-128">The corresponding time parameter can be **NULL** in that case.</span></span> <span data-ttu-id="0349c-129">В следующем примере производится поиск вперед на 10 секунд, но не изменяется и позиция останавливается.</span><span class="sxs-lookup"><span data-stu-id="0349c-129">The following example seeks forward by 10 seconds but leaves the stop position unchanged:</span></span>


```C++
REFERENCE_TIME rtNow = 10 * ONE_SECOND;
hr = pSeek->SetPositions(
    &rtNow, AM_SEEKING_RelativePositioning, 
    NULL, AM_SEEKING_NoPositioning
    );
```



<span data-ttu-id="0349c-130">Если граф фильтра остановлен, модуль подготовки видео не обновляет образ после операции поиска.</span><span class="sxs-lookup"><span data-stu-id="0349c-130">If the filter graph is stopped, the video renderer does not update the image after a seek operation.</span></span> <span data-ttu-id="0349c-131">Для пользователя он будет выглядеть так, как если бы поиск не выполнялся.</span><span class="sxs-lookup"><span data-stu-id="0349c-131">To the user, it will appear as if the seek did not happen.</span></span> <span data-ttu-id="0349c-132">Чтобы обновить образ, приостановите граф после операции поиска.</span><span class="sxs-lookup"><span data-stu-id="0349c-132">To update the image, pause the graph after the seek operation.</span></span> <span data-ttu-id="0349c-133">При приостановке графа подготавливается новый кадр видео для модуля подготовки видео.</span><span class="sxs-lookup"><span data-stu-id="0349c-133">Pausing the graph cues a new video frame for the video renderer.</span></span> <span data-ttu-id="0349c-134">Можно использовать метод [**имедиаконтрол:: стопвхенреади**](/windows/desktop/api/Control/nf-control-imediacontrol-stopwhenready) , который приостанавливает граф, а затем останавливает его.</span><span class="sxs-lookup"><span data-stu-id="0349c-134">You can use the [**IMediaControl::StopWhenReady**](/windows/desktop/api/Control/nf-control-imediacontrol-stopwhenready) method, which pauses the graph and then stops it.</span></span>

 

 




---
description: Форматы времени для команд Seek
ms.assetid: d9c1b860-f75f-4886-95d6-c62e9e5b69eb
title: Форматы времени для команд Seek
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de8217873a9443c2b56c60523f95a6fe599ee045
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104547127"
---
# <a name="time-formats-for-seek-commands"></a><span data-ttu-id="c8c45-103">Форматы времени для команд Seek</span><span class="sxs-lookup"><span data-stu-id="c8c45-103">Time Formats For Seek Commands</span></span>

<span data-ttu-id="c8c45-104">Многие методы в интерфейсе **имедиасикинг** имеют параметры, которые выражают значения позиции, такие как текущая позиция или позиция окончания.</span><span class="sxs-lookup"><span data-stu-id="c8c45-104">Many of the methods in the **IMediaSeeking** interface have parameters that express position values, such as current position or stop position.</span></span> <span data-ttu-id="c8c45-105">По умолчанию эти параметры выражаются в единицах 100 наносекунд, также называемых временем ссылки.</span><span class="sxs-lookup"><span data-stu-id="c8c45-105">By default, these parameters are expressed in units of 100 nanoseconds, also called reference time.</span></span> <span data-ttu-id="c8c45-106">Любой фильтр, который может выполнять поиск, должен поддерживать поиск по времени ссылки.</span><span class="sxs-lookup"><span data-stu-id="c8c45-106">Any filter that can seek must support seeking by reference time.</span></span> <span data-ttu-id="c8c45-107">Некоторые фильтры могут выполнять поиск с использованием других единиц времени, таких как поиск по определенному номеру кадра, или поиск в заданном байтовом смещении в потоке.</span><span class="sxs-lookup"><span data-stu-id="c8c45-107">Some filters can seek using other units of time as well, such as seeking to a particular frame number, or seeking to a given byte offset within a stream.</span></span> <span data-ttu-id="c8c45-108">Каждый из этих единиц времени называется форматом времени и определяется глобальным уникальным идентификатором (GUID).</span><span class="sxs-lookup"><span data-stu-id="c8c45-108">Each of these time units is called a time format, and is defined by a globally unique identifier (GUID).</span></span> <span data-ttu-id="c8c45-109">Список форматов времени, определенных DirectShow, см. в разделе [**идентификаторы GUID формата времени**](time-format-guids.md).</span><span class="sxs-lookup"><span data-stu-id="c8c45-109">For a list of the time formats that are defined by DirectShow, see [**Time Format GUIDs**](time-format-guids.md).</span></span> <span data-ttu-id="c8c45-110">Сторонние лица могут также определять идентификаторы GUID для пользовательских форматов времени.</span><span class="sxs-lookup"><span data-stu-id="c8c45-110">Third parties can also define GUIDs for custom time formats.</span></span>

<span data-ttu-id="c8c45-111">Чтобы определить, поддерживают ли текущие фильтры в графе фильтра определенный формат времени, вызовите метод [**имедиасикинг:: исформатсуппортед**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) .</span><span class="sxs-lookup"><span data-stu-id="c8c45-111">To determine whether the filters currently in the filter graph support a particular time format, call the [**IMediaSeeking::IsFormatSupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) method.</span></span> <span data-ttu-id="c8c45-112">Если формат поддерживается, метод возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="c8c45-112">The method returns S\_OK if the format is supported.</span></span> <span data-ttu-id="c8c45-113">В противном случае возвращается \_ значение false или код ошибки.</span><span class="sxs-lookup"><span data-stu-id="c8c45-113">Otherwise, it returns S\_FALSE or an error code.</span></span> <span data-ttu-id="c8c45-114">Если формат поддерживается, можно переключиться на этот формат, вызвав метод [**имедиасикинг:: сеттимеформат**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) .</span><span class="sxs-lookup"><span data-stu-id="c8c45-114">If a format is supported, you can switch to that format by calling the [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) method.</span></span> <span data-ttu-id="c8c45-115">Если метод **сеттимеформат** выполняется, последующие команды поиска выражаются с использованием нового формата времени.</span><span class="sxs-lookup"><span data-stu-id="c8c45-115">If the **SetTimeFormat** method succeeds, subsequent seek commands are expressed using the new time format.</span></span>

<span data-ttu-id="c8c45-116">В приведенном ниже примере проверяется, поддерживает ли граф Поиск по номеру кадра.</span><span class="sxs-lookup"><span data-stu-id="c8c45-116">The follow example checks whether the graph supports seeking by frame number.</span></span> <span data-ttu-id="c8c45-117">Если это так, он ищет кадр номер 20:</span><span class="sxs-lookup"><span data-stu-id="c8c45-117">If so, it seeks to frame number 20:</span></span>


```C++
hr = pSeek->IsFormatSupported(&TIME_FORMAT_FRAME);
if (hr == S_OK)
{
    hr = pSeek->SetTimeFormat(&TIME_FORMAT_FRAME);
    if (SUCCEEDED(hr))
    {
        // Seek to frame number 20.
        LONGLONG rtNow = 20;
        hr = pSeek->SetPositions(
            &rtNow, AM_SEEKING_AbsolutePositioning, 
            0, AM_SEEKING_NoPositioning);
    }
}
```



<span data-ttu-id="c8c45-118">Обратите внимание, что форматы времени применяются только к командам Seek.</span><span class="sxs-lookup"><span data-stu-id="c8c45-118">Note that time formats only apply to seek commands.</span></span> <span data-ttu-id="c8c45-119">Они не влияют на воспроизведение графа и другие действия.</span><span class="sxs-lookup"><span data-stu-id="c8c45-119">They do not affect graph playback or other actions.</span></span>

 

 




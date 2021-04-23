---
description: Потоки аудио и субтитров
ms.assetid: 8d361da3-a33a-401c-a750-f9b952022cf6
title: Потоки аудио и субтитров
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2f5c8c74f7507557f374d690a671b62e8b43343
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495654"
---
# <a name="audio-and-subpicture-streams"></a><span data-ttu-id="c3331-103">Потоки аудио и субтитров</span><span class="sxs-lookup"><span data-stu-id="c3331-103">Audio and Subpicture Streams</span></span>

<span data-ttu-id="c3331-104">DVD-Videoный диск может иметь до восьми звуковых потоков, пронумерованных от нуля до семи, каждый из которых имеет до шести дискретных каналов.</span><span class="sxs-lookup"><span data-stu-id="c3331-104">A DVD-Video disc can have up to eight audio streams, numbered zero through seven, each with up to six discrete channels.</span></span> <span data-ttu-id="c3331-105">(Обратите внимание, что потоки аудио и субтитров нумеруются от нуля, в то время как заголовки, углы и родительские уровни нумеруются по одному.) В любое заданное время можно выбрать только один из этих потоков.</span><span class="sxs-lookup"><span data-stu-id="c3331-105">(Note that audio and subpicture streams are numbered from zero, whereas titles, angles, and parental levels are numbered from one.) Only one of these streams can be selected at any given time.</span></span> <span data-ttu-id="c3331-106">Для подизображений доступно до 32 потоков, хотя в любой момент времени может быть активирован только один поток.</span><span class="sxs-lookup"><span data-stu-id="c3331-106">For subpictures, up to 32 streams are available, although only one stream can be activated at any given time.</span></span> <span data-ttu-id="c3331-107">Диски обычно создаются с помощью потоков аудио и субтитров по умолчанию, но приложение может позволить пользователям просматривать список всех доступных потоков и выбирать его на предпочтительном языке.</span><span class="sxs-lookup"><span data-stu-id="c3331-107">Discs are generally authored with default audio and subpicture streams, but an application can enable users to view a list of all the available streams, and select the one in the language they prefer.</span></span> <span data-ttu-id="c3331-108">Основные шаги этого процесса одинаковы для потоков аудио и субтитров.</span><span class="sxs-lookup"><span data-stu-id="c3331-108">The basic steps in this process are the same for both audio and subpicture streams.</span></span>

1.  <span data-ttu-id="c3331-109">Определите количество потоков, доступных для заголовка.</span><span class="sxs-lookup"><span data-stu-id="c3331-109">Determine the number of streams available for a title.</span></span>
2.  <span data-ttu-id="c3331-110">Выполните итерацию по потокам и извлеките атрибуты потока для каждого из них.</span><span class="sxs-lookup"><span data-stu-id="c3331-110">Iterate through the streams and retrieve the stream attributes for each.</span></span>
3.  <span data-ttu-id="c3331-111">Получите код языка из возвращенного идентификатора языка (LCID) и создайте удобочитаемую строку.</span><span class="sxs-lookup"><span data-stu-id="c3331-111">Retrieve the language code from the returned locale identifier (LCID) and create a human-readable string.</span></span>
4.  <span data-ttu-id="c3331-112">Заполнение списка или другого элемента управления пользовательского интерфейса для предоставления пользователю возможности выбора предпочтительного потока.</span><span class="sxs-lookup"><span data-stu-id="c3331-112">Populate a list box or other user interface (UI) control to enable the user to select a preferred stream.</span></span>

<span data-ttu-id="c3331-113">В примере приложения DVD метод Каудиолангдлг:: Макеаудиостреамлист в диалоговых окнах. cpp демонстрирует основные шаги.</span><span class="sxs-lookup"><span data-stu-id="c3331-113">In the DVD sample application, the CAudioLangDlg::MakeAudioStreamList method in Dialogs.cpp demonstrates the basic steps.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c3331-114">См. также</span><span class="sxs-lookup"><span data-stu-id="c3331-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3331-115">DVD-приложения</span><span class="sxs-lookup"><span data-stu-id="c3331-115">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 




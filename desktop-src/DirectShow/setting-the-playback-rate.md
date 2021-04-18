---
description: Настройка скорости воспроизведения
ms.assetid: 74ae45d3-4fea-491c-af1f-46768df41c5f
title: Настройка скорости воспроизведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e8a3297ca376b0cc55e4df4884b22d1cb2df81b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105682172"
---
# <a name="setting-the-playback-rate"></a><span data-ttu-id="a268d-103">Настройка скорости воспроизведения</span><span class="sxs-lookup"><span data-stu-id="a268d-103">Setting the Playback Rate</span></span>

<span data-ttu-id="a268d-104">Чтобы изменить скорость воспроизведения, вызовите метод [**имедиасикинг:: сетрате**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) .</span><span class="sxs-lookup"><span data-stu-id="a268d-104">To change the playback rate, call the [**IMediaSeeking::SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) method.</span></span> <span data-ttu-id="a268d-105">Укажите новую ставку как часть исходной ставки.</span><span class="sxs-lookup"><span data-stu-id="a268d-105">Specify the new rate as a fraction of the original rate.</span></span> <span data-ttu-id="a268d-106">Например, для воспроизведения на двух-нормальных скоростях используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="a268d-106">For example, to play at twice-normal speed, use the following:</span></span>


```C++
pSeek->SetRate(2.0)
```



<span data-ttu-id="a268d-107">Ставки, превышающие единицу, работают быстрее, чем обычные.</span><span class="sxs-lookup"><span data-stu-id="a268d-107">Rates greater than one are faster than normal.</span></span> <span data-ttu-id="a268d-108">Ставка между нулем и одной медленнее, чем обычная.</span><span class="sxs-lookup"><span data-stu-id="a268d-108">Rates between zero and one are slower than normal.</span></span> <span data-ttu-id="a268d-109">Отрицательные тарифы определяются в качестве обратного воспроизведения, но на практике они не поддерживаются большинством фильтров.</span><span class="sxs-lookup"><span data-stu-id="a268d-109">Negative rates are defined as backward playback, but in practice most filters do not support it.</span></span> <span data-ttu-id="a268d-110">В настоящее время ни один из стандартных фильтров DirectShow не поддерживает обратную воспроизведение.</span><span class="sxs-lookup"><span data-stu-id="a268d-110">Currently none of the standard DirectShow filters support reverse playback.</span></span>

<span data-ttu-id="a268d-111">Независимо от скорости воспроизведения Текущая позиция и позиция окончания всегда выражаются относительно исходного источника.</span><span class="sxs-lookup"><span data-stu-id="a268d-111">Regardless of the playback rate, the current position and the stop position are always expressed relative to the original source.</span></span> <span data-ttu-id="a268d-112">Например, если размер исходного файла составляет 20 секунд с нормальным темпом воспроизведения, установка текущей позиции равным 10 секундам попытается перейти в середину файла.</span><span class="sxs-lookup"><span data-stu-id="a268d-112">For example, if a source file is 20 seconds long at normal playback rate, setting the current position to 10 seconds will seek to the middle of the file.</span></span> <span data-ttu-id="a268d-113">Если скорость воспроизведения равна 2,0, то позиция окончания составляет 20 секунд, и вы ищете 10-секундную единицу, воспроизведение файла будет продолжено 5 секунды в режиме реального времени: 10 секунд, в два раза больше, чем нормальная скорость воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="a268d-113">If the playback rate is 2.0, the stop position is 20 seconds, and you seek to the 10-second position, the file will play for 5 seconds of real time: 10 seconds' worth, at twice the normal playback speed.</span></span> <span data-ttu-id="a268d-114">При скорости воспроизведения 2,0 текущая единица увеличивается в два раза больше скорости ссылочного времени.</span><span class="sxs-lookup"><span data-stu-id="a268d-114">At a playback rate of 2.0, the current position increases at twice the rate of the reference clock.</span></span>

 

 




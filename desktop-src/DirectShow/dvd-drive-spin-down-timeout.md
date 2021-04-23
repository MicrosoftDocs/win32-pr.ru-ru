---
description: Время ожидания вращения DVD-дисковода
ms.assetid: 2295253d-0199-41b4-95a8-cda049ca93c7
title: Время ожидания вращения DVD-дисковода
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acda6853830ee7289e529d029c78fe4e56e4a0e3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894958"
---
# <a name="dvd-drive-spin-down-timeout"></a><span data-ttu-id="f683e-103">Время ожидания вращения DVD-дисковода</span><span class="sxs-lookup"><span data-stu-id="f683e-103">DVD Drive Spin Down Timeout</span></span>

<span data-ttu-id="f683e-104">На переносных компьютерах, чтобы сэкономить время работы батареи, может быть желательно уменьшить продолжительность времени, в течение которого DVD-дисковод будет продолжать работать после приостановки воспроизведения пользователем.</span><span class="sxs-lookup"><span data-stu-id="f683e-104">On laptop computers, to conserve battery life it may be desirable to reduce the length of time that a DVD drive will continue to spin after the user has paused playback.</span></span> <span data-ttu-id="f683e-105">По умолчанию на DVD-диске диск вращается в течение двух минут.</span><span class="sxs-lookup"><span data-stu-id="f683e-105">By default, the DVD Navigator keeps the disc spinning for two minutes.</span></span> <span data-ttu-id="f683e-106">Это значение можно изменить в реестре Windows с помощью этого раздела:</span><span class="sxs-lookup"><span data-stu-id="f683e-106">This value can be modified in the Windows Registry under this key:</span></span>


```C++
DWORD HKLM\SOFTWARE\Microsoft\DVDNavigator\DriveSpindown 
[Sec]
```



<span data-ttu-id="f683e-107">where</span><span class="sxs-lookup"><span data-stu-id="f683e-107">where</span></span>


```
Sec
```



<span data-ttu-id="f683e-108">время вращения в секундах.</span><span class="sxs-lookup"><span data-stu-id="f683e-108">is the spin down time in seconds.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f683e-109">См. также</span><span class="sxs-lookup"><span data-stu-id="f683e-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f683e-110">Приложения</span><span class="sxs-lookup"><span data-stu-id="f683e-110">Appendixes</span></span>](appendixes.md)
</dt> </dl>

 

 




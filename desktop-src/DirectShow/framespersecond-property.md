---
description: Свойство Фрамесперсеконд извлекает частоту кадров видео для текущего заголовка DVD.
ms.assetid: c5d36308-1447-4636-9b3a-4a3f93d27789
title: Фрамесперсеконд, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e00ec3281d88a2901f630c9231edbf1e76a89c23
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105673011"
---
# <a name="framespersecond-property"></a><span data-ttu-id="dbd45-103">Фрамесперсеконд, свойство</span><span class="sxs-lookup"><span data-stu-id="dbd45-103">FramesPerSecond Property</span></span>

> [!Note]  
> <span data-ttu-id="dbd45-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="dbd45-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="dbd45-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="dbd45-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="dbd45-106">`FramesPerSecond`Свойство получает частоту кадров видео для текущего заголовка DVD.</span><span class="sxs-lookup"><span data-stu-id="dbd45-106">The `FramesPerSecond` property retrieves the video frame rate for the current DVD title.</span></span>

``` syntax
[ iFramesPerSec = ] MSWebDVD.FramesPerSecond
```

## <a name="return-value"></a><span data-ttu-id="dbd45-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dbd45-107">Return Value</span></span>

<span data-ttu-id="dbd45-108">Возвращает целочисленное значение, представляющее частоту кадров видео; 25 или 30 кадров в секунду.</span><span class="sxs-lookup"><span data-stu-id="dbd45-108">Returns an integer value representing the video frame rate; either 25 or 30 frames per second.</span></span>

## <a name="remarks"></a><span data-ttu-id="dbd45-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dbd45-109">Remarks</span></span>

<span data-ttu-id="dbd45-110">Это свойство доступно только для чтения и не имеет значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="dbd45-110">This property is read-only with no default value.</span></span> <span data-ttu-id="dbd45-111">Видеосигналы NTSC отображаются в 30 кадров в секунду.</span><span class="sxs-lookup"><span data-stu-id="dbd45-111">NTSC video signals are displayed at 30 frames per second.</span></span> <span data-ttu-id="dbd45-112">Список PAL отображается по 25 кадров в секунду.</span><span class="sxs-lookup"><span data-stu-id="dbd45-112">PAL is displayed at 25 frames per second.</span></span> <span data-ttu-id="dbd45-113">Диск кодируется для воспроизведения на NTSC или PAL, но не может воспроизводиться одновременно.</span><span class="sxs-lookup"><span data-stu-id="dbd45-113">A disc is encoded to play on either NTSC or PAL, but cannot play on both.</span></span>

 

 




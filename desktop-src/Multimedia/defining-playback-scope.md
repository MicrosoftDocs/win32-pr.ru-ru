---
title: Определение области воспроизведения
description: Определение области воспроизведения
ms.assetid: f2563226-7af1-4cb3-b468-c59738feeda2
keywords:
- Макрос МЦивндплайфром
- Макрос МЦивндплайто
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 518fc80588147c4ccbbca619452b714333a8a34d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986449"
---
# <a name="defining-playback-scope"></a><span data-ttu-id="049da-105">Определение области воспроизведения</span><span class="sxs-lookup"><span data-stu-id="049da-105">Defining Playback Scope</span></span>

<span data-ttu-id="049da-106">МЦивнд предоставляет макросы, позволяющие определить *область* воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="049da-106">MCIWnd provides macros that allow you to define the playback *scope*.</span></span> <span data-ttu-id="049da-107">Область — это часть воспроизведения, которую необходимо воспроизвести.</span><span class="sxs-lookup"><span data-stu-id="049da-107">The scope is the portion of the playback you want to play.</span></span> <span data-ttu-id="049da-108">Например, можно воспроизвести содержимое из другого расположения с помощью макроса [**мЦивндплайфром**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom) .</span><span class="sxs-lookup"><span data-stu-id="049da-108">For example, you can play the content from a position other than the beginning position by using the [**MCIWndPlayFrom**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom) macro.</span></span> <span data-ttu-id="049da-109">Этот макрос перемещается в указанную точку, начинает воспроизведение и продолжается до конца содержимого.</span><span class="sxs-lookup"><span data-stu-id="049da-109">This macro moves to the specified position, begins playback, and continues to the end of the content.</span></span> <span data-ttu-id="049da-110">Аналогичным образом можно воспроизвести содержимое в указанную конечную точку с помощью макроса [**мЦивндплайто**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) .</span><span class="sxs-lookup"><span data-stu-id="049da-110">Similarly, you can play the content to a specified end point by using the [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) macro.</span></span> <span data-ttu-id="049da-111">Этот макрос начинается с текущей позиции воспроизведения и выполняется до тех пор, пока не достигнет указанной позиции, или достигнут конец содержимого.</span><span class="sxs-lookup"><span data-stu-id="049da-111">This macro starts at the current playback position and plays until it reaches the specified position or the end of the content is reached, whichever comes first.</span></span>

<span data-ttu-id="049da-112">Кроме того, можно определить начальную и конечную позиции с помощью макроса [**мЦивндплайфромто**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto) .</span><span class="sxs-lookup"><span data-stu-id="049da-112">Also, you can define both the beginning and ending positions by using the [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto) macro.</span></span> <span data-ttu-id="049da-113">Этот макрос перемещается в указанную начальную точку и выполняется до тех пор, пока не будет достигнута заданная конечная позиция или конец содержимого.</span><span class="sxs-lookup"><span data-stu-id="049da-113">This macro moves to the specified starting position and plays until the specified ending position or the end of the content is reached.</span></span>

 

 





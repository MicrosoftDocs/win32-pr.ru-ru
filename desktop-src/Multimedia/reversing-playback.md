---
title: Обратное воспроизведение
description: Обратное воспроизведение
ms.assetid: cb7c1293-42d7-4c74-b9e6-cc8899ca7c54
keywords:
- Макрос МЦивндплайреверсе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a708915679f75bfe478c160d71d35b0bcfa48a23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410915"
---
# <a name="reversing-playback"></a><span data-ttu-id="753ca-104">Обратное воспроизведение</span><span class="sxs-lookup"><span data-stu-id="753ca-104">Reversing Playback</span></span>

<span data-ttu-id="753ca-105">Некоторые устройства поддерживают воспроизведение в обратном направлении.</span><span class="sxs-lookup"><span data-stu-id="753ca-105">Some devices support playback in the reverse direction.</span></span> <span data-ttu-id="753ca-106">Содержимое такого устройства можно воспроизвести в обратном направлении с помощью макроса [**мЦивндплайреверсе**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse) .</span><span class="sxs-lookup"><span data-stu-id="753ca-106">You can play the content of such a device in the reverse direction by using the [**MCIWndPlayReverse**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse) macro.</span></span> <span data-ttu-id="753ca-107">Этот макрос определяет область воспроизведения от текущей позицией воспроизведения до начала содержимого.</span><span class="sxs-lookup"><span data-stu-id="753ca-107">This macro defines the playback scope from the current playback position to the beginning of the content.</span></span> <span data-ttu-id="753ca-108">Устройство цифрового видео МЦИАВИ. DRV, может воспроизводиться назад.</span><span class="sxs-lookup"><span data-stu-id="753ca-108">The digital-video device, MCIAVI.DRV, can play backward.</span></span> <span data-ttu-id="753ca-109">Устройства, которые не могут воспроизводиться назад, например аудио компакт-диск, могут выдавать сообщение об ошибке при вызове **мЦивндплайреверсе** .</span><span class="sxs-lookup"><span data-stu-id="753ca-109">Devices that cannot play backward, such as CD audio, can issue an error message when **MCIWndPlayReverse** is invoked.</span></span>

 

 





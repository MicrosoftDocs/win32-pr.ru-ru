---
title: Протокол ВМПКД
description: Протокол ВМПКД
ms.assetid: 385cfb03-88cc-400c-a2b9-174008ebd854
keywords:
- Проигрыватель Windows Media, протоколы
- Объектная модель проигрывателя Windows Media, протоколы
- Объектная модель, протоколы
- Элемент управления ActiveX проигрывателя Windows Media, протоколы для объектной модели
- Элемент управления ActiveX, протоколы для объектной модели
- Элемент управления ActiveX мобильных устройств Windows Media Player, протоколы для объектной модели
- Проигрыватель Windows Media Mobile, протоколы для объектной модели
- протоколы, объектная модель проигрывателя Windows Media
- протоколы, ВМПКД
- Протокол ВМПКД
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa78c591d0ba9605f1f63e3e152b974d112548d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104253222"
---
# <a name="wmpcd-protocol"></a><span data-ttu-id="e867a-113">Протокол ВМПКД</span><span class="sxs-lookup"><span data-stu-id="e867a-113">WMPCD Protocol</span></span>

<span data-ttu-id="e867a-114">Протокол ВМПКД позволяет указывать дорожки на компакт-диске с помощью синтаксиса URL.</span><span class="sxs-lookup"><span data-stu-id="e867a-114">The WMPCD protocol enables you to specify tracks on a compact disc using URL syntax.</span></span> <span data-ttu-id="e867a-115">Это общий синтаксис протокола:</span><span class="sxs-lookup"><span data-stu-id="e867a-115">This is the general syntax of the protocol:</span></span>


```C++
wmpcd://drive/track
```



<span data-ttu-id="e867a-116">Сегмент *диска* — это индекс ДИСКОВОДА компакт-дисков.</span><span class="sxs-lookup"><span data-stu-id="e867a-116">The *drive* segment is the index of the CD drive.</span></span> <span data-ttu-id="e867a-117">Сегмент *Track* — это номер курса. В следующем примере демонстрируется использование протокола ВМПКД.</span><span class="sxs-lookup"><span data-stu-id="e867a-117">The *track* segment is the number of the track. The following example demonstrates using the WMPCD protocol.</span></span>


```C++
player.url = "wmpcd://0/4";
```



<span data-ttu-id="e867a-118">В примере воспроизводится четвертая запись на диске на первом компакт-диске (диск, индекс которого равен 0).</span><span class="sxs-lookup"><span data-stu-id="e867a-118">The example plays the fourth track on the disc in the first CD drive (the drive whose index is 0).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e867a-119">См. также</span><span class="sxs-lookup"><span data-stu-id="e867a-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e867a-120">**Поддерживаемые протоколы и типы файлов**</span><span class="sxs-lookup"><span data-stu-id="e867a-120">**Supported Protocols and File Types**</span></span>](supported-protocols-and-file-types.md)
</dt> </dl>

 

 





---
title: Об объекте DVD
description: Об объекте DVD
ms.assetid: 6c255e9e-d537-4f4f-865c-b7fb26c8e413
keywords:
- Проигрыватель Windows Media, объект DVD
- Объектная модель проигрывателя Windows Media, объект DVD
- Объектная модель, объект DVD
- Элемент управления ActiveX проигрывателя Windows Media, объект DVD
- Элемент управления ActiveX, объект DVD
- Элемент управления ActiveX проигрывателя Windows Media Mobile, объект DVD
- Проигрыватель Windows Media Mobile, объект DVD
- Объект DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29b9432fa90e409b40f9e1acd3e7686628bca3d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328523"
---
# <a name="about-the-dvd-object"></a><span data-ttu-id="4aa8b-111">Об объекте DVD</span><span class="sxs-lookup"><span data-stu-id="4aa8b-111">About the DVD Object</span></span>

<span data-ttu-id="4aa8b-112">Объект **DVD** добавляет функции, относящиеся к DVD-носителям.</span><span class="sxs-lookup"><span data-stu-id="4aa8b-112">The **DVD** object adds functionality specific to DVD media.</span></span> <span data-ttu-id="4aa8b-113">В общем смысле DVD-диски обрабатываются в проигрывателе Windows Media так же, как и другие цифровые носители.</span><span class="sxs-lookup"><span data-stu-id="4aa8b-113">In a general sense, DVD media is treated just like other digital media in Windows Media Player.</span></span> <span data-ttu-id="4aa8b-114">Например, DVD-дисководы перечисляются с помощью объектов и наименований DVD, **а также для** работы с ними используются объекты **списков воспроизведения** и объекты **мультимедиа** .</span><span class="sxs-lookup"><span data-stu-id="4aa8b-114">For instance, DVD drives are enumerated using the **CdromCollection** object and DVD titles and chapters are manipulated using **Playlist** objects and **Media** objects.</span></span> <span data-ttu-id="4aa8b-115">Однако некоторые функции относятся к DVD-диску, а также к объекту **DVD** .</span><span class="sxs-lookup"><span data-stu-id="4aa8b-115">Some functionality is DVD-specific, however, and the **DVD** object provides this.</span></span> <span data-ttu-id="4aa8b-116">Например, DVD имеет концепцию с именем domain.</span><span class="sxs-lookup"><span data-stu-id="4aa8b-116">For example, DVD has a concept called domain.</span></span> <span data-ttu-id="4aa8b-117">Чтобы получить текущий домен для носителя DVD, введите следующее:</span><span class="sxs-lookup"><span data-stu-id="4aa8b-117">To retrieve the current domain for DVD media, type the following:</span></span>


```C++
mydomain = player.dvd.domain;

```



## <a name="related-topics"></a><span data-ttu-id="4aa8b-118">См. также</span><span class="sxs-lookup"><span data-stu-id="4aa8b-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4aa8b-119">**Объект DVD**</span><span class="sxs-lookup"><span data-stu-id="4aa8b-119">**DVD Object**</span></span>](dvd-object.md)
</dt> <dt>

[<span data-ttu-id="4aa8b-120">**Объектная модель проигрывателя для языков сценариев**</span><span class="sxs-lookup"><span data-stu-id="4aa8b-120">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 





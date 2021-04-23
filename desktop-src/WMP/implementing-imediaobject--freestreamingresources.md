---
title: Реализация Имедиаобжект Фристреамингресаурцес
description: Реализация Имедиаобжект Фристреамингресаурцес
ms.assetid: 970dd10b-a7a0-4ba0-97e3-725d5c914500
keywords:
- Подключаемые модули проигрывателя Windows Media, эхо-образцы ресурсов потоковой передачи
- подключаемые модули, эхо-образцы ресурсов
- подключаемые модули обработки цифровых сигналов, образцы эхо-потоков
- Подключаемые модули DSP, потоковая передача образцов ресурсов
- Пример подключаемого модуля "Echo DSP", потоковая передача ресурсов
- Пример подключаемого модуля Echo DSP, освобождение памяти
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a31a293cfc68caf43496d031426de2441c9c1d05
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888039"
---
# <a name="implementing-imediaobjectfreestreamingresources"></a><span data-ttu-id="444d4-109">Реализация Имедиаобжект:: Фристреамингресаурцес</span><span class="sxs-lookup"><span data-stu-id="444d4-109">Implementing IMediaObject::FreeStreamingResources</span></span>

<span data-ttu-id="444d4-110">Важно, чтобы код выпустил выделенную память до уничтожения объекта подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="444d4-110">It is important that your code releases any allocated memory before the plug-in object is destroyed.</span></span> <span data-ttu-id="444d4-111">Проигрыватель Windows Media вызывает **фристреамингресаурцес** , чтобы это можно было сделать.</span><span class="sxs-lookup"><span data-stu-id="444d4-111">Windows Media Player calls **FreeStreamingResources** to allow you to do this.</span></span> <span data-ttu-id="444d4-112">Для обеспечения безопасности пример, созданный мастером подключаемых модулей, содержит вызов **фристреамингресаурцес** в методе **финалрелеасе** , чтобы гарантировать освобождение памяти.</span><span class="sxs-lookup"><span data-stu-id="444d4-112">For safety, the sample created by the plug-in wizard includes a call to **FreeStreamingResources** in the **FinalRelease** method to ensure that the memory is freed.</span></span> <span data-ttu-id="444d4-113">Для примера Echo необходимо добавить следующий код в **фристреамингресаурцес** :</span><span class="sxs-lookup"><span data-stu-id="444d4-113">You must add the following code to **FreeStreamingResources** for the Echo sample:</span></span>


```
// Test whether a buffer exists.
if (m_pbDelayBuffer)
{
    delete m_pbDelayBuffer;
    m_pbDelayBuffer = NULL;
    m_pbDelayPointer = NULL;
    m_cbDelayBuffer = 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="444d4-114">См. также</span><span class="sxs-lookup"><span data-stu-id="444d4-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="444d4-115">**Работа с потоковой передачей ресурсов**</span><span class="sxs-lookup"><span data-stu-id="444d4-115">**Working with Streaming Resources**</span></span>](working-with-streaming-resources.md)
</dt> </dl>

 

 





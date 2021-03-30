---
title: Переменные для управления буфером задержки
description: Переменные для управления буфером задержки
ms.assetid: 2c5963a1-04e2-4421-8f56-14c1e059de4e
keywords:
- Подключаемые модули проигрывателя Windows Media, эхо-образцы ресурсов потоковой передачи
- подключаемые модули, эхо-образцы ресурсов
- подключаемые модули обработки цифровых сигналов, образцы эхо-потоков
- Подключаемые модули DSP, потоковая передача образцов ресурсов
- Пример подключаемого модуля "Echo DSP", потоковая передача ресурсов
- Пример подключаемого модуля Echo DSP, буфер задержки
- буфер задержки
- буферы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09d7f9657d16d0805ff2fc85d2238635fbfa6e5e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104258581"
---
# <a name="variables-to-manage-the-delay-buffer"></a><span data-ttu-id="eb7e2-111">Переменные для управления буфером задержки</span><span class="sxs-lookup"><span data-stu-id="eb7e2-111">Variables to Manage the Delay Buffer</span></span>

<span data-ttu-id="eb7e2-112">Необходимо добавить объявления для переменных элементов, необходимых для управления буфером задержки.</span><span class="sxs-lookup"><span data-stu-id="eb7e2-112">You must add the declarations for the member variables you need to manage the delay buffer.</span></span> <span data-ttu-id="eb7e2-113">Добавьте следующие объявления в Echo. h в разделе "Private":</span><span class="sxs-lookup"><span data-stu-id="eb7e2-113">Add the following declarations to Echo.h in the "private" section:</span></span>


```C++
DWORD  m_cbDelayBuffer;   // Count of bytes in delay buffer size.
BYTE*  m_pbDelayPointer;  // Movable pointer to delay buffer.
BYTE*  m_pbDelayBuffer;   // Pointer to the head of the delay buffer.

```



<span data-ttu-id="eb7e2-114">Добавьте следующий код в конструктор Цечо для инициализации переменных буфера с задержкой:</span><span class="sxs-lookup"><span data-stu-id="eb7e2-114">Add the following code to the CEcho constructor to initialize the delay buffer variables:</span></span>


```C++
m_pbDelayBuffer = NULL;
m_pbDelayPointer = NULL;
m_cbDelayBuffer = 0;

```



## <a name="related-topics"></a><span data-ttu-id="eb7e2-115">См. также</span><span class="sxs-lookup"><span data-stu-id="eb7e2-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb7e2-116">**Работа с потоковой передачей ресурсов**</span><span class="sxs-lookup"><span data-stu-id="eb7e2-116">**Working with Streaming Resources**</span></span>](working-with-streaming-resources.md)
</dt> </dl>

 

 





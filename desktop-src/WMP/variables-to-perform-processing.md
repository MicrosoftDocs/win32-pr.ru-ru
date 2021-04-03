---
title: Переменные для выполнения обработки
description: Переменные для выполнения обработки
ms.assetid: 02f194ea-cac0-410f-886f-2894dd6971c8
keywords:
- Подключаемые модули проигрывателя Windows Media, метод Echo Sample Допроцессаутпут
- подключаемые модули, метод Echo Sample Допроцессаутпут
- подключаемые модули обработки цифровых сигналов, метод Echo Sample Допроцессаутпут
- Подключаемые модули DSP, метод Echo Sample Допроцессаутпут
- Пример подключаемого модуля Echo DSP, метод Допроцессаутпут
- Пример подключаемого модуля Echo DSP, обработка переменных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e44f044aee6d893fba97cf921360444ec43db871
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776643"
---
# <a name="variables-to-perform-processing"></a><span data-ttu-id="09140-109">Переменные для выполнения обработки</span><span class="sxs-lookup"><span data-stu-id="09140-109">Variables to Perform Processing</span></span>

<span data-ttu-id="09140-110">Переменные члена для обработки буфера задержки с количеством **байтов** ; они представляют собой **байтовые** указатели и целое число, в котором хранится число байтов.</span><span class="sxs-lookup"><span data-stu-id="09140-110">The member variables for handling the delay buffer deal with **BYTE** quantities; they are **BYTE** pointers and an integer that stores a count of bytes.</span></span> <span data-ttu-id="09140-111">Это идеальный вариант для обработки 8-разрядного звука, так как 8-разрядный пример хорошо помещается в один байт памяти.</span><span class="sxs-lookup"><span data-stu-id="09140-111">This is ideal for processing 8-bit audio, since an 8-bit sample fits nicely into one byte of memory.</span></span> <span data-ttu-id="09140-112">Однако при обработке 16-разрядного звука удобнее преобразовать их в **короткие** указатели, поэтому обработка может происходить по два байта за раз.</span><span class="sxs-lookup"><span data-stu-id="09140-112">When processing 16-bit audio, though, it is more convenient to convert these to **short** pointers, so the processing can occur two bytes at a time.</span></span>

<span data-ttu-id="09140-113">Следующий пример кода выделяет новые 16-разрядные указатели и добавляет переменную указателя, в которой хранится адрес конца буфера задержки.</span><span class="sxs-lookup"><span data-stu-id="09140-113">The following example code allocates the new 16-bit pointers, and adds a pointer variable that stores the address of the end of the delay buffer.</span></span> <span data-ttu-id="09140-114">Вставьте его в раздел "Case 16" непосредственно перед точкой входа цикла:</span><span class="sxs-lookup"><span data-stu-id="09140-114">Insert it in the "case 16" section just before the loop entry point:</span></span>


```C++
// Store local pointers to the delay buffer.
short    *pwDelayPointer = (short *)m_pbDelayPointer;
short    *pwDelayBuffer = (short *) m_pbDelayBuffer;
// Store the address of the last word of the delay buffer.
short    *pwEOFDelayBuffer = (short *)(m_pbDelayBuffer + m_cbDelayBuffer - sizeof(short)); 

```



<span data-ttu-id="09140-115">Код для 8-разрядной обработки также выделяет переменную, в которой хранится адрес конца буфера задержки.</span><span class="sxs-lookup"><span data-stu-id="09140-115">The code for 8-bit processing also allocates a variable that stores the address of the end of the delay buffer.</span></span> <span data-ttu-id="09140-116">Сохранение этого значения позволяет легко проверить, достигнут ли перемещаемый указатель буфера задержки на конец буфера задержки.</span><span class="sxs-lookup"><span data-stu-id="09140-116">Storing this value makes it easy to test whether the movable delay buffer pointer has reached the end of the delay buffer.</span></span> <span data-ttu-id="09140-117">В следующем примере кода вычисляется значение:</span><span class="sxs-lookup"><span data-stu-id="09140-117">The following example code calculates the value:</span></span>


```C++
// Store the address of the end of the delay buffer.
BYTE * pbEOFDelayBuffer = (m_pbDelayBuffer + m_cbDelayBuffer - sizeof(BYTE));

```



## <a name="related-topics"></a><span data-ttu-id="09140-118">См. также</span><span class="sxs-lookup"><span data-stu-id="09140-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09140-119">**Реализация Цечо::D Опроцессаутпут**</span><span class="sxs-lookup"><span data-stu-id="09140-119">**Implementing CEcho::DoProcessOutput**</span></span>](implementing-cecho--doprocessoutput.md)
</dt> </dl>

 

 





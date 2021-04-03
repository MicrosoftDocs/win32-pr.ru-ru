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
# <a name="variables-to-perform-processing"></a>Переменные для выполнения обработки

Переменные члена для обработки буфера задержки с количеством **байтов** ; они представляют собой **байтовые** указатели и целое число, в котором хранится число байтов. Это идеальный вариант для обработки 8-разрядного звука, так как 8-разрядный пример хорошо помещается в один байт памяти. Однако при обработке 16-разрядного звука удобнее преобразовать их в **короткие** указатели, поэтому обработка может происходить по два байта за раз.

Следующий пример кода выделяет новые 16-разрядные указатели и добавляет переменную указателя, в которой хранится адрес конца буфера задержки. Вставьте его в раздел "Case 16" непосредственно перед точкой входа цикла:


```C++
// Store local pointers to the delay buffer.
short    *pwDelayPointer = (short *)m_pbDelayPointer;
short    *pwDelayBuffer = (short *) m_pbDelayBuffer;
// Store the address of the last word of the delay buffer.
short    *pwEOFDelayBuffer = (short *)(m_pbDelayBuffer + m_cbDelayBuffer - sizeof(short)); 

```



Код для 8-разрядной обработки также выделяет переменную, в которой хранится адрес конца буфера задержки. Сохранение этого значения позволяет легко проверить, достигнут ли перемещаемый указатель буфера задержки на конец буфера задержки. В следующем примере кода вычисляется значение:


```C++
// Store the address of the end of the delay buffer.
BYTE * pbEOFDelayBuffer = (m_pbDelayBuffer + m_cbDelayBuffer - sizeof(BYTE));

```



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Реализация Цечо::D Опроцессаутпут**](implementing-cecho--doprocessoutput.md)
</dt> </dl>

 

 





---
title: Переменные для управления буфером задержки
description: Переменные для управления буфером задержки
ms.assetid: 2c5963a1-04e2-4421-8f56-14c1e059de4e
keywords:
- проигрыватель Windows Media подключаемых модулей, эхо-образцы ресурсов
- подключаемые модули, эхо-образцы ресурсов
- подключаемые модули обработки цифровых сигналов, образцы эхо-потоков
- Подключаемые модули DSP, потоковая передача образцов ресурсов
- Пример подключаемого модуля "Echo DSP", потоковая передача ресурсов
- Пример подключаемого модуля Echo DSP, буфер задержки
- буфер задержки
- буферы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5be71bc7f2ded34dcd5f29bc10ce01796b6498d36a9a194a48b0bfdec0e14662
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571744"
---
# <a name="variables-to-manage-the-delay-buffer"></a>Переменные для управления буфером задержки

Необходимо добавить объявления для переменных элементов, необходимых для управления буфером задержки. Добавьте следующие объявления в Echo. h в разделе "Private":


```C++
DWORD  m_cbDelayBuffer;   // Count of bytes in delay buffer size.
BYTE*  m_pbDelayPointer;  // Movable pointer to delay buffer.
BYTE*  m_pbDelayBuffer;   // Pointer to the head of the delay buffer.

```



Добавьте следующий код в конструктор Цечо для инициализации переменных буфера с задержкой:


```C++
m_pbDelayBuffer = NULL;
m_pbDelayPointer = NULL;
m_cbDelayBuffer = 0;

```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Работа с потоковой передачей ресурсов**](working-with-streaming-resources.md)
</dt> </dl>

 

 





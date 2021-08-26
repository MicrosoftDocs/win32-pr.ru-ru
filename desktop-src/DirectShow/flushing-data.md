---
description: Очистка данных
ms.assetid: 528763a2-c0f2-4981-91dc-dd17987f5bd5
title: Очистка данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8a435bf40ae9f71b35707935812c3a935a95df1904db00a652634b171f20a10
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965464"
---
# <a name="flushing-data"></a>Очистка данных

В следующем псевдокоде показано, как реализовать метод [**Ипин:: бегинфлуш**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) :


```C++
HRESULT CMyInputPin::BeginFlush()
{
    CAutoLock lock_it(m_pLock);
   
    // First, make sure the Receive method will fail from now on.
    HRESULT hr = CBaseInputPin::BeginFlush();
    
    // Force downstream filters to release samples. If our Receive method
    // is blocked in GetBuffer or Deliver, this will unblock it.
    for (each output pin)
    {
        hr = pOutputPin->DeliverBeginFlush();
    }

    // Unblock our Receive method if it is waiting on an event.
    SetEvent(m_hSomeEventThatReceiveNeedsToWaitOn);

    // At this point, the Receive method can't be blocked. Make sure 
    // it finishes, by taking the streaming lock. (Not necessary if this 
    // is the last step.)
    { 
        CAutoLock lock_2(&m_csReceive);

        /* Now it's safe to do anything that would crash or hang 
           if Receive were executing. */
    }
    return hr;
}
```



Когда начинается запись на диск, метод **бегинфлуш** принимает блокировку фильтра, которая сериализует изменение состояния. Блокировка потоковой передачи еще не является защищенной, так как в потоке приложения происходит запись на диск, а поток потоковой передачи может находиться в середине вызова **Receive** . ПИН-код должен гарантировать, что метод **Receive** не блокируется, и все последующие вызовы **Receive** завершатся ошибкой. Метод [**кбасеинпутпин:: бегинфлуш**](cbaseinputpin-beginflush.md) задает внутренний флаг, [**кбасеинпутпин:: m \_ бфлушинг**](cbaseinputpin-m-bflushing.md). Если флаг имеет **значение true**, метод **Receive** завершается ошибкой.

Получив вызов **бегинфлуш** , ПИН-код гарантирует, что все нисходящие фильтры выпускают свои примеры и возвращают из вызовов **Receive** . Это, в свою очередь, гарантирует, что входной ПИН-код не блокируется **в ожидании при** **получении**. Если метод **Receive** вашего ПИН-кода ожидает события (например, для получения ресурсов), метод **бегинфлуш** должен принудительно ожидать завершения, установив событие. На этом этапе гарантированно возвращается метод **Receive** , а флаг **m \_ бфлушинг** предотвращает выполнение новых вызовов **Receive** .

Для некоторых фильтров это все, что нужно сделать **бегинфлуш** . Метод **ендфлуш** сообщит фильтру, что он может снова начать получать образцы. Другим фильтрам может потребоваться использовать переменные или ресурсы в **бегинфлуш** , которые также используются в **Receive**. В этом случае фильтр должен сначала сохранить потоковую блокировку. Не забудьте сделать это до выполнения какого-либо из описанных выше действий, так как это может привести к взаимоблокировке.

Метод **ендфлуш** удерживает блокировку фильтра и распространяет вызов по нисходящей:


```C++
HRESULT CMyInputPin::EndFlush()
{
    CAutoLock lock_it(m_pLock);
    for (each output pin)
        hr = pOutputPin->DeliverEndFlush();
    return CBaseInputPin::EndFlush();
}
```



Метод [**кбасеинпутпин:: ендфлуш**](cbaseinputpin-endflush.md) сбрасывает флаг **m \_ бфлушинг** в **значение false**, что позволяет методу **Receive** снова начать получать образцы. Это должен быть последний шаг в **ендфлуш**, так как ПИН-код не должен получать выборки до тех пор, пока не будет выполнен сброс и не будут уведомлены все нисходящие фильтры.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Потоки и критические разделы](threads-and-critical-sections.md)
</dt> </dl>

 

 




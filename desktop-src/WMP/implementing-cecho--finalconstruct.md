---
title: Реализация Цечо Финалконструкт
description: Реализация Цечо Финалконструкт
ms.assetid: 149e99c5-9f57-4447-b520-39a6dd39fc86
keywords:
- Подключаемые модули проигрывателя Windows Media, примеры страниц свойств Echo
- страницы свойств "подключаемые модули", "Эхо-примеры"
- подключаемые модули обработки цифровых сигналов, примеры страниц свойств
- Подключаемые модули DSP, примеры страниц свойств
- Пример подключаемого модуля "Echo DSP", страницы свойств
- Пример подключаемого модуля Echo DSP, метод Цечо Финалконструкт
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 876db9f2479644800c42354a041ad3b1909b526b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104132922"
---
# <a name="implementing-cechofinalconstruct"></a>Реализация Цечо:: Финалконструкт

Метод Цечо:: Финалконструкт реализован в Echo. cpp. Он содержит код для чтения значений свойств из реестра, когда проигрыватель Windows Media создает экземпляр подключаемого объекта DSP. Это важно, так как позволяет сохранять параметры пользователя между экземплярами объекта, а также между сеансами. Образец кода мастера подключаемых модулей предоставляет реализацию для чтения одного свойства из реестра. Этот код можно изменить для работы со свойством время задержки, а затем добавить код для чтения значения свойства Mix.

Следующий пример кода считывает каждое значение свойства из реестра и сохраняет каждый в правильной переменной члена:


```CSharp
CRegKey key;
LONG    lResult;
DWORD   dwValue;

lResult = key.Open(HKEY_CURRENT_USER, kszPrefsRegKey, KEY_READ);
if (ERROR_SUCCESS == lResult)
{
    // Read the delay time from the registry. 
    lResult = key.QueryValue(dwValue, kszPrefsDelayTime );
    if (ERROR_SUCCESS == lResult)
    {
        m_dwDelayTime = dwValue;
    }

    // Read the wet mix value from the registry. 
    lResult = key.QueryValue(dwValue, kszPrefsWetmix );
    if (ERROR_SUCCESS == lResult)
    {
        // Convert the DWORD to a double.
        m_fWetMix = (double)dwValue / 100;
        // Calculate the dry mix value.
        m_fDryMix = 1.0 - m_fWetMix;
    }

}

return S_OK;
```



Обратите внимание, что значение DWORD для заданной позиции преобразуется в значение с плавающей запятой. Также обратите внимание, что код вычисляет правильное значение для m \_ фдримикс.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Изменение страницы свойств «пример эха»**](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 





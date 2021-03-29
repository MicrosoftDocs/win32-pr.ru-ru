---
title: Добавление свойства "Mix!"
description: Добавление свойства "Mix!"
ms.assetid: 4605d893-8ac0-42fd-a1ac-51430561f174
keywords:
- Подключаемые модули проигрывателя Windows Media, пример свойств Echo
- подключаемые модули, свойства образца Echo
- подключаемые модули обработки цифровых сигналов, свойства образца эха
- Подключаемые модули DSP, свойства образца Echo
- Пример подключаемого модуля "Echo DSP", свойства
- Пример подключаемого модуля Echo DSP, свойство Mix
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad6af8e7b4857ccbf6b725044575d1b8524aaf50
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330096"
---
# <a name="adding-the-wet-mix-property"></a>Добавление свойства "Mix!"

Необходимо добавить код, чтобы предоставить дополнительное свойство для уровня эффектов.

В разделе [Добавление свойств для примера подключаемого модуля DSP аудиоподсистемы](adding-properties-to-the-sample-audio-dsp-plug-in.md) содержатся сведения о том, как добавить новое свойство с помощью Visual C++. В этом разделе показано, как добавить код вручную. Это влечет за собой добавление кода в те же три места, где был изменен код для свойства время задержки.

Добавьте прототипы для \_ методов Get ветмикс и \_ ветмикс сразу после других прототипов метода свойства в Echo. h. Используйте следующий синтаксис:


```C++
STDMETHOD(get_wetmix)(double *pVal);
STDMETHOD(put_wetmix)(double newVal);

```



Теперь добавьте реализацию для каждого метода сразу после реализации других свойств в Echo. cpp. В следующем примере показан код для обоих методов:


```C++
// Property get to retrieve the wet mix value by using the public interface.
STDMETHODIMP CEcho::get_wetmix(double *pVal)
{
    if ( NULL == pVal )
    {
        return E_POINTER;
    }

    *pVal = m_fWetMix;

    return S_OK;
}

// Property put to store the wet mix value by using the public interface.
STDMETHODIMP CEcho::put_wetmix(double newVal)
{
    m_fWetMix = newVal;

    // Calculate m_fDryMix
    m_fDryMix = 1.0 - m_fWetMix;
    
    return S_OK;
}

```



Обратите внимание, что реализация метода \_ ветмикс включает код для вычисления правильного значения m \_ фдримикс. При каждом задании нового значения для m \_ фветмикс это вычисление является обязательным.

Добавьте следующий код в определение интерфейса сразу после кода для методов Delay в Echo. IDL:


```C++
HRESULT get_wetmix([out] double *pVal);
HRESULT put_wetmix([in] double newVal);

```



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Свойства образца Echo**](echo-sample-properties.md)
</dt> </dl>

 

 





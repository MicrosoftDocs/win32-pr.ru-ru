---
title: Добавление свойств в образец подключаемого модуля DSP для аудио
description: Добавление свойств в образец подключаемого модуля DSP для аудио
ms.assetid: 9c6c2a34-4844-476b-8814-a95a236e75bb
keywords:
- подключаемые модули проигрыватель Windows Media, DSP аудиоподсистемы
- подключаемые модули, DSP аудиоподсистемы
- подключаемые модули обработки цифровых сигналов, свойства аудио
- Подключаемые модули DSP, звуковые свойства
- подключаемые модули DSP аудио, свойства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b87c650ed66bbb3da0886eb02157804ca10005a47053def841996019917ceed8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031504"
---
# <a name="adding-properties-to-the-sample-audio-dsp-plug-in"></a>Добавление свойств в образец подключаемого модуля DSP для аудио

пример кода DSP, который создается мастером подключаемых модулей проигрыватель Windows Media, использует одно свойство, представляющее коэффициент масштабирования для звукового тома. Подключаемому модулю может потребоваться более одного свойства. вы можете легко добавить свойства в подключаемый модуль DSP в Visual Studio, выполнив следующие действия.

-   Определите методы в коде определения интерфейса в IDL-файле, который является частью проекта-заглушки.
    -   Добавьте реализации методов в основной файл CPP проекта:

    ```C++
    STDMETHODIMP CYourProject::get_color(COLORREF *pColor)
    {
        if ( NULL == pColor )
        {
            return E_POINTER;
        }

        *pColor = m_Color;

        return S_OK;
    }

    STDMETHODIMP CYourProject::put_color(COLORREF newColor)
    {
        m_Color = newColor;
        
        return S_OK;
    }
    
    ```

    

Наконец, чтобы сделать свойства доступными для пользователя, необходимо внести изменения в реализацию страницы свойств.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Реализация подключаемого модуля DSP аудиоподсистемы**](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 





---
title: Добавление свойств в образец подключаемого модуля DSP для аудио
description: Добавление свойств в образец подключаемого модуля DSP для аудио
ms.assetid: 9c6c2a34-4844-476b-8814-a95a236e75bb
keywords:
- Подключаемые модули проигрывателя Windows Media, DSP аудиоподсистемы
- подключаемые модули, DSP аудиоподсистемы
- подключаемые модули обработки цифровых сигналов, свойства аудио
- Подключаемые модули DSP, звуковые свойства
- подключаемые модули DSP аудио, свойства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d180ab1054631b09997ac986529a641e6ff05ec3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691219"
---
# <a name="adding-properties-to-the-sample-audio-dsp-plug-in"></a><span data-ttu-id="b1098-108">Добавление свойств в образец подключаемого модуля DSP для аудио</span><span class="sxs-lookup"><span data-stu-id="b1098-108">Adding Properties to the Sample Audio DSP Plug-in</span></span>

<span data-ttu-id="b1098-109">Пример кода DSP, создаваемый мастером подключаемых модулей проигрывателя Windows Media, использует одно свойство, представляющее коэффициент масштабирования для звукового тома.</span><span class="sxs-lookup"><span data-stu-id="b1098-109">The audio DSP sample code that the Windows Media Player Plug-in Wizard generates uses a single property that represents the scale factor for the audio volume.</span></span> <span data-ttu-id="b1098-110">Подключаемому модулю может потребоваться более одного свойства.</span><span class="sxs-lookup"><span data-stu-id="b1098-110">Your plug-in may require more than one property.</span></span> <span data-ttu-id="b1098-111">Вы можете легко добавить свойства в подключаемый модуль DSP в Visual Studio, выполнив следующие действия:</span><span class="sxs-lookup"><span data-stu-id="b1098-111">You can easily add properties to your DSP plug-in in Visual Studio using the following steps:</span></span>

-   <span data-ttu-id="b1098-112">Определите методы в коде определения интерфейса в IDL-файле, который является частью проекта-заглушки.</span><span class="sxs-lookup"><span data-stu-id="b1098-112">Define the methods in the interface definition code in the IDL file that is part of the proxy-stub project.</span></span>
    -   <span data-ttu-id="b1098-113">Добавьте реализации методов в основной файл CPP проекта:</span><span class="sxs-lookup"><span data-stu-id="b1098-113">Add the method implementations to the project's main CPP file:</span></span>

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

    

<span data-ttu-id="b1098-114">Наконец, чтобы сделать свойства доступными для пользователя, необходимо внести изменения в реализацию страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="b1098-114">Finally, to make the properties accessible to the user, you'll want to make changes to the property page implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b1098-115">См. также</span><span class="sxs-lookup"><span data-stu-id="b1098-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1098-116">**Реализация подключаемого модуля DSP аудиоподсистемы**</span><span class="sxs-lookup"><span data-stu-id="b1098-116">**Implementing an Audio DSP Plug-in**</span></span>](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 





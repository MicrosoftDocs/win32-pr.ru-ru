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
# <a name="adding-the-wet-mix-property"></a><span data-ttu-id="e39f9-109">Добавление свойства "Mix!"</span><span class="sxs-lookup"><span data-stu-id="e39f9-109">Adding the Wet Mix Property</span></span>

<span data-ttu-id="e39f9-110">Необходимо добавить код, чтобы предоставить дополнительное свойство для уровня эффектов.</span><span class="sxs-lookup"><span data-stu-id="e39f9-110">You must add the code to provide the additional property for the effect level.</span></span>

<span data-ttu-id="e39f9-111">В разделе [Добавление свойств для примера подключаемого модуля DSP аудиоподсистемы](adding-properties-to-the-sample-audio-dsp-plug-in.md) содержатся сведения о том, как добавить новое свойство с помощью Visual C++.</span><span class="sxs-lookup"><span data-stu-id="e39f9-111">The section [Adding Properties to the Sample Audio DSP Plug-in](adding-properties-to-the-sample-audio-dsp-plug-in.md) provides details about how to add a new property using Visual C++.</span></span> <span data-ttu-id="e39f9-112">В этом разделе показано, как добавить код вручную.</span><span class="sxs-lookup"><span data-stu-id="e39f9-112">This section shows you how to add the code manually.</span></span> <span data-ttu-id="e39f9-113">Это влечет за собой добавление кода в те же три места, где был изменен код для свойства время задержки.</span><span class="sxs-lookup"><span data-stu-id="e39f9-113">This entails adding code in the same three places where you modified the code for the delay time property.</span></span>

<span data-ttu-id="e39f9-114">Добавьте прототипы для \_ методов Get ветмикс и \_ ветмикс сразу после других прототипов метода свойства в Echo. h.</span><span class="sxs-lookup"><span data-stu-id="e39f9-114">Add the prototypes for the get\_wetmix and put\_wetmix methods immediately following the other property method prototypes in Echo.h.</span></span> <span data-ttu-id="e39f9-115">Используйте следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="e39f9-115">Use the following syntax:</span></span>


```C++
STDMETHOD(get_wetmix)(double *pVal);
STDMETHOD(put_wetmix)(double newVal);

```



<span data-ttu-id="e39f9-116">Теперь добавьте реализацию для каждого метода сразу после реализации других свойств в Echo. cpp.</span><span class="sxs-lookup"><span data-stu-id="e39f9-116">Now, add the implementation for each method immediately following the other property implementations in Echo.cpp.</span></span> <span data-ttu-id="e39f9-117">В следующем примере показан код для обоих методов:</span><span class="sxs-lookup"><span data-stu-id="e39f9-117">The following example shows the code for both methods:</span></span>


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



<span data-ttu-id="e39f9-118">Обратите внимание, что реализация метода \_ ветмикс включает код для вычисления правильного значения m \_ фдримикс.</span><span class="sxs-lookup"><span data-stu-id="e39f9-118">Notice that the implementation of put\_wetmix includes the code to calculate the correct value for m\_fDryMix.</span></span> <span data-ttu-id="e39f9-119">При каждом задании нового значения для m \_ фветмикс это вычисление является обязательным.</span><span class="sxs-lookup"><span data-stu-id="e39f9-119">Each time a new value is specified for m\_fWetMix, this calculation is required.</span></span>

<span data-ttu-id="e39f9-120">Добавьте следующий код в определение интерфейса сразу после кода для методов Delay в Echo. IDL:</span><span class="sxs-lookup"><span data-stu-id="e39f9-120">Add the following code in the interface definition just after the code for the delay methods in Echo.idl:</span></span>


```C++
HRESULT get_wetmix([out] double *pVal);
HRESULT put_wetmix([in] double newVal);

```



## <a name="related-topics"></a><span data-ttu-id="e39f9-121">См. также</span><span class="sxs-lookup"><span data-stu-id="e39f9-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e39f9-122">**Свойства образца Echo**</span><span class="sxs-lookup"><span data-stu-id="e39f9-122">**Echo Sample Properties**</span></span>](echo-sample-properties.md)
</dt> </dl>

 

 





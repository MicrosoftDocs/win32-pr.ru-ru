---
title: Переменные для хранения свойств
description: Переменные для хранения свойств
ms.assetid: a90a6e21-00fb-46f8-96c8-654d8f205905
keywords:
- Подключаемые модули проигрывателя Windows Media, пример свойств Echo
- подключаемые модули, свойства образца Echo
- подключаемые модули обработки цифровых сигналов, свойства образца эха
- Подключаемые модули DSP, свойства образца Echo
- Пример подключаемого модуля "Echo DSP", свойства
- Пример подключаемого модуля "Echo DSP", переменные для хранения свойств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d252962116ba9c72464273f9c4ea1688b151898
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104258580"
---
# <a name="variables-to-store-properties"></a><span data-ttu-id="f5567-109">Переменные для хранения свойств</span><span class="sxs-lookup"><span data-stu-id="f5567-109">Variables to Store Properties</span></span>

<span data-ttu-id="f5567-110">Во-первых, для хранения времени задержки потребуется переменная.</span><span class="sxs-lookup"><span data-stu-id="f5567-110">First, you will need a variable to store the delay time.</span></span> <span data-ttu-id="f5567-111">Образец по умолчанию, созданный мастером подключаемых модулей проигрывателя Windows Media, предоставляет переменную с именем m \_ фскалефактор для хранения коэффициента масштабирования, который он использует для обработки.</span><span class="sxs-lookup"><span data-stu-id="f5567-111">The default sample created by the Windows Media Player Plug-in Wizard provides a variable named m\_fScaleFactor to store the scaling multiplier it uses for processing.</span></span> <span data-ttu-id="f5567-112">Этому примеру больше не требуется эта переменная, поэтому можно изменить ее имя и тип для хранения значения времени задержки.</span><span class="sxs-lookup"><span data-stu-id="f5567-112">This sample no longer needs this variable, so you can change its name and type to store the delay time value.</span></span>

1.  <span data-ttu-id="f5567-113">Замените каждый экземпляр m \_ фскалефактор в Echo. h и Echo. cpp на m \_ двделайтиме.</span><span class="sxs-lookup"><span data-stu-id="f5567-113">Replace each instance of m\_fScaleFactor in Echo.h and Echo.cpp with m\_dwDelayTime.</span></span>
2.  <span data-ttu-id="f5567-114">Измените тип данных m \_ фскалефактор (теперь m \_ двделайтиме) с double на DWORD в Echo. h.</span><span class="sxs-lookup"><span data-stu-id="f5567-114">Change the data type for m\_fScaleFactor (now m\_dwDelayTime) from double to DWORD in Echo.h.</span></span>
3.  <span data-ttu-id="f5567-115">В конструкторе для Цечо измените значение времени задержки по умолчанию на 1000.</span><span class="sxs-lookup"><span data-stu-id="f5567-115">In the constructor for CEcho, change the default delay time value to 1000.</span></span>
    ```C++
    m_dwDelayTime = 1000;   // Default to a delay time of 1000 ms.
    
    ```

    

<span data-ttu-id="f5567-116">Затем объявите две новые переменные члена для хранения процентного сигнала и процентного сигнала, который должен быть смешан в конечном буфере вывода.</span><span class="sxs-lookup"><span data-stu-id="f5567-116">Next, declare two new member variables to store the percentage of effect signal and the percentage of source signal to be mixed in the final output buffer.</span></span> <span data-ttu-id="f5567-117">Термин «задолженность» относится к результату, а термин «сухой» — к исходному сигналу.</span><span class="sxs-lookup"><span data-stu-id="f5567-117">The term "wet" refers to the effect, and the term "dry" refers to the source signal.</span></span> <span data-ttu-id="f5567-118">Добавьте следующие объявления в Echo. h:</span><span class="sxs-lookup"><span data-stu-id="f5567-118">Add the following declarations to Echo.h:</span></span>


```C++
double  m_fWetMix;    // percentage of effect
double  m_fDryMix;    // percentage of dry signal

```



<span data-ttu-id="f5567-119">Эти значения хранятся в виде десятичных представлений процентов, поэтому их можно легко использовать в качестве коэффициентов масштабирования.</span><span class="sxs-lookup"><span data-stu-id="f5567-119">These values are stored as decimal representations of percentages so they can easily be used as scale factors.</span></span> <span data-ttu-id="f5567-120">Например, для каждой переменной будет представлено сочетание влияния на 50 процентов и сигнала "50% источника" в виде значения 0,50.</span><span class="sxs-lookup"><span data-stu-id="f5567-120">For instance, a mixture of 50 percent effect and 50 percent source signal would be represented as a value of 0.50 for each variable.</span></span> <span data-ttu-id="f5567-121">Сумма значений для m \_ фветмикс и m \_ фдримикс не должна превышать 1,0 (100 процентов).</span><span class="sxs-lookup"><span data-stu-id="f5567-121">The sum of the values for m\_fWetMix and m\_fDryMix must not be more than 1.0 (100 percent).</span></span> <span data-ttu-id="f5567-122">Со временем эти значения будут доступны как свойства.</span><span class="sxs-lookup"><span data-stu-id="f5567-122">Eventually, these values will be accessible as properties.</span></span>

<span data-ttu-id="f5567-123">Добавьте следующий код в конструктор Цечо, чтобы задать значения по умолчанию 50 процентов.</span><span class="sxs-lookup"><span data-stu-id="f5567-123">Add the following code to the CEcho constructor to set the default values to 50 percent each:</span></span>


```C++
m_fWetMix = 0.50;  // default to 50 percent wet
m_fDryMix = 0.50;  // default to 50 percent dry

```



## <a name="related-topics"></a><span data-ttu-id="f5567-124">См. также</span><span class="sxs-lookup"><span data-stu-id="f5567-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5567-125">**Свойства образца Echo**</span><span class="sxs-lookup"><span data-stu-id="f5567-125">**Echo Sample Properties**</span></span>](echo-sample-properties.md)
</dt> </dl>

 

 





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
# <a name="implementing-cechofinalconstruct"></a><span data-ttu-id="799d2-109">Реализация Цечо:: Финалконструкт</span><span class="sxs-lookup"><span data-stu-id="799d2-109">Implementing CEcho::FinalConstruct</span></span>

<span data-ttu-id="799d2-110">Метод Цечо:: Финалконструкт реализован в Echo. cpp.</span><span class="sxs-lookup"><span data-stu-id="799d2-110">The CEcho::FinalConstruct method is implemented in Echo.cpp.</span></span> <span data-ttu-id="799d2-111">Он содержит код для чтения значений свойств из реестра, когда проигрыватель Windows Media создает экземпляр подключаемого объекта DSP.</span><span class="sxs-lookup"><span data-stu-id="799d2-111">It contains code to read the property values from the registry when Windows Media Player instantiates the DSP plug-in object.</span></span> <span data-ttu-id="799d2-112">Это важно, так как позволяет сохранять параметры пользователя между экземплярами объекта, а также между сеансами.</span><span class="sxs-lookup"><span data-stu-id="799d2-112">This is important because it allows the user settings to persist between instances of the object, as well as between sessions.</span></span> <span data-ttu-id="799d2-113">Образец кода мастера подключаемых модулей предоставляет реализацию для чтения одного свойства из реестра.</span><span class="sxs-lookup"><span data-stu-id="799d2-113">The plug-in wizard sample code provides implementation to read a single property from the registry.</span></span> <span data-ttu-id="799d2-114">Этот код можно изменить для работы со свойством время задержки, а затем добавить код для чтения значения свойства Mix.</span><span class="sxs-lookup"><span data-stu-id="799d2-114">You can modify this code to handle the delay time property, and then add code to read the wet mix property value.</span></span>

<span data-ttu-id="799d2-115">Следующий пример кода считывает каждое значение свойства из реестра и сохраняет каждый в правильной переменной члена:</span><span class="sxs-lookup"><span data-stu-id="799d2-115">The following example code reads each property value from the registry and stores each in the correct member variable:</span></span>


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



<span data-ttu-id="799d2-116">Обратите внимание, что значение DWORD для заданной позиции преобразуется в значение с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="799d2-116">Notice that the DWORD value for the wet mix is converted to a floating-point value.</span></span> <span data-ttu-id="799d2-117">Также обратите внимание, что код вычисляет правильное значение для m \_ фдримикс.</span><span class="sxs-lookup"><span data-stu-id="799d2-117">Also note that the code calculates the correct value for m\_fDryMix.</span></span>

## <a name="related-topics"></a><span data-ttu-id="799d2-118">См. также</span><span class="sxs-lookup"><span data-stu-id="799d2-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="799d2-119">**Изменение страницы свойств «пример эха»**</span><span class="sxs-lookup"><span data-stu-id="799d2-119">**Modifying the Echo Sample Property Page**</span></span>](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 





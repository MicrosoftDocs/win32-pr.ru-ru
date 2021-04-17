---
title: Реализация Цечопроппаже Онинитдиалог
description: Реализация Цечопроппаже Онинитдиалог
ms.assetid: 568989b0-bc07-480f-8b5c-41bbada713f8
keywords:
- Подключаемые модули проигрывателя Windows Media, примеры страниц свойств Echo
- страницы свойств "подключаемые модули", "Эхо-примеры"
- подключаемые модули обработки цифровых сигналов, примеры страниц свойств
- Подключаемые модули DSP, примеры страниц свойств
- Пример подключаемого модуля "Echo DSP", страницы свойств
- Пример подключаемого модуля Echo DSP, метод Цечопроппаже Онинитдиалог
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0874c750914b5caecf86ffa61a0c42d38bb1c02e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691166"
---
# <a name="implementing-cechoproppageoninitdialog"></a><span data-ttu-id="f4abf-109">Реализация Цечопроппаже:: Онинитдиалог</span><span class="sxs-lookup"><span data-stu-id="f4abf-109">Implementing CEchoPropPage::OnInitDialog</span></span>

<span data-ttu-id="f4abf-110">Метод **цечопроппаже:: онинитдиалог** реализован в ечопроппаже. cpp.</span><span class="sxs-lookup"><span data-stu-id="f4abf-110">The **CEchoPropPage::OnInitDialog** method is implemented in EchoPropPage.cpp.</span></span> <span data-ttu-id="f4abf-111">Он выполняется при вызове диалогового окна страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="f4abf-111">It executes when the property page dialog box is invoked.</span></span> <span data-ttu-id="f4abf-112">Код в этом методе должен получить текущие значения свойств и отобразить их в правильном поле ввода.</span><span class="sxs-lookup"><span data-stu-id="f4abf-112">The code in this method needs to retrieve the current property values and display them in the correct edit box.</span></span> <span data-ttu-id="f4abf-113">Образец кода мастера подключаемых модулей предоставляет реализацию для одного свойства.</span><span class="sxs-lookup"><span data-stu-id="f4abf-113">The plug-in wizard sample code provides an implementation for a single property.</span></span> <span data-ttu-id="f4abf-114">Этот код можно изменить для одного из свойств образца Echo, а затем добавить код для получения второго значения свойства.</span><span class="sxs-lookup"><span data-stu-id="f4abf-114">You can modify this code for one of the Echo sample properties, and then add code to retrieve the second property value.</span></span>

## <a name="declaring-the-oninitdialog-method-variables"></a><span data-ttu-id="f4abf-115">Объявление переменных метода Онинитдиалог</span><span class="sxs-lookup"><span data-stu-id="f4abf-115">Declaring the OnInitDialog Method Variables</span></span>

<span data-ttu-id="f4abf-116">Сначала необходимо удалить объявление Фскалефактор и заменить его следующими объявлениями переменных:</span><span class="sxs-lookup"><span data-stu-id="f4abf-116">First, you must remove the declaration of fScaleFactor and replace it with the following variable declarations:</span></span>


```
DWORD  dwDelayTime = 1000;    // Default delay time.
DWORD  dwWetmix = 50;         // Default wet mix DWORD.
double fWetmix =  0.50;       // Default wet mix double.
```



## <a name="retrieving-the-current-values-from-the-plug-in"></a><span data-ttu-id="f4abf-117">Получение текущих значений из подключаемого модуля</span><span class="sxs-lookup"><span data-stu-id="f4abf-117">Retrieving the Current Values from the Plug-in</span></span>

<span data-ttu-id="f4abf-118">Код должен затем попытаться получить текущие значения свойств из подключаемого модуля Echo.</span><span class="sxs-lookup"><span data-stu-id="f4abf-118">The code should next attempt to retrieve the current property values from the Echo plug-in.</span></span> <span data-ttu-id="f4abf-119">В следующем примере предпринимается попытка получить каждое свойство:</span><span class="sxs-lookup"><span data-stu-id="f4abf-119">The following example attempts to retrieve each property:</span></span>


```
if (m_spEcho)
{
    m_spEcho->get_delay(&dwDelayTime);
    m_spEcho->get_wetmix(&fWetmix);
    // Convert wet mix from double to DWORD.
    dwWetmix = (DWORD)(fWetmix * 100);
}
```



<span data-ttu-id="f4abf-120">Диалоговое окно отображает значение уровня эффектов для пользователя в виде целого числа, но подключаемый модуль сохраняет значение в виде числа с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="f4abf-120">The dialog box displays the effects level value to the user as an integer, but the plug-in stores the value as a floating-point number.</span></span> <span data-ttu-id="f4abf-121">Поэтому код преобразует значение с плавающей запятой в значение **типа DWORD** .</span><span class="sxs-lookup"><span data-stu-id="f4abf-121">Therefore, the code converts the floating-point value to a **DWORD** value.</span></span>

## <a name="retrieving-the-current-values-from-the-registry"></a><span data-ttu-id="f4abf-122">Получение текущих значений из реестра</span><span class="sxs-lookup"><span data-stu-id="f4abf-122">Retrieving the Current Values from the Registry</span></span>

<span data-ttu-id="f4abf-123">Если страница свойств не может получить текущие значения из подключаемого модуля, она должна попытаться прочитать их из реестра.</span><span class="sxs-lookup"><span data-stu-id="f4abf-123">If the property page cannot retrieve the current values from the plug-in, it must attempt to read them from the registry.</span></span> <span data-ttu-id="f4abf-124">Следующий код считывает каждое значение свойства:</span><span class="sxs-lookup"><span data-stu-id="f4abf-124">The following code reads each property value:</span></span>


```
else // Otherwise, read values from registry
{
    CRegKey key;
    LONG    lResult;

    lResult = key.Open(HKEY_CURRENT_USER, kszPrefsRegKey, KEY_READ);
    if (ERROR_SUCCESS == lResult)
    {
        DWORD   dwValue = 0;

        // Read the delay time.
        lResult = key.QueryValue(dwValue, kszPrefsDelayTime );
        if (ERROR_SUCCESS == lResult)
        {
            dwDelayTime = dwValue;
        }

        // Read the wet mix value.
        lResult = key.QueryValue(dwValue, kszPrefsWetmix );
        if (ERROR_SUCCESS == lResult)
        {
            dwWetmix = dwValue;
        }
    }
}
```



<span data-ttu-id="f4abf-125">Обратите внимание на использование созданных ранее констант реестра.</span><span class="sxs-lookup"><span data-stu-id="f4abf-125">Notice the use of the registry constants you created previously.</span></span>

## <a name="displaying-the-values-to-the-user"></a><span data-ttu-id="f4abf-126">Отображение значений для пользователя</span><span class="sxs-lookup"><span data-stu-id="f4abf-126">Displaying the Values to the User</span></span>

<span data-ttu-id="f4abf-127">Наконец, страница свойств должна отображать значения в соответствующих элементах управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="f4abf-127">Finally, the property page must display the values in the correct edit box controls.</span></span> <span data-ttu-id="f4abf-128">Это показано в следующем примере кода:</span><span class="sxs-lookup"><span data-stu-id="f4abf-128">The following example code demonstrates this:</span></span>


```
 TCHAR   szStr[MAXSTRING];

// Display the delay time.
_stprintf_s(szStr, MAXSTRING, _T("%u"), dwDelayTime);
SetDlgItemText(IDC_DELAYTIME, szStr);

// Display the effect level.
_stprintf_s(szStr, MAXSTRING, _T("%u"), dwWetmix);
SetDlgItemText(IDC_WETMIX, szStr);
```



## <a name="related-topics"></a><span data-ttu-id="f4abf-129">См. также</span><span class="sxs-lookup"><span data-stu-id="f4abf-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4abf-130">**Изменение страницы свойств «пример эха»**</span><span class="sxs-lookup"><span data-stu-id="f4abf-130">**Modifying the Echo Sample Property Page**</span></span>](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 





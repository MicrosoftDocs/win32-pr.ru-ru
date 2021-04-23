---
title: Реализация Цечопроппаже Apply
description: Реализация Цечопроппаже Apply
ms.assetid: e887b851-e623-4ec4-8d8b-165e4b21e116
keywords:
- Подключаемые модули проигрывателя Windows Media, примеры страниц свойств Echo
- страницы свойств "подключаемые модули", "Эхо-примеры"
- подключаемые модули обработки цифровых сигналов, примеры страниц свойств
- Подключаемые модули DSP, примеры страниц свойств
- Пример подключаемого модуля "Echo DSP", страницы свойств
- Пример подключаемого модуля Echo DSP, метод Цечопроппаже Apply
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bdca8a771d3e3e26923567f25bf7d19e968595e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888551"
---
# <a name="implementing-cechoproppageapply"></a><span data-ttu-id="5cbc8-109">Реализация Цечопроппаже:: Apply</span><span class="sxs-lookup"><span data-stu-id="5cbc8-109">Implementing CEchoPropPage::Apply</span></span>

<span data-ttu-id="5cbc8-110">Метод Цечопроппаже:: Apply реализован в Ечопроппаже. cpp.</span><span class="sxs-lookup"><span data-stu-id="5cbc8-110">The CEchoPropPage::Apply method is implemented in EchoPropPage.cpp.</span></span> <span data-ttu-id="5cbc8-111">Он выполняется, когда пользователь нажимает кнопку **Применить** в диалоговом окне страницы свойств в проигрывателе Windows Media.</span><span class="sxs-lookup"><span data-stu-id="5cbc8-111">It executes when the user clicks **Apply** in the property page dialog box in Windows Media Player.</span></span> <span data-ttu-id="5cbc8-112">Образец кода мастера подключаемых модулей предоставляет реализацию для работы с одним свойством.</span><span class="sxs-lookup"><span data-stu-id="5cbc8-112">The plug-in wizard sample code provides an implementation to handle a single property.</span></span> <span data-ttu-id="5cbc8-113">Этот код можно изменить для одного из свойств образца Echo, а затем добавить код для хранения другого значения свойства.</span><span class="sxs-lookup"><span data-stu-id="5cbc8-113">You can modify this code for one of the Echo sample properties, and then add code to store the other property value.</span></span>

## <a name="declaring-the-apply-method-variables"></a><span data-ttu-id="5cbc8-114">Объявление переменных метода Apply</span><span class="sxs-lookup"><span data-stu-id="5cbc8-114">Declaring the Apply Method Variables</span></span>

<span data-ttu-id="5cbc8-115">Сначала необходимо удалить объявление Фскалефактор.</span><span class="sxs-lookup"><span data-stu-id="5cbc8-115">First, you must remove the declaration of fScaleFactor.</span></span> <span data-ttu-id="5cbc8-116">Затем добавьте объявления переменных, которые потребуются.</span><span class="sxs-lookup"><span data-stu-id="5cbc8-116">Then, add variable declarations that you will need.</span></span> <span data-ttu-id="5cbc8-117">В следующем примере показаны завершенные объявления переменных.</span><span class="sxs-lookup"><span data-stu-id="5cbc8-117">The following example shows the completed variable declarations:</span></span>


```
TCHAR   szStr[MAXSTRING] = { 0 };
DWORD   dwDelayTime = 1000;  // Initialize the delay time.
DWORD   dwWetmix = 50;       // Initialize a DWORD for effect level.
double  fWetmix = 0.50;      // Initialize a double for effect level.
```



## <a name="retrieving-the-values-from-the-property-page"></a><span data-ttu-id="5cbc8-118">Получение значений со страницы свойств</span><span class="sxs-lookup"><span data-stu-id="5cbc8-118">Retrieving the Values from the Property Page</span></span>

<span data-ttu-id="5cbc8-119">Для получения и проверки вводимых пользователем данных необходимо реализовать код.</span><span class="sxs-lookup"><span data-stu-id="5cbc8-119">You must implement code to retrieve and validate the user input.</span></span> <span data-ttu-id="5cbc8-120">В следующем примере кода извлекается значение времени задержки из \_ поля ввода IDC DELAYTIME, а затем проверяется, находится ли значение в указанном диапазоне:</span><span class="sxs-lookup"><span data-stu-id="5cbc8-120">The following code example retrieves the delay time value from the IDC\_DELAYTIME edit box, and then verifies that the value is within a specified range:</span></span>


```
// Get the delay time value from the dialog box.
GetDlgItemText(IDC_DELAYTIME, szStr, sizeof(szStr) / sizeof(szStr[0]));

dwDelayTime = atoi(szStr);

// Make sure delay time is valid.
if ((dwDelayTime < 10) || (dwDelayTime > 2000))
{
    if (::LoadString(_Module.GetResourceInstance(), IDS_DELAYRANGEERROR, szStr, sizeof(szStr) / sizeof(szStr[0])))
    {
        MessageBox(szStr);
    }

    return E_FAIL;
}
```



<span data-ttu-id="5cbc8-121">Если введенные пользователем данные не находятся в указанном диапазоне, в коде отображается окно сообщения.</span><span class="sxs-lookup"><span data-stu-id="5cbc8-121">If the user input is not in the specified range, the code displays a message box.</span></span> <span data-ttu-id="5cbc8-122">Обратите внимание на использование строкового ресурса, созданного ранее для сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="5cbc8-122">Notice the use of the string resource you created earlier for the error message.</span></span>

<span data-ttu-id="5cbc8-123">В следующем примере уровень влияния извлекается из \_ поля ввода IDC ветмикс, а затем проверяется, находится ли значение в указанном диапазоне:</span><span class="sxs-lookup"><span data-stu-id="5cbc8-123">The following example retrieves the effect level from the IDC\_WETMIX edit box and then verifies that the value is within a specified range:</span></span>


```
// Get the effects level value from the dialog box.
GetDlgItemText(IDC_WETMIX, szStr, sizeof(szStr) / sizeof(szStr[0]));

dwWetmix = atoi(szStr);

// Make sure wet mix value is valid.
if ((dwWetmix < 0) || (dwWetmix > 100))
{
    if (::LoadString(_Module.GetResourceInstance(), IDS_MIXRANGEERROR, szStr, sizeof(szStr) / sizeof(szStr[0])))
    {
        MessageBox(szStr);
    }

    return E_FAIL;
}
```



## <a name="storing-the-property-values-in-the-registry"></a><span data-ttu-id="5cbc8-124">Сохранение значений свойств в реестре</span><span class="sxs-lookup"><span data-stu-id="5cbc8-124">Storing the Property Values in the Registry</span></span>

<span data-ttu-id="5cbc8-125">Затем код должен сохранить новые значения свойств в реестре.</span><span class="sxs-lookup"><span data-stu-id="5cbc8-125">Next, your code must persist the new property values to the registry.</span></span> <span data-ttu-id="5cbc8-126">В следующем коде хранятся оба значения свойств:</span><span class="sxs-lookup"><span data-stu-id="5cbc8-126">The following code stores both property values:</span></span>


```
// update the registry
CRegKey key;
LONG    lResult;

// Write the delay time value to the registry.
lResult = key.Create(HKEY_CURRENT_USER, kszPrefsRegKey);
if (ERROR_SUCCESS == lResult)
{
    lResult = key.SetValue( dwDelayTime , kszPrefsDelayTime );
}

// Write the wet mix value to the registry.
lResult = key.Create(HKEY_CURRENT_USER, kszPrefsRegKey);
if (ERROR_SUCCESS == lResult)
{
    lResult = key.SetValue( dwWetmix , kszPrefsWetmix );
}
```



## <a name="updating-the-echo-plug-in-property-values"></a><span data-ttu-id="5cbc8-127">Обновление значений свойств подключаемого модуля Echo</span><span class="sxs-lookup"><span data-stu-id="5cbc8-127">Updating the Echo Plug-in Property Values</span></span>

<span data-ttu-id="5cbc8-128">Метод **Apply** должен информировать подключаемый модуль Echo о том, что значения свойств изменились.</span><span class="sxs-lookup"><span data-stu-id="5cbc8-128">The **Apply** method must inform the Echo plug-in that the property values have changed.</span></span> <span data-ttu-id="5cbc8-129">Следующий код вызывает метод размещения свойства для каждого свойства с помощью указателя интерфейса, полученного в Цечопроппаже:: Сетобжектс:</span><span class="sxs-lookup"><span data-stu-id="5cbc8-129">The following code calls the property put method for each property using the interface pointer retrieved in CEchoPropPage::SetObjects:</span></span>


```
// update the plug-in
if (m_spEcho)
{
    m_spEcho->put_delay(dwDelayTime);

    // Convert the wet mix value from DWORD to double.
    fWetmix = (double)dwWetmix / 100;
    m_spEcho->put_wetmix(fWetmix);
}
```



<span data-ttu-id="5cbc8-130">Обратите внимание, что перед передачей в подключаемый модуль значение смешения задолженности преобразуется в плавающую точку.</span><span class="sxs-lookup"><span data-stu-id="5cbc8-130">Notice that the wet mix value is converted to floating point before being passed to the plug-in.</span></span>

## <a name="disabling-the-apply-button"></a><span data-ttu-id="5cbc8-131">Отключение кнопки "Применить"</span><span class="sxs-lookup"><span data-stu-id="5cbc8-131">Disabling the Apply Button</span></span>

<span data-ttu-id="5cbc8-132">В качестве завершающего шага код должен отключать Apply в диалоговом окне страницы свойств в качестве сигнала пользователю о том, что значения успешно обновлены.</span><span class="sxs-lookup"><span data-stu-id="5cbc8-132">As a final step, your code should disable Apply in the property page dialog box as a signal to the user that the values have been successfully updated.</span></span> <span data-ttu-id="5cbc8-133">Для этого требуется следующая строка кода:</span><span class="sxs-lookup"><span data-stu-id="5cbc8-133">This requires the following single line of code:</span></span>


```
m_bDirty = FALSE; // Tell the property page to disable Apply.
```



## <a name="related-topics"></a><span data-ttu-id="5cbc8-134">См. также</span><span class="sxs-lookup"><span data-stu-id="5cbc8-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5cbc8-135">**Изменение страницы свойств «пример эха»**</span><span class="sxs-lookup"><span data-stu-id="5cbc8-135">**Modifying the Echo Sample Property Page**</span></span>](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 





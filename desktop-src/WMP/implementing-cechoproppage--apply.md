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
# <a name="implementing-cechoproppageapply"></a>Реализация Цечопроппаже:: Apply

Метод Цечопроппаже:: Apply реализован в Ечопроппаже. cpp. Он выполняется, когда пользователь нажимает кнопку **Применить** в диалоговом окне страницы свойств в проигрывателе Windows Media. Образец кода мастера подключаемых модулей предоставляет реализацию для работы с одним свойством. Этот код можно изменить для одного из свойств образца Echo, а затем добавить код для хранения другого значения свойства.

## <a name="declaring-the-apply-method-variables"></a>Объявление переменных метода Apply

Сначала необходимо удалить объявление Фскалефактор. Затем добавьте объявления переменных, которые потребуются. В следующем примере показаны завершенные объявления переменных.


```
TCHAR   szStr[MAXSTRING] = { 0 };
DWORD   dwDelayTime = 1000;  // Initialize the delay time.
DWORD   dwWetmix = 50;       // Initialize a DWORD for effect level.
double  fWetmix = 0.50;      // Initialize a double for effect level.
```



## <a name="retrieving-the-values-from-the-property-page"></a>Получение значений со страницы свойств

Для получения и проверки вводимых пользователем данных необходимо реализовать код. В следующем примере кода извлекается значение времени задержки из \_ поля ввода IDC DELAYTIME, а затем проверяется, находится ли значение в указанном диапазоне:


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



Если введенные пользователем данные не находятся в указанном диапазоне, в коде отображается окно сообщения. Обратите внимание на использование строкового ресурса, созданного ранее для сообщения об ошибке.

В следующем примере уровень влияния извлекается из \_ поля ввода IDC ветмикс, а затем проверяется, находится ли значение в указанном диапазоне:


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



## <a name="storing-the-property-values-in-the-registry"></a>Сохранение значений свойств в реестре

Затем код должен сохранить новые значения свойств в реестре. В следующем коде хранятся оба значения свойств:


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



## <a name="updating-the-echo-plug-in-property-values"></a>Обновление значений свойств подключаемого модуля Echo

Метод **Apply** должен информировать подключаемый модуль Echo о том, что значения свойств изменились. Следующий код вызывает метод размещения свойства для каждого свойства с помощью указателя интерфейса, полученного в Цечопроппаже:: Сетобжектс:


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



Обратите внимание, что перед передачей в подключаемый модуль значение смешения задолженности преобразуется в плавающую точку.

## <a name="disabling-the-apply-button"></a>Отключение кнопки "Применить"

В качестве завершающего шага код должен отключать Apply в диалоговом окне страницы свойств в качестве сигнала пользователю о том, что значения успешно обновлены. Для этого требуется следующая строка кода:


```
m_bDirty = FALSE; // Tell the property page to disable Apply.
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Изменение страницы свойств «пример эха»**](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 





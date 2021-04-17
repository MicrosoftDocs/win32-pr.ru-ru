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
# <a name="implementing-cechoproppageoninitdialog"></a>Реализация Цечопроппаже:: Онинитдиалог

Метод **цечопроппаже:: онинитдиалог** реализован в ечопроппаже. cpp. Он выполняется при вызове диалогового окна страницы свойств. Код в этом методе должен получить текущие значения свойств и отобразить их в правильном поле ввода. Образец кода мастера подключаемых модулей предоставляет реализацию для одного свойства. Этот код можно изменить для одного из свойств образца Echo, а затем добавить код для получения второго значения свойства.

## <a name="declaring-the-oninitdialog-method-variables"></a>Объявление переменных метода Онинитдиалог

Сначала необходимо удалить объявление Фскалефактор и заменить его следующими объявлениями переменных:


```
DWORD  dwDelayTime = 1000;    // Default delay time.
DWORD  dwWetmix = 50;         // Default wet mix DWORD.
double fWetmix =  0.50;       // Default wet mix double.
```



## <a name="retrieving-the-current-values-from-the-plug-in"></a>Получение текущих значений из подключаемого модуля

Код должен затем попытаться получить текущие значения свойств из подключаемого модуля Echo. В следующем примере предпринимается попытка получить каждое свойство:


```
if (m_spEcho)
{
    m_spEcho->get_delay(&dwDelayTime);
    m_spEcho->get_wetmix(&fWetmix);
    // Convert wet mix from double to DWORD.
    dwWetmix = (DWORD)(fWetmix * 100);
}
```



Диалоговое окно отображает значение уровня эффектов для пользователя в виде целого числа, но подключаемый модуль сохраняет значение в виде числа с плавающей запятой. Поэтому код преобразует значение с плавающей запятой в значение **типа DWORD** .

## <a name="retrieving-the-current-values-from-the-registry"></a>Получение текущих значений из реестра

Если страница свойств не может получить текущие значения из подключаемого модуля, она должна попытаться прочитать их из реестра. Следующий код считывает каждое значение свойства:


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



Обратите внимание на использование созданных ранее констант реестра.

## <a name="displaying-the-values-to-the-user"></a>Отображение значений для пользователя

Наконец, страница свойств должна отображать значения в соответствующих элементах управления "поле ввода". Это показано в следующем примере кода:


```
 TCHAR   szStr[MAXSTRING];

// Display the delay time.
_stprintf_s(szStr, MAXSTRING, _T("%u"), dwDelayTime);
SetDlgItemText(IDC_DELAYTIME, szStr);

// Display the effect level.
_stprintf_s(szStr, MAXSTRING, _T("%u"), dwWetmix);
SetDlgItemText(IDC_WETMIX, szStr);
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Изменение страницы свойств «пример эха»**](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 





---
description: Реализация DllRegisterServer
ms.assetid: aaa4069e-0b6a-4a76-b950-1a85a9ed969d
title: Реализация DllRegisterServer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e39d55b73dd70a21c10df26a100f964917a57dd9f036ebd5c2708359bca1dd50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117998095"
---
# <a name="implementing-dllregisterserver"></a>Реализация DllRegisterServer

Последним шагом является реализация функции **DllRegisterServer** . Библиотека DLL, содержащая компонент, должна экспортировать эту функцию. Функция будет вызываться приложением настройки или при запуске пользователем средства Regsvr32.exe.

В следующем примере показана минимальная реализация **DlLRegisterServer**:


```C++
STDAPI DllRegisterServer(void)
{
    return AMovieDllRegisterServer2(TRUE);
}
```



Функция [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) создает записи реестра для каждого компонента в


```
g_Templates
```



Массив. Однако эта функция имеет некоторые ограничения. во-первых, он назначает каждый фильтр категории "DirectShow" (CLSID \_ легациамфилтеркатегори), но не все фильтры, принадлежащие к этой категории. Например, фильтры записи и фильтры сжатия имеют собственные категории. Во-вторых, если фильтр поддерживает аппаратное устройство, может потребоваться зарегистрировать два дополнительных фрагмента информации, которые **AMovieDLLRegisterServer2** не обрабатывает: *средний уровень* и *Категория ПИН-кода*. Средний уровень определяет способ связи на аппаратном устройстве, таком как шина. Категория закрепления определяет функцию ПИН-кода. сведения о средних средах см. в разделе "кспин \_ MEDIUM" в пакете средств разработки драйверов (DDK) для Microsoft Windows. Список категорий ПИН-кодов см. в разделе [закрепить набор свойств](pin-property-set.md).

Если необходимо указать категорию фильтра, среднюю или закрепление, вызовите метод [**IFilterMapper2:: регистерфилтер**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) из функции **DllRegisterServer**. Этот метод принимает указатель на структуру [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) , которая задает сведения о фильтре.

Чтобы усложнить важность, структура **REGFILTER2** поддерживает два разных формата для регистрации ПИН-кодов. Элемент **двверсион** задает формат:

-   Если **двверсион** имеет значение 1, то формат ПИН-кода — **амовиесетуп \_ PIN** (описанный выше).
-   Если **двверсион** имеет значение 2, то формат ПИН-кода — [**REGFILTERPINS2**](/windows/desktop/api/strmif/ns-strmif-regfilterpins2).

Структура **REGFILTERPINS2** включает записи для средних и контактных категорий. Кроме того, в нем используются битовые флаги для некоторых элементов, которые **амовиесетуп \_ закрепить** как логические значения.

В следующем примере показано, как вызвать **IFilterMapper2:: регистерфилтер** из функции **DllRegisterServer**:


```C++
REGFILTER2 rf2FilterReg = {
    1,              // Version 1 (no pin mediums or pin category).
    MERIT_NORMAL,   // Merit.
    1,              // Number of pins.
    &sudPins        // Pointer to pin information.
};

STDAPI DllRegisterServer(void)
{
    HRESULT hr;
    IFilterMapper2 *pFM2 = NULL;

    hr = AMovieDllRegisterServer2(TRUE);
    if (FAILED(hr))
        return hr;

    hr = CoCreateInstance(CLSID_FilterMapper2, NULL, CLSCTX_INPROC_SERVER,
            IID_IFilterMapper2, (void **)&pFM2);

    if (FAILED(hr))
        return hr;

    hr = pFM2->RegisterFilter(
        CLSID_SomeFilter,                // Filter CLSID. 
        g_wszName,                       // Filter name.
        NULL,                            // Device moniker. 
        &CLSID_VideoCompressorCategory,  // Video compressor category.
        g_wszName,                       // Instance data.
        &rf2FilterReg                    // Pointer to filter information.
    );
    pFM2->Release();
    return hr;
}
```



 

 




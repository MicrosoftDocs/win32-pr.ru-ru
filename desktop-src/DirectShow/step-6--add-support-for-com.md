---
description: Шаг 6.
ms.assetid: 53e4f5b7-c85d-4b44-9a0c-0ad05ca872cc
title: Шаг 6. Добавление поддержки для COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e477cc22650604bce623874c0afbba1063609e44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684127"
---
# <a name="step-6-add-support-for-com"></a>Шаг 6. Добавление поддержки для COM

Это шаг 6 учебника [Создание фильтров преобразования](writing-transform-filters.md).

Последним шагом является добавление поддержки COM.

## <a name="reference-counting"></a>Подсчет ссылок

Реализовывать [**IUnknown:: AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) или [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)не требуется. Все классы фильтров и закрепления являются производными от [**кункновн**](cunknown.md), который обрабатывает подсчет ссылок.

## <a name="queryinterface"></a>QueryInterface

Все классы фильтров и закрепления реализуют [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) для всех COM-интерфейсов, которые они наследуют. Например, [**ктрансформфилтер**](ctransformfilter.md) наследует [**Ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) (через [**кбасефилтер**](cbasefilter.md)). Если фильтр не предоставляет никаких дополнительных интерфейсов, никаких других действий не требуется.

Чтобы предоставить дополнительные интерфейсы, переопределите метод [**кункновн:: нонделегатингкуеринтерфаце**](cunknown-nondelegatingqueryinterface.md) . Например, предположим, что фильтр реализует пользовательский интерфейс с именем Имикустоминтерфаце. Чтобы предоставить этот интерфейс клиентам, выполните следующие действия.

-   Создайте производный класс фильтра от этого интерфейса.
-   Вставьте макрос [**Declare \_ IUnknown**](declare-iunknown.md) в раздел объявления public.
-   Переопределите [**нонделегатингкуеринтерфаце**](cunknown-nondelegatingqueryinterface.md) , чтобы проверить идентификатор IID интерфейса и вернуть указатель на фильтр.

В следующем коде показаны следующие шаги.


```C++
CMyFilter : public CBaseFilter, public IMyCustomInterface
{
public:
    DECLARE_IUNKNOWN
    STDMETHODIMP NonDelegatingQueryInterface(REFIID iid, void **ppv);
};
STDMETHODIMP CMyFilter::NonDelegatingQueryInterface(REFIID iid, void **ppv)
{
    if (riid == IID_IMyCustomInterface) {
        return GetInterface(static_cast<IMyCustomInterface*>(this), ppv);
    }
    return CBaseFilter::NonDelegatingQueryInterface(riid,ppv);
}
```



Дополнительные сведения см. [в разделе Реализация IUnknown](how-to-implement-iunknown.md).

## <a name="object-creation"></a>Создание объектов

Если вы планируете упаковать фильтр в библиотеке DLL и сделаете его доступным для других клиентов, необходимо поддерживать [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) и другие связанные функции COM. Основная библиотека классов реализует большую часть этого. Вам нужно просто предоставить некоторую информацию о фильтре. В этом разделе приводится краткий обзор действий. Дополнительные сведения см. [в разделе Создание библиотеки DLL фильтра DirectShow](how-to-create-a-dll.md).

Сначала напишите статический метод класса, который возвращает новый экземпляр фильтра. Этот метод можно назвать любым, но подпись должна соответствовать показанной в следующем примере:


```C++
CUnknown * WINAPI CRleFilter::CreateInstance(LPUNKNOWN pUnk, HRESULT *pHr)
{
    CRleFilter *pFilter = new CRleFilter();
    if (pFilter== NULL) 
    {
        *pHr = E_OUTOFMEMORY;
    }
    return pFilter;
}
```



Затем объявите глобальный массив экземпляров класса [**кфакторитемплате**](cfactorytemplate.md) с именем *g \_ Templates*. Каждый класс **кфакторитемплате** содержит сведения о реестре для одного фильтра. Несколько фильтров могут находиться в одной библиотеке DLL. просто включите дополнительные записи **кфакторитемплате** . Можно также объявить другие COM-объекты, например страницы свойств.


```C++
static WCHAR g_wszName[] = L"My RLE Encoder";
CFactoryTemplate g_Templates[] = 
{
  { 
    g_wszName,
    &CLSID_RLEFilter,
    CRleFilter::CreateInstance,
    NULL,
    NULL
  }
};
```



Определите глобальное целое число с именем *g \_ ктемплатес* , значение которого равно длине массива *\_ шаблонов g* :


```C++
int g_cTemplates = sizeof(g_Templates) / sizeof(g_Templates[0]);  
```



Наконец, реализуйте функции регистрации DLL. В следующем примере показана минимальная реализация для этих функций:


```C++
STDAPI DllRegisterServer()
{
    return AMovieDllRegisterServer2( TRUE );
}
STDAPI DllUnregisterServer()
{
    return AMovieDllRegisterServer2( FALSE );
}
```



## <a name="filter-registry-entries"></a>Фильтрация записей реестра

В предыдущих примерах показано, как зарегистрировать CLSID фильтра для COM. Для многих фильтров это достаточно. Затем клиент должен создать фильтр с помощью [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) и добавить его в граф фильтра, вызвав [**Ифилтерграф:: аддфилтер**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter). Однако в некоторых случаях может потребоваться предоставить дополнительные сведения о фильтре в реестре. Эта информация выполняет следующие действия.

-   Позволяет клиентам обнаруживать фильтр с помощью модуля [сопоставления фильтров](filter-mapper.md) или [перечислителя системных устройств](system-device-enumerator.md).
-   Позволяет диспетчеру графа фильтров обнаруживать фильтр во время автоматического построения графа.

В следующем примере фильтр кодировщика RLE регистрируется в категории Video компрессор. Дополнительные сведения см. [в разделе Регистрация фильтров DirectShow](how-to-register-directshow-filters.md). Обязательно ознакомьтесь с [рекомендациями](guidelines-for-registering-filters.md)по регистрации фильтров, которые описывают рекомендации по регистрации фильтров.


```C++
// Declare media type information.
FOURCCMap fccMap = FCC('MRLE'); 
REGPINTYPES sudInputTypes = { &MEDIATYPE_Video, &GUID_NULL };
REGPINTYPES sudOutputTypes = { &MEDIATYPE_Video, (GUID*)&fccMap };

// Declare pin information.
REGFILTERPINS sudPinReg[] = {
    // Input pin.
    { 0, FALSE, // Rendered?
         FALSE, // Output?
         FALSE, // Zero?
         FALSE, // Many?
         0, 0, 
         1, &sudInputTypes  // Media types.
    },
    // Output pin.
    { 0, FALSE, // Rendered?
         TRUE, // Output?
         FALSE, // Zero?
         FALSE, // Many?
         0, 0, 
         1, &sudOutputTypes      // Media types.
    }
};
 
// Declare filter information.
REGFILTER2 rf2FilterReg = {
    1,                // Version number.
    MERIT_DO_NOT_USE, // Merit.
    2,                // Number of pins.
    sudPinReg         // Pointer to pin information.
};

STDAPI DllRegisterServer(void)
{
    HRESULT hr = AMovieDllRegisterServer2(TRUE);
    if (FAILED(hr))
    {
        return hr;
    }
    IFilterMapper2 *pFM2 = NULL;
    hr = CoCreateInstance(CLSID_FilterMapper2, NULL, CLSCTX_INPROC_SERVER,
            IID_IFilterMapper2, (void **)&pFM2);
    if (SUCCEEDED(hr))
    {
        hr = pFM2->RegisterFilter(
            CLSID_RLEFilter,                // Filter CLSID. 
            g_wszName,                       // Filter name.
            NULL,                            // Device moniker. 
            &CLSID_VideoCompressorCategory,  // Video compressor category.
            g_wszName,                       // Instance data.
            &rf2FilterReg                    // Filter information.
            );
        pFM2->Release();
    }
    return hr;
}

STDAPI DllUnregisterServer()
{
    HRESULT hr = AMovieDllRegisterServer2(FALSE);
    if (FAILED(hr))
    {
        return hr;
    }
    IFilterMapper2 *pFM2 = NULL;
    hr = CoCreateInstance(CLSID_FilterMapper2, NULL, CLSCTX_INPROC_SERVER,
            IID_IFilterMapper2, (void **)&pFM2);
    if (SUCCEEDED(hr))
    {
        hr = pFM2->UnregisterFilter(&CLSID_VideoCompressorCategory, 
            g_wszName, CLSID_RLEFilter);
        pFM2->Release();
    }
    return hr;
}
```



Кроме того, не обязательно упаковывать фильтры в библиотеки DLL. В некоторых случаях можно написать специальный фильтр, предназначенный только для конкретного приложения. В этом случае можно скомпилировать класс фильтра непосредственно в приложении и создать его с помощью `new` оператора, как показано в следующем примере:


```C++
#include "MyFilter.h"  // Header file that declares the filter class.
// Compile and link MyFilter.cpp.
int main()
{
    IBaseFilter *pFilter = 0;
    {
        // Scope to hide pF.
        CMyFilter* pF = new MyFilter();
        if (!pF)
        {
            printf("Could not create MyFilter.\n");
            return 1;
        }
        pF->QueryInterface(IID_IBaseFilter, 
            reinterpret_cast<void**>(&pFilter));
    }
    
    /* Now use pFilter as normal. */
    
    pFilter->Release();  // Deletes the filter.
    return 0;
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Интеллектуальное подключение](intelligent-connect.md)
</dt> <dt>

[Написание фильтров DirectShow](writing-directshow-filters.md)
</dt> <dt>

[Написание фильтров преобразования](writing-transform-filters.md)
</dt> </dl>

 

 

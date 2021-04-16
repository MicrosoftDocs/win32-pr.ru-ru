---
description: Использование перечислителя системных устройств
ms.assetid: 70db139c-2c5b-4574-bec3-dfe758b16715
title: Использование перечислителя системных устройств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88f8f66cb64e9f7bb51d6b0716b9fa23cf531435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104557454"
---
# <a name="using-the-system-device-enumerator"></a>Использование перечислителя системных устройств

Перечислитель системных устройств обеспечивает единообразный способ перечисления по категориям фильтров, зарегистрированных в системе пользователя. Кроме того, он различает отдельные аппаратные устройства, даже если один и тот же фильтр поддерживает их. Это особенно полезно для устройств, использующих WDM (WDM) и фильтр Кспрокси. Например, у пользователя может быть несколько устройств записи видео WDM, которые поддерживаются одним и тем же фильтром. Перечислитель системных устройств обрабатывает их как отдельные экземпляры устройств.

Перечислитель системных устройств работает путем создания перечислителя для определенной категории, например для записи звука или сжатия видео. Перечислитель категорий Возвращает уникальный моникер для каждого устройства в категории. Перечислитель категорий автоматически включает в категорию все соответствующие самонастраивающийся устройства. Список категорий см. в разделе [Фильтрация категорий](filter-categories.md).

Чтобы использовать перечислитель системных устройств, выполните следующие действия.

1.  Создайте перечислитель системных устройств, вызвав **CoCreateInstance**. Идентификатор класса (CLSID) — это CLSID \_ системдевицеенум.
2.  Получите перечислитель категорий, вызвав [**икреатедевенум:: креатеклассенумератор**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) с идентификатором CLSID нужной категории. Этот метод возвращает указатель интерфейса **иенуммоникер** . Если категория пуста (или не существует), метод возвращает значение S false, \_ а не код ошибки. Если это так, возвращаемый указатель **иенуммоникер** будет **иметь значение NULL** и разыменование этого указателя вызовет исключение. Таким образом, \_ при вызове **креатеклассенумератор** явным образом проверяйте, что вместо вызова обычного макроса с **успехом** .
3.  Используйте метод **иенуммоникер:: Next** для перечисления каждого моникера. Этот метод возвращает указатель интерфейса **IMoniker** . Когда **следующий** метод достигает конца перечисления, он также возвращает \_ значение false, поэтому еще раз проверьте наличие \_ ОК.
4.  Чтобы получить понятное имя устройства (например, для вывода в пользовательском интерфейсе), вызовите метод **IMoniker:: биндтостораже** .
5.  Чтобы создать и инициализировать фильтр DirectShow, управляющий устройством, вызовите **IMoniker:: биндтубжект** в моникере. Вызовите [**ифилтерграф:: аддфилтер**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) , чтобы добавить фильтр в граф.

Этот процесс представлен на схеме ниже.

![Перечисление устройств](images/sysdevenum.png)

В следующем примере показано, как перечислить Видеокомпрессоры, установленные в системе пользователя. Для краткости в примере выполняется минимальная проверка ошибок.


```C++
// Create the System Device Enumerator.
HRESULT hr;
ICreateDevEnum *pSysDevEnum = NULL;
hr = CoCreateInstance(CLSID_SystemDeviceEnum, NULL, CLSCTX_INPROC_SERVER,
    IID_ICreateDevEnum, (void **)&pSysDevEnum);
if (FAILED(hr))
{
    return hr;
}

// Obtain a class enumerator for the video compressor category.
IEnumMoniker *pEnumCat = NULL;
hr = pSysDevEnum->CreateClassEnumerator(CLSID_VideoCompressorCategory, &pEnumCat, 0);

if (hr == S_OK) 
{
    // Enumerate the monikers.
    IMoniker *pMoniker = NULL;
    ULONG cFetched;
    while(pEnumCat->Next(1, &pMoniker, &cFetched) == S_OK)
    {
        IPropertyBag *pPropBag;
        hr = pMoniker->BindToStorage(0, 0, IID_IPropertyBag, 
            (void **)&pPropBag);
        if (SUCCEEDED(hr))
        {
            // To retrieve the filter's friendly name, do the following:
            VARIANT varName;
            VariantInit(&varName);
            hr = pPropBag->Read(L"FriendlyName", &varName, 0);
            if (SUCCEEDED(hr))
            {
                // Display the name in your UI somehow.
            }
            VariantClear(&varName);

            // To create an instance of the filter, do the following:
            IBaseFilter *pFilter;
            hr = pMoniker->BindToObject(NULL, NULL, IID_IBaseFilter,
                (void**)&pFilter);
            // Now add the filter to the graph. 
            //Remember to release pFilter later.
            pPropBag->Release();
        }
        pMoniker->Release();
    }
    pEnumCat->Release();
}
pSysDevEnum->Release();
```



**Моникеры устройств**

Для моникеров устройств можно передать моникер методу [**IFilterGraph2:: аддсаурцефилтерформоникер**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-addsourcefilterformoniker) , чтобы создать фильтр записи для устройства. Пример кода см. в документации по этому методу.

Метод **IMoniker:: DisplayName** Возвращает отображаемое имя моникера. Хотя отображаемое имя доступно для чтения, оно обычно не отображается для конечного пользователя. Вместо этого получите понятное имя из контейнера свойств, как описано выше.

Метод **IMoniker::P арседисплайнаме** или функция **мкпарседисплайнаме** можно использовать для создания моникера устройства по умолчанию для данной категории фильтра. Используйте отображаемое имя в форме `@device:*:{category-clsid}` , где `category-clsid` — строковое представление GUID категории. Моникер по умолчанию является первым моникером, возвращенным перечислителем устройства для этой категории.

 

 




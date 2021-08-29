---
description: Перечисление эффектов и переходов
ms.assetid: 364b7bfb-5d6e-4ca6-b0c8-7a0180c3f61a
title: Перечисление эффектов и переходов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd94dee9ff6774e9608d6b599986c0b943b60d335df2ab9b27e8c2eb64d7fe42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685814"
---
# <a name="enumerating-effects-and-transitions"></a>Перечисление эффектов и переходов

\[Этот API не поддерживается и может быть изменен или недоступен в будущем.\]

DirectShow предоставляет объект [перечислителя системных устройств](system-device-enumerator.md) для перечисления устройств. Его можно использовать для получения моникеров для эффектов или переходов, установленных в системе пользователя.

Перечислитель системных устройств предоставляет интерфейс [**икреатедевенум**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) . Он возвращает перечислители категорий для указанных категорий устройств. Перечислитель категорий, в свою очередь, предоставляет интерфейс [**иенуммоникер**](/windows/desktop/api/objidl/nn-objidl-ienummoniker) и возвращает моникеры для каждого устройства в категории. Подробное описание использования **икреатедевенум** см. в разделе [Перечисление устройств и фильтров](enumerating-devices-and-filters.md). ниже приведен краткий обзор, относящийся к DirectShow служб редактирования.

Чтобы перечислить эффекты или переходы, выполните следующие действия.

1.  Создайте экземпляр перечислителя системных устройств.
2.  Вызовите метод [**икреатедевенум:: креатеклассенумератор**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) , чтобы получить перечислитель категорий. Категории определяются идентификаторами классов (CLSID). Используйте CLSID \_ VideoEffects1Category для эффектов или CLSID \_ VideoEffects2Category для переходов.
3.  Вызовите метод **иенуммоникер:: Next** , чтобы получить все моникеры в перечислении.
4.  Для каждого моникера вызовите **IMoniker:: биндтостораже** , чтобы получить связанный с ним контейнер свойств.

Контейнер свойств содержит понятное имя и глобальный уникальный идентификатор (GUID) для действия или перехода. Приложение может отобразить список понятных имен, а затем получить соответствующий идентификатор GUID.

Эти шаги показаны в следующем примере кода.


```C++
ICreateDevEnum *pCreateDevEnum = NULL;
IEnumMoniker *pEnumMoniker = NULL;

// Create the System Device Enumerator.
HRESULT hr = CoCreateInstance(CLSID_SystemDeviceEnum, NULL, 
    CLSCTX_INPROC_SERVER, IID_ICreateDevEnum, (void**)&pCreateDevEnum);
if (FAILED(hr))
{
    // Error handling omitted for clarity.
}

// Create an enumerator for the video effects category.
hr = pCreateDevEnum->CreateClassEnumerator(
    CLSID_VideoEffects1Category,  // Video effects category. 
    &pEnumMoniker, 0);               

// Note: Use CLSID_VideoEffects2Category for video transitions.

if (hr == S_OK)  // S_FALSE means the category is empty.
{
    // Enumerate each video effect.
    IMoniker *pMoniker;
    while (S_OK == pEnumMoniker->Next(1, &pMoniker, NULL))
    {
        IPropertyBag *pBag;
        hr = pMoniker->BindToStorage(0, 0, IID_IPropertyBag, 
            (void **)&pBag);
        if(FAILED(hr))
        {
            pMoniker->Release();
            continue; // Maybe the next one will work.
        }
        VARIANT var;
        VariantInit(&var);
        hr = pBag->Read(OLESTR("FriendlyName"), &var, NULL);
        if (SUCCEEDED(hr))
        {
            if ( ... )  // Check if var.bstrVal is the name you want.
            {
                VARIANT var2;
                GUID guid;
                var2.vt = VT_BSTR;
                pBag->Read(OLESTR("guid"), &var2, NULL);
                CLSIDFromString(var2.bstrVal, &guid);
                VariantClear(&var2);
                // GUID is now the CLSID for the effect.
            }
        }
        VariantClear(&var);
        pBag->Release();
        pMoniker->Release();
    }
    pEnumMoniker->Release();
}
pCreateDevEnum->Release();
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Работа с эффектами и переходами](working-with-effects-and-transitions.md)
</dt> </dl>

 

 

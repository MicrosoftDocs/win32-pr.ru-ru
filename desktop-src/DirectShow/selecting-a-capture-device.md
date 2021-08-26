---
description: Выбор устройства записи
ms.assetid: 8f92873d-569a-48af-a913-6d4cce65640f
title: Выбор устройства записи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5bf92692070c8a0191a91559481d5446bf3d4d894c8e7f6aafc2ed9e73a6667
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904414"
---
# <a name="selecting-a-capture-device"></a>Выбор устройства записи

Чтобы выбрать устройство для захвата аудио или видео, используйте [перечислитель системных устройств](system-device-enumerator.md), описанный в разделе [Использование перечислителя системных устройств](using-the-system-device-enumerator.md). Перечислитель системных устройств Возвращает коллекцию моникеров устройств, выбранную категорией устройств. *Моникер* — это COM-объект, который содержит сведения о другом объекте. Моникеры позволяют приложению получать сведения об объекте без фактического создания объекта. Позже приложение может использовать моникер для создания объекта. Дополнительные сведения об моникерах см. в документации по [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker).

Чтобы использовать перечислитель системных устройств, выполните следующие действия.

1.  Вызовите [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) , чтобы создать экземпляр перечислителя системных устройств.
2.  Вызовите [**икреатедевенум:: креатеклассенумератор**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) и укажите категорию устройства в виде идентификатора GUID. Для устройств записи важны следующие категории. 

    | GUID категории                       | Описание           |
    |-------------------------------------|-----------------------|
    | **\_АУДИОИНПУТДЕВИЦЕКАТЕГОРИ CLSID** | Устройства записи звука |
    | **\_ВИДЕОИНПУТДЕВИЦЕКАТЕГОРИ CLSID** | Устройства видеозаписи |

    

     

    Если видеокамера имеет встроенный микрофон, она отображается в обеих категориях. Однако Камера и микрофон обрабатываются системой как отдельные устройства для перечисления, создания устройств и потоковой передачи данных.

3.  Метод [**креатеклассенумератор**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) возвращает указатель на интерфейс [**иенуммоникер**](/windows/win32/api/objidl/nn-objidl-ienummoniker) . Чтобы перечислить моникеры, вызовите метод [**иенуммоникер:: Next**](/windows/win32/api/objidl/nf-objidl-ienummoniker-next).

Следующий код создает перечислитель для указанной категории устройств.


```C++
#include <windows.h>
#include <dshow.h>

#pragma comment(lib, "strmiids")

HRESULT EnumerateDevices(REFGUID category, IEnumMoniker **ppEnum)
{
    // Create the System Device Enumerator.
    ICreateDevEnum *pDevEnum;
    HRESULT hr = CoCreateInstance(CLSID_SystemDeviceEnum, NULL,  
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pDevEnum));

    if (SUCCEEDED(hr))
    {
        // Create an enumerator for the category.
        hr = pDevEnum->CreateClassEnumerator(category, ppEnum, 0);
        if (hr == S_FALSE)
        {
            hr = VFW_E_NOT_FOUND;  // The category is empty. Treat as an error.
        }
        pDevEnum->Release();
    }
    return hr;
}
```



Интерфейс [**иенуммоникер**](/windows/win32/api/objidl/nn-objidl-ienummoniker) перечисляет список интерфейсов [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) , каждый из которых представляет моникер устройства. приложение может считывать свойства из моникера или использовать моникер для создания DirectShow фильтра записи для устройства. Свойства моникера возвращаются в виде значений **типа Variant** . Специальные имена устройств поддерживают следующие свойства.



| Свойство       | Описание                                                               | Тип VARIANT |
|----------------|---------------------------------------------------------------------------|--------------|
| FriendlyName | Название устройства.                                                   | **VT \_ BSTR** |
| Nописание  | Описание устройства.                                              | **VT \_ BSTR** |
| Измените   | Уникальная строка, идентифицирующая устройство. (Только устройства записи видео.) | **VT \_ BSTR** |
| "Вавеинид"     | Идентификатор устройства аудиозаписи. (Только для устройств записи звука.) | **VT \_ I4**   |



 

Свойства "FriendlyName" и "Description" подходят для отображения в пользовательском интерфейсе.

-   Свойство "FriendlyName" доступно для каждого устройства. Он содержит удобное для чтения имя устройства.
-   Свойство "Description" доступно только для устройств с видеокамерой DV и D-ВХС/MPEG. Дополнительные сведения см. в разделе [драйвер мсдв](msdv-driver.md) и [драйвер мстапе](mstape-driver.md). Если он доступен, он содержит описание устройства, более конкретное, чем свойство "FriendlyName". Обычно он включает имя поставщика.
-   Свойство DevicePath не является удобной для чтения строкой, но гарантирует уникальность для каждого устройства видеозаписи в системе. Это свойство можно использовать для различения двух или более экземпляров одной и той же модели устройства.
-   если имеется свойство "вавеинид", это означает, что фильтр записи DirectShow использует для взаимодействия с устройством интерфейсы api [аудио Audio](../multimedia/waveform-audio.md) . Значение свойства "Вавеинид" соответствует идентификатору, используемому функциями **Wave \** _, например, [_ *вавеинопен* *](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen).

Чтобы прочитать свойства моникера, выполните следующие действия.

1.  Вызовите метод [**IMoniker:: биндтостораже**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage) , чтобы получить указатель на интерфейс [**ипропертибаг**](../com/ipropertybag-and-ipersistpropertybag.md) .
2.  Чтобы прочитать свойство, вызовите метод **ипропертибаг:: Read** .

В следующем примере кода показано, как перечислить список моникеров устройств и получить свойства.


```C++
void DisplayDeviceInformation(IEnumMoniker *pEnum)
{
    IMoniker *pMoniker = NULL;

    while (pEnum->Next(1, &pMoniker, NULL) == S_OK)
    {
        IPropertyBag *pPropBag;
        HRESULT hr = pMoniker->BindToStorage(0, 0, IID_PPV_ARGS(&pPropBag));
        if (FAILED(hr))
        {
            pMoniker->Release();
            continue;  
        } 

        VARIANT var;
        VariantInit(&var);

        // Get description or friendly name.
        hr = pPropBag->Read(L"Description", &var, 0);
        if (FAILED(hr))
        {
            hr = pPropBag->Read(L"FriendlyName", &var, 0);
        }
        if (SUCCEEDED(hr))
        {
            printf("%S\n", var.bstrVal);
            VariantClear(&var); 
        }

        hr = pPropBag->Write(L"FriendlyName", &var);

        // WaveInID applies only to audio capture devices.
        hr = pPropBag->Read(L"WaveInID", &var, 0);
        if (SUCCEEDED(hr))
        {
            printf("WaveIn ID: %d\n", var.lVal);
            VariantClear(&var); 
        }

        hr = pPropBag->Read(L"DevicePath", &var, 0);
        if (SUCCEEDED(hr))
        {
            // The device path is not intended for display.
            printf("Device path: %S\n", var.bstrVal);
            VariantClear(&var); 
        }

        pPropBag->Release();
        pMoniker->Release();
    }
}

void main()
{
    HRESULT hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
    if (SUCCEEDED(hr))
    {
        IEnumMoniker *pEnum;

        hr = EnumerateDevices(CLSID_VideoInputDeviceCategory, &pEnum);
        if (SUCCEEDED(hr))
        {
            DisplayDeviceInformation(pEnum);
            pEnum->Release();
        }
        hr = EnumerateDevices(CLSID_AudioInputDeviceCategory, &pEnum);
        if (SUCCEEDED(hr))
        {
            DisplayDeviceInformation(pEnum);
            pEnum->Release();
        }
        CoUninitialize();
    }
}
```



чтобы создать фильтр записи DirectShow для устройства, вызовите метод [**IMoniker:: биндтубжект**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject) , чтобы получить указатель [**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) . Затем вызовите [**ифилтерграф:: аддфилтер**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) , чтобы добавить фильтр в граф фильтра:


```C++
IBaseFilter *pCap = NULL;
hr = pMoniker->BindToObject(0, 0, IID_IBaseFilter, (void**)&pCap);
if (SUCCEEDED(hr))
{
    hr = m_pGraph->AddFilter(pCap, L"Capture Filter");
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Запись звука](audio-capture.md)
</dt> <dt>

[Видеозапись](video-capture.md)
</dt> </dl>

 

 

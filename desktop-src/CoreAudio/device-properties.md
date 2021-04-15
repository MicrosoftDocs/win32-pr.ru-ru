---
description: Свойства устройства
ms.assetid: ad8753ba-ad20-4122-b0f2-eb165f98db67
title: Свойства устройства (API-интерфейсы Core Audio)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14a868e4bb806bd49d934febed164bcd70fba39f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655626"
---
# <a name="device-properties-core-audio-apis"></a>Свойства устройства (API-интерфейсы Core Audio)

В процессе перечисления [устройств конечных точек звука](audio-endpoint-devices.md)клиентское приложение может опрашивать объекты конечной точки для их свойств устройства. Свойства устройства предоставляются в реализации интерфейса **ИПРОПЕРТИСТОРЕ** API ммдевице. При наличии ссылки на интерфейс [**иммдевице**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) объекта конечной точки клиент может получить ссылку на хранилище свойств объекта конечной точки, вызвав метод [**Иммдевице:: опенпропертисторе**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) .

Объект-хранилище свойств предоставляет интерфейс **ипропертисторе** . Два основных метода в этом интерфейсе — **ипропертисторе:: GetValue**, который получает значение свойства устройства, и **Ипропертисторе:: SetValue**, который задает значение свойства устройства. Дополнительные сведения о **ипропертисторе** см. в документации по Windows SDK.

Реализация Ммдевице API хранилища свойств отличается от объекта стандартного хранилища свойств оболочки. Чтобы изменить значение свойства, клиентское приложение должно вызвать метод **ипропертисторе:: SetValue** . Во время этого вызова новые значения задаются и записываются в реестр. Поэтому приложению не нужно вызывать метод **ипропертисторе:: Commit** после вызова **SetValue** . Дескриптор реестра закрывается только в том случае, если клиент освобождает указатель интерфейса.

Как правило, клиентские приложения сторонних производителей вызывают метод **GetValue** , но не метод **SetValue** . Диспетчер конечных точек задает основные свойства устройства для конечных узлов. Диспетчер конечных точек — это компонент Windows Vista, который отвечает за обнаружение наличия устройств конечных точек звука.

Каждый \_ идентификатор свойства PKEY XXX в следующем списке является константой типа **PROPERTYKEY** , которая определена в файле заголовка функтиондисковерикэйс \_ девпкэй. h. Все устройства конечных точек аудио имеют три свойства устройства.



| Свойство                                                                         | Описание                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PKEY \_ девицеинтерфаце \_ FriendlyName**](pkey-deviceinterface-friendlyname.md) | Понятное имя звукового адаптера, к которому подключено устройство конечной точки (например, "XYZ Audio Adapter"). **Пропвариант** Member **VT** имеет значение VT \_ LPWSTR, а Member **пвсзвал** указывает на строку расширенных символов, заканчивающуюся символом NULL, которая содержит понятное имя. |
| [**\_Девицедеск устройства \_ PKEY**](pkey-device-devicedesc.md)                       | Описание устройства конечной точки (например, "динамики"). **Пропвариант** Member **VT** имеет значение VT \_ LPWSTR, а Member **пвсзвал** указывает на строку расширенных символов, заканчивающуюся символом NULL, содержащую описание устройства.                                       |
| [**PKEY \_ устройство \_ FriendlyName**](pkey-device-friendlyname.md)                   | Понятное имя устройства конечной точки (например, "динамики (аудио-адаптер XYZ)"). **Пропвариант** Member **VT** имеет значение VT \_ LPWSTR, а Member **пвсзвал** указывает на строку расширенных символов, заканчивающуюся символом NULL, которая содержит понятное имя.                             |



 

Некоторые устройства конечных точек звука могут иметь дополнительные свойства, которые не отображаются в приведенном выше списке. Дополнительные сведения о дополнительных свойствах см. в разделе [свойства конечной точки аудио](audio-endpoint-properties.md). Дополнительные сведения о **PROPERTYKEY** см. в документации по Windows SDK.

В следующем примере кода выводятся отображаемые имена всех устройств конечной точки отрисовки звука в системе:


```C++
//-----------------------------------------------------------
// This function enumerates all active (plugged in) audio
// rendering endpoint devices. It prints the friendly name
// and endpoint ID string of each endpoint device.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

const CLSID CLSID_MMDeviceEnumerator = __uuidof(MMDeviceEnumerator);
const IID IID_IMMDeviceEnumerator = __uuidof(IMMDeviceEnumerator);

void PrintEndpointNames()
{
    HRESULT hr = S_OK;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDeviceCollection *pCollection = NULL;
    IMMDevice *pEndpoint = NULL;
    IPropertyStore *pProps = NULL;
    LPWSTR pwszID = NULL;

    hr = CoCreateInstance(
           CLSID_MMDeviceEnumerator, NULL,
           CLSCTX_ALL, IID_IMMDeviceEnumerator,
           (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    hr = pEnumerator->EnumAudioEndpoints(
                        eRender, DEVICE_STATE_ACTIVE,
                        &pCollection);
    EXIT_ON_ERROR(hr)

    UINT  count;
    hr = pCollection->GetCount(&count);
    EXIT_ON_ERROR(hr)

    if (count == 0)
    {
        printf("No endpoints found.\n");
    }

    // Each loop prints the name of an endpoint device.
    for (ULONG i = 0; i < count; i++)
    {
        // Get pointer to endpoint number i.
        hr = pCollection->Item(i, &pEndpoint);
        EXIT_ON_ERROR(hr)

        // Get the endpoint ID string.
        hr = pEndpoint->GetId(&pwszID);
        EXIT_ON_ERROR(hr)
        
        hr = pEndpoint->OpenPropertyStore(
                          STGM_READ, &pProps);
        EXIT_ON_ERROR(hr)

        PROPVARIANT varName;
        // Initialize container for property value.
        PropVariantInit(&varName);

        // Get the endpoint's friendly-name property.
        hr = pProps->GetValue(
                       PKEY_Device_FriendlyName, &varName);
        EXIT_ON_ERROR(hr)

        // Print endpoint friendly name and endpoint ID.
        printf("Endpoint %d: \"%S\" (%S)\n",
               i, varName.pwszVal, pwszID);

        CoTaskMemFree(pwszID);
        pwszID = NULL;
        PropVariantClear(&varName);
        SAFE_RELEASE(pProps)
        SAFE_RELEASE(pEndpoint)
    }
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pCollection)
    return;

Exit:
    printf("Error!\n");
    CoTaskMemFree(pwszID);
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pCollection)
    SAFE_RELEASE(pEndpoint)
    SAFE_RELEASE(pProps)
}
```



Макрос FAILed в предыдущем примере кода определен в файле заголовка Winerror. h.

В приведенном выше примере кода тело цикла **for** в функции принтендпоинтнамес вызывает метод [**Иммдевице:: GetId**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-getid) , чтобы получить [строку идентификатора конечной](endpoint-id-strings.md) точки для устройства аудио конечных точек, представленного экземпляром интерфейса **иммдевице** . Строка уникально идентифицирует устройство по отношению ко всем другим устройствам конечных точек звука в системе. Клиент может использовать строку идентификатора конечной точки для создания экземпляра устройства конечной точки аудио в более позднее время или в другом процессе, вызвав метод [**иммдевицеенумератор::-Device**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) . Клиенты должны считать содержимое строки идентификатора конечной точки непрозрачной. То есть клиенты не должны пытаться проанализировать содержимое строки для получения сведений об устройстве. Причина в том, что формат строки не определен и может изменяться от одной реализации API Ммдевице к следующему.

Понятные имена устройств и строки ИДЕНТИФИКАТОРов конечных точек, полученные функцией Принтендпоинтнамес в предыдущем примере кода, идентичны понятным именам устройств и строкам ИДЕНТИФИКАТОРов конечных точек, предоставляемым DirectSound во время перечисления устройств. Дополнительные сведения см. в статье [события аудио для устаревших аудио приложений](audio-events-for-legacy-audio-applications.md).

В предыдущем примере кода функция Принтендпоинтнамес вызывает функцию **CoCreateInstance** , чтобы создать перечислитель для устройств конечных точек аудио в системе. Если вызывающая программа ранее не вызывала  функцию CoInitialize или **CoInitializeEx** для инициализации библиотеки COM, вызов **CoCreateInstance** завершится ошибкой. Дополнительные сведения о **CoCreateInstance**, **CoInitialize** и **CoInitializeEx** см. в документации по Windows SDK.

Дополнительные сведения об интерфейсах **иммдевицеенумератор**, **иммдевицеколлектион** и **ИММДЕВИЦЕ** см. в разделе [API ммдевице](mmdevice-api.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Устройства конечных точек звука](audio-endpoint-devices.md)
</dt> </dl>

 

 




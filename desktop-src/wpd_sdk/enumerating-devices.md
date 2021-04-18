---
title: Перечисление устройств (WPD)
description: Перечисление устройств
ms.assetid: 28ded3cf-b0c8-4c90-ab39-efc879adb6e7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2738398de7f3bfb6aa1ea88175ff30241b4dbb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693711"
---
# <a name="enumerating-devices-wpd"></a>Перечисление устройств (WPD)

Первая задача, выполненная большинством приложений, — это перечисление устройств, подключенных к компьютеру. Эта задача и получение сведений об устройстве (например, производителя, понятное имя и описание) поддерживаются интерфейсом [**ипортабледевицеманажер**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) .

Функция Енумератеаллдевицес в модуле Девицеенумератион. cpp содержит код, демонстрирующий получение количества подключенных устройств и, при получении количества, получение сведений об устройстве для каждого подключенного устройства.

Функция Енумератеаллдевицес выполняет четыре основных задачи:

1.  Создает объект диспетчера переносимых устройств.
2.  Возвращает число подключенных устройств.
3.  Извлекает сведения об устройстве (для подключенных устройств).
4.  Освобождает память, используемую при извлечении сведений об устройстве.

Каждая из этих четырех задач более подробно описана в следующих разделах.

Первым шагом в процессе перечисления устройств является создание объекта диспетчера переносимых устройств. Для этого необходимо вызвать функцию CoCreateInstance и передать идентификатор класса (CLSID) для объекта, указать контекст, в котором будет выполняться код, указать идентификатор ссылки для интерфейса Ипортабледевицеманажер, а затем указать переменную указателя, которая получает указатель интерфейса Ипортабледевицеманажер.


```C++
HRESULT hr = CoCreateInstance(CLSID_PortableDeviceManager,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(&pPortableDeviceManager));
if (FAILED(hr))
{
    printf("! Failed to CoCreateInstance CLSID_PortableDeviceManager, hr = 0x%lx\n",hr);
}
```



После получения указателя на интерфейс [**ипортабледевицеманажер**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) можно приступить к вызову методов для этого интерфейса. Первый метод, вызываемый в функции Енумератеаллдевицес, — это [**ипортабледевицеманажер::**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices)-of-Devices. При вызове этого метода с первым аргументом, имеющим значение **null**, возвращается число подключенных устройств.


```C++
if (SUCCEEDED(hr))
{
    hr = pPortableDeviceManager->GetDevices(NULL, &cPnPDeviceIDs);
    if (FAILED(hr))
    {
        printf("! Failed to get number of devices on the system, hr = 0x%lx\n",hr);
    }
}

// Report the number of devices found.  NOTE: we will report 0, if an error
// occured.

printf("\n%d Windows Portable Device(s) found on the system\n\n", cPnPDeviceIDs);
```



После получения числа подключенных устройств можно использовать это значение для получения сведений об устройстве для каждого подключенного устройства. Этот процесс начинается с передачи массива указателей строк в качестве первого аргумента и количества элементов, которые этот массив может хранить в качестве второго аргумента (это число должно быть по крайней мере равно количеству доступных устройств).

Строки, возвращаемые этим методом, являются самонастраивающийся именами подключенных устройств. Эти имена, в свою очередь, передаются другим методам в интерфейсе [**ипортабледевицеманажер**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) для получения сведений об устройстве, таких как понятное имя, имя производителя и описание устройства. (Эти имена также используются для открытия подключения к устройству, когда приложение вызывает метод [**ипортабледевице:: Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open) .)


```C++
if (SUCCEEDED(hr) && (cPnPDeviceIDs > 0))
{
    pPnpDeviceIDs = new (std::nothrow) PWSTR[cPnPDeviceIDs];
    if (pPnpDeviceIDs != NULL)
    {
        DWORD dwIndex = 0;

        hr = pPortableDeviceManager->GetDevices(pPnpDeviceIDs, &cPnPDeviceIDs);
        if (SUCCEEDED(hr))
        {
            // For each device found, display the devices friendly name,
            // manufacturer, and description strings.
            for (dwIndex = 0; dwIndex < cPnPDeviceIDs; dwIndex++)
            {
                printf("[%d] ", dwIndex);
                DisplayFriendlyName(pPortableDeviceManager, pPnpDeviceIDs[dwIndex]);
                printf("    ");
                DisplayManufacturer(pPortableDeviceManager, pPnpDeviceIDs[dwIndex]);
                printf("    ");
                DisplayDescription(pPortableDeviceManager, pPnpDeviceIDs[dwIndex]);
            }
        }
        else
        {
            printf("! Failed to get the device list from the system, hr = 0x%lx\n",hr);
        }
```



После получения сведений об устройстве необходимо освободить память, связанную со строками, на которые указывает массив указателей строк. Кроме того, необходимо удалить этот массив.


```C++
for (dwIndex = 0; dwIndex < cPnPDeviceIDs; dwIndex++)
{
    CoTaskMemFree(pPnpDeviceIDs[dwIndex]);
    pPnpDeviceIDs[dwIndex] = NULL;
}

// Delete the array of PWSTR pointers
delete [] pPnpDeviceIDs;
pPnpDeviceIDs = NULL;
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Интерфейс Ипортабледевицеманажер**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager)
</dt> <dt>

[**Инструкции по программированию**](programming-guide.md)
</dt> </dl>

 

 




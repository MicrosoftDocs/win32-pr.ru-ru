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
# <a name="enumerating-devices-wpd"></a><span data-ttu-id="322ee-103">Перечисление устройств (WPD)</span><span class="sxs-lookup"><span data-stu-id="322ee-103">Enumerating devices (WPD)</span></span>

<span data-ttu-id="322ee-104">Первая задача, выполненная большинством приложений, — это перечисление устройств, подключенных к компьютеру.</span><span class="sxs-lookup"><span data-stu-id="322ee-104">The first task completed by most applications is the enumeration of the devices connected to the computer.</span></span> <span data-ttu-id="322ee-105">Эта задача и получение сведений об устройстве (например, производителя, понятное имя и описание) поддерживаются интерфейсом [**ипортабледевицеманажер**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) .</span><span class="sxs-lookup"><span data-stu-id="322ee-105">This task, and the retrieval of device information (such as manufacturer, friendly name, and description), is supported by the [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) interface.</span></span>

<span data-ttu-id="322ee-106">Функция Енумератеаллдевицес в модуле Девицеенумератион. cpp содержит код, демонстрирующий получение количества подключенных устройств и, при получении количества, получение сведений об устройстве для каждого подключенного устройства.</span><span class="sxs-lookup"><span data-stu-id="322ee-106">The EnumerateAllDevices function in the DeviceEnumeration.cpp module contains code that demonstrates the retrieval of the count of connected devices and, once the count is retrieved, the retrieval of device-specific information for each connected device.</span></span>

<span data-ttu-id="322ee-107">Функция Енумератеаллдевицес выполняет четыре основных задачи:</span><span class="sxs-lookup"><span data-stu-id="322ee-107">The EnumerateAllDevices function accomplishes four primary tasks:</span></span>

1.  <span data-ttu-id="322ee-108">Создает объект диспетчера переносимых устройств.</span><span class="sxs-lookup"><span data-stu-id="322ee-108">Creates the portable device manager object.</span></span>
2.  <span data-ttu-id="322ee-109">Возвращает число подключенных устройств.</span><span class="sxs-lookup"><span data-stu-id="322ee-109">Retrieves a count of connected devices.</span></span>
3.  <span data-ttu-id="322ee-110">Извлекает сведения об устройстве (для подключенных устройств).</span><span class="sxs-lookup"><span data-stu-id="322ee-110">Retrieves device information (for the connected devices).</span></span>
4.  <span data-ttu-id="322ee-111">Освобождает память, используемую при извлечении сведений об устройстве.</span><span class="sxs-lookup"><span data-stu-id="322ee-111">Frees the memory used when retrieving the device information.</span></span>

<span data-ttu-id="322ee-112">Каждая из этих четырех задач более подробно описана в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="322ee-112">Each of these four tasks is described in more detail in the following sections.</span></span>

<span data-ttu-id="322ee-113">Первым шагом в процессе перечисления устройств является создание объекта диспетчера переносимых устройств.</span><span class="sxs-lookup"><span data-stu-id="322ee-113">The first step in the device enumeration process is the creation of a portable device manager object.</span></span> <span data-ttu-id="322ee-114">Для этого необходимо вызвать функцию CoCreateInstance и передать идентификатор класса (CLSID) для объекта, указать контекст, в котором будет выполняться код, указать идентификатор ссылки для интерфейса Ипортабледевицеманажер, а затем указать переменную указателя, которая получает указатель интерфейса Ипортабледевицеманажер.</span><span class="sxs-lookup"><span data-stu-id="322ee-114">This is done by calling the CoCreateInstance function and passing the class identifier (CLSID) for the object, specifying the context in which the code will run, specifying a reference identifier for the IPortableDeviceManager interface, and then supplying a pointer variable that receives the IPortableDeviceManager interface pointer.</span></span>


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



<span data-ttu-id="322ee-115">После получения указателя на интерфейс [**ипортабледевицеманажер**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) можно приступить к вызову методов для этого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="322ee-115">Once you obtain an [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) interface pointer, you can begin calling methods on this interface.</span></span> <span data-ttu-id="322ee-116">Первый метод, вызываемый в функции Енумератеаллдевицес, — это [**ипортабледевицеманажер::**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices)-of-Devices.</span><span class="sxs-lookup"><span data-stu-id="322ee-116">The first method called in the EnumerateAllDevices function is [**IPortableDeviceManager::GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices).</span></span> <span data-ttu-id="322ee-117">При вызове этого метода с первым аргументом, имеющим значение **null**, возвращается число подключенных устройств.</span><span class="sxs-lookup"><span data-stu-id="322ee-117">When this method is called with the first argument set to **NULL**, it returns the count of connected devices.</span></span>


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



<span data-ttu-id="322ee-118">После получения числа подключенных устройств можно использовать это значение для получения сведений об устройстве для каждого подключенного устройства.</span><span class="sxs-lookup"><span data-stu-id="322ee-118">After you have retrieved the count of connected devices, you can use this value to retrieve device information for each connected device.</span></span> <span data-ttu-id="322ee-119">Этот процесс начинается с передачи массива указателей строк в качестве первого аргумента и количества элементов, которые этот массив может хранить в качестве второго аргумента (это число должно быть по крайней мере равно количеству доступных устройств).</span><span class="sxs-lookup"><span data-stu-id="322ee-119">This process begins by passing an array of string pointers as the first argument and a count of the number of elements that this array can hold as the second argument (this count should at least be equal to the number of available devices).</span></span>

<span data-ttu-id="322ee-120">Строки, возвращаемые этим методом, являются самонастраивающийся именами подключенных устройств.</span><span class="sxs-lookup"><span data-stu-id="322ee-120">The strings returned by this method are the Plug and Play names of the connected devices.</span></span> <span data-ttu-id="322ee-121">Эти имена, в свою очередь, передаются другим методам в интерфейсе [**ипортабледевицеманажер**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) для получения сведений об устройстве, таких как понятное имя, имя производителя и описание устройства.</span><span class="sxs-lookup"><span data-stu-id="322ee-121">These names, in turn, are passed to other methods on the [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) interface to retrieve device-specific information such as the friendly name, the manufacturer's name, and the device description.</span></span> <span data-ttu-id="322ee-122">(Эти имена также используются для открытия подключения к устройству, когда приложение вызывает метод [**ипортабледевице:: Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open) .)</span><span class="sxs-lookup"><span data-stu-id="322ee-122">(These names are also used to open a connection to the device when an application calls the [**IPortableDevice::Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open) method.)</span></span>


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



<span data-ttu-id="322ee-123">После получения сведений об устройстве необходимо освободить память, связанную со строками, на которые указывает массив указателей строк.</span><span class="sxs-lookup"><span data-stu-id="322ee-123">Once you've retrieved the device information, you will need to free the memory associated with the strings pointed to by the array of string pointers.</span></span> <span data-ttu-id="322ee-124">Кроме того, необходимо удалить этот массив.</span><span class="sxs-lookup"><span data-stu-id="322ee-124">You will also need to delete this array.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="322ee-125">См. также</span><span class="sxs-lookup"><span data-stu-id="322ee-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="322ee-126">**Интерфейс Ипортабледевицеманажер**</span><span class="sxs-lookup"><span data-stu-id="322ee-126">**IPortableDeviceManager Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager)
</dt> <dt>

[<span data-ttu-id="322ee-127">**Инструкции по программированию**</span><span class="sxs-lookup"><span data-stu-id="322ee-127">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 




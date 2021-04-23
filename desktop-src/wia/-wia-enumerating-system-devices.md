---
description: 'Используйте метод Ивиадевмгр:: Енумдевицеинфо (или IWiaDevMgr2:: Енумдевицеинфо) для перечисления устройств, установленных в системе для получения образа Windows (WIA).'
ms.assetid: 6465a33e-1b3b-4142-a58f-b27e9c95cd3e
title: Перечисление системных устройств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d2d65879cd1fc8466f4ada638281ef496636b19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998584"
---
# <a name="enumerating-system-devices"></a><span data-ttu-id="a4c4d-103">Перечисление системных устройств</span><span class="sxs-lookup"><span data-stu-id="a4c4d-103">Enumerating System Devices</span></span>

<span data-ttu-id="a4c4d-104">Используйте метод [**ивиадевмгр:: енумдевицеинфо**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo) (или [**IWiaDevMgr2:: енумдевицеинфо**](-wia-iwiadevmgr2-enumdeviceinfo.md)) для перечисления устройств, установленных в системе для получения образа Windows (WIA).</span><span class="sxs-lookup"><span data-stu-id="a4c4d-104">Use the [**IWiaDevMgr::EnumDeviceInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo) (or [**IWiaDevMgr2::EnumDeviceInfo**](-wia-iwiadevmgr2-enumdeviceinfo.md)) method to enumerate the Windows Image Acquisition (WIA) devices installed on a system.</span></span> <span data-ttu-id="a4c4d-105">Этот метод создает объект перечисления для свойств устройств и возвращает указатель на интерфейс [**иенумвиа \_ dev \_ info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) , который поддерживает объект перечисления.</span><span class="sxs-lookup"><span data-stu-id="a4c4d-105">This method creates an enumeration object for the properties of the devices, and returns a pointer to the [**IEnumWIA\_DEV\_INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) interface that the enumeration object supports.</span></span>

<span data-ttu-id="a4c4d-106">Затем можно использовать методы интерфейса [**иенумвиа \_ dev \_ info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) , чтобы получить указатель интерфейса [**ивиапропертистораже**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) для каждого устройства, установленного в системе.</span><span class="sxs-lookup"><span data-stu-id="a4c4d-106">You can then use the methods of the [**IEnumWIA\_DEV\_INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) interface to obtain an [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) interface pointer for each device installed on the system.</span></span>

<span data-ttu-id="a4c4d-107">В следующем коде из примера приложения Виассамп показано, как создать объект перечисления для устройств в системе и выполнить итерацию по этим устройствам:</span><span class="sxs-lookup"><span data-stu-id="a4c4d-107">The following code from the WiaSSamp sample application demonstrates how to create an enumeration object for the devices on a system and iterate through those devices:</span></span>


```
    HRESULT EnumerateWiaDevices( IWiaDevMgr *pWiaDevMgr ) //XP or earlier
    HRESULT EnumerateWiaDevices( IWiaDevMgr2 *pWiaDevMgr ) //Vista or later
    
    {
        //
        // Validate arguments
        //
        if (NULL == pWiaDevMgr)
        {
            return E_INVALIDARG;
        }

        //
        // Get a device enumerator interface
        //
        IEnumWIA_DEV_INFO *pWiaEnumDevInfo = NULL;
        HRESULT hr = pWiaDevMgr->EnumDeviceInfo( WIA_DEVINFO_ENUM_LOCAL, &pWiaEnumDevInfo );
        if (SUCCEEDED(hr))
        {
            //
            // Loop until you get an error or pWiaEnumDevInfo->Next returns
            // S_FALSE to signal the end of the list.
            //
            while (S_OK == hr)
            {
                //
                // Get the next device's property storage interface pointer
                //
                IWiaPropertyStorage *pWiaPropertyStorage = NULL;
                hr = pWiaEnumDevInfo->Next( 1, &pWiaPropertyStorage, NULL );

                //
                // pWiaEnumDevInfo->Next will return S_FALSE when the list is
                // exhausted, so check for S_OK before using the returned
                // value.
                //
                if (hr == S_OK)
                {
                    //
                    // Do something with the device's IWiaPropertyStorage*
                    //

                    //
                    // Release the device's IWiaPropertyStorage*
                    //
                    pWiaPropertyStorage->Release();
                    pWiaPropertyStorage = NULL;
                }
            }

            //
            // If the result of the enumeration is S_FALSE (which
            // is normal), change it to S_OK.
            //
            if (S_FALSE == hr)
            {
                hr = S_OK;
            }

            //
            // Release the enumerator
            //
            pWiaEnumDevInfo->Release();
            pWiaEnumDevInfo = NULL;
        }

        //
        // Return the result of the enumeration
        //
        return hr;
    }
```



<span data-ttu-id="a4c4d-108">WIA \_ DEVINFO \_ Enum \_ Local — это константа WIA, представляющая единственное допустимое значение для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="a4c4d-108">WIA\_DEVINFO\_ENUM\_LOCAL is a WIA constant that represents the only valid value for this parameter.</span></span>

<span data-ttu-id="a4c4d-109">В этом примере параметр **пвиадевмгр** указывает на экземпляр интерфейса [**Ивиадевмгр**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) (или [**IWiaDevMgr2**](-wia-iwiadevmgr2.md)) после предыдущего вызова [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="a4c4d-109">In the example, the parameter **pWiaDevMgr** points to an instance of the [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) (or [**IWiaDevMgr2**](-wia-iwiadevmgr2.md)) interface after a previous call to [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

<span data-ttu-id="a4c4d-110">Приложение вызывает метод [**ивиадевмгр:: енумдевицеинфо**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo) (или [**IWiaDevMgr2:: енумдевицеинфо**](-wia-iwiadevmgr2-enumdeviceinfo.md)) указателя [**ивиадевмгр (или IWiaDevMgr2), который**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) заполняет пвиадевмгр **с** адресом  указателя на интерфейс [**пвиаенумдевинфо \_ dev \_ info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) . [](-wia-iwiadevmgr2.md)</span><span class="sxs-lookup"><span data-stu-id="a4c4d-110">The application calls the [**IWiaDevMgr::EnumDeviceInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo) (or [**IWiaDevMgr2::EnumDeviceInfo**](-wia-iwiadevmgr2-enumdeviceinfo.md)) method of the [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) (or [**IWiaDevMgr2**](-wia-iwiadevmgr2.md)) pointer **pWiaDevMgr** that fills **pWiaEnumDevInfo** with the address of a pointer to the [**IEnumWIA\_DEV\_INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) interface.</span></span>

<span data-ttu-id="a4c4d-111">Если вызов будет выполнен, приложение вызывает метод [**иенумвиа \_ dev \_ info:: Reset**](/windows/desktop/api/wia_xp/nf-wia_xp-ienumwia_dev_info-reset) указателя [**иенумвиа \_ dev \_ info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) .</span><span class="sxs-lookup"><span data-stu-id="a4c4d-111">If the call succeeds, the application then calls the [**IEnumWIA\_DEV\_INFO::Reset**](/windows/desktop/api/wia_xp/nf-wia_xp-ienumwia_dev_info-reset) method of the [**IEnumWIA\_DEV\_INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) pointer.</span></span> <span data-ttu-id="a4c4d-112">Переменная **пвиаенумдевинфо** гарантирует, что перечисление начинается с начала.</span><span class="sxs-lookup"><span data-stu-id="a4c4d-112">The **pWiaEnumDevInfo** variable ensures that the enumeration starts at the beginning.</span></span>

<span data-ttu-id="a4c4d-113">Если этот вызов завершается успешно, приложение выполняет итерацию по устройствам в системе, повторно вызывая метод [**иенумвиа \_ dev \_ info:: Next**](/windows/desktop/api/wia_xp/nf-wia_xp-ienumwia_dev_info-next) класса [**иенумвиа \_ dev \_ info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) **пвиаенумдевинфо** , пока метод больше не возвратит значение S \_ ОК, что означает, что перечисление завершено.</span><span class="sxs-lookup"><span data-stu-id="a4c4d-113">If this call succeeds, the application iterates through the devices on the system by repeatedly calling the [**IEnumWIA\_DEV\_INFO::Next**](/windows/desktop/api/wia_xp/nf-wia_xp-ienumwia_dev_info-next) method of the [**IEnumWIA\_DEV\_INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) pointer **pWiaEnumDevInfo** until the method no longer returns S\_OK, indicating that the enumeration is complete.</span></span>

<span data-ttu-id="a4c4d-114">Каждый вызов **пвиаенумдевинфо->следующий** заполняет **пвиапропертистораже** указателем на интерфейс [**ивиапропертистораже**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) , который содержит сведения о свойствах для конкретного устройства.</span><span class="sxs-lookup"><span data-stu-id="a4c4d-114">Each call to **pWiaEnumDevInfo->Next** fills **pWiaPropertyStorage** with a pointer to the [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) interface that contains property information for a specific device.</span></span>

 

 

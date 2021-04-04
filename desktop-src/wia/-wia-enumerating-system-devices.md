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
# <a name="enumerating-system-devices"></a>Перечисление системных устройств

Используйте метод [**ивиадевмгр:: енумдевицеинфо**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo) (или [**IWiaDevMgr2:: енумдевицеинфо**](-wia-iwiadevmgr2-enumdeviceinfo.md)) для перечисления устройств, установленных в системе для получения образа Windows (WIA). Этот метод создает объект перечисления для свойств устройств и возвращает указатель на интерфейс [**иенумвиа \_ dev \_ info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) , который поддерживает объект перечисления.

Затем можно использовать методы интерфейса [**иенумвиа \_ dev \_ info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) , чтобы получить указатель интерфейса [**ивиапропертистораже**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) для каждого устройства, установленного в системе.

В следующем коде из примера приложения Виассамп показано, как создать объект перечисления для устройств в системе и выполнить итерацию по этим устройствам:


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



WIA \_ DEVINFO \_ Enum \_ Local — это константа WIA, представляющая единственное допустимое значение для этого параметра.

В этом примере параметр **пвиадевмгр** указывает на экземпляр интерфейса [**Ивиадевмгр**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) (или [**IWiaDevMgr2**](-wia-iwiadevmgr2.md)) после предыдущего вызова [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

Приложение вызывает метод [**ивиадевмгр:: енумдевицеинфо**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo) (или [**IWiaDevMgr2:: енумдевицеинфо**](-wia-iwiadevmgr2-enumdeviceinfo.md)) указателя [**ивиадевмгр (или IWiaDevMgr2), который**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) заполняет пвиадевмгр **с** адресом  указателя на интерфейс [**пвиаенумдевинфо \_ dev \_ info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) . [](-wia-iwiadevmgr2.md)

Если вызов будет выполнен, приложение вызывает метод [**иенумвиа \_ dev \_ info:: Reset**](/windows/desktop/api/wia_xp/nf-wia_xp-ienumwia_dev_info-reset) указателя [**иенумвиа \_ dev \_ info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) . Переменная **пвиаенумдевинфо** гарантирует, что перечисление начинается с начала.

Если этот вызов завершается успешно, приложение выполняет итерацию по устройствам в системе, повторно вызывая метод [**иенумвиа \_ dev \_ info:: Next**](/windows/desktop/api/wia_xp/nf-wia_xp-ienumwia_dev_info-next) класса [**иенумвиа \_ dev \_ info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) **пвиаенумдевинфо** , пока метод больше не возвратит значение S \_ ОК, что означает, что перечисление завершено.

Каждый вызов **пвиаенумдевинфо->следующий** заполняет **пвиапропертистораже** указателем на интерфейс [**ивиапропертистораже**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) , который содержит сведения о свойствах для конкретного устройства.

 

 

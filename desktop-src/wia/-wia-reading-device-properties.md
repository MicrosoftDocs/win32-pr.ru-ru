---
description: Приложения используют интерфейс Ивиапропертисторажеа устройства для чтения и записи свойств устройства. Ивиапропертистораже наследует все методы интерфейса модели COM Ипропертистораже.
ms.assetid: 65ca9e71-9a0f-495f-b78c-3b1a8d66ee33
title: Чтение свойств устройства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf102fb2ade1a13b648e13f56f7f999dd35c41f721ac20d72914219c98311505
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117669264"
---
# <a name="reading-device-properties"></a>Чтение свойств устройства

Приложения используют интерфейс [**ивиапропертисторажеа**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) устройства для чтения и записи свойств устройства. **Ивиапропертистораже** наследует все методы интерфейса модели COM [ипропертистораже](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage).

Свойства устройства включают сведения об устройстве, описывающем возможности и параметры устройства. Список этих свойств см. в разделе [Свойства устройства](-wia-device-properties.md).

к свойствам устройства, которые считываются с помощью [**ивиапропертистораже**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) , относится идентификатор устройства, который затем используется для создания устройства Windowsного получения изображений (WIA). Дополнительные сведения см. в разделе [**ивиадевмгр:: креатедевице**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) (или [**IWiaDevMgr2:: креатедевице**](-wia-iwiadevmgr2-createdevice.md)).

В следующем примере считывается идентификатор устройства, имя устройства и описание устройства из массива свойств устройства, а затем эти свойства выводятся на консоль.


```
    HRESULT ReadSomeWiaProperties( IWiaPropertyStorage *pWiaPropertyStorage )
    {
        //
        // Validate arguments
        //
        if (NULL == pWiaPropertyStorage)
        {
            return E_INVALIDARG;
        }

        //
        // Declare PROPSPECs and PROPVARIANTs, and initialize them to zero.
        //
        PROPSPEC PropSpec[3] = {0};
        PROPVARIANT PropVar[3] = {0};

        //
        // How many properties are you querying for?
        //
        const ULONG c_nPropertyCount = sizeof(PropSpec)/sizeof(PropSpec[0]);

        //
        // Define which properties you want to read:
        // Device ID.  This is what you would use to create
        // the device.
        //
        PropSpec[0].ulKind = PRSPEC_PROPID;
        PropSpec[0].propid = WIA_DIP_DEV_ID;

        //
        // Device Name
        //
        PropSpec[1].ulKind = PRSPEC_PROPID;
        PropSpec[1].propid = WIA_DIP_DEV_NAME;

        //
        // Device description
        //
        PropSpec[2].ulKind = PRSPEC_PROPID;
        PropSpec[2].propid = WIA_DIP_DEV_DESC;

        //
        // Ask for the property values
        //
        HRESULT hr = pWiaPropertyStorage->ReadMultiple( c_nPropertyCount, PropSpec, PropVar );
        if (SUCCEEDED(hr))
        {
            //
            // IWiaPropertyStorage::ReadMultiple will return S_FALSE if some
            // properties could not be read, so you have to check the return
            // types for each requested item.
            //

            //
            // Check the return type for the device ID
            //
            if (VT_BSTR == PropVar[0].vt)
            {
                //
                // Do something with the device ID
                //
                _tprintf( TEXT("WIA_DIP_DEV_ID: %ws\n"), PropVar[0].bstrVal );
            }

            //
            // Check the return type for the device name
            //
            if (VT_BSTR == PropVar[1].vt)
            {
                //
                // Do something with the device name
                //
                _tprintf( TEXT("WIA_DIP_DEV_NAME: %ws\n"), PropVar[1].bstrVal );
            }

            //
            // Check the return type for the device description
            //
            if (VT_BSTR == PropVar[2].vt)
            {
                //
                // Do something with the device description
                //
                _tprintf( TEXT("WIA_DIP_DEV_DESC: %ws\n"), PropVar[2].bstrVal );
            }

            //
            // Free the returned PROPVARIANTs
            //
            FreePropVariantArray( c_nPropertyCount, PropVar );
        }

        //
        // Return the result of reading the properties
        //
        return hr;
    }
```



В этом примере приложение настраивает массивы [пропвариант](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) (**пропспек** и **пропвар** соответственно) для хранения сведений о свойствах. Эти массивы передаются как параметры при вызове метода [ипропертистораже:: реадмултипле](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-readmultiple) указателя [**ивиапропертистораже**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) **пивиапропстг**. Каждый элемент массива **пропспек** содержит тип и имя свойства устройства. После возврата каждый элемент **пропвар** содержит значение свойства устройства, представленного соответствующим элементом массива **пропспек** .

Затем приложение вызывает свойство [ипропертистораже:: реадмултипле](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-readmultiple) указателя [**ивиапропертистораже**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) **пвиапропертистораже** для получения сведений о свойстве.

Метод, используемый для чтения и установки свойств устройства, аналогичен для свойств элемента, единственное отличие заключается в типе элемента WIA, для которого вызываются соответствующие методы. Список свойств элемента см. в разделе [свойства элемента](-wia-item-properties.md).

 

 

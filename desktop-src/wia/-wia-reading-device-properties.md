---
description: Приложения используют интерфейс Ивиапропертисторажеа устройства для чтения и записи свойств устройства. Ивиапропертистораже наследует все методы интерфейса модели COM Ипропертистораже.
ms.assetid: 65ca9e71-9a0f-495f-b78c-3b1a8d66ee33
title: Чтение свойств устройства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 235ba701ed3356e09070709f3c99f2826c69c8c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991152"
---
# <a name="reading-device-properties"></a><span data-ttu-id="c3a03-104">Чтение свойств устройства</span><span class="sxs-lookup"><span data-stu-id="c3a03-104">Reading Device Properties</span></span>

<span data-ttu-id="c3a03-105">Приложения используют интерфейс [**ивиапропертисторажеа**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) устройства для чтения и записи свойств устройства.</span><span class="sxs-lookup"><span data-stu-id="c3a03-105">Applications use a device's [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) interface to read and write device properties.</span></span> <span data-ttu-id="c3a03-106">**Ивиапропертистораже** наследует все методы интерфейса модели COM [ипропертистораже](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage).</span><span class="sxs-lookup"><span data-stu-id="c3a03-106">**IWiaPropertyStorage** inherits all of the methods of the Component Object Model (COM) interface [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage).</span></span>

<span data-ttu-id="c3a03-107">Свойства устройства включают сведения об устройстве, описывающем возможности и параметры устройства.</span><span class="sxs-lookup"><span data-stu-id="c3a03-107">Device properties include information about a device that describe the device's capabilities and settings.</span></span> <span data-ttu-id="c3a03-108">Список этих свойств см. в разделе [Свойства устройства](-wia-device-properties.md).</span><span class="sxs-lookup"><span data-stu-id="c3a03-108">For a list of these properties, see [Device Properties](-wia-device-properties.md).</span></span>

<span data-ttu-id="c3a03-109">К свойствам устройства, которые считываются с помощью [**ивиапропертистораже**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) , относится идентификатор устройства, который затем используется для создания устройства для получения образа Windows (WIA).</span><span class="sxs-lookup"><span data-stu-id="c3a03-109">Among the device properties that are read using [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) is the device ID, that is then used to create a Windows Image Acquisition (WIA) device.</span></span> <span data-ttu-id="c3a03-110">Дополнительные сведения см. в разделе [**ивиадевмгр:: креатедевице**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) (или [**IWiaDevMgr2:: креатедевице**](-wia-iwiadevmgr2-createdevice.md)).</span><span class="sxs-lookup"><span data-stu-id="c3a03-110">For more information, see [**IWiaDevMgr::CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) (or [**IWiaDevMgr2::CreateDevice**](-wia-iwiadevmgr2-createdevice.md)).</span></span>

<span data-ttu-id="c3a03-111">В следующем примере считывается идентификатор устройства, имя устройства и описание устройства из массива свойств устройства, а затем эти свойства выводятся на консоль.</span><span class="sxs-lookup"><span data-stu-id="c3a03-111">The following example reads the device ID, the device name, and the device description from the array of device properties, and prints these properties to the console.</span></span>


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



<span data-ttu-id="c3a03-112">В этом примере приложение настраивает массивы [пропвариант](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) (**пропспек** и **пропвар** соответственно) для хранения сведений о свойствах.</span><span class="sxs-lookup"><span data-stu-id="c3a03-112">In this example, the application sets up [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) arrays (**PropSpec** and **PropVar**, respectively) to hold property information.</span></span> <span data-ttu-id="c3a03-113">Эти массивы передаются как параметры при вызове метода [ипропертистораже:: реадмултипле](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-readmultiple) указателя [**ивиапропертистораже**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) **пивиапропстг**.</span><span class="sxs-lookup"><span data-stu-id="c3a03-113">These arrays are passed as parameters in the call to [IPropertyStorage::ReadMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-readmultiple) method of the [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) pointer **pIWiaPropStg**.</span></span> <span data-ttu-id="c3a03-114">Каждый элемент массива **пропспек** содержит тип и имя свойства устройства.</span><span class="sxs-lookup"><span data-stu-id="c3a03-114">Each element of the **PropSpec** array contains the type and name of a device property.</span></span> <span data-ttu-id="c3a03-115">После возврата каждый элемент **пропвар** содержит значение свойства устройства, представленного соответствующим элементом массива **пропспек** .</span><span class="sxs-lookup"><span data-stu-id="c3a03-115">Upon return, each element of the **PropVar** contains the value of the device property represented by the corresponding element of the **PropSpec** array.</span></span>

<span data-ttu-id="c3a03-116">Затем приложение вызывает свойство [ипропертистораже:: реадмултипле](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-readmultiple) указателя [**ивиапропертистораже**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) **пвиапропертистораже** для получения сведений о свойстве.</span><span class="sxs-lookup"><span data-stu-id="c3a03-116">The application then calls [IPropertyStorage::ReadMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-readmultiple) property of the [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) pointer **pWiaPropertyStorage** to retrieve the property information.</span></span>

<span data-ttu-id="c3a03-117">Метод, используемый для чтения и установки свойств устройства, аналогичен для свойств элемента, единственное отличие заключается в типе элемента WIA, для которого вызываются соответствующие методы.</span><span class="sxs-lookup"><span data-stu-id="c3a03-117">The technique used to read and set device properties is the same as that for item properties, the only difference is the type of the WIA item on which you call the appropriate methods.</span></span> <span data-ttu-id="c3a03-118">Список свойств элемента см. в разделе [свойства элемента](-wia-item-properties.md).</span><span class="sxs-lookup"><span data-stu-id="c3a03-118">For a list of item properties, see [Item Properties](-wia-item-properties.md).</span></span>

 

 

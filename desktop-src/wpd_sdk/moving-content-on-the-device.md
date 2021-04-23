---
description: Перемещение содержимого на устройстве
ms.assetid: 5072d308-d376-4141-96df-dbef23fb9f9b
title: Перемещение содержимого на устройстве
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3eb4a9638e656d5cab8437448d64b79947df337b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663614"
---
# <a name="moving-content-on-the-device"></a><span data-ttu-id="f4ea6-103">Перемещение содержимого на устройстве</span><span class="sxs-lookup"><span data-stu-id="f4ea6-103">Moving Content on the Device</span></span>

<span data-ttu-id="f4ea6-104">Другой распространенной операцией, выполняемой приложением WPD, является перенос содержимого из одного места на устройстве в другое.</span><span class="sxs-lookup"><span data-stu-id="f4ea6-104">Another common operation accomplished by a WPD application is the transfer of content from one location on the device to another.</span></span>

<span data-ttu-id="f4ea6-105">Операции перемещения содержимого выполняются с помощью интерфейсов, описанных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="f4ea6-105">Content move operations are accomplished using the interfaces described in the following table.</span></span>



| <span data-ttu-id="f4ea6-106">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="f4ea6-106">Interface</span></span>                                                                                      | <span data-ttu-id="f4ea6-107">Описание</span><span class="sxs-lookup"><span data-stu-id="f4ea6-107">Description</span></span>                                       |
|------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [<span data-ttu-id="f4ea6-108">**Интерфейс Ипортабледевицеконтент**</span><span class="sxs-lookup"><span data-stu-id="f4ea6-108">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | <span data-ttu-id="f4ea6-109">Предоставляет доступ к методам, относящимся к содержимому.</span><span class="sxs-lookup"><span data-stu-id="f4ea6-109">Provides access to the content-specific methods.</span></span>  |
| [<span data-ttu-id="f4ea6-110">**Интерфейс Ипортабледевицепропвариантколлектион**</span><span class="sxs-lookup"><span data-stu-id="f4ea6-110">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="f4ea6-111">Предоставляет доступ к методам, относящимся к конкретному свойству.</span><span class="sxs-lookup"><span data-stu-id="f4ea6-111">Provides access to the property-specific methods.</span></span> |



 

<span data-ttu-id="f4ea6-112">Функция Мовеконтенталреадйондевице в модуле Контенттрансфер. cpp примера приложения демонстрирует, как приложение может перемещать содержимое из одного расположения в другое.</span><span class="sxs-lookup"><span data-stu-id="f4ea6-112">The MoveContentAlreadyOnDevice function in the sample application's ContentTransfer.cpp module demonstrates how an application can move content from one location to another.</span></span>

<span data-ttu-id="f4ea6-113">Первая задача, выполняемая функцией Мовеконтенталреадйондевице, — запросить драйвер устройства, чтобы узнать, поддерживает ли он перемещение содержимого.</span><span class="sxs-lookup"><span data-stu-id="f4ea6-113">The first task accomplished by the MoveContentAlreadyOnDevice function is to query the device driver to see whether it supports content movement.</span></span> <span data-ttu-id="f4ea6-114">Это достигается путем вызова вспомогательной функции Суппортскомманд и передачи \_ \_ объектов управления командой объекта WPD \_ \_ Переместить \_ объекты в качестве второго аргумента.</span><span class="sxs-lookup"><span data-stu-id="f4ea6-114">This is accomplished by calling the SupportsCommand helper function and passing WPD\_COMMAND\_OBJECT\_MANAGEMENT\_MOVE\_OBJECTS as the second argument.</span></span>


```C++
HRESULT                                       hr                               = S_OK;
WCHAR                                         wszSelection[81]                 = {0};
WCHAR                                         wszDestinationFolderObjectID[81] = {0};
CComPtr<IPortableDeviceContent>               pContent;
CComPtr<IPortableDevicePropVariantCollection> pObjectsToMove;
CComPtr<IPortableDevicePropVariantCollection> pObjectsFailedToMove;
if (SupportsCommand(pDevice, WPD_COMMAND_OBJECT_MANAGEMENT_MOVE_OBJECTS) == FALSE)
{
    printf("! This device does not support the move operation (i.e. The WPD_COMMAND_OBJECT_MANAGEMENT_MOVE_OBJECTS command)\n");
    return;
}
```



<span data-ttu-id="f4ea6-115">На следующем шаге пользователю предлагается ввести два идентификатора объекта.</span><span class="sxs-lookup"><span data-stu-id="f4ea6-115">The next step entails prompting the user to enter two object identifiers.</span></span> <span data-ttu-id="f4ea6-116">Первый — это идентификатор перемещаемого содержимого.</span><span class="sxs-lookup"><span data-stu-id="f4ea6-116">The first is the identifier for the content that will be moved.</span></span> <span data-ttu-id="f4ea6-117">Второй — идентификатор расположения, в которое приложение должно перемещать это содержимое.</span><span class="sxs-lookup"><span data-stu-id="f4ea6-117">The second is the identifier for the location to which the application should move this content.</span></span>


```C++
HRESULT                                       hr                               = S_OK;
WCHAR                                         wszSelection[81]                 = {0};
WCHAR                                         wszDestinationFolderObjectID[81] = {0};
CComPtr<IPortableDeviceContent>               pContent;
CComPtr<IPortableDevicePropVariantCollection> pObjectsToMove;
CComPtr<IPortableDevicePropVariantCollection> pObjectsFailedToMove;
printf("Enter the identifer of the object you wish to move.\n>");
hr = StringCbGetsW(wszSelection,sizeof(wszSelection));
if (FAILED(hr))
{
    printf("An invalid object identifier was specified, aborting content moving\n");
}

// Prompt user to enter an object identifier on the device to move.
printf("Enter the identifer of the object you wish to move '%ws' to.\n>", wszSelection);
hr = StringCbGetsW(wszDestinationFolderObjectID,sizeof(wszDestinationFolderObjectID));
if (FAILED(hr))
{
    printf("An invalid object identifier was specified, aborting content moving\n");
}
```



<span data-ttu-id="f4ea6-118">Затем образец извлекает объект [**ипортабледевицеконтент**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) , который используется для доступа к методу [**Ипортабледевицеконтент:: Move**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-move) .</span><span class="sxs-lookup"><span data-stu-id="f4ea6-118">Next, the sample retrieves an [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) object that is used to access the [**IPortableDeviceContent::Move**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-move) method.</span></span>


```C++
HRESULT                                       hr                               = S_OK;
WCHAR                                         wszSelection[81]                 = {0};
WCHAR                                         wszDestinationFolderObjectID[81] = {0};
CComPtr<IPortableDeviceContent>               pContent;
CComPtr<IPortableDevicePropVariantCollection> pObjectsToMove;
CComPtr<IPortableDevicePropVariantCollection> pObjectsFailedToMove;
if (SUCCEEDED(hr))
{
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }
}
```



<span data-ttu-id="f4ea6-119">Наконец, содержимое перемещается.</span><span class="sxs-lookup"><span data-stu-id="f4ea6-119">Finally, the content is moved.</span></span> <span data-ttu-id="f4ea6-120">Этот процесс включает следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f4ea6-120">This process involves the following:</span></span>

1.  <span data-ttu-id="f4ea6-121">Создание объекта [**ипортабледевицепропвариантколлектион**](iportabledevicepropvariantcollection.md) , который получает структуру пропвариант для перемещаемого объекта.</span><span class="sxs-lookup"><span data-stu-id="f4ea6-121">Creating an [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) object that receives a PROPVARIANT structure for the object to be moved.</span></span>
2.  <span data-ttu-id="f4ea6-122">Добавление ПРОПВАРИАНТ в объект Ипортабледевицепропвариантколлектион.</span><span class="sxs-lookup"><span data-stu-id="f4ea6-122">Adding the PROPVARIANT to the IPortableDevicePropVariantCollection object.</span></span>
3.  <span data-ttu-id="f4ea6-123">Вызов метода Ипортабледевицеконтент:: Move.</span><span class="sxs-lookup"><span data-stu-id="f4ea6-123">Invoking the IPortableDeviceContent::Move method.</span></span>


```C++
HRESULT                                       hr                               = S_OK;
WCHAR                                         wszSelection[81]                 = {0};
WCHAR                                         wszDestinationFolderObjectID[81] = {0};
CComPtr<IPortableDeviceContent>               pContent;
CComPtr<IPortableDevicePropVariantCollection> pObjectsToMove;
CComPtr<IPortableDevicePropVariantCollection> pObjectsFailedToMove;
if (SUCCEEDED(hr))
{
    hr = CoCreateInstance(CLSID_PortableDevicePropVariantCollection,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IPortableDevicePropVariantCollection,
                          (VOID**) &pObjectsToMove);
    if (SUCCEEDED(hr))
    {
        if (pObjectsToMove != NULL)
        {
            PROPVARIANT pv = {0};
            PropVariantInit(&pv);

            // Initialize a PROPVARIANT structure with the object identifier string
            // that the user selected above. Notice we are allocating memory for the
            // LPWSTR value.  This memory will be freed when PropVariantClear() is
            // called below.
            pv.vt      = VT_LPWSTR;
            pv.pwszVal = AtlAllocTaskWideString(wszSelection);
            if (pv.pwszVal != NULL)
            {
                // Add the object identifier to the objects-to-move list
                // (We are only moving 1 in this example)
                hr = pObjectsToMove->Add(&pv);
                if (SUCCEEDED(hr))
                {
                    // Attempt to move the object on the device
                    hr = pContent->Move(pObjectsToMove,               // Object(s) to move
                                        wszDestinationFolderObjectID, // Folder to move to
                                        NULL);                        // Object(s) that failed to delete (we are only moving 1, so we can pass NULL here)
                    if (SUCCEEDED(hr))
                    {
                        // An S_OK return lets the caller know that the deletion was successful
                        if (hr == S_OK)
                        {
                            printf("The object '%ws' was moved on the device.\n", wszSelection);
                        }

                        // An S_FALSE return lets the caller know that the move failed.
                        // The caller should check the returned IPortableDevicePropVariantCollection
                        // for a list of object identifiers that failed to be moved.
                        else
                        {
                            printf("The object '%ws' failed to be moved on the device.\n", wszSelection);
                        }
                    }
                    else
                    {
                        printf("! Failed to move an object on the device, hr = 0x%lx\n",hr);
                    }
                }
                else
                {
                    printf("! Failed to move an object on the device because we could no add the object identifier string to the IPortableDevicePropVariantCollection, hr = 0x%lx\n",hr);
                }
            }
            else
            {
                hr = E_OUTOFMEMORY;
                printf("! Failed to move an object on the device because we could no allocate memory for the object identifier string, hr = 0x%lx\n",hr);
            }

            // Free any allocated values in the PROPVARIANT before exiting
            PropVariantClear(&pv);
        }
        else
        {
            printf("! Failed to move an object from the device because we were returned a NULL IPortableDevicePropVariantCollection interface pointer, hr = 0x%lx\n",hr);
        }
    }
    else
    {
        printf("! Failed to CoCreateInstance CLSID_PortableDevicePropVariantCollection, hr = 0x%lx\n",hr);
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="f4ea6-124">См. также</span><span class="sxs-lookup"><span data-stu-id="f4ea6-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4ea6-125">**Интерфейс Ипортабледевице**</span><span class="sxs-lookup"><span data-stu-id="f4ea6-125">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="f4ea6-126">**Интерфейс Ипортабледевицеконтент**</span><span class="sxs-lookup"><span data-stu-id="f4ea6-126">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="f4ea6-127">**Интерфейс Ипортабледевицепропвариантколлектион**</span><span class="sxs-lookup"><span data-stu-id="f4ea6-127">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="f4ea6-128">**Инструкции по программированию**</span><span class="sxs-lookup"><span data-stu-id="f4ea6-128">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 




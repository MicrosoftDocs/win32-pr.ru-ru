---
description: Передача объекта Properties-Only на устройство
ms.assetid: 6305cff9-c0ce-4ef5-a129-bc329b9c563f
title: Передача объекта Properties-Only на устройство
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e20f9bcfecd46ea3047310ea5b946a366b35b9c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816289"
---
# <a name="transferring-a-properties-only-object-to-the-device"></a><span data-ttu-id="32188-103">Передача объекта Properties-Only на устройство</span><span class="sxs-lookup"><span data-stu-id="32188-103">Transferring a Properties-Only Object to the Device</span></span>

<span data-ttu-id="32188-104">Хотя в примере из предыдущего раздела показано создание содержимого на устройстве, состоящем из свойств и данных, в этом разделе основное внимание уделяется созданию объекта, предназначенного только для свойств.</span><span class="sxs-lookup"><span data-stu-id="32188-104">While the example in the previous topic demonstrated the creation of content on a device consisting of both properties and data, this topic focuses on the creation of a properties-only object.</span></span>

<span data-ttu-id="32188-105">Передачи только свойств выполняются с помощью интерфейсов, описанных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="32188-105">Property-only transfers are accomplished using the interfaces described in the following table.</span></span>



| <span data-ttu-id="32188-106">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="32188-106">Interface</span></span>                                                          | <span data-ttu-id="32188-107">Описание</span><span class="sxs-lookup"><span data-stu-id="32188-107">Description</span></span>                                            |
|--------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="32188-108">**Интерфейс Ипортабледевицеконтент**</span><span class="sxs-lookup"><span data-stu-id="32188-108">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) | <span data-ttu-id="32188-109">Предоставляет доступ к методам, относящимся к содержимому.</span><span class="sxs-lookup"><span data-stu-id="32188-109">Provides access to the content-specific methods.</span></span>       |
| [<span data-ttu-id="32188-110">**Интерфейс Ипортабледевицевалуес**</span><span class="sxs-lookup"><span data-stu-id="32188-110">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)   | <span data-ttu-id="32188-111">Используется для получения свойств, описывающих содержимое.</span><span class="sxs-lookup"><span data-stu-id="32188-111">Used to retrieve properties that describe the content.</span></span> |



 

<span data-ttu-id="32188-112">`TransferContactToDevice`Функция в модуле контенттрансфер. cpp примера приложения демонстрирует, как приложение может передавать контактную информацию с компьютера на подключенное устройство.</span><span class="sxs-lookup"><span data-stu-id="32188-112">The `TransferContactToDevice` function in the sample application's ContentTransfer.cpp module demonstrates how an application could transfer contact information from a PC to a connected device.</span></span> <span data-ttu-id="32188-113">В этом конкретном примере переданное Контактное имя является жестко запрограммированным именем «Джон Кане», а переданный номер контактного телефона всегда равен «425-555-0123».</span><span class="sxs-lookup"><span data-stu-id="32188-113">In this particular sample, the transferred contact name is a hard-coded "John Kane" and the transferred contact phone number is always "425-555-0123".</span></span>

<span data-ttu-id="32188-114">Первая задача, выполняемая `TransferContactToDevice` функцией, — предложить пользователю ввести идентификатор объекта для родительского объекта на устройстве (при этом содержимое будет передано).</span><span class="sxs-lookup"><span data-stu-id="32188-114">The first task accomplished by the `TransferContactToDevice` function is to prompt the user to enter an object identifier for the parent object on the device (under which the content will be transferred).</span></span>


```C++
HRESULT                             hr = S_OK;
WCHAR                               szSelection[81]        = {0};
CComPtr<IPortableDeviceValues>      pFinalObjectProperties;
CComPtr<IPortableDeviceContent>     pContent;

// Prompt user to enter an object identifier for the parent object on the device to transfer.
printf("Enter the identifer of the parent object which the contact will be transferred under.\n>");
hr = StringCbGetsW(szSelection,sizeof(szSelection));
if (FAILED(hr))
{
    printf("An invalid object identifier was specified, aborting content transfer\n");
}
```



<span data-ttu-id="32188-115">Следующий шаг — получение свойств контакта, которые будут использоваться, когда образец записывает новый контакт на устройство.</span><span class="sxs-lookup"><span data-stu-id="32188-115">The next step is the retrieval of contact properties, which will be used when the sample writes the new contact to the device.</span></span> <span data-ttu-id="32188-116">Получение свойств контакта осуществляется `GetRequiredPropertiesForPropertiesOnlyContact` вспомогательной функцией.</span><span class="sxs-lookup"><span data-stu-id="32188-116">The retrieval of contact properties is performed by the `GetRequiredPropertiesForPropertiesOnlyContact` helper function.</span></span>


```C++
// 2) Get the properties that describe the object being created on the device

if (SUCCEEDED(hr))
{
    hr = GetRequiredPropertiesForPropertiesOnlyContact(szSelection,              // Parent to transfer the data under
                                                       &pFinalObjectProperties);  // Returned properties describing the data
    if (FAILED(hr))
    {
        printf("! Failed to get required properties needed to transfer an image file to the device, hr = 0x%lx\n", hr);
    }
}
```



<span data-ttu-id="32188-117">Эта функция записывает следующие данные в объект **ипортабледевицевалуес** .</span><span class="sxs-lookup"><span data-stu-id="32188-117">This function writes the following data to an **IPortableDeviceValues** object.</span></span>

-   <span data-ttu-id="32188-118">Идентификатор объекта для родителя контакта на устройстве.</span><span class="sxs-lookup"><span data-stu-id="32188-118">The object identifier for the contact's parent on the device.</span></span> <span data-ttu-id="32188-119">(Это место назначения, в котором устройство будет хранить объект.)</span><span class="sxs-lookup"><span data-stu-id="32188-119">(This is the destination where the device will store the object.)</span></span>
-   <span data-ttu-id="32188-120">Тип объекта (контакт).</span><span class="sxs-lookup"><span data-stu-id="32188-120">The object type (a contact).</span></span>
-   <span data-ttu-id="32188-121">Имя контакта (жестко запрограммированная строка "Джон Кане").</span><span class="sxs-lookup"><span data-stu-id="32188-121">The contact name (a hard coded string of "John Kane").</span></span>
-   <span data-ttu-id="32188-122">Номер контактного телефона (жестко закодированная строка "425-555-0123").</span><span class="sxs-lookup"><span data-stu-id="32188-122">The contact phone number (a hard-coded string of "425-555-0123").</span></span>

<span data-ttu-id="32188-123">На последнем шаге создается объект только для свойств на устройстве (с использованием свойств, заданных `GetRequiredPropertiesForPropertiesOnlyContact` вспомогательной функцией).</span><span class="sxs-lookup"><span data-stu-id="32188-123">The final step creates the properties-only object on the device (using the properties set by the `GetRequiredPropertiesForPropertiesOnlyContact` helper function).</span></span> <span data-ttu-id="32188-124">Это достигается путем вызова метода **ипортабледевицеконтент:: креатеобжектвиспропертиесонли** .</span><span class="sxs-lookup"><span data-stu-id="32188-124">This is accomplished by calling the **IPortableDeviceContent::CreateObjectWithPropertiesOnly** method.</span></span>


```C++
if (SUCCEEDED(hr))
{
    PWSTR pszNewlyCreatedObject = NULL;
    hr = pContent->CreateObjectWithPropertiesOnly(pFinalObjectProperties,    // Properties describing the object data
                                                  &pszNewlyCreatedObject);
    if (SUCCEEDED(hr))
    {
        printf("The contact was transferred to the device.\nThe newly created object's ID is '%ws'\n",pszNewlyCreatedObject);
    }

    if (FAILED(hr))
    {
        printf("! Failed to transfer contact object to the device, hr = 0x%lx\n",hr);
    }

    // Free the object identifier string returned from CreateObjectWithPropertiesOnly
    CoTaskMemFree(pszNewlyCreatedObject);
    pszNewlyCreatedObject = NULL;
}
```



## <a name="related-topics"></a><span data-ttu-id="32188-125">См. также</span><span class="sxs-lookup"><span data-stu-id="32188-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32188-126">**Интерфейс Ипортабледевице**</span><span class="sxs-lookup"><span data-stu-id="32188-126">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="32188-127">**Интерфейс Ипортабледевицеконтент**</span><span class="sxs-lookup"><span data-stu-id="32188-127">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="32188-128">**Интерфейс Ипортабледевицевалуес**</span><span class="sxs-lookup"><span data-stu-id="32188-128">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="32188-129">**Инструкции по программированию**</span><span class="sxs-lookup"><span data-stu-id="32188-129">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 




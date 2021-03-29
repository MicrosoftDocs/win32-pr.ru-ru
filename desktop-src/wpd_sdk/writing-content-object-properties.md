---
description: Запись свойств объекта
ms.assetid: f762a571-83ea-4999-ad49-a51044bc790d
title: Запись свойств объекта
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cb061288cbfde93f2baea1860581c25c61a8a0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647371"
---
# <a name="writing-object-properties"></a><span data-ttu-id="ba621-103">Запись свойств объекта</span><span class="sxs-lookup"><span data-stu-id="ba621-103">Writing Object Properties</span></span>

<span data-ttu-id="ba621-104">Службы часто содержат дочерние объекты, принадлежащие одному из форматов, поддерживаемых каждой службой.</span><span class="sxs-lookup"><span data-stu-id="ba621-104">Services often contain child objects that belong to one of the formats that each service supports.</span></span> <span data-ttu-id="ba621-105">Например, служба контактов может поддерживать несколько контактных объектов из формата абстрактного контакта.</span><span class="sxs-lookup"><span data-stu-id="ba621-105">For example, a Contacts service may support multiple contact objects of the Abstract Contact format.</span></span> <span data-ttu-id="ba621-106">Каждый объект Contact описывается связанными свойствами (имя контактного лица, номер телефона, адрес электронной почты и т. д.).</span><span class="sxs-lookup"><span data-stu-id="ba621-106">Each contact object is described by related properties (contact name, phone number, email address, and so on).</span></span>

<span data-ttu-id="ba621-107">Приложение Впдсервицесаписампле содержит код, демонстрирующий, как приложение может обновить свойство Name для дочернего объекта данной службы контактов.</span><span class="sxs-lookup"><span data-stu-id="ba621-107">The WpdServicesApiSample application includes code that demonstrates how an application can update the name property for a child object of the given Contacts service.</span></span> <span data-ttu-id="ba621-108">В этом примере используются следующие интерфейсы WPD.</span><span class="sxs-lookup"><span data-stu-id="ba621-108">This sample uses the following WPD interfaces.</span></span>



|                                                                |                                                                                                                                                                      |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba621-109">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="ba621-109">Interface</span></span>                                                      | <span data-ttu-id="ba621-110">Описание</span><span class="sxs-lookup"><span data-stu-id="ba621-110">Description</span></span>                                                                                                                                                          |
| [<span data-ttu-id="ba621-111">**ипортабледевицесервице**</span><span class="sxs-lookup"><span data-stu-id="ba621-111">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)       | <span data-ttu-id="ba621-112">Используется для получения интерфейса **IPortableDeviceContent2** для доступа к поддерживаемым методам службы.</span><span class="sxs-lookup"><span data-stu-id="ba621-112">Used to retrieve the **IPortableDeviceContent2** interface to access the supported service methods.</span></span>                                                                  |
| [<span data-ttu-id="ba621-113">**IPortableDeviceContent2**</span><span class="sxs-lookup"><span data-stu-id="ba621-113">**IPortableDeviceContent2**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)     | <span data-ttu-id="ba621-114">Предоставляет доступ к методам, относящимся к содержимому.</span><span class="sxs-lookup"><span data-stu-id="ba621-114">Provides access to the content-specific methods.</span></span>                                                                                                                     |
| [<span data-ttu-id="ba621-115">**ипортабледевицепропертиес**</span><span class="sxs-lookup"><span data-stu-id="ba621-115">**IPortableDeviceProperties**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) | <span data-ttu-id="ba621-116">Используется для записи значений свойств объекта и для определения возможности записи данного свойства</span><span class="sxs-lookup"><span data-stu-id="ba621-116">Used to write the object property values and to determine whether a given property can be written</span></span>                                                                    |
| [<span data-ttu-id="ba621-117">**ипортабледевицевалуес**</span><span class="sxs-lookup"><span data-stu-id="ba621-117">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)         | <span data-ttu-id="ba621-118">Используется для хранения записываемых значений свойств, определения результатов операции записи и получения атрибутов свойств (при определении возможности записи).</span><span class="sxs-lookup"><span data-stu-id="ba621-118">Used to hold the property values to be written, determine results of the write operation, and retrieve attributes of properties (when determining write capability).</span></span> |



 

<span data-ttu-id="ba621-119">Когда пользователь выбирает параметр "8" в командной строке, приложение вызывает метод **вритеконтентпропертиес** , который находится в модуле контентпропертиес. cpp.</span><span class="sxs-lookup"><span data-stu-id="ba621-119">When the user chooses option "8" at the command line, the application invokes the **WriteContentProperties** method that is found in the ContentProperties.cpp module.</span></span> <span data-ttu-id="ba621-120">Этот метод предлагает пользователю ввести идентификатор объекта для обновляемого свойства.</span><span class="sxs-lookup"><span data-stu-id="ba621-120">This method prompts the user to enter an object identifier for the property to be updated.</span></span> <span data-ttu-id="ba621-121">Пользователь определяет объект, и метод предлагает пользователю указать новое имя.</span><span class="sxs-lookup"><span data-stu-id="ba621-121">The user identifies the object, and the method prompts the user to specify a new name.</span></span> <span data-ttu-id="ba621-122">После указания этого имени метод обновляет свойство Name для заданного объекта.</span><span class="sxs-lookup"><span data-stu-id="ba621-122">After this name is specified, the method updates the Name property for the given object.</span></span>

<span data-ttu-id="ba621-123">Обратите внимание, что перед записью свойств объекта пример приложения открывает службу контактов на подключенном устройстве.</span><span class="sxs-lookup"><span data-stu-id="ba621-123">Note that prior to writing the object properties, the sample application opens a Contacts service on a connected device.</span></span>

<span data-ttu-id="ba621-124">В следующем коде для метода **вритеконтентпропертиес** показано, как приложение использует интерфейс [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2) для получения интерфейса [**ипортабледевицепропертиес**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) .</span><span class="sxs-lookup"><span data-stu-id="ba621-124">The following code for the **WriteContentProperties** method demonstrates how the application uses the [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2) interface to retrieve an [**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) interface.</span></span> <span data-ttu-id="ba621-125">Передавая ПРОПЕРТИКЭЙС запрошенных свойств в метод [**ипортабледевицепропертиес:: SetValue**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) , **вритеконтентпропертиес** обновляет свойство Name.</span><span class="sxs-lookup"><span data-stu-id="ba621-125">By passing the PROPERTYKEYS of the requested properties to the [**IPortableDeviceProperties::SetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) method, **WriteContentProperties** updates the name property.</span></span>


```C++
void WriteContentProperties(
 IPortableDeviceService* pService)
{
 if (pService == NULL)
 {
  printf("! A NULL IPortableDeviceService interface pointer was received\n");
  return;
 }

 HRESULT          hr       = S_OK;
 WCHAR         wszSelection[81]  = {0};
 WCHAR         wszNewObjectName[81] = {0};
 CComPtr<IPortableDeviceProperties> pProperties;
 CComPtr<IPortableDeviceContent2>   pContent;
 CComPtr<IPortableDeviceValues>  pObjectPropertiesToWrite;
 CComPtr<IPortableDeviceValues>  pPropertyWriteResults;
 CComPtr<IPortableDeviceValues>  pAttributes;
 BOOL          bCanWrite   = FALSE;

 // Prompt user to enter an object identifier on the device to write properties on.
 printf("Enter the identifer of the object you wish to write properties on.\n>");
 hr = StringCbGetsW(wszSelection,sizeof(wszSelection));
 if (FAILED(hr))
 {
  printf("An invalid object identifier was specified, aborting property reading\n");
 }

 // 1) Get an IPortableDeviceContent2 interface from the IPortableDeviceService interface to
 // access the content-specific methods.
 if (SUCCEEDED(hr))
 {
  hr = pService->Content(&pContent);
  if (FAILED(hr))
  {
   printf("! Failed to get IPortableDeviceContent2 from IPortableDeviceService, hr = 0x%lx\n",hr);
  }
 }

 // 2) Get an IPortableDeviceProperties interface from the IPortableDeviceContent2 interface
 // to access the property-specific methods.
 if (SUCCEEDED(hr))
 {
  hr = pContent->Properties(&pProperties);
  if (FAILED(hr))
  {
   printf("! Failed to get IPortableDeviceProperties from IPortableDeviceContent2, hr = 0x%lx\n",hr);
  }
 }

 // 3) Check the property attributes to see if we can write/change the NAME_GenericObj_Name property.
 if (SUCCEEDED(hr))
 {
  hr = pProperties->GetPropertyAttributes(wszSelection,
            PKEY_GenericObj_Name,
            &pAttributes);
  if (SUCCEEDED(hr))
  {
   hr = pAttributes->GetBoolValue(WPD_PROPERTY_ATTRIBUTE_CAN_WRITE, &bCanWrite);
   if (SUCCEEDED(hr))
   {
    if (bCanWrite)
    {
     printf("The attribute WPD_PROPERTY_ATTRIBUTE_CAN_WRITE for PKEY_GenericObj_Name reports TRUE\nThis means that the property can be changed/updated\n\n");
    }
    else
    {
     printf("The attribute WPD_PROPERTY_ATTRIBUTE_CAN_WRITE for PKEY_GenericObj_Name reports FALSE\nThis means that the property cannot be changed/updated\n\n");
    }
   }
   else
   {
    printf("! Failed to get the WPD_PROPERTY_ATTRIBUTE_CAN_WRITE value for PKEY_GenericObj_Name on object '%ws', hr = 0x%lx\n", wszSelection, hr);
   }
  }
 }

 // 4) Prompt the user for the new value of the NAME_GenericObj_Name property only if the property attributes report
 // that it can be changed/updated.
 if (bCanWrite)
 {
  printf("Enter the new PKEY_GenericObj_Name property for the object '%ws'.\n>",wszSelection);
  hr = StringCbGetsW(wszNewObjectName,sizeof(wszNewObjectName));
  if (FAILED(hr))
  {
   printf("An invalid PKEY_GenericObj_Name was specified, aborting property writing\n");
  }

  // 5) CoCreate an IPortableDeviceValues interface to hold the property values
  // we wish to write.
  if (SUCCEEDED(hr))
  {
   hr = CoCreateInstance(CLSID_PortableDeviceValues,
          NULL,
          CLSCTX_INPROC_SERVER,
          IID_IPortableDeviceValues,
          (VOID**) &pObjectPropertiesToWrite);
   if (SUCCEEDED(hr))
   {
    if (pObjectPropertiesToWrite != NULL)
    {
     hr = pObjectPropertiesToWrite->SetStringValue(PKEY_GenericObj_Name, wszNewObjectName);
     if (FAILED(hr))
     {
      printf("! Failed to add PKEY_GenericObj_Name to IPortableDeviceValues, hr= 0x%lx\n", hr);
     }
    }
   }
  }

  // 6) Call SetValues() passing the collection of specified PROPERTYKEYs.
  if (SUCCEEDED(hr))
  {
   hr = pProperties->SetValues(wszSelection,      // The object whose properties we are reading
          pObjectPropertiesToWrite,   // The properties we want to read
          &pPropertyWriteResults); // Driver supplied property result values for the property read operation
   if (FAILED(hr))
   {
    printf("! Failed to set properties for object '%ws', hr= 0x%lx\n", wszSelection, hr);
   }
   else
   {
    printf("The PKEY_GenericObj_Name property on object '%ws' was written successfully (Read the properties again to see the updated value)\n", wszSelection);
   }
  }
 }
}
```



## <a name="related-topics"></a><span data-ttu-id="ba621-126">См. также</span><span class="sxs-lookup"><span data-stu-id="ba621-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba621-127">**IPortableDeviceContent2**</span><span class="sxs-lookup"><span data-stu-id="ba621-127">**IPortableDeviceContent2**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)
</dt> <dt>

[<span data-ttu-id="ba621-128">**ипортабледевицепропертиес**</span><span class="sxs-lookup"><span data-stu-id="ba621-128">**IPortableDeviceProperties**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[<span data-ttu-id="ba621-129">впдсервицесаписампле</span><span class="sxs-lookup"><span data-stu-id="ba621-129">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 




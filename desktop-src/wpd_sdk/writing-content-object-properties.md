---
description: Запись свойств объекта
ms.assetid: f762a571-83ea-4999-ad49-a51044bc790d
title: Запись свойств объекта
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e140563c6cf17235d3709e0d53cbfda9ab602076c3e72c010570b004429c96e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657334"
---
# <a name="writing-object-properties"></a>Запись свойств объекта

Службы часто содержат дочерние объекты, принадлежащие одному из форматов, поддерживаемых каждой службой. Например, служба контактов может поддерживать несколько контактных объектов из формата абстрактного контакта. Каждый объект Contact описывается связанными свойствами (имя контактного лица, номер телефона, адрес электронной почты и т. д.).

Приложение Впдсервицесаписампле содержит код, демонстрирующий, как приложение может обновить свойство Name для дочернего объекта данной службы контактов. В этом примере используются следующие интерфейсы WPD.



| Интерфейс                                                      | Описание                                                                                                                                                          |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ипортабледевицесервице**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)       | Используется для получения интерфейса **IPortableDeviceContent2** для доступа к поддерживаемым методам службы.                                                                  |
| [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)     | Предоставляет доступ к методам, относящимся к содержимому.                                                                                                                     |
| [**ипортабледевицепропертиес**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) | Используется для записи значений свойств объекта и для определения возможности записи данного свойства                                                                    |
| [**ипортабледевицевалуес**](iportabledevicevalues.md)         | Используется для хранения записываемых значений свойств, определения результатов операции записи и получения атрибутов свойств (при определении возможности записи). |



 

Когда пользователь выбирает параметр "8" в командной строке, приложение вызывает метод **вритеконтентпропертиес** , который находится в модуле контентпропертиес. cpp. Этот метод предлагает пользователю ввести идентификатор объекта для обновляемого свойства. Пользователь определяет объект, и метод предлагает пользователю указать новое имя. После указания этого имени метод обновляет свойство Name для заданного объекта.

Обратите внимание, что перед записью свойств объекта пример приложения открывает службу контактов на подключенном устройстве.

В следующем коде для метода **вритеконтентпропертиес** показано, как приложение использует интерфейс [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2) для получения интерфейса [**ипортабледевицепропертиес**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) . Передавая ПРОПЕРТИКЭЙС запрошенных свойств в метод [**ипортабледевицепропертиес:: SetValue**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) , **вритеконтентпропертиес** обновляет свойство Name.


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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)
</dt> <dt>

[**ипортабледевицепропертиес**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[впдсервицесаписампле](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 




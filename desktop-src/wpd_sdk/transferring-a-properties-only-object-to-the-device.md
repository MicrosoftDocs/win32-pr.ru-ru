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
# <a name="transferring-a-properties-only-object-to-the-device"></a>Передача объекта Properties-Only на устройство

Хотя в примере из предыдущего раздела показано создание содержимого на устройстве, состоящем из свойств и данных, в этом разделе основное внимание уделяется созданию объекта, предназначенного только для свойств.

Передачи только свойств выполняются с помощью интерфейсов, описанных в следующей таблице.



| Интерфейс                                                          | Описание                                            |
|--------------------------------------------------------------------|--------------------------------------------------------|
| [**Интерфейс Ипортабледевицеконтент**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) | Предоставляет доступ к методам, относящимся к содержимому.       |
| [**Интерфейс Ипортабледевицевалуес**](iportabledevicevalues.md)   | Используется для получения свойств, описывающих содержимое. |



 

`TransferContactToDevice`Функция в модуле контенттрансфер. cpp примера приложения демонстрирует, как приложение может передавать контактную информацию с компьютера на подключенное устройство. В этом конкретном примере переданное Контактное имя является жестко запрограммированным именем «Джон Кане», а переданный номер контактного телефона всегда равен «425-555-0123».

Первая задача, выполняемая `TransferContactToDevice` функцией, — предложить пользователю ввести идентификатор объекта для родительского объекта на устройстве (при этом содержимое будет передано).


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



Следующий шаг — получение свойств контакта, которые будут использоваться, когда образец записывает новый контакт на устройство. Получение свойств контакта осуществляется `GetRequiredPropertiesForPropertiesOnlyContact` вспомогательной функцией.


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



Эта функция записывает следующие данные в объект **ипортабледевицевалуес** .

-   Идентификатор объекта для родителя контакта на устройстве. (Это место назначения, в котором устройство будет хранить объект.)
-   Тип объекта (контакт).
-   Имя контакта (жестко запрограммированная строка "Джон Кане").
-   Номер контактного телефона (жестко закодированная строка "425-555-0123").

На последнем шаге создается объект только для свойств на устройстве (с использованием свойств, заданных `GetRequiredPropertiesForPropertiesOnlyContact` вспомогательной функцией). Это достигается путем вызова метода **ипортабледевицеконтент:: креатеобжектвиспропертиесонли** .


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



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Интерфейс Ипортабледевице**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**Интерфейс Ипортабледевицеконтент**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[**Интерфейс Ипортабледевицевалуес**](iportabledevicevalues.md)
</dt> <dt>

[**Инструкции по программированию**](programming-guide.md)
</dt> </dl>

 

 




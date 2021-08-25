---
description: Получение идентификатора объекта из постоянного уникального идентификатора
ms.assetid: 146f8943-d4e1-4b87-a812-e534082a4f14
title: Получение идентификатора объекта из постоянного уникального идентификатора
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6d4f08d496c7c03101602c945e6c27e7a2624fe84957eda932ead806f964d3f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054774"
---
# <a name="retrieving-an-object-id-from-a-persistent-unique-id"></a>Получение идентификатора объекта из постоянного уникального идентификатора

Идентификаторы объектов гарантированно уникальны только для данного сеанса устройства; Если пользователь устанавливает новое соединение, идентификаторы из предыдущего сеанса могут не совпадать с идентификаторами текущего сеанса. Чтобы устранить эту проблему, API-интерфейс WPD поддерживает постоянные уникальные идентификаторы (Пуидс), которые сохраняются в сеансах устройств.

Некоторые устройства хранят свои Пуидс в собственном виде с помощью заданного объекта. Другие могут создать PUID на основе хэша выбранных данных объекта. Другие могут рассматривать идентификаторы объектов как Пуидс (поскольку они могут гарантировать, что эти идентификаторы никогда не изменяются).

Функция Жетобжектидентифиерфромперсистентуникуеидентифиер в модуле Контентпропертиес. cpp демонстрирует извлечение идентификатора объекта для заданного PUID.

Приложение может получить идентификатор объекта для соответствующего PUID с помощью интерфейсов, описанных в следующей таблице.



| Интерфейс                                                                                      | Описание                                                                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**Интерфейс Ипортабледевицеконтент**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | Предоставляет доступ к методу получения.                                                            |
| [**Интерфейс Ипортабледевицепропвариантколлектион**](iportabledevicepropvariantcollection.md) | Используется для хранения идентификатора объекта и соответствующего постоянного уникального идентификатора (PUID). |



 

Первая задача, которую выполняет образец приложения, — получение PUID от пользователя.


```C++
// Prompt user to enter an unique identifier to convert to an object idenifier.
printf("Enter the Persistant Unique Identifier of the object you wish to convert into an object identifier.\n>");
hr = StringCbGetsW(szSelection,sizeof(szSelection));
if (FAILED(hr))
{
    printf("An invalid persistent object identifier was specified, aborting the query operation\n");
}
```



После этого пример приложения извлекает объект [**ипортабледевицеконтент**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) , который будет использоваться для вызова метода [**жетобжектидсфромперсистентуникуеидс**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-getobjectidsfrompersistentuniqueids) .


```C++
if (SUCCEEDED(hr))
{
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }
}
```



Затем создается объект [**ипортабледевицепропвариантколлектион**](iportabledevicepropvariantcollection.md) , который будет содержать идентификатор PUID, предоставленный пользователем.


```C++
hr = CoCreateInstance(CLSID_PortableDevicePropVariantCollection,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(&pPersistentUniqueIDs));
```



После выполнения предыдущих трех действий пример готов получить идентификатор объекта, соответствующий PUID, предоставленному пользователем. Это достигается путем вызова метода [**ипортабледевицеконтент:: жетобжектидсфромперсистентуникуеидс**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-getobjectidsfrompersistentuniqueids) . Перед вызовом этого метода пример инициализирует структуру ПРОПВАРИАНТ, записывает в эту структуру PUID, предоставленный пользователем, и добавляет его в объект Ипортабледевицепропвариантколлектион, где Пперсистентуникуеидс указывает. Этот указатель передается в качестве первого аргумента в метод Жетобжектидсфромперсистентуникуеидс. Вторым аргументом Жетобжектидсфромперсистентуникуеидс является объект Ипортабледевицепропвариантколлектион, который получает соответствующий идентификатор объекта.


```C++
if (SUCCEEDED(hr))
{
    if (pPersistentUniqueIDs != NULL)
    {
        PROPVARIANT pv = {0};
        PropVariantInit(&pv);

        // Initialize a PROPVARIANT structure with the object identifier string
        // that the user selected above. Notice we are allocating memory for the
        // PWSTR value.  This memory will be freed when PropVariantClear() is
        // called below.
        pv.vt      = VT_LPWSTR;
        pv.pwszVal = AtlAllocTaskWideString(szSelection);
        if (pv.pwszVal != NULL)
        {
            // Add the object identifier to the objects-to-delete list
            // (We are only deleting 1 in this example)
            hr = pPersistentUniqueIDs->Add(&pv);
            if (SUCCEEDED(hr))
            {
                // 3) Attempt to get the unique idenifier for the object from the device
                hr = pContent->GetObjectIDsFromPersistentUniqueIDs(pPersistentUniqueIDs,
                                                                   &pObjectIDs);
                if (SUCCEEDED(hr))
                {
                    PROPVARIANT pvId = {0};
                    hr = pObjectIDs->GetAt(0, &pvId);
                    if (SUCCEEDED(hr))
                    {
                        printf("The persistent unique identifier '%ws' relates to object identifier '%ws' on the device.\n", szSelection, pvId.pwszVal);
                    }
                    else
                    {
                        printf("! Failed to get the object identifier for '%ws' from the IPortableDevicePropVariantCollection, hr = 0x%lx\n",szSelection, hr);
                    }

                    // Free the returned allocated string from the GetAt() call
                    PropVariantClear(&pvId);
                }
                else
                {
                    printf("! Failed to get the object identifier from persistent object idenifier '%ws', hr = 0x%lx\n",szSelection, hr);
                }
            }
            else
            {
                printf("! Failed to get the object identifier from persistent object idenifier because we could no add the persistent object identifier string to the IPortableDevicePropVariantCollection, hr = 0x%lx\n",hr);
            }
        }
        else
        {
            hr = E_OUTOFMEMORY;
            printf("! Failed to get the object identifier because we could no allocate memory for the persistent object identifier string, hr = 0x%lx\n",hr);
        }

        // Free any allocated values in the PROPVARIANT before exiting
        PropVariantClear(&pv);
    }
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Интерфейс Ипортабледевице**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**Интерфейс Ипортабледевицеконтент**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[**Интерфейс Ипортабледевицепропвариантколлектион**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[**Инструкции по программированию**](programming-guide.md)
</dt> </dl>

 

 




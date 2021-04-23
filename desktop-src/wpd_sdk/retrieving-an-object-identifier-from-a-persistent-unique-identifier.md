---
description: Получение идентификатора объекта из постоянного уникального идентификатора
ms.assetid: 146f8943-d4e1-4b87-a812-e534082a4f14
title: Получение идентификатора объекта из постоянного уникального идентификатора
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4f997f0faf586a374e5a83c6f96b6508f02eb41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712482"
---
# <a name="retrieving-an-object-id-from-a-persistent-unique-id"></a><span data-ttu-id="50ed2-103">Получение идентификатора объекта из постоянного уникального идентификатора</span><span class="sxs-lookup"><span data-stu-id="50ed2-103">Retrieving an Object Id from a Persistent Unique Id</span></span>

<span data-ttu-id="50ed2-104">Идентификаторы объектов гарантированно уникальны только для данного сеанса устройства; Если пользователь устанавливает новое соединение, идентификаторы из предыдущего сеанса могут не совпадать с идентификаторами текущего сеанса.</span><span class="sxs-lookup"><span data-stu-id="50ed2-104">Object identifiers are only guaranteed to be unique for a given device session; if the user establishes a new connection, identifiers from a previous session may not match identifiers for the current session.</span></span> <span data-ttu-id="50ed2-105">Чтобы устранить эту проблему, API-интерфейс WPD поддерживает постоянные уникальные идентификаторы (Пуидс), которые сохраняются в сеансах устройств.</span><span class="sxs-lookup"><span data-stu-id="50ed2-105">To resolve this issue, the WPD API supports persistent unique identifiers (PUIDs), which persist across device sessions.</span></span>

<span data-ttu-id="50ed2-106">Некоторые устройства хранят свои Пуидс в собственном виде с помощью заданного объекта.</span><span class="sxs-lookup"><span data-stu-id="50ed2-106">Some devices store their PUIDs natively with a given object.</span></span> <span data-ttu-id="50ed2-107">Другие могут создать PUID на основе хэша выбранных данных объекта.</span><span class="sxs-lookup"><span data-stu-id="50ed2-107">Others may generate the PUID based on a hash of selected object data.</span></span> <span data-ttu-id="50ed2-108">Другие могут рассматривать идентификаторы объектов как Пуидс (поскольку они могут гарантировать, что эти идентификаторы никогда не изменяются).</span><span class="sxs-lookup"><span data-stu-id="50ed2-108">Others may treat object identifiers as PUIDs (because they can guarantee that these identifiers never change).</span></span>

<span data-ttu-id="50ed2-109">Функция Жетобжектидентифиерфромперсистентуникуеидентифиер в модуле Контентпропертиес. cpp демонстрирует извлечение идентификатора объекта для заданного PUID.</span><span class="sxs-lookup"><span data-stu-id="50ed2-109">The GetObjectIdentifierFromPersistentUniqueIdentifier function in the ContentProperties.cpp module demonstrates the retrieval of an object identifier for a given PUID.</span></span>

<span data-ttu-id="50ed2-110">Приложение может получить идентификатор объекта для соответствующего PUID с помощью интерфейсов, описанных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="50ed2-110">Your application can retrieve an object identifier for a corresponding PUID using the interfaces described in the following table.</span></span>



| <span data-ttu-id="50ed2-111">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="50ed2-111">Interface</span></span>                                                                                      | <span data-ttu-id="50ed2-112">Описание</span><span class="sxs-lookup"><span data-stu-id="50ed2-112">Description</span></span>                                                                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="50ed2-113">**Интерфейс Ипортабледевицеконтент**</span><span class="sxs-lookup"><span data-stu-id="50ed2-113">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | <span data-ttu-id="50ed2-114">Предоставляет доступ к методу получения.</span><span class="sxs-lookup"><span data-stu-id="50ed2-114">Provides access to the retrieval method.</span></span>                                                            |
| [<span data-ttu-id="50ed2-115">**Интерфейс Ипортабледевицепропвариантколлектион**</span><span class="sxs-lookup"><span data-stu-id="50ed2-115">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="50ed2-116">Используется для хранения идентификатора объекта и соответствующего постоянного уникального идентификатора (PUID).</span><span class="sxs-lookup"><span data-stu-id="50ed2-116">Used to store both the object identifier and the corresponding persistent unique identifier (PUID).</span></span> |



 

<span data-ttu-id="50ed2-117">Первая задача, которую выполняет образец приложения, — получение PUID от пользователя.</span><span class="sxs-lookup"><span data-stu-id="50ed2-117">The first task that the sample application accomplishes is to obtain a PUID from the user.</span></span>


```C++
// Prompt user to enter an unique identifier to convert to an object idenifier.
printf("Enter the Persistant Unique Identifier of the object you wish to convert into an object identifier.\n>");
hr = StringCbGetsW(szSelection,sizeof(szSelection));
if (FAILED(hr))
{
    printf("An invalid persistent object identifier was specified, aborting the query operation\n");
}
```



<span data-ttu-id="50ed2-118">После этого пример приложения извлекает объект [**ипортабледевицеконтент**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) , который будет использоваться для вызова метода [**жетобжектидсфромперсистентуникуеидс**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-getobjectidsfrompersistentuniqueids) .</span><span class="sxs-lookup"><span data-stu-id="50ed2-118">After this, the sample application retrieves an [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) object, which it will use to invoke the [**GetObjectIDsFromPersistentUniqueIDs**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-getobjectidsfrompersistentuniqueids) method.</span></span>


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



<span data-ttu-id="50ed2-119">Затем создается объект [**ипортабледевицепропвариантколлектион**](iportabledevicepropvariantcollection.md) , который будет содержать идентификатор PUID, предоставленный пользователем.</span><span class="sxs-lookup"><span data-stu-id="50ed2-119">Next, it creates an [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) object that will hold the PUID supplied by the user.</span></span>


```C++
hr = CoCreateInstance(CLSID_PortableDevicePropVariantCollection,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(&pPersistentUniqueIDs));
```



<span data-ttu-id="50ed2-120">После выполнения предыдущих трех действий пример готов получить идентификатор объекта, соответствующий PUID, предоставленному пользователем.</span><span class="sxs-lookup"><span data-stu-id="50ed2-120">Once the previous three steps are taken, the sample is ready to retrieve the object identifier that matches the PUID supplied by the user.</span></span> <span data-ttu-id="50ed2-121">Это достигается путем вызова метода [**ипортабледевицеконтент:: жетобжектидсфромперсистентуникуеидс**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-getobjectidsfrompersistentuniqueids) .</span><span class="sxs-lookup"><span data-stu-id="50ed2-121">This is accomplished by calling the [**IPortableDeviceContent::GetObjectIDsFromPersistentUniqueIDs**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-getobjectidsfrompersistentuniqueids) method.</span></span> <span data-ttu-id="50ed2-122">Перед вызовом этого метода пример инициализирует структуру ПРОПВАРИАНТ, записывает в эту структуру PUID, предоставленный пользователем, и добавляет его в объект Ипортабледевицепропвариантколлектион, где Пперсистентуникуеидс указывает.</span><span class="sxs-lookup"><span data-stu-id="50ed2-122">Prior to calling this method, the sample initializes a PROPVARIANT structure, writes the PUID supplied by the user to this structure, and adds it to the IPortableDevicePropVariantCollection object at which pPersistentUniqueIDs points.</span></span> <span data-ttu-id="50ed2-123">Этот указатель передается в качестве первого аргумента в метод Жетобжектидсфромперсистентуникуеидс.</span><span class="sxs-lookup"><span data-stu-id="50ed2-123">This pointer is passed as the first argument to the GetObjectIDsFromPersistentUniqueIDs method.</span></span> <span data-ttu-id="50ed2-124">Вторым аргументом Жетобжектидсфромперсистентуникуеидс является объект Ипортабледевицепропвариантколлектион, который получает соответствующий идентификатор объекта.</span><span class="sxs-lookup"><span data-stu-id="50ed2-124">The second argument of GetObjectIDsFromPersistentUniqueIDs is an IPortableDevicePropVariantCollection object that receives the matching object identifier.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="50ed2-125">См. также</span><span class="sxs-lookup"><span data-stu-id="50ed2-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50ed2-126">**Интерфейс Ипортабледевице**</span><span class="sxs-lookup"><span data-stu-id="50ed2-126">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="50ed2-127">**Интерфейс Ипортабледевицеконтент**</span><span class="sxs-lookup"><span data-stu-id="50ed2-127">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="50ed2-128">**Интерфейс Ипортабледевицепропвариантколлектион**</span><span class="sxs-lookup"><span data-stu-id="50ed2-128">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="50ed2-129">**Инструкции по программированию**</span><span class="sxs-lookup"><span data-stu-id="50ed2-129">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 




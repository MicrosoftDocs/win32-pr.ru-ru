---
title: Изменение атрибутов с помощью интерфейса Идиректорйобжект
description: Помимо параметров IADs Путекс и IADs, для изменения значений атрибутов можно использовать метод Идиректорйобжект Сетобжектаттрибутес. Чтобы использовать этот метод, необходимо ввести \_ \_ структуру сведений о attr для каждого изменяемого атрибута.
ms.assetid: 1d3fe8f6-34be-4bcb-8ba5-2d92ddc0852a
ms.tgt_platform: multiple
keywords:
- Изменение атрибутов с помощью интерфейса Идиректорйобжект ADSI
- Идиректорйобжект ADSI, использование для изменения атрибутов
- ADSI ADSI, пример кода C/C++, использование Идиректорйобжект для изменения атрибутов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8715826d0fc835f3d9ecae914fcc51603883af5d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104132795"
---
# <a name="modifying-attributes-with-the-idirectoryobject-interface"></a><span data-ttu-id="e49ce-107">Изменение атрибутов с помощью интерфейса Идиректорйобжект</span><span class="sxs-lookup"><span data-stu-id="e49ce-107">Modifying Attributes with the IDirectoryObject Interface</span></span>

<span data-ttu-id="e49ce-108">Помимо [**iAds::P UT**](/windows/desktop/api/Iads/nf-iads-iads-put) и [**iAds::P утекс**](/windows/desktop/api/Iads/nf-iads-iads-putex), для изменения значений атрибутов можно использовать метод [**идиректорйобжект:: сетобжектаттрибутес**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) .</span><span class="sxs-lookup"><span data-stu-id="e49ce-108">In addition to [**IADs::Put**](/windows/desktop/api/Iads/nf-iads-iads-put) and [**IADs::PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex), you can use the [**IDirectoryObject::SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) method to modify attribute values.</span></span> <span data-ttu-id="e49ce-109">Чтобы использовать этот метод, необходимо ввести структуру [**\_ \_ сведений о attr**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) для каждого изменяемого атрибута.</span><span class="sxs-lookup"><span data-stu-id="e49ce-109">To use this method, you must fill in an [**ADS\_ATTR\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) structure for each attribute to modify.</span></span>

<span data-ttu-id="e49ce-110">Метод [**идиректорйобжект:: сетобжектаттрибутес**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) позволяет изменять атрибуты с одним и несколькими значениями.</span><span class="sxs-lookup"><span data-stu-id="e49ce-110">The [**IDirectoryObject::SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) method enables you to modify both single-valued and multi-valued attributes.</span></span> <span data-ttu-id="e49ce-111">Эта функция предоставляет аналогичные операционные элементы управления, такие как Clear, Append, DELETE и Update, для тех, которые найдены в методе [**iAds::P утекс**](/windows/desktop/api/Iads/nf-iads-iads-putex) .</span><span class="sxs-lookup"><span data-stu-id="e49ce-111">This function provides similar operational controls, such as clear, append, delete, and update, to those found in the [**IADs::PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) method.</span></span> <span data-ttu-id="e49ce-112">К константам элемента управления относятся:</span><span class="sxs-lookup"><span data-stu-id="e49ce-112">The control constants include:</span></span>

-   [<span data-ttu-id="e49ce-113">**\_ \_ четкое объявление attr**</span><span class="sxs-lookup"><span data-stu-id="e49ce-113">**ADS\_ATTR\_CLEAR**</span></span>](adsi-attribute-modification-types.md)
-   [<span data-ttu-id="e49ce-114">**\_Обновление attr для ADS \_**</span><span class="sxs-lookup"><span data-stu-id="e49ce-114">**ADS\_ATTR\_UPDATE**</span></span>](adsi-attribute-modification-types.md)
-   [<span data-ttu-id="e49ce-115">**\_Добавление attr \_ ADS**</span><span class="sxs-lookup"><span data-stu-id="e49ce-115">**ADS\_ATTR\_APPEND**</span></span>](adsi-attribute-modification-types.md)
-   [<span data-ttu-id="e49ce-116">**\_Удаление AD attr \_**</span><span class="sxs-lookup"><span data-stu-id="e49ce-116">**ADS\_ATTR\_DELETE**</span></span>](adsi-attribute-modification-types.md)

<span data-ttu-id="e49ce-117">При указании [**\_ \_ обновления attr**](adsi-attribute-modification-types.md) запустится операция на стороне сервера, которая может потребовать много ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e49ce-117">Specifying [**ADS\_ATTR\_UPDATE**](adsi-attribute-modification-types.md) will trigger a server side operation that can be resource-intensive.</span></span> <span data-ttu-id="e49ce-118">Примером может быть запуск операции обновления длинного списка членства в группе.</span><span class="sxs-lookup"><span data-stu-id="e49ce-118">An example would be to initiate the operation to update a long list of group membership.</span></span> <span data-ttu-id="e49ce-119">Как правило, не следует использовать эту операцию, если только изменение не включает небольшое количество атрибутов в каталоге.</span><span class="sxs-lookup"><span data-stu-id="e49ce-119">In general, refrain from using this operation unless the modification involves a small number of attributes in the directory.</span></span> <span data-ttu-id="e49ce-120">Чтобы изменить длинный список членств в группах, более эффективным подходом будет чтение списка из базового каталога, внесение изменений и сохранение обновленного списка в каталоге.</span><span class="sxs-lookup"><span data-stu-id="e49ce-120">To modify a long list of group memberships, the more efficient approach would be to read the list from the underlying directory, make modifications, and store the updated list back to the directory.</span></span>

> [!Note]  
> <span data-ttu-id="e49ce-121">Как и [**iAds::P UT**](/windows/desktop/api/Iads/nf-iads-iads-put) и [**iAds::P утекс**](/windows/desktop/api/Iads/nf-iads-iads-putex) с параметром [**iAds:: сетинфо**](/windows/desktop/api/Iads/nf-iads-iads-setinfo), изменения атрибутов либо полностью фиксируются, либо отбрасываются в Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e49ce-121">Like [**IADs::Put**](/windows/desktop/api/Iads/nf-iads-iads-put) and [**IADs::PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) with [**IADs::SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo), the attribute changes are either completely committed or discarded in Active Directory.</span></span> <span data-ttu-id="e49ce-122">Если одно или несколько изменений не разрешены и поэтому не могут быть выполнены, то ни одна из общих изменений атрибутов не зафиксирована в каталоге.</span><span class="sxs-lookup"><span data-stu-id="e49ce-122">If one or more of the modifications are not allowed and therefore not able to be performed, then none of the collective modifications made to the attributes are committed to the directory.</span></span>

 

## <a name="example"></a><span data-ttu-id="e49ce-123">Пример</span><span class="sxs-lookup"><span data-stu-id="e49ce-123">Example</span></span>

<span data-ttu-id="e49ce-124">В следующем примере кода показано, как изменить атрибуты с одним и несколькими значениями с помощью метода [**идиректорйобжект:: сетобжектаттрибутес**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) .</span><span class="sxs-lookup"><span data-stu-id="e49ce-124">The following code example shows how to modify both single and multi-valued attributes with the [**IDirectoryObject::SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) method.</span></span>


```C++
HRESULT hr;
LPCWSTR pwszADsPath = L"LDAP://CN=Jeff Smith,OU=Sales,DC=Fabrikam,DC=com";
IDirectoryObject *pDirObject = NULL;

// Bind to the object.
hr = ADsGetObject(pwszADsPath, IID_IDirectoryObject, (void**)&pDirObject);
if(SUCCEEDED(hr))
{ 
    ADSVALUE adsvFaxNumber;
    ADSVALUE rgadsvOtherTelephones[2];
     
    // Set the new FAX number.
    adsvFaxNumber.dwType = ADSTYPE_CASE_IGNORE_STRING; 
    adsvFaxNumber.CaseIgnoreString = L"425-707-9790";

    // Set the first telephone number.
    rgadsvOtherTelephones[0].dwType = ADSTYPE_CASE_IGNORE_STRING;
    rgadsvOtherTelephones[0].CaseIgnoreString = L"425-707-9791";

    // Set the second telephone number.
    rgadsvOtherTelephones[1].dwType = ADSTYPE_CASE_IGNORE_STRING;
    rgadsvOtherTelephones[1].CaseIgnoreString = L"425-707-9792";

    ADS_ATTR_INFO attrInfo[2];

    // Setup the facsimileTelephoneNumber attribute data.
    attrInfo[0].pszAttrName = L"facsimileTelephoneNumber";
    attrInfo[0].dwControlCode = ADS_ATTR_UPDATE;
    attrInfo[0].dwADsType = adsvFaxNumber.dwType;
    attrInfo[0].pADsValues = &adsvFaxNumber;
    attrInfo[0].dwNumValues = 1;

    // Setup the otherTelephone attribute data.
    attrInfo[1].pszAttrName = L"otherTelephone";
    attrInfo[1].dwControlCode = ADS_ATTR_UPDATE;
    attrInfo[1].dwADsType = rgadsvOtherTelephones[0].dwType;
    attrInfo[1].pADsValues = rgadsvOtherTelephones;
    attrInfo[1].dwNumValues = sizeof(rgadsvOtherTelephones)/sizeof(ADSVALUE);

    DWORD dwReturn;
 
    // Set the new attribute values.
    hr = pDirObject->SetObjectAttributes(attrInfo, 
        sizeof(attrInfo)/sizeof(ADS_ATTR_INFO), 
        &dwReturn);

    pDirObject->Release();
}
```



 

 





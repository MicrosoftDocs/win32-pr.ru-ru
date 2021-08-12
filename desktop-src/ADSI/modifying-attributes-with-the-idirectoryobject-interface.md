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
ms.openlocfilehash: 30fa7d75d3e0dce489f676dafb36992c95a1cba2e9856bbbaf49f14806a6c1ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118179032"
---
# <a name="modifying-attributes-with-the-idirectoryobject-interface"></a>Изменение атрибутов с помощью интерфейса Идиректорйобжект

Помимо [**iAds::P UT**](/windows/desktop/api/Iads/nf-iads-iads-put) и [**iAds::P утекс**](/windows/desktop/api/Iads/nf-iads-iads-putex), для изменения значений атрибутов можно использовать метод [**идиректорйобжект:: сетобжектаттрибутес**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) . Чтобы использовать этот метод, необходимо ввести структуру [**\_ \_ сведений о attr**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) для каждого изменяемого атрибута.

Метод [**идиректорйобжект:: сетобжектаттрибутес**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) позволяет изменять атрибуты с одним и несколькими значениями. Эта функция предоставляет аналогичные операционные элементы управления, такие как Clear, Append, DELETE и Update, для тех, которые найдены в методе [**iAds::P утекс**](/windows/desktop/api/Iads/nf-iads-iads-putex) . К константам элемента управления относятся:

-   [**\_ \_ четкое объявление attr**](adsi-attribute-modification-types.md)
-   [**\_Обновление attr для ADS \_**](adsi-attribute-modification-types.md)
-   [**\_Добавление attr \_ ADS**](adsi-attribute-modification-types.md)
-   [**\_Удаление AD attr \_**](adsi-attribute-modification-types.md)

При указании [**\_ \_ обновления attr**](adsi-attribute-modification-types.md) запустится операция на стороне сервера, которая может потребовать много ресурсов. Примером может быть запуск операции обновления длинного списка членства в группе. Как правило, не следует использовать эту операцию, если только изменение не включает небольшое количество атрибутов в каталоге. Чтобы изменить длинный список членств в группах, более эффективным подходом будет чтение списка из базового каталога, внесение изменений и сохранение обновленного списка в каталоге.

> [!Note]  
> Как и [**iAds::P UT**](/windows/desktop/api/Iads/nf-iads-iads-put) и [**iAds::P утекс**](/windows/desktop/api/Iads/nf-iads-iads-putex) с параметром [**iAds:: сетинфо**](/windows/desktop/api/Iads/nf-iads-iads-setinfo), изменения атрибутов либо полностью фиксируются, либо отбрасываются в Active Directory. Если одно или несколько изменений не разрешены и поэтому не могут быть выполнены, то ни одна из общих изменений атрибутов не зафиксирована в каталоге.

 

## <a name="example"></a>Пример

В следующем примере кода показано, как изменить атрибуты с одним и несколькими значениями с помощью метода [**идиректорйобжект:: сетобжектаттрибутес**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) .


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



 

 





---
title: Добавление вспомогательного класса к экземпляру объекта
description: В следующем примере кода показано, как использовать ADSI и LDAP для динамического добавления вспомогательного класса к существующему экземпляру объекта.
ms.assetid: 739dd372-3bda-4d94-8daf-f71e3091cfb6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46a6b1f61bffe9081350949cccddc70fee83a568
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104069824"
---
# <a name="adding-an-auxiliary-class-to-an-object-instance"></a>Добавление вспомогательного класса к экземпляру объекта

В следующем примере кода показано, как использовать ADSI и LDAP для динамического добавления вспомогательного класса к существующему экземпляру объекта. В примерах предполагается, что вспомогательный класс с именем **Vehicle** определен в схеме Active Directory и что класс **ТС** имеет атрибут **VIN** .

При динамическом добавлении вспомогательного класса к экземпляру объекта необходимо одновременно указать значения для всех обязательных атрибутов **муссаве** в классе. В следующих примерах показано, как это сделать с помощью атрибута "Vin", который должен быть обязательным.

Следующий пример C++ привязывает к объекту и использует метод [**iAds. путекс**](/windows/desktop/api/iads/nf-iads-iads-putex) для добавления вспомогательного класса к списку классов в свойстве **objectClass** объекта. Затем в примере используется метод [**iAds.**](/windows/desktop/api/iads/nf-iads-iads-put) Set, чтобы задать значение атрибута **VIN** . Наконец, он вызывает функцию [**iAds. сетинфо**](/windows/desktop/api/iads/nf-iads-iads-setinfo) для фиксации изменений в каталоге.


```C++
LPWSTR pszAuxClass[]={L"vehicle"};
LPWSTR pszVIN[]={L"df897dsfsa-0"};
VARIANT var;

VariantInit(&var);

ADsOpenObject(L"cn=johnd,cn=users,dc=fabrikam,dc=com", 
    NULL, 
    NULL, 
    ADS_SECURE_AUTHENTICATION, 
    IID_IADs,  
    (VOID**)&pIADs);

ADsBuildVarArrayStr(pszAuxClass, 1, &var);
pIADs->PutEx(ADS_PROPERTY_APPEND, CComBSTR("objectClass"), var);
ADsBuildVarArrayStr( pszVIN, 1, &var);
pIADs->Put(CComBSTR("vin"), var);
pIADs->SetInfo();

if(pIADs)
    pIADs->Release();

VariantClear(&var);
```



 

 
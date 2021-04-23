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
# <a name="adding-an-auxiliary-class-to-an-object-instance"></a><span data-ttu-id="c20c2-103">Добавление вспомогательного класса к экземпляру объекта</span><span class="sxs-lookup"><span data-stu-id="c20c2-103">Adding an Auxiliary Class to an Object Instance</span></span>

<span data-ttu-id="c20c2-104">В следующем примере кода показано, как использовать ADSI и LDAP для динамического добавления вспомогательного класса к существующему экземпляру объекта.</span><span class="sxs-lookup"><span data-stu-id="c20c2-104">The following code examples show how to use ADSI and LDAP to dynamically add an auxiliary class to an existing object instance.</span></span> <span data-ttu-id="c20c2-105">В примерах предполагается, что вспомогательный класс с именем **Vehicle** определен в схеме Active Directory и что класс **ТС** имеет атрибут **VIN** .</span><span class="sxs-lookup"><span data-stu-id="c20c2-105">The examples assume that an auxiliary class named **vehicle** is defined in the Active Directory schema, and that the **vehicle** class has a **vin** attribute.</span></span>

<span data-ttu-id="c20c2-106">При динамическом добавлении вспомогательного класса к экземпляру объекта необходимо одновременно указать значения для всех обязательных атрибутов **муссаве** в классе.</span><span class="sxs-lookup"><span data-stu-id="c20c2-106">When you dynamically add an auxiliary class to an object instance, you must simultaneously specify values for any mandatory **mustHave** attributes in the class.</span></span> <span data-ttu-id="c20c2-107">В следующих примерах показано, как это сделать с помощью атрибута "Vin", который должен быть обязательным.</span><span class="sxs-lookup"><span data-stu-id="c20c2-107">The following examples show how to do this with the "vin" attribute, which is assumed to be mandatory.</span></span>

<span data-ttu-id="c20c2-108">Следующий пример C++ привязывает к объекту и использует метод [**iAds. путекс**](/windows/desktop/api/iads/nf-iads-iads-putex) для добавления вспомогательного класса к списку классов в свойстве **objectClass** объекта.</span><span class="sxs-lookup"><span data-stu-id="c20c2-108">The following C++ example binds to an object, and uses [**IADs.PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) to append the auxiliary class to the list of classes in the object's **objectClass** property.</span></span> <span data-ttu-id="c20c2-109">Затем в примере используется метод [**iAds.**](/windows/desktop/api/iads/nf-iads-iads-put) Set, чтобы задать значение атрибута **VIN** .</span><span class="sxs-lookup"><span data-stu-id="c20c2-109">Then the example uses [**IADs.Put**](/windows/desktop/api/iads/nf-iads-iads-put) to set the value of the **vin** attribute.</span></span> <span data-ttu-id="c20c2-110">Наконец, он вызывает функцию [**iAds. сетинфо**](/windows/desktop/api/iads/nf-iads-iads-setinfo) для фиксации изменений в каталоге.</span><span class="sxs-lookup"><span data-stu-id="c20c2-110">Finally, it calls [**IADs.SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) to commit the changes to the directory.</span></span>


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



 

 
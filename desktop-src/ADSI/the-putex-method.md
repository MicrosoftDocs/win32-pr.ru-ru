---
title: Метод Путекс
description: Метод IADs Путекс использует имя свойства для сохранения свойства с одним или несколькими значениями в кэше свойств.
ms.assetid: fb9a0610-e955-424b-a2b9-da4986d0ba5f
ms.tgt_platform: multiple
keywords:
- Путекс ADSI, сведения
- ADSI ADSI, пример кода Visual Basic, использование метода Путекс
- свойства ADSI, сохранение одного или нескольких значений свойства в кэше свойств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ea698c2dd14f3ddf8f3ad97459fad598006db22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887476"
---
# <a name="the-putex-method"></a><span data-ttu-id="23997-106">Метод Путекс</span><span class="sxs-lookup"><span data-stu-id="23997-106">The PutEx Method</span></span>

<span data-ttu-id="23997-107">Метод [**iAds::P утекс**](/windows/desktop/api/Iads/nf-iads-iads-putex) использует имя свойства для сохранения свойства с одним или несколькими значениями в кэше свойств.</span><span class="sxs-lookup"><span data-stu-id="23997-107">The [**IADs::PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) method uses the name of a property to save a property with single or multiple values into the property cache.</span></span> <span data-ttu-id="23997-108">Это перезаписывает все значения, находящиеся в кэше свойств.</span><span class="sxs-lookup"><span data-stu-id="23997-108">This overwrites any value currently in the property cache.</span></span> <span data-ttu-id="23997-109">Значения в кэше не записываются в базовую службу каталогов до тех пор, пока не будет вызвано значение [**iAds:: сетинфо**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) .</span><span class="sxs-lookup"><span data-stu-id="23997-109">The values in the cache are not written to the underlying directory service until an [**IADs::SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) occurs.</span></span> <span data-ttu-id="23997-110">Первый аргумент **путекс** указывает, нужно ли заменить или добавить к любому существующему значению для свойства.</span><span class="sxs-lookup"><span data-stu-id="23997-110">The first argument of **PutEx** indicates whether you want to replace or add to any existing values for the property.</span></span> <span data-ttu-id="23997-111">В следующем примере любые существующие значения атрибута **Description** удаляются в кэше при вызове **путекс** и удаляются на сервере при вызове **сетинфо** .</span><span class="sxs-lookup"><span data-stu-id="23997-111">In the following example, any existing values of the **description** attribute are erased in the cache when **PutEx** is called, and erased on the server when **SetInfo** is called.</span></span>


```VB
Dim x As IADs
Set x = GetObject("LDAP://CN=Administrator,CN=Users,DC=Fabrikam,DC=com")
'----------------------------------------------
' Assume the otherHomePhoneNumber has the following values:
' 111-1111, 222-2222
'----------------------------------------------
x.PutEx ADS_PROPERTY_APPEND, "OtherhomePhone", Array("333-3333" )  
x.SetInfo              'Now the values are 111-1111,222-222,333-3333.
 
x.PutEx ADS_PROPERTY_DELETE, "OtherHomePhone", Array("111-1111", "222-2222")
x.SetInfo              'Now the values are 333-3333.
x.PutEx ADS_PROPERTY_UPDATE, "OtherHomePhone", Array("888-8888", "999-9999")
x.SetInfo              'Now the values are 888-8888,999-9999.
x.PutEx ADS_PROPERTY_CLEAR, "OtherHomePhone",  vbNull
x.SetInfo              'Now the property has no value.
```



 

 





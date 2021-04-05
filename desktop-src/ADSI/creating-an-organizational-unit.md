---
title: Создание подразделения
description: Теперь, когда у вас есть объект Domain, можно приступить к созданию подразделений.
ms.assetid: c9955b44-5ca1-4b4b-85c8-e0d55a4304ca
ms.tgt_platform: multiple
keywords:
- Создание подразделения ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78ec0da1efe78d54eba8bc0dc05a998717aaf91f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986111"
---
# <a name="creating-an-organizational-unit"></a><span data-ttu-id="5ec77-104">Создание подразделения</span><span class="sxs-lookup"><span data-stu-id="5ec77-104">Creating an Organizational Unit</span></span>

<span data-ttu-id="5ec77-105">Теперь, когда у вас есть объект Domain, можно приступить к созданию подразделений.</span><span class="sxs-lookup"><span data-stu-id="5ec77-105">Now that you have the domain object, you can start creating organizational units.</span></span> <span data-ttu-id="5ec77-106">Fabrikam имеет два подразделения: Sales и Production.</span><span class="sxs-lookup"><span data-stu-id="5ec77-106">Fabrikam has two divisions: Sales and Production.</span></span> <span data-ttu-id="5ec77-107">Компания планирует нанять двух администраторов Windows 2000 для управления каждым подразделением.</span><span class="sxs-lookup"><span data-stu-id="5ec77-107">The company is planning to hire two Windows 2000 administrators to manage each division.</span></span> <span data-ttu-id="5ec77-108">Джо Ворден, как администратор предприятия, создаст два новых подразделения в домене Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="5ec77-108">Joe Worden, as the enterprise administrator, will create two new organizational units under the Fabrikam domain.</span></span> <span data-ttu-id="5ec77-109">Создавая подразделение, Сергей может сгруппировать несколько объектов и позволить другим управлять этими объектами.</span><span class="sxs-lookup"><span data-stu-id="5ec77-109">By creating an organizational unit, Joe can group multiple objects together and let someone else manage these objects.</span></span> <span data-ttu-id="5ec77-110">В следующем примере кода создается подразделение «продажи» (OU).</span><span class="sxs-lookup"><span data-stu-id="5ec77-110">The following code example creates the Sales Organizational Unit (OU).</span></span>


```VB
Dim dom as IADsContainer
Set dom = GetObject("LDAP://DC=Fabrikam,DC=Com")
Set salesOrg = dom.Create("organizationalUnit", "OU=Sales")
salesOrg.Put "description", "Sales Headquarter,SF"
salesOrg.Put "wwwHomePage", "https://fabrikam.com/sales"
salesOrg.SetInfo
```



<span data-ttu-id="5ec77-111">Метод [**иадсконтаинер. Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create) принимает имя класса и имя нового объекта.</span><span class="sxs-lookup"><span data-stu-id="5ec77-111">The [**IADsContainer.Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create) method accepts the class name and the name of the new object.</span></span> <span data-ttu-id="5ec77-112">На этом этапе объект не фиксируется в Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5ec77-112">At this point the object is not committed to Active Directory.</span></span> <span data-ttu-id="5ec77-113">Однако у вас будет ссылка на объект ADSI/COM на клиенте.</span><span class="sxs-lookup"><span data-stu-id="5ec77-113">You, however, will have an ADSI/COM object reference on the client.</span></span> <span data-ttu-id="5ec77-114">Этот объект ADSI позволяет задавать или изменять атрибуты с помощью метода [**iAds. поместил**](/windows/desktop/api/Iads/nf-iads-iads-put) .</span><span class="sxs-lookup"><span data-stu-id="5ec77-114">With this ADSI object, you can set or modify attributes using the [**IADs.Put**](/windows/desktop/api/Iads/nf-iads-iads-put) method.</span></span> <span data-ttu-id="5ec77-115">Метод **iAds. помещаем** принимает имя атрибута и значение атрибута.</span><span class="sxs-lookup"><span data-stu-id="5ec77-115">The **IADs.Put** method accepts the attribute name and the value of the attribute.</span></span> <span data-ttu-id="5ec77-116">По-прежнему в каталог ничего не фиксируется; все кэшируется на клиенте.</span><span class="sxs-lookup"><span data-stu-id="5ec77-116">Still, nothing is committed to the directory; everything is cached at the client.</span></span> <span data-ttu-id="5ec77-117">При вызове метода [**iAds. сетинфо**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) изменения, в данном случае, создание объектов и изменение атрибутов, фиксируются в каталоге.</span><span class="sxs-lookup"><span data-stu-id="5ec77-117">When you call the [**IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method, the changes, in this case, object creation and attribute modification, are committed to the directory.</span></span> <span data-ttu-id="5ec77-118">Эти изменения являются транзакционными, то есть вы увидите либо новый объект со всеми заданными атрибутами, либо ни один объект.</span><span class="sxs-lookup"><span data-stu-id="5ec77-118">These changes are transacted, meaning that you will see either the new object with all attributes you set, or no object at all.</span></span>

<span data-ttu-id="5ec77-119">Кроме того, можно вкладывать подразделения.</span><span class="sxs-lookup"><span data-stu-id="5ec77-119">You can also nest organizational units.</span></span> <span data-ttu-id="5ec77-120">В следующем примере кода предполагается, что Отдел продаж делится на регионы "Восток" и "Западная".</span><span class="sxs-lookup"><span data-stu-id="5ec77-120">The following code example assumes that the Sales division is divided further into the East and West regions.</span></span>


```VB
Set east = salesOrg.Create("organizationalUnit", "OU=East")
east.SetInfo
```



<span data-ttu-id="5ec77-121">Это также относится к западному региону.</span><span class="sxs-lookup"><span data-stu-id="5ec77-121">This also applies for the West region.</span></span>

<span data-ttu-id="5ec77-122">Чтобы выполнить прямую привязку к Восточной области в организации продаж, укажите различающееся имя.</span><span class="sxs-lookup"><span data-stu-id="5ec77-122">To bind directly to the East region in the Sales organization, specify the distinguished name.</span></span>


```VB
Set east = GetObject("LDAP://OU=East,OU=Sales,DC=Fabrikam,DC=COM")
Debug.Print east.Get "description"
east.Put "wwwHomePage", "https://fabrikam.com/sales/east"
```



<span data-ttu-id="5ec77-123">Если вы уже привязаны к родительскому объекту (Sales), можно выполнить привязку к дочернему объекту (восток) из родительского объекта, используя относительное имя дочернего объекта.</span><span class="sxs-lookup"><span data-stu-id="5ec77-123">If you have already bound to the parent object (Sales), you can bind to the child object (East) from the parent object using the relative name of the child object.</span></span>


```VB
Set east = salesOU.GetObject("organizationalUnit", "OU=East")
```



<span data-ttu-id="5ec77-124">Чтобы убедиться, что объекты созданы, используйте оснастку MMC "Active Directory пользователи и компьютеры" для просмотра новых подразделений.</span><span class="sxs-lookup"><span data-stu-id="5ec77-124">To ensure that the objects have been created, use the Active Directory Users and Computers MMC snap-in to view the new organizational units.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5ec77-125">См. также</span><span class="sxs-lookup"><span data-stu-id="5ec77-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ec77-126">Перемещение существующих пользователей в подразделение</span><span class="sxs-lookup"><span data-stu-id="5ec77-126">Moving Existing Users to the Organizational Unit</span></span>](moving-existing-users-to-the-organizational-unit.md)
</dt> </dl>

 

 





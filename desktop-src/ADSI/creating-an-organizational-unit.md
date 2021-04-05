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
# <a name="creating-an-organizational-unit"></a>Создание подразделения

Теперь, когда у вас есть объект Domain, можно приступить к созданию подразделений. Fabrikam имеет два подразделения: Sales и Production. Компания планирует нанять двух администраторов Windows 2000 для управления каждым подразделением. Джо Ворден, как администратор предприятия, создаст два новых подразделения в домене Fabrikam. Создавая подразделение, Сергей может сгруппировать несколько объектов и позволить другим управлять этими объектами. В следующем примере кода создается подразделение «продажи» (OU).


```VB
Dim dom as IADsContainer
Set dom = GetObject("LDAP://DC=Fabrikam,DC=Com")
Set salesOrg = dom.Create("organizationalUnit", "OU=Sales")
salesOrg.Put "description", "Sales Headquarter,SF"
salesOrg.Put "wwwHomePage", "https://fabrikam.com/sales"
salesOrg.SetInfo
```



Метод [**иадсконтаинер. Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create) принимает имя класса и имя нового объекта. На этом этапе объект не фиксируется в Active Directory. Однако у вас будет ссылка на объект ADSI/COM на клиенте. Этот объект ADSI позволяет задавать или изменять атрибуты с помощью метода [**iAds. поместил**](/windows/desktop/api/Iads/nf-iads-iads-put) . Метод **iAds. помещаем** принимает имя атрибута и значение атрибута. По-прежнему в каталог ничего не фиксируется; все кэшируется на клиенте. При вызове метода [**iAds. сетинфо**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) изменения, в данном случае, создание объектов и изменение атрибутов, фиксируются в каталоге. Эти изменения являются транзакционными, то есть вы увидите либо новый объект со всеми заданными атрибутами, либо ни один объект.

Кроме того, можно вкладывать подразделения. В следующем примере кода предполагается, что Отдел продаж делится на регионы "Восток" и "Западная".


```VB
Set east = salesOrg.Create("organizationalUnit", "OU=East")
east.SetInfo
```



Это также относится к западному региону.

Чтобы выполнить прямую привязку к Восточной области в организации продаж, укажите различающееся имя.


```VB
Set east = GetObject("LDAP://OU=East,OU=Sales,DC=Fabrikam,DC=COM")
Debug.Print east.Get "description"
east.Put "wwwHomePage", "https://fabrikam.com/sales/east"
```



Если вы уже привязаны к родительскому объекту (Sales), можно выполнить привязку к дочернему объекту (восток) из родительского объекта, используя относительное имя дочернего объекта.


```VB
Set east = salesOU.GetObject("organizationalUnit", "OU=East")
```



Чтобы убедиться, что объекты созданы, используйте оснастку MMC "Active Directory пользователи и компьютеры" для просмотра новых подразделений.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Перемещение существующих пользователей в подразделение](moving-existing-users-to-the-organizational-unit.md)
</dt> </dl>

 

 





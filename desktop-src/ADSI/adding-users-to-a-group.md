---
title: Добавление пользователей в группу
description: Джо Ворден, администратор предприятия, теперь будет добавлять Юлия Банкерт в группу управления. Чтобы добавить объект в группу, используйте метод Иадсграуп. Add.
ms.assetid: 57a9f5b2-2e48-401d-8d3b-eceb711a1df9
ms.tgt_platform: multiple
keywords:
- Добавление пользователей в группу ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ea0ac78c0175248cb12e0f47a94ae60e7f1d16c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328459"
---
# <a name="adding-users-to-a-group"></a>Добавление пользователей в группу

Джо Ворден, администратор предприятия, теперь будет добавлять Юлия Банкерт в группу управления. Чтобы добавить объект в группу, используйте метод [**иадсграуп. Add**](/windows/desktop/api/Iads/nf-iads-iadsgroup-add) .


```VB
Dim grp as IADsGroup

Set grp = GetObject("LDAP://CN=Management,OU=Sales,DC=Fabrikam,DC=COM") 
grp.Add ("LDAP://CN=Julie Bankert,OU=Sales,DC=Fabrikam,DC=COM")
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Создание новой группы](creating-a-new-group.md)
</dt> </dl>

 

 





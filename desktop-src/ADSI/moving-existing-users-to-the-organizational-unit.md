---
title: Перемещение существующих пользователей в подразделение
description: когда администратор предприятия джо ворден обновляет домен Windows NT 4,0 до Active Directory, все пользователи и группы переносятся в контейнеры пользователей в домене Fabrikam.
ms.assetid: 230a594f-70c2-4ab6-a7e8-d5a77f2d6dd1
ms.tgt_platform: multiple
keywords:
- Перемещение существующих пользователей в AD подразделений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d26104feb5d4c8b6a1f24176ce23fcbb6ef6a965ca29c58887f02724b3ccba8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118178958"
---
# <a name="moving-existing-users-to-the-organizational-unit"></a>Перемещение существующих пользователей в подразделение

когда администратор предприятия джо ворден обновляет домен Windows NT 4,0 до Active Directory, все пользователи и группы переносятся в контейнеры пользователей в домене Fabrikam. Сергей теперь может переместить этих пользователей и группы в соответствующие подразделенные подразделения. объект также можно перемещать между связанными доменами Windows 2000 с помощью ADSI.

В следующем примере кода Джо перемещает "жеффсмис" в организацию продаж.


```VB
Set usr = salesOU.MoveHere("LDAP://CN=jeffsmith,CN=Users,DC=fabrikam,DC=com", vbNullString)
```



Метод [**иадсконтаинер. мовехере**](/windows/desktop/api/Iads/nf-iads-iadscontainer-movehere) принимает путь ADsPath объекта, который необходимо переместить, и новое имя объекта (RDN). Чтобы иметь то же имя, можно указать **значение NULL** (**вбнуллстринг**) для параметра *бстрневнаме* . Чтобы переименовать объект при перемещении, укажите новое относительное различающееся имя для параметра *бстрневнаме* . Например, чтобы переместить жеффсмис в организацию продаж и переименовать объект «жеффсмис» в «Джефф \_ Иванов» в той же операции, Джо выполнит следующий код:


```VB
Set usr = salesOU.MoveHere("LDAP://CN=jeffsmith,CN=Users,DC=Fabrikam,DC=com", "CN=jeff_smith")
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Создание новых пользователей в подразделении](creating-new-users-in-the-organizational-unit.md)
</dt> </dl>

 

 





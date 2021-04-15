---
title: Делегирование организационных подразделений
description: Компания Fabrikam нанимает двух администраторов, Майк и пол, чтобы управлять подразделениями Восточной и Западной соответственно.
ms.assetid: ecf71ae6-9b6f-4e3c-878a-2c6fd193da33
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9928884c8be19f9668d6f81ed9462f6fb757286f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105654141"
---
# <a name="delegating-organizational-units"></a>Делегирование организационных подразделений

Компания Fabrikam нанимает двух администраторов, Майк и пол, чтобы управлять подразделениями Восточной и Западной соответственно. Джо делегирует ему административные обязанности, чтобы они могли создавать и удалять пользователей в соответствующих подразделениях.

Прежде чем узнать, как настроить эти подразделения в Майк и пол, необходимо понять, как настроить доступ к объектам в Active Directory. Каждый объект в Active Directory имеет дескриптор безопасности. С помощью дескриптора безопасности можно изменить разрешения на объект, распространить разрешения, включить аудит и т. д. Сам дескриптор безопасности имеет два списка управления доступом (ACL): избирательный список ACL (DACL) и системный список управления доступом (SACL). Каждый список ACL может содержать записи контроля доступа (ACE). С помощью записи ACE можно задать разрешенный или запрещенный доступ к объекту. Кроме того, можно указать определенные действия для разрешения или запрета. Примеры действий: создание дочерних элементов, удаление дочерних элементов, чтение свойства и запись свойства. Эти права указываются с помощью [**AccessMask**](iadsaccesscontrolentry-property-methods.md).

Далее можно указать классы или атрибуты, с которыми связан этот элемент управления доступом. В следующем примере Fabrikam Сергей выбирает класс пользователя, чтобы каждый администратор мог добавить пользователей в систему. Далее необходимо ответить на вопрос: "кто будет бенефициаром этого ACE?" Джо будет указывать Mike.

Наконец, можно задать поведение наследования ACE, например, можно указать ACE, чтобы распространить вниз по иерархии. В итоге, в предыдущем примере, Майк сможет создавать и удалять объекты пользователя в подразделении восточной части продаж.

Джо использует следующий пример кода для настройки элементов управления доступом и ACL в Восточной подразделении.


```VB
Set ou = GetObject("LDAP://OU=East, OU=Sales, DC=Fabrikam,DC=COM")
Set sec = ou.Get("ntSecurityDescriptor")
Set acl = sec.DiscretionaryAcl

Set ace = CreateObject("AccessControlEntry") 
' You can also use Set ace = new ADsAccessControlEntry.

' Grant access to the object.
ace.AceType = ADS_ACETYPE_ACCESS_ALLOWED_OBJECT 

' Create and delete child objects.
ace.AccessMask = ADS_RIGHT_DS_CREATE_CHILD Or ADS_RIGHT_DS_DELETE_CHILD 
' Create the user object with the user schema IDGUID.
ace.ObjectType = "{BF967ABA-0DE6-11D0-A285-00AA003049E2}" 
' Propagate the ACE down.  
ace.AceFlags = ADS_ACEFLAG_INHERIT_ACE
' Provide an option that notifies that the objectType is filled.
ace.Flags = ADS_FLAG_OBJECT_TYPE_PRESENT 
' Show the beneficiary of this ACE.
ace.Trustee = "FABRIKAM\Mike" 
acl.AddAce ace

sec.DiscretionaryAcl = acl
ou.Put "ntSecurityDescriptor", Array(sec)
' Use SetInfo to commit the data to Active Directory.
ou.SetInfo 

' Release the objects.
Set ace = Nothing
Set acl  = Nothing
Set sec = Nothing
```



На следующем рисунке показан Active Directory меню **создать новое представление** после выполнения кода. Когда Сергей, администратор, входит в систему, он видит несколько классов, которые он может создать. Однако, когда Майк входит в систему, он может только создавать объекты пользователя.

![меню параметров создания нового представления](images/adadsi5.png)

Дополнительные сведения см. в разделе [модель безопасности ADSI](adsi-security-model.md).

 

 





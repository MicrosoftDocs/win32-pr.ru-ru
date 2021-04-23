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
# <a name="delegating-organizational-units"></a><span data-ttu-id="5a328-103">Делегирование организационных подразделений</span><span class="sxs-lookup"><span data-stu-id="5a328-103">Delegating Organizational Units</span></span>

<span data-ttu-id="5a328-104">Компания Fabrikam нанимает двух администраторов, Майк и пол, чтобы управлять подразделениями Восточной и Западной соответственно.</span><span class="sxs-lookup"><span data-stu-id="5a328-104">The Fabrikam company hires two administrators, Mike and Paul, to manage the East and West organizational units, respectively.</span></span> <span data-ttu-id="5a328-105">Джо делегирует ему административные обязанности, чтобы они могли создавать и удалять пользователей в соответствующих подразделениях.</span><span class="sxs-lookup"><span data-stu-id="5a328-105">Joe delegates his administrative responsibilities to them so that they can create and delete users in their respective organizational units.</span></span>

<span data-ttu-id="5a328-106">Прежде чем узнать, как настроить эти подразделения в Майк и пол, необходимо понять, как настроить доступ к объектам в Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5a328-106">Before seeing how to set up these organizational units under Mike and Paul, you must understand how to set up access to objects in Active Directory.</span></span> <span data-ttu-id="5a328-107">Каждый объект в Active Directory имеет дескриптор безопасности.</span><span class="sxs-lookup"><span data-stu-id="5a328-107">Each object in Active Directory has a security descriptor.</span></span> <span data-ttu-id="5a328-108">С помощью дескриптора безопасности можно изменить разрешения на объект, распространить разрешения, включить аудит и т. д.</span><span class="sxs-lookup"><span data-stu-id="5a328-108">With the security descriptor, you can modify permissions on the object, propagate permissions, enable auditing, and so on.</span></span> <span data-ttu-id="5a328-109">Сам дескриптор безопасности имеет два списка управления доступом (ACL): избирательный список ACL (DACL) и системный список управления доступом (SACL).</span><span class="sxs-lookup"><span data-stu-id="5a328-109">The security descriptor itself has two access control lists (ACLs): a discretionary ACL (DACL) and a system ACL (SACL).</span></span> <span data-ttu-id="5a328-110">Каждый список ACL может содержать записи контроля доступа (ACE).</span><span class="sxs-lookup"><span data-stu-id="5a328-110">Each ACL can contain access control entries (ACEs).</span></span> <span data-ttu-id="5a328-111">С помощью записи ACE можно задать разрешенный или запрещенный доступ к объекту.</span><span class="sxs-lookup"><span data-stu-id="5a328-111">With an ACE, you can set allowed or denied access on an object.</span></span> <span data-ttu-id="5a328-112">Кроме того, можно указать определенные действия для разрешения или запрета.</span><span class="sxs-lookup"><span data-stu-id="5a328-112">In addition, you can specify specific actions to allow or deny.</span></span> <span data-ttu-id="5a328-113">Примеры действий: создание дочерних элементов, удаление дочерних элементов, чтение свойства и запись свойства.</span><span class="sxs-lookup"><span data-stu-id="5a328-113">Examples of actions include Create Child, Delete Child, Read Property, and Write Property.</span></span> <span data-ttu-id="5a328-114">Эти права указываются с помощью [**AccessMask**](iadsaccesscontrolentry-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="5a328-114">These rights are specified with the [**AccessMask**](iadsaccesscontrolentry-property-methods.md).</span></span>

<span data-ttu-id="5a328-115">Далее можно указать классы или атрибуты, с которыми связан этот элемент управления доступом.</span><span class="sxs-lookup"><span data-stu-id="5a328-115">Next, you may specify the classes or attributes to which this ACE is associated.</span></span> <span data-ttu-id="5a328-116">В следующем примере Fabrikam Сергей выбирает класс пользователя, чтобы каждый администратор мог добавить пользователей в систему.</span><span class="sxs-lookup"><span data-stu-id="5a328-116">In the Fabrikam example that follows, Joe picks the user class so that each administrator can add users to the system.</span></span> <span data-ttu-id="5a328-117">Далее необходимо ответить на вопрос: "кто будет бенефициаром этого ACE?"</span><span class="sxs-lookup"><span data-stu-id="5a328-117">Next, you must answer the question: "Who will be the beneficiary of this ACE?"</span></span> <span data-ttu-id="5a328-118">Джо будет указывать Mike.</span><span class="sxs-lookup"><span data-stu-id="5a328-118">Joe will specify Mike.</span></span>

<span data-ttu-id="5a328-119">Наконец, можно задать поведение наследования ACE, например, можно указать ACE, чтобы распространить вниз по иерархии.</span><span class="sxs-lookup"><span data-stu-id="5a328-119">Finally, you can set the ACE inheritance behavior—for example, ACEs can be specified to propagate down the hierarchy.</span></span> <span data-ttu-id="5a328-120">В итоге, в предыдущем примере, Майк сможет создавать и удалять объекты пользователя в подразделении восточной части продаж.</span><span class="sxs-lookup"><span data-stu-id="5a328-120">In summary, the previous example will result in Mike being able to create and delete user objects under the East Sales organizational unit.</span></span>

<span data-ttu-id="5a328-121">Джо использует следующий пример кода для настройки элементов управления доступом и ACL в Восточной подразделении.</span><span class="sxs-lookup"><span data-stu-id="5a328-121">Joe uses the following code example to set up the ACEs and ACLs on the East organizational unit.</span></span>


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



<span data-ttu-id="5a328-122">На следующем рисунке показан Active Directory меню **создать новое представление** после выполнения кода.</span><span class="sxs-lookup"><span data-stu-id="5a328-122">The following figure shows the Active Directory **Create New View** menu after the code runs.</span></span> <span data-ttu-id="5a328-123">Когда Сергей, администратор, входит в систему, он видит несколько классов, которые он может создать.</span><span class="sxs-lookup"><span data-stu-id="5a328-123">When Joe, the administrator, logs on, he sees several classes that he can create.</span></span> <span data-ttu-id="5a328-124">Однако, когда Майк входит в систему, он может только создавать объекты пользователя.</span><span class="sxs-lookup"><span data-stu-id="5a328-124">However, when Mike logs on, he is able only to create user objects.</span></span>

![меню параметров создания нового представления](images/adadsi5.png)

<span data-ttu-id="5a328-126">Дополнительные сведения см. в разделе [модель безопасности ADSI](adsi-security-model.md).</span><span class="sxs-lookup"><span data-stu-id="5a328-126">For more information, see [ADSI Security Model](adsi-security-model.md).</span></span>

 

 





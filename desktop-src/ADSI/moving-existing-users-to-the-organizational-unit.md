---
title: Перемещение существующих пользователей в подразделение
description: Когда администратор предприятия Джо Ворден обновляет домен Windows NT 4,0 до Active Directory, все пользователи и группы переносятся в контейнеры пользователей в домене Fabrikam.
ms.assetid: 230a594f-70c2-4ab6-a7e8-d5a77f2d6dd1
ms.tgt_platform: multiple
keywords:
- Перемещение существующих пользователей в AD подразделений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 535ff7110eaf956f108854e8442faa7386667346
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104252754"
---
# <a name="moving-existing-users-to-the-organizational-unit"></a><span data-ttu-id="19b54-104">Перемещение существующих пользователей в подразделение</span><span class="sxs-lookup"><span data-stu-id="19b54-104">Moving Existing Users to the Organizational Unit</span></span>

<span data-ttu-id="19b54-105">Когда администратор предприятия Джо Ворден обновляет домен Windows NT 4,0 до Active Directory, все пользователи и группы переносятся в контейнеры пользователей в домене Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="19b54-105">When the enterprise administrator, Joe Worden, upgrades the Windows NT 4.0 domain to Active Directory, all users and groups are migrated to the Users containers in the Fabrikam domain.</span></span> <span data-ttu-id="19b54-106">Сергей теперь может переместить этих пользователей и группы в соответствующие подразделенные подразделения.</span><span class="sxs-lookup"><span data-stu-id="19b54-106">Joe can now move those users and groups to the appropriate organizational units.</span></span> <span data-ttu-id="19b54-107">Объект также можно перемещать между связанными доменами Windows 2000 с помощью ADSI.</span><span class="sxs-lookup"><span data-stu-id="19b54-107">An object can also be moved between related Windows 2000 domains using ADSI.</span></span>

<span data-ttu-id="19b54-108">В следующем примере кода Джо перемещает "жеффсмис" в организацию продаж.</span><span class="sxs-lookup"><span data-stu-id="19b54-108">In the following code example, Joe moves "jeffsmith" to the Sales organization.</span></span>


```VB
Set usr = salesOU.MoveHere("LDAP://CN=jeffsmith,CN=Users,DC=fabrikam,DC=com", vbNullString)
```



<span data-ttu-id="19b54-109">Метод [**иадсконтаинер. мовехере**](/windows/desktop/api/Iads/nf-iads-iadscontainer-movehere) принимает путь ADsPath объекта, который необходимо переместить, и новое имя объекта (RDN).</span><span class="sxs-lookup"><span data-stu-id="19b54-109">The [**IADsContainer.MoveHere**](/windows/desktop/api/Iads/nf-iads-iadscontainer-movehere) method takes the ADsPath of the object to be moved and the new object name (RDN).</span></span> <span data-ttu-id="19b54-110">Чтобы иметь то же имя, можно указать **значение NULL** (**вбнуллстринг**) для параметра *бстрневнаме* .</span><span class="sxs-lookup"><span data-stu-id="19b54-110">To keep the same name, you can specify **NULL** (**vbNullString**) for the *bstrNewName* parameter.</span></span> <span data-ttu-id="19b54-111">Чтобы переименовать объект при перемещении, укажите новое относительное различающееся имя для параметра *бстрневнаме* .</span><span class="sxs-lookup"><span data-stu-id="19b54-111">To rename the object when it is moved, specify the new relative distinguished name for the *bstrNewName* parameter.</span></span> <span data-ttu-id="19b54-112">Например, чтобы переместить жеффсмис в организацию продаж и переименовать объект «жеффсмис» в «Джефф \_ Иванов» в той же операции, Джо выполнит следующий код:</span><span class="sxs-lookup"><span data-stu-id="19b54-112">For example, to move jeffsmith to the sales organization and rename the "jeffsmith" object to "jeff\_smith" in the same operation, Joe would execute the following code:</span></span>


```VB
Set usr = salesOU.MoveHere("LDAP://CN=jeffsmith,CN=Users,DC=Fabrikam,DC=com", "CN=jeff_smith")
```



## <a name="related-topics"></a><span data-ttu-id="19b54-113">См. также</span><span class="sxs-lookup"><span data-stu-id="19b54-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19b54-114">Создание новых пользователей в подразделении</span><span class="sxs-lookup"><span data-stu-id="19b54-114">Creating New Users in the Organizational Unit</span></span>](creating-new-users-in-the-organizational-unit.md)
</dt> </dl>

 

 





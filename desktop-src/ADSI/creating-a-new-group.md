---
title: Создание новой группы
description: Джо Ворден, администратор предприятия, должен создать новую группу.
ms.assetid: a1bea695-d43f-47e6-af74-ba5abb0116a2
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03a4f46d595aa892ac75aa67d14bbc0356122271
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103987890"
---
# <a name="creating-a-new-group"></a><span data-ttu-id="d69c9-103">Создание новой группы</span><span class="sxs-lookup"><span data-stu-id="d69c9-103">Creating a New Group</span></span>

<span data-ttu-id="d69c9-104">Джо Ворден, администратор предприятия, должен создать новую группу.</span><span class="sxs-lookup"><span data-stu-id="d69c9-104">Joe Worden, the enterprise administrator, must create a new group.</span></span> <span data-ttu-id="d69c9-105">Он хочет защитить некоторые ресурсы, такие как файлы, Active Directory объекты или другие объекты, на основе членства в этой группе.</span><span class="sxs-lookup"><span data-stu-id="d69c9-105">He would like to secure some resources, such as file, Active Directory objects, or other objects, based on the membership of this group.</span></span> <span data-ttu-id="d69c9-106">В следующем примере кода показано, как создать новую группу.</span><span class="sxs-lookup"><span data-stu-id="d69c9-106">The following code example shows how to create a new group.</span></span>


```VB
Set ou = GetObject("LDAP://OU=Sales,DC=Fabrikam,DC=COM")
Set grp = ou.Create("group", "CN=Management")
grp.Put "samAccountName", "mgmt"
grp.Put "groupType", ADS_GROUP_TYPE_DOMAIN_LOCAL_GROUP Or ADS_GROUP_TYPE_SECURITY_ENABLED
grp.SetInfo
```



<span data-ttu-id="d69c9-107">Эта группа, управление, будет создана в подразделении Sales.</span><span class="sxs-lookup"><span data-stu-id="d69c9-107">This group, Management, will be created in the Sales organizational unit.</span></span> <span data-ttu-id="d69c9-108">Во первых, Джо должен создать объект ADSI для подразделения Sales.</span><span class="sxs-lookup"><span data-stu-id="d69c9-108">First, Joe must create an ADSI object for the Sales organizational unit.</span></span> <span data-ttu-id="d69c9-109">Во-вторых, он должен установить атрибут [**SamAccountName**](/windows/desktop/AD/group-objects) для этого объекта, так как он является обязательным атрибутом для обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="d69c9-109">Second, he must set the [**samAccountName**](/windows/desktop/AD/group-objects) attribute on this object, because it is a mandatory attribute for backward compatibility.</span></span> <span data-ttu-id="d69c9-110">В этом примере, когда задан параметр **SamAccountName** , средства Windows NT 4,0, такие как диспетчер пользователей, видят атрибут в качестве **руководства** , а не **управления**.</span><span class="sxs-lookup"><span data-stu-id="d69c9-110">For this example, when **samAccountName** is set, Windows NT 4.0 tools such as User Manager see the attribute as **mgmt** instead of **Management**.</span></span>

<span data-ttu-id="d69c9-111">В третьих, Джо должен указывать тип группы.</span><span class="sxs-lookup"><span data-stu-id="d69c9-111">Third, Joe must specify the type of group.</span></span> <span data-ttu-id="d69c9-112">В домене Windows 2000 существует три типа групп: Глобальная, Доменная локальная и универсальная.</span><span class="sxs-lookup"><span data-stu-id="d69c9-112">In a Windows 2000 domain, there are three types of groups: Global, Domain Local, and Universal.</span></span> <span data-ttu-id="d69c9-113">Кроме того, группа несет свою характеристику безопасности.</span><span class="sxs-lookup"><span data-stu-id="d69c9-113">In addition, the group carries its security characteristic.</span></span> <span data-ttu-id="d69c9-114">Группа может быть группой с поддержкой безопасности или без защиты.</span><span class="sxs-lookup"><span data-stu-id="d69c9-114">A group can be either a security-enabled or a non-secured group.</span></span> <span data-ttu-id="d69c9-115">По сути, группы с поддержкой безопасности — это те, которым могут быть предоставлены или запрещены права доступа к ресурсам, аналогичные пользователю.</span><span class="sxs-lookup"><span data-stu-id="d69c9-115">Essentially, security-enabled groups are those that can be granted or denied access rights to resources, similar to a user.</span></span> <span data-ttu-id="d69c9-116">Например, предоставление группе доступа к общей папке предполагает, что все члены группы имеют доступ к общей папке.</span><span class="sxs-lookup"><span data-stu-id="d69c9-116">Granting a group access to a file share, for example, implies that all members of the group can access the file share.</span></span> <span data-ttu-id="d69c9-117">Списки рассылки нельзя использовать аналогичным образом — вы не можете, например, предоставить список рассылки право доступа к общей папке.</span><span class="sxs-lookup"><span data-stu-id="d69c9-117">Distribution lists cannot be used in a similar manner—you cannot, for example, grant a distribution list the right to access a file share.</span></span> <span data-ttu-id="d69c9-118">Во время обновления группы Windows NT 4,0 переносятся как группы с включенной безопасностью.</span><span class="sxs-lookup"><span data-stu-id="d69c9-118">During the upgrade, Windows NT 4.0 groups are migrated as security-enabled groups.</span></span> <span data-ttu-id="d69c9-119">Незащищенные группы в Active Directory похожи на списки рассылки в Exchange.</span><span class="sxs-lookup"><span data-stu-id="d69c9-119">Non-secured groups in Active Directory are similar to distribution lists in Exchange.</span></span> <span data-ttu-id="d69c9-120">Таким образом, создание групп или списков рассылки аналогично операциям в Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="d69c9-120">Hence, creating groups or distribution lists are similar operations in Windows 2000.</span></span> <span data-ttu-id="d69c9-121">В основном режиме Windows 2000 (основной режим означает, что все контроллеры домена находятся на компьютерах под управлением Windows 2000 Server) группы могут быть вложены на любой уровень.</span><span class="sxs-lookup"><span data-stu-id="d69c9-121">In the Windows 2000 native mode (native mode means that all domain controllers in a domain are computers running Windows 2000 Server), the groups can be nested to any level.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d69c9-122">См. также</span><span class="sxs-lookup"><span data-stu-id="d69c9-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d69c9-123">Перечисление объектов</span><span class="sxs-lookup"><span data-stu-id="d69c9-123">Enumerating Objects</span></span>](enumerating-objects.md)
</dt> </dl>

 

 
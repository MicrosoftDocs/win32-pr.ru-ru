---
title: Создание групп в домене
description: Объект группы создается в службах домен Active Directory в контейнере домена, где будет содержаться новая группа.
ms.assetid: 40792878-4219-4242-8cf7-b092b28f2ff4
ms.tgt_platform: multiple
keywords:
- группы AD, создание групп в домене
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 100700b08fb82b750ee68dfed6bcb26060929e87
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104069794"
---
# <a name="creating-groups-in-a-domain"></a><span data-ttu-id="242e6-104">Создание групп в домене</span><span class="sxs-lookup"><span data-stu-id="242e6-104">Creating Groups in a Domain</span></span>

<span data-ttu-id="242e6-105">Объект группы создается в службах домен Active Directory в контейнере домена, где будет содержаться новая группа.</span><span class="sxs-lookup"><span data-stu-id="242e6-105">A group object is created in Active Directory Domain Services in the domain container where the new group will be contained.</span></span> <span data-ttu-id="242e6-106">Группы можно создавать в корне домена, в подразделении или в контейнере.</span><span class="sxs-lookup"><span data-stu-id="242e6-106">Groups can be created at the root of the domain, within an organizational unit, or within a container.</span></span> <span data-ttu-id="242e6-107">Чтобы создать объект группы, используйте метод [**иадсконтаинер:: Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) или [**Идиректорйобжект:: креатедсобжект**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) .</span><span class="sxs-lookup"><span data-stu-id="242e6-107">To create a group object, use the [**IADsContainer::Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) or the [**IDirectoryObject::CreateDSObject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) method.</span></span>

<span data-ttu-id="242e6-108">Следующие атрибуты необходимы для того, чтобы сделать объект группы юридическим группой, которую будет распознать сервер Active Directory и система безопасности Windows:</span><span class="sxs-lookup"><span data-stu-id="242e6-108">The following attributes are required to make the group object a legal group that the Active Directory server and the Windows security system will recognize:</span></span>

<dl> <dt>

<span data-ttu-id="242e6-109"><span id="cn"></span><span id="CN"></span>**CN**</span><span class="sxs-lookup"><span data-stu-id="242e6-109"><span id="cn"></span><span id="CN"></span>**cn**</span></span>
</dt> <dd>

<span data-ttu-id="242e6-110">Указывает имя объекта группы в каталоге.</span><span class="sxs-lookup"><span data-stu-id="242e6-110">Specifies the name of the group object in the directory.</span></span> <span data-ttu-id="242e6-111">Это будет относительное различающееся имя объекта в контейнере, в котором создается группа.</span><span class="sxs-lookup"><span data-stu-id="242e6-111">This will be the object's relative distinguished name within the container where the group is created.</span></span>

</dd> <dt>

<span data-ttu-id="242e6-112"><span id="groupType"></span><span id="grouptype"></span><span id="GROUPTYPE"></span>**groupType**</span><span class="sxs-lookup"><span data-stu-id="242e6-112"><span id="groupType"></span><span id="grouptype"></span><span id="GROUPTYPE"></span>**groupType**</span></span>
</dt> <dd>

<span data-ttu-id="242e6-113">Содержит целое число, указывающее тип и область действия группы.</span><span class="sxs-lookup"><span data-stu-id="242e6-113">Contains an integer that specifies the group type and scope.</span></span> <span data-ttu-id="242e6-114">Перечисление перечисления [**\_ \_ типов \_ групп ADS**](/windows/win32/api/iads/ne-iads-ads_group_type_enum) определяет возможные значения для атрибута **groupType** .</span><span class="sxs-lookup"><span data-stu-id="242e6-114">The [**ADS\_GROUP\_TYPE\_ENUM**](/windows/win32/api/iads/ne-iads-ads_group_type_enum) enumeration defines the possible values for the **groupType** attribute.</span></span>

<span data-ttu-id="242e6-115">В следующем списке определяются общие типы групп и значения для этого атрибута.</span><span class="sxs-lookup"><span data-stu-id="242e6-115">The following list defines common group types and values for this attribute.</span></span>

<dl> <dt>

<span data-ttu-id="242e6-116"><span id="Domain_Local_Distribution"></span><span id="domain_local_distribution"></span><span id="DOMAIN_LOCAL_DISTRIBUTION"></span>Локальное распределение домена</span><span class="sxs-lookup"><span data-stu-id="242e6-116"><span id="Domain_Local_Distribution"></span><span id="domain_local_distribution"></span><span id="DOMAIN_LOCAL_DISTRIBUTION"></span>Domain Local Distribution</span></span>
</dt> <dd>

<span data-ttu-id="242e6-117">**\_Тип группы \_ ADS \_ \_ Локальная \_ группа домена**</span><span class="sxs-lookup"><span data-stu-id="242e6-117">**ADS\_GROUP\_TYPE\_DOMAIN\_LOCAL\_GROUP**</span></span>

</dd> <dt>

<span data-ttu-id="242e6-118"><span id="Domain_Local_Security"></span><span id="domain_local_security"></span><span id="DOMAIN_LOCAL_SECURITY"></span>Локальная безопасность домена</span><span class="sxs-lookup"><span data-stu-id="242e6-118"><span id="Domain_Local_Security"></span><span id="domain_local_security"></span><span id="DOMAIN_LOCAL_SECURITY"></span>Domain Local Security</span></span>
</dt> <dd>

<span data-ttu-id="242e6-119">**Реклама \_ Группа \_ типов групп объявлений \_ \_ локальной \_ группы домена тип** \| **\_ \_ \_ безопасности \_ включена**</span><span class="sxs-lookup"><span data-stu-id="242e6-119">**ADS\_GROUP\_TYPE\_DOMAIN\_LOCAL\_GROUP** \| **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED**</span></span>

</dd> <dt>

<span data-ttu-id="242e6-120"><span id="Global_Distribution"></span><span id="global_distribution"></span><span id="GLOBAL_DISTRIBUTION"></span>Глобальное распределение</span><span class="sxs-lookup"><span data-stu-id="242e6-120"><span id="Global_Distribution"></span><span id="global_distribution"></span><span id="GLOBAL_DISTRIBUTION"></span>Global Distribution</span></span>
</dt> <dd>

<span data-ttu-id="242e6-121">**\_ \_ \_ Глобальная \_ группа типов ADS**</span><span class="sxs-lookup"><span data-stu-id="242e6-121">**ADS\_GROUP\_TYPE\_GLOBAL\_GROUP**</span></span>

</dd> <dt>

<span data-ttu-id="242e6-122"><span id="Global_Security"></span><span id="global_security"></span><span id="GLOBAL_SECURITY"></span>Глобальная безопасность</span><span class="sxs-lookup"><span data-stu-id="242e6-122"><span id="Global_Security"></span><span id="global_security"></span><span id="GLOBAL_SECURITY"></span>Global Security</span></span>
</dt> <dd>

<span data-ttu-id="242e6-123">**Реклама \_ Тип группы ADS \_ \_ глобальные \_ группы** \| **баннеры с \_ \_ \_ \_ включенной безопасностью**</span><span class="sxs-lookup"><span data-stu-id="242e6-123">**ADS\_GROUP\_TYPE\_GLOBAL\_GROUP** \| **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED**</span></span>

</dd> <dt>

<span data-ttu-id="242e6-124"><span id="Universal_Distribution"></span><span id="universal_distribution"></span><span id="UNIVERSAL_DISTRIBUTION"></span>Универсальное распределение</span><span class="sxs-lookup"><span data-stu-id="242e6-124"><span id="Universal_Distribution"></span><span id="universal_distribution"></span><span id="UNIVERSAL_DISTRIBUTION"></span>Universal Distribution</span></span>
</dt> <dd>

<span data-ttu-id="242e6-125">**\_ \_ \_ универсальная группа ADS Type Group \_**</span><span class="sxs-lookup"><span data-stu-id="242e6-125">**ADS\_GROUP\_TYPE\_UNIVERSAL\_GROUP**</span></span>

</dd> <dt>

<span data-ttu-id="242e6-126"><span id="Universal_Security"></span><span id="universal_security"></span><span id="UNIVERSAL_SECURITY"></span>Универсальная безопасность</span><span class="sxs-lookup"><span data-stu-id="242e6-126"><span id="Universal_Security"></span><span id="universal_security"></span><span id="UNIVERSAL_SECURITY"></span>Universal Security</span></span>
</dt> <dd>

<span data-ttu-id="242e6-127">**Реклама \_ Тип \_ группы \_ \_** \| **ADS группа AD с \_ \_ \_ \_ включенной безопасностью**</span><span class="sxs-lookup"><span data-stu-id="242e6-127">**ADS\_GROUP\_TYPE\_UNIVERSAL\_GROUP** \| **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED**</span></span>

</dd> <dt>


</dt> <dd>

</dd> </dl>

<span data-ttu-id="242e6-128">Если группа предназначена для настройки контроля доступа к объектам каталога, группа должна быть глобальной безопасностью или универсальной группой безопасности.</span><span class="sxs-lookup"><span data-stu-id="242e6-128">If the group is intended for setting access control on directory objects, the group should be a Global Security or Universal Security group.</span></span>

<span data-ttu-id="242e6-129">Имейте в виду, что универсальные группы безопасности можно создавать только в доменах Windows 2000, работающих в собственном режиме.</span><span class="sxs-lookup"><span data-stu-id="242e6-129">Be aware that Universal Security groups can only be created on Windows 2000 domains running in native mode.</span></span> <span data-ttu-id="242e6-130">Дополнительные сведения об обнаружении смешанного и собственного режимов см. [в разделе Обнаружение режима работы домена](detecting-the-operation-mode-of-a-domain.md).</span><span class="sxs-lookup"><span data-stu-id="242e6-130">For more information about detecting mixed and native mode, see [Detecting the Operation Mode of a Domain](detecting-the-operation-mode-of-a-domain.md).</span></span>

</dd> <dt>

<span data-ttu-id="242e6-131"><span id="sAMAccountName"></span><span id="samaccountname"></span><span id="SAMACCOUNTNAME"></span>**sAMAccountName**</span><span class="sxs-lookup"><span data-stu-id="242e6-131"><span id="sAMAccountName"></span><span id="samaccountname"></span><span id="SAMACCOUNTNAME"></span>**sAMAccountName**</span></span>
</dt> <dd>

<span data-ttu-id="242e6-132">Содержит строку, которая является именем, используемым для поддержки клиентов и серверов из предыдущей версии.</span><span class="sxs-lookup"><span data-stu-id="242e6-132">Contains a string that is the name used to support clients and servers from a previous version.</span></span> <span data-ttu-id="242e6-133">Для поддержки клиентов предыдущей версии Windows значение **SamAccountName** должно быть меньше 20 символов.</span><span class="sxs-lookup"><span data-stu-id="242e6-133">The **sAMAccountName** should be less than 20 characters to support clients of a previous version of Windows.</span></span>

<span data-ttu-id="242e6-134">Значение **SamAccountName** должно быть уникальным для всех объектов субъекта безопасности в домене.</span><span class="sxs-lookup"><span data-stu-id="242e6-134">The **sAMAccountName** must be unique among all security principal objects within the domain.</span></span> <span data-ttu-id="242e6-135">Для проверки уникальности **SamAccountName** в домене необходимо выполнить запрос к домену.</span><span class="sxs-lookup"><span data-stu-id="242e6-135">A query should be performed against the domain to verify that the **sAMAccountName** is unique within the domain.</span></span>

</dd> </dl>

<span data-ttu-id="242e6-136">Элементы группы можно добавить во время создания с помощью метода [**идиректорйобжект:: креатедсобжект**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) .</span><span class="sxs-lookup"><span data-stu-id="242e6-136">The members of the group can be added at creation time using the [**IDirectoryObject::CreateDSObject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) method.</span></span> <span data-ttu-id="242e6-137">При необходимости члены можно добавить в группу после создания с помощью метода [**иадсграуп:: Add**](/windows/desktop/api/iads/nf-iads-iadsgroup-add) .</span><span class="sxs-lookup"><span data-stu-id="242e6-137">Optionally, members can be added to the group after creation using the [**IADsGroup::Add**](/windows/desktop/api/iads/nf-iads-iadsgroup-add) method.</span></span> <span data-ttu-id="242e6-138">Дополнительные сведения о добавлении членов в группу см. в разделе [Добавление членов в группы в домене](adding-members-to-groups-in-a-domain.md).</span><span class="sxs-lookup"><span data-stu-id="242e6-138">For more information about adding members to a group, see [Adding Members to Groups in a Domain](adding-members-to-groups-in-a-domain.md).</span></span>

 

 
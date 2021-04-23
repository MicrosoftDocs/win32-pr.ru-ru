---
title: Защита объектов от воздействия наследуемых прав
description: Как описано в разделе наследование и делегирование администрирования, ACE можно задать для объекта контейнера, например organizationalUnit, Домаинднс, контейнера и т. д., и распространить на дочерние объекты на основе флагов ACE, установленных для этих записей ACE.
ms.assetid: 3da000dd-3a32-4294-a636-ad077e618db2
ms.tgt_platform: multiple
keywords:
- Защита объектов от воздействия наследуемых прав AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78e49991cd8a479e05b024c6ea2538783a843025
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104069757"
---
# <a name="protecting-objects-from-the-effects-of-inherited-rights"></a><span data-ttu-id="169ab-104">Защита объектов от воздействия наследуемых прав</span><span class="sxs-lookup"><span data-stu-id="169ab-104">Protecting Objects from the Effects of Inherited Rights</span></span>

<span data-ttu-id="169ab-105">Как описано в разделе [наследование и делегирование администрирования](inheritance-and-delegation-of-administration.md), ACE можно задать для объекта контейнера, например **OrganizationalUnit**, **домаинднс**, **контейнера** и т. д., и распространить на ДОчерние объекты на основе флагов ACE, установленных для этих записей ACE.</span><span class="sxs-lookup"><span data-stu-id="169ab-105">As discussed in the topic [Inheritance and Delegation of Administration](inheritance-and-delegation-of-administration.md), ACEs can be set on a container object, such as an **organizationalUnit**, **domainDNS**, **container**, and so on, and propagated to child objects based on the ACE flags set on those ACEs.</span></span>

<span data-ttu-id="169ab-106">При наличии защищенного объекта или объекта, элементы управления доступом к которым нужно явно контролировать, такие как частное подразделение или особый пользователь, можно запретить распространение элементов ACE на объект родительским контейнером или его предшественниками родительского контейнера.</span><span class="sxs-lookup"><span data-stu-id="169ab-106">If you have a secure object or an object whose ACEs you want to explicitly control, such as a private OU or a special user, you can prevent ACEs from being propagated to the object by its parent container or its parent container's predecessors.</span></span>

<span data-ttu-id="169ab-107">Используйте свойство [**иадссекуритидескриптор. Control**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) , чтобы определить, наследуются ли объекты DACL и SACL от родительского контейнера.</span><span class="sxs-lookup"><span data-stu-id="169ab-107">Use the [**IADsSecurityDescriptor.Control**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) property to control whether DACLs and SACLs are inherited by the object from its parent container.</span></span>

<span data-ttu-id="169ab-108">Свойство [**иадссекуритидескриптор. Control**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) можно использовать для защиты объекта от воздействия наследуемых ACE.</span><span class="sxs-lookup"><span data-stu-id="169ab-108">The [**IADsSecurityDescriptor.Control**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) property can be used to protect an object from the effects of inherited ACEs.</span></span> <span data-ttu-id="169ab-109">Следующие флаги контролируют управление доступом явно для объекта и запрещают пользователю изменять управление доступом к объекту, устанавливая наследуемые ACE в родительском контейнере объекта или его предшественниках родительского контейнера.</span><span class="sxs-lookup"><span data-stu-id="169ab-109">The following flags force access control to be set explicitly on the object and prevent a user from modifying access control to the object by setting inheritable ACEs on the object's parent container, or its parent container's predecessors.</span></span>



| <span data-ttu-id="169ab-110">Flag</span><span class="sxs-lookup"><span data-stu-id="169ab-110">Flag</span></span>                               | <span data-ttu-id="169ab-111">Описание</span><span class="sxs-lookup"><span data-stu-id="169ab-111">Description</span></span>                                                                                                                                                                     |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="169ab-112">**SE \_ — \_ защищенный список DACL**</span><span class="sxs-lookup"><span data-stu-id="169ab-112">**SE\_DACL\_PROTECTED**</span></span><br/> | <span data-ttu-id="169ab-113">Предотвращает применение ACE, установленных для родительского контейнера, и всех объектов, нашеуказанных над родительским контейнером в иерархии каталогов, от применения к DACL объекта.</span><span class="sxs-lookup"><span data-stu-id="169ab-113">Prevents ACEs set on the DACL of the parent container, and any objects above the parent container in the directory hierarchy, from being applied to the object DACL.</span></span><br/> |
| <span data-ttu-id="169ab-114">**\_ \_ защищенный список SACL**</span><span class="sxs-lookup"><span data-stu-id="169ab-114">**SE\_SACL\_PROTECTED**</span></span><br/> | <span data-ttu-id="169ab-115">Предотвращает применение ACE, заданных в списке SACL родительского контейнера, и всех объектов, нашеуказанных над родительским контейнером в иерархии каталогов, от применения к SACL объекта.</span><span class="sxs-lookup"><span data-stu-id="169ab-115">Prevents ACEs set on the SACL of the parent container, and any objects above the parent container in the directory hierarchy, from being applied to the object SACL.</span></span><br/> |



 

<span data-ttu-id="169ab-116">Имейте в виду, что для установки защиты списка SACL необходимо наличие флага **\_ \_ присутствие** в списке DACL, чтобы установить флажок **\_ \_ защищенный список DACL** , а для управления доступом на уровне записей **(SACL) \_ \_** — SE. **\_ \_**</span><span class="sxs-lookup"><span data-stu-id="169ab-116">Be aware that the **SE\_DACL\_PRESENT** flag must be present to set **SE\_DACL\_PROTECTED** and **SE\_SACL\_PRESENT** must be present to set **SE\_SACL\_PROTECTED**.</span></span>

 


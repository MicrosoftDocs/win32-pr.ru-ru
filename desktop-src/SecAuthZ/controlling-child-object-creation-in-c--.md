---
description: Список DACL объекта-контейнера можно использовать для управления тем, кому разрешено создавать дочерние объекты в контейнере.
ms.assetid: 95f2f058-f847-4f58-b469-090bf599ae98
title: Управление созданием дочерних объектов в C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 598b2fd9a9889fbb77d2b3a4ecd004efcd823b8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543543"
---
# <a name="controlling-child-object-creation-in-c"></a><span data-ttu-id="3f0f6-103">Управление созданием дочерних объектов в C++</span><span class="sxs-lookup"><span data-stu-id="3f0f6-103">Controlling Child Object Creation in C++</span></span>

<span data-ttu-id="3f0f6-104">Список DACL объекта-контейнера можно использовать для управления тем, кому разрешено создавать дочерние объекты в контейнере.</span><span class="sxs-lookup"><span data-stu-id="3f0f6-104">You can use the DACL of a container object to control who is allowed to create child objects within the container.</span></span> <span data-ttu-id="3f0f6-105">Это может быть важно, поскольку создатель объекта обычно назначается владельцем объекта, а владелец объекта может управлять доступом к объекту.</span><span class="sxs-lookup"><span data-stu-id="3f0f6-105">This can be important because the creator of an object is typically assigned as the object's owner, and an object's owner can control access to the object.</span></span>

<span data-ttu-id="3f0f6-106">Различные типы объектов контейнера имеют определенные права доступа, которые управляют возможностью создания дочерних объектов.</span><span class="sxs-lookup"><span data-stu-id="3f0f6-106">The various types of container objects have specific access rights that control the ability to create child objects.</span></span> <span data-ttu-id="3f0f6-107">Например, поток должен иметь \_ доступ к ключу Create, чтобы \_ \_ создать подключ в разделе реестра.</span><span class="sxs-lookup"><span data-stu-id="3f0f6-107">For example, a thread must have KEY\_CREATE\_SUB\_KEY access to a registry key to create a subkey under the key.</span></span> <span data-ttu-id="3f0f6-108">Список DACL раздела реестра может содержать ACE, которые разрешают или отклоняют это право доступа.</span><span class="sxs-lookup"><span data-stu-id="3f0f6-108">The DACL of a registry key can contain ACEs that allow or deny this access right.</span></span> <span data-ttu-id="3f0f6-109">Аналогичным образом, ФАЙЛовая система NTFS поддерживает права доступа "добавить файл" и "добавить файл" \_ \_ \_ \_ для управления возможностью создания файлов или каталогов в каталоге.</span><span class="sxs-lookup"><span data-stu-id="3f0f6-109">Similarly, NTFS supports the FILE\_ADD\_FILE and FILE\_ADD\_SUBDIRECTORY access rights for controlling the ability to create files or directories in a directory.</span></span>

<span data-ttu-id="3f0f6-110">Права на \_ \_ \_ Создание \_ дочерних объектов в ОБЪЕКТЕ службы каталогов (DS) создаются с помощью прав доступа DS.</span><span class="sxs-lookup"><span data-stu-id="3f0f6-110">The ADS\_RIGHT\_DS\_CREATE\_CHILD access right controls the creation of child objects in a directory service (DS) object.</span></span> <span data-ttu-id="3f0f6-111">Однако объекты DS могут содержать различные типы объектов, поэтому система поддерживает более детализированный контроль.</span><span class="sxs-lookup"><span data-stu-id="3f0f6-111">However, DS objects can contain different types of objects, so the system supports a finer granularity of control.</span></span> <span data-ttu-id="3f0f6-112">Для разрешения или запрета права на создание указанного типа дочернего объекта можно использовать [записи ACE для конкретного объекта](object-specific-aces.md) .</span><span class="sxs-lookup"><span data-stu-id="3f0f6-112">You can use [object-specific ACEs](object-specific-aces.md) to allow or deny the right to create a specified type of child object.</span></span> <span data-ttu-id="3f0f6-113">Можно разрешить пользователю создавать один тип дочернего объекта, не мешая пользователю создавать другие типы дочерних объектов.</span><span class="sxs-lookup"><span data-stu-id="3f0f6-113">You can allow a user to create one type of child object while preventing the user from creating other types of child objects.</span></span>

<span data-ttu-id="3f0f6-114">В следующем примере функция [**сетентриесинакл**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) используется для добавления элемента управления доступом, относящегося к объекту, к списку ACL.</span><span class="sxs-lookup"><span data-stu-id="3f0f6-114">The following example uses the [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) function to add an object-specific ACE to an ACL.</span></span> <span data-ttu-id="3f0f6-115">ACE предоставляет разрешение на создание указанного типа дочернего объекта.</span><span class="sxs-lookup"><span data-stu-id="3f0f6-115">The ACE grants permission to create a specified type of child object.</span></span> <span data-ttu-id="3f0f6-116">Член **Грфакцесспермиссионс** [**явной структуры \_ доступа**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) имеет значение ADS \_ Active Directory Right, \_ \_ \_ чтобы указать, что ACE управляет созданием дочернего объекта.</span><span class="sxs-lookup"><span data-stu-id="3f0f6-116">The **grfAccessPermissions** member of the [**EXPLICIT\_ACCESS**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) structure is set to ADS\_RIGHT\_DS\_CREATE\_CHILD to indicate that the ACE controls the child object creation.</span></span> <span data-ttu-id="3f0f6-117">Элемент **обжектспресент** в структуре [**объектов \_ и \_ идентификатора SID**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_sid) имеет значение \_ тип объекта ACE \_ \_ , указывающее, что элемент **обжекттипегуид** содержит допустимый идентификатор GUID.</span><span class="sxs-lookup"><span data-stu-id="3f0f6-117">The **ObjectsPresent** member of the [**OBJECTS\_AND\_SID**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_sid) structure is set to ACE\_OBJECT\_TYPE\_PRESENT to indicate that the **ObjectTypeGuid** member contains a valid GUID.</span></span> <span data-ttu-id="3f0f6-118">GUID определяет тип дочернего объекта, для которого управляется создание.</span><span class="sxs-lookup"><span data-stu-id="3f0f6-118">The GUID identifies a type of child object whose creation is being controlled.</span></span>

<span data-ttu-id="3f0f6-119">В следующем примере Полддакл должен быть допустимым указателем на существующую структуру [**ACL**](/windows/desktop/api/Winnt/ns-winnt-acl) .</span><span class="sxs-lookup"><span data-stu-id="3f0f6-119">In the following example, pOldDACL must be a valid pointer to an existing [**ACL**](/windows/desktop/api/Winnt/ns-winnt-acl) structure.</span></span> <span data-ttu-id="3f0f6-120">Сведения о создании структуры **ACL** для объекта см. [в разделе Создание дескриптора безопасности для нового объекта в C++](creating-a-security-descriptor-for-a-new-object-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="3f0f6-120">For information about how to create an **ACL** structure for an object, see [Creating a Security Descriptor for a New Object in C++](creating-a-security-descriptor-for-a-new-object-in-c--.md).</span></span>


```C++
DWORD dwRes;
PACL pOldDACL = NULL;
PACL pNewDACL = NULL;
GUID guidChildObjectType = GUID_NULL;   // GUID of object to control creation of
PSID pTrusteeSID = NULL;           // trustee for new ACE
EXPLICIT_ACCESS ea;
OBJECTS_AND_SID ObjectsAndSID;

// pOldDACL must be a valid pointer to an existing ACL structure.

// guidChildObjectType must be the GUID of an object type 
// that is a possible child of the object associated with pOldDACL.
 
// Initialize an OBJECTS_AND_SID structure with object type GUIDs and 
// the SID of the trustee for the new ACE. 

ZeroMemory(&ObjectsAndSID, sizeof(OBJECTS_AND_SID));
ObjectsAndSID.ObjectsPresent = ACE_OBJECT_TYPE_PRESENT;
ObjectsAndSID.ObjectTypeGuid = guidChildObjectType;
ObjectsAndSID.InheritedObjectTypeGuid  = GUID_NULL;
ObjectsAndSID.pSid = (SID *)pTrusteeSID;

// Initialize an EXPLICIT_ACCESS structure for the new ACE. 

ZeroMemory(&ea, sizeof(EXPLICIT_ACCESS));
ea.grfAccessPermissions = ADS_RIGHT_DS_CREATE_CHILD;
ea.grfAccessMode = GRANT_ACCESS;
ea.grfInheritance= NO_INHERITANCE;
ea.Trustee.TrusteeForm = TRUSTEE_IS_OBJECTS_AND_SID;
ea.Trustee.ptstrName = (LPTSTR) &ObjectsAndSID;

// Create a new ACL that merges the new ACE
// into the existing DACL.

dwRes = SetEntriesInAcl(1, &ea, pOldDACL, &pNewDACL);
```



 

 




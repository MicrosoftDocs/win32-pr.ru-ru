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
# <a name="controlling-child-object-creation-in-c"></a>Управление созданием дочерних объектов в C++

Список DACL объекта-контейнера можно использовать для управления тем, кому разрешено создавать дочерние объекты в контейнере. Это может быть важно, поскольку создатель объекта обычно назначается владельцем объекта, а владелец объекта может управлять доступом к объекту.

Различные типы объектов контейнера имеют определенные права доступа, которые управляют возможностью создания дочерних объектов. Например, поток должен иметь \_ доступ к ключу Create, чтобы \_ \_ создать подключ в разделе реестра. Список DACL раздела реестра может содержать ACE, которые разрешают или отклоняют это право доступа. Аналогичным образом, ФАЙЛовая система NTFS поддерживает права доступа "добавить файл" и "добавить файл" \_ \_ \_ \_ для управления возможностью создания файлов или каталогов в каталоге.

Права на \_ \_ \_ Создание \_ дочерних объектов в ОБЪЕКТЕ службы каталогов (DS) создаются с помощью прав доступа DS. Однако объекты DS могут содержать различные типы объектов, поэтому система поддерживает более детализированный контроль. Для разрешения или запрета права на создание указанного типа дочернего объекта можно использовать [записи ACE для конкретного объекта](object-specific-aces.md) . Можно разрешить пользователю создавать один тип дочернего объекта, не мешая пользователю создавать другие типы дочерних объектов.

В следующем примере функция [**сетентриесинакл**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) используется для добавления элемента управления доступом, относящегося к объекту, к списку ACL. ACE предоставляет разрешение на создание указанного типа дочернего объекта. Член **Грфакцесспермиссионс** [**явной структуры \_ доступа**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) имеет значение ADS \_ Active Directory Right, \_ \_ \_ чтобы указать, что ACE управляет созданием дочернего объекта. Элемент **обжектспресент** в структуре [**объектов \_ и \_ идентификатора SID**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_sid) имеет значение \_ тип объекта ACE \_ \_ , указывающее, что элемент **обжекттипегуид** содержит допустимый идентификатор GUID. GUID определяет тип дочернего объекта, для которого управляется создание.

В следующем примере Полддакл должен быть допустимым указателем на существующую структуру [**ACL**](/windows/desktop/api/Winnt/ns-winnt-acl) . Сведения о создании структуры **ACL** для объекта см. [в разделе Создание дескриптора безопасности для нового объекта в C++](creating-a-security-descriptor-for-a-new-object-in-c--.md).


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



 

 




---
description: Для объектов службы каталогов (DS) поддерживаются записи ACE для конкретного объекта. ACE для конкретного объекта содержит пару идентификаторов GUID, которые расширяют способы защиты объекта элементом управления доступом.
ms.assetid: 37d353c0-ac22-430f-b5f3-15deb69be24b
title: Записи ACE для конкретного объекта
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40760e5cd06af97e93f74c6ff8daff89cd5962f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081135"
---
# <a name="object-specific-aces"></a><span data-ttu-id="d1d1a-104">Записи ACE для конкретного объекта</span><span class="sxs-lookup"><span data-stu-id="d1d1a-104">Object-specific ACEs</span></span>

<span data-ttu-id="d1d1a-105">Для объектов службы каталогов (DS) поддерживаются [*записи ACE*](/windows/desktop/SecGloss/a-gly) для конкретного объекта.</span><span class="sxs-lookup"><span data-stu-id="d1d1a-105">Object-specific [*ACEs*](/windows/desktop/SecGloss/a-gly) are supported for directory service (DS) objects.</span></span> <span data-ttu-id="d1d1a-106">ACE для конкретного объекта содержит пару идентификаторов GUID, которые расширяют способы защиты объекта элементом управления доступом.</span><span class="sxs-lookup"><span data-stu-id="d1d1a-106">An object-specific ACE contains a pair of GUIDs that expand the ways in which the ACE can protect an object.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d1d1a-107">Идентификатор GUID</span><span class="sxs-lookup"><span data-stu-id="d1d1a-107">GUID</span></span></th>
<th><span data-ttu-id="d1d1a-108">Описание</span><span class="sxs-lookup"><span data-stu-id="d1d1a-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d1d1a-109"><strong>ObjectType</strong></span><span class="sxs-lookup"><span data-stu-id="d1d1a-109"><strong>ObjectType</strong></span></span></td>
<td><span data-ttu-id="d1d1a-110">Определяет один из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="d1d1a-110">Identifies one of the following:</span></span>
<ul>
<li><span data-ttu-id="d1d1a-111">Тип дочернего объекта.</span><span class="sxs-lookup"><span data-stu-id="d1d1a-111">A type of child object.</span></span> <span data-ttu-id="d1d1a-112">ACE определяет право на создание указанного типа дочернего объекта.</span><span class="sxs-lookup"><span data-stu-id="d1d1a-112">The ACE controls the right to create a specified type of child object.</span></span> <span data-ttu-id="d1d1a-113">Дополнительные сведения см. <a href="controlling-child-object-creation-in-c--.md">в разделе Управление созданием дочерних объектов в C++</a>.</span><span class="sxs-lookup"><span data-stu-id="d1d1a-113">For more information, see <a href="controlling-child-object-creation-in-c--.md">Controlling Child Object Creation in C++</a>.</span></span></li>
<li><span data-ttu-id="d1d1a-114">Набор свойств или свойство.</span><span class="sxs-lookup"><span data-stu-id="d1d1a-114">A property set or property.</span></span> <span data-ttu-id="d1d1a-115">ACE определяет право на чтение или запись свойства или набора свойств.</span><span class="sxs-lookup"><span data-stu-id="d1d1a-115">The ACE controls the right to read or write the property or property set.</span></span> <span data-ttu-id="d1d1a-116">Дополнительные сведения см. <a href="aces-to-control-access-to-an-object-s-properties.md">в разделе ACE для управления доступом к свойствам объекта</a>.</span><span class="sxs-lookup"><span data-stu-id="d1d1a-116">For more information, see <a href="aces-to-control-access-to-an-object-s-properties.md">ACEs to Control Access to an Object's Properties</a>.</span></span></li>
<li><span data-ttu-id="d1d1a-117">Расширенное право.</span><span class="sxs-lookup"><span data-stu-id="d1d1a-117">An extended right.</span></span> <span data-ttu-id="d1d1a-118">ACE управляет правом выполнения операции, связанной с расширенным правым элементом.</span><span class="sxs-lookup"><span data-stu-id="d1d1a-118">The ACE controls the right to perform the operation associated with the extended right.</span></span></li>
<li><span data-ttu-id="d1d1a-119">Проверенная запись.</span><span class="sxs-lookup"><span data-stu-id="d1d1a-119">A validated write.</span></span> <span data-ttu-id="d1d1a-120">ACE управляет правом выполнения определенных операций записи.</span><span class="sxs-lookup"><span data-stu-id="d1d1a-120">The ACE controls the right to perform certain write operations.</span></span> <span data-ttu-id="d1d1a-121">Эти проверенные разрешения на запись, определенные и предоставляемые в редакторе ACL, предоставляют разрешения на проверенные записи свойств, а не на непроверенные записи любого значения в свойство, предоставленное с разрешением на &quot; запись свойств &quot; .</span><span class="sxs-lookup"><span data-stu-id="d1d1a-121">These validated write permissions, defined and exposed in the ACL Editor, provide permissions for validated writes of properties rather than unchecked low-level writes of any value to a property that is granted with a &quot;write property&quot; permission.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d1d1a-122"><strong>инхеритедобжекттипе</strong></span><span class="sxs-lookup"><span data-stu-id="d1d1a-122"><strong>InheritedObjectType</strong></span></span></td>
<td><span data-ttu-id="d1d1a-123">Указывает тип дочернего объекта, который может наследовать ACE.</span><span class="sxs-lookup"><span data-stu-id="d1d1a-123">Indicates the type of child object that can inherit the ACE.</span></span> <span data-ttu-id="d1d1a-124">Наследование также управляется флагами наследования в <a href="/windows/desktop/api/Winnt/ns-winnt-ace_header"><strong>ACE_HEADER</strong></a>, а также любой защитой от наследования, размещенного в дочерних объектах.</span><span class="sxs-lookup"><span data-stu-id="d1d1a-124">Inheritance is also controlled by the inheritance flags in the <a href="/windows/desktop/api/Winnt/ns-winnt-ace_header"><strong>ACE_HEADER</strong></a>, as well as by any protection against inheritance placed on the child objects.</span></span> <span data-ttu-id="d1d1a-125">Дополнительные сведения см. в разделе <a href="ace-inheritance.md">наследование ACE</a>.</span><span class="sxs-lookup"><span data-stu-id="d1d1a-125">For more information, see <a href="ace-inheritance.md">ACE Inheritance</a>.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="d1d1a-126">Поддерживаются три типа объектов ACE для конкретного объекта.</span><span class="sxs-lookup"><span data-stu-id="d1d1a-126">Three types of object-specific ACEs are supported.</span></span>

> [!Note]  
> <span data-ttu-id="d1d1a-127">Записи ACE объекта системного оповещения в настоящее время не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="d1d1a-127">System-alarm object ACEs are not currently supported.</span></span>

 



| <span data-ttu-id="d1d1a-128">Тип</span><span class="sxs-lookup"><span data-stu-id="d1d1a-128">Type</span></span>                      | <span data-ttu-id="d1d1a-129">Описание</span><span class="sxs-lookup"><span data-stu-id="d1d1a-129">Description</span></span>                                                                                                                                                                                                                                       |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1d1a-130">ACE объекта, доступ запрещен</span><span class="sxs-lookup"><span data-stu-id="d1d1a-130">Access-denied object ACE</span></span>  | <span data-ttu-id="d1d1a-131">Используется в списке DACL для запрета доступа доверенного лица к свойству или свойству объекта или для ограничения наследования ACE указанным типом дочернего объекта.</span><span class="sxs-lookup"><span data-stu-id="d1d1a-131">Used in a DACL to deny a trustee access to a property or property set on the object, or to limit ACE inheritance to a specified type of child object.</span></span> <span data-ttu-id="d1d1a-132">Использует структуру [**ACE "запрещен доступ к \_ \_ объекту \_**](/windows/desktop/api/Winnt/ns-winnt-access_denied_object_ace) ".</span><span class="sxs-lookup"><span data-stu-id="d1d1a-132">Uses the [**ACCESS\_DENIED\_OBJECT\_ACE**](/windows/desktop/api/Winnt/ns-winnt-access_denied_object_ace) structure.</span></span>         |
| <span data-ttu-id="d1d1a-133">ACE объекта, разрешенный доступом</span><span class="sxs-lookup"><span data-stu-id="d1d1a-133">Access-allowed object ACE</span></span> | <span data-ttu-id="d1d1a-134">Используется в списке DACL для предоставления доверенному лицу доступа к свойству или свойству, заданному для объекта, или для ограничения наследования ACE указанным типом дочернего объекта.</span><span class="sxs-lookup"><span data-stu-id="d1d1a-134">Used in a DACL to allow a trustee access to a property or property set on the object, or to limit ACE inheritance to a specified type of child object.</span></span> <span data-ttu-id="d1d1a-135">Использует структуру [**\_ \_ \_ ACE Access Allowed Object**](/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace) .</span><span class="sxs-lookup"><span data-stu-id="d1d1a-135">Uses the [**ACCESS\_ALLOWED\_OBJECT\_ACE**](/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace) structure.</span></span>      |
| <span data-ttu-id="d1d1a-136">Системный аудит объектов ACE</span><span class="sxs-lookup"><span data-stu-id="d1d1a-136">System-audit object ACE</span></span>   | <span data-ttu-id="d1d1a-137">Используется в SACL для записи в журнал попыток доступа к свойству или набору свойств объекта или для ограничения наследования ACE указанным типом дочернего объекта.</span><span class="sxs-lookup"><span data-stu-id="d1d1a-137">Used in a SACL to log a trustee's attempts to access a property or property set on the object, or to limit ACE inheritance to a specified type of child object.</span></span> <span data-ttu-id="d1d1a-138">Использует структуру [**\_ \_ \_ ACE объекта системного аудита**](/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace) .</span><span class="sxs-lookup"><span data-stu-id="d1d1a-138">Uses the [**SYSTEM\_AUDIT\_OBJECT\_ACE**](/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace) structure.</span></span> |



 

<span data-ttu-id="d1d1a-139">Все списки управления доступом, содержащие записи ACE для конкретного объекта, должны использовать версию ACL редакции \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="d1d1a-139">Any ACL that contains an object-specific ACE must use the revision ACL\_REVISION\_DS.</span></span>

 

 

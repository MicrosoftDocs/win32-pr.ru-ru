---
title: Установка разрешений для операций с дочерними объектами
description: Разрешения, такие как создание дочерних и удаляемых дочерних элементов, также могут быть предоставлены или запрещены для операций со всеми подобъектам или подобъектам определенного класса.
ms.assetid: fe2f8939-7562-4c03-a7a9-3ac5fc3e81bb
ms.tgt_platform: multiple
keywords:
- Настройка разрешений для операций с дочерними объектами AD
- объекты AD, Child, установка разрешений для операций с дочерними объектами
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d407e9b0db865c5df8d5dab53bd97f9f1afa1497
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104133654"
---
# <a name="setting-permissions-on-child-object-operations"></a><span data-ttu-id="68754-105">Установка разрешений для операций с дочерними объектами</span><span class="sxs-lookup"><span data-stu-id="68754-105">Setting Permissions on Child Object Operations</span></span>

<span data-ttu-id="68754-106">Разрешения, такие как создание дочерних и удаляемых дочерних элементов, также могут быть предоставлены или запрещены для операций со всеми подобъектам или подобъектам определенного класса.</span><span class="sxs-lookup"><span data-stu-id="68754-106">Permissions, such as Create Child and Delete Child, can also be granted or denied for operations on all subobjects or subobjects of a specific class.</span></span>

<span data-ttu-id="68754-107">Следующую процедуру можно использовать для задания разрешений для определенного типа подобъекта.</span><span class="sxs-lookup"><span data-stu-id="68754-107">The following procedure can be used to set permissions for a specific subobject type.</span></span>

<span data-ttu-id="68754-108">**Установка разрешений для определенного типа подобъекта**</span><span class="sxs-lookup"><span data-stu-id="68754-108">**To set permissions for a specific subobject type**</span></span>

1.  <span data-ttu-id="68754-109">Задайте для свойства [**иадсакцессконтролентри. AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) **ADS \_ AceType \_ доступ к \_ разрешенному \_ объекту** или **ADS \_ AceType \_ доступ к \_ \_ объекту**.</span><span class="sxs-lookup"><span data-stu-id="68754-109">Set the [**IADsAccessControlEntry.AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to **ADS\_ACETYPE\_ACCESS\_ALLOWED\_OBJECT** or **ADS\_ACETYPE\_ACCESS\_DENIED\_OBJECT**.</span></span>
2.  <span data-ttu-id="68754-110">Присвойте свойству [**иадсакцессконтролентри. ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) значение GUID для класса объекта.</span><span class="sxs-lookup"><span data-stu-id="68754-110">Set the [**IADsAccessControlEntry.ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to the GUID for object class.</span></span> <span data-ttu-id="68754-111">Это свойство **schemaIDGUID** объекта classSchema, определяющего класс объекта.</span><span class="sxs-lookup"><span data-stu-id="68754-111">This is the **schemaIDGUID** property of the classSchema object that defines the object class.</span></span> <span data-ttu-id="68754-112">Если свойство **ObjectType** имеет **значение NULL**, ACE применяется к подобъектам любого класса.</span><span class="sxs-lookup"><span data-stu-id="68754-112">If the **ObjectType** property is **NULL**, the ACE applies to subobjects of any class.</span></span>
3.  <span data-ttu-id="68754-113">Установите для свойства [**иадсакцессконтролентри. flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) значение **\_ \_ тип объекта \_ \_ флага ADS**.</span><span class="sxs-lookup"><span data-stu-id="68754-113">Set the [**IADsAccessControlEntry.Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to **ADS\_FLAG\_OBJECT\_TYPE\_PRESENT**.</span></span>

<span data-ttu-id="68754-114">Дополнительные сведения и процедура создания элемента управления доступом см. в разделе [Установка прав доступа для объекта](setting-access-rights-on-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="68754-114">For more information and a procedure for creating an ACE, see [Setting Access Rights on an Object](setting-access-rights-on-an-object.md).</span></span>

<span data-ttu-id="68754-115">Дополнительные сведения и пример кода, который можно использовать для задания ACE, управляющего операциями с дочерними объектами, см. в разделе [пример кода для настройки записи ACE в объекте каталога](example-code-for-setting-an-ace-on-a-directory-object.md).</span><span class="sxs-lookup"><span data-stu-id="68754-115">For more information and a code example that can be used to set an ACE that controls child object operations, see [Example Code for Setting an ACE on a Directory Object](example-code-for-setting-an-ace-on-a-directory-object.md).</span></span>

 

 
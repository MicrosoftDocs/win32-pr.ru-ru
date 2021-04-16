---
description: Запись управления доступом (ACE) — это элемент в списке управления доступом (ACL).
ms.assetid: 9cf4d796-3955-456b-9db9-ae9fa83752f6
title: Записи контроля доступа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49fe98cf1c1c4d5fb23091a6539564ff964202cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662893"
---
# <a name="access-control-entries"></a><span data-ttu-id="6e88a-103">Записи контроля доступа</span><span class="sxs-lookup"><span data-stu-id="6e88a-103">Access Control Entries</span></span>

<span data-ttu-id="6e88a-104">[*Запись управления доступом*](/windows/desktop/SecGloss/a-gly) (ACE) — это элемент в [*списке управления доступом*](/windows/desktop/SecGloss/a-gly) (ACL).</span><span class="sxs-lookup"><span data-stu-id="6e88a-104">An [*access control entry*](/windows/desktop/SecGloss/a-gly) (ACE) is an element in an [*access control list*](/windows/desktop/SecGloss/a-gly) (ACL).</span></span> <span data-ttu-id="6e88a-105">Список ACL может содержать ноль или более записей ACE.</span><span class="sxs-lookup"><span data-stu-id="6e88a-105">An ACL can have zero or more ACEs.</span></span> <span data-ttu-id="6e88a-106">Каждый элемент управления доступом или наблюдает за доступом к объекту с помощью указанного доверенного лица.</span><span class="sxs-lookup"><span data-stu-id="6e88a-106">Each ACE controls or monitors access to an object by a specified trustee.</span></span> <span data-ttu-id="6e88a-107">Дополнительные сведения о добавлении, удалении или изменении записей ACE в списках ACL объекта см. в разделе [изменение списков управления доступом объекта на языке C++](modifying-the-acls-of-an-object-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="6e88a-107">For information about adding, removing, or changing the ACEs in an object's ACLs, see [Modifying the ACLs of an Object in C++](modifying-the-acls-of-an-object-in-c--.md).</span></span>

<span data-ttu-id="6e88a-108">Существует шесть типов записей ACE, три из которых поддерживаются всеми защищаемыми объектами.</span><span class="sxs-lookup"><span data-stu-id="6e88a-108">There are six types of ACEs, three of which are supported by all securable objects.</span></span> <span data-ttu-id="6e88a-109">Другие три типа — это объекты [ACE](object-specific-aces.md) , которые поддерживаются объектами службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="6e88a-109">The other three types are [Object-specific ACEs](object-specific-aces.md) supported by directory service objects.</span></span>

<span data-ttu-id="6e88a-110">Все типы записей ACE содержат следующие сведения об управлении доступом:</span><span class="sxs-lookup"><span data-stu-id="6e88a-110">All types of ACEs contain the following access control information:</span></span>

-   <span data-ttu-id="6e88a-111">[Идентификатор безопасности](security-identifiers.md) (SID), определяющий [доверенное лицо](trustees.md) , к которому применяется ACE.</span><span class="sxs-lookup"><span data-stu-id="6e88a-111">A [security identifier](security-identifiers.md) (SID) that identifies the [trustee](trustees.md) to which the ACE applies.</span></span>
-   <span data-ttu-id="6e88a-112">[*Маска доступа*](/windows/desktop/SecGloss/a-gly) , указывающая [права доступа](access-rights-and-access-masks.md) , контролируемые элементом управления доступом.</span><span class="sxs-lookup"><span data-stu-id="6e88a-112">An [*access mask*](/windows/desktop/SecGloss/a-gly) that specifies the [access rights](access-rights-and-access-masks.md) controlled by the ACE.</span></span>
-   <span data-ttu-id="6e88a-113">Флаг, указывающий тип записи ACE.</span><span class="sxs-lookup"><span data-stu-id="6e88a-113">A flag that indicates the type of ACE.</span></span>
-   <span data-ttu-id="6e88a-114">Набор битовых флагов, который определяет, могут ли дочерние контейнеры или объекты наследовать ACE от основного объекта, к которому присоединен ACL.</span><span class="sxs-lookup"><span data-stu-id="6e88a-114">A set of bit flags that determine whether child containers or objects can inherit the ACE from the primary object to which the ACL is attached.</span></span>

<span data-ttu-id="6e88a-115">В следующей таблице перечислены три типа ACE, поддерживаемые всеми защищаемыми объектами.</span><span class="sxs-lookup"><span data-stu-id="6e88a-115">The following table lists the three ACE types supported by all securable objects.</span></span>



| <span data-ttu-id="6e88a-116">Тип</span><span class="sxs-lookup"><span data-stu-id="6e88a-116">Type</span></span>               | <span data-ttu-id="6e88a-117">Описание</span><span class="sxs-lookup"><span data-stu-id="6e88a-117">Description</span></span>                                                                                                                                                                                                                                      |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e88a-118">Запрещен доступ к ACE</span><span class="sxs-lookup"><span data-stu-id="6e88a-118">Access-denied ACE</span></span>  | <span data-ttu-id="6e88a-119">Используется в [*избирательном списке управления доступом*](/windows/desktop/SecGloss/d-gly) (DACL) для запрета прав доступа к доверенному лицу.</span><span class="sxs-lookup"><span data-stu-id="6e88a-119">Used in a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) to deny access rights to a trustee.</span></span>                                       |
| <span data-ttu-id="6e88a-120">ACE, разрешенный доступом</span><span class="sxs-lookup"><span data-stu-id="6e88a-120">Access-allowed ACE</span></span> | <span data-ttu-id="6e88a-121">Используется в списке DACL для разрешения прав доступа к доверенному лицу.</span><span class="sxs-lookup"><span data-stu-id="6e88a-121">Used in a DACL to allow access rights to a trustee.</span></span>                                                                                                                                                                                              |
| <span data-ttu-id="6e88a-122">ACE аудита системы</span><span class="sxs-lookup"><span data-stu-id="6e88a-122">System-audit ACE</span></span>   | <span data-ttu-id="6e88a-123">Используется в [*системном списке управления доступом*](/windows/desktop/SecGloss/s-gly) (SACL) для создания записи аудита, когда доверенное лицо пытается применить указанные права доступа.</span><span class="sxs-lookup"><span data-stu-id="6e88a-123">Used in a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL) to generate an audit record when the trustee attempts to exercise the specified access rights.</span></span> |



 

<span data-ttu-id="6e88a-124">Таблицу записей ACE для конкретного объекта см. в разделе [записи ACE для конкретного объекта](object-specific-aces.md).</span><span class="sxs-lookup"><span data-stu-id="6e88a-124">For a table of object-specific ACEs, see [Object-specific ACEs](object-specific-aces.md).</span></span>

> [!Note]  
> <span data-ttu-id="6e88a-125">Записи ACE объекта системного оповещения в настоящее время не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="6e88a-125">System-alarm object ACEs are not currently supported.</span></span>

 

 

 

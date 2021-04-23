---
description: Когда процесс пытается получить доступ к защищаемому объекту, система выполняет шаги по записи управления доступом (ACE) в списке управления доступом на уровне объектов (DACL) до тех пор, пока не найдет ACE, которые разрешают или отклоняют запрошенный доступ.
ms.assetid: fccf043e-e769-4f3f-b18c-252be20190d8
title: Порядок элементов ACE в списке DACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc45d6fd286bb06bd4311a8a02010c68832735ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663827"
---
# <a name="order-of-aces-in-a-dacl"></a><span data-ttu-id="5032e-103">Порядок элементов ACE в списке DACL</span><span class="sxs-lookup"><span data-stu-id="5032e-103">Order of ACEs in a DACL</span></span>

<span data-ttu-id="5032e-104">Когда [*процесс*](/windows/desktop/SecGloss/p-gly) пытается получить доступ к защищаемому объекту, система выполняет шаги по [*записи управления доступом*](/windows/desktop/SecGloss/a-gly) (ACE) в [*списке управления доступом на уровне пользователей*](/windows/desktop/SecGloss/d-gly) (DACL) объекта до тех пор, пока не найдет записи ACE, которые разрешают или отклоняют запрошенный доступ.</span><span class="sxs-lookup"><span data-stu-id="5032e-104">When a [*process*](/windows/desktop/SecGloss/p-gly) tries to access a securable object, the system steps through the [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs) in the object's [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) until it finds ACEs that allow or deny the requested access.</span></span> <span data-ttu-id="5032e-105">Права доступа, разрешенные в списке DACL, могут различаться в зависимости от порядка записей ACE в списке DACL.</span><span class="sxs-lookup"><span data-stu-id="5032e-105">The access rights that a DACL allows a user could vary depending on the order of ACEs in the DACL.</span></span> <span data-ttu-id="5032e-106">Следовательно, операционная система Windows XP определяет предпочтительный порядок записей ACE в списке DACL защищаемого объекта.</span><span class="sxs-lookup"><span data-stu-id="5032e-106">Consequently, the Windows XP operating system defines a preferred order for ACEs in the DACL of a securable object.</span></span> <span data-ttu-id="5032e-107">Предпочтительный порядок — это простая платформа, которая обеспечивает запрет доступа к ACE.</span><span class="sxs-lookup"><span data-stu-id="5032e-107">The preferred order provides a simple framework that ensures that an access-denied ACE actually denies access.</span></span> <span data-ttu-id="5032e-108">Дополнительные сведения о алгоритме системы для проверки доступа см. в статье [Управление доступом к объекту в DACL](how-dacls-control-access-to-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="5032e-108">For more information about the system's algorithm for checking access, see [How DACLs Control Access to an Object](how-dacls-control-access-to-an-object.md).</span></span>

<span data-ttu-id="5032e-109">В Windows Server 2003 и Windows XP правильный порядок записей ACE усложняется за счет введения элементов ACE для конкретного объекта и автоматического наследования.</span><span class="sxs-lookup"><span data-stu-id="5032e-109">For Windows Server 2003 and Windows XP, the proper order of ACEs is complicated by the introduction of object-specific ACEs and automatic inheritance.</span></span>

<span data-ttu-id="5032e-110">Следующие шаги описывают предпочтительный порядок.</span><span class="sxs-lookup"><span data-stu-id="5032e-110">The following steps describe the preferred order:</span></span>

1.  <span data-ttu-id="5032e-111">Все явные записи ACE помещаются в группу до наследуемых ACE.</span><span class="sxs-lookup"><span data-stu-id="5032e-111">All explicit ACEs are placed in a group before any inherited ACEs.</span></span>
2.  <span data-ttu-id="5032e-112">В группе явных ACE элементы ACE, запрещенные доступом, помещаются перед доступом к записям ACE.</span><span class="sxs-lookup"><span data-stu-id="5032e-112">Within the group of explicit ACEs, access-denied ACEs are placed before access-allowed ACEs.</span></span>
3.  <span data-ttu-id="5032e-113">Наследуемые ACE размещаются в том порядке, в котором они унаследованы.</span><span class="sxs-lookup"><span data-stu-id="5032e-113">Inherited ACEs are placed in the order in which they are inherited.</span></span> <span data-ttu-id="5032e-114">Записи ACE, унаследованные от родительского объекта, сначала берутся, затем ACE наследуются от «бабушке» и т. д. в дереве объектов.</span><span class="sxs-lookup"><span data-stu-id="5032e-114">ACEs inherited from the child object's parent come first, then ACEs inherited from the grandparent, and so on up the tree of objects.</span></span>
4.  <span data-ttu-id="5032e-115">Для каждого уровня наследуемых ACE ACE размещаются до тех пор, пока доступ к ним запрещен.</span><span class="sxs-lookup"><span data-stu-id="5032e-115">For each level of inherited ACEs, access-denied ACEs are placed before access-allowed ACEs.</span></span>

<span data-ttu-id="5032e-116">Конечно, в списке ACL требуются не все типы ACE.</span><span class="sxs-lookup"><span data-stu-id="5032e-116">Of course, not all ACE types are required in an ACL.</span></span>

<span data-ttu-id="5032e-117">Такие функции, как [**аддакцессалловедацеекс**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedaceex) и [**аддакцессалловедобжектаце**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedobjectace) , добавляют ACE в конец списка ACL.</span><span class="sxs-lookup"><span data-stu-id="5032e-117">Functions such as [**AddAccessAllowedAceEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedaceex) and [**AddAccessAllowedObjectAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedobjectace) add an ACE to the end of an ACL.</span></span> <span data-ttu-id="5032e-118">Ответственность за то, чтобы элементы ACE добавлялись в правильном порядке, отвечает вызывающему объекту.</span><span class="sxs-lookup"><span data-stu-id="5032e-118">It is the caller's responsibility to ensure that the ACEs are added in the proper order.</span></span>

 

 

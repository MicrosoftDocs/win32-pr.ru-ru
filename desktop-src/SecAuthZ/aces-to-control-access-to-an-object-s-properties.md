---
description: ACE для управления доступом к свойствам объектов
ms.assetid: 79dd4a45-c42c-4775-93ce-6e3206894d63
title: ACE для управления доступом к свойствам объектов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1068ceb994e72deedcb795586ddf712fe9c1893
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264171"
---
# <a name="aces-to-control-access-to-an-objects-properties"></a><span data-ttu-id="6042d-103">ACE для управления доступом к свойствам объекта</span><span class="sxs-lookup"><span data-stu-id="6042d-103">ACEs to Control Access to an Object's Properties</span></span>

<span data-ttu-id="6042d-104">[*Список управления доступом на уровне пользователей*](/windows/desktop/SecGloss/d-gly) (DACL) объекта службы каталогов (DS) может содержать иерархию [*записей управления доступом*](/windows/desktop/SecGloss/a-gly) (ACE), как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="6042d-104">The [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) of a directory service (DS) object can contain a hierarchy of [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs), as follows:</span></span>

1.  <span data-ttu-id="6042d-105">ACE, защищающие сам объект</span><span class="sxs-lookup"><span data-stu-id="6042d-105">ACEs that protect the object itself</span></span>
2.  <span data-ttu-id="6042d-106">[Записи ACE для конкретного объекта](object-specific-aces.md) , защищающие заданный набор свойств для объекта.</span><span class="sxs-lookup"><span data-stu-id="6042d-106">[Object-specific ACEs](object-specific-aces.md) that protect a specified property set on the object</span></span>
3.  <span data-ttu-id="6042d-107">Записи ACE для конкретного объекта, защищающие указанное свойство объекта</span><span class="sxs-lookup"><span data-stu-id="6042d-107">Object-specific ACEs that protect a specified property on the object</span></span>

<span data-ttu-id="6042d-108">В этой иерархии права, предоставленные или запрещенные на более высоком уровне, также применяются к более низким уровням.</span><span class="sxs-lookup"><span data-stu-id="6042d-108">Within this hierarchy, the rights granted or denied at a higher level apply also to the lower levels.</span></span> <span data-ttu-id="6042d-109">Например, если запись ACE, относящаяся к конкретному объекту, в наборе свойств, позволяет доверенному лицу право \_ \_ доступа DS redirectory \_ Read \_ prop, доверенное лицо имеет неявный доступ на чтение ко всем свойствам этого набора свойств.</span><span class="sxs-lookup"><span data-stu-id="6042d-109">For example, if an object-specific ACE on a property set allows a trustee the ADS\_RIGHT\_DS\_READ\_PROP right, the trustee has implicit read access to all of the properties of that property set.</span></span> <span data-ttu-id="6042d-110">Аналогичным образом запись ACE для самого объекта, позволяющая БАННЕРам \_ право доступа доступ к \_ свойству Active Directory, \_ \_ предоставляет доверенному лицу доступ на чтение ко всем свойствам объекта.</span><span class="sxs-lookup"><span data-stu-id="6042d-110">Similarly, an ACE on the object itself that allows ADS\_RIGHT\_DS\_READ\_PROP access gives the trustee read access to all of the object's properties.</span></span>

<span data-ttu-id="6042d-111">На следующем рисунке показано дерево гипотетического объекта DS и его наборов свойств и свойств.</span><span class="sxs-lookup"><span data-stu-id="6042d-111">The following illustration shows the tree of a hypothetical DS object and its property sets and properties.</span></span>

![Иерархия объектов службы каталогов](images/accctrl2.png)

<span data-ttu-id="6042d-113">Предположим, что требуется разрешить следующий доступ к свойствам этого объекта DS:</span><span class="sxs-lookup"><span data-stu-id="6042d-113">Suppose you want to allow the following access to the properties of this DS object:</span></span>

-   <span data-ttu-id="6042d-114">Разрешить группе разрешение на чтение и запись для всех свойств объекта</span><span class="sxs-lookup"><span data-stu-id="6042d-114">Allow Group A read/write permission to all of the object's properties</span></span>
-   <span data-ttu-id="6042d-115">Разрешить всем остальным разрешение на чтение и запись всем свойствам, кроме свойства D</span><span class="sxs-lookup"><span data-stu-id="6042d-115">Allow everyone else read/write permission to all properties except Property D</span></span>

<span data-ttu-id="6042d-116">Для этого установите ACE в списке DACL объекта, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="6042d-116">To do this, set the ACEs in the object's DACL as shown in the following table.</span></span>



| <span data-ttu-id="6042d-117">Доверенное лицо</span><span class="sxs-lookup"><span data-stu-id="6042d-117">Trustee</span></span>  | <span data-ttu-id="6042d-118">GUID объекта</span><span class="sxs-lookup"><span data-stu-id="6042d-118">Object GUID</span></span>    | <span data-ttu-id="6042d-119">Тип ACE</span><span class="sxs-lookup"><span data-stu-id="6042d-119">ACE type</span></span>                  | <span data-ttu-id="6042d-120">Права доступа</span><span class="sxs-lookup"><span data-stu-id="6042d-120">Access rights</span></span>                                             |
|----------|----------------|---------------------------|-----------------------------------------------------------|
| <span data-ttu-id="6042d-121">Группа A</span><span class="sxs-lookup"><span data-stu-id="6042d-121">Group A</span></span>  | <span data-ttu-id="6042d-122">Нет</span><span class="sxs-lookup"><span data-stu-id="6042d-122">None</span></span>           | <span data-ttu-id="6042d-123">ACE, разрешенный доступом</span><span class="sxs-lookup"><span data-stu-id="6042d-123">Access-allowed ACE</span></span>        | <span data-ttu-id="6042d-124">Реклама \_ справа в \_ DS \_ чтение свойства \_ \| AD \_ справа \_ DS \_ Write \_ prop</span><span class="sxs-lookup"><span data-stu-id="6042d-124">ADS\_RIGHT\_DS\_READ\_PROP \| ADS\_RIGHT\_DS\_WRITE\_PROP</span></span> |
| <span data-ttu-id="6042d-125">Все</span><span class="sxs-lookup"><span data-stu-id="6042d-125">Everyone</span></span> | <span data-ttu-id="6042d-126">Набор свойств 1</span><span class="sxs-lookup"><span data-stu-id="6042d-126">Property Set 1</span></span> | <span data-ttu-id="6042d-127">ACE объекта, разрешенный доступом</span><span class="sxs-lookup"><span data-stu-id="6042d-127">Access-allowed object ACE</span></span> | <span data-ttu-id="6042d-128">Реклама \_ справа в \_ DS \_ чтение свойства \_ \| AD \_ справа \_ DS \_ Write \_ prop</span><span class="sxs-lookup"><span data-stu-id="6042d-128">ADS\_RIGHT\_DS\_READ\_PROP \| ADS\_RIGHT\_DS\_WRITE\_PROP</span></span> |
| <span data-ttu-id="6042d-129">Все</span><span class="sxs-lookup"><span data-stu-id="6042d-129">Everyone</span></span> | <span data-ttu-id="6042d-130">Свойство C</span><span class="sxs-lookup"><span data-stu-id="6042d-130">Property C</span></span>     | <span data-ttu-id="6042d-131">ACE объекта, разрешенный доступом</span><span class="sxs-lookup"><span data-stu-id="6042d-131">Access-allowed object ACE</span></span> | <span data-ttu-id="6042d-132">Реклама \_ справа в \_ DS \_ чтение свойства \_ \| AD \_ справа \_ DS \_ Write \_ prop</span><span class="sxs-lookup"><span data-stu-id="6042d-132">ADS\_RIGHT\_DS\_READ\_PROP \| ADS\_RIGHT\_DS\_WRITE\_PROP</span></span> |



 

<span data-ttu-id="6042d-133">ACE для группы A не имеет идентификатора GUID объекта, что означает, что он разрешает доступ ко всем свойствам объекта.</span><span class="sxs-lookup"><span data-stu-id="6042d-133">The ACE for Group A does not have an object GUID, which means that it allows access to all the object's properties.</span></span> <span data-ttu-id="6042d-134">ACE конкретного объекта для набора свойств 1 позволяет любому пользователю обращаться к свойствам A и B. Другой элемент ACE, относящийся к конкретному объекту, позволяет любому пользователю обращаться к свойству C. Обратите внимание, что хотя этот список DACL не имеет записей ACE, запрещающих доступ, он неявно запрещает доступ к свойству D для всех, кроме группы A.</span><span class="sxs-lookup"><span data-stu-id="6042d-134">The object-specific ACE for Property Set 1 allows everyone access to Properties A and B. The other object-specific ACE allows everyone access to Property C. Note that although this DACL does not have any access-denied ACEs, it implicitly denies Property D access to everyone except Group A.</span></span>

<span data-ttu-id="6042d-135">Когда пользователь пытается получить доступ к свойству объекта, система проверяет ACE по порядку, пока запрошенный доступ не будет явно предоставлен, запрещен или отсутствуют другие элементы ACE. в этом случае доступ неявно отклоняется.</span><span class="sxs-lookup"><span data-stu-id="6042d-135">When a user tries to access an object's property, the system checks the ACEs, in order, until the requested access is explicitly granted, denied, or there are no more ACEs, in which case, access is implicitly denied.</span></span>

<span data-ttu-id="6042d-136">Система оценивает:</span><span class="sxs-lookup"><span data-stu-id="6042d-136">The system evaluates:</span></span>

-   <span data-ttu-id="6042d-137">ACE, которые применяются к самому объекту</span><span class="sxs-lookup"><span data-stu-id="6042d-137">ACEs that apply to the object itself</span></span>
-   <span data-ttu-id="6042d-138">Записи ACE для конкретного объекта, которые применяются к набору свойств, содержащему свойство, к которому осуществляется доступ</span><span class="sxs-lookup"><span data-stu-id="6042d-138">Object-specific ACEs that apply to the property set that contains the property being accessed</span></span>
-   <span data-ttu-id="6042d-139">Записи ACE для конкретного объекта, применимые к свойству, к которому осуществляется доступ</span><span class="sxs-lookup"><span data-stu-id="6042d-139">Object-specific ACEs that apply to the property being accessed</span></span>

<span data-ttu-id="6042d-140">Система не учитывает записи ACE для конкретного объекта, которые применяются к другим наборам свойств или свойствам.</span><span class="sxs-lookup"><span data-stu-id="6042d-140">The system ignores object-specific ACEs that apply to other property sets or properties.</span></span>

 

 

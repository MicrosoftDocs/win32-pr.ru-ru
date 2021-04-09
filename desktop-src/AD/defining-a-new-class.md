---
title: Определение нового класса
description: При определении нового класса укажите юридические родительские классы нового класса, то есть классы, которые могут содержать экземпляры нового класса.
ms.assetid: 24e346b3-2de2-41f9-a0a2-7b7d8ab5668b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 069d6c0ede945c39a00111cd43ece8257031b3aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986162"
---
# <a name="defining-a-new-class"></a><span data-ttu-id="c8d08-103">Определение нового класса</span><span class="sxs-lookup"><span data-stu-id="c8d08-103">Defining a New Class</span></span>

<span data-ttu-id="c8d08-104">При определении нового класса укажите юридические родительские классы нового класса, то есть классы, которые могут содержать экземпляры нового класса.</span><span class="sxs-lookup"><span data-stu-id="c8d08-104">When you define a new class, specify the legal parent classes of the new class, that is, the classes that can contain instances of your new class.</span></span> <span data-ttu-id="c8d08-105">Юридические родительские классы указываются в атрибутах **possSuperiors** и **системпосссупериорс** нового класса, а также в возможных старших классах, унаследованных от его классов, но не из вспомогательных классов.</span><span class="sxs-lookup"><span data-stu-id="c8d08-105">The legal parent classes are specified in the **possSuperiors** and **systemPossSuperiors** attributes of the new class, as well as in the possible superiors inherited from its superclasses, but not from auxiliary classes.</span></span>

<span data-ttu-id="c8d08-106">Будьте специфичны при определении юридических родительских классов для нового класса.</span><span class="sxs-lookup"><span data-stu-id="c8d08-106">Be specific when defining the legal parent classes for the new class.</span></span> <span data-ttu-id="c8d08-107">Определите, где пользователи должны создавать экземпляры класса.</span><span class="sxs-lookup"><span data-stu-id="c8d08-107">Decide where you want users to create instances of your class.</span></span> <span data-ttu-id="c8d08-108">Например, указание "Container" в качестве юридического родителя позволит пользователю создавать экземпляры в любом из стандартных контейнеров (**контейнер**, **OrganizationalUnit** и т. д.), при указании "Computer" создание экземпляров будет разрешено только в экземплярах объекта **Computer** .</span><span class="sxs-lookup"><span data-stu-id="c8d08-108">For example, specifying "container" as a legal parent will enable the user create instances under any of the standard containers (**container**, **organizationalUnit**, and so on), while specifying "computer" would enable instances to be created only under instances of the **computer** object.</span></span>

<span data-ttu-id="c8d08-109">**Создание класса**</span><span class="sxs-lookup"><span data-stu-id="c8d08-109">**To Create a Class**</span></span>

1.  <span data-ttu-id="c8d08-110">Выберите имя класса.</span><span class="sxs-lookup"><span data-stu-id="c8d08-110">Choose a name for the class.</span></span> <span data-ttu-id="c8d08-111">Дополнительные сведения о создании общего имени и отображаемого имени LDAP для нового класса см. в разделе [присвоение имен атрибутам и классам](naming-attributes-and-classes.md).</span><span class="sxs-lookup"><span data-stu-id="c8d08-111">For more information about composing a common-name and an LDAP display name for a new class, see [Naming Attributes and Classes](naming-attributes-and-classes.md).</span></span>
2.  <span data-ttu-id="c8d08-112">Получите идентификатор объекта (OID) для класса.</span><span class="sxs-lookup"><span data-stu-id="c8d08-112">Obtain an object identifier (OID) for the class.</span></span> <span data-ttu-id="c8d08-113">Дополнительные сведения см. в разделе [Получение идентификатора объекта](obtaining-an-object-identifier.md).</span><span class="sxs-lookup"><span data-stu-id="c8d08-113">For more information, see [Obtaining an Object Identifier](obtaining-an-object-identifier.md).</span></span>
3.  <span data-ttu-id="c8d08-114">Выберите категорию объектов по умолчанию для класса.</span><span class="sxs-lookup"><span data-stu-id="c8d08-114">Choose a "default object category" for the class.</span></span> <span data-ttu-id="c8d08-115">Дополнительные сведения см. в разделе [класс объектов и категория объектов](object-class-and-object-category.md).</span><span class="sxs-lookup"><span data-stu-id="c8d08-115">For more information, see [Object Class and Object Category](object-class-and-object-category.md).</span></span>
4.  <span data-ttu-id="c8d08-116">Выберите "Категория класса объектов" для класса.</span><span class="sxs-lookup"><span data-stu-id="c8d08-116">Choose an "object class category" for the class.</span></span> <span data-ttu-id="c8d08-117">Указывает, является ли класс абстрактным, структурным или вспомогательным.</span><span class="sxs-lookup"><span data-stu-id="c8d08-117">This indicates whether the class is abstract, structural, or auxiliary.</span></span> <span data-ttu-id="c8d08-118">Дополнительные сведения см. в разделе [структурные, абстрактные и вспомогательные классы](structural-abstract-and-auxiliary-classes.md).</span><span class="sxs-lookup"><span data-stu-id="c8d08-118">For more information, see [Structural, Abstract, and Auxiliary Classes](structural-abstract-and-auxiliary-classes.md).</span></span>
5.  <span data-ttu-id="c8d08-119">Создайте новый объект **classSchema** .</span><span class="sxs-lookup"><span data-stu-id="c8d08-119">Create a new **classSchema** object.</span></span> <span data-ttu-id="c8d08-120">Для объекта **classSchema** можно задать множество атрибутов.</span><span class="sxs-lookup"><span data-stu-id="c8d08-120">Many attributes can be set for an **classSchema** object.</span></span> <span data-ttu-id="c8d08-121">Следующие атрибуты являются критически важными для определения нового класса:</span><span class="sxs-lookup"><span data-stu-id="c8d08-121">The following attributes are critical to the definition of a new class:</span></span>

    -   <span data-ttu-id="c8d08-122">Классы, от которых наследуется новый класс: **списках subClassOf**, **auxiliaryClass** и **системауксилиарикласс**</span><span class="sxs-lookup"><span data-stu-id="c8d08-122">Classes from which the new class inherits: **subClassOf**, **auxiliaryClass**, and **systemAuxiliaryClass**</span></span>
    -   <span data-ttu-id="c8d08-123">Имена и идентификаторы для нового класса: **CN**, **lDAPDisplayName**, **админдисплайнаме**, **schemaIDGUID**, **governsID**</span><span class="sxs-lookup"><span data-stu-id="c8d08-123">Names and identifiers for the new class: **cn**, **lDAPDisplayName**, **adminDisplayName**, **schemaIDGUID**, **governsID**</span></span>
    -   <span data-ttu-id="c8d08-124">Возможные атрибуты нового класса: **mustContain**, **системмустконтаин**, **mayContain**, **системмайконтаин**</span><span class="sxs-lookup"><span data-stu-id="c8d08-124">Possible attributes of the new class: **mustContain**, **systemMustContain**, **mayContain**, **systemMayContain**</span></span>
    -   <span data-ttu-id="c8d08-125">Возможные родители нового класса: **possSuperiors**, **системпосссупериорс**</span><span class="sxs-lookup"><span data-stu-id="c8d08-125">Possible parents of the new class: **possSuperiors**, **systemPossSuperiors**</span></span>
    -   <span data-ttu-id="c8d08-126">**objectClassCategory**</span><span class="sxs-lookup"><span data-stu-id="c8d08-126">**objectClassCategory**</span></span>
    -   <span data-ttu-id="c8d08-127">**defaultObjectCategory**</span><span class="sxs-lookup"><span data-stu-id="c8d08-127">**defaultObjectCategory**</span></span>
    -   <span data-ttu-id="c8d08-128">**дефаулсидингвалуе**</span><span class="sxs-lookup"><span data-stu-id="c8d08-128">**defaultHidingValue**</span></span>
    -   <span data-ttu-id="c8d08-129">**рднаттид**</span><span class="sxs-lookup"><span data-stu-id="c8d08-129">**rDnAttId**</span></span>
    -   <span data-ttu-id="c8d08-130">**дефаултсекуритидескриптор**</span><span class="sxs-lookup"><span data-stu-id="c8d08-130">**defaultSecurityDescriptor**</span></span>
    -   <span data-ttu-id="c8d08-131">**Описание** (необязательно)</span><span class="sxs-lookup"><span data-stu-id="c8d08-131">**description** (optional)</span></span>

    <span data-ttu-id="c8d08-132">Дополнительные сведения и описания этих атрибутов см. в разделе [характеристики классов объектов](characteristics-of-object-classes.md).</span><span class="sxs-lookup"><span data-stu-id="c8d08-132">For more information, and descriptions of these attributes, see [Characteristics of Object Classes](characteristics-of-object-classes.md).</span></span>

    <span data-ttu-id="c8d08-133">Имейте в виду, что классы, указанные в **списках subClassOf**, **possSuperiors**, **системпосссупериорс**, **auxiliaryClass** и **системауксилиарикласс**, должны существовать, когда новый класс записывается в каталог. в противном случае объект **classSchema** не будет добавлен в каталог.</span><span class="sxs-lookup"><span data-stu-id="c8d08-133">Be aware that the classes specified in **subClassOf**, **possSuperiors**, **systemPossSuperiors**, **auxiliaryClass**, and **systemAuxiliaryClass**, must exist when the new class is written to the directory; otherwise, the **classSchema** object will fail to be added to the directory.</span></span> <span data-ttu-id="c8d08-134">Аналогичным образом, атрибуты, указанные в **mustContain**, **системмустконтаин**, **mayContain** и **системмайконтаин**, должны существовать, иначе операция создания класса завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="c8d08-134">Similarly, the attributes specified in **mustContain**, **systemMustContain**, **mayContain**, and **systemMayContain**, must exist or the class creation operation will fail.</span></span>

6.  <span data-ttu-id="c8d08-135">Запишите новый объект **classSchema** в каталог.</span><span class="sxs-lookup"><span data-stu-id="c8d08-135">Write the new **classSchema** object to the directory.</span></span>

<span data-ttu-id="c8d08-136">**Добавление атрибута в свойство mayContain**</span><span class="sxs-lookup"><span data-stu-id="c8d08-136">**To add an attribute to the mayContain property**</span></span>

1.  <span data-ttu-id="c8d08-137">Получите объект **classSchema** для изменяемого класса.</span><span class="sxs-lookup"><span data-stu-id="c8d08-137">Obtain the **classSchema** object for the class to modify.</span></span>
2.  <span data-ttu-id="c8d08-138">Добавьте новый атрибут в свойство **mayContain** с несколькими значениями.</span><span class="sxs-lookup"><span data-stu-id="c8d08-138">Add the new attribute to the **mayContain** multi-valued property.</span></span>
3.  <span data-ttu-id="c8d08-139">Запишите измененный объект **classSchema** обратно в каталог.</span><span class="sxs-lookup"><span data-stu-id="c8d08-139">Write the changed **classSchema** object back to the directory.</span></span>

<span data-ttu-id="c8d08-140">Новые атрибуты можно создавать одновременно с новыми классами. порядок создания новых атрибутов и классов важен.</span><span class="sxs-lookup"><span data-stu-id="c8d08-140">New attributes can be created at the same time as new classes; the order of creating the new attributes and classes is important.</span></span> <span data-ttu-id="c8d08-141">Дополнительные сведения см. [в разделе что должна делать установка](what-the-installation-must-do.md).</span><span class="sxs-lookup"><span data-stu-id="c8d08-141">For more information, see [What the Installation Must Do](what-the-installation-must-do.md).</span></span>

<span data-ttu-id="c8d08-142">**Добавление новых атрибутов и новых классов в одно и то же время**</span><span class="sxs-lookup"><span data-stu-id="c8d08-142">**To add new attributes and new classes at the same time**</span></span>

1.  <span data-ttu-id="c8d08-143">Сначала определите все новые атрибуты.</span><span class="sxs-lookup"><span data-stu-id="c8d08-143">Define all of the new attributes first.</span></span> <span data-ttu-id="c8d08-144">Дополнительные сведения см. [в разделе Определение нового атрибута](defining-a-new-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="c8d08-144">For more information, see [Defining a New Attribute](defining-a-new-attribute.md).</span></span>
2.  <span data-ttu-id="c8d08-145">Обновите кэш схемы, прежде чем определять новые классы.</span><span class="sxs-lookup"><span data-stu-id="c8d08-145">Update the Schema Cache before defining any new classes.</span></span> <span data-ttu-id="c8d08-146">Дополнительные сведения см. [в разделе Обновление кэша схемы](updating-the-schema-cache.md).</span><span class="sxs-lookup"><span data-stu-id="c8d08-146">For more information, see [Updating the Schema Cache](updating-the-schema-cache.md).</span></span>
3.  <span data-ttu-id="c8d08-147">Создайте новые классы.</span><span class="sxs-lookup"><span data-stu-id="c8d08-147">Create the new classes.</span></span>
4.  <span data-ttu-id="c8d08-148">Добавьте необходимые атрибуты в новые классы.</span><span class="sxs-lookup"><span data-stu-id="c8d08-148">Add the desired attributes to the new classes.</span></span>
5.  <span data-ttu-id="c8d08-149">Снова Обновите кэш схемы.</span><span class="sxs-lookup"><span data-stu-id="c8d08-149">Update the Schema Cache again.</span></span>

 

 





---
title: Структурные, абстрактные и вспомогательные классы
description: Атрибут objectClassCategory объекта classSchema может иметь значение, как указано в следующей таблице, которое указывает, является ли класс структурным, абстрактным или вспомогательным.
ms.assetid: 5af740cb-b292-4d80-abe5-3e3d194758f3
ms.tgt_platform: multiple
keywords:
- Структурные, абстрактные и вспомогательные классы AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 561bc836794b45b6c028fe8da772b0b38d0936a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067350"
---
# <a name="structural-abstract-and-auxiliary-classes"></a><span data-ttu-id="27d7f-104">Структурные, абстрактные и вспомогательные классы</span><span class="sxs-lookup"><span data-stu-id="27d7f-104">Structural, Abstract, and Auxiliary Classes</span></span>

<span data-ttu-id="27d7f-105">Атрибут **objectClassCategory** объекта **classSchema** может иметь значение, как указано в следующей таблице, которое указывает, является ли класс структурным, абстрактным или вспомогательным.</span><span class="sxs-lookup"><span data-stu-id="27d7f-105">The **objectClassCategory** attribute of a **classSchema** object can have a value, as listed in the following table, that indicates whether the class is structural, abstract, or auxiliary.</span></span>



| <span data-ttu-id="27d7f-106">Значение</span><span class="sxs-lookup"><span data-stu-id="27d7f-106">Value</span></span> | <span data-ttu-id="27d7f-107">Описание</span><span class="sxs-lookup"><span data-stu-id="27d7f-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27d7f-108">1</span><span class="sxs-lookup"><span data-stu-id="27d7f-108">1</span></span>     | <span data-ttu-id="27d7f-109">Структурный класс, который является единственным типом класса, который может иметь экземпляры в домен Active Directory Services.</span><span class="sxs-lookup"><span data-stu-id="27d7f-109">A structural class, which is the only type of class that can have instances in Active Directory Domain Services.</span></span> <span data-ttu-id="27d7f-110">Структурный класс может быть подклассом абстрактного или структурного класса.</span><span class="sxs-lookup"><span data-stu-id="27d7f-110">A structural class can be a subclass of an abstract or structural class.</span></span> <span data-ttu-id="27d7f-111">Структурный класс может включать любое количество вспомогательных классов в его определении.</span><span class="sxs-lookup"><span data-stu-id="27d7f-111">A structural class can include any number of auxiliary classes in its definition.</span></span>                                                                                                                                                                                                                                           |
| <span data-ttu-id="27d7f-112">2</span><span class="sxs-lookup"><span data-stu-id="27d7f-112">2</span></span>     | <span data-ttu-id="27d7f-113">Абстрактный класс, который является шаблоном, используемым для наследования новых абстрактных, вспомогательных и структурных классов.</span><span class="sxs-lookup"><span data-stu-id="27d7f-113">An abstract class, which is a template used to derive new abstract, auxiliary, and structural classes.</span></span> <span data-ttu-id="27d7f-114">Абстрактный класс может быть только подклассом абстрактного класса.</span><span class="sxs-lookup"><span data-stu-id="27d7f-114">An abstract class can only be a subclass of an abstract class.</span></span> <span data-ttu-id="27d7f-115">Не удается создать экземпляры абстрактных классов в службах домен Active Directory.</span><span class="sxs-lookup"><span data-stu-id="27d7f-115">Abstract classes cannot be instantiated in Active Directory Domain Services.</span></span> <span data-ttu-id="27d7f-116">Абстрактный класс может включать любое количество вспомогательных классов в его определении.</span><span class="sxs-lookup"><span data-stu-id="27d7f-116">An abstract class can include any number of auxiliary classes in its definition.</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="27d7f-117">3</span><span class="sxs-lookup"><span data-stu-id="27d7f-117">3</span></span>     | <span data-ttu-id="27d7f-118">Вспомогательный класс, который может быть включен в определение структурного, абстрактного или вспомогательного класса, в этом случае значения **mustContain**, **системмустконтаин**, **mayContain** и **системмайконтаин** вспомогательного класса добавляются к элементам класса.</span><span class="sxs-lookup"><span data-stu-id="27d7f-118">An auxiliary class, which can be included in the definition of a structural, abstract, or auxiliary class, in which case, the **mustContain**, **systemMustContain**, **mayContain**, and **systemMayContain** values of the auxiliary class are added to those of the class.</span></span> <span data-ttu-id="27d7f-119">Вспомогательный класс может быть подклассом абстрактного или вспомогательного класса.</span><span class="sxs-lookup"><span data-stu-id="27d7f-119">An auxiliary class can be a subclass of an abstract or auxiliary class.</span></span> <span data-ttu-id="27d7f-120">Экземпляры вспомогательных классов не могут быть созданы в службах домен Active Directory.</span><span class="sxs-lookup"><span data-stu-id="27d7f-120">Auxiliary classes cannot be instantiated in Active Directory Domain Services.</span></span> <span data-ttu-id="27d7f-121">Вспомогательный класс может включать любое количество вспомогательных классов в его определении.</span><span class="sxs-lookup"><span data-stu-id="27d7f-121">An auxiliary class can include any number of auxiliary classes in its definition.</span></span> |



 

<span data-ttu-id="27d7f-122">Не путайте **objectClassCategory** с [категорией объектов](object-class-and-object-category.md).</span><span class="sxs-lookup"><span data-stu-id="27d7f-122">Do not confuse the **objectClassCategory** with an [object category](object-class-and-object-category.md).</span></span>

 

 





---
title: Абстрактная схема
description: Контейнер схемы содержит все объекты classSchema и attributeSchema, определяющие классы и атрибуты, которые могут существовать в лесу каталога.
ms.assetid: 688fccf7-37ce-4eea-b4ff-b0b3223a964e
ms.tgt_platform: multiple
keywords:
- Абстрактная схема AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9123c72cc4cc38eafa77e0ad0c6384940667e54
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067348"
---
# <a name="the-abstract-schema"></a><span data-ttu-id="69be6-104">Абстрактная схема</span><span class="sxs-lookup"><span data-stu-id="69be6-104">The Abstract Schema</span></span>

<span data-ttu-id="69be6-105">Контейнер схемы содержит все объекты **classSchema** и **attributeSchema** , определяющие классы и атрибуты, которые могут существовать в лесу каталога.</span><span class="sxs-lookup"><span data-stu-id="69be6-105">The schema container contains all of the **classSchema** and **attributeSchema** objects that define the classes and attributes that can exist in a directory forest.</span></span> <span data-ttu-id="69be6-106">Контейнер схемы также содержит объект с именем Aggregate для **подсхемы** класса.</span><span class="sxs-lookup"><span data-stu-id="69be6-106">The schema container also contains an object named Aggregate of class **subSchema**.</span></span> <span data-ttu-id="69be6-107">Этот объект этой **подсхемы** называется абстрактной схемой.</span><span class="sxs-lookup"><span data-stu-id="69be6-107">This **subSchema** object is known as the abstract schema.</span></span>

<span data-ttu-id="69be6-108">Абстрактная схема содержит подмножество данных, хранящихся в объектах **classSchema** и **attributeSchema** .</span><span class="sxs-lookup"><span data-stu-id="69be6-108">The abstract schema contains a subset of the data stored in the **classSchema** and **attributeSchema** objects.</span></span> <span data-ttu-id="69be6-109">Его целью является предоставление простого и эффективного механизма для получения часто используемых элементов определений классов и атрибутов.</span><span class="sxs-lookup"><span data-stu-id="69be6-109">Its purpose is to provide a simple and efficient mechanism for retrieving the frequently used elements of the class and attribute definitions.</span></span> <span data-ttu-id="69be6-110">Например, чтобы получить необязательные и обязательные атрибуты класса Object, выполните привязку к нескольким объектам для получения значений **mayContain**, **mustContain**, **системмайконтаин** и **системмустконтаин** из класса и всех его классов, а также из любых вспомогательных классов класса и его классов.</span><span class="sxs-lookup"><span data-stu-id="69be6-110">For example, to retrieve the optional and mandatory attributes of an object class, bind to multiple objects to collect the **mayContain**, **mustContain**, **systemMayContain**, and **systemMustContain** values from the class and all its superclasses, as well as from any auxiliary classes of the class and its superclasses.</span></span> <span data-ttu-id="69be6-111">Абстрактная схема позволяет легко собрать все эти данные в одном объекте.</span><span class="sxs-lookup"><span data-stu-id="69be6-111">The abstract schema conveniently collects all this data in a single object.</span></span>

<span data-ttu-id="69be6-112">Как и для любого объекта в службах домен Active Directory, можно выполнить привязку к объекту **подсхемы** и прочитать его атрибуты, анализируя строковые значения для получения нужных данных.</span><span class="sxs-lookup"><span data-stu-id="69be6-112">As with any object in Active Directory Domain Services, you can bind to the **subSchema** object and read its attributes, parsing the string values to retrieve the desired data.</span></span> <span data-ttu-id="69be6-113">Однако ADSI предоставляет набор интерфейсов, которые упрощают чтение абстрактной схемы.</span><span class="sxs-lookup"><span data-stu-id="69be6-113">However, ADSI provides a set of interfaces that make it much easier to read the abstract schema.</span></span> <span data-ttu-id="69be6-114">Дополнительные сведения см. [в разделе чтение абстрактной схемы](reading-the-abstract-schema.md).</span><span class="sxs-lookup"><span data-stu-id="69be6-114">For more information, see [Reading the Abstract Schema](reading-the-abstract-schema.md).</span></span>

<span data-ttu-id="69be6-115">В следующей таблице перечислены ключевые атрибуты объекта « **подсхема** ».</span><span class="sxs-lookup"><span data-stu-id="69be6-115">The following table lists key attributes of a **subSchema** object.</span></span>



| <span data-ttu-id="69be6-116">attribute</span><span class="sxs-lookup"><span data-stu-id="69be6-116">Attribute</span></span>                 | <span data-ttu-id="69be6-117">Описание</span><span class="sxs-lookup"><span data-stu-id="69be6-117">Description</span></span>                                                                                                                                                                                                                                                                               |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69be6-118">**аттрибутетипес**</span><span class="sxs-lookup"><span data-stu-id="69be6-118">**attributeTypes**</span></span>        | <span data-ttu-id="69be6-119">Атрибут с несколькими значениями, содержащий строки, представляющие каждый атрибут в схеме.</span><span class="sxs-lookup"><span data-stu-id="69be6-119">A multi-valued attribute that contains strings that represent each attribute in the schema.</span></span> <span data-ttu-id="69be6-120">Каждое значение содержит **attributeID**, **lDAPDisplayName**, **attributeSyntax**, **ранжеловер**, **ранжеуппер** и элемент, указывающий, может ли атрибут иметь несколько значений.</span><span class="sxs-lookup"><span data-stu-id="69be6-120">Each value contains the **attributeID**, **lDAPDisplayName**, **attributeSyntax**, **rangeLower**, **rangeUpper**, and an item that indicates whether the attribute can have multiple values.</span></span> |
| <span data-ttu-id="69be6-121">**екстендедаттрибутеинфо**</span><span class="sxs-lookup"><span data-stu-id="69be6-121">**extendedAttributeInfo**</span></span> | <span data-ttu-id="69be6-122">Атрибут с несколькими значениями, содержащий строки, представляющие дополнительные данные для каждого атрибута.</span><span class="sxs-lookup"><span data-stu-id="69be6-122">A multi-valued attribute that contains strings that represent additional data for each attribute.</span></span> <span data-ttu-id="69be6-123">Каждое значение содержит **attributeID**, **lDAPDisplayName**, **schemaIDGUID** и **аттрибутесекуритигуид**.</span><span class="sxs-lookup"><span data-stu-id="69be6-123">Each value contains the **attributeID**, **lDAPDisplayName**, **schemaIDGUID**, and **attributeSecurityGUID**.</span></span>                                                                          |
| <span data-ttu-id="69be6-124">**екстендедклассинфо**</span><span class="sxs-lookup"><span data-stu-id="69be6-124">**extendedClassInfo**</span></span>     | <span data-ttu-id="69be6-125">Атрибут с несколькими значениями, содержащий строки, представляющие дополнительные данные для каждого класса.</span><span class="sxs-lookup"><span data-stu-id="69be6-125">A multi-valued attribute that contains strings that represent additional data for each class.</span></span> <span data-ttu-id="69be6-126">Каждое значение содержит **governsID**, **lDAPDisplayName** и **schemaIDGUID** класса.</span><span class="sxs-lookup"><span data-stu-id="69be6-126">Each value contains the **governsID**, **lDAPDisplayName**, and **schemaIDGUID** of the class.</span></span>                                                                                              |
| <span data-ttu-id="69be6-127">**обжектклассес**</span><span class="sxs-lookup"><span data-stu-id="69be6-127">**objectClasses**</span></span>         | <span data-ttu-id="69be6-128">Атрибут с несколькими значениями, содержащий строки, представляющие каждый класс в схеме.</span><span class="sxs-lookup"><span data-stu-id="69be6-128">A multi-valued attribute that contains strings that represent each class in the schema.</span></span> <span data-ttu-id="69be6-129">Каждое значение содержит **governsID**, **lDAPDisplayName**, **mustContain**, **mayContain** и т. д.</span><span class="sxs-lookup"><span data-stu-id="69be6-129">Each value contains the **governsID**, **lDAPDisplayName**, **mustContain**, **mayContain**, and so on.</span></span>                                                                                           |



 

 

 





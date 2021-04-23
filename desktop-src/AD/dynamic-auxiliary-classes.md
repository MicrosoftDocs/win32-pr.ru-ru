---
title: Динамические вспомогательные классы
description: Как и структурные и абстрактные классы объектов, вспомогательные классы определяются объектом classSchema в схеме Active Directory.
ms.assetid: bd5f6aed-c79a-4c03-ad03-a4ae00f0b888
ms.tgt_platform: multiple
keywords:
- Динамические вспомогательные классы Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8c13fc8231b5232b82a61b9409f1736e5bd9249
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104487452"
---
# <a name="dynamic-auxiliary-classes"></a><span data-ttu-id="b78a5-104">Динамические вспомогательные классы</span><span class="sxs-lookup"><span data-stu-id="b78a5-104">Dynamic Auxiliary Classes</span></span>

<span data-ttu-id="b78a5-105">Как и структурные и абстрактные классы объектов, вспомогательные классы определяются объектом [**classSchema**](/windows/desktop/ADSchema/c-classschema) в схеме Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b78a5-105">Similar to structural and abstract object classes, auxiliary classes are defined by a [**classSchema**](/windows/desktop/ADSchema/c-classschema) object in the Active Directory schema.</span></span> <span data-ttu-id="b78a5-106">Дополнительные сведения см. в разделе [структурные, абстрактные и вспомогательные классы](structural-abstract-and-auxiliary-classes.md).</span><span class="sxs-lookup"><span data-stu-id="b78a5-106">For more information, see [Structural, Abstract, and Auxiliary Classes](structural-abstract-and-auxiliary-classes.md).</span></span> <span data-ttu-id="b78a5-107">Это определение схемы задает различные характеристики класса, включая атрибуты, связанные с классом.</span><span class="sxs-lookup"><span data-stu-id="b78a5-107">This schema definition specifies various characteristics of the class, including the attributes associated with the class.</span></span>

<span data-ttu-id="b78a5-108">В отличие от структурных классов, нельзя создать экземпляр вспомогательного класса, как это можно сделать с помощью структурного класса.</span><span class="sxs-lookup"><span data-stu-id="b78a5-108">Unlike with structural classes, You cannot create an instance of an auxiliary class as you can with a structural class.</span></span> <span data-ttu-id="b78a5-109">Вместо этого используйте вспомогательный класс, чтобы расширить список атрибутов, связанных с другим структурным, абстрактным или вспомогательным классом объекта.</span><span class="sxs-lookup"><span data-stu-id="b78a5-109">Instead, you use an auxiliary class to extend the list of attributes that is associated with another structural, abstract, or auxiliary object class.</span></span>

<span data-ttu-id="b78a5-110">В первоначальном выпуске Windows 2000 службы домен Active Directory поддерживали статические связывание вспомогательных классов с определением [**classSchema**](/windows/desktop/ADSchema/c-classschema) другого класса объектов.</span><span class="sxs-lookup"><span data-stu-id="b78a5-110">In the initial release of Windows 2000, Active Directory Domain Services provided support for statically linking auxiliary classes to the [**classSchema**](/windows/desktop/ADSchema/c-classschema) definition of another object class.</span></span> <span data-ttu-id="b78a5-111">При использовании вспомогательного класса таким образом каждый экземпляр класса Object поддерживает атрибуты вспомогательного класса.</span><span class="sxs-lookup"><span data-stu-id="b78a5-111">When an auxiliary class is used in this way, every instance of the object class supports the attributes of the auxiliary class.</span></span>

<span data-ttu-id="b78a5-112">**Windows 2000 Server и более ранние версии:** Домен Active Directory Services не поддерживает динамическое связывание вспомогательных классов с отдельными объектами, а не только с целыми классами объектов.</span><span class="sxs-lookup"><span data-stu-id="b78a5-112">**Windows 2000 Server and earlier:** Active Directory Domain Services does not provide support for dynamically linking auxiliary classes to individual objects, and not just to entire classes of objects.</span></span> <span data-ttu-id="b78a5-113">Кроме того, вспомогательные классы, которые были присоединены к экземпляру объекта, впоследствии не могут быть удалены из экземпляра.</span><span class="sxs-lookup"><span data-stu-id="b78a5-113">In addition, auxiliary classes that have been attached to an object instance cannot subsequently be removed from the instance.</span></span>

<span data-ttu-id="b78a5-114">**Windows Server 2003:** Динамические вспомогательные классы поддерживаются, если все контроллеры домена в лесу работают под Windows Server 2003, а функциональный режим леса — Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b78a5-114">**Windows Server 2003:** Dynamic Auxiliary Classes are supported when all domain controllers in the forest are running Windows Server 2003 and the forest functional mode is Windows Server 2003.</span></span>

<span data-ttu-id="b78a5-115">Дополнительные сведения о вспомогательных классах см. в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="b78a5-115">For more information about auxiliary classes, see:</span></span>

-   [<span data-ttu-id="b78a5-116">Динамически связываемые вспомогательные классы</span><span class="sxs-lookup"><span data-stu-id="b78a5-116">Dynamically Linked Auxiliary Classes</span></span>](dynamically-linked-auxiliary-classes.md)
-   [<span data-ttu-id="b78a5-117">Статически связанные вспомогательные классы</span><span class="sxs-lookup"><span data-stu-id="b78a5-117">Statically Linked Auxiliary Classes</span></span>](statically-linked-auxiliary-classes.md)
-   [<span data-ttu-id="b78a5-118">Определение классов, связанных с экземпляром объекта</span><span class="sxs-lookup"><span data-stu-id="b78a5-118">Determining the Classes Associated With an Object Instance</span></span>](determining-the-classes-associated-with-an-object-instance.md)
-   [<span data-ttu-id="b78a5-119">Добавление вспомогательного класса к экземпляру объекта</span><span class="sxs-lookup"><span data-stu-id="b78a5-119">Adding an Auxiliary Class to an Object Instance</span></span>](adding-an-auxiliary-class-to-an-object-instance.md)

<span data-ttu-id="b78a5-120">Дополнительные сведения о режимах работы леса см. в разделе "как повысить функциональные уровни Active Directory домена и леса" в базе знаний справки и поддержки по адресу [https://support/microsoft.com/kb/322692\#4](https://support.microsoft.com/kb/322692) .</span><span class="sxs-lookup"><span data-stu-id="b78a5-120">For more information about forest functional levels, see "How to raise Active Directory domain and forest functional levels" in the Help and Support Knowledge Base at [https://support/microsoft.com/kb/322692\#4](https://support.microsoft.com/kb/322692).</span></span>

 

 
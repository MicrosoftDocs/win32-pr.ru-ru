---
description: Квалификатор — это строка данных, которая предоставляет дополнительные сведения о классе, экземпляре, свойстве, методе или параметре.
ms.assetid: 6984b575-b365-49dd-aeab-a763430f434c
ms.tgt_platform: multiple
title: Добавление квалификатора
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5a6f18f2b79bcd25b2b4ca75811157c9091e6eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693798"
---
# <a name="adding-a-qualifier"></a><span data-ttu-id="346f2-103">Добавление квалификатора</span><span class="sxs-lookup"><span data-stu-id="346f2-103">Adding a Qualifier</span></span>

<span data-ttu-id="346f2-104">Квалификатор — это строка данных, которая предоставляет дополнительные сведения о классе, экземпляре, свойстве, методе или параметре.</span><span class="sxs-lookup"><span data-stu-id="346f2-104">A qualifier is a data string that provides more information about a class, instance, property, method, or parameter.</span></span>

<span data-ttu-id="346f2-105">Следующее определение класса является примером производного класса, имеющего квалификаторы класса.</span><span class="sxs-lookup"><span data-stu-id="346f2-105">The following class definition is an example of a derived class that has class qualifiers.</span></span>

``` syntax
[Dynamic, Provider ("ProviderX")] 
class MyDerivedClass : MyClass
{
    [key] string sKey;
    [Implemented] sint32 ValueMethod();
    [Implemented] sint32 MyMethod ([in, Id(0)] sint32 Param);
};
```

<span data-ttu-id="346f2-106">Квалификаторы можно разделить на стандартные квалификаторы, квалификаторы CIM и уникальные квалификаторы:</span><span class="sxs-lookup"><span data-stu-id="346f2-106">Qualifiers can be divided into standard qualifiers, CIM qualifiers, and unique qualifiers include the following:</span></span>

-   <span data-ttu-id="346f2-107">Стандартный квалификатор</span><span class="sxs-lookup"><span data-stu-id="346f2-107">Standard qualifier</span></span>

    <span data-ttu-id="346f2-108">Стандартный квалификатор — это квалификатор, определяемый WMI и часто используемый в MOF-коде.</span><span class="sxs-lookup"><span data-stu-id="346f2-108">A standard qualifier is a qualifier defined by WMI and commonly used in MOF code.</span></span> <span data-ttu-id="346f2-109">Например, квалификаторы [**dynamic**](dynamic-qualifier.md) и [**Read**](standard-qualifiers.md) являются стандартными квалификаторами.</span><span class="sxs-lookup"><span data-stu-id="346f2-109">For example, the [**Dynamic**](dynamic-qualifier.md) and [**Read**](standard-qualifiers.md) qualifiers are both standard qualifiers.</span></span> <span data-ttu-id="346f2-110">Дополнительные сведения см. в разделе [квалификаторы WMI](wmi-qualifiers.md).</span><span class="sxs-lookup"><span data-stu-id="346f2-110">For more information, see [WMI Qualifiers](wmi-qualifiers.md).</span></span>

-   <span data-ttu-id="346f2-111">Квалификатор CIM</span><span class="sxs-lookup"><span data-stu-id="346f2-111">CIM qualifier</span></span>

    <span data-ttu-id="346f2-112">Квалификатор CIM является квалификатором, включенным в спецификацию CIM.</span><span class="sxs-lookup"><span data-stu-id="346f2-112">A CIM qualifier is a qualifier included in the CIM specification.</span></span> <span data-ttu-id="346f2-113">При использовании квалификаторов CIM в MOF-коде стандартные квалификаторы разработаны специально для инструментария WMI.</span><span class="sxs-lookup"><span data-stu-id="346f2-113">While use CIM qualifiers in MOF code, the standard qualifiers are designed specifically with WMI in mind.</span></span> <span data-ttu-id="346f2-114">Дополнительные сведения см. в [спецификации CIM](https://www.dmtf.org/spec/cims.html/)в DMTF.</span><span class="sxs-lookup"><span data-stu-id="346f2-114">For more information, see the DMTF [CIM Specification](https://www.dmtf.org/spec/cims.html/).</span></span>

-   <span data-ttu-id="346f2-115">Уникальный квалификатор</span><span class="sxs-lookup"><span data-stu-id="346f2-115">Unique qualifier</span></span>

    <span data-ttu-id="346f2-116">Уникальный квалификатор — это квалификатор, определенный специально для нового класса поставщиком класса.</span><span class="sxs-lookup"><span data-stu-id="346f2-116">A unique qualifier is a qualifier defined specifically for a new class by a class provider.</span></span> <span data-ttu-id="346f2-117">Например, квалификатор [**Units**](standard-qualifiers.md) является нестандартным квалификатором, зависящим от поставщика.</span><span class="sxs-lookup"><span data-stu-id="346f2-117">For example, the [**Units**](standard-qualifiers.md) qualifier is a nonstandard, provider-specific qualifier.</span></span> <span data-ttu-id="346f2-118">Вы можете создавать собственные квалификаторы для использования с поставщиком.</span><span class="sxs-lookup"><span data-stu-id="346f2-118">You can create your own qualifiers for use with your provider.</span></span> <span data-ttu-id="346f2-119">Дополнительные сведения о создании поставщика см. в разделе [Разработка поставщика WMI](developing-a-wmi-provider.md).</span><span class="sxs-lookup"><span data-stu-id="346f2-119">For more information about creating a provider, see [Developing a WMI Provider](developing-a-wmi-provider.md).</span></span>

<span data-ttu-id="346f2-120">Независимо от вашего квалификатора, основной процесс, который вы выполняете, заключается в использовании квалификатора в коде MOF.</span><span class="sxs-lookup"><span data-stu-id="346f2-120">Whatever your qualifier does, the main process you perform is to use the qualifier in your MOF code.</span></span> <span data-ttu-id="346f2-121">Дополнительные сведения см. [в разделе Применение квалификатора](applying-a-qualifier.md).</span><span class="sxs-lookup"><span data-stu-id="346f2-121">For more information, see [Applying a Qualifier](applying-a-qualifier.md).</span></span> <span data-ttu-id="346f2-122">Можно дополнительно описать квалификатор с разновидностью квалификатора.</span><span class="sxs-lookup"><span data-stu-id="346f2-122">You can further describe a qualifier with a qualifier flavor.</span></span> <span data-ttu-id="346f2-123">Разновидность квалификатора содержит дополнительные сведения о том, как поставщик должен использовать квалификатор.</span><span class="sxs-lookup"><span data-stu-id="346f2-123">A qualifier flavor contains more information regarding how a provider should use a qualifier.</span></span> <span data-ttu-id="346f2-124">Дополнительные сведения см. в разделе [Описание квалификатора с разновидностью квалификатора](describing-a-qualifier-with-a-qualifier-flavor.md).</span><span class="sxs-lookup"><span data-stu-id="346f2-124">For more information, see [Describing a Qualifier with a Qualifier Flavor](describing-a-qualifier-with-a-qualifier-flavor.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="346f2-125">См. также</span><span class="sxs-lookup"><span data-stu-id="346f2-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="346f2-126">Разработка классов MOF-файл (MOF)</span><span class="sxs-lookup"><span data-stu-id="346f2-126">Designing Managed Object Format (MOF) Classes</span></span>](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 




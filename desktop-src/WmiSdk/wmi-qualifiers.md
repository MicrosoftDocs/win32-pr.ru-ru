---
description: Инструментарий WMI имеет несколько типов квалификаторов класса и свойств. Квалификаторы также могут изменять разновидности.
ms.assetid: b889df69-327b-40d0-bbd7-a33d7924f3e1
ms.tgt_platform: multiple
title: Квалификаторы WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90b14dc8f1f73571fc2c449e55c30034f86c2453
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263784"
---
# <a name="wmi-qualifiers"></a><span data-ttu-id="6a4e9-104">Квалификаторы WMI</span><span class="sxs-lookup"><span data-stu-id="6a4e9-104">WMI Qualifiers</span></span>

<span data-ttu-id="6a4e9-105">Инструментарий WMI имеет несколько типов [*квалификаторов*](gloss-q.md)класса и свойств.</span><span class="sxs-lookup"><span data-stu-id="6a4e9-105">WMI has several types of class and property [*qualifiers*](gloss-q.md).</span></span> <span data-ttu-id="6a4e9-106">Квалификаторы также могут изменять [*разновидности*](gloss-f.md).</span><span class="sxs-lookup"><span data-stu-id="6a4e9-106">Qualifiers can also have modifying [*flavors*](gloss-f.md).</span></span> <span data-ttu-id="6a4e9-107">В инструментарии WMI используются следующие типы квалификаторов и разновидностей.</span><span class="sxs-lookup"><span data-stu-id="6a4e9-107">The following types of qualifiers and flavors are used in WMI.</span></span>

<span data-ttu-id="6a4e9-108">Имя каждого квалификатора отображается с типом данных и индикатор того, можно ли применить квалификатор к классу, экземпляру, свойству или методу.</span><span class="sxs-lookup"><span data-stu-id="6a4e9-108">The name of each qualifier appears with its data type and an indicator of whether the qualifier can be applied to a class, instance, property, or method.</span></span> <span data-ttu-id="6a4e9-109">Для таких квалификаторов, как **Association** (рассматривается в разделе [meta квалификаторы](meta-qualifiers.md)), существует подразумеваемое правило использования, которое также должен присутствовать квалификатор meta.</span><span class="sxs-lookup"><span data-stu-id="6a4e9-109">For qualifiers such as **Association** (discussed under [Meta Qualifiers](meta-qualifiers.md)), there is an implied usage rule that the meta qualifier must also be present.</span></span> <span data-ttu-id="6a4e9-110">Например, неявное правило использования для квалификаторов **агрегатов** заключается в том, что квалификатор **ассоциации** также должен присутствовать.</span><span class="sxs-lookup"><span data-stu-id="6a4e9-110">For example, the implicit usage rule for the **Aggregation** qualifiers is that the **Association** qualifier must also be present.</span></span>



| <span data-ttu-id="6a4e9-111">Тип квалификатора</span><span class="sxs-lookup"><span data-stu-id="6a4e9-111">Qualifier type</span></span>                              | <span data-ttu-id="6a4e9-112">Описание</span><span class="sxs-lookup"><span data-stu-id="6a4e9-112">Description</span></span>                                                                                                                           |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6a4e9-113">Метаконфигурации</span><span class="sxs-lookup"><span data-stu-id="6a4e9-113">Meta</span></span>](meta-qualifiers.md)                 | <span data-ttu-id="6a4e9-114">Уточнение определения мета-конструкций путем уточнения фактического использования объявления класса или свойства.</span><span class="sxs-lookup"><span data-stu-id="6a4e9-114">Refines the definition of meta-constructs by clarifying the actual usage of a class or property declaration.</span></span>                          |
| [<span data-ttu-id="6a4e9-115">Необязательный</span><span class="sxs-lookup"><span data-stu-id="6a4e9-115">Optional</span></span>](optional-qualifiers.md)         | <span data-ttu-id="6a4e9-116">Рассматриваются ситуации, которые не являются общими для всех реализаций, совместимых с CIM.</span><span class="sxs-lookup"><span data-stu-id="6a4e9-116">Addresses situations not common to all CIM-compliant implementations.</span></span>                                                                 |
| [<span data-ttu-id="6a4e9-117">Разновидности квалификаторов</span><span class="sxs-lookup"><span data-stu-id="6a4e9-117">Qualifier Flavors</span></span>](qualifier-flavors.md)  | <span data-ttu-id="6a4e9-118">Предоставляет дополнительные сведения об квалификаторе, например, может ли производный класс или экземпляр переопределить исходное значение квалификатора.</span><span class="sxs-lookup"><span data-stu-id="6a4e9-118">Provides more information about a qualifier, such as whether a derived class or instance can override the qualifier's original value.</span></span> |
| [<span data-ttu-id="6a4e9-119">Стандартный</span><span class="sxs-lookup"><span data-stu-id="6a4e9-119">Standard</span></span>](standard-qualifiers.md)         | <span data-ttu-id="6a4e9-120">Поддерживает описания, которые должны быть обработаны всеми CLS-совместимыми реализациями.</span><span class="sxs-lookup"><span data-stu-id="6a4e9-120">Supports the descriptions that all CIM-compliant implementations must handle.</span></span>                                                         |
| [<span data-ttu-id="6a4e9-121">Зависит от инструментария WMI</span><span class="sxs-lookup"><span data-stu-id="6a4e9-121">WMI-specific</span></span>](wmi-specific-qualifiers.md) | <span data-ttu-id="6a4e9-122">Описывает квалификаторы, относящиеся к WMI, такие как квалификаторы класса счетчика производительности.</span><span class="sxs-lookup"><span data-stu-id="6a4e9-122">Describes qualifiers specific to WMI, such as performance counter class qualifiers.</span></span>                                                   |



 

<span data-ttu-id="6a4e9-123">Дополнительные сведения о применении квалификаторов к классам WMI см. в разделе [Добавление квалификатора](adding-a-qualifier.md).</span><span class="sxs-lookup"><span data-stu-id="6a4e9-123">For more information on applying qualifiers to your WMI classes, see [Adding a Qualifier](adding-a-qualifier.md).</span></span> <span data-ttu-id="6a4e9-124">Чтобы узнать, как проверить квалификаторы существующих классов WMI, см. Приведенный ниже пример кода.</span><span class="sxs-lookup"><span data-stu-id="6a4e9-124">To see how to examine qualifiers on existing WMI classes, see the example code below.</span></span>

## <a name="example"></a><span data-ttu-id="6a4e9-125">Пример</span><span class="sxs-lookup"><span data-stu-id="6a4e9-125">Example</span></span>

<span data-ttu-id="6a4e9-126">Следующий код PowerShell, взятый из [коллекции TechNet](https://Gallery.TechNet.Microsoft.Com/Get-WMI-Class-qualifiers-239970e7), описывает, как получить квалификаторы из класса WMI.</span><span class="sxs-lookup"><span data-stu-id="6a4e9-126">The following PowerShell code, taken from the [TechNet gallery](https://Gallery.TechNet.Microsoft.Com/Get-WMI-Class-qualifiers-239970e7), describes how to retrieve qualifiers from a WMI class.</span></span>


```PowerShell
Function Get-WMIClassesWithQualifiers 
{ 
 Param([string]$qualifier = "dynamic", 
  [string]$namespace = "root\cimv2") 
 $classes = Gwmi -list -namespace $namespace 
 foreach($class in $classes) 
 { 
  $query = "select * from meta_class where __this isa ""$($class.name)"" " 
  $a = gwmi -Query $query -Namespace $namespace |  
  select -Property __class, qualifiers 
   if($a.qualifiers | % { $_ | ? { $_.name -match "$qualifier" }}) 
    { $a.__class } 
  } #end foreach $class 
} 
```



 

 




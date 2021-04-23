---
title: Зависимость конфигурации PrintCapabilities
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 9b1f3f49-2a4a-4413-9708-a430011314e6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e7f376d8bd0dab823adb3a2e0665db27508b1d7
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "103914259"
---
# <a name="configuration-dependency-in-the-printcapabilities-schema"></a><span data-ttu-id="04b22-104">Зависимость конфигурации в схеме PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="04b22-104">Configuration Dependency in the PrintCapabilities Schema</span></span>

<span data-ttu-id="04b22-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="04b22-105">This topic is not current.</span></span> <span data-ttu-id="04b22-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="04b22-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="04b22-107">Схема PrintCapabilities тесно параллельна с платформой схемы печати с точки зрения используемых элементов и общей структуры, выраженной родительскими и дочерними элементами.</span><span class="sxs-lookup"><span data-stu-id="04b22-107">The PrintCapabilities Schema closely parallels the Print Schema Framework, in terms of the elements used and the general structure expressed by parent and child elements.</span></span> <span data-ttu-id="04b22-108">Зависимости конфигурации, относящиеся к PrintCapabilities, перечислены здесь как расширение для общей инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="04b22-108">Configuration dependencies, which pertain specifically to the PrintCapabilities, are listed here as an extension to the general framework.</span></span> <span data-ttu-id="04b22-109">Зависимости конфигурации относятся к тому факту, что некоторые элементы, включая их содержимое, могут быть изменены или даже удалены из одного документа PrintCapabilities на следующий в результате зависимости от конфигурации.</span><span class="sxs-lookup"><span data-stu-id="04b22-109">Configuration dependencies refer to the fact that some elements, including their contents, can be altered or even deleted from one PrintCapabilities document to the next, as a result of dependencies on the configuration.</span></span> <span data-ttu-id="04b22-110">Даже если родительский элемент должен быть независимым от конфигурации, его дочерние элементы могут иметь зависимости.</span><span class="sxs-lookup"><span data-stu-id="04b22-110">Even if a parent element is required to be independent of the configuration, its child elements might have dependencies.</span></span> <span data-ttu-id="04b22-111">Такие зависимости выражаются с помощью \* конструкций переключения или \* вариантов в файлах ГПД.</span><span class="sxs-lookup"><span data-stu-id="04b22-111">Such dependencies are expressed using \*Switch/\*Case constructs in GPD files.</span></span>

<span data-ttu-id="04b22-112">В качестве примера зависимости конфигурации учитывайте значения, связанные с каждым свойством в документе PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="04b22-112">As an example of a configuration dependency, consider the values associated with each Property in the PrintCapabilities document.</span></span> <span data-ttu-id="04b22-113">Каждый документ PrintCapabilities может отличаться в определенных экземплярах свойств и в экземплярах значений, назначенных этим экземплярам свойств.</span><span class="sxs-lookup"><span data-stu-id="04b22-113">Each PrintCapabilities document can differ in the Property instances that are defined and in the Value instances assigned to those Property instances.</span></span>



| <span data-ttu-id="04b22-114">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="04b22-114">Element Type</span></span>                                                                                                                                                                             | <span data-ttu-id="04b22-115">Зависимость конфигурации</span><span class="sxs-lookup"><span data-stu-id="04b22-115">Configuration Dependency</span></span>                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04b22-116">Функция</span><span class="sxs-lookup"><span data-stu-id="04b22-116">Feature</span></span> <br/> <span data-ttu-id="04b22-117">Параметр</span><span class="sxs-lookup"><span data-stu-id="04b22-117">Option</span></span><br/> <span data-ttu-id="04b22-118">параметеринит</span><span class="sxs-lookup"><span data-stu-id="04b22-118">ParameterInit</span></span><br/> <span data-ttu-id="04b22-119">ParameterRef</span><span class="sxs-lookup"><span data-stu-id="04b22-119">ParameterRef</span></span><br/> <span data-ttu-id="04b22-120">PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="04b22-120">PrintCapabilities</span></span><br/> <span data-ttu-id="04b22-121">PrintTicket</span><span class="sxs-lookup"><span data-stu-id="04b22-121">PrintTicket</span></span><br/> <span data-ttu-id="04b22-122">Свойство</span><span class="sxs-lookup"><span data-stu-id="04b22-122">Property</span></span><br/> <span data-ttu-id="04b22-123">скоредпроперти</span><span class="sxs-lookup"><span data-stu-id="04b22-123">ScoredProperty</span></span><br/> | <span data-ttu-id="04b22-124">Эти элементы не должны иметь зависимостей конфигурации.</span><span class="sxs-lookup"><span data-stu-id="04b22-124">These elements must not have configuration dependencies.</span></span><br/>                                                                                                                                                           |
| <span data-ttu-id="04b22-125">параметердеф</span><span class="sxs-lookup"><span data-stu-id="04b22-125">ParameterDef</span></span> <br/>                                                                                                                                                                 | <span data-ttu-id="04b22-126">Элементы Параметердеф и элементы, содержащиеся в них, не должны иметь зависимостей конфигурации.</span><span class="sxs-lookup"><span data-stu-id="04b22-126">ParameterDef elements and elements contained within them to any nesting level must not have any configuration dependencies.</span></span><br/>                                                                                        |
| <span data-ttu-id="04b22-127">Свойство</span><span class="sxs-lookup"><span data-stu-id="04b22-127">Property</span></span> <br/>                                                                                                                                                                     | <span data-ttu-id="04b22-128">Элементы свойств могут иметь зависимости конфигурации, за исключением случаев, когда они появляются в элементах Параметердеф.</span><span class="sxs-lookup"><span data-stu-id="04b22-128">Property elements may have configuration dependencies, except when they appear within ParameterDef elements.</span></span><br/>                                                                                                       |
| <span data-ttu-id="04b22-129">Значение</span><span class="sxs-lookup"><span data-stu-id="04b22-129">Value</span></span> <br/>                                                                                                                                                                        | <span data-ttu-id="04b22-130">Элементы значения, которые отображаются в элементах Скоредпроперти, не должны иметь зависимостей конфигурации.</span><span class="sxs-lookup"><span data-stu-id="04b22-130">Value elements that appear within ScoredProperty elements must not have any configuration dependencies.</span></span> <span data-ttu-id="04b22-131">Элементы значения, отображаемые в элементе Property, могут иметь произвольную зависимость от конфигурации.</span><span class="sxs-lookup"><span data-stu-id="04b22-131">Value elements that appear within a Property element may have arbitrary dependencies on the configuration.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="04b22-132">См. также</span><span class="sxs-lookup"><span data-stu-id="04b22-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04b22-133">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="04b22-133">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 





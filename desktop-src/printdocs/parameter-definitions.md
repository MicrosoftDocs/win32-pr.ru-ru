---
description: Ознакомьтесь с определениями параметров в документе PrintCapabilities. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 82ba4658-f0e1-47a7-bb0c-1b527fabde4a
title: Определения параметров
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dc8ad2bed3a972202bc0a5bb07cbdd4ef9d8f44
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396579"
---
# <a name="parameter-definitions"></a><span data-ttu-id="108c1-105">Определения параметров</span><span class="sxs-lookup"><span data-stu-id="108c1-105">Parameter Definitions</span></span>

<span data-ttu-id="108c1-106">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="108c1-106">This topic is not current.</span></span> <span data-ttu-id="108c1-107">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="108c1-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="108c1-108">В этом разделе описываются определения открытых параметров, которые могут присутствовать в документе PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="108c1-108">This section outlines the public parameter definitions which may appear in either a PrintCapabilities document.</span></span>

<span data-ttu-id="108c1-109">Параметры используются для описания допустимого диапазона значений, а не дискретного перечисления значений.</span><span class="sxs-lookup"><span data-stu-id="108c1-109">Parameters are used to describe an acceptable range of values, rather than a discrete enumeration of values.</span></span>

## <a name="parameterdef"></a><span data-ttu-id="108c1-110">параметердеф</span><span class="sxs-lookup"><span data-stu-id="108c1-110">ParameterDef</span></span>

<span data-ttu-id="108c1-111">Сводку по типу элемента Параметердеф см. в разделе [параметердеф](parameterdef.md) .</span><span class="sxs-lookup"><span data-stu-id="108c1-111">For a summary of the ParameterDef element type, please refer to [ParameterDef](parameterdef.md) section.</span></span>

<span data-ttu-id="108c1-112">Дополнительные сведения о взаимодействии между элементами Параметердеф и Параметеринит см. в разделе [параметердеф и Параметеринит Elements](./parameterdef-and-parameterinit-elements.md) .</span><span class="sxs-lookup"><span data-stu-id="108c1-112">For more information on the interaction between ParameterDef elements and ParameterInit elements, refer to [ParameterDef and ParameterInit Elements](./parameterdef-and-parameterinit-elements.md) section.</span></span>

<span data-ttu-id="108c1-113">Элементы Параметердеф, определенные в ключевых словах схемы Print, должны быть полностью определены в документе PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="108c1-113">ParameterDef elements that are defined in the Print Schema Keywords must be fully defined in a PrintCapabilities document.</span></span>

## <a name="parameterref"></a><span data-ttu-id="108c1-114">ParameterRef</span><span class="sxs-lookup"><span data-stu-id="108c1-114">ParameterRef</span></span>

<span data-ttu-id="108c1-115">Сводку по типу элемента ParameterRef см. в разделе [ParameterRef](parameterref.md) .</span><span class="sxs-lookup"><span data-stu-id="108c1-115">For a summary of the ParameterRef element type, please refer to [ParameterRef](parameterref.md) section.</span></span>

<span data-ttu-id="108c1-116">Зарезервированное пользователем ключевое слово element может содержать ссылку на параметр.</span><span class="sxs-lookup"><span data-stu-id="108c1-116">A user configurable element keyword may contain a reference to a Parameter.</span></span> <span data-ttu-id="108c1-117">Элементы ParameterRef указаны как дочерний элемент элемента Скоредпроперти. Дополнительные сведения см. в разделе " [элементы ссылки на параметры](parameter-reference-elements.md) ".</span><span class="sxs-lookup"><span data-stu-id="108c1-117">ParameterRef elements are specified as a child of a ScoredProperty element For more information, please refer to [Parameter Reference Elements](parameter-reference-elements.md) section.</span></span>

## <a name="related-topics"></a><span data-ttu-id="108c1-118">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="108c1-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="108c1-119">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="108c1-119">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 

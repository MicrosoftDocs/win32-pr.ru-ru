---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 82ba4658-f0e1-47a7-bb0c-1b527fabde4a
title: Определения параметров
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca5a71bfc5a5111a826b5d221ff1436ecf921dd2
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "104273331"
---
# <a name="parameter-definitions"></a><span data-ttu-id="380ca-104">Определения параметров</span><span class="sxs-lookup"><span data-stu-id="380ca-104">Parameter Definitions</span></span>

<span data-ttu-id="380ca-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="380ca-105">This topic is not current.</span></span> <span data-ttu-id="380ca-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="380ca-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="380ca-107">В этом разделе описываются определения открытых параметров, которые могут присутствовать в документе PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="380ca-107">This section outlines the public parameter definitions which may appear in either a PrintCapabilities document.</span></span>

<span data-ttu-id="380ca-108">Параметры используются для описания допустимого диапазона значений, а не дискретного перечисления значений.</span><span class="sxs-lookup"><span data-stu-id="380ca-108">Parameters are used to describe an acceptable range of values, rather than a discrete enumeration of values.</span></span>

## <a name="parameterdef"></a><span data-ttu-id="380ca-109">параметердеф</span><span class="sxs-lookup"><span data-stu-id="380ca-109">ParameterDef</span></span>

<span data-ttu-id="380ca-110">Сводку по типу элемента Параметердеф см. в разделе [параметердеф](parameterdef.md) .</span><span class="sxs-lookup"><span data-stu-id="380ca-110">For a summary of the ParameterDef element type, please refer to [ParameterDef](parameterdef.md) section.</span></span>

<span data-ttu-id="380ca-111">Дополнительные сведения о взаимодействии между элементами Параметердеф и Параметеринит см. в разделе [параметердеф и Параметеринит Elements](./parameterdef-and-parameterinit-elements.md) .</span><span class="sxs-lookup"><span data-stu-id="380ca-111">For more information on the interaction between ParameterDef elements and ParameterInit elements, refer to [ParameterDef and ParameterInit Elements](./parameterdef-and-parameterinit-elements.md) section.</span></span>

<span data-ttu-id="380ca-112">Элементы Параметердеф, определенные в ключевых словах схемы Print, должны быть полностью определены в документе PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="380ca-112">ParameterDef elements that are defined in the Print Schema Keywords must be fully defined in a PrintCapabilities document.</span></span>

## <a name="parameterref"></a><span data-ttu-id="380ca-113">ParameterRef</span><span class="sxs-lookup"><span data-stu-id="380ca-113">ParameterRef</span></span>

<span data-ttu-id="380ca-114">Сводку по типу элемента ParameterRef см. в разделе [ParameterRef](parameterref.md) .</span><span class="sxs-lookup"><span data-stu-id="380ca-114">For a summary of the ParameterRef element type, please refer to [ParameterRef](parameterref.md) section.</span></span>

<span data-ttu-id="380ca-115">Зарезервированное пользователем ключевое слово element может содержать ссылку на параметр.</span><span class="sxs-lookup"><span data-stu-id="380ca-115">A user configurable element keyword may contain a reference to a Parameter.</span></span> <span data-ttu-id="380ca-116">Элементы ParameterRef указаны как дочерний элемент элемента Скоредпроперти. Дополнительные сведения см. в разделе " [элементы ссылки на параметры](parameter-reference-elements.md) ".</span><span class="sxs-lookup"><span data-stu-id="380ca-116">ParameterRef elements are specified as a child of a ScoredProperty element For more information, please refer to [Parameter Reference Elements](parameter-reference-elements.md) section.</span></span>

## <a name="related-topics"></a><span data-ttu-id="380ca-117">См. также</span><span class="sxs-lookup"><span data-stu-id="380ca-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="380ca-118">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="380ca-118">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 

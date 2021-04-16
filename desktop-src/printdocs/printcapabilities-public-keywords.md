---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 7f08747f-f7ff-4381-b2b9-1917e4708ee3
title: Общедоступные ключевые слова PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81d5e7b001a8106f95c830f0af5e99ee9821af64
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105664835"
---
# <a name="printcapabilities-public-keywords"></a><span data-ttu-id="cb0d3-104">Общедоступные ключевые слова PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="cb0d3-104">PrintCapabilities Public Keywords</span></span>

<span data-ttu-id="cb0d3-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="cb0d3-105">This topic is not current.</span></span> <span data-ttu-id="cb0d3-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="cb0d3-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="cb0d3-107">В следующем разделе указаны настраиваемые пользователем элементы и определения параметров, которые могут быть применимы к документу PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="cb0d3-107">The following section specifies both user configurable elements and parameter definitions which may be applicable to a PrintCapabilities document.</span></span>

## <a name="user-configurable-elements-usage"></a><span data-ttu-id="cb0d3-108">Использование настраиваемых элементов</span><span class="sxs-lookup"><span data-stu-id="cb0d3-108">User Configurable Elements Usage</span></span>

<span data-ttu-id="cb0d3-109">Настраиваемые пользователем элементы представляют собой общедоступные ключевые слова схемы печати, которые могут присутствовать в документе PrintCapabilities или PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="cb0d3-109">User Configurable Elements represent Print Schema Public Keywords which may appear in either a PrintCapabilities document or a PrintTicket.</span></span> <span data-ttu-id="cb0d3-110">Они предназначены для представления настраиваемых атрибутов устройств, поддерживаемых конкретным устройством, или для передачи параметров печати приложением или пользователем.</span><span class="sxs-lookup"><span data-stu-id="cb0d3-110">They are intended to represent configurable device attributes supported by a specific device or communicate print setting intent by an application or user.</span></span>

<span data-ttu-id="cb0d3-111">Настраиваемые пользователем элементы могут ссылаться на элементы ссылки на параметр.</span><span class="sxs-lookup"><span data-stu-id="cb0d3-111">User Configurable Elements may reference Parameter Reference Elements.</span></span> <span data-ttu-id="cb0d3-112">Дополнительные сведения см. в разделе " [элементы справочника по параметрам](parameter-reference-elements.md) ".</span><span class="sxs-lookup"><span data-stu-id="cb0d3-112">For more information, please refer to [Parameter Reference Elements](parameter-reference-elements.md) section.</span></span>

## <a name="parameter-definitions-usage"></a><span data-ttu-id="cb0d3-113">Использование определений параметров</span><span class="sxs-lookup"><span data-stu-id="cb0d3-113">Parameter Definitions Usage</span></span>

<span data-ttu-id="cb0d3-114">Определения параметров принимают форму типов элементов Параметердеф в документе возможностей печати.</span><span class="sxs-lookup"><span data-stu-id="cb0d3-114">Parameters definitions take the form of ParameterDef element types in a Print Capabilities document.</span></span> <span data-ttu-id="cb0d3-115">Типы элементов Параметердеф инициализируются в PrintTicket с помощью типа элемента Параметеринит.</span><span class="sxs-lookup"><span data-stu-id="cb0d3-115">ParameterDef element types are initialized in a PrintTicket using the ParameterInit element type.</span></span> <span data-ttu-id="cb0d3-116">Значение параметра будет указано с помощью элемента Параметеринит.</span><span class="sxs-lookup"><span data-stu-id="cb0d3-116">The value of the parameter will be specified using the ParameterInit element.</span></span> <span data-ttu-id="cb0d3-117">Настраиваемое пользователем ключевое слово может ссылаться на определение параметра с помощью типа элемента ParameterRef.</span><span class="sxs-lookup"><span data-stu-id="cb0d3-117">A user configurable keyword may reference a parameter definition using the ParameterRef element type.</span></span> <span data-ttu-id="cb0d3-118">Дополнительные сведения см. в разделе [конструкции параметров](parameter-constructs.md) .</span><span class="sxs-lookup"><span data-stu-id="cb0d3-118">For more information, please refer to [Parameter Constructs](parameter-constructs.md) section.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cb0d3-119">См. также</span><span class="sxs-lookup"><span data-stu-id="cb0d3-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb0d3-120">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="cb0d3-120">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




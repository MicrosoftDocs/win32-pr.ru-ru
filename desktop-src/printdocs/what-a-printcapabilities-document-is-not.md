---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 87a897cd-d3aa-488a-b129-9837d3500d0d
title: Что такое документ PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd6e18082a5e551f3997dad8b9688d84ff2f824a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105703513"
---
# <a name="what-a-printcapabilities-document-is-not"></a><span data-ttu-id="49307-104">Что такое документ PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="49307-104">What a PrintCapabilities Document Is Not</span></span>

<span data-ttu-id="49307-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="49307-105">This topic is not current.</span></span> <span data-ttu-id="49307-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="49307-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="49307-107">Стоит перечислить некоторые функциональные возможности и сведения, которые не должны предоставляться для документа PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="49307-107">It is worthwhile to list some of the functionality and information the PrintCapabilities document is not intended to provide.</span></span>

<span data-ttu-id="49307-108">Документ PrintCapabilities:</span><span class="sxs-lookup"><span data-stu-id="49307-108">A PrintCapabilities document:</span></span>

-   <span data-ttu-id="49307-109">Не представляет данные с несколькими значениями (зависящими от конфигурации).</span><span class="sxs-lookup"><span data-stu-id="49307-109">Does not represent multivalued (configuration-dependent) data.</span></span>

    <span data-ttu-id="49307-110">Каждый документ PrintCapabilities создается для конкретной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="49307-110">Each PrintCapabilities document is constructed for a specific configuration.</span></span> <span data-ttu-id="49307-111">Ни одно свойство, ни Скоредпроперти в документе не могут иметь значение, зависящее от конкретной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="49307-111">No Property or ScoredProperty in the document can have a Value that depends on the particular configuration.</span></span> <span data-ttu-id="49307-112">В исходной версии схемы поставщик PrintCapabilities должен обработать входной PrintTicket и создать документ PrintCapabilities, содержащий значения свойств, соответствующие конфигурации, указанной в PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="49307-112">In the initial schema version, the PrintCapabilities provider must process the input PrintTicket and create a PrintCapabilities document that contains Property values appropriate for the configuration specified in the PrintTicket.</span></span>

-   <span data-ttu-id="49307-113">Не содержит сведений об ограничениях.</span><span class="sxs-lookup"><span data-stu-id="49307-113">Does not contain constraint information.</span></span>

    <span data-ttu-id="49307-114">Документ PrintCapabilities не указывает, какие конфигурации разрешены и что не разрешено.</span><span class="sxs-lookup"><span data-stu-id="49307-114">The PrintCapabilities document does not indicate which configurations are allowed and which are not allowed.</span></span> <span data-ttu-id="49307-115">В первоначальной версии схемы поставщик PrintCapabilities должен хранить все данные, необходимые для проверки конфигурации, предоставить метод, проверяющий входной PrintTicket, и возвратить исправленный PrintTicket в случае, если указанный PrintTicket нарушает одно или несколько ограничений.</span><span class="sxs-lookup"><span data-stu-id="49307-115">In the initial schema version, the PrintCapabilities provider must store any information needed to validate configurations, supply a method that validates the input PrintTicket, and return a corrected PrintTicket in the event that the specified PrintTicket violates one or more constraints.</span></span>

-   <span data-ttu-id="49307-116">Не содержит динамических сведений об устройстве.</span><span class="sxs-lookup"><span data-stu-id="49307-116">Does not contain dynamic device information.</span></span>

    <span data-ttu-id="49307-117">При формировании документа PrintCapabilities для хранения быстро изменяющихся сведений о состоянии, таких как уровни рукописного ввода, оставшийся объем бумаги в каждом лотке или состояние застревания бумаги, возникает слишком много ресурсов.</span><span class="sxs-lookup"><span data-stu-id="49307-117">There is too much overhead involved in constructing the PrintCapabilities document for it to be used to hold rapidly changing status information, such as ink levels, paper remaining in each tray, or paper jam status.</span></span>

## <a name="related-topics"></a><span data-ttu-id="49307-118">См. также</span><span class="sxs-lookup"><span data-stu-id="49307-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49307-119">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="49307-119">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




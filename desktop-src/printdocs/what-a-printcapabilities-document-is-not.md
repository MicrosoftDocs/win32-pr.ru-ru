---
description: Узнайте о некоторых функциональных возможностях и сведениях, которые не должны предоставляться в документе PrintCapabilities.
ms.assetid: 87a897cd-d3aa-488a-b129-9837d3500d0d
title: Что такое документ PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bcd5dbedf6ee3a7e2713bd3591b182c606cfb0c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409897"
---
# <a name="what-a-printcapabilities-document-is-not"></a><span data-ttu-id="937c2-103">Что такое документ PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="937c2-103">What a PrintCapabilities Document Is Not</span></span>

<span data-ttu-id="937c2-104">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="937c2-104">This topic is not current.</span></span> <span data-ttu-id="937c2-105">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="937c2-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="937c2-106">Стоит перечислить некоторые функциональные возможности и сведения, которые не должны предоставляться для документа PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="937c2-106">It is worthwhile to list some of the functionality and information the PrintCapabilities document is not intended to provide.</span></span>

<span data-ttu-id="937c2-107">Документ PrintCapabilities:</span><span class="sxs-lookup"><span data-stu-id="937c2-107">A PrintCapabilities document:</span></span>

-   <span data-ttu-id="937c2-108">Не представляет данные с несколькими значениями (зависящими от конфигурации).</span><span class="sxs-lookup"><span data-stu-id="937c2-108">Does not represent multivalued (configuration-dependent) data.</span></span>

    <span data-ttu-id="937c2-109">Каждый документ PrintCapabilities создается для конкретной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="937c2-109">Each PrintCapabilities document is constructed for a specific configuration.</span></span> <span data-ttu-id="937c2-110">Ни одно свойство, ни Скоредпроперти в документе не могут иметь значение, зависящее от конкретной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="937c2-110">No Property or ScoredProperty in the document can have a Value that depends on the particular configuration.</span></span> <span data-ttu-id="937c2-111">В исходной версии схемы поставщик PrintCapabilities должен обработать входной PrintTicket и создать документ PrintCapabilities, содержащий значения свойств, соответствующие конфигурации, указанной в PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="937c2-111">In the initial schema version, the PrintCapabilities provider must process the input PrintTicket and create a PrintCapabilities document that contains Property values appropriate for the configuration specified in the PrintTicket.</span></span>

-   <span data-ttu-id="937c2-112">Не содержит сведений об ограничениях.</span><span class="sxs-lookup"><span data-stu-id="937c2-112">Does not contain constraint information.</span></span>

    <span data-ttu-id="937c2-113">Документ PrintCapabilities не указывает, какие конфигурации разрешены и что не разрешено.</span><span class="sxs-lookup"><span data-stu-id="937c2-113">The PrintCapabilities document does not indicate which configurations are allowed and which are not allowed.</span></span> <span data-ttu-id="937c2-114">В первоначальной версии схемы поставщик PrintCapabilities должен хранить все данные, необходимые для проверки конфигурации, предоставить метод, проверяющий входной PrintTicket, и возвратить исправленный PrintTicket в случае, если указанный PrintTicket нарушает одно или несколько ограничений.</span><span class="sxs-lookup"><span data-stu-id="937c2-114">In the initial schema version, the PrintCapabilities provider must store any information needed to validate configurations, supply a method that validates the input PrintTicket, and return a corrected PrintTicket in the event that the specified PrintTicket violates one or more constraints.</span></span>

-   <span data-ttu-id="937c2-115">Не содержит динамических сведений об устройстве.</span><span class="sxs-lookup"><span data-stu-id="937c2-115">Does not contain dynamic device information.</span></span>

    <span data-ttu-id="937c2-116">При формировании документа PrintCapabilities для хранения быстро изменяющихся сведений о состоянии, таких как уровни рукописного ввода, оставшийся объем бумаги в каждом лотке или состояние застревания бумаги, возникает слишком много ресурсов.</span><span class="sxs-lookup"><span data-stu-id="937c2-116">There is too much overhead involved in constructing the PrintCapabilities document for it to be used to hold rapidly changing status information, such as ink levels, paper remaining in each tray, or paper jam status.</span></span>

## <a name="related-topics"></a><span data-ttu-id="937c2-117">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="937c2-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="937c2-118">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="937c2-118">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




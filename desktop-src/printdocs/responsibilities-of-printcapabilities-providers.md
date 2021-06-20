---
description: Поставщики PrintCapabilities должны поддерживать минимальный набор возможностей, которые подразумеваются интерфейсом поставщика PrintTicket/PrintCapabilities.
ms.assetid: 92e9bce1-d58e-40a4-9721-832d7c3bc2b2
title: Обязанности поставщиков PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70cc04137eacdd2395205b96233db3c53964bc02
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404917"
---
# <a name="responsibilities-of-printcapabilities-providers"></a><span data-ttu-id="e3efe-103">Обязанности поставщиков PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="e3efe-103">Responsibilities of PrintCapabilities Providers</span></span>

<span data-ttu-id="e3efe-104">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="e3efe-104">This topic is not current.</span></span> <span data-ttu-id="e3efe-105">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="e3efe-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e3efe-106">Поставщики PrintCapabilities должны поддерживать минимальный набор возможностей, которые подразумеваются интерфейсом поставщика PrintTicket/PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="e3efe-106">PrintCapabilities providers must support a minimum set of capabilities, which are implied by the PrintTicket/PrintCapabilities Provider Interface.</span></span> <span data-ttu-id="e3efe-107">Эти возможности перечислены здесь.</span><span class="sxs-lookup"><span data-stu-id="e3efe-107">These capabilities are listed here.</span></span>

-   <span data-ttu-id="e3efe-108">Они должны следовать направлению распространения? Атрибут XML, если он присутствует в соответствующем контексте и содержит допустимое значение для этого контекста.</span><span class="sxs-lookup"><span data-stu-id="e3efe-108">They must follow the direction of the propagate??XML attribute, when it appears in the appropriate context and contains a valid value for that context.</span></span>

-   <span data-ttu-id="e3efe-109">Они должны создать документ PrintCapabilities, который соответствует схеме PrintCapabilities и удовлетворяет требованиям, указанным в схеме печати.</span><span class="sxs-lookup"><span data-stu-id="e3efe-109">They must generate a PrintCapabilities document that conforms to the PrintCapabilities Schema and satisfies the requirements specified in the Print Schema.</span></span>

-   <span data-ttu-id="e3efe-110">Они должны иметь возможность распознать допустимый PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="e3efe-110">They must be able to recognize a valid PrintTicket.</span></span>

-   <span data-ttu-id="e3efe-111">Они должны уметь интерпретировать PrintTicket и понимать конкретную конфигурацию, которую он представляет.</span><span class="sxs-lookup"><span data-stu-id="e3efe-111">They must be able to interpret a PrintTicket and understand the specific configuration it represents.</span></span>

-   <span data-ttu-id="e3efe-112">Они должны иметь возможность определить, содержит ли эта конфигурация конфликты ограничений.</span><span class="sxs-lookup"><span data-stu-id="e3efe-112">They must be able to determine whether that configuration contains constraint conflicts.</span></span>

-   <span data-ttu-id="e3efe-113">Они должны иметь возможность изменить недопустимый или конфликтующий PrintTicket, сделав минимально существенные изменения, чтобы сделать его как допустимым, так и без конфликтов.</span><span class="sxs-lookup"><span data-stu-id="e3efe-113">They must be able to modify an invalid or conflicting PrintTicket by making the least significant change necessary to make it both valid and without conflicts.</span></span>

-   <span data-ttu-id="e3efe-114">Они должны иметь возможность создавать документ PrintCapabilities для конкретной конфигурации устройства.</span><span class="sxs-lookup"><span data-stu-id="e3efe-114">They must be able to generate a PrintCapabilities document for a particular device configuration.</span></span>

-   <span data-ttu-id="e3efe-115">Они должны иметь возможность создавать конфигурацию по умолчанию или PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="e3efe-115">They must be able to generate a default configuration or PrintTicket.</span></span>

-   <span data-ttu-id="e3efe-116">Они должны иметь возможность создавать документ PrintCapabilities, соответствующий конфигурации по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e3efe-116">They must be able to generate a PrintCapabilities document that corresponds to the default configuration.</span></span>

-   <span data-ttu-id="e3efe-117">Они должны реализовать процесс оценки параметров, определяемый драйвером устройства, который способен определить близкость соответствия между двумя экземплярами параметров, принадлежащими к одной и той же функции.</span><span class="sxs-lookup"><span data-stu-id="e3efe-117">They must implement an Option-scoring process defined by the device driver capable of determining the closeness of match between two Option instances that belong to the same Feature.</span></span> <span data-ttu-id="e3efe-118">Этот алгоритм используется в процессе проверки PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="e3efe-118">This algorithm is used in the PrintTicket validation process.</span></span>

<span data-ttu-id="e3efe-119">В дополнение к вышеизложенным требованиям, документ PrintCapabilities должен содержать допустимые и правильные значения для каждого атрибута XML (например, ограниченного) каждого параметра.</span><span class="sxs-lookup"><span data-stu-id="e3efe-119">In addition to the foregoing requirements, the PrintCapabilities document must contain valid and correct values for each XML attribute (for example, constrained) of each Option.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e3efe-120">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="e3efe-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3efe-121">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="e3efe-121">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




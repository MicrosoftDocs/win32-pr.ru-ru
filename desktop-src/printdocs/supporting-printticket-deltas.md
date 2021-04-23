---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 80fdc8f1-4fda-4102-9b27-16d9acb4d077
title: Поддержка разностей PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 730c8d32d881dd30a6ab57b88d8fc1dfa87eee7a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105703525"
---
# <a name="supporting-printticket-deltas"></a><span data-ttu-id="5973b-104">Поддержка разностей PrintTicket</span><span class="sxs-lookup"><span data-stu-id="5973b-104">Supporting PrintTicket Deltas</span></span>

<span data-ttu-id="5973b-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="5973b-105">This topic is not current.</span></span> <span data-ttu-id="5973b-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="5973b-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5973b-107">В интерфейсе поставщика PrintTicket есть методы, которые можно использовать для внесения добавочных изменений в существующий PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="5973b-107">The PrintTicket Provider Interface has methods that can be used to make incremental changes to an existing PrintTicket.</span></span> <span data-ttu-id="5973b-108">Добавочные изменения PrintTicket можно указать в частичном PrintTicket, который называется разностью PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="5973b-108">The incremental PrintTicket changes can be specified in a partial PrintTicket that is known as a PrintTicket delta.</span></span> <span data-ttu-id="5973b-109">Пересмотренный объект PrintTicket создается путем объединения дельты PrintTicket с существующим PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="5973b-109">A revised PrintTicket is created by merging a PrintTicket delta with an existing PrintTicket.</span></span> <span data-ttu-id="5973b-110">Дополнительные сведения о методах, включающих изменения PrintTicket, см. в этом документе.</span><span class="sxs-lookup"><span data-stu-id="5973b-110">See the forthcoming PrintTicket Provider Interface document for more information about methods involving PrintTicket deltas.</span></span>

<span data-ttu-id="5973b-111">При обработке разностной учетной операции PrintTicket необходимо выполнить следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="5973b-111">When a PrintTicket delta is processed, the following steps must be performed.</span></span>

1.  <span data-ttu-id="5973b-112">Определение экземпляров функций или Параметеринит, общих для существующего объекта PrintTicket (целевой PrintTicket) и дельты PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="5973b-112">Identify Feature or ParameterInit instances that are common to both the existing PrintTicket (the target PrintTicket) and the PrintTicket delta.</span></span>

    -   <span data-ttu-id="5973b-113">Для каждого компонента, общего для целевого объекта PrintTicket и разностного изменения PrintTicket, замените функцию в целевом объекте PrintTicket соответствующей функцией в Дельта PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="5973b-113">For each Feature common to both the target PrintTicket and the PrintTicket delta, replace the Feature in the target PrintTicket by the corresponding Feature in the PrintTicket delta.</span></span>

    -   <span data-ttu-id="5973b-114">Для каждого Параметеринит, общего для целевого объекта PrintTicket и разностного изменения PrintTicket, замените Параметеринит в целевом объекте PrintTicket соответствующим Параметеринит в Дельта PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="5973b-114">For each ParameterInit common to both the target PrintTicket and the PrintTicket delta, replace the ParameterInit in the target PrintTicket by the corresponding ParameterInit in the PrintTicket delta.</span></span>

2.  <span data-ttu-id="5973b-115">Скопируйте все оставшиеся экземпляры компонента и Параметеринит в Дельта PrintTicket в целевой объект PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="5973b-115">Copy all remaining Feature and ParameterInit instances in the PrintTicket delta to the target PrintTicket.</span></span>

3.  <span data-ttu-id="5973b-116">Если алгоритм разрешения конфликтов позволяет указать приоритеты в самом PrintTicket, вы можете повысить приоритетность компонента и экземпляров Параметеринит, имена которых указаны в Дельта PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="5973b-116">If your conflict resolution algorithm allows priorities to be specified in the PrintTicket itself, you may choose to elevate the priorities of the Feature and ParameterInit instances named in the PrintTicket delta.</span></span>

4.  <span data-ttu-id="5973b-117">Выполните проверку PrintTicket, как описано в [контрольном списке PrintTicket](printticket-validation-checklist.md).</span><span class="sxs-lookup"><span data-stu-id="5973b-117">Perform PrintTicket validation as described in [PrintTicket Validation Checklist](printticket-validation-checklist.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5973b-118">См. также</span><span class="sxs-lookup"><span data-stu-id="5973b-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5973b-119">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="5973b-119">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




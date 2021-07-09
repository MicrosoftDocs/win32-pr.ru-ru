---
description: Сведения о поддержке разностей PrintTicket. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 80fdc8f1-4fda-4102-9b27-16d9acb4d077
title: Поддержка разностей PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7f72f82875d0207ed232f4db897c78295ce2ee0
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548783"
---
# <a name="supporting-printticket-deltas"></a><span data-ttu-id="4d298-105">Поддержка разностей PrintTicket</span><span class="sxs-lookup"><span data-stu-id="4d298-105">Supporting PrintTicket Deltas</span></span>

<span data-ttu-id="4d298-106">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="4d298-106">This topic is not current.</span></span> <span data-ttu-id="4d298-107">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="4d298-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="4d298-108">В интерфейсе поставщика PrintTicket есть методы, которые можно использовать для внесения добавочных изменений в существующий PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="4d298-108">The PrintTicket Provider Interface has methods that can be used to make incremental changes to an existing PrintTicket.</span></span> <span data-ttu-id="4d298-109">Добавочные изменения PrintTicket можно указать в частичном PrintTicket, который называется разностью PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="4d298-109">The incremental PrintTicket changes can be specified in a partial PrintTicket that is known as a PrintTicket delta.</span></span> <span data-ttu-id="4d298-110">Пересмотренный объект PrintTicket создается путем объединения дельты PrintTicket с существующим PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="4d298-110">A revised PrintTicket is created by merging a PrintTicket delta with an existing PrintTicket.</span></span> <span data-ttu-id="4d298-111">Дополнительные сведения о методах, включающих изменения PrintTicket, см. в этом документе.</span><span class="sxs-lookup"><span data-stu-id="4d298-111">See the forthcoming PrintTicket Provider Interface document for more information about methods involving PrintTicket deltas.</span></span>

<span data-ttu-id="4d298-112">При обработке разностной учетной операции PrintTicket необходимо выполнить следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="4d298-112">When a PrintTicket delta is processed, the following steps must be performed.</span></span>

1.  <span data-ttu-id="4d298-113">Определение экземпляров функций или Параметеринит, общих для существующего объекта PrintTicket (целевой PrintTicket) и дельты PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="4d298-113">Identify Feature or ParameterInit instances that are common to both the existing PrintTicket (the target PrintTicket) and the PrintTicket delta.</span></span>

    -   <span data-ttu-id="4d298-114">Для каждого компонента, общего для целевого объекта PrintTicket и разностного изменения PrintTicket, замените функцию в целевом объекте PrintTicket соответствующей функцией в Дельта PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="4d298-114">For each Feature common to both the target PrintTicket and the PrintTicket delta, replace the Feature in the target PrintTicket by the corresponding Feature in the PrintTicket delta.</span></span>

    -   <span data-ttu-id="4d298-115">Для каждого Параметеринит, общего для целевого объекта PrintTicket и разностного изменения PrintTicket, замените Параметеринит в целевом объекте PrintTicket соответствующим Параметеринит в Дельта PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="4d298-115">For each ParameterInit common to both the target PrintTicket and the PrintTicket delta, replace the ParameterInit in the target PrintTicket by the corresponding ParameterInit in the PrintTicket delta.</span></span>

2.  <span data-ttu-id="4d298-116">Скопируйте все оставшиеся экземпляры компонента и Параметеринит в Дельта PrintTicket в целевой объект PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="4d298-116">Copy all remaining Feature and ParameterInit instances in the PrintTicket delta to the target PrintTicket.</span></span>

3.  <span data-ttu-id="4d298-117">Если алгоритм разрешения конфликтов позволяет указать приоритеты в самом PrintTicket, вы можете повысить приоритетность компонента и экземпляров Параметеринит, имена которых указаны в Дельта PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="4d298-117">If your conflict resolution algorithm allows priorities to be specified in the PrintTicket itself, you may choose to elevate the priorities of the Feature and ParameterInit instances named in the PrintTicket delta.</span></span>

4.  <span data-ttu-id="4d298-118">Выполните проверку PrintTicket, как описано в [контрольном списке PrintTicket](printticket-validation-checklist.md).</span><span class="sxs-lookup"><span data-stu-id="4d298-118">Perform PrintTicket validation as described in [PrintTicket Validation Checklist](printticket-validation-checklist.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4d298-119">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="4d298-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d298-120">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="4d298-120">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




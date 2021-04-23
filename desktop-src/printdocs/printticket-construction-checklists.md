---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: ed53d1a8-d302-4855-9858-0f37dfbbd1d3
title: Контрольные списки для создания PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e742bcd3b94c5016fda6f97e2fb5e20a2cf70f73
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105693892"
---
# <a name="printticket-construction-checklists"></a><span data-ttu-id="b1fa3-104">Контрольные списки для создания PrintTicket</span><span class="sxs-lookup"><span data-stu-id="b1fa3-104">PrintTicket Construction Checklists</span></span>

<span data-ttu-id="b1fa3-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="b1fa3-105">This topic is not current.</span></span> <span data-ttu-id="b1fa3-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="b1fa3-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b1fa3-107">В этом разделе показано, как автор клиента PrintTicket может использовать типы элементов, определенные в платформе схемы печати, для создания PrintTicket, который описывает цель для устройства.</span><span class="sxs-lookup"><span data-stu-id="b1fa3-107">This section demonstrates how the author of a PrintTicket client can use the element types defined in the Print Schema Framework to create a PrintTicket that describes intents for a device.</span></span> <span data-ttu-id="b1fa3-108">PrintTicket может быть универсальным (не привязанным к конкретному устройству) или может быть специфичным для конкретного устройства.</span><span class="sxs-lookup"><span data-stu-id="b1fa3-108">The PrintTicket can be generic (not tied to a specific device), or it can be device-specific.</span></span> <span data-ttu-id="b1fa3-109">Семантика PrintTicket представлена более подробно.</span><span class="sxs-lookup"><span data-stu-id="b1fa3-109">The semantics of the PrintTicket are presented in greater detail.</span></span> <span data-ttu-id="b1fa3-110">Кроме того, этот раздел содержит общие сведения о концепциях и терминологии, более подробно описанные в последующих разделах.</span><span class="sxs-lookup"><span data-stu-id="b1fa3-110">In addition, this section contains an overview of concepts and terminology that are covered in more depth in subsequent sections.</span></span>

<span data-ttu-id="b1fa3-111">Существует два принципиально различных подхода к построению PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="b1fa3-111">There are two fundamentally different approaches to constructing a PrintTicket.</span></span> <span data-ttu-id="b1fa3-112">Можно использовать любой из этих подходов.</span><span class="sxs-lookup"><span data-stu-id="b1fa3-112">Either approach can be used.</span></span>

-   <span data-ttu-id="b1fa3-113">Нацеливание PrintTicket на неизвестное или универсальное устройство, [создав универсальный PrintTicket](creating-a-generic-printticket.md).</span><span class="sxs-lookup"><span data-stu-id="b1fa3-113">Target the PrintTicket to an unknown or generic device by [Creating a Generic PrintTicket](creating-a-generic-printticket.md).</span></span>

    <span data-ttu-id="b1fa3-114">Если ваша основная цель — сохранить намерение конечного пользователя, можно воспользоваться этим подходом, создав и сохранив непроверенный универсальный PrintTicket с документом.</span><span class="sxs-lookup"><span data-stu-id="b1fa3-114">If your primary objective is to preserve the end user's intent, you might want to take this approach, by constructing and storing an unvalidated generic PrintTicket with the document.</span></span>

-   <span data-ttu-id="b1fa3-115">Нацеливание PrintTicket на определенное устройство путем [создания Device-Specific PrintTicket](creating-a-device-specific-printticket.md).</span><span class="sxs-lookup"><span data-stu-id="b1fa3-115">Target the PrintTicket to a specific device, by [Creating a Device-Specific PrintTicket](creating-a-device-specific-printticket.md).</span></span>

    <span data-ttu-id="b1fa3-116">Если вы больше заинтересованы в использовании всех функций, предлагаемых определенным устройством, можно воспользоваться этим подходом, создав PrintTicket для конкретного устройства и сохранив проверенный PrintTicket в документе.</span><span class="sxs-lookup"><span data-stu-id="b1fa3-116">If you are more interested in taking advantage of all of the features offered by a particular device, you might want to take this approach, by constructing a PrintTicket for the specific device and storing the validated PrintTicket with the document.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b1fa3-117">См. также</span><span class="sxs-lookup"><span data-stu-id="b1fa3-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1fa3-118">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="b1fa3-118">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




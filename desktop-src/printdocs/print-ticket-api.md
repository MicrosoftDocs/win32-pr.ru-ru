---
description: API билета печати позволяет приложениям управлять и преобразовывать билеты печати.
ms.assetid: 4f854c1a-f2e1-48c4-9cc1-8a0fcf1bebed
title: API билетов на печать
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e19cfd8d624a1390b8afacd625e92fcee2704dd
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "104081734"
---
# <a name="print-ticket-api"></a><span data-ttu-id="db572-103">API билетов на печать</span><span class="sxs-lookup"><span data-stu-id="db572-103">Print Ticket API</span></span>

<span data-ttu-id="db572-104">API билета печати позволяет приложениям управлять и преобразовывать билеты печати.</span><span class="sxs-lookup"><span data-stu-id="db572-104">The Print Ticket API provides enables applications to manage and convert print tickets.</span></span>

<span data-ttu-id="db572-105">Билет на печать — это компонент документа XPS, который содержит предпочтительные параметры принтера для страницы в документе или для всего документа либо для задания печати, содержащего один или несколько документов.</span><span class="sxs-lookup"><span data-stu-id="db572-105">A print ticket is an XPS document component that contains the preferred printer settings for a page in a document, or for an entire document, or for a print job that contains one or more documents.</span></span> <span data-ttu-id="db572-106">Обратите внимание, что билеты печати находятся только в документах XPS.</span><span class="sxs-lookup"><span data-stu-id="db572-106">Note that print tickets are only found in XPS documents.</span></span>

<span data-ttu-id="db572-107">Прежде чем принтер сможет использовать билет печати, необходимо проверить билет печати на соответствие характеристикам принтера, определенным в функциях печати принтера.</span><span class="sxs-lookup"><span data-stu-id="db572-107">Before the printer can use the print ticket, the print ticket must be validated against the printer's characteristics, which are defined in the printer's Print Capabilities.</span></span> <span data-ttu-id="db572-108">Приложение выполняет эту проверку, вызывая API билета печати.</span><span class="sxs-lookup"><span data-stu-id="db572-108">The application performs that validation by calling the Print Ticket API.</span></span>

<span data-ttu-id="db572-109">PrintTicket и PrintCapabilities описываются с помощью элементов схемы печати, которая определяется [спецификацией печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="db572-109">The PrintTicket and PrintCapabilities are described by using elements of the Print Schema, which is defined by the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="db572-110">Этот раздел содержит сведения о следующих элементах API:</span><span class="sxs-lookup"><span data-stu-id="db572-110">This topic contains information about the following API elements:</span></span>

-   [<span data-ttu-id="db572-111">Функции API билетов на печать</span><span class="sxs-lookup"><span data-stu-id="db572-111">Print Ticket API Functions</span></span>](print-ticket-api-functions.md)
-   [<span data-ttu-id="db572-112">Перечисление API билетов на печать</span><span class="sxs-lookup"><span data-stu-id="db572-112">Print Ticket API Enumerations</span></span>](print-ticket-api-enumerations.md)

<span data-ttu-id="db572-113">На следующей схеме показана связь API билета печати с другими API-интерфейсами печати, которые может использовать собственное приложение Windows.</span><span class="sxs-lookup"><span data-stu-id="db572-113">The following diagram shows the relationship of the Print Ticket API to the other Print APIs that a native Windows application can use.</span></span>

![Схема, показывающая связь API билета печати с другими API-интерфейсами печати, которые может использовать собственное приложение Windows](images/print-apis-pt.png)

## <a name="related-topics"></a><span data-ttu-id="db572-115">См. также</span><span class="sxs-lookup"><span data-stu-id="db572-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db572-116">API печати XPS</span><span class="sxs-lookup"><span data-stu-id="db572-116">XPS Print API</span></span>](xps-printing.md)
</dt> <dt>

[<span data-ttu-id="db572-117">API диспетчера очереди печати</span><span class="sxs-lookup"><span data-stu-id="db572-117">Print Spooler API</span></span>](print-spooler-api.md)
</dt> <dt>

[<span data-ttu-id="db572-118">API печати GDI</span><span class="sxs-lookup"><span data-stu-id="db572-118">GDI Print API</span></span>](gdi-printing.md)
</dt> <dt>

[<span data-ttu-id="db572-119">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="db572-119">Print Schema Specification</span></span>](https://go.microsoft.com/fwlink/?linkid=2022117)
</dt> <dt>

[<span data-ttu-id="db572-120">XPS</span><span class="sxs-lookup"><span data-stu-id="db572-120">XML Paper Specification</span></span>](https://go.microsoft.com/fwlink/?linkid=2022122)
</dt> </dl>

 

 




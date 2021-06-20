---
description: В этой статье указаны общедоступные ключевые слова, определенные для схемы печати, и их использование для PrintCapabilities и PrintTicket.
ms.assetid: ff966475-626d-4a48-9349-e60454d47c57
title: Общие ключевые слова схемы печати
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0878ced6b011393479657a4fcdd4b7b7f9a2b62a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407147"
---
# <a name="print-schema-public-keywords"></a><span data-ttu-id="b8359-103">Общие ключевые слова схемы печати</span><span class="sxs-lookup"><span data-stu-id="b8359-103">Print Schema Public Keywords</span></span>

<span data-ttu-id="b8359-104">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="b8359-104">This topic is not current.</span></span> <span data-ttu-id="b8359-105">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="b8359-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b8359-106">В следующем разделе указываются открытые ключевые слова, которые определены для схемы печати.</span><span class="sxs-lookup"><span data-stu-id="b8359-106">The following section specifies the public keywords which are defined for the Print Schema.</span></span>

## <a name="print-schema-public-keywords-usage-for-print-capabilities"></a><span data-ttu-id="b8359-107">Вывод сведений об использовании общих ключевых слов схемы для возможностей печати</span><span class="sxs-lookup"><span data-stu-id="b8359-107">Print Schema Public Keywords Usage for Print Capabilities</span></span>

<span data-ttu-id="b8359-108">Ключевые слова, указанные в разделе PrintCapabilities Public Keywords, могут отображаться в документе возможностей печати.</span><span class="sxs-lookup"><span data-stu-id="b8359-108">Keywords specified under PrintCapabilities Public Keywords MAY appear in a Print Capabilities document.</span></span> <span data-ttu-id="b8359-109">Дополнительные сведения о взаимодействии этих ключевых слов с технологией PrintCapabilities см. в разделе [Обзор раздела PrintCapabilities](overview-of-the-printcapabilities.md) .</span><span class="sxs-lookup"><span data-stu-id="b8359-109">For more information on how these keywords interact with PrintCapabilities technology, please refer to [Overview of the PrintCapabilities](overview-of-the-printcapabilities.md) section.</span></span>

<span data-ttu-id="b8359-110">Общедоступные ключевые слова, относящиеся к PrintTicket, не должны отображаться в документе PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="b8359-110">Public keywords specific to PrintTicket SHOULD NOT appear in a PrintCapabilities document.</span></span>

## <a name="print-schema-public-keywords-usage-for-printticket"></a><span data-ttu-id="b8359-111">Вывод сведений об использовании общедоступных ключевых слов схемы для PrintTicket</span><span class="sxs-lookup"><span data-stu-id="b8359-111">Print Schema Public Keywords Usage for PrintTicket</span></span>

<span data-ttu-id="b8359-112">Ключевые слова, указанные в разделе PrintTicket Public Keywords, могут присутствовать в PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="b8359-112">Keywords specified under PrintTicket Public Keywords MAY appear in a PrintTicket.</span></span> <span data-ttu-id="b8359-113">Ключевые слова PrintTicket реализуются как тип элемента свойства.</span><span class="sxs-lookup"><span data-stu-id="b8359-113">PrintTicket keywords are implemented as a Property element type.</span></span> <span data-ttu-id="b8359-114">Дополнительные сведения о взаимодействии этих ключевых слов с технологией PrintTicket см. в разделе [сведения о конфигурации, не связанные с PrintCapabilities](configuration-information-not-related-to-printcapabilities.md) .</span><span class="sxs-lookup"><span data-stu-id="b8359-114">For more information on how these keywords interact with PrintTicket technology, please refer to [Configuration Information Not Related to PrintCapabilities](configuration-information-not-related-to-printcapabilities.md) section.</span></span>

<span data-ttu-id="b8359-115">Ключевые слова, указанные в разделе PrintCapabilities Public Keywords, могут отображаться в PrintTicket в зависимости от реализации PrintTicket в приложении и (или) драйвере.</span><span class="sxs-lookup"><span data-stu-id="b8359-115">Keywords specified under PrintCapabilities Public Keywords MAY appear in a PrintTicket depending on the implementation of the PrintTicket in an application and/or driver.</span></span> <span data-ttu-id="b8359-116">Это позволяет выбирать атрибуты устройств, определенные в документе PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="b8359-116">This provides selections for device attributes defined in the PrintCapabilities document.</span></span> <span data-ttu-id="b8359-117">Дополнительные сведения о взаимодействии между ключевыми словами PrintCapabilities и PrintTicket см. в разделе [назначение PrintTicket](purpose-of-the-printticket.md) .</span><span class="sxs-lookup"><span data-stu-id="b8359-117">For more information on the interaction between PrintCapabilities keywords and the PrintTicket, please refer to [Purpose of the PrintTicket](purpose-of-the-printticket.md) section.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b8359-118">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="b8359-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8359-119">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="b8359-119">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




---
description: В этом обзоре описывается схема печати и ссылки на разделы справки по печати схемы. Схема печати включает ключевые слова и платформу для схемы печати.
ms.assetid: d746bdd1-96c2-41f5-ad99-0b51c8ee8731
title: Ссылка на схему печати прежних версий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81a8f417d20913563cfd4a52ba51d21b516e73f0
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407137"
---
# <a name="legacy-print-schema-reference"></a><span data-ttu-id="5b1c5-104">Ссылка на схему печати прежних версий</span><span class="sxs-lookup"><span data-stu-id="5b1c5-104">Legacy Print Schema Reference</span></span>

<span data-ttu-id="5b1c5-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="5b1c5-105">This topic is not current.</span></span> <span data-ttu-id="5b1c5-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="5b1c5-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5b1c5-107">Схема печати и связанные с ней технологии доступны в Microsoft .NET Framework 3,0, Microsoft Windows Vista и более поздних выпусках.</span><span class="sxs-lookup"><span data-stu-id="5b1c5-107">The Print Schema and related technologies are available in the Microsoft .NET Framework 3.0, Microsoft Windows Vista, and later releases.</span></span>

<span data-ttu-id="5b1c5-108">Схема печати предоставляет формат на основе XML для выражения и организации большого набора свойств, описывающих формат задания или PrintCapabilities иерархически структурированным способом.</span><span class="sxs-lookup"><span data-stu-id="5b1c5-108">The Print Schema provides an XML-based format for expressing and organizing a large set of properties that describe either a job format or PrintCapabilities in a hierarchically structured manner.</span></span>

<span data-ttu-id="5b1c5-109">Схема печати — это термин-тег, который включает два компонента: ключевые слова схемы печати и платформу для печати схемы.</span><span class="sxs-lookup"><span data-stu-id="5b1c5-109">The Print Schema is an umbrella term that includes two components, the Print Schema Keywords and the Print Schema Framework.</span></span> <span data-ttu-id="5b1c5-110">Документ зарезервированных слов схемы печати — это открытая схема, которая определяет набор экземпляров элементов, которые можно использовать для описания атрибутов устройств и форматирования заданий печати.</span><span class="sxs-lookup"><span data-stu-id="5b1c5-110">The Print Schema Keywords document is a public schema that defines a set of element instances that can be used to describe device attributes and print job formatting.</span></span> <span data-ttu-id="5b1c5-111">Платформа схемы печати — это открытая схема, которая определяет иерархическую структуру типов элементов XML и указывает, как типы элементов могут использоваться вместе.</span><span class="sxs-lookup"><span data-stu-id="5b1c5-111">The Print Schema Framework is a public schema that defines a hierarchically structured collection of XML element types, and specifies how the element types can be used together.</span></span>

<span data-ttu-id="5b1c5-112">Ключевые слова и платформа Print Schema (Печать схемы) формируют основу для двух технологий печати, связанных с схемой, схемы PrintCapabilities и схемы PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="5b1c5-112">The Print Schema Keywords and the Print Schema Framework form the foundation for two Print Schema-related technologies, the PrintCapabilities Schema, and the PrintTicket Schema.</span></span>

<span data-ttu-id="5b1c5-113">Важно помнить, что одной из целей схемы печати является поддержка расширений схемы поставщиками.</span><span class="sxs-lookup"><span data-stu-id="5b1c5-113">It is important to keep in mind that one of the goals of the Print Schema is to support schema extensions by providers.</span></span> <span data-ttu-id="5b1c5-114">Это значит, что поставщики не ограничиваются использованием только тех экземпляров свойств, компонентов или Параметеринит, которые определены в ключевых словах «Печать схемы» в технологиях, созданных на платформе схемы печати.</span><span class="sxs-lookup"><span data-stu-id="5b1c5-114">That is, providers are not restricted to using only those Property, Feature, Option, or ParameterInit instances defined in the Print Schema Keywords in the technologies built on the Print Schema Framework.</span></span> <span data-ttu-id="5b1c5-115">Экземпляры элементов, зависящие от поставщика, могут свободно перемещаться между экземплярами элементов, определенными в ключевых словах схемы Print.</span><span class="sxs-lookup"><span data-stu-id="5b1c5-115">Provider-specific element instances may be freely interspersed within element instances defined in the Print Schema Keywords.</span></span> <span data-ttu-id="5b1c5-116">Единственное требование заключается в том, что экземпляры свойств, специфичные для конкретного поставщика (то есть частные), должны принадлежать пространству имен, которое явно связано с поставщиком.</span><span class="sxs-lookup"><span data-stu-id="5b1c5-116">The only requirement is that provider-specific (that is, private) Property instances must belong to a namespace that is clearly associated with the provider.</span></span>

-   [<span data-ttu-id="5b1c5-117">Фон схемы печати</span><span class="sxs-lookup"><span data-stu-id="5b1c5-117">Print Schema Background</span></span>](print-schema-background.md)

-   [<span data-ttu-id="5b1c5-118">Технологии печати Schema-Related</span><span class="sxs-lookup"><span data-stu-id="5b1c5-118">Print Schema-Related Technologies</span></span>](print-schema-related-technologies.md)

-   [<span data-ttu-id="5b1c5-119">Термины, используемые в схеме печати</span><span class="sxs-lookup"><span data-stu-id="5b1c5-119">Terms Used in the Print Schema</span></span>](terms-used-in-the-print-schema.md)

-   [<span data-ttu-id="5b1c5-120">Синтаксис схемы печати</span><span class="sxs-lookup"><span data-stu-id="5b1c5-120">Syntax of the Print Schema</span></span>](syntax-of-the-print-schema.md)

-   [<span data-ttu-id="5b1c5-121">Общие сведения о типах элементов</span><span class="sxs-lookup"><span data-stu-id="5b1c5-121">Summary of Element Types</span></span>](summary-of-element-types.md)

-   [<span data-ttu-id="5b1c5-122">Платформа для печати схемы</span><span class="sxs-lookup"><span data-stu-id="5b1c5-122">Print Schema Framework</span></span>](print-schema-framework.md)

-   [<span data-ttu-id="5b1c5-123">Общие ключевые слова схемы печати</span><span class="sxs-lookup"><span data-stu-id="5b1c5-123">Print Schema Public Keywords</span></span>](print-schema-public-keywords.md)

-   [<span data-ttu-id="5b1c5-124">PrintCapabilities схемы и построения документов</span><span class="sxs-lookup"><span data-stu-id="5b1c5-124">PrintCapabilities Schema and Document Construction</span></span>](printcapabilities-schema-and-document-construction.md)

-   [<span data-ttu-id="5b1c5-125">Создание схемы и построения документов PrintTicket</span><span class="sxs-lookup"><span data-stu-id="5b1c5-125">PrintTicket Schema and Document Construction</span></span>](printticket-schema-and-document-construction.md)

## <a name="related-topics"></a><span data-ttu-id="5b1c5-126">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="5b1c5-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b1c5-127">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="5b1c5-127">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




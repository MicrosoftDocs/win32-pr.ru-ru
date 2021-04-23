---
description: Схема печати и связанные технологии доступны в Microsoft .NET Framework 3,0 и более поздних версиях Microsoft .NET Framework, а также в Windows Vista и более поздних версиях Windows.
ms.assetid: 98d5f8ec-54bd-4e88-b632-ed427b599cb6
title: Схема печати
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae3ac50b9a2f2aba9cda7dc73f183e1f3571cc9d
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105684804"
---
# <a name="print-schema"></a><span data-ttu-id="a7952-103">Схема печати</span><span class="sxs-lookup"><span data-stu-id="a7952-103">Print Schema</span></span>

<span data-ttu-id="a7952-104">Схема печати и связанные технологии доступны в Microsoft .NET Framework 3,0 и более поздних версиях Microsoft .NET Framework, а также в Windows Vista и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="a7952-104">The Print Schema and related technologies are available in Microsoft .NET Framework 3.0 and later versions of Microsoft .NET Framework, and in Windows Vista and later versions of Windows.</span></span> <span data-ttu-id="a7952-105">Документы XPS и объектная модель XPS могут использовать объекты билетов на печать, которые описаны в [спецификации схемы печати](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip), чтобы задать параметры печати документа для принтеров и просмотра приложений.</span><span class="sxs-lookup"><span data-stu-id="a7952-105">XPS documents and the XPS Object Model can use the print ticket objects, which are described in the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip), to specify the printing preferences of a document to printers and viewing applications.</span></span>

<span data-ttu-id="a7952-106">[Спецификация печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip) — это загружаемый документ, содержащий сведения о схеме печати и способах ее использования в документах и печати.</span><span class="sxs-lookup"><span data-stu-id="a7952-106">The [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip) is a downloadable document that contains information about the Print Schema and how to use it in documents and printing.</span></span> <span data-ttu-id="a7952-107">Дополнительные сведения предоставляются только для вашей информации, в [устаревшей ссылке на схему печати](print-schema.md). Однако она может не точно отражать текущую версию [спецификации схемы печати](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="a7952-107">Additional information is provided online for your information only, at [Legacy Print Schema Reference](print-schema.md); however, it might not accurately reflect the current version of the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span> <span data-ttu-id="a7952-108">Актуальные сведения о проектировании см. в [спецификации схемы печати](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip) .</span><span class="sxs-lookup"><span data-stu-id="a7952-108">Refer to the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip) for the most current design information.</span></span>

## <a name="print-schema-overview"></a><span data-ttu-id="a7952-109">Обзор схемы печати</span><span class="sxs-lookup"><span data-stu-id="a7952-109">Print Schema Overview</span></span>

<span data-ttu-id="a7952-110">Схема печати — это иерархическая структурированная схема на основе XML, которая используется для Организации и описания свойств принтера или задания печати.</span><span class="sxs-lookup"><span data-stu-id="a7952-110">The Print Schema is a hierarchically structured, XML-based schema that is used to organize and describe the properties of a printer or print job.</span></span> <span data-ttu-id="a7952-111">Схема печати включает два компонента: ключевые слова схемы печати и платформу печати схемы.</span><span class="sxs-lookup"><span data-stu-id="a7952-111">The Print Schema includes two components: the Print Schema Keywords and the Print Schema Framework.</span></span> <span data-ttu-id="a7952-112">Ключевые слова схемы Print — это набор экземпляров элементов, описывающих атрибуты принтера и намерение форматирования задания печати.</span><span class="sxs-lookup"><span data-stu-id="a7952-112">The Print Schema Keywords are a set of element instances that describe printer attributes and print job formatting intent.</span></span> <span data-ttu-id="a7952-113">Платформа схемы печати определяет иерархически структурированную коллекцию типов элементов XML и то, как эти типы элементов могут использоваться вместе.</span><span class="sxs-lookup"><span data-stu-id="a7952-113">The Print Schema Framework defines a hierarchically structured collection of XML element types and how these element types can be used together.</span></span>

<span data-ttu-id="a7952-114">Технологии печатной схемы, называемые *PrintCapabilities* и *PrintTicket*, создаются с помощью ключевых слов схемы Print, как указано в платформе схемы печати.</span><span class="sxs-lookup"><span data-stu-id="a7952-114">The Print Schema technologies, called *PrintCapabilities* and *PrintTicket*, are built using the Print Schema Keywords as specified by the Print Schema Framework.</span></span> <span data-ttu-id="a7952-115">Спецификация печати схемы поддерживает расширения схемы сторонними производителями, поэтому пользователи схемы печати не ограничиваются экземплярами свойств, компонентов, параметров или Параметеринит, которые определены ключевыми словами схемы печати.</span><span class="sxs-lookup"><span data-stu-id="a7952-115">The Print Schema Specification supports schema extensions by third parties, so that Print Schema users are not restricted to the Property, Feature, Option, or ParameterInit instances that are defined by the Print Schema Keywords.</span></span> <span data-ttu-id="a7952-116">К экземплярам элементов, определяемым ключевыми словами схемы Print, можно добавлять сторонние экземпляры элементов. Однако частные экземпляры свойств сторонних разработчиков должны принадлежать пространству имен, которое явно связано с третьим лицом, создавшим пространство имен.</span><span class="sxs-lookup"><span data-stu-id="a7952-116">Third-party element instances can be added to element instances that are defined by the Print Schema Keywords; however, private, third-party Property instances must belong to a namespace that is clearly associated with the third party that created the namespace.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a7952-117">См. также</span><span class="sxs-lookup"><span data-stu-id="a7952-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7952-118">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="a7952-118">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> <dt>

[<span data-ttu-id="a7952-119">Ссылка на схему печати прежних версий</span><span class="sxs-lookup"><span data-stu-id="a7952-119">Legacy Print Schema Reference</span></span>](print-schema.md)
</dt> <dt>

[<span data-ttu-id="a7952-120">Двунаправленное взаимодействие с принтерами (центр разработки оборудования)</span><span class="sxs-lookup"><span data-stu-id="a7952-120">Bidirectional printer communications (Hardware Dev Center)</span></span>](/windows-hardware/drivers/print/bidirectional-communication)
</dt> </dl>

 

 

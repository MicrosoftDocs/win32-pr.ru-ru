---
description: Научитесь поддерживать различные версии платформы схемы печати. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: fc89dd2d-9a5d-400b-aee9-a1e4cf7d83da
title: Поддержка версий схемы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eac627d3dd711bc952d881efd393720af128e7f
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120599"
---
# <a name="supporting-schema-versions"></a><span data-ttu-id="2600c-105">Поддержка версий схемы</span><span class="sxs-lookup"><span data-stu-id="2600c-105">Supporting Schema Versions</span></span>

<span data-ttu-id="2600c-106">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="2600c-106">This topic is not current.</span></span> <span data-ttu-id="2600c-107">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="2600c-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="2600c-108">Платформа печати схемы может быть изменена в будущем по мере возникновения новых потребностей.</span><span class="sxs-lookup"><span data-stu-id="2600c-108">The Print Schema Framework is subject to change in the future as new needs arise.</span></span> <span data-ttu-id="2600c-109">Такие изменения должны быть очень редкими, поскольку наиболее распространенным изменением является ввод новых имен экземпляров.</span><span class="sxs-lookup"><span data-stu-id="2600c-109">Such changes are expected to be very infrequent, because the most common change is the introduction of new instance names.</span></span> <span data-ttu-id="2600c-110">Это изменение не влияет на структуру платформы и должно быть прозрачным для клиентов и поставщиков.</span><span class="sxs-lookup"><span data-stu-id="2600c-110">This change does not affect the structure of the Framework, and should be transparent to clients and providers.</span></span> <span data-ttu-id="2600c-111">Любые изменения структуры и организации платформы схемы печати будут определяться с шагом приращения до номера версии.</span><span class="sxs-lookup"><span data-stu-id="2600c-111">Any changes to the structure and organization of the Print Schema Framework will be identified by increments to its version number.</span></span> <span data-ttu-id="2600c-112">Дополнения к ключевым словам схемы печати не будут идентифицированы.</span><span class="sxs-lookup"><span data-stu-id="2600c-112">Additions to the Print Schema Keywords will not be identified.</span></span> <span data-ttu-id="2600c-113">Поставщики PrintTicket должны поддерживать текущую версию платформы схемы печати, а также любые предыдущие версии.</span><span class="sxs-lookup"><span data-stu-id="2600c-113">PrintTicket providers must be capable of supporting the current Print Schema Framework version, as well as any prior version.</span></span> <span data-ttu-id="2600c-114">Версия платформы для печати схемы определяется с помощью атрибута XML: Version, который отображается в корневом элементе PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="2600c-114">The Print Schema Framework version is identified using the XML Attribute: Version that appears at the root element of the PrintTicket.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2600c-115">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="2600c-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2600c-116">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="2600c-116">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




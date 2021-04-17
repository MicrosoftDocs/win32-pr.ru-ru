---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: fc89dd2d-9a5d-400b-aee9-a1e4cf7d83da
title: Поддержка версий схемы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d674449d581aca2ddfc80da2312b31eb6c930a6f
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105647769"
---
# <a name="supporting-schema-versions"></a><span data-ttu-id="eda7a-104">Поддержка версий схемы</span><span class="sxs-lookup"><span data-stu-id="eda7a-104">Supporting Schema Versions</span></span>

<span data-ttu-id="eda7a-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="eda7a-105">This topic is not current.</span></span> <span data-ttu-id="eda7a-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="eda7a-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="eda7a-107">Платформа печати схемы может быть изменена в будущем по мере возникновения новых потребностей.</span><span class="sxs-lookup"><span data-stu-id="eda7a-107">The Print Schema Framework is subject to change in the future as new needs arise.</span></span> <span data-ttu-id="eda7a-108">Такие изменения должны быть очень редкими, поскольку наиболее распространенным изменением является ввод новых имен экземпляров.</span><span class="sxs-lookup"><span data-stu-id="eda7a-108">Such changes are expected to be very infrequent, because the most common change is the introduction of new instance names.</span></span> <span data-ttu-id="eda7a-109">Это изменение не влияет на структуру платформы и должно быть прозрачным для клиентов и поставщиков.</span><span class="sxs-lookup"><span data-stu-id="eda7a-109">This change does not affect the structure of the Framework, and should be transparent to clients and providers.</span></span> <span data-ttu-id="eda7a-110">Любые изменения структуры и организации платформы схемы печати будут определяться с шагом приращения до номера версии.</span><span class="sxs-lookup"><span data-stu-id="eda7a-110">Any changes to the structure and organization of the Print Schema Framework will be identified by increments to its version number.</span></span> <span data-ttu-id="eda7a-111">Дополнения к ключевым словам схемы печати не будут идентифицированы.</span><span class="sxs-lookup"><span data-stu-id="eda7a-111">Additions to the Print Schema Keywords will not be identified.</span></span> <span data-ttu-id="eda7a-112">Поставщики PrintTicket должны поддерживать текущую версию платформы схемы печати, а также любые предыдущие версии.</span><span class="sxs-lookup"><span data-stu-id="eda7a-112">PrintTicket providers must be capable of supporting the current Print Schema Framework version, as well as any prior version.</span></span> <span data-ttu-id="eda7a-113">Версия платформы для печати схемы определяется с помощью атрибута XML: Version, который отображается в корневом элементе PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="eda7a-113">The Print Schema Framework version is identified using the XML Attribute: Version that appears at the root element of the PrintTicket.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eda7a-114">См. также</span><span class="sxs-lookup"><span data-stu-id="eda7a-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eda7a-115">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="eda7a-115">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




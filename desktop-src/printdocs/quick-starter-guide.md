---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 2c1d912e-464e-48d2-ba4f-c0b9a811b25e
title: Краткое руководство
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8f3933cb59e270dd8ef2eff8d295d33ab1f9203
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "104351775"
---
# <a name="quick-starter-guide"></a><span data-ttu-id="8f44f-104">Краткое руководство</span><span class="sxs-lookup"><span data-stu-id="8f44f-104">Quick Starter Guide</span></span>

<span data-ttu-id="8f44f-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="8f44f-105">This topic is not current.</span></span> <span data-ttu-id="8f44f-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="8f44f-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="8f44f-107">Эта страница предназначена для быстрого начала реализации PrintTicket и PrintCapabilities для вашего приложения или драйвера устройства.</span><span class="sxs-lookup"><span data-stu-id="8f44f-107">This page is designed to give you a quick start to implement PrintTicket and PrintCapabilities for your application or device driver.</span></span> <span data-ttu-id="8f44f-108">Хотя мы рекомендуем полностью прочитать спецификацию схемы печати, эта страница поможет вам приступить к работе в ключевых областях, на которые следует обратить внимание.</span><span class="sxs-lookup"><span data-stu-id="8f44f-108">Although we encourage that you read the Print Schema specification in full, this page will help give you a jump start in key areas you should pay attention to.</span></span>

1) <span data-ttu-id="8f44f-109">Ознакомьтесь с [технологиями печати Schema-Related](print-schema-related-technologies.md) , чтобы получить обзор технологий PrintTicket и возможностей печати.</span><span class="sxs-lookup"><span data-stu-id="8f44f-109">Read the [Print Schema-Related Technologies](print-schema-related-technologies.md) to give you an overview of PrintTicket and Print Capabilities technologies</span></span>

2) <span data-ttu-id="8f44f-110">Убедитесь, что у вас есть отчет по [сводкам типов элементов](summary-of-element-types.md) , которые используются для быстрой печати связанных с схемой технологий.</span><span class="sxs-lookup"><span data-stu-id="8f44f-110">Ensure that you have a grasp on the [Summary of Element Types](summary-of-element-types.md) which are used to express Print Schema related technologies.</span></span>

3) <span data-ttu-id="8f44f-111">PrintCapabilities документы и PrintTicket определяются по трем уровням [префиксов](scoping-prefix.md) , заданиям, документам и страницам.</span><span class="sxs-lookup"><span data-stu-id="8f44f-111">PrintCapabilities documents and PrintTickets are defined at three [Scoping Prefix](scoping-prefix.md) levels, Job, Document and Page.</span></span>

4) <span data-ttu-id="8f44f-112">Прочтите различные [XML-атрибуты](xml-attributes.md) , используемые в различных типах элементов схемы печати</span><span class="sxs-lookup"><span data-stu-id="8f44f-112">Read over the different [XML Attributes](xml-attributes.md) which are used within different Print Schema element types</span></span>

5) <span data-ttu-id="8f44f-113">Ознакомьтесь с [контрольным списком для создания документа PrintCapabilities](printcapabilities-document-construction-checklist.md) , а также предоставленным [примером документа PrintCapabilities](printcapabilities-document-example.md)</span><span class="sxs-lookup"><span data-stu-id="8f44f-113">Review the [PrintCapabilities Document Construction Checklist](printcapabilities-document-construction-checklist.md) and also the provided [PrintCapabilities Document Example](printcapabilities-document-example.md)</span></span>

6) <span data-ttu-id="8f44f-114">Проверьте [Контрольные списки для создания PrintTicket](printticket-construction-checklists.md) , а также предоставленный [Пример PrintTicket](printticket-example.md) .</span><span class="sxs-lookup"><span data-stu-id="8f44f-114">Review the [PrintTicket Construction Checklists](printticket-construction-checklists.md) and also the provided [PrintTicket Example](printticket-example.md)</span></span>

7) <span data-ttu-id="8f44f-115">Поставщики PrintTicket также должны изучить [Контрольный список для проверки PrintTicket](printticket-validation-checklist.md) , чтобы обеспечить соответствие спецификации принтсчема.</span><span class="sxs-lookup"><span data-stu-id="8f44f-115">PrintTicket providers should also review the [PrintTicket Validation Checklist](printticket-validation-checklist.md) to ensure conformance with the PrintSchema specification</span></span>

8) <span data-ttu-id="8f44f-116">Проверьте как [настраиваемые пользователем элементы](user-configurable-elements.md) , так и [определения параметров](parameter-definitions.md) общие ключевые слова схемы печати, которые могут появиться в документе PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="8f44f-116">Review both [User Configurable Elements](user-configurable-elements.md) and [Parameter Definitions](parameter-definitions.md) public Print Schema keywords which may appear in a PrintCapabilities document</span></span>

## <a name="related-topics"></a><span data-ttu-id="8f44f-117">См. также</span><span class="sxs-lookup"><span data-stu-id="8f44f-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f44f-118">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="8f44f-118">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




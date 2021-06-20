---
description: После проверки PrintTicket можно использовать для создания моментального снимка PrintCapabilities.
ms.assetid: b49e20b7-bd9e-4b8f-bb4a-bb1e99b0c417
title: Создание документа PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b96ea51cef9dfd0f351704b3b71a7f6163737736
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409517"
---
# <a name="creating-a-printcapabilities-document"></a><span data-ttu-id="e0109-103">Создание документа PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="e0109-103">Creating a PrintCapabilities Document</span></span>

<span data-ttu-id="e0109-104">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="e0109-104">This topic is not current.</span></span> <span data-ttu-id="e0109-105">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="e0109-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e0109-106">После проверки PrintTicket можно использовать для создания моментального снимка PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="e0109-106">After a PrintTicket is validated, it can be used to create a snapshot of the PrintCapabilities.</span></span> <span data-ttu-id="e0109-107">Поставщик должен иметь внутреннее представление для любого свойства, значение которого зависит от конфигурации устройства.</span><span class="sxs-lookup"><span data-stu-id="e0109-107">The provider must have an internal representation for any Property whose Value is dependent on the device configuration.</span></span> <span data-ttu-id="e0109-108">Например, если Спотдиаметер является свойством, которое зависит от функций разрешения и MediaType, внутреннее представление Спотдиаметер, связанное с различными значениями для разрешения, и параметр MediaType может выглядеть так, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="e0109-108">For example, if SpotDiameter is a Property that is dependent on both the Resolution and MediaType Features, an internal representation of SpotDiameter as it relates to the various values for Resolution and MediaType might appear as in the following table:</span></span>



| <span data-ttu-id="e0109-109">Решение</span><span class="sxs-lookup"><span data-stu-id="e0109-109">Resolution</span></span>      | <span data-ttu-id="e0109-110">MediaType</span><span class="sxs-lookup"><span data-stu-id="e0109-110">MediaType</span></span>         | <span data-ttu-id="e0109-111">спотдиаметер</span><span class="sxs-lookup"><span data-stu-id="e0109-111">SpotDiameter</span></span>   |
|-----------------|-------------------|----------------|
| <span data-ttu-id="e0109-112">300</span><span class="sxs-lookup"><span data-stu-id="e0109-112">300</span></span><br/>  | <span data-ttu-id="e0109-113">Bond</span><span class="sxs-lookup"><span data-stu-id="e0109-113">Bond</span></span><br/>   | <span data-ttu-id="e0109-114">520</span><span class="sxs-lookup"><span data-stu-id="e0109-114">520</span></span><br/> |
| <span data-ttu-id="e0109-115">300</span><span class="sxs-lookup"><span data-stu-id="e0109-115">300</span></span><br/>  | <span data-ttu-id="e0109-116">Глянцевое</span><span class="sxs-lookup"><span data-stu-id="e0109-116">Glossy</span></span><br/> | <span data-ttu-id="e0109-117">350</span><span class="sxs-lookup"><span data-stu-id="e0109-117">350</span></span><br/> |
| <span data-ttu-id="e0109-118">600</span><span class="sxs-lookup"><span data-stu-id="e0109-118">600</span></span><br/>  | <span data-ttu-id="e0109-119">Bond</span><span class="sxs-lookup"><span data-stu-id="e0109-119">Bond</span></span><br/>   | <span data-ttu-id="e0109-120">330</span><span class="sxs-lookup"><span data-stu-id="e0109-120">330</span></span><br/> |
| <span data-ttu-id="e0109-121">600</span><span class="sxs-lookup"><span data-stu-id="e0109-121">600</span></span><br/>  | <span data-ttu-id="e0109-122">Глянцевое</span><span class="sxs-lookup"><span data-stu-id="e0109-122">Glossy</span></span><br/> | <span data-ttu-id="e0109-123">180</span><span class="sxs-lookup"><span data-stu-id="e0109-123">180</span></span><br/> |
| <span data-ttu-id="e0109-124">1200</span><span class="sxs-lookup"><span data-stu-id="e0109-124">1200</span></span><br/> | <span data-ttu-id="e0109-125">Bond</span><span class="sxs-lookup"><span data-stu-id="e0109-125">Bond</span></span><br/>   | <span data-ttu-id="e0109-126">250</span><span class="sxs-lookup"><span data-stu-id="e0109-126">250</span></span><br/> |
| <span data-ttu-id="e0109-127">1200</span><span class="sxs-lookup"><span data-stu-id="e0109-127">1200</span></span><br/> | <span data-ttu-id="e0109-128">Глянцевое</span><span class="sxs-lookup"><span data-stu-id="e0109-128">Glossy</span></span><br/> | <span data-ttu-id="e0109-129">100</span><span class="sxs-lookup"><span data-stu-id="e0109-129">100</span></span><br/> |



 

<span data-ttu-id="e0109-130">В этом примере поставщик PrintCapabilities должен использовать предоставленный PrintTicket, чтобы выбрать соответствующую запись из внутренней таблицы и сообщить о том, что в качестве значения свойства Спотдиаметер.</span><span class="sxs-lookup"><span data-stu-id="e0109-130">For this example, the PrintCapabilities provider must use the provided PrintTicket to select the proper entry from the internal table and report that as the Value for the SpotDiameter Property.</span></span> <span data-ttu-id="e0109-131">Этот процесс повторяется для каждого свойства с несколькими значениями (для каждого свойства, значение которого зависит от конфигурации).</span><span class="sxs-lookup"><span data-stu-id="e0109-131">This process is repeated for every multi-valued Property (for every Property whose Value is dependent on the configuration).</span></span> <span data-ttu-id="e0109-132">В разделе [схема и построение документа PrintCapabilities](printcapabilities-schema-and-document-construction.md) описаны другие шаги, связанные с созданием моментального снимка PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="e0109-132">The [PrintCapabilities Schema and Document Construction](printcapabilities-schema-and-document-construction.md) section describes the other steps involved in creating a snapshot of the PrintCapabilities.</span></span>

<span data-ttu-id="e0109-133">Чтобы создать моментальный снимок документа PrintCapabilities по умолчанию, укажите PrintTicket по умолчанию (а не произвольный PrintTicket) для метода, который создает документы PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="e0109-133">To create a snapshot of the default PrintCapabilities document, provide a default PrintTicket (rather than an arbitrary PrintTicket) to the method that creates PrintCapabilities documents.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e0109-134">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="e0109-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0109-135">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="e0109-135">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 





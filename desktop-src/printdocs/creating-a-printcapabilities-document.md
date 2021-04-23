---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: b49e20b7-bd9e-4b8f-bb4a-bb1e99b0c417
title: Создание документа PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ccb1adf4626254ba9f71c706ad7d4556a23aeb6
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105703487"
---
# <a name="creating-a-printcapabilities-document"></a><span data-ttu-id="b9b8f-104">Создание документа PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="b9b8f-104">Creating a PrintCapabilities Document</span></span>

<span data-ttu-id="b9b8f-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="b9b8f-105">This topic is not current.</span></span> <span data-ttu-id="b9b8f-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="b9b8f-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b9b8f-107">После проверки PrintTicket можно использовать для создания моментального снимка PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="b9b8f-107">After a PrintTicket is validated, it can be used to create a snapshot of the PrintCapabilities.</span></span> <span data-ttu-id="b9b8f-108">Поставщик должен иметь внутреннее представление для любого свойства, значение которого зависит от конфигурации устройства.</span><span class="sxs-lookup"><span data-stu-id="b9b8f-108">The provider must have an internal representation for any Property whose Value is dependent on the device configuration.</span></span> <span data-ttu-id="b9b8f-109">Например, если Спотдиаметер является свойством, которое зависит от функций разрешения и MediaType, внутреннее представление Спотдиаметер, связанное с различными значениями для разрешения, и параметр MediaType может выглядеть так, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="b9b8f-109">For example, if SpotDiameter is a Property that is dependent on both the Resolution and MediaType Features, an internal representation of SpotDiameter as it relates to the various values for Resolution and MediaType might appear as in the following table:</span></span>



| <span data-ttu-id="b9b8f-110">Решение</span><span class="sxs-lookup"><span data-stu-id="b9b8f-110">Resolution</span></span>      | <span data-ttu-id="b9b8f-111">MediaType</span><span class="sxs-lookup"><span data-stu-id="b9b8f-111">MediaType</span></span>         | <span data-ttu-id="b9b8f-112">спотдиаметер</span><span class="sxs-lookup"><span data-stu-id="b9b8f-112">SpotDiameter</span></span>   |
|-----------------|-------------------|----------------|
| <span data-ttu-id="b9b8f-113">300</span><span class="sxs-lookup"><span data-stu-id="b9b8f-113">300</span></span><br/>  | <span data-ttu-id="b9b8f-114">Bond</span><span class="sxs-lookup"><span data-stu-id="b9b8f-114">Bond</span></span><br/>   | <span data-ttu-id="b9b8f-115">520</span><span class="sxs-lookup"><span data-stu-id="b9b8f-115">520</span></span><br/> |
| <span data-ttu-id="b9b8f-116">300</span><span class="sxs-lookup"><span data-stu-id="b9b8f-116">300</span></span><br/>  | <span data-ttu-id="b9b8f-117">Глянцевое</span><span class="sxs-lookup"><span data-stu-id="b9b8f-117">Glossy</span></span><br/> | <span data-ttu-id="b9b8f-118">350</span><span class="sxs-lookup"><span data-stu-id="b9b8f-118">350</span></span><br/> |
| <span data-ttu-id="b9b8f-119">600</span><span class="sxs-lookup"><span data-stu-id="b9b8f-119">600</span></span><br/>  | <span data-ttu-id="b9b8f-120">Bond</span><span class="sxs-lookup"><span data-stu-id="b9b8f-120">Bond</span></span><br/>   | <span data-ttu-id="b9b8f-121">330</span><span class="sxs-lookup"><span data-stu-id="b9b8f-121">330</span></span><br/> |
| <span data-ttu-id="b9b8f-122">600</span><span class="sxs-lookup"><span data-stu-id="b9b8f-122">600</span></span><br/>  | <span data-ttu-id="b9b8f-123">Глянцевое</span><span class="sxs-lookup"><span data-stu-id="b9b8f-123">Glossy</span></span><br/> | <span data-ttu-id="b9b8f-124">180</span><span class="sxs-lookup"><span data-stu-id="b9b8f-124">180</span></span><br/> |
| <span data-ttu-id="b9b8f-125">1200</span><span class="sxs-lookup"><span data-stu-id="b9b8f-125">1200</span></span><br/> | <span data-ttu-id="b9b8f-126">Bond</span><span class="sxs-lookup"><span data-stu-id="b9b8f-126">Bond</span></span><br/>   | <span data-ttu-id="b9b8f-127">250</span><span class="sxs-lookup"><span data-stu-id="b9b8f-127">250</span></span><br/> |
| <span data-ttu-id="b9b8f-128">1200</span><span class="sxs-lookup"><span data-stu-id="b9b8f-128">1200</span></span><br/> | <span data-ttu-id="b9b8f-129">Глянцевое</span><span class="sxs-lookup"><span data-stu-id="b9b8f-129">Glossy</span></span><br/> | <span data-ttu-id="b9b8f-130">100</span><span class="sxs-lookup"><span data-stu-id="b9b8f-130">100</span></span><br/> |



 

<span data-ttu-id="b9b8f-131">В этом примере поставщик PrintCapabilities должен использовать предоставленный PrintTicket, чтобы выбрать соответствующую запись из внутренней таблицы и сообщить о том, что в качестве значения свойства Спотдиаметер.</span><span class="sxs-lookup"><span data-stu-id="b9b8f-131">For this example, the PrintCapabilities provider must use the provided PrintTicket to select the proper entry from the internal table and report that as the Value for the SpotDiameter Property.</span></span> <span data-ttu-id="b9b8f-132">Этот процесс повторяется для каждого свойства с несколькими значениями (для каждого свойства, значение которого зависит от конфигурации).</span><span class="sxs-lookup"><span data-stu-id="b9b8f-132">This process is repeated for every multi-valued Property (for every Property whose Value is dependent on the configuration).</span></span> <span data-ttu-id="b9b8f-133">В разделе [схема и построение документа PrintCapabilities](printcapabilities-schema-and-document-construction.md) описаны другие шаги, связанные с созданием моментального снимка PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="b9b8f-133">The [PrintCapabilities Schema and Document Construction](printcapabilities-schema-and-document-construction.md) section describes the other steps involved in creating a snapshot of the PrintCapabilities.</span></span>

<span data-ttu-id="b9b8f-134">Чтобы создать моментальный снимок документа PrintCapabilities по умолчанию, укажите PrintTicket по умолчанию (а не произвольный PrintTicket) для метода, который создает документы PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="b9b8f-134">To create a snapshot of the default PrintCapabilities document, provide a default PrintTicket (rather than an arbitrary PrintTicket) to the method that creates PrintCapabilities documents.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b9b8f-135">См. также</span><span class="sxs-lookup"><span data-stu-id="b9b8f-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9b8f-136">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="b9b8f-136">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 





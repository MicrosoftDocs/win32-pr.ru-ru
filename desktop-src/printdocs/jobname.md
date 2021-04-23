---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 1e7b0681-a29b-4fd6-8518-dc9d0b716b12
title: JobName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 161801e56a27e33cdf921cc07c93e59836d4dd90
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105720059"
---
# <a name="jobname"></a><span data-ttu-id="07983-104">JobName</span><span class="sxs-lookup"><span data-stu-id="07983-104">JobName</span></span>

<span data-ttu-id="07983-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="07983-105">This topic is not current.</span></span> <span data-ttu-id="07983-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="07983-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="07983-107">Указывает описательное имя задания.</span><span class="sxs-lookup"><span data-stu-id="07983-107">Specifies a descriptive name for the job.</span></span>

-   [<span data-ttu-id="07983-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="07983-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="07983-109">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="07983-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="07983-110">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="07983-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="07983-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="07983-111">Element Information</span></span>



| <span data-ttu-id="07983-112">Имя</span><span class="sxs-lookup"><span data-stu-id="07983-112">Name</span></span>                       |                     |
|----------------------------|---------------------|
| <span data-ttu-id="07983-113">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="07983-113">Element Type</span></span> <br/>   | <span data-ttu-id="07983-114">Свойство</span><span class="sxs-lookup"><span data-stu-id="07983-114">Property</span></span><br/> |
| <span data-ttu-id="07983-115">Префикс области</span><span class="sxs-lookup"><span data-stu-id="07983-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="07983-116">Задание</span><span class="sxs-lookup"><span data-stu-id="07983-116">Job</span></span><br/>      |
| <span data-ttu-id="07983-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="07983-117">Notes</span></span> <br/>          | <span data-ttu-id="07983-118">Нет</span><span class="sxs-lookup"><span data-stu-id="07983-118">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="07983-119">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="07983-119">Structural Content</span></span>

<span data-ttu-id="07983-120">XML-структура этого элемента выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="07983-120">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:JobName">
    <psf:Value xsi:type="xs:string">_JobNameValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="07983-121">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="07983-121">Structure Variables</span></span>

<span data-ttu-id="07983-122">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="07983-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="07983-123">Имя</span><span class="sxs-lookup"><span data-stu-id="07983-123">Name</span></span>                        | <span data-ttu-id="07983-124">Тип данных</span><span class="sxs-lookup"><span data-stu-id="07983-124">Data type</span></span>         | <span data-ttu-id="07983-125">Unit</span><span class="sxs-lookup"><span data-stu-id="07983-125">Unit</span></span> | <span data-ttu-id="07983-126">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="07983-126">Supported values</span></span> | <span data-ttu-id="07983-127">Сводка</span><span class="sxs-lookup"><span data-stu-id="07983-127">Summary</span></span> |
|-----------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="07983-128">\_жобнамевалуе\_</span><span class="sxs-lookup"><span data-stu-id="07983-128">\_JobNameValue\_</span></span><br/> | <span data-ttu-id="07983-129">строка</span><span class="sxs-lookup"><span data-stu-id="07983-129">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="07983-130">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="07983-130">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:JobName">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="07983-131">См. также</span><span class="sxs-lookup"><span data-stu-id="07983-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07983-132">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="07983-132">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 





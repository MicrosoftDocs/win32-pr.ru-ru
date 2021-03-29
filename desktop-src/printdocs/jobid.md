---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 138a0ae5-160d-46f2-91ae-596d8892351a
title: JobID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c182e5d0bfcfb395eb553570cca745b618fc56b5
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105647765"
---
# <a name="jobid"></a><span data-ttu-id="b9d5b-104">JobID</span><span class="sxs-lookup"><span data-stu-id="b9d5b-104">JobID</span></span>

<span data-ttu-id="b9d5b-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="b9d5b-105">This topic is not current.</span></span> <span data-ttu-id="b9d5b-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="b9d5b-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b9d5b-107">Указывает уникальный идентификатор задания.</span><span class="sxs-lookup"><span data-stu-id="b9d5b-107">Specifies a unique ID for the job.</span></span>

-   [<span data-ttu-id="b9d5b-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="b9d5b-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="b9d5b-109">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="b9d5b-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="b9d5b-110">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="b9d5b-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="b9d5b-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="b9d5b-111">Element Information</span></span>



| <span data-ttu-id="b9d5b-112">Имя</span><span class="sxs-lookup"><span data-stu-id="b9d5b-112">Name</span></span>                       |                     |
|----------------------------|---------------------|
| <span data-ttu-id="b9d5b-113">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="b9d5b-113">Element Type</span></span> <br/>   | <span data-ttu-id="b9d5b-114">Свойство</span><span class="sxs-lookup"><span data-stu-id="b9d5b-114">Property</span></span><br/> |
| <span data-ttu-id="b9d5b-115">Префикс области</span><span class="sxs-lookup"><span data-stu-id="b9d5b-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="b9d5b-116">Задание</span><span class="sxs-lookup"><span data-stu-id="b9d5b-116">Job</span></span><br/>      |
| <span data-ttu-id="b9d5b-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="b9d5b-117">Notes</span></span> <br/>          | <span data-ttu-id="b9d5b-118">Нет</span><span class="sxs-lookup"><span data-stu-id="b9d5b-118">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="b9d5b-119">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="b9d5b-119">Structural Content</span></span>

<span data-ttu-id="b9d5b-120">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="b9d5b-120">The XML structure of this element is:</span></span>

``` syntax
<psf:Property name="psk:JobID">
    <psf:Value xsi:type="xs:string">_JobIDValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="b9d5b-121">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="b9d5b-121">Structure Variables</span></span>

<span data-ttu-id="b9d5b-122">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="b9d5b-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="b9d5b-123">Имя</span><span class="sxs-lookup"><span data-stu-id="b9d5b-123">Name</span></span>                      | <span data-ttu-id="b9d5b-124">Тип данных</span><span class="sxs-lookup"><span data-stu-id="b9d5b-124">Data type</span></span>         | <span data-ttu-id="b9d5b-125">Unit</span><span class="sxs-lookup"><span data-stu-id="b9d5b-125">Unit</span></span> | <span data-ttu-id="b9d5b-126">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="b9d5b-126">Supported values</span></span> | <span data-ttu-id="b9d5b-127">Сводка</span><span class="sxs-lookup"><span data-stu-id="b9d5b-127">Summary</span></span> |
|---------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="b9d5b-128">\_жобидвалуе\_</span><span class="sxs-lookup"><span data-stu-id="b9d5b-128">\_JobIDValue\_</span></span><br/> | <span data-ttu-id="b9d5b-129">строка</span><span class="sxs-lookup"><span data-stu-id="b9d5b-129">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="b9d5b-130">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="b9d5b-130">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:JobID">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="b9d5b-131">См. также</span><span class="sxs-lookup"><span data-stu-id="b9d5b-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9d5b-132">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="b9d5b-132">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 





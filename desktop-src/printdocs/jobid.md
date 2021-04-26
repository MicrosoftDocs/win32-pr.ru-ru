---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 138a0ae5-160d-46f2-91ae-596d8892351a
title: JobID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd2d77d185ab7edc611a82f94a2ce92428d9f167
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998141"
---
# <a name="jobid"></a><span data-ttu-id="ae44f-104">JobID</span><span class="sxs-lookup"><span data-stu-id="ae44f-104">JobID</span></span>

<span data-ttu-id="ae44f-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="ae44f-105">This topic is not current.</span></span> <span data-ttu-id="ae44f-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="ae44f-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ae44f-107">Указывает уникальный идентификатор задания.</span><span class="sxs-lookup"><span data-stu-id="ae44f-107">Specifies a unique ID for the job.</span></span>

-   [<span data-ttu-id="ae44f-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="ae44f-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="ae44f-109">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="ae44f-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="ae44f-110">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="ae44f-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="ae44f-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="ae44f-111">Element Information</span></span>



| <span data-ttu-id="ae44f-112">Имя</span><span class="sxs-lookup"><span data-stu-id="ae44f-112">Name</span></span> | <span data-ttu-id="ae44f-113">Значение</span><span class="sxs-lookup"><span data-stu-id="ae44f-113">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="ae44f-114">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="ae44f-114">Element Type</span></span> <br/>   | <span data-ttu-id="ae44f-115">Свойство</span><span class="sxs-lookup"><span data-stu-id="ae44f-115">Property</span></span><br/> |
| <span data-ttu-id="ae44f-116">Префикс области</span><span class="sxs-lookup"><span data-stu-id="ae44f-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="ae44f-117">Задание</span><span class="sxs-lookup"><span data-stu-id="ae44f-117">Job</span></span><br/>      |
| <span data-ttu-id="ae44f-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="ae44f-118">Notes</span></span> <br/>          | <span data-ttu-id="ae44f-119">Нет</span><span class="sxs-lookup"><span data-stu-id="ae44f-119">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="ae44f-120">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="ae44f-120">Structural Content</span></span>

<span data-ttu-id="ae44f-121">XML-структура этого элемента:</span><span class="sxs-lookup"><span data-stu-id="ae44f-121">The XML structure of this element is:</span></span>

``` syntax
<psf:Property name="psk:JobID">
    <psf:Value xsi:type="xs:string">_JobIDValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="ae44f-122">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="ae44f-122">Structure Variables</span></span>

<span data-ttu-id="ae44f-123">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="ae44f-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="ae44f-124">Имя</span><span class="sxs-lookup"><span data-stu-id="ae44f-124">Name</span></span>                      | <span data-ttu-id="ae44f-125">Тип данных</span><span class="sxs-lookup"><span data-stu-id="ae44f-125">Data type</span></span>         | <span data-ttu-id="ae44f-126">Unit</span><span class="sxs-lookup"><span data-stu-id="ae44f-126">Unit</span></span> | <span data-ttu-id="ae44f-127">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="ae44f-127">Supported values</span></span> | <span data-ttu-id="ae44f-128">Сводка</span><span class="sxs-lookup"><span data-stu-id="ae44f-128">Summary</span></span> |
|---------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="ae44f-129">\_жобидвалуе\_</span><span class="sxs-lookup"><span data-stu-id="ae44f-129">\_JobIDValue\_</span></span><br/> | <span data-ttu-id="ae44f-130">строка</span><span class="sxs-lookup"><span data-stu-id="ae44f-130">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="ae44f-131">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="ae44f-131">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:JobID">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="ae44f-132">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="ae44f-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae44f-133">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="ae44f-133">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 





---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 1e7b0681-a29b-4fd6-8518-dc9d0b716b12
title: JobName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcb6259d8623a4611364023bf0f74784fe308b58
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998111"
---
# <a name="jobname"></a><span data-ttu-id="0a80c-104">JobName</span><span class="sxs-lookup"><span data-stu-id="0a80c-104">JobName</span></span>

<span data-ttu-id="0a80c-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="0a80c-105">This topic is not current.</span></span> <span data-ttu-id="0a80c-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="0a80c-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="0a80c-107">Указывает описательное имя задания.</span><span class="sxs-lookup"><span data-stu-id="0a80c-107">Specifies a descriptive name for the job.</span></span>

-   [<span data-ttu-id="0a80c-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="0a80c-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="0a80c-109">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="0a80c-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="0a80c-110">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="0a80c-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="0a80c-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="0a80c-111">Element Information</span></span>



| <span data-ttu-id="0a80c-112">Имя</span><span class="sxs-lookup"><span data-stu-id="0a80c-112">Name</span></span> | <span data-ttu-id="0a80c-113">Значение</span><span class="sxs-lookup"><span data-stu-id="0a80c-113">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="0a80c-114">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="0a80c-114">Element Type</span></span> <br/>   | <span data-ttu-id="0a80c-115">Свойство</span><span class="sxs-lookup"><span data-stu-id="0a80c-115">Property</span></span><br/> |
| <span data-ttu-id="0a80c-116">Префикс области</span><span class="sxs-lookup"><span data-stu-id="0a80c-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="0a80c-117">Задание</span><span class="sxs-lookup"><span data-stu-id="0a80c-117">Job</span></span><br/>      |
| <span data-ttu-id="0a80c-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="0a80c-118">Notes</span></span> <br/>          | <span data-ttu-id="0a80c-119">Нет</span><span class="sxs-lookup"><span data-stu-id="0a80c-119">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="0a80c-120">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="0a80c-120">Structural Content</span></span>

<span data-ttu-id="0a80c-121">XML-структура этого элемента выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="0a80c-121">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:JobName">
    <psf:Value xsi:type="xs:string">_JobNameValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="0a80c-122">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="0a80c-122">Structure Variables</span></span>

<span data-ttu-id="0a80c-123">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="0a80c-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="0a80c-124">Имя</span><span class="sxs-lookup"><span data-stu-id="0a80c-124">Name</span></span>                        | <span data-ttu-id="0a80c-125">Тип данных</span><span class="sxs-lookup"><span data-stu-id="0a80c-125">Data type</span></span>         | <span data-ttu-id="0a80c-126">Unit</span><span class="sxs-lookup"><span data-stu-id="0a80c-126">Unit</span></span> | <span data-ttu-id="0a80c-127">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="0a80c-127">Supported values</span></span> | <span data-ttu-id="0a80c-128">Сводка</span><span class="sxs-lookup"><span data-stu-id="0a80c-128">Summary</span></span> |
|-----------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="0a80c-129">\_жобнамевалуе\_</span><span class="sxs-lookup"><span data-stu-id="0a80c-129">\_JobNameValue\_</span></span><br/> | <span data-ttu-id="0a80c-130">строка</span><span class="sxs-lookup"><span data-stu-id="0a80c-130">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="0a80c-131">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="0a80c-131">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:JobName">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="0a80c-132">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="0a80c-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a80c-133">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="0a80c-133">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 





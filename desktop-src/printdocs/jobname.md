---
description: Сведения об элементе JobName, который указывает описательное имя задания. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 1e7b0681-a29b-4fd6-8518-dc9d0b716b12
title: JobName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bfb63a54e9501ff5dc45ff09a925396c168b20c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408877"
---
# <a name="jobname"></a><span data-ttu-id="63bdd-104">JobName</span><span class="sxs-lookup"><span data-stu-id="63bdd-104">JobName</span></span>

<span data-ttu-id="63bdd-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="63bdd-105">This topic is not current.</span></span> <span data-ttu-id="63bdd-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="63bdd-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="63bdd-107">Указывает описательное имя задания.</span><span class="sxs-lookup"><span data-stu-id="63bdd-107">Specifies a descriptive name for the job.</span></span>

-   [<span data-ttu-id="63bdd-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="63bdd-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="63bdd-109">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="63bdd-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="63bdd-110">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="63bdd-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="63bdd-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="63bdd-111">Element Information</span></span>



| <span data-ttu-id="63bdd-112">Имя</span><span class="sxs-lookup"><span data-stu-id="63bdd-112">Name</span></span> | <span data-ttu-id="63bdd-113">Значение</span><span class="sxs-lookup"><span data-stu-id="63bdd-113">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="63bdd-114">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="63bdd-114">Element Type</span></span> <br/>   | <span data-ttu-id="63bdd-115">Свойство</span><span class="sxs-lookup"><span data-stu-id="63bdd-115">Property</span></span><br/> |
| <span data-ttu-id="63bdd-116">Префикс области</span><span class="sxs-lookup"><span data-stu-id="63bdd-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="63bdd-117">Задание</span><span class="sxs-lookup"><span data-stu-id="63bdd-117">Job</span></span><br/>      |
| <span data-ttu-id="63bdd-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="63bdd-118">Notes</span></span> <br/>          | <span data-ttu-id="63bdd-119">Нет</span><span class="sxs-lookup"><span data-stu-id="63bdd-119">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="63bdd-120">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="63bdd-120">Structural Content</span></span>

<span data-ttu-id="63bdd-121">XML-структура этого элемента выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="63bdd-121">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:JobName">
    <psf:Value xsi:type="xs:string">_JobNameValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="63bdd-122">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="63bdd-122">Structure Variables</span></span>

<span data-ttu-id="63bdd-123">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="63bdd-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="63bdd-124">Имя</span><span class="sxs-lookup"><span data-stu-id="63bdd-124">Name</span></span>                        | <span data-ttu-id="63bdd-125">Тип данных</span><span class="sxs-lookup"><span data-stu-id="63bdd-125">Data type</span></span>         | <span data-ttu-id="63bdd-126">Unit</span><span class="sxs-lookup"><span data-stu-id="63bdd-126">Unit</span></span> | <span data-ttu-id="63bdd-127">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="63bdd-127">Supported values</span></span> | <span data-ttu-id="63bdd-128">Итоги</span><span class="sxs-lookup"><span data-stu-id="63bdd-128">Summary</span></span> |
|-----------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="63bdd-129">\_жобнамевалуе\_</span><span class="sxs-lookup"><span data-stu-id="63bdd-129">\_JobNameValue\_</span></span><br/> | <span data-ttu-id="63bdd-130">строка</span><span class="sxs-lookup"><span data-stu-id="63bdd-130">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="63bdd-131">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="63bdd-131">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:JobName">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="63bdd-132">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="63bdd-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63bdd-133">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="63bdd-133">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 





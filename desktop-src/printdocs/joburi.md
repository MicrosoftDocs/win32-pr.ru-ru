---
description: Сведения об элементе Жобури, который указывает универсальный код ресурса (URI) для документа.
ms.assetid: c7abb657-6c9d-435a-a700-2eb0f14707c0
title: жобури
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecc145ac9a393c09ecab762b84e9ac7d58870ddf
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408617"
---
# <a name="joburi"></a><span data-ttu-id="c16c7-103">жобури</span><span class="sxs-lookup"><span data-stu-id="c16c7-103">JobURI</span></span>

<span data-ttu-id="c16c7-104">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="c16c7-104">This topic is not current.</span></span> <span data-ttu-id="c16c7-105">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="c16c7-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c16c7-106">Задает универсальный код ресурса (URI) для документа.</span><span class="sxs-lookup"><span data-stu-id="c16c7-106">Specifies a uniform resource identifier (URI) for the document.</span></span>

-   [<span data-ttu-id="c16c7-107">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="c16c7-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c16c7-108">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="c16c7-108">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="c16c7-109">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="c16c7-109">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="c16c7-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="c16c7-110">Element Information</span></span>



| <span data-ttu-id="c16c7-111">Имя</span><span class="sxs-lookup"><span data-stu-id="c16c7-111">Name</span></span> | <span data-ttu-id="c16c7-112">Значение</span><span class="sxs-lookup"><span data-stu-id="c16c7-112">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="c16c7-113">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="c16c7-113">Element Type</span></span> <br/>   | <span data-ttu-id="c16c7-114">Свойство</span><span class="sxs-lookup"><span data-stu-id="c16c7-114">Property</span></span><br/> |
| <span data-ttu-id="c16c7-115">Префикс области</span><span class="sxs-lookup"><span data-stu-id="c16c7-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="c16c7-116">Задание</span><span class="sxs-lookup"><span data-stu-id="c16c7-116">Job</span></span><br/>      |
| <span data-ttu-id="c16c7-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="c16c7-117">Notes</span></span> <br/>          | <span data-ttu-id="c16c7-118">Нет</span><span class="sxs-lookup"><span data-stu-id="c16c7-118">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="c16c7-119">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="c16c7-119">Structural Content</span></span>

<span data-ttu-id="c16c7-120">XML-структура этого элемента выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c16c7-120">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:JobURI">
    <psf:Value xsi:type="xs:string">_JobURIValue_</psf:Value>
</psf:Property>
      
```

## <a name="structure-variables"></a><span data-ttu-id="c16c7-121">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="c16c7-121">Structure Variables</span></span>

<span data-ttu-id="c16c7-122">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="c16c7-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="c16c7-123">Имя</span><span class="sxs-lookup"><span data-stu-id="c16c7-123">Name</span></span>                       | <span data-ttu-id="c16c7-124">Тип данных</span><span class="sxs-lookup"><span data-stu-id="c16c7-124">Data type</span></span>         | <span data-ttu-id="c16c7-125">Unit</span><span class="sxs-lookup"><span data-stu-id="c16c7-125">Unit</span></span> | <span data-ttu-id="c16c7-126">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="c16c7-126">Supported values</span></span> | <span data-ttu-id="c16c7-127">Итоги</span><span class="sxs-lookup"><span data-stu-id="c16c7-127">Summary</span></span> |
|----------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="c16c7-128">\_жобуривалуе\_</span><span class="sxs-lookup"><span data-stu-id="c16c7-128">\_JobURIValue\_</span></span><br/> | <span data-ttu-id="c16c7-129">строка</span><span class="sxs-lookup"><span data-stu-id="c16c7-129">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="c16c7-130">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="c16c7-130">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:JobURI">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="c16c7-131">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="c16c7-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c16c7-132">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="c16c7-132">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 





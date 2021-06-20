---
description: Сведения об элементе DocumentID, который указывает уникальный идентификатор для документа. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 6e7899e3-9b64-48bd-8683-aba627458f2a
title: DocumentID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b267fead0322351cde396bf2eb6d0efa8c523f0
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409288"
---
# <a name="documentid"></a><span data-ttu-id="eff3b-104">DocumentID</span><span class="sxs-lookup"><span data-stu-id="eff3b-104">DocumentID</span></span>

<span data-ttu-id="eff3b-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="eff3b-105">This topic is not current.</span></span> <span data-ttu-id="eff3b-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="eff3b-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="eff3b-107">Указывает уникальный идентификатор документа.</span><span class="sxs-lookup"><span data-stu-id="eff3b-107">Specifies a unique ID for the document.</span></span>

-   [<span data-ttu-id="eff3b-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="eff3b-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="eff3b-109">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="eff3b-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="eff3b-110">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="eff3b-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="eff3b-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="eff3b-111">Element Information</span></span>



| <span data-ttu-id="eff3b-112">Имя</span><span class="sxs-lookup"><span data-stu-id="eff3b-112">Name</span></span> | <span data-ttu-id="eff3b-113">Значение</span><span class="sxs-lookup"><span data-stu-id="eff3b-113">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="eff3b-114">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="eff3b-114">Element Type</span></span> <br/>   | <span data-ttu-id="eff3b-115">Свойство</span><span class="sxs-lookup"><span data-stu-id="eff3b-115">Property</span></span><br/> |
| <span data-ttu-id="eff3b-116">Префикс области</span><span class="sxs-lookup"><span data-stu-id="eff3b-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="eff3b-117">Документ</span><span class="sxs-lookup"><span data-stu-id="eff3b-117">Document</span></span><br/> |
| <span data-ttu-id="eff3b-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="eff3b-118">Notes</span></span> <br/>          | <span data-ttu-id="eff3b-119">Нет</span><span class="sxs-lookup"><span data-stu-id="eff3b-119">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="eff3b-120">Структурное содержимое</span><span class="sxs-lookup"><span data-stu-id="eff3b-120">Structural Content</span></span>

<span data-ttu-id="eff3b-121">XML-структура этого элемента выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="eff3b-121">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Property name="psk:DocumentID">
    <psf:Value xsi:type="xs:string">_DocumentIDValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="eff3b-122">Переменные структуры</span><span class="sxs-lookup"><span data-stu-id="eff3b-122">Structure Variables</span></span>

<span data-ttu-id="eff3b-123">В следующей таблице описаны характеристики переменных, определенных в структуре XML.</span><span class="sxs-lookup"><span data-stu-id="eff3b-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="eff3b-124">Имя</span><span class="sxs-lookup"><span data-stu-id="eff3b-124">Name</span></span>                           | <span data-ttu-id="eff3b-125">Тип данных</span><span class="sxs-lookup"><span data-stu-id="eff3b-125">Data type</span></span>         | <span data-ttu-id="eff3b-126">Unit</span><span class="sxs-lookup"><span data-stu-id="eff3b-126">Unit</span></span> | <span data-ttu-id="eff3b-127">Поддерживаемые значения</span><span class="sxs-lookup"><span data-stu-id="eff3b-127">Supported values</span></span> | <span data-ttu-id="eff3b-128">Итоги</span><span class="sxs-lookup"><span data-stu-id="eff3b-128">Summary</span></span> |
|--------------------------------|-------------------|------|------------------|---------|
| <span data-ttu-id="eff3b-129">\_документидвалуе\_</span><span class="sxs-lookup"><span data-stu-id="eff3b-129">\_DocumentIDValue\_</span></span><br/> | <span data-ttu-id="eff3b-130">строка</span><span class="sxs-lookup"><span data-stu-id="eff3b-130">string</span></span><br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="eff3b-131">Содержимое язык XML (XML)</span><span class="sxs-lookup"><span data-stu-id="eff3b-131">Extensible Markup Language (XML) Content</span></span>

``` syntax
<psf:Property name="psk:DocumentID">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a><span data-ttu-id="eff3b-132">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="eff3b-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eff3b-133">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="eff3b-133">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 





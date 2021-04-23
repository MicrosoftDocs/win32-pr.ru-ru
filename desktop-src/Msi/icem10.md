---
description: ICEM10 проверяет, что модуль слияния содержит только те свойства, которые разрешены в таблице свойств.
ms.assetid: 9ac7a724-ea0e-4caa-bb4f-846bfb802037
title: ICEM10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80263e5033ec14bd669c5d046c7f3842d58e332f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650973"
---
# <a name="icem10"></a><span data-ttu-id="ef930-103">ICEM10</span><span class="sxs-lookup"><span data-stu-id="ef930-103">ICEM10</span></span>

<span data-ttu-id="ef930-104">ICEM10 проверяет, что модуль слияния содержит только те свойства, которые разрешены в [таблице свойств](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="ef930-104">ICEM10 verifies that a merge module contains only properties that are allowed in the [Property Table](property-table.md).</span></span> <span data-ttu-id="ef930-105">Следующие свойства продукта не допускаются в таблице свойств:</span><span class="sxs-lookup"><span data-stu-id="ef930-105">The following product specific properties are not allowed in the Property Table:</span></span>

-   [<span data-ttu-id="ef930-106">**Продуктлангуаже, свойство**</span><span class="sxs-lookup"><span data-stu-id="ef930-106">**ProductLanguage Property**</span></span>](productlanguage.md)
-   [<span data-ttu-id="ef930-107">**ProductCode, свойство**</span><span class="sxs-lookup"><span data-stu-id="ef930-107">**ProductCode Property**</span></span>](productcode.md)
-   [<span data-ttu-id="ef930-108">**ProductVersion, свойство**</span><span class="sxs-lookup"><span data-stu-id="ef930-108">**ProductVersion Property**</span></span>](productversion.md)
-   [<span data-ttu-id="ef930-109">**Свойство ProductName**</span><span class="sxs-lookup"><span data-stu-id="ef930-109">**ProductName Property**</span></span>](productname.md)
-   [<span data-ttu-id="ef930-110">**Свойство Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="ef930-110">**Manufacturer Property**</span></span>](manufacturer.md)

## <a name="result"></a><span data-ttu-id="ef930-111">Результат</span><span class="sxs-lookup"><span data-stu-id="ef930-111">Result</span></span>

<span data-ttu-id="ef930-112">ICEM10 отправляет сообщение об ошибке, если модуль слияния содержит свойство, недопустимое в [таблице свойств](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="ef930-112">ICEM10 posts an error when a merge module contains a property that is not allowed in the [Property Table](property-table.md).</span></span>

## <a name="example"></a><span data-ttu-id="ef930-113">Пример</span><span class="sxs-lookup"><span data-stu-id="ef930-113">Example</span></span>

<span data-ttu-id="ef930-114">ICEM10 отправляет следующие сообщения об ошибках для модуля, содержащего отображаемые записи базы данных.</span><span class="sxs-lookup"><span data-stu-id="ef930-114">ICEM10 posts the following error messages for a module that contains the database entries shown.</span></span>

``` syntax
The property 'ProductLanguage' is not allowed in a merge module.

The property 'Manufacturer' is not allowed in a merge module.
```

<span data-ttu-id="ef930-115">В следующей таблице показана таблица с частичным [свойством](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="ef930-115">The following table shows you a partial [Property Table](property-table.md).</span></span>



| <span data-ttu-id="ef930-116">Свойство</span><span class="sxs-lookup"><span data-stu-id="ef930-116">Property</span></span>                                   | <span data-ttu-id="ef930-117">Значения</span><span class="sxs-lookup"><span data-stu-id="ef930-117">Values</span></span>    |
|--------------------------------------------|-----------|
| <span data-ttu-id="ef930-118">Цвет</span><span class="sxs-lookup"><span data-stu-id="ef930-118">Color</span></span>                                      | <span data-ttu-id="ef930-119">Красный</span><span class="sxs-lookup"><span data-stu-id="ef930-119">Red</span></span>       |
| [<span data-ttu-id="ef930-120">**Производителя**</span><span class="sxs-lookup"><span data-stu-id="ef930-120">**Manufacturer**</span></span>](manufacturer.md)       | <span data-ttu-id="ef930-121">Microsoft</span><span class="sxs-lookup"><span data-stu-id="ef930-121">Microsoft</span></span> |
| [<span data-ttu-id="ef930-122">**продуктлангуаже**</span><span class="sxs-lookup"><span data-stu-id="ef930-122">**ProductLanguage**</span></span>](productlanguage.md) | <span data-ttu-id="ef930-123">1033</span><span class="sxs-lookup"><span data-stu-id="ef930-123">1033</span></span>      |



 

<span data-ttu-id="ef930-124">В следующей процедуре показано, как исправить ошибки.</span><span class="sxs-lookup"><span data-stu-id="ef930-124">The following procedure shows you how to fix errors.</span></span>

<span data-ttu-id="ef930-125">**Исправление ошибок**</span><span class="sxs-lookup"><span data-stu-id="ef930-125">**To fix the errors**</span></span>

1.  <span data-ttu-id="ef930-126">Удалите свойство [**Manufacturer**](manufacturer.md)из [таблицы свойств](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="ef930-126">Remove the '[**Manufacturer**](manufacturer.md)' property from the [Property Table](property-table.md).</span></span>
2.  <span data-ttu-id="ef930-127">Удалите свойство "[**продуктлангуаже**](productlanguage.md)" из [таблицы свойств](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="ef930-127">Remove the '[**ProductLanguage**](productlanguage.md)' property from the [Property Table](property-table.md).</span></span>

## <a name="table-used-during-execution"></a><span data-ttu-id="ef930-128">Таблица, используемая во время выполнения</span><span class="sxs-lookup"><span data-stu-id="ef930-128">Table Used During Execution</span></span>

<span data-ttu-id="ef930-129">[Таблица свойств](property-table.md) используется во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="ef930-129">The [Property Table](property-table.md) is used during execution.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ef930-130">См. также</span><span class="sxs-lookup"><span data-stu-id="ef930-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef930-131">Ссылка на модуль слияния ICE</span><span class="sxs-lookup"><span data-stu-id="ef930-131">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 




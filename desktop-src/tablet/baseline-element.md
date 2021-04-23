---
description: Предоставляет сведения (x, y) для начальной и конечной точек базового плана абзаца в документе журнала. Координатное пространство, используемое для этих значений, — HIMETRIC.
ms.assetid: ff6a97ad-0e48-4128-8f94-24802b6ddc05
title: Базовый элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b64986707eaa1b382d2f88851367b9147c59c5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262859"
---
# <a name="baseline-element"></a><span data-ttu-id="10c0d-104">Базовый элемент</span><span class="sxs-lookup"><span data-stu-id="10c0d-104">Baseline Element</span></span>

<span data-ttu-id="10c0d-105">Предоставляет сведения (x, y) для начальной и конечной точек базового плана абзаца в документе журнала.</span><span class="sxs-lookup"><span data-stu-id="10c0d-105">Provides (x, y) information for the starting and ending points of the baseline of a paragraph in the Journal document.</span></span> <span data-ttu-id="10c0d-106">Координатное пространство, используемое для этих значений, — **HIMETRIC**.</span><span class="sxs-lookup"><span data-stu-id="10c0d-106">The coordinate space used for these values is **HIMETRIC**.</span></span>

## <a name="definition"></a><span data-ttu-id="10c0d-107">Определение</span><span class="sxs-lookup"><span data-stu-id="10c0d-107">Definition</span></span>

``` syntax
<xs:element name="Baseline" type="BaseLineType" />
```

## <a name="parent-elements"></a><span data-ttu-id="10c0d-108">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="10c0d-108">Parent Elements</span></span>

[<span data-ttu-id="10c0d-109">**параграфлинеметрикс**</span><span class="sxs-lookup"><span data-stu-id="10c0d-109">**ParagraphLineMetrics**</span></span>](paragraphlinemetrics-element.md)

## <a name="child-elements"></a><span data-ttu-id="10c0d-110">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="10c0d-110">Child Elements</span></span>

<span data-ttu-id="10c0d-111">Отсутствует.</span><span class="sxs-lookup"><span data-stu-id="10c0d-111">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="10c0d-112">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="10c0d-112">Attributes</span></span>



| <span data-ttu-id="10c0d-113">attribute</span><span class="sxs-lookup"><span data-stu-id="10c0d-113">Attribute</span></span>  | <span data-ttu-id="10c0d-114">Тип</span><span class="sxs-lookup"><span data-stu-id="10c0d-114">Type</span></span>                      | <span data-ttu-id="10c0d-115">Обязательно</span><span class="sxs-lookup"><span data-stu-id="10c0d-115">Required</span></span> | <span data-ttu-id="10c0d-116">Описание</span><span class="sxs-lookup"><span data-stu-id="10c0d-116">Description</span></span>                                                      | <span data-ttu-id="10c0d-117">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="10c0d-117">Possible Values</span></span>           |
|------------|---------------------------|----------|------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="10c0d-118">**старткс**</span><span class="sxs-lookup"><span data-stu-id="10c0d-118">**StartX**</span></span> | <span data-ttu-id="10c0d-119">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="10c0d-119">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="10c0d-120">Обязательно</span><span class="sxs-lookup"><span data-stu-id="10c0d-120">Required</span></span> | <span data-ttu-id="10c0d-121">Значение X для точки, помечающая начало базовых показателей.</span><span class="sxs-lookup"><span data-stu-id="10c0d-121">The X value for the point marking the beginning of the baseline.</span></span> | <span data-ttu-id="10c0d-122">Любое неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="10c0d-122">Any non-negative integer.</span></span> |
| <span data-ttu-id="10c0d-123">**Запуск**</span><span class="sxs-lookup"><span data-stu-id="10c0d-123">**StartY**</span></span> | <span data-ttu-id="10c0d-124">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="10c0d-124">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="10c0d-125">Обязательно</span><span class="sxs-lookup"><span data-stu-id="10c0d-125">Required</span></span> | <span data-ttu-id="10c0d-126">Значение Y для точки, помечающая начало базовых показателей.</span><span class="sxs-lookup"><span data-stu-id="10c0d-126">The Y value for the point marking the beginning of the baseline.</span></span> | <span data-ttu-id="10c0d-127">Любое неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="10c0d-127">Any non-negative integer.</span></span> |
| <span data-ttu-id="10c0d-128">**ендкс**</span><span class="sxs-lookup"><span data-stu-id="10c0d-128">**EndX**</span></span>   | <span data-ttu-id="10c0d-129">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="10c0d-129">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="10c0d-130">Обязательно</span><span class="sxs-lookup"><span data-stu-id="10c0d-130">Required</span></span> | <span data-ttu-id="10c0d-131">Значение X для точки, помечающая конец базового плана.</span><span class="sxs-lookup"><span data-stu-id="10c0d-131">The X value for the point marking the end of the baseline.</span></span>       | <span data-ttu-id="10c0d-132">Любое неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="10c0d-132">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="10c0d-133">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="10c0d-133">Element Information</span></span>



|              |                                                               |
|--------------|---------------------------------------------------------------|
| <span data-ttu-id="10c0d-134">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="10c0d-134">Element type</span></span> | <span data-ttu-id="10c0d-135">[**BaselineType**](baselinetype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="10c0d-135">[**BaselineType**](baselinetype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="10c0d-136">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="10c0d-136">Namespace</span></span>    | <span data-ttu-id="10c0d-137">urn: schemas-microsoft-com: TabletPC: ричинк</span><span class="sxs-lookup"><span data-stu-id="10c0d-137">urn:schemas-microsoft-com:tabletpc:richink</span></span>                    |
| <span data-ttu-id="10c0d-138">Имя схемы</span><span class="sxs-lookup"><span data-stu-id="10c0d-138">Schema name</span></span>  | <span data-ttu-id="10c0d-139">Средство чтения журнала</span><span class="sxs-lookup"><span data-stu-id="10c0d-139">Journal Reader</span></span>                                                |



 

 

 




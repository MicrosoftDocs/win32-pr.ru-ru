---
description: В таблице Феатурекомпонентс определяется связь между компонентами и компонентами. Для каждого компонента в этой таблице перечислены все компоненты, составляющие эту функцию.
ms.assetid: aff16483-a9ed-4675-8e87-8adf695605ee
title: Таблица Феатурекомпонентс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6c93a7c020f179843916b063b48e2e4d19f7bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811819"
---
# <a name="featurecomponents-table"></a><span data-ttu-id="913c6-104">Таблица Феатурекомпонентс</span><span class="sxs-lookup"><span data-stu-id="913c6-104">FeatureComponents Table</span></span>

<span data-ttu-id="913c6-105">В таблице Феатурекомпонентс определяется связь между компонентами и компонентами.</span><span class="sxs-lookup"><span data-stu-id="913c6-105">The FeatureComponents table defines the relationship between features and components.</span></span> <span data-ttu-id="913c6-106">Для каждого компонента в этой таблице перечислены все компоненты, составляющие эту функцию.</span><span class="sxs-lookup"><span data-stu-id="913c6-106">For each feature, this table lists all the components that make up that feature.</span></span>

<span data-ttu-id="913c6-107">Таблица Феатурекомпонентс содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="913c6-107">The FeatureComponents table has the following columns.</span></span>



| <span data-ttu-id="913c6-108">Столбец</span><span class="sxs-lookup"><span data-stu-id="913c6-108">Column</span></span>      | <span data-ttu-id="913c6-109">Type</span><span class="sxs-lookup"><span data-stu-id="913c6-109">Type</span></span>                         | <span data-ttu-id="913c6-110">Ключ</span><span class="sxs-lookup"><span data-stu-id="913c6-110">Key</span></span> | <span data-ttu-id="913c6-111">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="913c6-111">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="913c6-112">Функция\_</span><span class="sxs-lookup"><span data-stu-id="913c6-112">Feature\_</span></span>   | [<span data-ttu-id="913c6-113">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="913c6-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="913c6-114">Да</span><span class="sxs-lookup"><span data-stu-id="913c6-114">Y</span></span>   | <span data-ttu-id="913c6-115">Нет</span><span class="sxs-lookup"><span data-stu-id="913c6-115">N</span></span>        |
| <span data-ttu-id="913c6-116">Компонент\_</span><span class="sxs-lookup"><span data-stu-id="913c6-116">Component\_</span></span> | [<span data-ttu-id="913c6-117">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="913c6-117">Identifier</span></span>](identifier.md) | <span data-ttu-id="913c6-118">Да</span><span class="sxs-lookup"><span data-stu-id="913c6-118">Y</span></span>   | <span data-ttu-id="913c6-119">Нет</span><span class="sxs-lookup"><span data-stu-id="913c6-119">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="913c6-120">Столбцы</span><span class="sxs-lookup"><span data-stu-id="913c6-120">Columns</span></span>

<dl> <dt>

<span data-ttu-id="913c6-121"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Функциями\_</span><span class="sxs-lookup"><span data-stu-id="913c6-121"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Feature\_</span></span>
</dt> <dd>

<span data-ttu-id="913c6-122">Внешний ключ в первом столбце [таблицы](feature-table.md)Feature.</span><span class="sxs-lookup"><span data-stu-id="913c6-122">An external key into the first column of the Feature [table](feature-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="913c6-123"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>См\_</span><span class="sxs-lookup"><span data-stu-id="913c6-123"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="913c6-124">Внешний ключ в первом столбце [таблицы Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="913c6-124">An external key into the first column of the [Component table](component-table.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="913c6-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="913c6-125">Remarks</span></span>

<span data-ttu-id="913c6-126">Максимальное число компонентов для каждого компонента — 1600.</span><span class="sxs-lookup"><span data-stu-id="913c6-126">There is a maximum limit of 1600 components per feature.</span></span>

<span data-ttu-id="913c6-127">Компоненты могут совместно использоваться двумя или более компонентами, то есть один и тот же компонент может ссылаться более чем на одну функцию.</span><span class="sxs-lookup"><span data-stu-id="913c6-127">Components can be shared by two or more features, that is, the same component can be referred to by more than one feature.</span></span>

<span data-ttu-id="913c6-128">Эта таблица упоминается при выполнении [действия публишфеатурес](publishfeatures-action.md) или [унпублишфеатурес](unpublishfeatures-action.md) .</span><span class="sxs-lookup"><span data-stu-id="913c6-128">This table is referred to when the [PublishFeatures action](publishfeatures-action.md) or the [UnpublishFeatures action](unpublishfeatures-action.md) is executed.</span></span>

## <a name="validation"></a><span data-ttu-id="913c6-129">Проверка</span><span class="sxs-lookup"><span data-stu-id="913c6-129">Validation</span></span>

<dl>

[<span data-ttu-id="913c6-130">ICE03</span><span class="sxs-lookup"><span data-stu-id="913c6-130">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="913c6-131">ICE06</span><span class="sxs-lookup"><span data-stu-id="913c6-131">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="913c6-132">ICE21</span><span class="sxs-lookup"><span data-stu-id="913c6-132">ICE21</span></span>](ice21.md)  
[<span data-ttu-id="913c6-133">ICE22</span><span class="sxs-lookup"><span data-stu-id="913c6-133">ICE22</span></span>](ice22.md)  
[<span data-ttu-id="913c6-134">ICE32</span><span class="sxs-lookup"><span data-stu-id="913c6-134">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="913c6-135">ICE41</span><span class="sxs-lookup"><span data-stu-id="913c6-135">ICE41</span></span>](ice41.md)  
[<span data-ttu-id="913c6-136">ICE47</span><span class="sxs-lookup"><span data-stu-id="913c6-136">ICE47</span></span>](ice47.md)  
[<span data-ttu-id="913c6-137">ICE59</span><span class="sxs-lookup"><span data-stu-id="913c6-137">ICE59</span></span>](ice59.md)  
[<span data-ttu-id="913c6-138">ICE62</span><span class="sxs-lookup"><span data-stu-id="913c6-138">ICE62</span></span>](ice62.md)  
[<span data-ttu-id="913c6-139">ICE69</span><span class="sxs-lookup"><span data-stu-id="913c6-139">ICE69</span></span>](ice69.md)  
</dl>

 

 




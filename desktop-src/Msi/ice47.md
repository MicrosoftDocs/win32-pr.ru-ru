---
description: ICE47 проверяет таблицы функций и Феатурекомпонентс для функций с 1600 или более компонентами.
ms.assetid: e3101569-4d0b-48c9-8ba2-6f0de0c39e74
title: ICE47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baa04c2df52571f56612242d2dc7da8b5a91647c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264391"
---
# <a name="ice47"></a><span data-ttu-id="78d81-103">ICE47</span><span class="sxs-lookup"><span data-stu-id="78d81-103">ICE47</span></span>

<span data-ttu-id="78d81-104">ICE47 проверяет таблицы [функций](feature-table.md) и [феатурекомпонентс](featurecomponents-table.md) для функций с 1600 или более компонентами.</span><span class="sxs-lookup"><span data-stu-id="78d81-104">ICE47 checks the [Feature](feature-table.md) and [FeatureComponents](featurecomponents-table.md) tables for features with 1600 or more components.</span></span>

## <a name="result"></a><span data-ttu-id="78d81-105">Результат</span><span class="sxs-lookup"><span data-stu-id="78d81-105">Result</span></span>

<span data-ttu-id="78d81-106">ICE47 отправляет сообщение об ошибке, если компонент превышает максимальное ограничение в 1600 компонентов на компонент.</span><span class="sxs-lookup"><span data-stu-id="78d81-106">ICE47 posts an error message if a feature exceeds the maximum limit of 1600 components per feature.</span></span>

## <a name="example"></a><span data-ttu-id="78d81-107">Пример</span><span class="sxs-lookup"><span data-stu-id="78d81-107">Example</span></span>

<span data-ttu-id="78d81-108">ICE47 сообщит о следующем предупреждении:</span><span class="sxs-lookup"><span data-stu-id="78d81-108">ICE47 would report the following warning:</span></span>

``` syntax
Feature 'Feature1' has 1600 components. This could cause 
    problems on Win9X systems. You should try to have less 
    than 800 components per feature."
```

<span data-ttu-id="78d81-109">[Таблица компонентов](feature-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="78d81-109">[Feature Table](feature-table.md) (partial)</span></span>



| <span data-ttu-id="78d81-110">Функция</span><span class="sxs-lookup"><span data-stu-id="78d81-110">Feature</span></span>  |
|----------|
| <span data-ttu-id="78d81-111">Feature1</span><span class="sxs-lookup"><span data-stu-id="78d81-111">Feature1</span></span> |



 

<span data-ttu-id="78d81-112">[Таблица феатурекомпонентс](featurecomponents-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="78d81-112">[FeatureComponents Table](featurecomponents-table.md) (partial)</span></span>



| <span data-ttu-id="78d81-113">Действие</span><span class="sxs-lookup"><span data-stu-id="78d81-113">Action</span></span>   | <span data-ttu-id="78d81-114">Условие</span><span class="sxs-lookup"><span data-stu-id="78d81-114">Condition</span></span>     |
|----------|---------------|
| <span data-ttu-id="78d81-115">Feature1</span><span class="sxs-lookup"><span data-stu-id="78d81-115">Feature1</span></span> | <span data-ttu-id="78d81-116">Component1</span><span class="sxs-lookup"><span data-stu-id="78d81-116">Component1</span></span>    |
| <span data-ttu-id="78d81-117">Feature1</span><span class="sxs-lookup"><span data-stu-id="78d81-117">Feature1</span></span> | <span data-ttu-id="78d81-118">Component1600</span><span class="sxs-lookup"><span data-stu-id="78d81-118">Component1600</span></span> |



 

<span data-ttu-id="78d81-119">Чтобы устранить это предупреждение, попробуйте разделить компонент на несколько функций.</span><span class="sxs-lookup"><span data-stu-id="78d81-119">To fix this warning, try splitting the feature into several features</span></span>

## <a name="related-topics"></a><span data-ttu-id="78d81-120">См. также</span><span class="sxs-lookup"><span data-stu-id="78d81-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78d81-121">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="78d81-121">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




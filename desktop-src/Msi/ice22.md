---
description: ICE22 использует таблицу Феатурекомпонентс для проверки сопоставления компонентов и компонентов, упоминаемых в таблице Публишкомпонент.
ms.assetid: 1aa3e2e6-3f05-411e-829f-aeddbb53445d
title: ICE22
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26574b11f9d908026d901a74632766998246d31a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663667"
---
# <a name="ice22"></a><span data-ttu-id="2e02d-103">ICE22</span><span class="sxs-lookup"><span data-stu-id="2e02d-103">ICE22</span></span>

<span data-ttu-id="2e02d-104">ICE22 использует [таблицу феатурекомпонентс](featurecomponents-table.md) для проверки сопоставления компонентов и компонентов, упоминаемых в [таблице публишкомпонент](publishcomponent-table.md).</span><span class="sxs-lookup"><span data-stu-id="2e02d-104">ICE22 uses the [FeatureComponents table](featurecomponents-table.md) to validate the mapping of features and components referenced in the [PublishComponent table](publishcomponent-table.md).</span></span>

## <a name="result"></a><span data-ttu-id="2e02d-105">Результат</span><span class="sxs-lookup"><span data-stu-id="2e02d-105">Result</span></span>

<span data-ttu-id="2e02d-106">ICE22 отправляет сообщение об ошибке, если компоненты и компоненты сопоставлены неправильно в [таблице публишкомпонент](publishcomponent-table.md).</span><span class="sxs-lookup"><span data-stu-id="2e02d-106">ICE22 posts an error message if the features and components are mapped incorrectly in the [PublishComponent table](publishcomponent-table.md).</span></span>

## <a name="example"></a><span data-ttu-id="2e02d-107">Пример</span><span class="sxs-lookup"><span data-stu-id="2e02d-107">Example</span></span>

<span data-ttu-id="2e02d-108">В следующем примере ICE22 отправляет ошибку, которая {00000003-0004-0000-0000-624474732465} не имеет правильного сопоставления для \_ столбцов компонента и компонента \_ .</span><span class="sxs-lookup"><span data-stu-id="2e02d-108">For the following example ICE22 posts an error that {00000003-0004-0000-0000-624474732465} does not have the correct mapping for the Feature\_ and Component\_ columns.</span></span>

<span data-ttu-id="2e02d-109">[Таблица публишкомпонент](publishcomponent-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="2e02d-109">[PublishComponent Table](publishcomponent-table.md) (partial)</span></span>



| <span data-ttu-id="2e02d-110">ComponentId</span><span class="sxs-lookup"><span data-stu-id="2e02d-110">ComponentId</span></span>                            | <span data-ttu-id="2e02d-111">Функция\_</span><span class="sxs-lookup"><span data-stu-id="2e02d-111">Feature\_</span></span> | <span data-ttu-id="2e02d-112">Компонент\_</span><span class="sxs-lookup"><span data-stu-id="2e02d-112">Component\_</span></span> |
|----------------------------------------|-----------|-------------|
| {00000002-0003-0000-0000-624474736554} | <span data-ttu-id="2e02d-113">Feat1</span><span class="sxs-lookup"><span data-stu-id="2e02d-113">Feat1</span></span>     | <span data-ttu-id="2e02d-114">Comp1</span><span class="sxs-lookup"><span data-stu-id="2e02d-114">Comp1</span></span>       |
| {00000003-0004-0000-0000-624474732465} | <span data-ttu-id="2e02d-115">Feat1</span><span class="sxs-lookup"><span data-stu-id="2e02d-115">Feat1</span></span>     | <span data-ttu-id="2e02d-116">Comp2</span><span class="sxs-lookup"><span data-stu-id="2e02d-116">Comp2</span></span>       |



 

<span data-ttu-id="2e02d-117">[Таблица феатурекомпонентс](featurecomponents-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="2e02d-117">[FeatureComponents Table](featurecomponents-table.md) (partial)</span></span>



| <span data-ttu-id="2e02d-118">Функция\_</span><span class="sxs-lookup"><span data-stu-id="2e02d-118">Feature\_</span></span> | <span data-ttu-id="2e02d-119">Компонент\_</span><span class="sxs-lookup"><span data-stu-id="2e02d-119">Component\_</span></span> |
|-----------|-------------|
| <span data-ttu-id="2e02d-120">Feat1</span><span class="sxs-lookup"><span data-stu-id="2e02d-120">Feat1</span></span>     | <span data-ttu-id="2e02d-121">Comp1</span><span class="sxs-lookup"><span data-stu-id="2e02d-121">Comp1</span></span>       |



 

## <a name="related-topics"></a><span data-ttu-id="2e02d-122">См. также</span><span class="sxs-lookup"><span data-stu-id="2e02d-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e02d-123">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="2e02d-123">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




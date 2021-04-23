---
description: ICE21 проверяет, относится каждый компонент в таблице Component к компоненту. Для проверки этого сопоставления используется таблица Феатурекомпонентс.
ms.assetid: 68983d6a-b807-4730-a645-378001e558ec
title: ICE21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c457d026b3dc57a718eabea704254a3448a3de26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663668"
---
# <a name="ice21"></a><span data-ttu-id="52a7d-104">ICE21</span><span class="sxs-lookup"><span data-stu-id="52a7d-104">ICE21</span></span>

<span data-ttu-id="52a7d-105">ICE21 проверяет, относится каждый компонент в [таблице Component](component-table.md) к компоненту.</span><span class="sxs-lookup"><span data-stu-id="52a7d-105">ICE21 validates that every component in the [Component table](component-table.md) belongs to a feature.</span></span> <span data-ttu-id="52a7d-106">Для проверки этого сопоставления используется [Таблица феатурекомпонентс](featurecomponents-table.md) .</span><span class="sxs-lookup"><span data-stu-id="52a7d-106">It uses the [FeatureComponents table](featurecomponents-table.md) to check for this mapping.</span></span>

## <a name="result"></a><span data-ttu-id="52a7d-107">Результат</span><span class="sxs-lookup"><span data-stu-id="52a7d-107">Result</span></span>

<span data-ttu-id="52a7d-108">ICE21 отправляет сообщение об ошибке, если пакет установки содержит компонент, который не принадлежит к компоненту.</span><span class="sxs-lookup"><span data-stu-id="52a7d-108">ICE21 posts an error message if the installation package contains a component that does not belong to a feature.</span></span>

## <a name="example"></a><span data-ttu-id="52a7d-109">Пример</span><span class="sxs-lookup"><span data-stu-id="52a7d-109">Example</span></span>

<span data-ttu-id="52a7d-110">В следующем примере ICE21 отправляет сообщение об ошибке, уведомляющее о том, что компонент comp1 не сопоставлен ни с одной функцией.</span><span class="sxs-lookup"><span data-stu-id="52a7d-110">For the following example, ICE21 posts an error message stating that the component Comp1 does not map to any feature.</span></span>

<span data-ttu-id="52a7d-111">[Таблица Component](component-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="52a7d-111">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="52a7d-112">Компонент</span><span class="sxs-lookup"><span data-stu-id="52a7d-112">Component</span></span> |
|-----------|
| <span data-ttu-id="52a7d-113">Comp1</span><span class="sxs-lookup"><span data-stu-id="52a7d-113">Comp1</span></span>     |
| <span data-ttu-id="52a7d-114">Comp2</span><span class="sxs-lookup"><span data-stu-id="52a7d-114">Comp2</span></span>     |



 

<span data-ttu-id="52a7d-115">[Таблица феатурекомпонентс](featurecomponents-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="52a7d-115">[FeatureComponents Table](featurecomponents-table.md) (partial)</span></span>



| <span data-ttu-id="52a7d-116">Функция</span><span class="sxs-lookup"><span data-stu-id="52a7d-116">Feature</span></span>  | <span data-ttu-id="52a7d-117">Компонент</span><span class="sxs-lookup"><span data-stu-id="52a7d-117">Component</span></span> |
|----------|-----------|
| <span data-ttu-id="52a7d-118">Feature1</span><span class="sxs-lookup"><span data-stu-id="52a7d-118">Feature1</span></span> | <span data-ttu-id="52a7d-119">Comp2</span><span class="sxs-lookup"><span data-stu-id="52a7d-119">Comp2</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="52a7d-120">См. также</span><span class="sxs-lookup"><span data-stu-id="52a7d-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52a7d-121">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="52a7d-121">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




---
title: Проверка нажатия касания
description: В подразделах этого раздела приводятся общие сведения о поддержке проверки нажатия сенсорного ввода в Windows 8.
ms.assetid: bdd7630c-b2d8-4080-a149-efec018f697d
keywords:
- взаимодействие с пользователем
- input
- указатель
- Сенсорный ввод
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 8cf6d28badb47a176a6feccf166344003faf1de8
ms.sourcegitcommit: 9e389b8e39616dcef8f7ff4bc53d945179401478
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/07/2020
ms.locfileid: "103890203"
---
# <a name="touch-hit-testing"></a><span data-ttu-id="aad1a-107">Проверка нажатия касания</span><span class="sxs-lookup"><span data-stu-id="aad1a-107">Touch Hit Testing</span></span>

## <a name="purpose"></a><span data-ttu-id="aad1a-108">Назначение</span><span class="sxs-lookup"><span data-stu-id="aad1a-108">Purpose</span></span>

<span data-ttu-id="aad1a-109">В подразделах этого раздела приводятся общие сведения о поддержке проверки нажатия касанием в Windows.</span><span class="sxs-lookup"><span data-stu-id="aad1a-109">The topics in this section provide an overview of support for Touch Hit Testing in Windows.</span></span> <span data-ttu-id="aad1a-110">Проверка попадания касания позволяет определить целевой объект на основе того, попадает ли область содержимого элемента пользовательского интерфейса в область контакта или включает контактную точку.</span><span class="sxs-lookup"><span data-stu-id="aad1a-110">Touch Hit Testing lets you identify an input target based on whether the content area of a UI element falls within the contact area or includes the contact point.</span></span>

<span data-ttu-id="aad1a-111">При проверке нажатия касания используется сложная геометрия контакта для всей сенсорной области, а не отдельной интерполяции x-y.</span><span class="sxs-lookup"><span data-stu-id="aad1a-111">Touch hit testing uses complex contact geometry for the entire touch area rather than a single interpolated x-y coordinate.</span></span> <span data-ttu-id="aad1a-112">Использование всей геометрии контакта значительно повышает точность и точность при определении наиболее вероятной цели сенсорного ввода.</span><span class="sxs-lookup"><span data-stu-id="aad1a-112">Using the entire contact geometry greatly improves precision and accuracy when you're identifying the most likely target of touch input.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="aad1a-113">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="aad1a-113">In this section</span></span>

| <span data-ttu-id="aad1a-114">Раздел</span><span class="sxs-lookup"><span data-stu-id="aad1a-114">Topic</span></span> | <span data-ttu-id="aad1a-115">Описание</span><span class="sxs-lookup"><span data-stu-id="aad1a-115">Description</span></span> |
| --- | --- |
| [<span data-ttu-id="aad1a-116">Ссылка на проверку нажатия касания</span><span class="sxs-lookup"><span data-stu-id="aad1a-116">Touch Hit Testing Reference</span></span>](touchhittest-reference.md)<br/> | <span data-ttu-id="aad1a-117">В подразделах этого раздела приведены справочные спецификации для [проверки нажатия касания](touch-hit-testing-portal.md).</span><span class="sxs-lookup"><span data-stu-id="aad1a-117">The topics in this section provide the reference specifications for [Touch Hit Testing](touch-hit-testing-portal.md).</span></span><br/> |

## <a name="developer-audience"></a><span data-ttu-id="aad1a-118">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="aad1a-118">Developer audience</span></span>

<span data-ttu-id="aad1a-119">API проверки нажатия касания предназначены для разработчиков, создающих платформы пользовательского интерфейса, которые обеспечивают единообразное взаимодействие с пользователями в настольных приложениях.</span><span class="sxs-lookup"><span data-stu-id="aad1a-119">The Touch Hit Testing APIs are designed for developers who are building UI frameworks that provide a consistent touch-optimized user experience across desktop applications.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aad1a-120">См. также</span><span class="sxs-lookup"><span data-stu-id="aad1a-120">Related topics</span></span>

[<span data-ttu-id="aad1a-121">Взаимодействие с пользователем</span><span class="sxs-lookup"><span data-stu-id="aad1a-121">User Interaction</span></span>](../user-interaction.md)

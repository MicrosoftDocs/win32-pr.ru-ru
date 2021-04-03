---
title: дупликатесиблингнамес
description: дупликатесиблингнамес
ms.assetid: 4E9FFD16-EAC0-4778-8DEB-D179E2197411
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aed5a7caeadc34519988fe8a4a1f12ec4e05ce13
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103780048"
---
# <a name="duplicatesiblingnames"></a><span data-ttu-id="664e5-103">дупликатесиблингнамес</span><span class="sxs-lookup"><span data-stu-id="664e5-103">DuplicateSiblingNames</span></span>

## <a name="text"></a><span data-ttu-id="664e5-104">Текст</span><span class="sxs-lookup"><span data-stu-id="664e5-104">Text</span></span>

<span data-ttu-id="664e5-105">Дублирование имени и роли однорангового элемента \\ " {0} \\ " приведет к неоднозначности между элементами.</span><span class="sxs-lookup"><span data-stu-id="664e5-105">Duplicate sibling Name+Role \\"{0}\\" will cause ambiguity between elements.</span></span>

## <a name="type"></a><span data-ttu-id="664e5-106">Тип</span><span class="sxs-lookup"><span data-stu-id="664e5-106">Type</span></span>

<span data-ttu-id="664e5-107">Ошибка</span><span class="sxs-lookup"><span data-stu-id="664e5-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="664e5-108">Описание</span><span class="sxs-lookup"><span data-stu-id="664e5-108">Description</span></span>

<span data-ttu-id="664e5-109">Элемент имеет то же имя и роль или ControlType, что и другой элемент.</span><span class="sxs-lookup"><span data-stu-id="664e5-109">An element has the same Name and Role/ControlType as another element.</span></span>

<span data-ttu-id="664e5-110">Эта проблема может вызвать путаницу, так как средства чтения с экрана будут читать один и тот же текст для всех элементов с одинаковыми именами и ролями или ControlType.</span><span class="sxs-lookup"><span data-stu-id="664e5-110">This issue can cause confusion because screen readers will read the same text for all the elements with the same Name and Role/ControlType.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="664e5-111">Возможные причины</span><span class="sxs-lookup"><span data-stu-id="664e5-111">Possible causes</span></span>

-   <span data-ttu-id="664e5-112">Имя элемента содержит текст Role/ControlType.</span><span class="sxs-lookup"><span data-stu-id="664e5-112">Element’s name contain Role/ControlType text.</span></span>
-   <span data-ttu-id="664e5-113">Имя элемента или его родительский элемент не заданы или заданы неправильно.</span><span class="sxs-lookup"><span data-stu-id="664e5-113">Element’s name or the name of its parent is not set or is set incorrectly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="664e5-114">См. также</span><span class="sxs-lookup"><span data-stu-id="664e5-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="664e5-115">**IAccessible:: Get \_ аккнаме**</span><span class="sxs-lookup"><span data-stu-id="664e5-115">**IAccessible::get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[<span data-ttu-id="664e5-116">Свойство Name</span><span class="sxs-lookup"><span data-stu-id="664e5-116">Name Property</span></span>](name-property.md)
</dt> <dt>

[<span data-ttu-id="664e5-117">**UIA \_ намепропертид**</span><span class="sxs-lookup"><span data-stu-id="664e5-117">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)
</dt> <dt>

[<span data-ttu-id="664e5-118">**Иуиаутоматионелемент. Куррентнаме**</span><span class="sxs-lookup"><span data-stu-id="664e5-118">**IUIAutomationElement.CurrentName**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname)
</dt> </dl>

 

 





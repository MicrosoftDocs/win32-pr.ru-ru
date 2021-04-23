---
title: елеменсаснонаме
description: елеменсаснонаме
ms.assetid: 893A758F-BD34-4ABE-A99E-8CABE33966E0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc9af7e1ad0a62f35edb88102b68bfa6de3d5c28
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332659"
---
# <a name="elementhasnoname"></a><span data-ttu-id="04523-103">елеменсаснонаме</span><span class="sxs-lookup"><span data-stu-id="04523-103">ElementHasNoName</span></span>

## <a name="text"></a><span data-ttu-id="04523-104">Текст</span><span class="sxs-lookup"><span data-stu-id="04523-104">Text</span></span>

<span data-ttu-id="04523-105">У элемента нет имени</span><span class="sxs-lookup"><span data-stu-id="04523-105">Element has no name</span></span>

## <a name="type"></a><span data-ttu-id="04523-106">Тип</span><span class="sxs-lookup"><span data-stu-id="04523-106">Type</span></span>

<span data-ttu-id="04523-107">Ошибка</span><span class="sxs-lookup"><span data-stu-id="04523-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="04523-108">Описание</span><span class="sxs-lookup"><span data-stu-id="04523-108">Description</span></span>

<span data-ttu-id="04523-109">У элемента нет имени.</span><span class="sxs-lookup"><span data-stu-id="04523-109">An element does not have a name.</span></span> <span data-ttu-id="04523-110">Например, элемент не имеет реализованного Аккнаме и возвращается пустая строка, если метод [**Get \_ аккнаме**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) используется для получения имени MSAA элемента.</span><span class="sxs-lookup"><span data-stu-id="04523-110">For example, the element does not have accName implemented and an empty string is returned when the [**get\_accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) method is used to retrieve the MSAA name of the element.</span></span>

<span data-ttu-id="04523-111">Эта проблема вызывает проблемы для пользователей, которые используют средство чтения с экрана и клавиатуру для навигации, поскольку элемент может быть неверно идентифицирован пользователю.</span><span class="sxs-lookup"><span data-stu-id="04523-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because an element might be incorrectly identified to the user.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="04523-112">Возможные причины</span><span class="sxs-lookup"><span data-stu-id="04523-112">Possible causes</span></span>

-   <span data-ttu-id="04523-113">У элемента или его родителя нет имени или метки.</span><span class="sxs-lookup"><span data-stu-id="04523-113">The element or its parent has no name or label.</span></span>
-   <span data-ttu-id="04523-114">Элементу назначается [**аккроле**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) , предлагающий элементу имя.</span><span class="sxs-lookup"><span data-stu-id="04523-114">The element is assigned an [**accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) that suggests the element have a name.</span></span>
-   <span data-ttu-id="04523-115">Элемент, имеющий фокус, не должен получать фокус.</span><span class="sxs-lookup"><span data-stu-id="04523-115">The element that has focus should not receive focus.</span></span> <span data-ttu-id="04523-116">Например, метка или отключенный элемент управления.</span><span class="sxs-lookup"><span data-stu-id="04523-116">For example, a label or a disabled control.</span></span>
-   <span data-ttu-id="04523-117">Фокус получен на невидимый элемент управления.</span><span class="sxs-lookup"><span data-stu-id="04523-117">An invisible control has received focus.</span></span>

## <a name="related-topics"></a><span data-ttu-id="04523-118">См. также</span><span class="sxs-lookup"><span data-stu-id="04523-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04523-119">**IAccessible:: Get \_ аккнаме**</span><span class="sxs-lookup"><span data-stu-id="04523-119">**IAccessible::get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[<span data-ttu-id="04523-120">Свойство Name</span><span class="sxs-lookup"><span data-stu-id="04523-120">Name Property</span></span>](name-property.md)
</dt> </dl>

 

 





---
title: Для элементов Драгпаттерн/Драгдроппаттерн требуется имя
description: Для элементов Драгпаттерн/Драгдроппаттерн требуется имя
ms.assetid: DEF58FB2-5830-4162-87D0-40DEC1237529
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ecc60eeca59f4754f9c160696cdfa2556c36a5e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700471"
---
# <a name="dragpatterndragdroppattern-elements-requires-name"></a><span data-ttu-id="f308e-103">Для элементов Драгпаттерн/Драгдроппаттерн требуется имя</span><span class="sxs-lookup"><span data-stu-id="f308e-103">DragPattern/DragDropPattern elements requires Name</span></span>

## <a name="text"></a><span data-ttu-id="f308e-104">Текст</span><span class="sxs-lookup"><span data-stu-id="f308e-104">Text</span></span>

<span data-ttu-id="f308e-105">Элементы, поддерживающие перетаскивание, должны иметь допустимый набор "Name"</span><span class="sxs-lookup"><span data-stu-id="f308e-105">Elements that support Drag/Drop should have a valid 'Name' set</span></span>

## <a name="type"></a><span data-ttu-id="f308e-106">Тип</span><span class="sxs-lookup"><span data-stu-id="f308e-106">Type</span></span>

<span data-ttu-id="f308e-107">Ошибка</span><span class="sxs-lookup"><span data-stu-id="f308e-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="f308e-108">Описание</span><span class="sxs-lookup"><span data-stu-id="f308e-108">Description</span></span>

<span data-ttu-id="f308e-109">Элемент поддерживает либо [**иуиаутоматиондрагпаттерн**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) , либо [**иуиаутоматиондроптаржетпаттерн**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern), но не имеет допустимого набора имен.</span><span class="sxs-lookup"><span data-stu-id="f308e-109">The element supports either [**IUIAutomationDragPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) or [**IUIAutomationDropTargetPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern), but does not have a valid Name set.</span></span>

<span data-ttu-id="f308e-110">Эта проблема вызывает проблемы для пользователей, которые используют средство чтения с экрана.</span><span class="sxs-lookup"><span data-stu-id="f308e-110">This issue causes problems for people who rely on a screen-reader.</span></span> <span data-ttu-id="f308e-111">Пользователь не сможет определить, что этот объект с момента считывания с экрана не будет считать допустимое имя, чтобы отличать этот элемент от перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="f308e-111">The user will not be able to tell what this object is since the screen read will not read out a valid name to distinguish what this element is when dragging.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="f308e-112">Возможные причины</span><span class="sxs-lookup"><span data-stu-id="f308e-112">Possible causes</span></span>

-   <span data-ttu-id="f308e-113">Элемент или его родитель имеет неправильно назначенное имя или подпись.</span><span class="sxs-lookup"><span data-stu-id="f308e-113">The element, or its parent, has an incorrectly assigned name or label.</span></span>
-   <span data-ttu-id="f308e-114">Разработчик не знает, что читатели экрана считывают имена и типы элементов управления.</span><span class="sxs-lookup"><span data-stu-id="f308e-114">A developer is not aware that screen readers read names and control types.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f308e-115">См. также</span><span class="sxs-lookup"><span data-stu-id="f308e-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f308e-116">**IAccessible:: Get \_ аккнаме**</span><span class="sxs-lookup"><span data-stu-id="f308e-116">**IAccessible::get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[<span data-ttu-id="f308e-117">Свойство Name</span><span class="sxs-lookup"><span data-stu-id="f308e-117">Name Property</span></span>](name-property.md)
</dt> <dt>

[<span data-ttu-id="f308e-118">**UIA \_ намепропертид**</span><span class="sxs-lookup"><span data-stu-id="f308e-118">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)
</dt> <dt>

[<span data-ttu-id="f308e-119">**Иуиаутоматионелемент:: Куррентнаме**</span><span class="sxs-lookup"><span data-stu-id="f308e-119">**IUIAutomationElement::CurrentName**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname)
</dt> </dl>

 

 





---
title: Для элементов Драгпаттерн/Драгдроппаттерн требуется допустимый Дропеффект
description: Для элементов Драгпаттерн/Драгдроппаттерн требуется допустимый Дропеффект
ms.assetid: 508DD4F3-4878-4A9E-859D-06BBDA505708
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33acda19732e2ebd96182023fce9641012b50d6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772701"
---
# <a name="dragpatterndragdroppattern-elements-requires-valid-dropeffect"></a><span data-ttu-id="df5c9-103">Для элементов Драгпаттерн/Драгдроппаттерн требуется допустимый Дропеффект</span><span class="sxs-lookup"><span data-stu-id="df5c9-103">DragPattern/DragDropPattern elements requires valid DropEffect</span></span>

## <a name="text"></a><span data-ttu-id="df5c9-104">Текст</span><span class="sxs-lookup"><span data-stu-id="df5c9-104">Text</span></span>

<span data-ttu-id="df5c9-105">Элементы, поддерживающие перетаскивание, должны иметь допустимый набор "Дропеффект"</span><span class="sxs-lookup"><span data-stu-id="df5c9-105">Elements that support Drag/Drop should have a valid 'DropEffect' set</span></span>

## <a name="type"></a><span data-ttu-id="df5c9-106">Тип</span><span class="sxs-lookup"><span data-stu-id="df5c9-106">Type</span></span>

<span data-ttu-id="df5c9-107">Ошибка</span><span class="sxs-lookup"><span data-stu-id="df5c9-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="df5c9-108">Описание</span><span class="sxs-lookup"><span data-stu-id="df5c9-108">Description</span></span>

<span data-ttu-id="df5c9-109">Элемент поддерживает либо [**иуиаутоматиондрагпаттерн**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) , либо [**иуиаутоматиондроптаржетпаттерн**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern), но не имеет допустимого набора свойств [**дропеффект**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) .</span><span class="sxs-lookup"><span data-stu-id="df5c9-109">The element supports either [**IUIAutomationDragPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) or [**IUIAutomationDropTargetPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern), but does not have a valid [**DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) property set.</span></span>

<span data-ttu-id="df5c9-110">Эта проблема вызывает проблемы для пользователей, которые используют средство чтения с экрана.</span><span class="sxs-lookup"><span data-stu-id="df5c9-110">This issue causes problems for people who rely on a screen-reader.</span></span> <span data-ttu-id="df5c9-111">Пользователь не сможет определить, какое действие этот объект имеет при перетаскивании.</span><span class="sxs-lookup"><span data-stu-id="df5c9-111">The user will not be able to tell what effect this object has when dragging.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="df5c9-112">Возможные причины</span><span class="sxs-lookup"><span data-stu-id="df5c9-112">Possible causes</span></span>

-   <span data-ttu-id="df5c9-113">Элемент или его родитель не создал [**дропеффект**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) или [**дропеффектс**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffects) неправильно назначенное имя или метка.</span><span class="sxs-lookup"><span data-stu-id="df5c9-113">The element, or its parent, has not created the [**DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) or [**DropEffects**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffects) an incorrectly assigned name or label.</span></span>
-   <span data-ttu-id="df5c9-114">Разработчик не знает, что читатели экрана читают Дропеффект.</span><span class="sxs-lookup"><span data-stu-id="df5c9-114">A developer is not aware that screen readers read DropEffect(s).</span></span>

 

 





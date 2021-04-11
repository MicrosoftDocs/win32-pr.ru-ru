---
title: Интерфейсы условий свойств для клиентов
description: В этом разделе описываются интерфейсы условий свойств для клиентов автоматизации пользовательского интерфейса для приложений Microsoft Win32.
ms.assetid: cea34e47-03a9-4ff9-9019-427a2a3e13d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00f840706d4f9e340cae86813a4992400791dccd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070093"
---
# <a name="property-condition-interfaces-for-clients"></a><span data-ttu-id="b6294-103">Интерфейсы условий свойств для клиентов</span><span class="sxs-lookup"><span data-stu-id="b6294-103">Property Condition Interfaces for Clients</span></span>

<span data-ttu-id="b6294-104">В этом разделе описываются интерфейсы условий свойств для клиентов автоматизации пользовательского интерфейса для приложений Microsoft Win32.</span><span class="sxs-lookup"><span data-stu-id="b6294-104">This section describes property condition interfaces for UI Automation clients for Microsoft Win32 applications.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b6294-105">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="b6294-105">In this section</span></span>



| <span data-ttu-id="b6294-106">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="b6294-106">Interface</span></span>                                                                                  | <span data-ttu-id="b6294-107">Описание</span><span class="sxs-lookup"><span data-stu-id="b6294-107">Description</span></span>                                                                                                                                                        |
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b6294-108">**иуиаутоматионандкондитион**</span><span class="sxs-lookup"><span data-stu-id="b6294-108">**IUIAutomationAndCondition**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationandcondition)<br/>           | <span data-ttu-id="b6294-109">Предоставляет свойства и методы, которые клиентские приложения автоматизации пользовательского интерфейса Майкрософт могут использовать для получения сведений о условии свойства, основанного на и.</span><span class="sxs-lookup"><span data-stu-id="b6294-109">Exposes properties and methods that Microsoft UI Automation client applications can use to retrieve information about an AND-based property condition.</span></span> <br/> |
| [<span data-ttu-id="b6294-110">**иуиаутоматионбулкондитион**</span><span class="sxs-lookup"><span data-stu-id="b6294-110">**IUIAutomationBoolCondition**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationboolcondition)<br/>         | <span data-ttu-id="b6294-111">Представляет условие, которое может иметь **значение true** (выбирает все элементы) или **false** (не выбирает элементов).</span><span class="sxs-lookup"><span data-stu-id="b6294-111">Represents a condition that can be either **TRUE** (selects all elements) or **FALSE** (selects no elements).</span></span><br/>                                           |
| [<span data-ttu-id="b6294-112">**иуиаутоматионкондитион**</span><span class="sxs-lookup"><span data-stu-id="b6294-112">**IUIAutomationCondition**</span></span>](/windows/win32/api/uiautomationclient/nn-uiautomationclient-iuiautomationcondition)<br/>                 | <span data-ttu-id="b6294-113">Это основной интерфейс для условий, используемых для фильтрации при поиске элементов в дереве модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="b6294-113">This is the primary interface for conditions used in filtering when searching for elements in the UI Automation tree.</span></span><br/>                                   |
| [<span data-ttu-id="b6294-114">**иуиаутоматионноткондитион**</span><span class="sxs-lookup"><span data-stu-id="b6294-114">**IUIAutomationNotCondition**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationnotcondition)<br/>           | <span data-ttu-id="b6294-115">Представляет условие, которое является отрицательным для другого условия.</span><span class="sxs-lookup"><span data-stu-id="b6294-115">Represents a condition that is the negative of another condition.</span></span><br/>                                                                                       |
| [<span data-ttu-id="b6294-116">**иуиаутоматионоркондитион**</span><span class="sxs-lookup"><span data-stu-id="b6294-116">**IUIAutomationOrCondition**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationorcondition)<br/>             | <span data-ttu-id="b6294-117">Представляет условие, состоящие из нескольких условий, по крайней мере одно из которых должно иметь значение true.</span><span class="sxs-lookup"><span data-stu-id="b6294-117">Represents a condition made up of multiple conditions, at least one of which must be true.</span></span><br/>                                                              |
| [<span data-ttu-id="b6294-118">**иуиаутоматионпропертикондитион**</span><span class="sxs-lookup"><span data-stu-id="b6294-118">**IUIAutomationPropertyCondition**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertycondition)<br/> | <span data-ttu-id="b6294-119">Представляет условие на основе значения свойства, используемого для поиска элементов модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="b6294-119">Represents a condition based on a property value that is used to find UI Automation elements.</span></span><br/>                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="b6294-120">См. также</span><span class="sxs-lookup"><span data-stu-id="b6294-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6294-121">Клиенты автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="b6294-121">UI Automation Clients</span></span>](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 


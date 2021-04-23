---
title: Структуры модели автоматизации пользовательского интерфейса
description: В этом разделе описываются структуры, используемые клиентскими приложениями модели автоматизации пользовательского интерфейса и поставщиком автоматизации пользовательского интерфейса для Microsoft Win32.
ms.assetid: 37d6a7c0-6925-443b-aa21-da2a14a9ddad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c55ddf9086f0714665c944a5a80e53e63eb3a91a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486677"
---
# <a name="ui-automation-structures"></a><span data-ttu-id="96038-103">Структуры модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="96038-103">UI Automation Structures</span></span>

<span data-ttu-id="96038-104">В этом разделе описываются структуры, используемые клиентскими приложениями модели автоматизации пользовательского интерфейса и поставщиком автоматизации пользовательского интерфейса для Microsoft Win32.</span><span class="sxs-lookup"><span data-stu-id="96038-104">This section describes the structures used by UI Automation client applications and UI Automation provider for Microsoft Win32.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="96038-105">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="96038-105">In this section</span></span>



| <span data-ttu-id="96038-106">Структура</span><span class="sxs-lookup"><span data-stu-id="96038-106">Structure</span></span>                                                                            | <span data-ttu-id="96038-107">Описание</span><span class="sxs-lookup"><span data-stu-id="96038-107">Description</span></span>                                                                                   |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="96038-108">**ExtendedProperty**</span><span class="sxs-lookup"><span data-stu-id="96038-108">**ExtendedProperty**</span></span>](/windows/desktop/api/UIAutomationClient/ns-uiautomationclient-extendedproperty)<br/>                       | <span data-ttu-id="96038-109">Содержит сведения о расширенном свойстве.</span><span class="sxs-lookup"><span data-stu-id="96038-109">Contains information about an extended property.</span></span> <br/>                                  |
| [<span data-ttu-id="96038-110">**уиаутоматионевентинфо**</span><span class="sxs-lookup"><span data-stu-id="96038-110">**UIAutomationEventInfo**</span></span>](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo)<br/>       | <span data-ttu-id="96038-111">Содержит сведения о пользовательском событии.</span><span class="sxs-lookup"><span data-stu-id="96038-111">Contains information about a custom event.</span></span><br/>                                         |
| [<span data-ttu-id="96038-112">**уиаутоматионмесодинфо**</span><span class="sxs-lookup"><span data-stu-id="96038-112">**UIAutomationMethodInfo**</span></span>](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationmethodinfo)<br/>     | <span data-ttu-id="96038-113">Содержит сведения о методе, поддерживаемом настраиваемым шаблоном элемента управления.</span><span class="sxs-lookup"><span data-stu-id="96038-113">Contains information about a method that is supported by a custom control pattern.</span></span><br/> |
| [<span data-ttu-id="96038-114">**уиаутоматионпараметер**</span><span class="sxs-lookup"><span data-stu-id="96038-114">**UIAutomationParameter**</span></span>](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationparameter)<br/>       | <span data-ttu-id="96038-115">Содержит сведения о параметре пользовательского шаблона элемента управления.</span><span class="sxs-lookup"><span data-stu-id="96038-115">Contains information about a parameter of a custom control pattern.</span></span><br/>                |
| [<span data-ttu-id="96038-116">**уиаутоматионпаттернинфо**</span><span class="sxs-lookup"><span data-stu-id="96038-116">**UIAutomationPatternInfo**</span></span>](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpatterninfo)<br/>   | <span data-ttu-id="96038-117">Содержит сведения о шаблоне пользовательского элемента управления.</span><span class="sxs-lookup"><span data-stu-id="96038-117">Contains information about a custom control pattern.</span></span><br/>                               |
| [<span data-ttu-id="96038-118">**уиаутоматионпропертинфо**</span><span class="sxs-lookup"><span data-stu-id="96038-118">**UIAutomationPropertyInfo**</span></span>](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo)<br/> | <span data-ttu-id="96038-119">Содержит сведения о пользовательском свойстве.</span><span class="sxs-lookup"><span data-stu-id="96038-119">Contains information about a custom property.</span></span><br/>                                      |
| [<span data-ttu-id="96038-120">**уиачанжеинфо**</span><span class="sxs-lookup"><span data-stu-id="96038-120">**UiaChangeInfo**</span></span>](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiachangeinfo)<br/>                                    | <span data-ttu-id="96038-121">Содержит данные о произошедших изменениях автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="96038-121">Contains data about a UI Automation change that occurred.</span></span><br/>                          |
| [<span data-ttu-id="96038-122">**уиапоинт**</span><span class="sxs-lookup"><span data-stu-id="96038-122">**UiaPoint**</span></span>](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiapoint)<br/>                                 | <span data-ttu-id="96038-123">Содержит координаты точки.</span><span class="sxs-lookup"><span data-stu-id="96038-123">Contains the coordinates of a point.</span></span> <br/>                                              |
| [<span data-ttu-id="96038-124">**уиарект**</span><span class="sxs-lookup"><span data-stu-id="96038-124">**UiaRect**</span></span>](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiarect)<br/>                                   | <span data-ttu-id="96038-125">Содержит расположение и размер прямоугольника в экранных координатах.</span><span class="sxs-lookup"><span data-stu-id="96038-125">Contains the position and size of a rectangle, in screen coordinates.</span></span><br/>              |



 

 

 






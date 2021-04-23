---
title: контролтипеноекспектедпаттернссуппортед
description: контролтипеноекспектедпаттернссуппортед
ms.assetid: 2C9CEFEA-8207-47A7-B100-A56CFBFB792D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78c40f9f094589b312a033d6bdadf3fbf3b5020b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330240"
---
# <a name="controltypenoexpectedpatternssupported"></a><span data-ttu-id="0b0b0-103">контролтипеноекспектедпаттернссуппортед</span><span class="sxs-lookup"><span data-stu-id="0b0b0-103">ControlTypeNoExpectedPatternsSupported</span></span>

## <a name="text"></a><span data-ttu-id="0b0b0-104">Текст</span><span class="sxs-lookup"><span data-stu-id="0b0b0-104">Text</span></span>

<span data-ttu-id="0b0b0-105">Элемент с ControlType {0} должен поддерживать хотя бы один из этих шаблонов: {1} но этот элемент не</span><span class="sxs-lookup"><span data-stu-id="0b0b0-105">Element with a ControlType of {0} should support at least one of these patterns:{1} but this element does not</span></span>

## <a name="type"></a><span data-ttu-id="0b0b0-106">Тип</span><span class="sxs-lookup"><span data-stu-id="0b0b0-106">Type</span></span>

<span data-ttu-id="0b0b0-107">Ошибка</span><span class="sxs-lookup"><span data-stu-id="0b0b0-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="0b0b0-108">Описание</span><span class="sxs-lookup"><span data-stu-id="0b0b0-108">Description</span></span>

<span data-ttu-id="0b0b0-109">Поддержка модели автоматизации пользовательского интерфейса элемента не соответствует спецификации модели автоматизации пользовательского интерфейса, поскольку элемент должен поддерживать по крайней мере один из указанных в списке шаблонов элементов управления, но не имеет.</span><span class="sxs-lookup"><span data-stu-id="0b0b0-109">The element's UI Automation support does not comply with the UI Automation specification because the element should support at least one of the provided list of control patterns, but does not.</span></span> <span data-ttu-id="0b0b0-110">В результате этот элемент может быть неверно предоставлен для вспомогательных технологий, что может оказать серьезное влияние на взаимодействие с пользователем.</span><span class="sxs-lookup"><span data-stu-id="0b0b0-110">As a result, this element might not be properly exposed to assistive technologies, which could have a serious impact on user experience.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="0b0b0-111">Возможные причины</span><span class="sxs-lookup"><span data-stu-id="0b0b0-111">Possible causes</span></span>

-   <span data-ttu-id="0b0b0-112">Неполная реализация модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="0b0b0-112">Incomplete UI Automation implementation.</span></span>
-   <span data-ttu-id="0b0b0-113">Свойство ControlType задано неправильно.</span><span class="sxs-lookup"><span data-stu-id="0b0b0-113">The ControlType property is not set correctly.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b0b0-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0b0b0-114">Remarks</span></span>

<span data-ttu-id="0b0b0-115">Аккчеккер регистрирует это сообщение об ошибке для неопределенного индикатора выполнения.</span><span class="sxs-lookup"><span data-stu-id="0b0b0-115">AccChecker logs this error message for an indeterminate progress bar.</span></span> <span data-ttu-id="0b0b0-116">Можно проигнорировать это сообщение и (или) добавить его в список подавлений.</span><span class="sxs-lookup"><span data-stu-id="0b0b0-116">You can ignore this message and/or add it to the suppressions list.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0b0b0-117">См. также</span><span class="sxs-lookup"><span data-stu-id="0b0b0-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b0b0-118">**UIA \_ контролтипепропертид**</span><span class="sxs-lookup"><span data-stu-id="0b0b0-118">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)
</dt> <dt>

[<span data-ttu-id="0b0b0-119">Общие сведения о типах элементов управления автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="0b0b0-119">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="0b0b0-120">Общие сведения о шаблонах элементов управления модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="0b0b0-120">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 





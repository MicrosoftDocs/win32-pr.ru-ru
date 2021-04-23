---
title: Использование элементов управления ToolTip
description: В этом разделе содержатся примеры, демонстрирующие создание различных типов подсказок.
ms.assetid: 4486b406-a069-4250-b7ab-671d895b79f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86fd4a0cef452be3f9700f8466959043ac8d30b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775560"
---
# <a name="using-tooltip-controls"></a><span data-ttu-id="de0df-103">Использование элементов управления ToolTip</span><span class="sxs-lookup"><span data-stu-id="de0df-103">Using Tooltip Controls</span></span>

<span data-ttu-id="de0df-104">В этом разделе содержатся примеры, демонстрирующие создание различных типов подсказок.</span><span class="sxs-lookup"><span data-stu-id="de0df-104">This section contains examples that demonstrate how to create different types of tooltips.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="de0df-105">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="de0df-105">In this section</span></span>



| <span data-ttu-id="de0df-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="de0df-106">Topic</span></span>                                                                                                    | <span data-ttu-id="de0df-107">Описание</span><span class="sxs-lookup"><span data-stu-id="de0df-107">Description</span></span>                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="de0df-108">Создание подсказки для элемента управления</span><span class="sxs-lookup"><span data-stu-id="de0df-108">How to Create a Tooltip for a Control</span></span>](create-a-tooltip-for-a-control.md)<br/>                   | <span data-ttu-id="de0df-109">Следующий пример функции создает подсказку и связывает ее с элементом управления, чей идентификатор ресурса передается.</span><span class="sxs-lookup"><span data-stu-id="de0df-109">The following example function creates a tooltip and associates it with the control whose resource ID is passed in.</span></span> <br/>                                                                                                                                                  |
| [<span data-ttu-id="de0df-110">Создание всплывающей подсказки для прямоугольной области</span><span class="sxs-lookup"><span data-stu-id="de0df-110">How to Create a Tooltip for a Rectangular Area</span></span>](create-a-tooltip-for-a-rectangular-area.md)<br/> | <span data-ttu-id="de0df-111">В следующем примере показано, как создать стандартный элемент управления ToolTip для всей клиентской области окна.</span><span class="sxs-lookup"><span data-stu-id="de0df-111">The following example demonstrates how to create a standard tooltip control for a window's entire client area.</span></span> <br/>                                                                                                                                                       |
| [<span data-ttu-id="de0df-112">Реализация подсказок отслеживания</span><span class="sxs-lookup"><span data-stu-id="de0df-112">How to Implement Tracking Tooltips</span></span>](implement-tracking-tooltips.md)<br/>                         | <span data-ttu-id="de0df-113">Отслеживание всплывающих подсказок остается видимым, пока приложение не закроет их явным образом, и может динамически изменять расположение на экране.</span><span class="sxs-lookup"><span data-stu-id="de0df-113">Tracking tooltips remain visible until they are explicitly closed by the application, and can change position on the screen dynamically.</span></span> <span data-ttu-id="de0df-114">Они поддерживаются в [версии 4,70](common-control-versions.md) и более поздних стандартных элементах управления.</span><span class="sxs-lookup"><span data-stu-id="de0df-114">They are supported by [version 4.70](common-control-versions.md) and later of the common controls.</span></span> <br/>                         |
| [<span data-ttu-id="de0df-115">Как реализовать многострочные подсказки</span><span class="sxs-lookup"><span data-stu-id="de0df-115">How to Implement Multiline Tooltips</span></span>](implement-multiline-tooltips.md)<br/>                       | <span data-ttu-id="de0df-116">Многострочные подсказки позволяют отображать текст более чем в одной строке.</span><span class="sxs-lookup"><span data-stu-id="de0df-116">Multiline tooltips allow text to be displayed on more than one line.</span></span> <br/>                                                                                                                                                                                                 |
| [<span data-ttu-id="de0df-117">Как реализовать всплывающие подсказки</span><span class="sxs-lookup"><span data-stu-id="de0df-117">How to Implement Balloon Tooltips</span></span>](implement-balloon-tooltips.md)<br/>                           | <span data-ttu-id="de0df-118">Всплывающие подсказки аналогичны стандартным всплывающим подсказкам, но отображаются в виде всплывающей подсказки, указывающей на средство.</span><span class="sxs-lookup"><span data-stu-id="de0df-118">Balloon tooltips are similar to standard tooltips, but are displayed in a cartoon-style "balloon" with a stem pointing to the tool.</span></span> <span data-ttu-id="de0df-119">Всплывающие подсказки могут быть либо однострочными, либо многострочными.</span><span class="sxs-lookup"><span data-stu-id="de0df-119">Balloon tooltips can be either single-line or multiline.</span></span> <span data-ttu-id="de0df-120">Они создаются и обрабатываются во многом так же, как стандартные подсказки.</span><span class="sxs-lookup"><span data-stu-id="de0df-120">They are created and handled in much the same way as standard tooltips.</span></span> <br/> |
| [<span data-ttu-id="de0df-121">Как реализовать подсказки для значков строки состояния</span><span class="sxs-lookup"><span data-stu-id="de0df-121">How to Implement Tooltips for Status Bar Icons</span></span>](implement-tooltips-for-status-bar-icons.md)<br/> | <span data-ttu-id="de0df-122">Неагрессивный способ отобразить пояснительное сообщение для значка строки состояния — реализовать подсказку.</span><span class="sxs-lookup"><span data-stu-id="de0df-122">A nonintrusive way to display an explanatory message for a status bar icon is to implement a tooltip.</span></span> <span data-ttu-id="de0df-123">При щелчке всплывающая подсказка исчезает, но можно также указать значение времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="de0df-123">The tooltip disappears when clicked, but you can also specify a time-out value.</span></span> <br/>                                                                                |
| [<span data-ttu-id="de0df-124">Реализация In-Place подсказок</span><span class="sxs-lookup"><span data-stu-id="de0df-124">How to Implement In-Place Tooltips</span></span>](implement-in-place-tooltips.md)<br/>                         | <span data-ttu-id="de0df-125">Подсказки на месте используются для вывода текстовых строк для объектов, которые были обрезаны.</span><span class="sxs-lookup"><span data-stu-id="de0df-125">In-place tooltips are used to display text strings for objects that have been clipped.</span></span> <span data-ttu-id="de0df-126">Иллюстрация см. в разделе [о элементах управления ToolTip](tooltip-controls.md).</span><span class="sxs-lookup"><span data-stu-id="de0df-126">For an illustration, see [About Tooltip Controls](tooltip-controls.md).</span></span> <br/>                                                                                                      |



 

 

 






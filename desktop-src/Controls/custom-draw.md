---
title: Пользовательская прорисовка
description: Пользовательская прорисовка не является стандартным элементом управления; это служба, которую предоставляет множество стандартных элементов управления.
ms.assetid: vs|controls|~\controls\custdraw\custdraw.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5184d06dbb8e04185bf12a43c6c71dd96b933a6a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986277"
---
# <a name="custom-draw"></a><span data-ttu-id="69d3b-103">Пользовательская прорисовка</span><span class="sxs-lookup"><span data-stu-id="69d3b-103">Custom Draw</span></span>

<span data-ttu-id="69d3b-104">Пользовательская прорисовка не является стандартным элементом управления; это служба, которую предоставляет множество стандартных элементов управления.</span><span class="sxs-lookup"><span data-stu-id="69d3b-104">Custom draw is not a common control; it is a service that many common controls provide.</span></span> <span data-ttu-id="69d3b-105">Пользовательская служба рисования позволяет приложению повысить гибкость при настройке внешнего вида элемента управления.</span><span class="sxs-lookup"><span data-stu-id="69d3b-105">The custom draw service allows an application greater flexibility in customizing a control's appearance.</span></span> <span data-ttu-id="69d3b-106">Приложение может использовать пользовательские уведомления рисования для простого изменения шрифта, используемого для отображения элементов, или ручного рисования элемента без полного рисования владельцем.</span><span class="sxs-lookup"><span data-stu-id="69d3b-106">Your application can harness custom draw notifications to easily change the font used to display items or manually draw an item without having to do a full owner draw.</span></span>

<span data-ttu-id="69d3b-107">В этом разделе содержатся сведения об элементах программирования, используемых с пользовательской прорисовкой.</span><span class="sxs-lookup"><span data-stu-id="69d3b-107">This section contains information about the programming elements used with custom draw.</span></span>

## <a name="overviews"></a><span data-ttu-id="69d3b-108">Разделы общих сведений</span><span class="sxs-lookup"><span data-stu-id="69d3b-108">Overviews</span></span>



| <span data-ttu-id="69d3b-109">Раздел</span><span class="sxs-lookup"><span data-stu-id="69d3b-109">Topic</span></span>                                      | <span data-ttu-id="69d3b-110">Содержимое</span><span class="sxs-lookup"><span data-stu-id="69d3b-110">Contents</span></span>                                                                                                                                                               |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="69d3b-111">О пользовательской прорисовке</span><span class="sxs-lookup"><span data-stu-id="69d3b-111">About Custom Draw</span></span>](about-custom-draw.md) | <span data-ttu-id="69d3b-112">В этом разделе содержатся общие сведения о пользовательской функции рисования и дается концептуальный обзор того, как приложение может поддерживать пользовательскую прорисовку.</span><span class="sxs-lookup"><span data-stu-id="69d3b-112">This section contains general information about custom draw functionality and provides a conceptual overview of how an application can support custom draw.</span></span><br/> |
| [<span data-ttu-id="69d3b-113">Использование пользовательского рисования</span><span class="sxs-lookup"><span data-stu-id="69d3b-113">Using Custom Draw</span></span>](using-custom-draw.md) | <span data-ttu-id="69d3b-114">В этом разделе содержатся примеры, демонстрирующие реализацию пользовательского рисования.</span><span class="sxs-lookup"><span data-stu-id="69d3b-114">This section contains examples that demonstrate how to implement custom draw.</span></span> <br/>                                                                              |



 

## <a name="notifications"></a><span data-ttu-id="69d3b-115">Уведомления</span><span class="sxs-lookup"><span data-stu-id="69d3b-115">Notifications</span></span>



| <span data-ttu-id="69d3b-116">Раздел</span><span class="sxs-lookup"><span data-stu-id="69d3b-116">Topic</span></span>                               | <span data-ttu-id="69d3b-117">Содержимое</span><span class="sxs-lookup"><span data-stu-id="69d3b-117">Contents</span></span>                                                                                                                                                                 |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="69d3b-118">NM \_ кустомдрав</span><span class="sxs-lookup"><span data-stu-id="69d3b-118">NM\_CUSTOMDRAW</span></span>](nm-customdraw.md) | <span data-ttu-id="69d3b-119">Сообщает родительскому окну элемента управления о пользовательских операциях рисования.</span><span class="sxs-lookup"><span data-stu-id="69d3b-119">Notifies a control's parent window about custom drawing operations.</span></span> <span data-ttu-id="69d3b-120">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="69d3b-120">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span> <br/> |



 

## <a name="structures"></a><span data-ttu-id="69d3b-121">Структуры</span><span class="sxs-lookup"><span data-stu-id="69d3b-121">Structures</span></span>



| <span data-ttu-id="69d3b-122">Раздел</span><span class="sxs-lookup"><span data-stu-id="69d3b-122">Topic</span></span>                                | <span data-ttu-id="69d3b-123">Содержимое</span><span class="sxs-lookup"><span data-stu-id="69d3b-123">Contents</span></span>                                                                                              |
|--------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="69d3b-124">**нмкустомдрав**</span><span class="sxs-lookup"><span data-stu-id="69d3b-124">**NMCUSTOMDRAW**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) | <span data-ttu-id="69d3b-125">Содержит сведения, относящиеся к коду уведомления [NM \_ кустомдрав](nm-customdraw.md) .</span><span class="sxs-lookup"><span data-stu-id="69d3b-125">Contains information specific to an [NM\_CUSTOMDRAW](nm-customdraw.md) notification code.</span></span><br/> |



 

 

 






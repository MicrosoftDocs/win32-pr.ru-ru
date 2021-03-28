---
description: Контекст родительского устройства позволяет приложению максимально сокращать время, необходимое для настройки области отсечения для окна.
ms.assetid: 194d5add-d1a1-4c10-89ee-171ff008a7ab
title: Контексты отображаемых родительских устройств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e423ceaa65790df35fa55c8dda597cb1bb45019
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984881"
---
# <a name="parent-display-device-contexts"></a><span data-ttu-id="78115-103">Контексты отображаемых родительских устройств</span><span class="sxs-lookup"><span data-stu-id="78115-103">Parent Display Device Contexts</span></span>

<span data-ttu-id="78115-104">*Контекст родительского устройства* позволяет приложению максимально сокращать время, необходимое для настройки области отсечения для окна.</span><span class="sxs-lookup"><span data-stu-id="78115-104">A *parent device context* enables an application to minimize the time necessary to set up the clipping region for a window.</span></span> <span data-ttu-id="78115-105">В приложении обычно используются родительские контексты устройств для ускорения рисования окон элементов управления без необходимости использовать частный контекст или контекста устройства класса.</span><span class="sxs-lookup"><span data-stu-id="78115-105">An application typically uses parent device contexts to speed up drawing for control windows without requiring a private or class device context.</span></span> <span data-ttu-id="78115-106">Например, система использует родительские контексты устройств для кнопок "Отправить" и "Изменить".</span><span class="sxs-lookup"><span data-stu-id="78115-106">For example, the system uses parent device contexts for push button and edit controls.</span></span> <span data-ttu-id="78115-107">Контексты родительских устройств предназначены для использования только с дочерними окнами, но никогда не с окнами верхнего уровня или всплывающих окон.</span><span class="sxs-lookup"><span data-stu-id="78115-107">Parent device contexts are intended for use with child windows only, never with top-level or pop-up windows.</span></span>

<span data-ttu-id="78115-108">Приложение может указать \_ стиль CS парентдк, чтобы задать в качестве вырезанной области дочернего окна родительское окно, чтобы дочерний элемент мог рисовать в родительском окне.</span><span class="sxs-lookup"><span data-stu-id="78115-108">An application can specify the CS\_PARENTDC style to set the clipping region of the child window to that of the parent window so that the child can draw in the parent.</span></span> <span data-ttu-id="78115-109">Указание CS \_ парентдк повышает производительность приложения, так как системе не нужно выполнять повторное вычисление видимой области для каждого дочернего окна.</span><span class="sxs-lookup"><span data-stu-id="78115-109">Specifying CS\_PARENTDC enhances an application's performance because the system doesn't need to keep recalculating the visible region for each child window.</span></span>

<span data-ttu-id="78115-110">Значения атрибутов, заданные родительским окном, не сохраняются для дочернего окна; Например, родительское окно не может задать кисть для своих дочерних окон.</span><span class="sxs-lookup"><span data-stu-id="78115-110">Attribute values set by the parent window are not preserved for the child window; for example, the parent window cannot set the brush for its child windows.</span></span> <span data-ttu-id="78115-111">Единственным сохраненным свойством является отсеченная область.</span><span class="sxs-lookup"><span data-stu-id="78115-111">The only property preserved is the clipping region.</span></span> <span data-ttu-id="78115-112">Окно должно отсекать свои выходные данные с ограничениями окна.</span><span class="sxs-lookup"><span data-stu-id="78115-112">The window must clip its own output to the limits of the window.</span></span> <span data-ttu-id="78115-113">Поскольку вырезанная область для контекста родительского устройства идентична родительскому окну, дочернее окно может нарисоваться во всем родительском окне, но контекст родительского устройства не должен использоваться таким образом.</span><span class="sxs-lookup"><span data-stu-id="78115-113">Because the clipping region for the parent device context is identical to the parent window, the child window can potentially draw over the entire parent window, but the parent device context must not be used in this way.</span></span>

<span data-ttu-id="78115-114">Система пропускает \_ стиль CS парентдк, если в родительском окне используется закрытый контекст устройства или контекста класса, если родительское окно записывает свои дочерние окна или если дочернее окно обрезает свои дочерние окна или одноуровневые окна.</span><span class="sxs-lookup"><span data-stu-id="78115-114">The system ignores the CS\_PARENTDC style if the parent window uses a private or class device context, if the parent window clips its child windows, or if the child window clips its child windows or sibling windows.</span></span>

 

 




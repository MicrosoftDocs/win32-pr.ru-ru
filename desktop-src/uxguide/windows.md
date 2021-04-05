---
title: Windows (основы разработки)
description: Windows — это основной \ 0034; холсты \ 0034; или области пользовательского интерфейса для классического приложения, включая основные окна и всплывающие окна, диалоги и мастера. При принятии решения о том, какую поверхность использовать и как лучше ее использовать, следуйте этим рекомендациям.
ms.assetid: E1FA78DA-D580-4B0E-AB59-29F013278766
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 5b7bb58750635af25d49208992d5583c44520a04
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "103999835"
---
# <a name="windows-design-basics"></a><span data-ttu-id="1ca4f-104">Windows (основы разработки)</span><span class="sxs-lookup"><span data-stu-id="1ca4f-104">Windows (Design basics)</span></span>

> [!NOTE]
> <span data-ttu-id="1ca4f-105">Это руководство по проектированию было создано для Windows 7 и не Обновлено для более новых версий Windows.</span><span class="sxs-lookup"><span data-stu-id="1ca4f-105">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="1ca4f-106">Многие рекомендации по-прежнему применяются в принципе, но презентация и примеры не соответствуют нашим [текущим руководствам по проектированию](/windows/uwp/design/).</span><span class="sxs-lookup"><span data-stu-id="1ca4f-106">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="1ca4f-107">Windows — это основные поверхности пользовательского интерфейса для классического приложения, включая основные окна и всплывающие окна, диалоги и мастера.</span><span class="sxs-lookup"><span data-stu-id="1ca4f-107">Windows are the main "canvases" or UI surfaces of your desktop app, including the main windows itself and pop-ups, dialogs, and wizards.</span></span> <span data-ttu-id="1ca4f-108">При принятии решения о том, какую поверхность использовать и как лучше ее использовать, следуйте этим рекомендациям.</span><span class="sxs-lookup"><span data-stu-id="1ca4f-108">Follow these guidelines when deciding which surface to use and how best to use them.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1ca4f-109">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="1ca4f-109">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1ca4f-110">Раздел</span><span class="sxs-lookup"><span data-stu-id="1ca4f-110">Topic</span></span></th>
<th><span data-ttu-id="1ca4f-111">Описание</span><span class="sxs-lookup"><span data-stu-id="1ca4f-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1ca4f-112"><a href="win-window-mgt.md">Управление окнами</a></span><span class="sxs-lookup"><span data-stu-id="1ca4f-112"><a href="win-window-mgt.md">Window Management</a></span></span><br/></td>
<td><span data-ttu-id="1ca4f-113">В этой статье описывается размещение окон по умолчанию при первоначальном отображении на экране, порядок их размещения относительно других окон (<a href="glossary.md">Z-порядок</a>), их первоначальный размер и влияние на фокус ввода.</span><span class="sxs-lookup"><span data-stu-id="1ca4f-113">This article covers default placement of windows when initially displayed on the screen, their stacking order relative to other windows (<a href="glossary.md">Z order</a>), their initial size, and how their display affects input focus.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1ca4f-114"><a href="win-window-frames.md">Фреймы окна</a></span><span class="sxs-lookup"><span data-stu-id="1ca4f-114"><a href="win-window-frames.md">Window Frames</a></span></span><br/></td>
<td><span data-ttu-id="1ca4f-115">Большинство программ должны использовать стандартные рамки окон.</span><span class="sxs-lookup"><span data-stu-id="1ca4f-115">Most programs should use standard window frames.</span></span> <span data-ttu-id="1ca4f-116">Иммерсивное приложение может иметь полноэкранный режим, который скрывает рамку окна.</span><span class="sxs-lookup"><span data-stu-id="1ca4f-116">Immersive applications can have a full screen mode that hides the window frame.</span></span> <span data-ttu-id="1ca4f-117">Рассмотрите возможность использования "стратегического" для упрощения, более простого и более единообразного вида.</span><span class="sxs-lookup"><span data-stu-id="1ca4f-117">Consider using glass strategically for a simpler, lighter, more cohesive look.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1ca4f-118"><a href="win-dialog-box.md">Диалоговые окна</a></span><span class="sxs-lookup"><span data-stu-id="1ca4f-118"><a href="win-dialog-box.md">Dialog Boxes</a></span></span><br/></td>
<td><span data-ttu-id="1ca4f-119">Диалоговое окно — это дополнительное окно, которое позволяет пользователям выполнять команду, запрашивает у пользователя вопрос или предоставляет пользователям сведения или отзывы о ходе выполнения.</span><span class="sxs-lookup"><span data-stu-id="1ca4f-119">A dialog box is a secondary window that allows users to perform a command, asks users a question, or provides users with information or progress feedback.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1ca4f-120"><a href="win-common-dlg.md">Общие диалоговые окна</a></span><span class="sxs-lookup"><span data-stu-id="1ca4f-120"><a href="win-common-dlg.md">Common Dialogs</a></span></span><br/></td>
<td><span data-ttu-id="1ca4f-121">Общие диалоговые окна Microsoft Windows состоят из диалоговых окон Открытие файла, сохранение файла, открытие папки, Поиск и замена, печать, Настройка страницы, шрифт и цвет.</span><span class="sxs-lookup"><span data-stu-id="1ca4f-121">The Microsoft Windows common dialogs consist of the Open File, Save File, Open Folder, Find and Replace, Print, Page Setup, Font, and Color dialog boxes.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1ca4f-122"><a href="win-wizards.md">Мастеры</a></span><span class="sxs-lookup"><span data-stu-id="1ca4f-122"><a href="win-wizards.md">Wizards</a></span></span><br/></td>
<td><span data-ttu-id="1ca4f-123">Несмотря на то, что замечательно, замысловатое имя, мастера не являются специальными формами пользовательского интерфейса и имеют только определенный диапазон служебной программы.</span><span class="sxs-lookup"><span data-stu-id="1ca4f-123">Despite that wonderful, whimsical name, wizards are not really a special form of user interface, and they have only a particular range of utility.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1ca4f-124"><a href="win-property-win.md">Окна свойств</a></span><span class="sxs-lookup"><span data-stu-id="1ca4f-124"><a href="win-property-win.md">Property Windows</a></span></span><br/></td>
<td><span data-ttu-id="1ca4f-125">Окно свойств — это совокупное имя для следующих типов пользовательских интерфейсов (UI):</span><span class="sxs-lookup"><span data-stu-id="1ca4f-125">Property window is the collective name for the following types of user interfaces (UIs):</span></span><br/>
<ul>
<li><span data-ttu-id="1ca4f-126">Страница свойств: используется для <strong>просмотра и изменения свойств объекта или коллекции объектов в диалоговом окне</strong>.</span><span class="sxs-lookup"><span data-stu-id="1ca4f-126">Property sheet: used to <strong>view and change properties for an object or collection of objects in a dialog box</strong>.</span></span></li>
<li><span data-ttu-id="1ca4f-127">Инспектор свойств. используется для <strong>просмотра и изменения свойств объекта или коллекции объектов на панели</strong>.</span><span class="sxs-lookup"><span data-stu-id="1ca4f-127">Property inspector: used to <strong>view and change properties for an object or collection of objects in a pane</strong>.</span></span></li>
<li><span data-ttu-id="1ca4f-128">Диалоговое окно "Параметры" — используется для <strong>просмотра и изменения параметров приложения</strong>.</span><span class="sxs-lookup"><span data-stu-id="1ca4f-128">Options dialog box: used to <strong>view and change options for an application</strong>.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

 


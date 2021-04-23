---
description: Общие сведения о отображении панели ввода.
ms.assetid: 6301dde1-e46b-42a0-ae0b-ccd984e9199b
title: Отображение панели ввода
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1fa8404cadd7c40b0185d60b574ac7d8ec77ced
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703329"
---
# <a name="displaying-the-input-panel"></a><span data-ttu-id="20fce-103">Отображение панели ввода</span><span class="sxs-lookup"><span data-stu-id="20fce-103">Displaying the Input Panel</span></span>

<span data-ttu-id="20fce-104">\[[**Пенинпутпанел**](peninputpanel-class.md) был заменен [**текстинпутпанел**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) ([Microsoft. Ink. TextInput](/previous-versions/dotnet/netframework-3.5/ms581554(v=vs.90)) для управляемого кода).</span><span class="sxs-lookup"><span data-stu-id="20fce-104">\[[**PenInputPanel**](peninputpanel-class.md) has been replaced by [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) ([Microsoft.Ink.TextInput](/previous-versions/dotnet/netframework-3.5/ms581554(v=vs.90)) for managed code).</span></span> <span data-ttu-id="20fce-105">Дополнительные сведения см. в разделе [Программирование панели ввода текста](programming-the-text-input-panel.md).\]</span><span class="sxs-lookup"><span data-stu-id="20fce-105">Please refer to the [Programming the Text Input Panel](programming-the-text-input-panel.md).\]</span></span>

<span data-ttu-id="20fce-106">Порядок различных событий фокуса для элемента управления выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="20fce-106">The order of the various focus events for a control is as follows:</span></span>

-   [<span data-ttu-id="20fce-107">Control. Enter</span><span class="sxs-lookup"><span data-stu-id="20fce-107">Control.Enter</span></span>](/dotnet/api/system.windows.forms.control.enter?view=netcore-3.1)
-   [<span data-ttu-id="20fce-108">Control. GotFocus</span><span class="sxs-lookup"><span data-stu-id="20fce-108">Control.GotFocus</span></span>](/dotnet/api/system.windows.forms.control.gotfocus?view=netcore-3.1)
-   [<span data-ttu-id="20fce-109">Control. Leave</span><span class="sxs-lookup"><span data-stu-id="20fce-109">Control.Leave</span></span>](/dotnet/api/system.windows.forms.control.leave?view=netcore-3.1)
-   [<span data-ttu-id="20fce-110">Control. Проверка</span><span class="sxs-lookup"><span data-stu-id="20fce-110">Control.Validating</span></span>](/dotnet/api/system.windows.forms.control.validating?view=netcore-3.1)
-   [<span data-ttu-id="20fce-111">Control. Validated</span><span class="sxs-lookup"><span data-stu-id="20fce-111">Control.Validated</span></span>](/dotnet/api/system.windows.forms.control.validated?view=netcore-3.1)
-   [<span data-ttu-id="20fce-112">Control. LostFocus</span><span class="sxs-lookup"><span data-stu-id="20fce-112">Control.LostFocus</span></span>](/dotnet/api/system.windows.forms.control.lostfocus?view=netcore-3.1)

<span data-ttu-id="20fce-113">Нет никакой гарантии, что элемент управления на самом деле имеет фокус на момент, когда свойство [Control. Visible](/dotnet/api/system.windows.forms.control.visible?view=netcore-3.1) записывается, когда оно задано в обработчике событий [Control. Enter](/dotnet/api/system.windows.forms.control.enter?view=netcore-3.1) .</span><span class="sxs-lookup"><span data-stu-id="20fce-113">There is no guarantee that the control actually has focus by the time the [Control.Visible](/dotnet/api/system.windows.forms.control.visible?view=netcore-3.1) property is written when it is set in the [Control.Enter](/dotnet/api/system.windows.forms.control.enter?view=netcore-3.1) event handler.</span></span> <span data-ttu-id="20fce-114">Событие Control. Enter является лучшим местом для присоединения объекта [пенинпутпанел](/previous-versions/ms583923(v=vs.100)) к элементу управления, но событие [Control. GotFocus](/dotnet/api/system.windows.forms.control.gotfocus?view=netcore-3.1) является лучшим местом для изменения свойства [пенинпутпанел. Visible](/previous-versions/ms571984(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="20fce-114">The Control.Enter event is the best place to attach the [PenInputPanel](/previous-versions/ms583923(v=vs.100)) object to a control, but the [Control.GotFocus](/dotnet/api/system.windows.forms.control.gotfocus?view=netcore-3.1) event is the best place to change the [PenInputPanel.Visible](/previous-versions/ms571984(v=vs.100)) property.</span></span>

 

 

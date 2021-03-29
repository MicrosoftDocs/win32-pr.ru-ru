---
description: Описывает использование объекта Пенинпутпанел с полями со списком.
ms.assetid: 19902bfa-504e-40cd-882a-4fac4bb7daf6
title: Использование Пенинпутпанел с полями со списком
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c5306708fd00871f07b241ca777e672e2d3de94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809598"
---
# <a name="using-the-peninputpanel-with-combo-boxes"></a><span data-ttu-id="4c44d-103">Использование Пенинпутпанел с полями со списком</span><span class="sxs-lookup"><span data-stu-id="4c44d-103">Using the PenInputPanel with Combo Boxes</span></span>

<span data-ttu-id="4c44d-104">\[Объект [пенинпутпанел](/previous-versions/aa514041(v=msdn.10)) был заменен [Microsoft. Ink. TextInput](/previous-versions/ms581554(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="4c44d-104">\[The [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object has been replaced by [Microsoft.Ink.TextInput](/previous-versions/ms581554(v=vs.100)).</span></span> <span data-ttu-id="4c44d-105">Дополнительные сведения см. в разделе [Программирование панели ввода текста](programming-the-text-input-panel.md).\]</span><span class="sxs-lookup"><span data-stu-id="4c44d-105">Please refer to the [Programming the Text Input Panel](programming-the-text-input-panel.md).\]</span></span>

<span data-ttu-id="4c44d-106">Если вы присоединяете объект [пенинпутпанел](/previous-versions/aa514041(v=msdn.10)) к элементу управления [ComboBox](/dotnet/api/system.windows.forms.combobox?view=netcore-3.1) , коснитесь пера планшета в поле со списком изменить элемент управления во время выполнения, объект пенинпутпанел не отображается.</span><span class="sxs-lookup"><span data-stu-id="4c44d-106">If you attach a [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object to a [ComboBox](/dotnet/api/system.windows.forms.combobox?view=netcore-3.1) control, then tap your tablet pen on the edit control portion combo box at runtime, the PenInputPanel object does not appear.</span></span> <span data-ttu-id="4c44d-107">Однако он отображается при нажатии кнопки со стрелкой раскрывающегося списка.</span><span class="sxs-lookup"><span data-stu-id="4c44d-107">However, it does appear if you tap on the dropdown arrow.</span></span> <span data-ttu-id="4c44d-108">Это связано с тем, что окно элемента управления редактирования в поле со списком не является окном, которое получает сообщения пера.</span><span class="sxs-lookup"><span data-stu-id="4c44d-108">This is because the window of the edit control in the combo box is not the window that receives pen messages.</span></span> <span data-ttu-id="4c44d-109">Поля со списками имеют дочерние окна редактирования.</span><span class="sxs-lookup"><span data-stu-id="4c44d-109">Combo boxes have a child edit window.</span></span> <span data-ttu-id="4c44d-110">Решение этой проблемы заключается в том, чтобы определить, имеет ли окно, к которому присоединен объект Пенинпутпанел, дочернее окно.</span><span class="sxs-lookup"><span data-stu-id="4c44d-110">The solution to this problem is to determine whether the window the PenInputPanel object is attached to has a child window.</span></span> <span data-ttu-id="4c44d-111">В этом случае можно присоединить объект Пенинпутпанел к дочернему окну.</span><span class="sxs-lookup"><span data-stu-id="4c44d-111">If so, you can attach the PenInputPanel object to the child window.</span></span>

<span data-ttu-id="4c44d-112">Установка значения-1 для свойства [VerticalOffset](/previous-versions/ms571983(v=vs.100)) объекта [пенинпутпанел](/previous-versions/aa514041(v=msdn.10)) приводит к отображению панели поверх поля со списком.</span><span class="sxs-lookup"><span data-stu-id="4c44d-112">Setting the [VerticalOffset](/previous-versions/ms571983(v=vs.100)) property of the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object to a value of -1 makes the panel appear on top of the combo box.</span></span>

 

 

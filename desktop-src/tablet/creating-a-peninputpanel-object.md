---
description: Описывает, как создать объект Пенинпутпанел.
ms.assetid: fd9ce912-5cec-4bec-b7d8-5a4f71000c95
title: Создание объекта Пенинпутпанел
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4072d5dca28801ee45b7747504a93d755443cfb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692044"
---
# <a name="creating-a-peninputpanel-object"></a><span data-ttu-id="9cb7d-103">Создание объекта Пенинпутпанел</span><span class="sxs-lookup"><span data-stu-id="9cb7d-103">Creating a PenInputPanel Object</span></span>

<span data-ttu-id="9cb7d-104">\[[**Пенинпутпанел**](peninputpanel-class.md) заменен на [**текстинпутпанел**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) и [Microsoft. Ink. TextInput](/previous-versions/dotnet/netframework-3.5/ms581554(v=vs.90)).</span><span class="sxs-lookup"><span data-stu-id="9cb7d-104">\[[**PenInputPanel**](peninputpanel-class.md) has been replaced by [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) and [Microsoft.Ink.TextInput](/previous-versions/dotnet/netframework-3.5/ms581554(v=vs.90)).</span></span> <span data-ttu-id="9cb7d-105">Дополнительные сведения см. в разделе [Программирование панели ввода текста](programming-the-text-input-panel.md).\]</span><span class="sxs-lookup"><span data-stu-id="9cb7d-105">Please refer to the [Programming the Text Input Panel](programming-the-text-input-panel.md).\]</span></span>

<span data-ttu-id="9cb7d-106">Конструкторы управляемого кода предоставляют удобный способ создания объекта [пенинпутпанел](/previous-versions/ms583923(v=vs.100)) и его присоединения к элементу управления за один шаг.</span><span class="sxs-lookup"><span data-stu-id="9cb7d-106">Managed code constructors provide a convenient way to create a [PenInputPanel](/previous-versions/ms583923(v=vs.100)) object and attach it to a control in one step.</span></span> <span data-ttu-id="9cb7d-107">В этом \# примере на языке C создается объект пенинпутпанел и прикрепляется к существующему элементу управления [InkEdit](/previous-versions/ms835842(v=msdn.10)) `InkEdit1` с одной строкой кода.</span><span class="sxs-lookup"><span data-stu-id="9cb7d-107">This C\# example creates a PenInputPanel object and attaches it to an existing [InkEdit](/previous-versions/ms835842(v=msdn.10)) control, `InkEdit1`, with one line of code.</span></span>


```C++
PenInputPanel thePenInputPanel = new PenInputPanel(InkEdit1);
```



<span data-ttu-id="9cb7d-108">Тот же пример в Visual Basic .NET выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="9cb7d-108">The same example in Visual Basic .NET looks like this:</span></span>


```C++
Dim thePenInputPanel As New PenInputPanel(InkEdit1)
```



<span data-ttu-id="9cb7d-109">Этот метод полезен в случаях, когда один объект [пенинпутпанел](/previous-versions/ms583923(v=vs.100)) будет связан с одним элементом управления в течение его жизненного цикла.</span><span class="sxs-lookup"><span data-stu-id="9cb7d-109">This technique is useful in cases where one [PenInputPanel](/previous-versions/ms583923(v=vs.100)) object will be associated with a single control throughout its lifetime.</span></span> <span data-ttu-id="9cb7d-110">В случаях, когда необходимо использовать один объект Пенинпутпанел и связать его с несколькими элементами управления, как показано в [примере пенинпутпанел](peninputpanel-sample.md), используйте свойство [аттачедедитконтрол](/previous-versions/ms582239(v=vs.100)) , чтобы изменить элемент управления, с которым связан объект пенинпутпанел.</span><span class="sxs-lookup"><span data-stu-id="9cb7d-110">In cases where you want to use one PenInputPanel object and associate it with multiple controls, as demonstrated in the [PenInputPanel Sample](peninputpanel-sample.md), use the [AttachedEditControl](/previous-versions/ms582239(v=vs.100)) property to change the control to which the PenInputPanel object is associated.</span></span>

<span data-ttu-id="9cb7d-111">Чтобы присоединить объект [пенинпутпанел](/previous-versions/ms583923(v=vs.100)) к элементу управления без использования конструктора, используйте свойство [аттачедедитконтрол](/previous-versions/ms582239(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="9cb7d-111">To attach a [PenInputPanel](/previous-versions/ms583923(v=vs.100)) object to a control without using a constructor, use the [AttachedEditControl](/previous-versions/ms582239(v=vs.100)) property.</span></span> <span data-ttu-id="9cb7d-112">Используйте этот метод для языков, которые не поддерживают управляемые конструкторы, такие как C++.</span><span class="sxs-lookup"><span data-stu-id="9cb7d-112">Use this technique for languages that do not support the managed constructors, such as C++.</span></span>

 

 

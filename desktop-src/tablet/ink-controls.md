---
description: Обзор элементов управления рукописным вводом для планшетных ПК.
ms.assetid: 03229b86-f59b-4946-8816-fa153af57630
title: Элементы управления рукописным вводом
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1206c5e77c12c31a80dcfbca0bebf317a28e0e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541314"
---
# <a name="ink-controls"></a><span data-ttu-id="ae05a-103">Элементы управления рукописным вводом</span><span class="sxs-lookup"><span data-stu-id="ae05a-103">Ink Controls</span></span>

<span data-ttu-id="ae05a-104">Платформа Tablet PC предоставляет два элемента управления: [InkEdit](inkedit-control.md) и [InkPicture](inkpicture-control.md), которые позволяют легко добавлять рукописные данные и распознавание рукописного ввода в приложения для планшетных ПК.</span><span class="sxs-lookup"><span data-stu-id="ae05a-104">The Tablet PC platform provides two controls, [InkEdit](inkedit-control.md) and [InkPicture](inkpicture-control.md), which enable you to easily add ink and handwriting recognition to Tablet PC applications.</span></span> <span data-ttu-id="ae05a-105">Элемент управления InkEdit имеет версии [Managed](/previous-versions/ms835842(v=msdn.10)), [ActiveX](inkedit-control-reference.md) и Win32, в то время как InkPicture имеет только управляемые версии [InkPicture](/previous-versions/ms583740(v=vs.100)) и [ActiveX](inkpicture-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="ae05a-105">The InkEdit control has [managed](/previous-versions/ms835842(v=msdn.10)), [ActiveX](inkedit-control-reference.md) , and Win32 versions, while InkPicture has only the managed [InkPicture](/previous-versions/ms583740(v=vs.100)) and [ActiveX](inkpicture-control-reference.md) versions.</span></span>

<span data-ttu-id="ae05a-106">Основное различие между элементами управления заключается в том, как сохраняются данные.</span><span class="sxs-lookup"><span data-stu-id="ae05a-106">The key difference between the controls is in how data is saved.</span></span> <span data-ttu-id="ae05a-107">Элемент управления [InkEdit](inkedit-control.md) сохраняет рукописные данные в виде текста по умолчанию, а в процессе [InkPicture](inkpicture-control.md) рукописный ввод сохраняется.</span><span class="sxs-lookup"><span data-stu-id="ae05a-107">The [InkEdit](inkedit-control.md) control saves ink as text by default, while [InkPicture](inkpicture-control.md) saves ink as ink.</span></span>

<span data-ttu-id="ae05a-108">Элемент управления [InkEdit](inkedit-control.md) предназначен для ввода текста с помощью распознавания рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="ae05a-108">The [InkEdit](inkedit-control.md) control is intended for text entry through handwriting recognition.</span></span> <span data-ttu-id="ae05a-109">[InkPicture](inkpicture-control.md) предназначен для аннотации (например, при пометке слайда презентации или другого изображения).</span><span class="sxs-lookup"><span data-stu-id="ae05a-109">[InkPicture](inkpicture-control.md) is intended for annotation (for example, marking up a presentation slide or other picture).</span></span>

<span data-ttu-id="ae05a-110">В управляемом коде создайте элементы управления рукописным вводом в том же потоке, что и основной поток для формы.</span><span class="sxs-lookup"><span data-stu-id="ae05a-110">In managed code, create ink controls in the same thread as the main thread for the form.</span></span> <span data-ttu-id="ae05a-111">Если элемент управления [InkEdit](inkedit-control.md) или [InkPicture](inkpicture-control.md) создается в другом потоке, приложение может не реагировать должным образом.</span><span class="sxs-lookup"><span data-stu-id="ae05a-111">If an [InkEdit](inkedit-control.md) or [InkPicture](inkpicture-control.md) control is created in a different thread, then your application may not respond properly.</span></span>

<span data-ttu-id="ae05a-112">Перед созданием элемента управления рукописного ввода необходимо явно изменить модель потоков на подразделение с одним потоком (STA).</span><span class="sxs-lookup"><span data-stu-id="ae05a-112">You should explicitly change the threading model to single-thread apartment (STA) before creating an ink control.</span></span> <span data-ttu-id="ae05a-113">Это приводит к тому, что элемент управления создается в основном потоке.</span><span class="sxs-lookup"><span data-stu-id="ae05a-113">This causes the control to be created on the main thread.</span></span> <span data-ttu-id="ae05a-114">Для явной установки потоковой модели можно использовать следующий управляемый код C++.</span><span class="sxs-lookup"><span data-stu-id="ae05a-114">You can use the following Managed C++ code to explicitly set the threading model.</span></span>


```C++
Thread::get_CurrentThread()->set_ApartmentState(ApartmentState::STA);
```



<span data-ttu-id="ae05a-115">Для того же результата в C можно использовать следующий код \# .</span><span class="sxs-lookup"><span data-stu-id="ae05a-115">You can use the following code to do the same thing in C\#.</span></span>


```C++
System.Threading.Thread.CurrentThread.ApartmentState = System.Threading.ApartmentState.STA;
```



<span data-ttu-id="ae05a-116">Чтобы избежать утечки памяти в управляемом коде, необходимо явным образом вызвать метод [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) на любом элементе управления Tablet PC, к которому был присоединен обработчик событий, прежде чем элемент управления выходит из области действия.</span><span class="sxs-lookup"><span data-stu-id="ae05a-116">In managed code, to avoid a memory leak you must explicitly call the [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method on any Tablet PC control to which an event handler has been attached before the control goes out of scope.</span></span>

<span data-ttu-id="ae05a-117">В следующих разделах описываются элементы управления рукописного ввода и использование элементов управления рукописного ввода в приложениях.</span><span class="sxs-lookup"><span data-stu-id="ae05a-117">The following sections describe ink controls and the use of ink controls in applications:</span></span>

-   [<span data-ttu-id="ae05a-118">Добавление элементов управления рукописного ввода в проект</span><span class="sxs-lookup"><span data-stu-id="ae05a-118">Adding Ink Controls to a Project</span></span>](adding-ink-controls-to-a-project.md)
-   [<span data-ttu-id="ae05a-119">Элемент управления InkEdit</span><span class="sxs-lookup"><span data-stu-id="ae05a-119">InkEdit Control</span></span>](inkedit-control.md)
-   [<span data-ttu-id="ae05a-120">Элемент управления InkPicture</span><span class="sxs-lookup"><span data-stu-id="ae05a-120">InkPicture Control</span></span>](inkpicture-control.md)

 

 

---
title: Перевод в Visual Basic
description: Перевод в Visual Basic
ms.assetid: 48672d0c-b0d7-4820-91d4-d985030396f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c45e7beedaaa3983b1be1503b5ce443a3adf4d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888636"
---
# <a name="translating-to-visual-basic"></a><span data-ttu-id="416ee-103">Перевод в Visual Basic</span><span class="sxs-lookup"><span data-stu-id="416ee-103">Translating to Visual Basic</span></span>

<span data-ttu-id="416ee-104">Вы можете добавить COM-объект в проект Visual Basic либо в виде ссылки, либо в виде компонента.</span><span class="sxs-lookup"><span data-stu-id="416ee-104">You can add a COM object to your Visual Basic project either as a reference or a component.</span></span> <span data-ttu-id="416ee-105">После добавления объекта в проект приложение может получить доступ к его классам и интерфейсам.</span><span class="sxs-lookup"><span data-stu-id="416ee-105">Once the object is added to your project, your application can access its classes and interfaces.</span></span> <span data-ttu-id="416ee-106">Затем можно использовать обозреватель объектов Visual Basic для просмотра сведений о библиотеке типов объекта в синтаксисе Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="416ee-106">You can then use the Visual Basic Object Browser to view the object's type library information in Visual Basic syntax.</span></span>

<span data-ttu-id="416ee-107">Как правило, элементы управления добавляются в проект в виде компонентов, а неэлементы управления добавляются в качестве ссылок.</span><span class="sxs-lookup"><span data-stu-id="416ee-107">Typically, controls are added to a project as a components and noncontrols are added as references.</span></span> <span data-ttu-id="416ee-108">Когда COM-объект добавляется в качестве компонента, он отображается на панели элементов Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="416ee-108">When a COM object is added as a component, it appears in the Visual Basic toolbox.</span></span> <span data-ttu-id="416ee-109">Новые экземпляры этого объекта создаются путем перетаскивания значка объекта с панели элементов на Visual Basic форму или контейнер другого типа.</span><span class="sxs-lookup"><span data-stu-id="416ee-109">New instances of that object are created by dragging the object icon from the toolbox onto a Visual Basic form or other type of container.</span></span> <span data-ttu-id="416ee-110">Новые экземпляры COM-объектов, добавленные в виде ссылок, создаются с помощью ключевого слова **New** .</span><span class="sxs-lookup"><span data-stu-id="416ee-110">New instances of COM objects added as references are created using the **new** keyword.</span></span>

<span data-ttu-id="416ee-111">Различие между использованием класса в качестве ссылки и компонента является неочевидным, но важным.</span><span class="sxs-lookup"><span data-stu-id="416ee-111">The distinction between using a class as a reference versus a component is subtle but important.</span></span> <span data-ttu-id="416ee-112">При добавлении объекта в качестве ссылки можно использовать только библиотеку типов, которую предоставляет элемент управления, или библиотеку типов "RAW".</span><span class="sxs-lookup"><span data-stu-id="416ee-112">When you add an object as a reference, you can use only the type library that the control provides, or the "raw" type library.</span></span>

<span data-ttu-id="416ee-113">При добавлении элемента управления в качестве компонента Visual Basic выполняет слияние свойств и методов расширителя формы, в которой элемент управления внедряется с помощью библиотеки типов элемента управления, тем самым предоставляя упакованную, расширенную версию библиотеки типов.</span><span class="sxs-lookup"><span data-stu-id="416ee-113">If you add a control as a component, Visual Basic merges the extender properties and methods of the form in which the control is embedded with the control's type library, thus providing a wrapped, extended version of the type library.</span></span> <span data-ttu-id="416ee-114">В этой версии библиотеки типов можно использовать свойства расширителей, такие как Top и Left, как если бы они были частью элемента управления, а не контейнера элемента управления.</span><span class="sxs-lookup"><span data-stu-id="416ee-114">With this version of the type library, you can use extender properties such as Top and Left as if they were part of the control, instead of the control's container.</span></span>

<span data-ttu-id="416ee-115">Visual Basic в настоящее время не поддерживает несколько библиотек типов, встроенных в один DLL-файл.</span><span class="sxs-lookup"><span data-stu-id="416ee-115">Visual Basic does not currently support multiple type libraries built into a single .dll file.</span></span> <span data-ttu-id="416ee-116">При запуске в библиотеке DLL, включающей несколько библиотек типов, следует получить автономные копии библиотек типов из источника, который представил объект, чтобы использовать объект с Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="416ee-116">If you run into a DLL that incorporates multiple type libraries, you should get stand-alone copies of the type libraries from the source that supplied the object in order to use the object with Visual Basic.</span></span>

<span data-ttu-id="416ee-117">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="416ee-117">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="416ee-118">Преобразование в Visual Basic из C++</span><span class="sxs-lookup"><span data-stu-id="416ee-118">Translating to Visual Basic from C++</span></span>](translating-to-visual-basic-from-c--.md)
-   [<span data-ttu-id="416ee-119">Перевод в Visual Basic из Java</span><span class="sxs-lookup"><span data-stu-id="416ee-119">Translating to Visual Basic from Java</span></span>](translating-to-visual-basic-from-java.md)
-   [<span data-ttu-id="416ee-120">Добавление компонента в проект Visual Basic</span><span class="sxs-lookup"><span data-stu-id="416ee-120">Adding a Component to a Visual Basic Project</span></span>](adding-a-component-to-a-visual-basic-project.md)
-   [<span data-ttu-id="416ee-121">Добавление ссылки на проект Visual Basic</span><span class="sxs-lookup"><span data-stu-id="416ee-121">Adding a Reference to a Visual Basic Project</span></span>](adding-a-reference-to-a-visual-basic-project.md)
-   [<span data-ttu-id="416ee-122">Обозреватель объектов Visual Basic</span><span class="sxs-lookup"><span data-stu-id="416ee-122">Visual Basic Object Browser</span></span>](visual-basic-object-browser.md)

## <a name="related-topics"></a><span data-ttu-id="416ee-123">См. также</span><span class="sxs-lookup"><span data-stu-id="416ee-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="416ee-124">Преобразование в C++</span><span class="sxs-lookup"><span data-stu-id="416ee-124">Translating to C++</span></span>](translating-to-c--.md)
</dt> <dt>

[<span data-ttu-id="416ee-125">Перевод на Java</span><span class="sxs-lookup"><span data-stu-id="416ee-125">Translating to Java</span></span>](translating-to-java.md)
</dt> </dl>

 

 





---
title: Печать и списки команд
description: Элемент управления печатью Direct2D \ 32; является новым компонентом в модуле Direct2D в Windows 8.
ms.assetid: C51ACCDE-B205-4F79-A2FD-D112BAAD1616
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b6beb16a24c972016686e2dffe915a947128a63
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413085"
---
# <a name="printing-and-command-lists"></a><span data-ttu-id="8dd1f-103">Печать и списки команд</span><span class="sxs-lookup"><span data-stu-id="8dd1f-103">Printing and command lists</span></span>

<span data-ttu-id="8dd1f-104">[**Элемент управления печатью**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) [Direct2D](./direct2d-portal.md) — это новый компонент в модуле Direct2D в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="8dd1f-104">The [Direct2D](./direct2d-portal.md) [**print control**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) is a new component in the Direct2D module in Windows 8.</span></span> <span data-ttu-id="8dd1f-105">Этот компонент позволяет Direct2D приложениям повторно использовать вызовы рисования Direct2D (с точки зрения изменений состояния и примитивов отрисовки) для доставки результатов печати, сходных с отображаемыми на экране.</span><span class="sxs-lookup"><span data-stu-id="8dd1f-105">This component lets Direct2D apps reuse their Direct2D drawing calls (in terms of state changes and rending primitives) to deliver printing results that are similar to what you see on the screen.</span></span>

<span data-ttu-id="8dd1f-106">Интерфейс [**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) представляет собой виртуальное задание печати. можно создать элемент управления печатью [Direct2D](./direct2d-portal.md) , чтобы запустить новое задание печати, передать содержимое Direct2D для каждой страницы, которую нужно напечатать, а затем закрыть элемент управления печатью для завершения задания печати.</span><span class="sxs-lookup"><span data-stu-id="8dd1f-106">The [**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) interface represents a virtual print job: you can create a [Direct2D](./direct2d-portal.md) print control to initiate a new print job, pass in Direct2D contents for each page you want to print, then close the print control to complete a print job.</span></span>

> [!Note]  
> <span data-ttu-id="8dd1f-107">Элемент управления печатью сопоставляется с одним и тем же заданием печати, и его нельзя использовать повторно.</span><span class="sxs-lookup"><span data-stu-id="8dd1f-107">A print control maps to one and exactly one print job, and you can't reuse it.</span></span>

<span data-ttu-id="8dd1f-108">Элемент управления печатью [Direct2D](./direct2d-portal.md) преобразует и оптимизирует переданное содержимое Direct2D для подсистемы печати, которая работает с реальными принтерами для доставки фактической печати.</span><span class="sxs-lookup"><span data-stu-id="8dd1f-108">The [Direct2D](./direct2d-portal.md) print control converts and optimizes the passed in Direct2D contents for the print sub-system, which works with the real printers to deliver the actual printout.</span></span> <span data-ttu-id="8dd1f-109">Все сведения, относящиеся к печати, скрыты от приложений Direct2D. Это означает, что Direct2D приложения могут печататься, не зная, на каких устройствах они рисуются, или о переводе документов для печати.</span><span class="sxs-lookup"><span data-stu-id="8dd1f-109">All print-specific details are hidden from Direct2D apps, which means Direct2D apps can print without knowing what devices they are drawing to, or how the drawings are translated to printing.</span></span>

<span data-ttu-id="8dd1f-110">Для печати с помощью [Direct2D](./direct2d-portal.md)необходимо подготовить один список команд Direct2D для каждой страницы, которую нужно напечатать, а затем передать этот список команд в элемент управления печатью Direct2D.</span><span class="sxs-lookup"><span data-stu-id="8dd1f-110">To print with [Direct2D](./direct2d-portal.md), you need to prepare one Direct2D command list for each page you want to print, then pass that command list to the Direct2D print control.</span></span> <span data-ttu-id="8dd1f-111">Чтобы подготовить этот список команд Direct2D, просто создайте и настройте список команд в качестве целевого объекта для текущего контекста устройства, а затем нарисуйте его в контексте устройства точно так же, как при рисовании в точечный рисунок для отображения.</span><span class="sxs-lookup"><span data-stu-id="8dd1f-111">To prepare that Direct2D command list, you simply create and set a command list as the drawing target of the current device context, and then draw to that device context, exactly as if you are drawing to a bitmap target for display.</span></span> <span data-ttu-id="8dd1f-112">Дополнительные сведения об устройствах и целевых объектах см. в разделе [устройства и контексты устройств](devices-and-device-contexts.md) .</span><span class="sxs-lookup"><span data-stu-id="8dd1f-112">See [Devices and Device Contexts](devices-and-device-contexts.md) for more info on devices and targets.</span></span>

<span data-ttu-id="8dd1f-113">На схеме здесь показано взаимодействие между приложением, контекстом устройства, целевым объектом точечного рисунка, целевым объектом списка команд и элементом управления печатью.</span><span class="sxs-lookup"><span data-stu-id="8dd1f-113">The diagram here illustrates the interaction between the app, device context, bitmap target, command list target, and the print control.</span></span>

> [!Note]  
> <span data-ttu-id="8dd1f-114">Компоненты Sub-System печати и принтеров Windows выделены серым цветом, так как они полностью скрыты от приложений [Direct2D](./direct2d-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="8dd1f-114">The Windows Print Sub-System and Printer components are in gray because they are completely hidden from [Direct2D](./direct2d-portal.md) apps.</span></span>

![Схема, показывающая, как коммандлист и печать взаимодействуют с приложением и Direct2D.](images/d2dprintcontroldiagram.png)

## <a name="example"></a><span data-ttu-id="8dd1f-116">Пример</span><span class="sxs-lookup"><span data-stu-id="8dd1f-116">Example</span></span>

<span data-ttu-id="8dd1f-117">Полный процесс печати содержимого Direct2D включает следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="8dd1f-117">The complete process of printing Direct2D content includes the following steps.</span></span>

1.  <span data-ttu-id="8dd1f-118">Создайте элемент управления печатью для запуска задания печати.</span><span class="sxs-lookup"><span data-stu-id="8dd1f-118">Create a print control to initiate a print job.</span></span>
2.  <span data-ttu-id="8dd1f-119">Добавьте страницу в элемент управления печатью, передав список команд.</span><span class="sxs-lookup"><span data-stu-id="8dd1f-119">Add a page to the print control by passing in a command list.</span></span>
3.  <span data-ttu-id="8dd1f-120">Повторите шаг 2 для каждой страницы в оставшейся части документа.</span><span class="sxs-lookup"><span data-stu-id="8dd1f-120">Repeat step 2 for each page in the rest of the document</span></span>
4.  <span data-ttu-id="8dd1f-121">Закройте элемент управления печатью, чтобы завершить задание печати.</span><span class="sxs-lookup"><span data-stu-id="8dd1f-121">Close the print control to complete the print job.</span></span>

<span data-ttu-id="8dd1f-122">Ниже приведен пример кода, демонстрирующий процесс.</span><span class="sxs-lookup"><span data-stu-id="8dd1f-122">Here is a code example showing the process.</span></span>

```cpp
ID2D1CommandList* commandList;
// Skip command list creation and drawing for simplicity.

// Set print control properties.
D2D1_PRINT_CONTROL_PROPERTIES printControlProperties;
printControlProperties.rasterDPI = 150.0f; // Use the default rasterization DPI for all unsupported Direct2D commands 
                                                                                                                                                                            //  or options.
printControlProperties.fontSubset = D2D1_PRINT_FONT_SUBSET_MODE_DEFAULT; // Using the default font subset strategy.
printControlProperties.colorSpace = D2D1_COLOR_SPACE_SRGB; // Color space for vector graphics in Direct2D print control.

// Create a Direct2D Print Control to initiate a print job.
ID2D1PrintControl* d2dPrintControl;
d2dDevice->CreatePrintControl(
    wicFactory,
    documentTarget,
    printControlProperties,
    &d2dPrintControl
    );

// Add Direct2D drawing commands encapsulated in a command list.
// You can add in more pages by calling this API multiple times.
d2dPrintControl->AddPage(commandList);

// Close the print control to complete a print job.
d2dPrintControl->Close();
```

## <a name="related-topics"></a><span data-ttu-id="8dd1f-123">См. также</span><span class="sxs-lookup"><span data-stu-id="8dd1f-123">Related topics</span></span>

[<span data-ttu-id="8dd1f-124">**ID2D1CommandList**</span><span class="sxs-lookup"><span data-stu-id="8dd1f-124">**ID2D1CommandList**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist)

[<span data-ttu-id="8dd1f-125">**ID2D1PrintControl**</span><span class="sxs-lookup"><span data-stu-id="8dd1f-125">**ID2D1PrintControl**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol)

[<span data-ttu-id="8dd1f-126">Повышение производительности приложений Direct2D и печати</span><span class="sxs-lookup"><span data-stu-id="8dd1f-126">Improving the Performance of Direct2D Applications and Printing</span></span>](improving-direct2d-performance.md)
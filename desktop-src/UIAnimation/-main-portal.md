---
title: Диспетчер анимации Windows
description: Диспетчер анимации Windows (Windows Animation) включает насыщенную анимацию элементов пользовательского интерфейса.
ms.assetid: 1d840263-d9da-4cab-9bc3-0c143c9c8741
keywords:
- Анимация Windows анимации Windows, портал
- Анимация Windows для диспетчера анимации Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d274b9f2d5e386fbe01c2caeb9e1e65ddbdc73f3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987632"
---
# <a name="windows-animation-manager"></a><span data-ttu-id="d679d-105">Диспетчер анимации Windows</span><span class="sxs-lookup"><span data-stu-id="d679d-105">Windows Animation Manager</span></span>

## <a name="purpose"></a><span data-ttu-id="d679d-106">Назначение</span><span class="sxs-lookup"><span data-stu-id="d679d-106">Purpose</span></span>

<span data-ttu-id="d679d-107">Диспетчер анимации Windows (Windows Animation) включает насыщенную анимацию элементов пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="d679d-107">The Windows Animation Manager (Windows Animation) enables rich animation of user interface elements.</span></span> <span data-ttu-id="d679d-108">Он предназначен для упрощения процесса добавления анимации в пользовательский интерфейс приложения и позволяет разработчикам реализовывать анимации, которые являются гладкими, естественными и интерактивными.</span><span class="sxs-lookup"><span data-stu-id="d679d-108">It is designed to simplify the process of adding animation to an application's user interface and to enable developers to implement animations that are smooth, natural, and interactive.</span></span>

<span data-ttu-id="d679d-109">Платформа анимации управляет планированием и выполнением анимаций.</span><span class="sxs-lookup"><span data-stu-id="d679d-109">The animation framework manages the scheduling and execution of animations.</span></span> <span data-ttu-id="d679d-110">Он предоставляет библиотеку полезных математических функций для указания поведения элемента пользовательского интерфейса с течением времени, а также позволяет разработчикам реализовывать пользовательские функции, предоставляющие дополнительные поведений.</span><span class="sxs-lookup"><span data-stu-id="d679d-110">It supplies a library of useful mathematical functions for specifying the behavior of a UI element over time, and also enables developers to implement custom functions that provide additional behaviors.</span></span>

<span data-ttu-id="d679d-111">Анимация Windows не выполняет отрисовку; его можно использовать с любой графической платформой, включая Direct2D, Direct3D или GDI+.</span><span class="sxs-lookup"><span data-stu-id="d679d-111">Windows Animation does not perform the rendering; it can be used with any graphics platform, including Direct2D, Direct3D, or GDI+.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d679d-112">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="d679d-112">In this section</span></span>



| <span data-ttu-id="d679d-113">Раздел</span><span class="sxs-lookup"><span data-stu-id="d679d-113">Topic</span></span>                                                                                   | <span data-ttu-id="d679d-114">Описание</span><span class="sxs-lookup"><span data-stu-id="d679d-114">Description</span></span>                                                                                                                                       |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d679d-115">Руководством по разработке анимации Windows</span><span class="sxs-lookup"><span data-stu-id="d679d-115">Windows Animation Development Guide</span></span>](windows-animation-developer-guide.md)<br/> | <span data-ttu-id="d679d-116">В руководстве для разработчиков представлен обзор анимации Windows и приведен пример кода, охватывающего основные задачи анимации.</span><span class="sxs-lookup"><span data-stu-id="d679d-116">The developer guide provides an overview of Windows Animation and provides sample code that covers the basic animation tasks.</span></span><br/>          |
| [<span data-ttu-id="d679d-117">Справочник по анимации Windows</span><span class="sxs-lookup"><span data-stu-id="d679d-117">Windows Animation Reference</span></span>](windows-animation-reference.md)<br/>               | <span data-ttu-id="d679d-118">Разделы, содержащиеся в этом разделе, содержат справочные спецификации для диспетчера анимации Windows.</span><span class="sxs-lookup"><span data-stu-id="d679d-118">The topics contained in this section provide the reference specifications for the Windows Animation Manager.</span></span><br/>                           |
| [<span data-ttu-id="d679d-119">Примеры анимации Windows</span><span class="sxs-lookup"><span data-stu-id="d679d-119">Windows Animation Samples</span></span>](windows-animation-samples.md)<br/>                   | <span data-ttu-id="d679d-120">Разделы, содержащиеся в этом разделе, содержат сведения о примерах кода, которые поддерживают документацию по диспетчеру анимации Windows.</span><span class="sxs-lookup"><span data-stu-id="d679d-120">The topics contained in this section provide details about the code samples that support the Windows Animation Manager documentation.</span></span> <br/> |
| [<span data-ttu-id="d679d-121">Глоссарий анимации Windows</span><span class="sxs-lookup"><span data-stu-id="d679d-121">Windows Animation Glossary</span></span>](-ui-animation-glossary.md)<br/>                     | <span data-ttu-id="d679d-122">В этом глоссарии содержатся термины и акронимы, представляющие интерес для разработчиков, использующих диспетчер анимации Windows.</span><span class="sxs-lookup"><span data-stu-id="d679d-122">This glossary contains terms and acronyms of interest to developers using the Windows Animation Manager.</span></span><br/>                               |



 

## <a name="developer-audience"></a><span data-ttu-id="d679d-123">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="d679d-123">Developer audience</span></span>

<span data-ttu-id="d679d-124">Анимация Windows предназначена для использования опытными разработчиками на C/C++, знакомыми с COM, концепциями программирования пользовательского интерфейса и общими концепциями анимации.</span><span class="sxs-lookup"><span data-stu-id="d679d-124">Windows Animation is designed for use by experienced C/C++ developers who are familiar with COM, UI programming concepts, and general animation concepts.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="d679d-125">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="d679d-125">Run-time requirements</span></span>

<span data-ttu-id="d679d-126">Диспетчер анимации Windows появился в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d679d-126">The Windows Animation Manager was introduced in Windows 7.</span></span>

<span data-ttu-id="d679d-127">Приложения, для которых требуется поддержка Windows Animation Manager в Windows Vista, могут использовать обновление платформы для Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d679d-127">Applications that require support for Windows Animation Manager on Windows Vista can utilize the Platform Update for Windows Vista.</span></span> <span data-ttu-id="d679d-128">Приложения, для которых требуется обновление платформы для Windows Vista, могут иметь Центр обновления Windows убедиться, что они установлены, или скачать и установить его в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="d679d-128">Applications that require Platform Update for Windows Vista can have Windows Update verify that it is installed, or download and install it in the background otherwise.</span></span> <span data-ttu-id="d679d-129">Дополнительные сведения см. в [статье об обновлении платформы для Windows Vista](../win7ip/platform-update-for-windows-vista-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d679d-129">For more information, see [About Platform Update for Windows Vista](../win7ip/platform-update-for-windows-vista-overview.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d679d-130">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d679d-130">Additional resources</span></span>

-   <span data-ttu-id="d679d-131">[Общие сведения об анимации Windows Scenic](https://channel9.msdn.com/blogs/yochay/windows-scenic-animation-overview) (видео)</span><span class="sxs-lookup"><span data-stu-id="d679d-131">[Windows Scenic Animation Overview](https://channel9.msdn.com/blogs/yochay/windows-scenic-animation-overview) (video)</span></span>
-   <span data-ttu-id="d679d-132">[В Windows 7: подробный обзор и учебник по диспетчеру анимации](https://channel9.msdn.com/blogs/yochay/inside-windows-7-animation-manager-deep-dive) (видео)</span><span class="sxs-lookup"><span data-stu-id="d679d-132">[Inside Windows 7: Animation Manager Deep Dive and Tutorial](https://channel9.msdn.com/blogs/yochay/inside-windows-7-animation-manager-deep-dive) (video)</span></span>
-   <span data-ttu-id="d679d-133">[Анимация Windows — дополнительные разделы](https://channel9.msdn.com/posts/yochay/Windows-Animation-Advance-Topics/) (видео)</span><span class="sxs-lookup"><span data-stu-id="d679d-133">[Windows Animation - Advanced Topics](https://channel9.msdn.com/posts/yochay/Windows-Animation-Advance-Topics/) (video)</span></span>
-   [<span data-ttu-id="d679d-134">Пример кода для диспетчера анимации Windows</span><span class="sxs-lookup"><span data-stu-id="d679d-134">Windows Animation Manager Sample Code</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)

## <a name="related-topics"></a><span data-ttu-id="d679d-135">См. также</span><span class="sxs-lookup"><span data-stu-id="d679d-135">Related topics</span></span>

[<span data-ttu-id="d679d-136">Общие сведения об анимации (платформа .NET Framework)</span><span class="sxs-lookup"><span data-stu-id="d679d-136">Animation Overview (.NET Framework)</span></span>](/dotnet/framework/wpf/graphics-multimedia/animation-overview)
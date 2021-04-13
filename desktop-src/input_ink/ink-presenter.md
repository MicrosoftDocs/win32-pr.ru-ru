---
description: API-интерфейсы обработчика рукописного ввода позволяют классическим приложениям Майкрософт Win32 управлять вводом, обработкой и отрисовкой рукописного ввода (стандартного и модифицированного) с помощью объекта InkPresenter, добавляемого в визуальное дерево приложения DirectComposition.
ms.assetid: 8BD52813-3741-4C1F-B62A-B3C366A86362
title: Показ рукописных данных
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 9bd9f4c3c98b443110a0a7948075ab836a9493c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265517"
---
# <a name="ink-presenter"></a><span data-ttu-id="b4a4c-103">Показ рукописных данных</span><span class="sxs-lookup"><span data-stu-id="b4a4c-103">Ink presenter</span></span>

<span data-ttu-id="b4a4c-104">Интерфейсы API-интерфейсов рукописного ввода позволяют приложениям Microsoft Win32 управлять вводом, обработкой и отрисовкой рукописного ввода (Standard и Modified) с помощью объекта [**InkPresenter**](/uwp/api/windows.ui.input.inking.inkpresenter) , вставленного в визуальное дерево [DirectComposition](../directcomp/directcomposition-portal.md) приложения.</span><span class="sxs-lookup"><span data-stu-id="b4a4c-104">The ink presenter APIs enable Microsoft Win32 apps to manage the input, processing, and rendering of ink input (standard and modified) through an [**InkPresenter**](/uwp/api/windows.ui.input.inking.inkpresenter) object inserted into the app's [DirectComposition](../directcomp/directcomposition-portal.md) visual tree.</span></span>

> [!Note]
>
> <span data-ttu-id="b4a4c-105">Стандартный ввод рукописных данных (кончик пера или кончик или кнопка ластика) не изменен с помощью вторичного уровня доступности, такого как кнопка с изображением пера, правая кнопка мыши или аналогичный.</span><span class="sxs-lookup"><span data-stu-id="b4a4c-105">Standard ink input (pen tip or eraser tip/button) is not modified with a secondary affordance, such as a pen barrel button, right mouse button, or similar.</span></span>

<span data-ttu-id="b4a4c-106">Приложения универсальная платформа Windows (UWP), использующие XAML (XAML), предоставляют эту функцию с помощью элемента управления [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) , а также объекта [**InkPresenter**](/uwp/api/windows.ui.input.inking.inkpresenter) , который подключается к визуальному дереву XAML [DirectComposition](../directcomp/directcomposition-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="b4a4c-106">Universal Windows Platform (UWP) apps using Extensible Application Markup Language (XAML) provide this functionality through an [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) control along with an [**InkPresenter**](/uwp/api/windows.ui.input.inking.inkpresenter) object that connects to the XAML [DirectComposition](../directcomp/directcomposition-portal.md) visual tree.</span></span> <span data-ttu-id="b4a4c-107">Дополнительные сведения см. в разделе [взаимодействие пером и](/windows/uwp/design/input/pen-and-stylus-interactions)пера.</span><span class="sxs-lookup"><span data-stu-id="b4a4c-107">For more detail, see [Pen and stylus interactions](/windows/uwp/design/input/pen-and-stylus-interactions).</span></span>

<span data-ttu-id="b4a4c-108">Модуль [подготовки рукописного ввода](ink-renderer.md) предназначен для использования разработчиками универсальных приложений Windows, заинтересованными в предоставлении функциональных возможностей элемента управления [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas)на основе XAML / [](/uwp/api/windows.ui.input.inking.inkpresenter) в собственных приложениях Win32.</span><span class="sxs-lookup"><span data-stu-id="b4a4c-108">[Ink renderer](ink-renderer.md) is designed for use by Universal Windows app developers interested in providing XAML-based [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas)/[**InkPresenter**](/uwp/api/windows.ui.input.inking.inkpresenter) functionality in native Win32 apps.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b4a4c-109">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="b4a4c-109">In this section</span></span>



| <span data-ttu-id="b4a4c-110">Раздел</span><span class="sxs-lookup"><span data-stu-id="b4a4c-110">Topic</span></span>                                                               | <span data-ttu-id="b4a4c-111">Описание</span><span class="sxs-lookup"><span data-stu-id="b4a4c-111">Description</span></span>                                                                                                         |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b4a4c-112">Классы для рукописного показа</span><span class="sxs-lookup"><span data-stu-id="b4a4c-112">Ink presenter classes</span></span>](ink-presenter-classes.md)<br/>       | <span data-ttu-id="b4a4c-113">Подразделы, содержащиеся в этом разделе, содержат справочные спецификации для классов в области рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="b4a4c-113">The topics contained in this section provide the reference specifications for Ink presenter classes.</span></span> <br/>    |
| [<span data-ttu-id="b4a4c-114">Интерфейсы выступающих чернил</span><span class="sxs-lookup"><span data-stu-id="b4a4c-114">Ink presenter interfaces</span></span>](ink-presenter-interfaces.md)<br/> | <span data-ttu-id="b4a4c-115">Подразделы, содержащиеся в этом разделе, содержат справочные спецификации для интерфейсов для показа рукописных данных.</span><span class="sxs-lookup"><span data-stu-id="b4a4c-115">The topics contained in this section provide the reference specifications for Ink presenter interfaces.</span></span> <br/> |



 

## <a name="related-topics"></a><span data-ttu-id="b4a4c-116">См. также</span><span class="sxs-lookup"><span data-stu-id="b4a4c-116">Related topics</span></span>

<span data-ttu-id="b4a4c-117">Взаимодействие [рукописного ввода](ink-presenter.md), [перо и](/windows/uwp/design/input/pen-and-stylus-interactions)перо, [Пример анализа рукописного текста](/samples/microsoft/windows-universal-samples/inkanalysis/), [простой пример](/samples/microsoft/windows-universal-samples/simpleink/)с рукописным вводом, [сложный образец для рукописного](/samples/microsoft/windows-universal-samples/complexink/) ввода</span><span class="sxs-lookup"><span data-stu-id="b4a4c-117">[Ink presenter](ink-presenter.md), [Pen and stylus interactions](/windows/uwp/design/input/pen-and-stylus-interactions), [Ink Analysis sample](/samples/microsoft/windows-universal-samples/inkanalysis/), [Simple inking sample](/samples/microsoft/windows-universal-samples/simpleink/), [Complex inking sample](/samples/microsoft/windows-universal-samples/complexink/)</span></span>

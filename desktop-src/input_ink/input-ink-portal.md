---
description: Узнайте о различных интерфейсах API рукописного ввода для приложений Windows.
ms.assetid: 0691afb1-575a-4bb7-8fa5-006b231b8f1f
title: Рукописный ввод
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: ffb67d452e3bee327195f8ff920bfcab3c0232a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719602"
---
# <a name="ink-input"></a><span data-ttu-id="883d2-103">Рукописный ввод</span><span class="sxs-lookup"><span data-stu-id="883d2-103">Ink input</span></span>

<span data-ttu-id="883d2-104">Узнайте о различных интерфейсах API рукописного ввода для приложений Windows.</span><span class="sxs-lookup"><span data-stu-id="883d2-104">Learn about the various Desktop inking APIs for Windows apps.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="883d2-105">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="883d2-105">In this section</span></span>

| <span data-ttu-id="883d2-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="883d2-106">Topic</span></span> | <span data-ttu-id="883d2-107">Описание</span><span class="sxs-lookup"><span data-stu-id="883d2-107">Description</span></span> |
|---|---|
| [<span data-ttu-id="883d2-108">Показ рукописных данных</span><span class="sxs-lookup"><span data-stu-id="883d2-108">Ink presenter</span></span>](ink-presenter.md)<br/> | <span data-ttu-id="883d2-109">Интерфейсы API-интерфейсов рукописного ввода позволяют приложениям Microsoft Win32 управлять вводом, обработкой и отрисовкой рукописного ввода (Standard и Modified) с помощью объекта [**InkPresenter**](/uwp/api/Windows.UI.Input.Inking.InkPresenter) , вставленного в визуальное дерево [DirectComposition](../directcomp/directcomposition-portal.md) приложения.</span><span class="sxs-lookup"><span data-stu-id="883d2-109">The ink presenter APIs enable Microsoft Win32 apps to manage the input, processing, and rendering of ink input (standard and modified) through an [**InkPresenter**](/uwp/api/Windows.UI.Input.Inking.InkPresenter) object inserted into the app's [DirectComposition](../directcomp/directcomposition-portal.md) visual tree.</span></span><br/> |
| [<span data-ttu-id="883d2-110">Модуль подготовки рукописных данных</span><span class="sxs-lookup"><span data-stu-id="883d2-110">Ink renderer</span></span>](ink-renderer.md)<br/>   | <span data-ttu-id="883d2-111">Интерфейсы API модуля [подготовки рукописного ввода позволяют визуализировать](ink-renderer.md) рукописные штрихи в назначенный контекст устройства Direct2D универсального приложения Windows вместо элемента управления [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="883d2-111">The [Ink renderer](ink-renderer.md) APIs enable the rendering of ink strokes onto the designated Direct2D device context of a Universal Windows app, instead of the default [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) control.</span></span><br/>                                                                        |

## <a name="related-topics"></a><span data-ttu-id="883d2-112">См. также</span><span class="sxs-lookup"><span data-stu-id="883d2-112">Related topics</span></span>

<span data-ttu-id="883d2-113">[Взаимодействие пером и пера](/windows/uwp/design/input/pen-and-stylus-interactions), пример " [анализ рукописного ввода](/samples/microsoft/windows-universal-samples/inkanalysis/)", [простой пример с рукописным](/samples/microsoft/windows-universal-samples/simpleink/)вводом, [сложный пример для рукописного](/samples/microsoft/windows-universal-samples/complexink/) ввода</span><span class="sxs-lookup"><span data-stu-id="883d2-113">[Pen and stylus interactions](/windows/uwp/design/input/pen-and-stylus-interactions), [Ink Analysis sample](/samples/microsoft/windows-universal-samples/inkanalysis/), [Simple inking sample](/samples/microsoft/windows-universal-samples/simpleink/), [Complex inking sample](/samples/microsoft/windows-universal-samples/complexink/)</span></span>

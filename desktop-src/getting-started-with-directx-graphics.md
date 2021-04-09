---
description: .
ms.assetid: 49E0D0C2-E6EC-4849-A44F-36FDEFBB9838
title: Начало работы с графикой DirectX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5278e759ea0faf04ac8b247ad3ea1c687dd205c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104080874"
---
# <a name="getting-started-with-directx-graphics"></a><span data-ttu-id="6cd31-103">Начало работы с графикой DirectX</span><span class="sxs-lookup"><span data-stu-id="6cd31-103">Getting started with DirectX Graphics</span></span>

<span data-ttu-id="6cd31-104">Microsoft DirectX Graphics предоставляет набор интерфейсов API, которые можно использовать для создания игр и других высокопроизводительных мультимедийных приложений.</span><span class="sxs-lookup"><span data-stu-id="6cd31-104">Microsoft DirectX graphics provides a set of APIs that you can use to create games and other high-performance multimedia applications.</span></span> <span data-ttu-id="6cd31-105">DirectX Graphics поддерживает высокопроизводительные высокопроизводительные и трехмерные графики.</span><span class="sxs-lookup"><span data-stu-id="6cd31-105">DirectX graphics includes support for high-performance 2-D and 3-D graphics.</span></span>

<span data-ttu-id="6cd31-106">Для трехмерной графики используйте API Microsoft Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="6cd31-106">For 3-D graphics, use the Microsoft Direct3D 11 API.</span></span> <span data-ttu-id="6cd31-107">Даже при наличии аппаратного обеспечения Microsoft Direct3D 9-Level или Microsoft Direct3D 10, вы можете использовать API Direct3D 11 и ориентироваться на устройство [уровня "](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x" или "Feature" 10 \_ x.</span><span class="sxs-lookup"><span data-stu-id="6cd31-107">Even if you have Microsoft Direct3D 9-level or Microsoft Direct3D 10-level hardware, you can use the Direct3D 11 API and target a [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9\_x or feature level 10\_x device.</span></span> <span data-ttu-id="6cd31-108">Сведения о разработке трехмерной графики с помощью DirectX см. в статье [Создание трехмерной графики с помощью DirectX](/previous-versions/windows/apps/hh465137(v=win.10)
).</span><span class="sxs-lookup"><span data-stu-id="6cd31-108">For info about how to develop 3-D graphics with DirectX, see [Create 3D graphics with DirectX](/previous-versions/windows/apps/hh465137(v=win.10)
).</span></span>

<span data-ttu-id="6cd31-109">Для двухмерной графики и текста используйте Direct2D и [DirectWrite](./directwrite/direct-write-portal.md) , а не Windows интерфейс графических устройств (GDI).</span><span class="sxs-lookup"><span data-stu-id="6cd31-109">For 2-D graphics and text, use Direct2D and [DirectWrite](./directwrite/direct-write-portal.md) rather than Windows Graphics Device Interface (GDI).</span></span>

<span data-ttu-id="6cd31-110">Чтобы создать точечные рисунки, заполненные Direct3D 11 или Direct2D, используйте [DirectComposition](./directcomp/directcomposition-portal.md).</span><span class="sxs-lookup"><span data-stu-id="6cd31-110">To compose bitmaps that Direct3D 11 or Direct2D populated, use [DirectComposition](./directcomp/directcomposition-portal.md).</span></span>

<span data-ttu-id="6cd31-111">Дополнительные сведения о создании приложения для Магазина Windows, использующего DirectX, см. в статье [Создание первого приложения для Магазина Windows с помощью DirectX](/previous-versions/windows/apps/br229580(v=win.10)
).</span><span class="sxs-lookup"><span data-stu-id="6cd31-111">To learn about how to create a Windows Store app that uses DirectX, see [Create your first Windows Store app using DirectX](/previous-versions/windows/apps/br229580(v=win.10)
).</span></span> <span data-ttu-id="6cd31-112">Вы можете использовать класс [**Windows. UI:: XAML:: Controls:: SwapChainPanel**](/uwp/api/Windows.UI.Xaml.Controls.SwapChainPanel?view=winrt-19041) для создания высокопроизводительных приложений DirectX с наложением ПОЛЬЗОВАТЕЛЬСКОГО интерфейса XAML.</span><span class="sxs-lookup"><span data-stu-id="6cd31-112">You can use the [**Windows.UI::Xaml::Controls::SwapChainPanel**](/uwp/api/Windows.UI.Xaml.Controls.SwapChainPanel?view=winrt-19041) class to create high-performance DirectX apps with a XAML UI overlay.</span></span> <span data-ttu-id="6cd31-113">Дополнительные сведения о сочетании XAML и DirectX в приложении Windows см. в разделе [взаимодействие DirectX и XAML](/previous-versions/windows/apps/hh825871(v=win.10)).</span><span class="sxs-lookup"><span data-stu-id="6cd31-113">For more info about combining XAML and DirectX in a Windows app, see [DirectX and XAML interop](/previous-versions/windows/apps/hh825871(v=win.10)).</span></span>

<span data-ttu-id="6cd31-114">Дополнительные сведения о создании видеодрайверов для Windows 8 см. в разделе [Путеводитель по модели видеодрайверов Windows (WDDM)](/windows-hardware/drivers/display/roadmap-for-developing-drivers-for-the-windows-vista-display-driver-mo).</span><span class="sxs-lookup"><span data-stu-id="6cd31-114">To learn about how to build a display driver for Windows 8, see [Roadmap for the Windows Display Driver Model (WDDM)](/windows-hardware/drivers/display/roadmap-for-developing-drivers-for-the-windows-vista-display-driver-mo).</span></span>

<span data-ttu-id="6cd31-115">Если вам нужна документация по предыдущим версиям DirectX, см. раздел [Классическая графика DirectX](/windows/desktop/classic-directx-graphics).</span><span class="sxs-lookup"><span data-stu-id="6cd31-115">If you need the documentation for previous DirectX versions, see [Classic DirectX Graphics](/windows/desktop/classic-directx-graphics).</span></span>


 

 

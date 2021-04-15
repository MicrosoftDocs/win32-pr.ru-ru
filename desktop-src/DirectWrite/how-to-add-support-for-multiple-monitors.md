---
title: Добавление поддержки нескольких мониторов
description: DirectWrite включает поддержку систем с несколькими мониторами.
ms.assetid: 62274126-49da-4166-8482-73aac2b29c26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74c5d95d0e727b4184a2dcce1720379231ce22a8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413247"
---
# <a name="how-to-add-support-for-multiple-monitors"></a><span data-ttu-id="cca9d-103">Добавление поддержки нескольких мониторов</span><span class="sxs-lookup"><span data-stu-id="cca9d-103">How to Add Support for Multiple Monitors</span></span>

<span data-ttu-id="cca9d-104">[DirectWrite](direct-write-portal.md) включает поддержку систем с несколькими мониторами.</span><span class="sxs-lookup"><span data-stu-id="cca9d-104">[DirectWrite](direct-write-portal.md) includes support for systems with multiple monitors.</span></span> <span data-ttu-id="cca9d-105">Разные мониторы могут иметь разную геометрию (RGB, BGR или плоский) или другие атрибуты.</span><span class="sxs-lookup"><span data-stu-id="cca9d-105">Different monitors may have different pixel geometry (RGB, BGR, or FLAT) or other attributes.</span></span> <span data-ttu-id="cca9d-106">Дополнительные сведения о пиксельной геометрии см. в разделе Справочник по [**\_ \_ геометрии дврите Pixel**](/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry) .</span><span class="sxs-lookup"><span data-stu-id="cca9d-106">For more information about pixel geometry, see the [**DWRITE\_PIXEL\_GEOMETRY**](/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry) reference topic.</span></span> <span data-ttu-id="cca9d-107">В этом разделе мы покажем, как добавить поддержку нескольких мониторов в приложение DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="cca9d-107">This topic will show you how to add support for multiple monitors to your DirectWrite application.</span></span>

<span data-ttu-id="cca9d-108">Для поддержки нескольких мониторов необходимо выполнить обработку сообщения окна **WM \_ виндовпосчанжед** .</span><span class="sxs-lookup"><span data-stu-id="cca9d-108">In order to support multiple monitors, you must handle the **WM\_WINDOWPOSCHANGED** window message.</span></span> <span data-ttu-id="cca9d-109">Это сообщение отправляется при перемещении окна, поэтому необходимо проверить, переместилось ли окно на другой монитор, как показано в следующем коде.</span><span class="sxs-lookup"><span data-stu-id="cca9d-109">This message is sent when the window is moved, so you must check if the window has moved to a different monitor as shown in the following code.</span></span>


```C++
case WM_WINDOWPOSCHANGED:
    {
        HMONITOR monitor = MonitorFromWindow(hwnd, MONITOR_DEFAULTTONULL);
        if (monitor != g_monitor)
        {
            g_monitor = monitor;
            if (g_spRenderTarget != NULL)
            {
                IDWriteRenderingParams* pRenderingParams = NULL;
                g_spDWriteFactory->CreateMonitorRenderingParams(monitor, &pRenderingParams);

                g_spRenderTarget->SetTextRenderingParams(pRenderingParams);

                SafeRelease(&pRenderingParams);
            }

            InvalidateRect(hwnd, NULL, TRUE);
        }
    }
    break;
```



<span data-ttu-id="cca9d-110">Если окно находится на новом мониторе, необходимо создать параметры отрисовки для нового монитора с помощью метода [**идвритефактори:: креатемониторрендерингпарамс**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createmonitorrenderingparams) .</span><span class="sxs-lookup"><span data-stu-id="cca9d-110">If the window is located on a new monitor, then you must create rendering parameters for the new monitor by using the [**IDWriteFactory::CreateMonitorRenderingParams**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createmonitorrenderingparams) method.</span></span>

> [!Note]  
> <span data-ttu-id="cca9d-111">Не используйте метод [**идвритефактори:: креатерендерингпарамс**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createrenderingparams) для создания параметров отрисовки, так как он всегда создает параметры для основного монитора.</span><span class="sxs-lookup"><span data-stu-id="cca9d-111">Do not use the [**IDWriteFactory::CreateRenderingParams**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createrenderingparams) method to create the rendering parameters, because it always creates parameters for the primary monitor.</span></span>

 

<span data-ttu-id="cca9d-112">При наличии объекта [**идвритерендерингпарамс**](/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams) задайте параметры отрисовки для целевого объекта отрисовки с помощью метода [**ID2DRenderTarget:: сеттекстрендерингпарамс**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settextrenderingparams) .</span><span class="sxs-lookup"><span data-stu-id="cca9d-112">When you have an [**IDWriteRenderingParams**](/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams) object, set the rendering parameters for the render target by using the [**ID2DRenderTarget::SetTextRenderingParams**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settextrenderingparams) method.</span></span>

<span data-ttu-id="cca9d-113">Наконец, используйте функцию [**инвалидатерект**](/windows/win32/api/winuser/nf-winuser-invalidaterect) , чтобы заставить окно перерисовываться с новыми параметрами отрисовки.</span><span class="sxs-lookup"><span data-stu-id="cca9d-113">Finally, use the [**InvalidateRect**](/windows/win32/api/winuser/nf-winuser-invalidaterect) function to cause the window to redraw with the new rendering parameters.</span></span>

 

 
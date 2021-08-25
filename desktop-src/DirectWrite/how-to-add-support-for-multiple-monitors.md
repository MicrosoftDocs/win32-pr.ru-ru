---
title: Добавление поддержки нескольких мониторов
description: DirectWrite включает поддержку систем с несколькими мониторами.
ms.assetid: 62274126-49da-4166-8482-73aac2b29c26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12bbfb2c803372e52128cd62dddeec407985e4180039d84f9aed66092149911b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048894"
---
# <a name="how-to-add-support-for-multiple-monitors"></a>Добавление поддержки нескольких мониторов

[DirectWrite](direct-write-portal.md) включает поддержку систем с несколькими мониторами. Разные мониторы могут иметь разную геометрию (RGB, BGR или плоский) или другие атрибуты. Дополнительные сведения о пиксельной геометрии см. в разделе Справочник по [**\_ \_ геометрии дврите Pixel**](/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry) . в этом разделе будет показано, как добавить поддержку нескольких мониторов в приложение DirectWrite.

Для поддержки нескольких мониторов необходимо выполнить обработку сообщения окна **WM \_ виндовпосчанжед** . Это сообщение отправляется при перемещении окна, поэтому необходимо проверить, переместилось ли окно на другой монитор, как показано в следующем коде.


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



Если окно находится на новом мониторе, необходимо создать параметры отрисовки для нового монитора с помощью метода [**идвритефактори:: креатемониторрендерингпарамс**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createmonitorrenderingparams) .

> [!Note]  
> Не используйте метод [**идвритефактори:: креатерендерингпарамс**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createrenderingparams) для создания параметров отрисовки, так как он всегда создает параметры для основного монитора.

 

При наличии объекта [**идвритерендерингпарамс**](/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams) задайте параметры отрисовки для целевого объекта отрисовки с помощью метода [**ID2DRenderTarget:: сеттекстрендерингпарамс**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settextrenderingparams) .

Наконец, используйте функцию [**инвалидатерект**](/windows/win32/api/winuser/nf-winuser-invalidaterect) , чтобы заставить окно перерисовываться с новыми параметрами отрисовки.

 

 
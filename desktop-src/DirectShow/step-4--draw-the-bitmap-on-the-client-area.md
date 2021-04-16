---
description: Шаг 4. Рисование точечного рисунка в клиентской области
ms.assetid: fb22468c-9113-46ff-a576-8dee30c458be
title: Шаг 4. Рисование точечного рисунка в клиентской области
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4975215e5d75de9909f029a3378bd6cc8bc60916
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104424082"
---
# <a name="step-4-draw-the-bitmap-on-the-client-area"></a><span data-ttu-id="6c61d-103">Шаг 4. Рисование точечного рисунка в клиентской области</span><span class="sxs-lookup"><span data-stu-id="6c61d-103">Step 4: Draw the Bitmap on the Client Area</span></span>

<span data-ttu-id="6c61d-104">\[Этот API не поддерживается и может быть изменен или недоступен в будущем.\]</span><span class="sxs-lookup"><span data-stu-id="6c61d-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="6c61d-105">В этом разделе приведен шаг 4 из [фрагмента плаката](grabbing-a-poster-frame.md).</span><span class="sxs-lookup"><span data-stu-id="6c61d-105">This topic is Step 4 of [Grabbing a Poster Frame](grabbing-a-poster-frame.md).</span></span>

<span data-ttu-id="6c61d-106">Последним шагом является Отрисовка точечного рисунка в клиентской области окна приложения с помощью функции [**сетдибитстодевице**](/windows/win32/api/wingdi/nf-wingdi-setdibitstodevice) .</span><span class="sxs-lookup"><span data-stu-id="6c61d-106">The final step is to draw the bitmap onto the client area of the application window, using the [**SetDIBitsToDevice**](/windows/win32/api/wingdi/nf-wingdi-setdibitstodevice) function.</span></span> <span data-ttu-id="6c61d-107">В этом примере точечный рисунок просто закрашивается в левом верхнем углу клиентской области без учета размера окна:</span><span class="sxs-lookup"><span data-stu-id="6c61d-107">This example simply paints the bitmap in the upper-left corner of the client area, without regard to the window size:</span></span>


```C++
case WM_PAINT:
    {
        PAINTSTRUCT ps;
        HDC hdc = BeginPaint(hwnd, &ps);
        if (pbmi)
        {
            int result = SetDIBitsToDevice(hdc, 0, 0, 
                pbmi->biWidth,
                pbmi->biHeight,
                0, 0, 0,
                pbmi->biHeight,
                pBuffer,
                reinterpret_cast<BITMAPINFO*>(pbmi),
                DIB_RGB_COLORS);
        }
        EndPaint(hwnd, &ps);
    }
    break;
```



<span data-ttu-id="6c61d-108">Переменные *pBuffer* и *пбми* объявляются на [шаге 1: создание Windows Framework](step-1--create-the-windows-framework.md), а их значения получаются на [шаге 3. Реализация функции Frame-Grabbing](step-3--implement-the-frame-grabbing-function.md).</span><span class="sxs-lookup"><span data-stu-id="6c61d-108">The *pBuffer* and *pbmi* variables are declared in [Step 1: Create the Windows Framework](step-1--create-the-windows-framework.md), and their values are obtained in [Step 3: Implement the Frame-Grabbing Function](step-3--implement-the-frame-grabbing-function.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6c61d-109">См. также</span><span class="sxs-lookup"><span data-stu-id="6c61d-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6c61d-110">Зафрагментировать рамку афиши</span><span class="sxs-lookup"><span data-stu-id="6c61d-110">Grabbing a Poster Frame</span></span>](grabbing-a-poster-frame.md)
</dt> </dl>

 

 

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
# <a name="step-4-draw-the-bitmap-on-the-client-area"></a>Шаг 4. Рисование точечного рисунка в клиентской области

\[Этот API не поддерживается и может быть изменен или недоступен в будущем.\]

В этом разделе приведен шаг 4 из [фрагмента плаката](grabbing-a-poster-frame.md).

Последним шагом является Отрисовка точечного рисунка в клиентской области окна приложения с помощью функции [**сетдибитстодевице**](/windows/win32/api/wingdi/nf-wingdi-setdibitstodevice) . В этом примере точечный рисунок просто закрашивается в левом верхнем углу клиентской области без учета размера окна:


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



Переменные *pBuffer* и *пбми* объявляются на [шаге 1: создание Windows Framework](step-1--create-the-windows-framework.md), а их значения получаются на [шаге 3. Реализация функции Frame-Grabbing](step-3--implement-the-frame-grabbing-function.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Зафрагментировать рамку афиши](grabbing-a-poster-frame.md)
</dt> </dl>

 

 

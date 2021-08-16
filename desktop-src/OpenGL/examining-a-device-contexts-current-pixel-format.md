---
title: Проверка контекстов устройств текущий формат пикселей
description: Используйте функции Жетпикселформат и Дескрибепикселформат для проверки текущего формата пикселей контекста устройства, как показано в следующем фрагменте кода.
ms.assetid: 1da8c8e0-9444-421a-9c2e-c196b5a9db36
keywords:
- OpenGL на Windows, пикселей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b76dd8db71356b16a5a258669ffe2938d0982ab5e1417389840610c57a0fcdc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118361374"
---
# <a name="examining-a-device-contexts-current-pixel-format"></a>Проверка контекстов устройств текущий формат пикселей

Используйте функции [**жетпикселформат**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat) и [**дескрибепикселформат**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat) для проверки текущего формата пикселей контекста устройства, как показано в следующем фрагменте кода.


```C++
PIXELFORMATDESCRIPTOR  pfd;
HDC    hdc;
int    iPixelFormat;
 
// if the device context has a current pixel format ...  
if (iPixelFormat = GetPixelFormat(hdc)) { 
 
    // obtain a detailed description of that pixel format  
    DescribePixelFormat(hdc, iPixelFormat, 
                             sizeof(PIXELFORMATDESCRIPTOR), &pfd); 
    }
```



 

 





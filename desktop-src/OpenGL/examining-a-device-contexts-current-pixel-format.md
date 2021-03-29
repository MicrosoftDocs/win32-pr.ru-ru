---
title: Проверка контекстов устройств текущий формат пикселей
description: Используйте функции Жетпикселформат и Дескрибепикселформат для проверки текущего формата пикселей контекста устройства, как показано в следующем фрагменте кода.
ms.assetid: 1da8c8e0-9444-421a-9c2e-c196b5a9db36
keywords:
- OpenGL в Windows, ПКС
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea36f0f25b2cf76a6fb2ffb3159a4f2763a95af3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104253033"
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



 

 





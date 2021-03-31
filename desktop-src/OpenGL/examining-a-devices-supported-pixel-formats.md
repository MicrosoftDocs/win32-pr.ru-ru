---
title: Проверка поддерживаемых устройствами форматов пикселей
description: Функция Дескрибепикселформат получает данные формата пикселей для контекста устройства.
ms.assetid: 1ebeb051-2dc9-4753-a0f3-7d2737b5f7f2
keywords:
- OpenGL в Windows, ПКС
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05ee45212111354d79b7a23fd35490a08f0aead4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411274"
---
# <a name="examining-a-devices-supported-pixel-formats"></a>Проверка поддерживаемых устройствами форматов пикселей

Функция [**дескрибепикселформат**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat) получает данные формата пикселей для контекста устройства. Он также возвращает целое число, которое является максимальным индексом формата пикселей для контекста устройства. В следующем примере кода показано, как использовать этот результат для пошагового и изучения форматов пикселей, поддерживаемых устройством.


```C++
// local variables  
int                      iMax ; 
PIXELFORMATDESCRIPTOR    pfd; 
int                      iPixelFormat ; 
 
// initialize a pixel format index variable  
iPixelFormat = 1; 
 
// keep obtaining and examining pixel format data...  
do { 
    // try to obtain some pixel format data  
    iMax = DescribePixelFormat(hdc, iPixelFormat, sizeof(pfd), &pfd); 
 
    // if there was some problem with that...   
    if (iMax == 0) 
     
        // return indicating failure  
        return(FALSE); 
     
    // we have successfully obtained pixel format data  
 
    // let's examine the pixel format data...  
    myPixelFormatExaminer (&pfd); 
    }  
 
// ...until we've looked at all the device context's pixel formats  
while (++iPixelFormat <= iMax);
```



 

 





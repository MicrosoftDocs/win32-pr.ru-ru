---
title: Автономное приложение
description: Это автономное приложение, которое состоит из вызова одной функции, образует базу для нашего распределенного приложения.
ms.assetid: 640f5d01-84c8-4fe8-9dae-f4d55cc6f06b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 946d76d0259fd3db971da345a10108cb3dbe11c23184b4ea9a88254e4ecb5e0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118923868"
---
# <a name="the-standalone-application"></a>Автономное приложение

Это автономное приложение, которое состоит из вызова одной функции, образует базу для нашего распределенного приложения. Функция **хеллопрок** определена в собственном исходном файле, чтобы ее можно было скомпилировать и связать с отдельным приложением или распределенным приложением.


```C++
/* file hellop.c */
#include <stdio.h>
#include <windows.h>

void HelloProc(char * pszString)
{
    printf("%s\n", pszString);
}
 
/* file: hello.c, a stand-alone application */
#include "hellop.c"

void main(void)
{
    char * pszString = "Hello, World";
    HelloProc(pszString);
}
```



 

 





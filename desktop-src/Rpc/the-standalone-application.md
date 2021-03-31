---
title: Автономное приложение
description: Это автономное приложение, которое состоит из вызова одной функции, образует базу для нашего распределенного приложения.
ms.assetid: 640f5d01-84c8-4fe8-9dae-f4d55cc6f06b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddf1b11df2372a1db5c74659d1800b62e53b7309
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067970"
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



 

 





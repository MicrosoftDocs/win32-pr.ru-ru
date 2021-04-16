---
title: Получение адреса таблицы виртуальной функции
description: Получение адреса таблицы виртуальной функции
ms.assetid: c9e9e2df-75e6-4684-a465-6905e76b10a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c0d618e75d2c3a4fcc2550fca7cb90bd2a51d2f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532111"
---
# <a name="obtaining-the-address-of-a-virtual-function-table"></a>Получение адреса таблицы виртуальной функции

В приложении, написанном на языке C, можно получить адрес структуры **иавистреамвтбл** с помощью функции невбалл. Эта функция возвращает адрес структуры, содержащей указатель на **иавистреамвтбл**. Сведения, следующие за указателем **иавистреамвтбл** , указывают данные, используемые внутри авибалл. Обработчик потока может добавлять свои собственные данные после указателя **иавистреамвтбл** . Эти сведения возвращаются при последующих вызовах обработчика потока.


```C++
PAVISTREAM WINAPI NewBall(VOID) 
{ 
    PAVIBALL pball; 
    pball = (PAVIBALL) GlobalAllocPtr(GHND, sizeof(AVIBALL)); 
    if (!pball) 
        return 0; 
    pball->lpvtbl = &AVIBallHandler; 
    pball->lpvtbl->Create((PAVISTREAM) pball, 0, 0); 
    return (PAVISTREAM) pball; 
} 
```



 

 





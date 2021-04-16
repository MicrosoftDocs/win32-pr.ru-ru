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
# <a name="obtaining-the-address-of-a-virtual-function-table"></a><span data-ttu-id="209c1-103">Получение адреса таблицы виртуальной функции</span><span class="sxs-lookup"><span data-stu-id="209c1-103">Obtaining the Address of a Virtual Function Table</span></span>

<span data-ttu-id="209c1-104">В приложении, написанном на языке C, можно получить адрес структуры **иавистреамвтбл** с помощью функции невбалл.</span><span class="sxs-lookup"><span data-stu-id="209c1-104">In an application written in the C programming language, you can retrieve the address of the **IAVIStreamVtbl** structure by using the NewBall function.</span></span> <span data-ttu-id="209c1-105">Эта функция возвращает адрес структуры, содержащей указатель на **иавистреамвтбл**.</span><span class="sxs-lookup"><span data-stu-id="209c1-105">This function returns the address of a structure containing a pointer to **IAVIStreamVtbl**.</span></span> <span data-ttu-id="209c1-106">Сведения, следующие за указателем **иавистреамвтбл** , указывают данные, используемые внутри авибалл.</span><span class="sxs-lookup"><span data-stu-id="209c1-106">Information following the **IAVIStreamVtbl** pointer specifies data used internally by AVIBall.</span></span> <span data-ttu-id="209c1-107">Обработчик потока может добавлять свои собственные данные после указателя **иавистреамвтбл** .</span><span class="sxs-lookup"><span data-stu-id="209c1-107">Your stream handler can append its own information after the **IAVIStreamVtbl** pointer.</span></span> <span data-ttu-id="209c1-108">Эти сведения возвращаются при последующих вызовах обработчика потока.</span><span class="sxs-lookup"><span data-stu-id="209c1-108">This information is returned in subsequent calls to your stream handler.</span></span>


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



 

 





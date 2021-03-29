---
title: Создание указателя на объект
description: Создание указателя на объект
ms.assetid: b66a2725-6ba1-4aea-b165-fe3f4da00375
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f57451e2781a94642e61365d3a6c694758f4056
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104253106"
---
# <a name="creating-an-object-pointer"></a><span data-ttu-id="dad36-103">Создание указателя на объект</span><span class="sxs-lookup"><span data-stu-id="dad36-103">Creating an Object Pointer</span></span>

<span data-ttu-id="dad36-104">Авибалл использует в качестве указателя на объект следующую структуру.</span><span class="sxs-lookup"><span data-stu-id="dad36-104">AVIBall uses the following structure as its object pointer.</span></span> <span data-ttu-id="dad36-105">Первый элемент этой структуры указывает на таблицу виртуальной функции, которую Авибалл использует для доступа к ее функциям.</span><span class="sxs-lookup"><span data-stu-id="dad36-105">The first member of this structure points to the virtual function table that AVIBall uses to access its functions.</span></span> <span data-ttu-id="dad36-106">Приложения могут привести эту структуру к типу данных ПАВИСТРЕАМ.</span><span class="sxs-lookup"><span data-stu-id="dad36-106">Applications can cast this structure to the PAVISTREAM data type.</span></span> <span data-ttu-id="dad36-107">Методы, использующие тип данных ПАВИСТРЕАМ, используют только указатель на таблицу виртуальной функции.</span><span class="sxs-lookup"><span data-stu-id="dad36-107">Methods that use the PAVISTREAM data type use only the pointer to the virtual function table.</span></span> <span data-ttu-id="dad36-108">Элементы, следующие за указателем на таблицу виртуальной функции, используются внутренне Авибалл.</span><span class="sxs-lookup"><span data-stu-id="dad36-108">The members following the pointer to the virtual function table are used internally by AVIBall.</span></span>


```C++
typedef struct 
{ 
    IAVIStreamVtbl FAR * lpvtbl; 
 
    // Ball instance data. 
    ULONG     ulRefCount; 
    DWORD     fccType;  // is this audio/video? 
    int        width;    // size, in pixels, of each frame 
    int        height; 
    int        length;   // length, in frames 
    int        size; 
    COLORREF    color;    // ball color 
} AVIBALL, FAR * PAVIBALL; 

```



 

 





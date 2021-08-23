---
title: Создание указателя на объект
description: Создание указателя на объект
ms.assetid: b66a2725-6ba1-4aea-b165-fe3f4da00375
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586ba0b8c9ee261e29f21ed58c84193f4cc89d1399c62d75d82a2c0a49075dcc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144687"
---
# <a name="creating-an-object-pointer"></a>Создание указателя на объект

Авибалл использует в качестве указателя на объект следующую структуру. Первый элемент этой структуры указывает на таблицу виртуальной функции, которую Авибалл использует для доступа к ее функциям. Приложения могут привести эту структуру к типу данных ПАВИСТРЕАМ. Методы, использующие тип данных ПАВИСТРЕАМ, используют только указатель на таблицу виртуальной функции. Элементы, следующие за указателем на таблицу виртуальной функции, используются внутренне Авибалл.


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



 

 





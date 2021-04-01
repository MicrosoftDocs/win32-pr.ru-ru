---
description: Определяет нормали для сетки.
ms.assetid: 05f17128-dfc9-4a78-b23c-0420a1c3d1bd
title: мешнормалс
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65b9e0ffc89af5a0a55ef7bd1fa2575a4943137e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104262408"
---
# <a name="meshnormals"></a>мешнормалс

Определяет нормали для сетки. Первый массив векторов — это обычные векторы, а второй массив — это массив индексов, указывающий, какие нормали должны применяться к данной грани. Значение элемента Нфаценормалс должно быть равно числу граней в сети.

``` syntax
template MeshNormals
{
    < F6F23F43-7686-11cf-8F52-0040333594A3 >
    DWORD nNormals;
    array Vector normals[nNormals];
    DWORD nFaceNormals;
    array MeshFace faceNormals[nFaceNormals];
} 
```

Где:

-   Ннормалс — число нормалей.
-   Векторы массивов нормали \[ ннормалс \] -Array нормалей. См. раздел [**vector**](vector.md).
-   Нфаценормалс — число нормальных граней.
-   Array Мешфаце Фаценормалс \[ нфаценормалс \] -массив нормалей граней. См. [**мешфаце**](meshface.md).

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Шаблоны](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 




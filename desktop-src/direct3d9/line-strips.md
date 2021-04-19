---
description: Ломаная — это примитив, состоящий из соединенных отрезков.
ms.assetid: 73905718-a4c6-4f73-beef-4cccac7eea8c
title: Полосы строк
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dee7eb79b583ad04dc0ed576a7d9426e8dda9fa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537616"
---
# <a name="line-strips"></a>Полосы строк

Ломаная — это примитив, состоящий из соединенных отрезков. Приложение может использовать ломаные линии для создания незамкнутых многоугольников. Замкнутый многоугольник — это многоугольник, последняя вершина которого соединяется отрезком с его первой вершиной. Если приложение создает многоугольники на основе ломаных, вершины могут находиться в разных плоскостях.

На следующем рисунке показана отрисованная ломаная линия.

![иллюстрация ломаной линии](images/linstrip.gif)

Следующий код показывает, как создать вершины для такой ломаной линии.


```
struct CUSTOMVERTEX
{
    float x,y,z;
};

CUSTOMVERTEX Vertices[] = 
{
    {-5.0, -5.0, 0.0},
    { 0.0,  5.0, 0.0},
    { 5.0, -5.0, 0.0},
    {10.0,  5.0, 0.0},
    {15.0, -5.0, 0.0},
    {20.0,  5.0, 0.0}
};
```



В приведенном ниже примере кода показано, как отобразить полосу строк в Direct3D 9 с помощью [**IDirect3DDevice9::D равпримитиве**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) .


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_LINESTRIP, 0, 5 );
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Примитивы](primitives.md)
</dt> </dl>

 

 

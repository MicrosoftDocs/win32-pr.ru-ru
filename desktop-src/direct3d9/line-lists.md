---
description: Список линий — это список изолированных прямых отрезков.
ms.assetid: bb02b3d6-f30f-4f2b-8b40-a7e37faf524a
title: Списки строк
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f06ca68e3fefab1217e77bbf41bc30aa42dac9631b70480fe4bf0a98d38d913
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606803"
---
# <a name="line-lists"></a>Списки строк

Список линий — это список изолированных прямых отрезков. Списки линий полезны для таких задач, как добавление дождя или ливня в трехмерную сцену. Приложения создают списки линий, заполняя массив вершин. Обратите внимание, что число вершин в списке линий должно быть четным числом больше двух или равным двум.

На следующем рисунке показан список отображаемых линий.

![иллюстрация списка линий](images/linelst.png)

К списку линий можно применять материалы и текстуры. Цвета в материале или текстуре отображаются только на прорисованных линиях и отсутствуют во всех других точках, не относящихся к этим линиям.

Следующий код показывает, как создать вершины для такого списка линий.


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



В приведенном ниже примере кода показано, как отобразить список строк в Direct3D 9 с помощью [**IDirect3DDevice9::D равпримитиве**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_LINELIST, 0, 3 );
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Примитивы](primitives.md)
</dt> </dl>

 

 

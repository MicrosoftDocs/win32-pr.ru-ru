---
description: Перечисление D3DXMESHOPT — указывает тип выполняемой оптимизации сетки.
ms.assetid: 32ef227a-b299-47c4-96b8-c0ea7bf549e1
title: Перечисление D3DXMESHOPT (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _D3DXMESHOPT
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: d4d26538832a698909ace59da42b13ae51aef93d2d4d622b687f324a62d8361e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986494"
---
# <a name="d3dxmeshopt-enumeration"></a>Перечисление D3DXMESHOPT

Указывает тип оптимизации сетки для выполнения.

## <a name="syntax"></a>Синтаксис


```C++
enum _D3DXMESHOPT {
  D3DXMESHOPT_COMPACT            = 0x01000000, 
  D3DXMESHOPT_ATTRSORT           = 0x02000000, 
  D3DXMESHOPT_VERTEXCACHE        = 0x04000000, 
  D3DXMESHOPT_STRIPREORDER       = 0x08000000, 
  D3DXMESHOPT_IGNOREVERTS        = 0x10000000, 
  D3DXMESHOPT_DONOTSPLIT         = 0x20000000, 
  D3DXMESHOPT_DEVICEINDEPENDENT  = 0x40000000 

};
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="D3DXMESHOPT_COMPACT"></span><span id="d3dxmeshopt_compact"></span>**D3DXMESHOPT \_ Compact**
</dt> <dd>

Переупорядочивает лица, чтобы удалить неиспользуемые вершины и грани.

</dd> <dt>

<span id="D3DXMESHOPT_ATTRSORT"></span><span id="d3dxmeshopt_attrsort"></span>**D3DXMESHOPT \_ аттрсорт**
</dt> <dd>

Переупорядочивает лиц, чтобы оптимизировать для уменьшения количества изменений состояния набора атрибутов и повышения производительности [**ID3DXBaseMesh::D равсубсет**](id3dxbasemesh--drawsubset.md) .

</dd> <dt>

<span id="D3DXMESHOPT_VERTEXCACHE"></span><span id="d3dxmeshopt_vertexcache"></span>**D3DXMESHOPT \_ вертекскаче**
</dt> <dd>

Переупорядочивает лиц, чтобы увеличить количество попаданий в кэш вершин.

</dd> <dt>

<span id="D3DXMESHOPT_STRIPREORDER"></span><span id="d3dxmeshopt_stripreorder"></span>**D3DXMESHOPT \_ стрипреордер**
</dt> <dd>

Переупорядочивает лиц, чтобы максимально увеличить длину смежных треугольников.

</dd> <dt>

<span id="D3DXMESHOPT_IGNOREVERTS"></span><span id="d3dxmeshopt_ignoreverts"></span>**D3DXMESHOPT \_ игноревертс**
</dt> <dd>

Оптимизируйте только грани; не Оптимизируйте вершины.

</dd> <dt>

<span id="D3DXMESHOPT_DONOTSPLIT"></span><span id="d3dxmeshopt_donotsplit"></span>**D3DXMESHOPT \_ донотсплит**
</dt> <dd>

При сортировке атрибутов не разделите вершины, которые являются общими между группами атрибутов.

</dd> <dt>

<span id="D3DXMESHOPT_DEVICEINDEPENDENT"></span><span id="d3dxmeshopt_deviceindependent"></span>**D3DXMESHOPT \_ девицеиндепендент**
</dt> <dd>

Влияет на размер кэша вершин. С помощью этого флага задается размер кэша вершин по умолчанию, который хорошо работает на устаревшем оборудовании.

</dd> </dl>

## <a name="remarks"></a>Remarks

\_Флаги оптимизации D3DXMESHOPT стрипреордер и D3DXMESHOPT \_ вертекскаче являются взаимоисключающими.

Флаг D3DXMESHOPT \_ шаревб был удален из этого перечисления. \_ \_ Вместо этого используйте общую папку VB D3DXMESH в [**D3DXMESH**](./d3dxmesh.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Перечисления D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 

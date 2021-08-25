---
description: Определяет операции, выполняемые с вершинами при подготовке к очистке сетки.
ms.assetid: f222acaa-fa82-4591-b7c2-b520cb648ed5
title: Перечисление D3DXCLEANTYPE (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCLEANTYPE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 2517c59d5505a8f2892ef0aee1d3884b8d489625637002d6e69a4f86434237fd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894114"
---
# <a name="d3dxcleantype-enumeration"></a>Перечисление D3DXCLEANTYPE

Определяет операции, выполняемые с вершинами при подготовке к очистке сетки.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum D3DXCLEANTYPE { 
  D3DXCLEAN_BACKFACING      = 1,
  D3DXCLEAN_BOWTIES         = 2,
  D3DXCLEAN_SKINNING        = D3DXCLEAN_BACKFACING,
  D3DXCLEAN_OPTIMIZATION    = D3DXCLEAN_BACKFACING,
  D3DXCLEAN_SIMPLIFICATION  = D3DXCLEAN_BACKFACING | D3DXCLEAN_BOWTIES
} D3DXCLEANTYPE, *LPD3DXCLEANTYPE;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="D3DXCLEAN_BACKFACING"></span><span id="d3dxclean_backfacing"></span>**D3DXCLEAN с \_ выходом**
</dt> <dd>

Объедините треугольники, которые используют одни и те же индексы вершин, но имеют обычные нормали, указывающие в противоположных направлениях (треугольники с обратным переходом). Если треугольники не разбиваются путем добавления реплицируемой вершины, то данные о смежности между сетками из двух треугольников могут конфликтовать.

</dd> <dt>

<span id="D3DXCLEAN_BOWTIES"></span><span id="d3dxclean_bowties"></span>**D3DXCLEAN \_ бовтиес**
</dt> <dd>

Если вершина является вершине двух треугольников (bowtie), а операции сетки повлияют на один из вентиляторов, то разделите общую вершину на две новые вершины. Бовтиес может вызвать проблемы для таких операций, как упрощение сетки, которое удаляет вершины, так как удаление одной вершины влияет на два отдельных набора треугольников.

</dd> <dt>

<span id="D3DXCLEAN_SKINNING"></span><span id="d3dxclean_skinning"></span>**Выбор \_ обложки D3DXCLEAN**
</dt> <dd>

Используйте этот флаг, чтобы предотвратить бесконечные циклы во время операций настройки сетки.

</dd> <dt>

<span id="D3DXCLEAN_OPTIMIZATION"></span><span id="d3dxclean_optimization"></span>**\_Оптимизация D3DXCLEAN**
</dt> <dd>

Используйте этот флаг, чтобы предотвратить бесконечные циклы во время операций оптимизации сетки.

</dd> <dt>

<span id="D3DXCLEAN_SIMPLIFICATION"></span><span id="d3dxclean_simplification"></span>**\_Упрощение D3DXCLEAN**
</dt> <dd>

Используйте этот флаг, чтобы предотвратить бесконечные циклы во время операций упрощения сетки.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Перечисления D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 





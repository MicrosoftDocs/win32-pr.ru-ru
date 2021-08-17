---
description: Измеряет скорость попадания в кэш для текстур и индексированных вершин.
ms.assetid: 70bc4e93-0a34-485b-bdcc-028c24b52f62
title: Структура D3DDEVINFO_D3D9CACHEUTILIZATION (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9CACHEUTILIZATION
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 01f0521ca7833cd74c3cb45b5a650fbd12aae485e36a153b57e6d9b10b49d1f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117733075"
---
# <a name="d3ddevinfo_d3d9cacheutilization-structure"></a>\_Структура D3D9CACHEUTILIZATION D3DDEVINFO

Измеряет скорость попадания в кэш для текстур и индексированных вершин.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DDEVINFO_D3D9CACHEUTILIZATION {
  FLOAT TextureCacheHitRate;
  FLOAT PostTransformVertexCacheHitRate;
} D3DDEVINFO_D3D9CACHEUTILIZATION, *LPD3DDEVINFO_D3D9CACHEUTILIZATION;
```



## <a name="members"></a>Члены

<dl> <dt>

**текстурекачехитрате**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Коэффициент попадания для поиска текстуры в кэше текстуры. В этом случае предполагается наличие кэша текстуры. Увеличение уровня детализации для использования наиболее подробной текстуры, использование большого количества крупных текстур или создание практически случайного шаблона доступа к текстуре на больших текстурах с помощью пользовательского кода шейдера может значительно повлиять на скорость попаданий в кэш текстуры.

</dd> <dt>

**посттрансформвертекскачехитрате**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Коэффициент попадания для поиска преобразованных вершин в кэше вершин. GPU предназначен для преобразования индексированных вершин и может хранить их в кэше вершин. Если используются сети, [**D3DXOptimizeFaces**](d3dxoptimizefaces.md) или [**D3DXOptimizeVertices**](d3dxoptimizevertices.md) могут повысить эффективность использования кэша вершин.

</dd> </dl>

## <a name="remarks"></a>Remarks

Эффективный кэш, как правило, приближается к проценту попадания в 90 процентов, а неэффективный кэш, как правило, приближается к проценту попадания в 10 процентов (хотя низкий процент не обязательно является проблемой).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 

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
ms.openlocfilehash: 94f77549d0ea2a9c59d7de8367a6133085cc2771
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104547847"
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

## <a name="remarks"></a>Комментарии

Эффективный кэш, как правило, приближается к проценту попадания в 90 процентов, а неэффективный кэш, как правило, приближается к проценту попадания в 10 процентов (хотя низкий процент не обязательно является проблемой).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 

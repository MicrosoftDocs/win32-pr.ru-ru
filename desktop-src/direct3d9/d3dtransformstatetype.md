---
description: Определяет константы, описывающие значения состояния преобразования.
ms.assetid: 53535d9f-246a-42cf-82a2-fb3cf6d4ebac
title: Перечисление D3DTRANSFORMSTATETYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTRANSFORMSTATETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: c618e0e19bf7dd01dec73d35436f23189f9e78a6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713599"
---
# <a name="d3dtransformstatetype-enumeration"></a>Перечисление D3DTRANSFORMSTATETYPE

Определяет константы, описывающие значения состояния преобразования.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum D3DTRANSFORMSTATETYPE { 
  D3DTS_VIEW         = 2,
  D3DTS_PROJECTION   = 3,
  D3DTS_TEXTURE0     = 16,
  D3DTS_TEXTURE1     = 17,
  D3DTS_TEXTURE2     = 18,
  D3DTS_TEXTURE3     = 19,
  D3DTS_TEXTURE4     = 20,
  D3DTS_TEXTURE5     = 21,
  D3DTS_TEXTURE6     = 22,
  D3DTS_TEXTURE7     = 23,
  D3DTS_FORCE_DWORD  = 0x7fffffff
} D3DTRANSFORMSTATETYPE, *LPD3DTRANSFORMSTATETYPE;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="D3DTS_VIEW"></span><span id="d3dts_view"></span>**D3DTS, \_ представление**
</dt> <dd>

Определяет матрицу преобразования, заданную как матрица преобразования представления. Значение по умолчанию — **null** (матрица идентификаторов).

</dd> <dt>

<span id="D3DTS_PROJECTION"></span><span id="d3dts_projection"></span>**\_ПРОЕКЦИЯ D3DTS**
</dt> <dd>

Определяет матрицу преобразования, заданную как матрица преобразования проекции. Значение по умолчанию — **null** (матрица идентификаторов).

</dd> <dt>

<span id="D3DTS_TEXTURE0"></span><span id="d3dts_texture0"></span>**D3DTS \_ TEXTURE0**
</dt> <dd>

Определяет матрицу преобразования, заданную для указанной стадии текстуры.

</dd> <dt>

<span id="D3DTS_TEXTURE1"></span><span id="d3dts_texture1"></span>**D3DTS \_ TEXTURE1**
</dt> <dd>

Определяет матрицу преобразования, заданную для указанной стадии текстуры.

</dd> <dt>

<span id="D3DTS_TEXTURE2"></span><span id="d3dts_texture2"></span>**D3DTS \_ TEXTURE2**
</dt> <dd>

Определяет матрицу преобразования, заданную для указанной стадии текстуры.

</dd> <dt>

<span id="D3DTS_TEXTURE3"></span><span id="d3dts_texture3"></span>**D3DTS \_ TEXTURE3**
</dt> <dd>

Определяет матрицу преобразования, заданную для указанной стадии текстуры.

</dd> <dt>

<span id="D3DTS_TEXTURE4"></span><span id="d3dts_texture4"></span>**D3DTS \_ TEXTURE4**
</dt> <dd>

Определяет матрицу преобразования, заданную для указанной стадии текстуры.

</dd> <dt>

<span id="D3DTS_TEXTURE5"></span><span id="d3dts_texture5"></span>**D3DTS \_ TEXTURE5**
</dt> <dd>

Определяет матрицу преобразования, заданную для указанной стадии текстуры.

</dd> <dt>

<span id="D3DTS_TEXTURE6"></span><span id="d3dts_texture6"></span>**D3DTS \_ TEXTURE6**
</dt> <dd>

Определяет матрицу преобразования, заданную для указанной стадии текстуры.

</dd> <dt>

<span id="D3DTS_TEXTURE7"></span><span id="d3dts_texture7"></span>**D3DTS \_ TEXTURE7**
</dt> <dd>

Определяет матрицу преобразования, заданную для указанной стадии текстуры.

</dd> <dt>

<span id="D3DTS_FORCE_DWORD"></span><span id="d3dts_force_dword"></span>**D3DTS \_ Force \_ DWORD**
</dt> <dd>

Заставляет это перечисление компилироваться до 32 бит в размере. Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит. Это значение не используется.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Состояния преобразования в диапазоне от 256 до 511 зарезервированы для хранения до 256 матриц мира, которые можно индексировать с помощью \_ макросов D3DTS ворлдматрикс и D3DTS \_ World.



| Макросы                                                  |                                                                                                                                                                       |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**D3DTS \_ мир**](d3dts-world.md)                     | Эквивалентно D3DTS \_ ворлдматрикс (0).                                                                                                                                  |
| [**D3DTS \_ ВОРЛДМАТРИКС**](d3dts-worldmatrix.md) (индекс) | Определяет матрицу преобразования, заданную для матрицы мира по индексу. Несколько мировых матриц используются только для смешивания вершин. В противном случае используется только D3DTS \_ World. |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Перечисления Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3DDevice9:: Transform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettransform)
</dt> <dt>

[**IDirect3DDevice9:: Мултиплитрансформ**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-multiplytransform)
</dt> <dt>

[**IDirect3DDevice9:: Сеттрансформ**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
</dt> <dt>

[**D3DTS \_ мир**](d3dts-world.md)
</dt> <dt>

[**D3DTS \_ ворлдн**](d3dts-worldn.md)
</dt> <dt>

[**D3DTS \_ ворлдматрикс**](d3dts-worldmatrix.md)
</dt> </dl>

 

 

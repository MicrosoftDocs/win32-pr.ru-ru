---
description: Определяет значения преобразования координат текстуры.
ms.assetid: a91f33ce-2db5-437a-ac29-402b26b0d4e1
title: Перечисление D3DTEXTURETRANSFORMFLAGS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTURETRANSFORMFLAGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 514b8066b19ea5a3f558d9edee7cd57bae69dbb443e9b662a0209c9b57b58f31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118096609"
---
# <a name="d3dtexturetransformflags-enumeration"></a>Перечисление D3DTEXTURETRANSFORMFLAGS

Определяет значения преобразования координат текстуры.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum D3DTEXTURETRANSFORMFLAGS { 
  D3DTTFF_DISABLE      = 0,
  D3DTTFF_COUNT1       = 1,
  D3DTTFF_COUNT2       = 2,
  D3DTTFF_COUNT3       = 3,
  D3DTTFF_COUNT4       = 4,
  D3DTTFF_PROJECTED    = 256,
  D3DTTFF_FORCE_DWORD  = 0x7fffffff
} D3DTEXTURETRANSFORMFLAGS, *LPD3DTEXTURETRANSFORMFLAGS;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="D3DTTFF_DISABLE"></span><span id="d3dttff_disable"></span>**\_Отключение D3DTTFF**
</dt> <dd>

Координаты текстуры передаются непосредственно в средство программной прорисовки.

</dd> <dt>

<span id="D3DTTFF_COUNT1"></span><span id="d3dttff_count1"></span>**D3DTTFF \_ COUNT1**
</dt> <dd>

Средство программной прорисовки должно рассчитывать Координаты одномерной текстуры. Это значение используется при обработке вершин фиксированной функции. При использовании программируемого шейдера вершин для него должно быть задано значение 0.

</dd> <dt>

<span id="D3DTTFF_COUNT2"></span><span id="d3dttff_count2"></span>**D3DTTFF \_ COUNT2**
</dt> <dd>

Средство программной прорисовки должно рассчитывать координаты двухмерной текстуры. Это значение используется при обработке вершин фиксированной функции. При использовании программируемого шейдера вершин для него должно быть задано значение 0.

</dd> <dt>

<span id="D3DTTFF_COUNT3"></span><span id="d3dttff_count3"></span>**D3DTTFF \_ COUNT3**
</dt> <dd>

Средство программной прорисовки должно рассчитывать координаты трехмерной текстуры. Это значение используется при обработке вершин фиксированной функции. При использовании программируемого шейдера вершин для него должно быть задано значение 0.

</dd> <dt>

<span id="D3DTTFF_COUNT4"></span><span id="d3dttff_count4"></span>**D3DTTFF \_ COUNT4**
</dt> <dd>

Средство программной прорисовки должно рассчитывать координаты текстуры 4D. Это значение используется при обработке вершин фиксированной функции. При использовании программируемого шейдера вершин для него должно быть задано значение 0.

</dd> <dt>

<span id="D3DTTFF_PROJECTED"></span><span id="d3dttff_projected"></span>**D3DTTFF \_ Прогноз**
</dt> <dd>

Этот флаг учитывается с помощью конвейера пикселей функции с фиксированной функцией, а также программируемого конвейера пикселей в версиях PS \_ 1 \_ 1 до PS \_ 1 \_ 3. Если для этапа текстуры включена проекция текстуры, все четыре значения с плавающей запятой должны быть записаны в соответствующий регистр текстуры. Каждая координата текстуры делится на последний элемент перед передачей в средство программной прорисовки. Например, если этот флаг указан с \_ флагом D3DTTFF COUNT3, то первая и вторая координаты текстуры делятся на третью координат перед передачей в средство программной прорисовки.

</dd> <dt>

<span id="D3DTTFF_FORCE_DWORD"></span><span id="d3dttff_force_dword"></span>**D3DTTFF \_ Force \_ DWORD**
</dt> <dd>

Заставляет это перечисление компилироваться до 32 бит в размере. Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит. Это значение не используется.

</dd> </dl>

## <a name="remarks"></a>Remarks

Координаты текстуры можно преобразовать с помощью матрицы размером 4 x 4 до передачи результатов в средство программной прорисовки. Преобразования координат текстуры задаются путем вызова [**IDirect3DDevice9:: сеттекстурестажестате**](/windows/desktop/api)и передачи в \_ состояние этапа текстуры D3DTSS текстуретрансформфлагс и одного из значений из **D3DTEXTURETRANSFORMFLAGS**. Дополнительные сведения о преобразованиях текстур см. в разделе [преобразования координат текстуры (Direct3D 9)](texture-coordinate-transformations.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Перечисления Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md)
</dt> </dl>

 

 

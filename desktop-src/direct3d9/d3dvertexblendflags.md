---
description: Определяет флаги, используемые для управления числом или матрицами, применяемыми системой при выполнении многоматричного смешения вершин.
ms.assetid: 5314f455-ce5f-4ff5-81fc-d3dffc8705b7
title: Перечисление D3DVERTEXBLENDFLAGS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVERTEXBLENDFLAGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: ecc7f99e26088ff03b626604279bffe5c64ddb82b95a6f6219b637b3fce5a59b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118527308"
---
# <a name="d3dvertexblendflags-enumeration"></a>Перечисление D3DVERTEXBLENDFLAGS

Определяет флаги, используемые для управления числом или матрицами, применяемыми системой при выполнении многоматричного смешения вершин.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum D3DVERTEXBLENDFLAGS { 
  D3DVBF_DISABLE   = 0,
  D3DVBF_1WEIGHTS  = 1,
  D3DVBF_2WEIGHTS  = 2,
  D3DVBF_3WEIGHTS  = 3,
  D3DVBF_TWEENING  = 255,
  D3DVBF_0WEIGHTS  = 256
} D3DVERTEXBLENDFLAGS, *LPD3DVERTEXBLENDFLAGS;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="D3DVBF_DISABLE"></span><span id="d3dvbf_disable"></span>**\_Отключение D3DVBF**
</dt> <dd>

Отключить смешение вершин; Примените только матрицу World, заданную с помощью макроса [**D3DTS \_ ворлдматрикс**](d3dts-worldmatrix.md) , где значение индекса для состояния преобразования равно 0.

</dd> <dt>

<span id="D3DVBF_1WEIGHTS"></span><span id="d3dvbf_1weights"></span>**D3DVBF \_ 1WEIGHTS**
</dt> <dd>

Включите смешение вершин между двумя матрицами, заданными в макросе [**D3DTS \_ ворлдматрикс**](d3dts-worldmatrix.md) , где значение индекса для состояний преобразования — 0 и 1.

</dd> <dt>

<span id="D3DVBF_2WEIGHTS"></span><span id="d3dvbf_2weights"></span>**D3DVBF \_ 2WEIGHTS**
</dt> <dd>

Включите смешение вершин между тремя матрицами, заданными в макросе [**D3DTS \_ ворлдматрикс**](d3dts-worldmatrix.md) , где значение индекса для состояний преобразования — 0, 1 и 2.

</dd> <dt>

<span id="D3DVBF_3WEIGHTS"></span><span id="d3dvbf_3weights"></span>**D3DVBF \_ 3WEIGHTS**
</dt> <dd>

Включите смешение вершин между четырьмя матрицами, заданными в макросе [**D3DTS \_ ворлдматрикс**](d3dts-worldmatrix.md) , где значение индекса для состояний преобразования — 0, 1, 2 и 3.

</dd> <dt>

<span id="D3DVBF_TWEENING"></span><span id="d3dvbf_tweening"></span>**Tween — D3DVBF \_**
</dt> <dd>

Смешивание вершин выполняется с использованием значения, присвоенного D3DRS \_ твинфактор.

</dd> <dt>

<span id="D3DVBF_0WEIGHTS"></span><span id="d3dvbf_0weights"></span>**D3DVBF \_ 0WEIGHTS**
</dt> <dd>

Используйте одну матрицу с весом 1,0.

</dd> </dl>

## <a name="remarks"></a>Remarks

Члены этого типа используются с \_ состоянием отрисовки D3DRS вертексбленд.

Смешивание геометрических объектов (многоматричное смешение вершин) требует, чтобы приложение использовало формат вершин, в котором для каждой вершины используются веса смешения (бета-версии).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Перечисления Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> <dt>

[**D3DTS \_ мир**](d3dts-world.md)
</dt> <dt>

[**D3DTS \_ ворлдн**](d3dts-worldn.md)
</dt> <dt>

[**D3DTS \_ ворлдматрикс**](d3dts-worldmatrix.md)
</dt> </dl>

 

 

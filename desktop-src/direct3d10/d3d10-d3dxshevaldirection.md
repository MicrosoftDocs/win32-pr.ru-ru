---
description: Функция D3DXSHEvalDirection (D3DX10. h) — вычисляет основные функции сферического гармонического (SH) на основе вектора направления ввода.
ms.assetid: c86973cc-c5b0-4358-b7eb-5c31f38b5b5a
title: Функция D3DXSHEvalDirection (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHEvalDirection
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: bf52e29962e773798073ad6c779394318fcfcbc7186db5b4f0e6862a8e7b672c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070034"
---
# <a name="d3dxshevaldirection-function-d3dx10h"></a>Функция D3DXSHEvalDirection (D3DX10. h)

Вычисляет основные функции "сферический гармонией" (SH) на основе вектора направления ввода.

## <a name="syntax"></a>Синтаксис


```C++
FLOAT* D3DXSHEvalDirection(
  _In_       FLOAT       *pOut,
  _In_       UINT        Order,
  _In_ const D3DXVECTOR3 *pDir
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тоска* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)\***

Указатель на коэффициенты вывода в сферическую гармонию (SH). При оценке создается коэффициент порядка ². См. заметки.

</dd> <dt>

*Порядок следования* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Порядок вычисления SH. Должен находиться в диапазоне от D3DXSH \_ минордер до D3DXSH \_ максордер, включительно. При оценке создается коэффициент порядка ². Степень оценки — Order-1.

</dd> <dt>

*пдир* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

вектор направления (x, y, z), в котором оцениваются функции-основания SH. Должен быть нормализован. См. заметки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **float**](../winprog/windows-data-types.md)\***

Указатель на коэффициенты вывода SH. См. заметки.

## <a name="remarks"></a>Remarks

Каждый коэффициент базисной функции илм хранится в памяти l ² + m + l, где:

-   l — это степень базовой функции.
-   m — это базовый индекс функции для заданного значения l и диапазон от-l до l включительно.

В сфере с радиусом единицы, как показано на следующем рисунке, направление может быть задано просто с помощью тета, угла относительно оси z в правильном направлении, а значение фи — от z.

![Иллюстрация сферы с радиусом единицы](images/spherical-coordinates.png)

В следующих уравнениях показана связь между координатами декартовы (x, y, z) и сферами (тета, фи) в единичной сфере. Угол тета зависит от диапазона от 0 до 2 Пи, а значение фи отличается от 0 до PI.

![формулы связи между декартовы и сферыми координатами](images/spherical-coordinates-equations.png)

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Математические функции](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 

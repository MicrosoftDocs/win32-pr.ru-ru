---
description: Функция D3DXSHEvalConeLight (D3DX10. h) — вычисляет освещение, которое представляет собой конус с постоянной интенсивностью и возвращает Спектрал сферическую гармонию (SH) данных.
ms.assetid: ad2b9c86-cf1a-426e-88e6-4c543519e002
title: Функция D3DXSHEvalConeLight (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHEvalConeLight
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: fc11e7bab4cbbd6c8a685b289d4bde476cd465ca
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108612"
---
# <a name="d3dxshevalconelight-function-d3dx10h"></a>Функция D3DXSHEvalConeLight (D3DX10. h)

Вычисляет освещение, которое представляет собой конус с постоянной интенсивностью и возвращает Спектрал сферическую гармонию (SH) данных.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXSHEvalConeLight(
  _In_       UINT        Order,
  _In_ const D3DXVECTOR3 *pDir,
  _In_       FLOAT       Radius,
  _In_       FLOAT       RIntensity,
  _In_       FLOAT       GIntensity,
  _In_       FLOAT       BIntensity,
  _In_       FLOAT       *pROut,
  _In_       FLOAT       *pGOut,
  _In_       FLOAT       *pBOut
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Порядок следования* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Порядок вычисления SH. Должен находиться в диапазоне от D3DXSH \_ минордер до D3DXSH \_ максордер, включительно. При оценке создается коэффициент порядка ². Степень оценки — Order-1.

</dd> <dt>

*пдир* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Указатель на вектор направления (x, y, z) полушари оси, в котором оцениваются функции-основания SH. См. заметки.

</dd> <dt>

*Радиус* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Радиус конуса в радианах.

</dd> <dt>

*Ринтенсити* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Красная интенсивность освещения.

</dd> <dt>

*Гинтенсити* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Зеленая интенсивность освещения.

</dd> <dt>

*Бинтенсити* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Синяя интенсивность освещения.

</dd> <dt>

*Праут* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)\***

Указатель на выходной вектор SH для красного компонента.

</dd> <dt>

*пгаут* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)\***

Указатель на выходной вектор SH для зеленого компонента.

</dd> <dt>

*пбаут* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)\***

Указатель на выходной вектор SH для синего компонента.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть следующим: D3DERR \_ инвалидкалл.

## <a name="remarks"></a>Remarks

Вычисляет освещение, которое представляет собой конус с постоянной интенсивностью и возвращает Спектрал данные SH. Выходной вектор выдается таким образом, что если коэффициент интенсивности/G/B равен 1, радианце выхода точки непосредственно под светлой стороной (ориентированной на конусное направление на рассеянном объекте с албедоом 1) будет 1,0. Будет выполнено вычисление трех примеров Спектрал. Праут будет возвращен, тогда как Пгаут и Пбаут могут быть возвращены.

В сфере с радиусом единицы, как показано на следующем рисунке, направление может быть задано просто с помощью тета, угла относительно оси z в правильном направлении, а значение фи — от z.

![Иллюстрация сферы с радиусом единицы](images/spherical-coordinates.png)

В следующих уравнениях показана связь между координатами декартовы (x, y, z) и сферами (тета, фи) в единичной сфере. Угол тета зависит от диапазона от 0 до 2 Пи, а значение фи отличается от 0 до PI.

![формулы связи между декартовы и сферыми координатами](images/spherical-coordinates-equations.png)

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Математические функции](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 

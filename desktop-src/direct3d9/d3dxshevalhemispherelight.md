---
description: Функция D3DXSHEvalHemisphereLight (D3dx9math. h) — вычисляет освещение, которое является линейной интерполяцией между двумя цветами в сфере.
ms.assetid: c5815f12-f706-40f6-bf5e-78a211cfbbea
title: Функция D3DXSHEvalHemisphereLight (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHEvalHemisphereLight
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7bc06dcf866c21cc5dcb96b23dea5a4640293fef
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093972"
---
# <a name="d3dxshevalhemispherelight-function-d3dx9mathh"></a>Функция D3DXSHEvalHemisphereLight (D3dx9math. h)

Вычисляет освещение, которое является линейной интерполяцией между двумя цветами в сфере.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXSHEvalHemisphereLight(
  _In_       UINT        Order,
  _In_ const D3DXVECTOR3 *pDir,
  _In_       D3DXCOLOR   Top,
  _In_       D3DXCOLOR   Bottom,
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

Порядок вычисления сферического гармонического (SH). Должен находиться в диапазоне от [D3DXSH \_ МИНОРДЕР](other-d3dx-constants.md) до D3DXSH \_ максордер, включительно. При оценке создается коэффициент порядка ². Степень оценки — Order-1.

</dd> <dt>

*пдир* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Указатель на вектор направления (x, y, z) полушари оси, в котором оцениваются функции-основания SH. См. заметки.

</dd> <dt>

В *Начало* \[ окне\]
</dt> <dd>

Тип: **[ **D3DXCOLOR**](d3dxcolor.md)**

Голубой цвет.

</dd> <dt>

По *нижнему краю* \[ окне\]
</dt> <dd>

Тип: **[ **D3DXCOLOR**](d3dxcolor.md)**

Цвет заземления.

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

Интерполяция выполняется линейно между двумя точками, а не за поверхностью сферы (т. е. Если ось имеет значение (0, 0, 1), линейная — Z, а не в азимусал углом). Результирующая функция сферического освещения нормализована таким образом, что точка на идеально рассеянной поверхности без тени и обычной, направленной в направлении *пдир* , приведет к выходу радианце со значением 1 (если верхний цвет был белым и нижний цвет был черным). Это очень простая модель, где *Top* представляет интенсивность "небесной" и *нижней части* представляет интенсивность "заземления".

В сфере с радиусом единицы, как показано на следующем рисунке, направление может быть задано просто с помощью тета, угла относительно оси z в [правильном направлении](coordinate-systems.md), а значение фи — от z.

![Иллюстрация сферы с радиусом единицы](images/spherical-coordinates.png)

В следующих уравнениях показана связь между координатами декартовы (x, y, z) и сферами (тета, фи) в единичной сфере. Угол тета зависит от диапазона от 0 до 2 Пи, а значение фи отличается от 0 до PI.

![формулы связи между декартовы и сферыми координатами](images/spherical-coordinates-equations.png)

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[Математические функции](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[Предварительно вычисленный перенос Радианце (Direct3D 9)](precomputed-radiance-transfer.md)
</dt> </dl>

 

 

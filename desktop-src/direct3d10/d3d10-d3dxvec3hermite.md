---
description: Функция D3DXVec3Hermite (D3DX10Math. h) — выполняет интерполяцию Хермите сплайна, используя указанные трехмерные векторы.
ms.assetid: d2212299-0478-48a6-b303-60c212528058
title: Функция D3DXVec3Hermite (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Hermite
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 955843e7171aaa64e5fa7027b0e0f6049613e31c2d3c647fd705623456ac4e56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990624"
---
# <a name="d3dxvec3hermite-function-d3dx10mathh"></a>Функция D3DXVec3Hermite (D3DX10Math. h)

Выполняет интерполяцию Хермите сплайна, используя указанные трехмерные векторы.

## <a name="syntax"></a>Синтаксис


```C++
D3DXVECTOR3* D3DXVec3Hermite(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pT1,
  _In_    const D3DXVECTOR3 *pV2,
  _In_    const D3DXVECTOR3 *pT2,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тоска* \[ в, out\]
</dt> <dd>

Тип: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Указатель на [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , который является результатом операции.

</dd> <dt>

*pV1* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Указатель на исходную структуру D3DXVECTOR3, вектор позиции.

</dd> <dt>

*pT1* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Указатель на исходную структуру D3DXVECTOR3 — вектор касательной.

</dd> <dt>

*pV2* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Указатель на исходную структуру D3DXVECTOR3, вектор позиции.

</dd> <dt>

*PT2* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Указатель на исходную структуру D3DXVECTOR3 — вектор касательной.

</dd> <dt>

*s* \[ в\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Весовой коэффициент. См. заметки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Указатель на структуру D3DXVECTOR3, которая является результатом интерполяции Хермите сплайна.

## <a name="remarks"></a>Remarks

Функция **D3DXVec3Hermite** выполняет интерполяцию от (позиционирован, тангенс) к (Поситионб, танжентб) с помощью интерполяции хермите сплайна.

Интерполяция сплайна — это обобщение простого и упрощенного сплайна. Пандус — это функция Q (s) со следующими свойствами.

Q (s) = AS ³ + BS ² + CS + D (и, следовательно, Q "(s) = 3As ² + 2Bs + C)

a) Q (0) = v1, т. е. Q ' (0) = T1

б) Q (1) = v2, so Q ' (1) = T2

v1 — это содержимое pV1, v2 в содержимом pV2, T1 — это содержимое pT1, а T2 — содержимое pT2.

Эти свойства используются для решения для A, B, C, D.


```
D = v1  (from a)
C = t1  (from a)
3A + 2B = t2 - t1 (substituting for C)
A + B = v2 - v1 - t1 (substituting for C and D)
```



Подключайте решения для A, B, C и D, чтобы создать Q (ы).


```
A = 2v1 - 2v2 + t2 + t1 
B = 3v2 - 3v1 - 2t1 - t2
C = t1 
D = v1
```



Мы получаем такой результат:

Q (s) = (2V1-2v2 + T2 + T1) s ³ + (3V2-3v1-2T1-T2) s ² + t1s + v1

Который можно изменить следующим образом:

Q (s) = (2S ³-3S ² + 1) v1 + (-2S ³ + 3S ²) v2 + (s ³-2S ² + s) T1 + (s ³-s ²) T2

Хермитеные сплайны полезны для управления анимацией, так как кривая выполняется через все контрольные точки. Кроме того, поскольку позиция и тангенс явно указываются на концах каждого сегмента, можно легко создать непрерывную кривую C2, пока вы убедитесь, что начальная позиция и тангенс соответствуют конечным значениям последнего сегмента.

Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска. Таким образом, функция **D3DXVec3Hermite** может использоваться в качестве параметра для другой функции.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3DX10Math. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Математические функции](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 

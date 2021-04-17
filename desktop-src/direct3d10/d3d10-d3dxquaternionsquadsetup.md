---
description: Настраивает контрольные точки для сферической куадрангле интерполяции.
ms.assetid: c66227bd-8cc1-4173-9dc2-5aab9d57301e
title: Функция D3DXQuaternionSquadSetup (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionSquadSetup
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4a0683bce3642b0300e68be348d8aed39b3c333d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703933"
---
# <a name="d3dxquaternionsquadsetup-function-d3dx10mathh"></a>Функция D3DXQuaternionSquadSetup (D3DX10Math. h)

Настраивает контрольные точки для сферической куадрангле интерполяции.

## <a name="syntax"></a>Синтаксис


```C++
void D3DXQuaternionSquadSetup(
  _In_       D3DXQUATERNION *pAOut,
  _In_       D3DXQUATERNION *pBOut,
  _In_       D3DXQUATERNION *pCOut,
  _In_ const D3DXQUATERNION *pQ0,
  _In_ const D3DXQUATERNION *pQ1,
  _In_ const D3DXQUATERNION *pQ2,
  _In_ const D3DXQUATERNION *pQ3
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пааут* \[ окне\]
</dt> <dd>

Тип: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Указатель на Ааут.

</dd> <dt>

*пбаут* \[ окне\]
</dt> <dd>

Тип: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Указатель на грамме.

</dd> <dt>

*пкаут* \[ окне\]
</dt> <dd>

Тип: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Указатель на COut.

</dd> <dt>

*pQ0* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Указатель на входную точку управления Q0.

</dd> <dt>

*pQ1* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Указатель на точку управления ввода, Q1.

</dd> <dt>

*pQ2* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Указатель на точку управления ввода, Q2.

</dd> <dt>

*pQ3* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Указатель на точку управления ввода, Q3.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет.

## <a name="remarks"></a>Remarks

Эта функция принимает четыре контрольные точки, которые предоставляются входным данным pQ0, pQ1, pQ2 и pQ3. Затем функция изменяет эти значения, чтобы найти кривую, которая проходит вдоль кратчайшего пути. Значения Q0, Q2 и Q3 рассчитываются, как показано ниже.


```
q0 = |Q0 + Q1| < |Q0 - Q1| ? -Q0 : Q0
q2 = |Q1 + Q2| < |Q1 - Q2| ? -Q2 : Q2
q3 = |Q2 + Q3| < |Q2 - Q3| ? -Q3 : Q3
```



После вычисления новых значений Q значения для Ааут, грамме и COut рассчитываются следующим образом:

Ааут = Q1 \* e<sup> \[ -0,25 \ \* (\ LN \[ exp (Q1) \* Q2 \] \ + \ LN \[ exp (Q1) \* Q0 \] \) \ \] </sup>

Грамме = Q2 \* e<sup> \[ -0,25 \ \* (\ LN \[ exp (Q2) \* Q3 \] \ + \ LN \[ exp (Q2) \* Q1 \] \) \ \] </sup>

COut = Q2

> [!Note]  
> LN — это метод API [**D3DXQuaternionLn**](d3d10-d3dxquaternionln.md) , а exp — метод API [**D3DXQuaternionExp**](d3d10-d3dxquaternionexp.md).

 

Используйте [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) для любых входных данных кватернион, которые еще не нормализованы.

### <a name="examples"></a>Примеры

В следующем примере показано, как использовать набор ключей кватернион (q0, Q1, Q2, Q3) для расчета внутренних точек куадрангле (A, B, C). Это гарантирует непрерывность касательных между смежными сегментами.


```
      A     B
Q0    Q1    Q2    Q3
```



В следующем примере кода показано, как можно выполнить интерполяцию между Q1 и Q2.


```
// Rotation about the z-axis
D3DXQUATERNION Q0 = D3DXQUATERNION(0,  0, 0.707f, -.707f);
D3DXQUATERNION Q1 = D3DXQUATERNION(0,  0, 0.000f, 1.000f);
D3DXQUATERNION Q2 = D3DXQUATERNION(0,  0, 0.707f, 0.707f);
D3DXQUATERNION Q3 = D3DXQUATERNION(0,  0, 1.000f, 0.000f);
D3DXQUATERNION A, B, C, Qt;
FLOAT time = 0.5f;

D3DXQuaternionSquadSetup(&A, &B, &C, &Q0, &Q1, &Q2, &Q3);
D3DXQuaternionSquad(&Qt, &Q1, &A, &B, &C, time);
```



> [!Note]
>
> -   C — это +/-Q2 в зависимости от результата функции.
> -   Qt является результатом функции.
>
> Результатом является поворот на 45 градусов вокруг оси z для времени = 0,5.

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Математические функции](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 

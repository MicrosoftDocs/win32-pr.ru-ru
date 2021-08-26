---
title: функция DST
description: Вычисляет вектор расстояний. | функция DST
ms.assetid: 24d22743-5867-49db-8d0a-55cc3625c947
keywords:
- функция DST HLSL
topic_type:
- apiref
api_name:
- dst
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d8b0d8112902486102e6a4338445a2526b23cab8dafb2ea8b7d68b87d5b803af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068344"
---
# <a name="dst-function"></a>функция DST

Вычисляет вектор расстояний.

## <a name="syntax"></a>Синтаксис

``` syntax
fVector dst(
  in fVector src0,
  in fVector src1
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*src0* \[ окне\]
</dt> <dd>

Тип: **[фвектор](dx-graphics-hlsl-vector.md)**

Первый вектор.

</dd> <dt>

*src1* \[ окне\]
</dt> <dd>

Тип: **[фвектор](dx-graphics-hlsl-vector.md)**

Второй вектор.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[фвектор](dx-graphics-hlsl-vector.md)**

Вычисленный вектор расстояний.

## <a name="remarks"></a>Remarks

Эта встроенная функция предоставляет те же функциональные возможности, что и время [летнего времени](dst---vs.md)для инструкции шейдера вершин.

## <a name="see-also"></a>См. также

<dl> <dt>

[Встроенные функции](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 





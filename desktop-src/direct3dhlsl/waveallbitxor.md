---
title: Функция Вавеактивебитксор
description: Возвращает побитовое ИСКЛЮЧАЮЩее число всех значений выражения для всех активных дорожек в текущей волновой передаче и реплицирует его обратно во все активные дорожки.
ms.assetid: A6807D17-1E6E-4997-AB52-32FAB5857219
keywords:
- Функция Вавеактивебитксор HLSL
topic_type:
- apiref
api_name:
- WaveActiveBitXor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 733ab8c40a59b784af8a7d50c4f8e1e543f344ee2d75ed9b6896992e6176ff18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118504884"
---
# <a name="waveactivebitxor-function"></a>Функция Вавеактивебитксор

Возвращает побитовое ИСКЛЮЧАЮЩее число всех значений выражения для всех активных дорожек в текущей волновой передаче и реплицирует его обратно во все активные дорожки.

## <a name="syntax"></a>Синтаксис

``` syntax
<int_type> WaveActiveBitXor(
   <int_type> expr
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*expr* 
</dt> <dd>

Выражение для вычисления.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Побитовое значение XOR.

## <a name="remarks"></a>Remarks

Эта функция поддерживается из модели шейдеров 6,0 на всех стадиях шейдера. 



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Общие сведения о модели шейдеров 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Модель шейдеров 6](shader-model-6-0.md)
</dt> </dl>

 

 





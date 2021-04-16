---
title: Функция Вавеактивемакс
description: Возвращает максимальное значение выражения для всех активных дорожек в текущей волновой передаче и реплицирует его обратно во все активные дорожки.
ms.assetid: 19101C56-2618-4F34-8725-DF92198ABDA4
keywords:
- Функция Вавеактивемакс HLSL
topic_type:
- apiref
api_name:
- WaveActiveMax
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7c0fd10f578d598c326cdfb4cf943d3a35fe78a9
ms.sourcegitcommit: a232805e6c618673f2df904111cc4f5a33e15504
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/07/2020
ms.locfileid: "104414260"
---
# <a name="waveactivemax-function"></a>Функция Вавеактивемакс

Возвращает максимальное значение выражения для всех активных дорожек в текущей волновой передаче и реплицирует его обратно во все активные дорожки.

## <a name="syntax"></a>Синтаксис

``` syntax
<type> WaveActiveMax(
   <type> expr
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*expr* 
</dt> <dd>

Выражение для вычисления.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Максимальное значение.

## <a name="remarks"></a>Примечания

Порядок операций не определен.

Эта функция поддерживается из модели шейдеров 6,0 на всех стадиях шейдера. 



 

## <a name="examples"></a>Примеры

``` syntax
 float3 maxPos = WaveActiveMax( myPoint.position );
    BoundingBox.max = max( maxPos, BoundingBox.max );
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Общие сведения о модели шейдеров 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Модель шейдеров 6](shader-model-6-0.md)
</dt> </dl>

 

 





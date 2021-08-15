---
title: Функция Вавеактивемин
description: Возвращает минимальное значение выражения для всех активных желобов в текущем звуковом процессе реплицирует его обратно во все активные дорожки.
ms.assetid: BA762C02-894C-4AF9-A226-C1E3AAC286FF
keywords:
- Функция Вавеактивемин HLSL
topic_type:
- apiref
api_name:
- WaveActiveMin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b97f2e58449e8b33270318f305a6fee87662a6aac4643b35152024366bf8b08b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117721791"
---
# <a name="waveactivemin-function"></a>Функция Вавеактивемин

Возвращает минимальное значение выражения для всех активных желобов в текущем звуковом процессе реплицирует его обратно во все активные дорожки.

## <a name="syntax"></a>Синтаксис

``` syntax
<type> WaveActiveMin(
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

Минимальное значение.

## <a name="remarks"></a>Remarks

Порядок операций не определен.

Эта функция поддерживается из модели шейдеров 6,0 на всех стадиях шейдера. 



 

## <a name="examples"></a>Примеры

``` syntax
 float3 minPos = WaveActiveMin( myPoint.position );
    BoundingBox.min = min( minPos, BoundingBox.min );
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Общие сведения о модели шейдеров 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Модель шейдеров 6](shader-model-6-0.md)
</dt> </dl>

 

 





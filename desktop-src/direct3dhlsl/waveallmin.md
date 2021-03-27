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
ms.openlocfilehash: 91555df354ab2b7ffc447a9422c4811ae23e6e0c
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104070854"
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

## <a name="remarks"></a>Примечания

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

 

 





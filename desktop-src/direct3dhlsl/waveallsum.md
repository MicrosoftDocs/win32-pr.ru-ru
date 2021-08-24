---
title: Функция Вавеактивесум
description: Суммирует значение выражения по всем активным желобам в текущей волновой записи и реплицирует его во все дорожки в текущей волн.
ms.assetid: 94CEF4AA-D6DE-4B00-9743-F491F255FE3D
keywords:
- Функция Вавеактивесум HLSL
topic_type:
- apiref
api_name:
- WaveActiveSum
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 403768b875ed9462b79fb5d0abeee9539189597591f3a3b20f5a3b9662995542
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119742264"
---
# <a name="waveactivesum-function"></a>Функция Вавеактивесум

Суммирует значение выражения по всем активным желобам в текущей волновой записи и реплицирует его во все дорожки в текущей волн.

## <a name="syntax"></a>Синтаксис

``` syntax
<type> WaveActiveSum(
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

Значение Sum.

## <a name="remarks"></a>Remarks

Порядок операций не определен.

Эта функция поддерживается из модели шейдеров 6,0 на всех стадиях шейдера. 



 

## <a name="examples"></a>Примеры

``` syntax
float3 total = WaveActiveSum( position ); // sum positions in wave
float3 center = total/count;           // compute average of these positions
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Общие сведения о модели шейдеров 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Модель шейдеров 6](shader-model-6-0.md)
</dt> </dl>

 

 





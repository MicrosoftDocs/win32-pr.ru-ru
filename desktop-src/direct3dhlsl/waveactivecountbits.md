---
title: Функция Вавеактивекаунтбитс
description: Подсчитывает количество логических переменных, которые имеют значение true во всех активных желобах в текущей волновой области, и реплицирует результат во все желобы в волне.
ms.assetid: 053E100C-7E09-4F9D-9F38-9D5E208A38CE
keywords:
- Функция Вавеактивекаунтбитс HLSL
topic_type:
- apiref
api_name:
- WaveActiveCountBits
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4e1642cbd5cbdef162511185e9d2c05e849d78486b82e8219623286f33e39223
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118504939"
---
# <a name="waveactivecountbits-function"></a>Функция Вавеактивекаунтбитс

Подсчитывает количество логических переменных, которые имеют значение true во всех активных желобах в текущей волновой области, и реплицирует результат во все желобы в волне.

## <a name="syntax"></a>Синтаксис


``` syntax
uint WaveActiveCountBits(
   bool bBit
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ббит* 
</dt> <dd>

Логические переменные для вычисления. Предоставление явного логического значения true Возвращает число активных дорожек.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Число, которое вычисляется на значение true во всех активных желобах в текущей волны.

## <a name="remarks"></a>Remarks

Эта функция поддерживается из модели шейдеров 6,0 на всех стадиях шейдера. 



 

## <a name="examples"></a>Примеры

Это может быть реализовано более эффективно, чем полное Вавеактивесум, как описано в следующем примере:

``` syntax
result = WaveActiveCountBits( WaveActiveBallot( bBit ) );
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Общие сведения о модели шейдеров 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Модель шейдеров 6](shader-model-6-0.md)
</dt> </dl>

 

 





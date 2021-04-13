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
ms.openlocfilehash: 4c4d2db55e9e3a0ad8f0a66be183d6e39d2a8b9c
ms.sourcegitcommit: a232805e6c618673f2df904111cc4f5a33e15504
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/07/2020
ms.locfileid: "104339781"
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

## <a name="remarks"></a>Примечания

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

 

 





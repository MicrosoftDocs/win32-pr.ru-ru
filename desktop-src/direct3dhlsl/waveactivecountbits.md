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
ms.openlocfilehash: a53a2953ba7d77f1969a7d5dabef3c17437e8bbb
ms.sourcegitcommit: 8d7ce0c4827f8a4fd501cc6487f1a8360e944577
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/24/2021
ms.locfileid: "122767608"
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

Число дорожек, для которых логическая переменная принимает значение true, во всех активных желобах в текущем волне.

## <a name="remarks"></a>Remarks

Эта функция поддерживается из модели шейдеров 6,0 на всех стадиях шейдера. 



 

## <a name="examples"></a>Примеры

Это может быть реализовано более эффективно, чем полное Вавеактивесум, как описано в следующем примере:

``` syntax
result = WaveActiveCountBits( WaveActiveBallot( bBit ) );
```

## <a name="see-also"></a>См. также

<dl> <dt>

[Общие сведения о модели шейдеров 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Модель шейдеров 6](shader-model-6-0.md)
</dt> </dl>

 

 





---
title: Функция Вавеактивеанитруе
description: Возвращает значение true, если выражение имеет значение true в любом из активных желобов в текущей волны.
ms.assetid: 203E2E1D-0AA2-4E4A-80F7-D1FE7579A742
keywords:
- Функция Вавеактивеанитруе HLSL
topic_type:
- apiref
api_name:
- WaveActiveAnyTrue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2c49c9727461d316d7d2c9d8f048971384e568476d1ca693aeec49cdf14a4795
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117721734"
---
# <a name="waveactiveanytrue-function"></a>Функция Вавеактивеанитруе

Возвращает значение true, если выражение имеет значение true в любом из активных желобов в текущей волны.

## <a name="syntax"></a>Синтаксис

``` syntax
bool WaveActiveAnyTrue(
   bool expr
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*expr* 
</dt> <dd>

Логическое выражение для вычисления.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Значение true, если выражение имеет значение true в любой полосе.

## <a name="remarks"></a>Remarks

Эта функция поддерживается из модели шейдеров 6,0 на всех стадиях шейдера. 



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Общие сведения о модели шейдеров 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Модель шейдеров 6](shader-model-6-0.md)
</dt> </dl>

 

 





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
ms.openlocfilehash: 16801c4329f5bc0bf325d8bb67e8c0bb94887678
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104997174"
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

## <a name="remarks"></a>Примечания

Эта функция поддерживается из модели шейдеров 6,0 на всех стадиях шейдера. 



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Общие сведения о модели шейдеров 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Модель шейдеров 6](shader-model-6-0.md)
</dt> </dl>

 

 





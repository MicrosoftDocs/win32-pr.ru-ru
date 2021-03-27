---
title: Функция Вавеактивепродукт
description: Умножает значения выражения на все активные дорожки в текущей волне и реплицирует их обратно во все активные дорожки.
ms.assetid: B259244D-C993-4F4A-AF09-F077D99AD025
keywords:
- Функция Вавеактивепродукт HLSL
topic_type:
- apiref
api_name:
- WaveActiveProduct
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b8e1d400541a2654657c1a462c38494d20af13e6
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "103891236"
---
# <a name="waveactiveproduct-function"></a>Функция Вавеактивепродукт

Умножает значения выражения на все активные дорожки в текущей волне и реплицирует их обратно во все активные дорожки.

## <a name="syntax"></a>Синтаксис

``` syntax
<type> WaveActiveProduct(
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

Значение продукта.

## <a name="remarks"></a>Примечания

Порядок операций не определен.

Эта функция поддерживается из модели шейдеров 6,0 на всех стадиях шейдера. 



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Общие сведения о модели шейдеров 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Модель шейдеров 6](shader-model-6-0.md)
</dt> </dl>

 

 





---
title: Функция Вавеактивеаллекуал
description: Возвращает значение true, если выражение одинаково для каждой активной полосы в текущем звуковом поле (и, таким образом, единообразно в нем).
ms.assetid: E0A051A8-0ADD-4EC7-8D9A-8820CED9DA9D
keywords:
- Функция Вавеактивеаллекуал HLSL
topic_type:
- apiref
api_name:
- WaveActiveAllEqual
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f62493a1bf08b85e95acad319bac2d022c30a53d43c28a87d0f5f603e78d300f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118786114"
---
# <a name="waveactiveallequal-function"></a>Функция Вавеактивеаллекуал

Возвращает значение true, если выражение одинаково для каждой активной полосы в текущем звуковом поле (и, таким образом, единообразно в нем).

## <a name="syntax"></a>Синтаксис


``` syntax
bool WaveActiveAllEqual(
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

Значение true, если выражение одинаково для каждой активной полосы в текущем волна.

## <a name="remarks"></a>Remarks

Эта функция поддерживается из модели шейдеров 6,0 на всех стадиях шейдера. 



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Общие сведения о модели шейдеров 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Модель шейдеров 6](shader-model-6-0.md)
</dt> </dl>

 

 





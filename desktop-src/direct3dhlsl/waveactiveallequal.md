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
ms.openlocfilehash: 34745e428fcd4453ce7274fc2a5accc6185f5b10
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "103797250"
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

## <a name="remarks"></a>Примечания

Эта функция поддерживается из модели шейдеров 6,0 на всех стадиях шейдера. 



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Общие сведения о модели шейдеров 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Модель шейдеров 6](shader-model-6-0.md)
</dt> </dl>

 

 





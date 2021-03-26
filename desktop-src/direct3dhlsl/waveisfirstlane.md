---
title: Функция Вавеисфирстлане
description: Возвращает значение true только для активной полосы в текущем волне с наименьшим индексом.
ms.assetid: 5D90F713-08C7-4BD4-867B-2E7CA3A85E87
keywords:
- Функция Вавеисфирстлане HLSL
topic_type:
- apiref
api_name:
- WaveIsFirstLane
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 49e875463d8281ff7e7699694c02d087df1a372f
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104339661"
---
# <a name="waveisfirstlane-function"></a>Функция Вавеисфирстлане

Возвращает значение true только для активной полосы в текущем волне с наименьшим индексом.

## <a name="syntax"></a>Синтаксис


``` syntax
bool WaveIsFirstLane(void);
```



## <a name="parameters"></a>Параметры

У этой функции нет параметров.

## <a name="return-value"></a>Возвращаемое значение

Значение true только для активной полосы в текущей волны с наименьшим индексом.

## <a name="remarks"></a>Примечания

Эта функция может использоваться для определения операций, выполняемых только один раз для каждой волны.

Эта функция поддерживается из модели шейдеров 6,0 на всех стадиях шейдера. 



 

## <a name="examples"></a>Примеры

``` syntax
 if ( WaveIsFirstLane() )
{
    . . . // once per-wave code
}
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Общие сведения о модели шейдеров 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Модель шейдеров 6](shader-model-6-0.md)
</dt> </dl>

 

 





---
title: Функция Вавежетланекаунт
description: Возвращает количество желобов в волне на этой архитектуре.
ms.assetid: 04059B5E-0F62-4623-84AD-E41FF7166B34
keywords:
- Функция Вавежетланекаунт HLSL
topic_type:
- apiref
api_name:
- WaveGetLaneCount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6a177e50ee3c4c9c715ea109faaed72c24e174e4e942059a4dee0dcd0de91a9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118504742"
---
# <a name="wavegetlanecount-function"></a>Функция Вавежетланекаунт

Возвращает количество желобов в волне на этой архитектуре.

## <a name="syntax"></a>Синтаксис

``` syntax
uint WaveGetLaneCount(void);
```

## <a name="parameters"></a>Параметры

У этой функции нет параметров.

## <a name="return-value"></a>Возвращаемое значение

Результат будет составлять от 4 до 128 и включает все волны: активные, неактивные и (или) вспомогательные желобы. Результат, возвращаемый этой функцией, может значительно различаться в зависимости от реализации драйвера.

## <a name="remarks"></a>Remarks

Эта функция поддерживается из модели шейдеров 6,0 на всех стадиях шейдера. 



 

## <a name="examples"></a>Примеры

``` syntax
 uint laneCount = WaveGetLaneCount();    // number of lanes in wave
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Общие сведения о модели шейдеров 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Модель шейдеров 6](shader-model-6-0.md)
</dt> </dl>

 

 





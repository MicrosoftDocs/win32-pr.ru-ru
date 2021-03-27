---
title: Функция Вавежетланеиндекс
description: Возвращает индекс текущей полосы в пределах текущей волны.
ms.assetid: C05BD814-23DF-432F-8669-C03842B77AC7
keywords:
- Функция Вавежетланеиндекс HLSL
topic_type:
- apiref
api_name:
- WaveGetLaneIndex
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8adea1091739981523ab19b69158ead9aafa600c
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104997175"
---
# <a name="wavegetlaneindex-function"></a>Функция Вавежетланеиндекс

Возвращает индекс текущей полосы в пределах текущей волны.

## <a name="syntax"></a>Синтаксис

``` syntax
uint WaveGetLaneIndex(void);
```

## <a name="parameters"></a>Параметры

У этой функции нет параметров.

## <a name="return-value"></a>Возвращаемое значение

Текущий индекс полосы. Результат будет находиться в диапазоне от 0 до результата, возвращенного из [**вавежетланекаунт**](wavegetlanecount.md).

## <a name="remarks"></a>Примечания

Эта функция поддерживается из модели шейдеров 6,0 на всех стадиях шейдера. 



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Общие сведения о модели шейдеров 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Модель шейдеров 6](shader-model-6-0.md)
</dt> </dl>

 

 





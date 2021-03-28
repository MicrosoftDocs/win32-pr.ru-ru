---
title: Функция Вавереадланеат
description: Возвращает значение выражения для заданного индекса полосы в заданной волны.
ms.assetid: CA9467D9-8885-4A5D-87F3-5BA40AE78993
keywords:
- Функция Вавереадланеат HLSL
topic_type:
- apiref
api_name:
- WaveReadLaneAt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e40940f2df6685a3096da6886ad3bcb6d9ca99af
ms.sourcegitcommit: 4423a9d48f1c90d2ec2eca68e9cae30df1787f25
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/25/2020
ms.locfileid: "104412748"
---
# <a name="wavereadlaneat-function"></a>Функция Вавереадланеат

Возвращает значение выражения для заданного индекса полосы в заданной волны.

## <a name="syntax"></a>Синтаксис

``` syntax
<type> WaveReadLaneAt(
   <type> expr,
   uint laneIndex
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*expr* 
</dt> <dd>

Выражение для вычисления.

</dd> <dt>

*ланеиндекс* 
</dt> <dd>

Индекс полосы, для которой будет возвращен результат *expr* .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Полученное значение является результатом *выражения expr*. Он будет единообразным, если *ланеиндекс* является однородным.

## <a name="remarks"></a>Примечания

Эта функция фактически является широковещательной рассылкой значения в Ланеиндекс'с Lane.

Эта функция поддерживается из модели шейдеров 6,0 в следующих типах шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Вычисления |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Общие сведения о модели шейдеров 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Модель шейдеров 6](shader-model-6-0.md)
</dt> </dl>

 

 





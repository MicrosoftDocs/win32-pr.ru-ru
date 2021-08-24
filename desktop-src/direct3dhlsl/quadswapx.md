---
title: Функция Куадреадакросскс
description: Возвращает указанное локальное значение, считанное из другой полосы в данном Quad по оси X.
ms.assetid: 7A7E0623-30EC-4167-90A5-D79E10A394CC
keywords:
- Функция Куадреадакросскс HLSL
topic_type:
- apiref
api_name:
- QuadReadAcrossX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 86a2f525a79fa2458e4f7e0ef44379053e03128782d2625e1bdceb23ec518b16
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119672444"
---
# <a name="quadreadacrossx-function"></a>Функция Куадреадакросскс

Возвращает указанное локальное значение, считанное из другой полосы в данном Quad по оси X.

## <a name="syntax"></a>Синтаксис

``` syntax
<type> QuadReadAcrossX(
   <type> localValue
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*локалвалуе* 
</dt> <dd>

Запрошенный тип.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Указанное локальное значение. Если исходная полоса неактивна, результаты будут неопределенными.

## <a name="remarks"></a>Remarks

Дополнительные сведения об четырехъядерях см. в разделе [Общие сведения о модели шейдеров 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).

Эта функция поддерживается из модели шейдеров 6,0 только в пиксельных шейдерах и.



 

## <a name="see-also"></a>См. также

<dl> <dt>

[Модель шейдеров 6](shader-model-6-0.md)
</dt> </dl>

 

 





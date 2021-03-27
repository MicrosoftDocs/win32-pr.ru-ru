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
ms.openlocfilehash: cd41b0bd84861d23153f02ba6328d17b70287866
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104134787"
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

## <a name="remarks"></a>Примечания

Дополнительные сведения об четырехъядерях см. в разделе [Общие сведения о модели шейдеров 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).

Эта функция поддерживается из модели шейдеров 6,0 только в пиксельных шейдерах и.



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Модель шейдеров 6](shader-model-6-0.md)
</dt> </dl>

 

 





---
title: Функция Куадреадакросси
description: Возвращает указанное исходное значение, считанное из другой полосы в данном Quad по оси Y.
ms.assetid: 6C03D1E6-433F-4CCA-A5EA-C3F34BB2B93B
keywords:
- Функция Куадреадакросси HLSL
topic_type:
- apiref
api_name:
- QuadReadAcrossY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 72b5ede0df733e60ba4b1bcc01a04f1daaedc708
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104984100"
---
# <a name="quadreadacrossy-function"></a>Функция Куадреадакросси

Возвращает указанное исходное значение, считанное из другой полосы в данном Quad по оси Y.

## <a name="syntax"></a>Синтаксис

``` syntax
<type> QuadReadAcrossY(
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

Указанное исходное значение. Если исходная полоса неактивна, результаты будут неопределенными.

## <a name="remarks"></a>Примечания

Дополнительные сведения об четырехъядерях см. в разделе [Общие сведения о модели шейдеров 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).

Эта функция поддерживается из модели шейдеров 6,0 только в пиксельных шейдерах и.



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Модель шейдеров 6](shader-model-6-0.md)
</dt> </dl>

 

 





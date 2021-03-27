---
title: Функция Куадреадланеат
description: Возвращает указанное исходное значение из полосы, определяемой ИДЕНТИФИКАТОРом полосы в текущем объекте Quad.
ms.assetid: 5CD7EE4C-E64E-46A3-ABDC-1BF65D0F96BE
keywords:
- Функция Куадреадланеат HLSL
topic_type:
- apiref
api_name:
- QuadReadLaneAt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ddc772c2dca66873891483431eab14ad504da77e
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104488535"
---
# <a name="quadreadlaneat-function"></a>Функция Куадреадланеат

Возвращает указанное исходное значение из полосы, определяемой ИДЕНТИФИКАТОРом полосы в текущем объекте Quad.

## <a name="syntax"></a>Синтаксис


``` syntax
<type> QuadReadLaneAt(
   <type> sourceValue,
   uint   quadLaneID  
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*саурцевалуе* 
</dt> <dd>

Запрошенный тип.

</dd> <dt>

*куадланеид* 
</dt> <dd>

Идентификатор полосы; оно будет иметь значение от 0 до 3.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Указанное исходное значение. Результат этой функции является единообразным по отношению к четырем. Если исходная полоса неактивна, результаты будут неопределенными.

## <a name="remarks"></a>Примечания

Дополнительные сведения об четырехъядерях см. в разделе [Общие сведения о модели шейдеров 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).

Эта функция поддерживается из модели шейдеров 6,0 только в пиксельных шейдерах и.



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Модель шейдеров 6](shader-model-6-0.md)
</dt> </dl>

 

 





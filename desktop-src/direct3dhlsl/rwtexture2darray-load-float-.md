---
title: 'Функция RWTexture2DArray:: Load (int)'
description: 'Считывает данные текстуры. | Функция RWTexture2DArray:: Load (int)'
ms.assetid: BC247B2A-1744-4E37-A501-22E4A592A32D
keywords:
- Загрузить функцию HLSL
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7459e0bfacda9075fd587be69f8a3d69adbefb855608e5f949e250d0e35de786
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118790840"
---
# <a name="rwtexture2darrayloadint-function"></a>Функция RWTexture2DArray:: Load (int)

Считывает данные текстуры.

## <a name="syntax"></a>Синтаксис


``` syntax
 Load(
  in int Location
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Расположение* \[ окне\]
</dt> <dd>

Тип: **int**

Расположение текстуры.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип:

Возвращаемый тип соответствует типу в объявлении для объекта [**RWTexture2DArray**](sm5-object-rwtexture2darray.md) .

## <a name="remarks"></a>Remarks

Эта функция поддерживается для следующих типов шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Службы вычислений |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Методы Load](rwtexture2darray-load.md)
</dt> </dl>

 

 





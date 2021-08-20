---
title: 'Функция RWTexture3D:: Load (int)'
description: 'Считывает данные текстуры. | Функция RWTexture3D:: Load (int)'
ms.assetid: 93C4FFFF-8695-4BAF-BAE4-A2704332E6A9
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
ms.openlocfilehash: d233559739e86a1cf5a8cbdc9af18ea6c12550c5f6118d63b5382689cd80bba2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119671894"
---
# <a name="rwtexture3dloadint-function"></a>Функция RWTexture3D:: Load (int)

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

Возвращаемый тип соответствует типу в объявлении для объекта [**RWTexture3D**](sm5-object-rwtexture3d.md) .

## <a name="remarks"></a>Remarks

Эта функция поддерживается для следующих типов шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Вычисления |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>См. также

<dl> <dt>

[Методы Load](rwtexture3d-load.md)
</dt> </dl>

 

 





---
title: 'Функция Рвструктуредбуффер:: Load (int)'
description: 'Считывает данные буфера. | Функция Рвструктуредбуффер:: Load (int)'
ms.assetid: 9CB40579-6BF8-468C-81B8-936D9940458E
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
ms.openlocfilehash: e3cc8fbd0cfa18f2ac6c5d7109e8690d829bbde2175e8808865e68e29e63c955
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067764"
---
# <a name="rwstructuredbufferloadint-function"></a>Функция Рвструктуредбуффер:: Load (int)

Считывает данные буфера.

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

Расположение буфера.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип:

Возвращаемый тип соответствует типу в объявлении для объекта [**рвструктуредбуффер**](sm5-object-rwstructuredbuffer.md) .

## <a name="remarks"></a>Remarks

Эта функция поддерживается для следующих типов шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Вычисления |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>См. также

<dl> <dt>

[Методы Load](rwstructuredbuffer-load.md)
</dt> </dl>

 

 





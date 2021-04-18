---
title: 'Функция Структуредбуффер:: Load (int)'
description: 'Считывает данные буфера. | Функция Структуредбуффер:: Load (int)'
ms.assetid: ef08d360-0494-49f7-9481-cb802e14aeee
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
ms.openlocfilehash: 883d483044a27e35848457e70e22888dd5ad6320
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986609"
---
# <a name="structuredbufferloadint-function"></a>Функция Структуредбуффер:: Load (int)

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

Возвращаемый тип соответствует типу в объявлении для объекта [**структуредбуффер**](sm5-object-structuredbuffer.md) .

## <a name="remarks"></a>Примечания

Эта функция поддерживается для следующих типов шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Вычисления |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Методы Load](structuredbuffer-load.md)
</dt> </dl>

 

 





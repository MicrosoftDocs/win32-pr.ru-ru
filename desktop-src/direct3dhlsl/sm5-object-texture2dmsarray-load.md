---
title: 'Функция Texture2DMSArray:: Load (int, int)'
description: 'Возвращает одно значение. | Функция Texture2DMSArray:: Load (int, int)'
ms.assetid: 955135cf-1bac-4d0c-9870-2b6d59d9dd88
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
ms.openlocfilehash: 83da1a2af6ffc7e990ba1fd4c7f220387304c770
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104000257"
---
# <a name="texture2dmsarrayloadintint-function"></a>Функция Texture2DMSArray:: Load (int, int)

Возвращает одно значение.

## <a name="syntax"></a>Синтаксис

``` syntax
T Load(
  in int3 coord,
  in int sampleindex
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*курд* \[ окне\]
</dt> <dd>

Тип: " **корпус** "

Входное расположение.

</dd> <dt>

*sampleindex* \[ окне\]
</dt> <dd>

Тип: **[ **int**](/windows/desktop/WinProg/windows-data-types)**

Пример индекса.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **T**

Одно значение, тип которого соответствует типу шаблона текстуры.

## <a name="remarks"></a>Примечания

Это список перегруженных версий этого метода.


```
void Load(in int3 coord,
  in int sampleindex,
  in int2 offset);
```



Эта функция поддерживается для следующих типов шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Вычисления |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Методы Load](texture2dmsarray-load.md)
</dt> <dt>

[Модель шейдера 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 

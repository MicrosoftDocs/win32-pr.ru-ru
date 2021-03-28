---
title: 'Функция Texture2DMS:: Load (int, int)'
description: 'Возвращает одно значение. | Функция Texture2DMS:: Load (int, int)'
ms.assetid: b49b94e0-5c49-4901-b49d-3e652d4fd2d1
keywords:
- Загрузить функцию DXGI
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7d9c86bea7d914dd5975105a00a64789864a1fbd
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986456"
---
# <a name="texture2dmsloadintint-function"></a>Функция Texture2DMS:: Load (int, int)

Возвращает одно значение.

## <a name="syntax"></a>Синтаксис

``` syntax
T Load(
  in int2 coord,
  in int sampleindex
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*курд* \[ окне\]
</dt> <dd>

Тип: **int2**

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
void Load(in int2 coord,
  in int sampleindex,
  in int2 offset);
```



Эта функция поддерживается для следующих типов шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Вычисления |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Методы Load](texture2dms-load.md)
</dt> <dt>

[Модель шейдера 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 

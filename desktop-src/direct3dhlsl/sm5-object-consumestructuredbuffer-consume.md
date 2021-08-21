---
title: 'Консуместруктуредбуффер:: использование функции'
description: Удаляет значение из конца буфера.
ms.assetid: b4f7b472-9274-463d-99b0-f05b74f54fc1
keywords:
- Использование функции HLSL
topic_type:
- apiref
api_name:
- Consume
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a76f8c27ed50c7d7eab1b37cd5c60257691b8db5e5af412f5b3bfe678c283bba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119486704"
---
# <a name="consume-function"></a>Использование функции

Удаляет значение из конца буфера.

## <a name="syntax"></a>Синтаксис

``` syntax
T Consume(void);
```

## <a name="parameters"></a>Параметры

У этой функции нет параметров.

## <a name="return-value"></a>Возвращаемое значение

Тип: **T**

Значение удалено (может быть структурой).

## <a name="remarks"></a>Remarks

T может быть любым типом данных, включая структуру.

Эта функция поддерживается для следующих типов шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Вычисления |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>См. также

<dl> <dt>

[консуместруктуредбуффер](sm5-object-consumestructuredbuffer.md)
</dt> <dt>

[Модель шейдера 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 





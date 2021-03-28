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
ms.openlocfilehash: 9d5a43c53089a7e7b19d0f1ecef5c0e5608e8ee9
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2019
ms.locfileid: "104069247"
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

## <a name="remarks"></a>Примечания

T может быть любым типом данных, включая структуру.

Эта функция поддерживается для следующих типов шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Вычисления |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[консуместруктуредбуффер](sm5-object-consumestructuredbuffer.md)
</dt> <dt>

[Модель шейдера 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 





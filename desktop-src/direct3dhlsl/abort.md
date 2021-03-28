---
title: Функция Abort (Корекрт \_ Terminate. h)
description: Отправляет сообщение об ошибке в информационную очередь и завершает текущий выполняемый вызов Draw или Dispatch.
ms.assetid: b8ce153b-0d1c-4294-b88e-b7e50e708ab9
keywords:
- Функция Abort HLSL
topic_type:
- apiref
api_name:
- abort
api_location:
- corecrt_terminate.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9428a03b422aed9ff6fae097459a53369d3a30e1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987266"
---
# <a name="abort-function"></a>Функция abort

Отправляет сообщение об ошибке в информационную очередь и завершает текущий выполняемый вызов Draw или Dispatch.

## <a name="syntax"></a>Синтаксис

``` syntax
void abort(
    
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

 
</dt> <dd>

None

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="remarks"></a>Примечания

Эта операция не выполняет никаких действий на средствах прорисовки, не поддерживающих эту операцию.

### <a name="minimum-shader-model"></a>Минимальная модель шейдера

Эта функция поддерживается в следующих моделях шейдеров.



| Модель шейдера                                                        | Поддерживается |
|---------------------------------------------------------------------|-----------|
| [Shader Model 4 (DirectX HLSL) или более поздней версии.](dx-graphics-hlsl-sm3.md) | да       |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Корекрт \_ Terminate. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Встроенные функции](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 






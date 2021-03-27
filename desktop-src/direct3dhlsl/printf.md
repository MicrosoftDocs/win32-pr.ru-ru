---
title: printf - функция
description: Отправляет настраиваемое сообщение шейдера в информационную очередь.
ms.assetid: 0c6c15fc-1da5-4a26-ade0-5a0489e4f564
keywords:
- Функция printf HLSL
topic_type:
- apiref
api_name:
- printf
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 74492cc613e22f335eace684300f0380e5751a95
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103987014"
---
# <a name="printf-function"></a>printf - функция

Отправляет настраиваемое сообщение шейдера в информационную очередь.

## <a name="syntax"></a>Синтаксис

``` syntax
void printf(
   string format,
    argument ...
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*format* 
</dt> <dd>

Строка формата.

</dd> <dt>

*аргумент...* 
</dt> <dd>

Необязательные аргументы.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="remarks"></a>Примечания

Эта операция не выполняет никаких действий на устройствах, которые ее не поддерживают.

### <a name="minimum-shader-model"></a>Минимальная модель шейдера

Эта функция поддерживается в следующих моделях шейдеров.



| Модель шейдера                                                        | Поддерживается |
|---------------------------------------------------------------------|-----------|
| [Shader Model 4 (DirectX HLSL) или более поздней версии.](dx-graphics-hlsl-sm3.md) | да       |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Встроенные функции](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 





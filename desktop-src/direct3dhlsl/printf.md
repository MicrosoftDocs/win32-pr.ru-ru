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
ms.openlocfilehash: 47131cacef436572f519b394a02b4aaa357a426dd80a192868712cb3d7779e24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119672524"
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

## <a name="remarks"></a>Remarks

Эта операция не выполняет никаких действий на устройствах, которые ее не поддерживают.

### <a name="minimum-shader-model"></a>Минимальная модель шейдера

Эта функция поддерживается в следующих моделях шейдеров.



| Модель шейдера                                                        | Поддерживается |
|---------------------------------------------------------------------|-----------|
| [Shader Model 4 (DirectX HLSL) или более поздней версии.](dx-graphics-hlsl-sm3.md) | Да       |



 

## <a name="see-also"></a>См. также

<dl> <dt>

[Встроенные функции](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 





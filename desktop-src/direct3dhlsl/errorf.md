---
title: Функция еррорф
description: Отправляет сообщение об ошибке в информационную очередь.
ms.assetid: bf4dc6dc-b36e-4b71-ad61-b7a5ba332879
keywords:
- Функция еррорф HLSL
topic_type:
- apiref
api_name:
- errorf
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0651a27419a369721806e9aa4717a20088f8f5fbbaa0063628d2feb69648c7cf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119562684"
---
# <a name="errorf-function"></a>Функция еррорф

Отправляет сообщение об ошибке в информационную очередь.

## <a name="syntax"></a>Синтаксис

``` syntax
void errorf(
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

 

 





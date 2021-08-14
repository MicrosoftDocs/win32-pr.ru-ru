---
title: 'Функция Рвбитеаддрессбуффер:: Интерлоккедмин'
description: Находит минимальное значение, атомарно.
ms.assetid: bf650b2e-9c6c-4458-9565-1e9ec76a1472
keywords:
- Функция Интерлоккедмин HLSL
topic_type:
- apiref
api_name:
- InterlockedMin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 062ae6c5fa37b732411891427770761881429069d030e9266ab20adb3e2d3726
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118509554"
---
# <a name="interlockedmin-function"></a>Функция Интерлоккедмин

Находит минимальное значение, атомарно.

## <a name="syntax"></a>Синтаксис

``` syntax
void InterlockedMin(
  in  UINT dest,
  in  UINT value,
  out UINT original_value
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*конечный адрес* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Адрес назначения.

</dd> <dt>

*значение* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Входное значение.

</dd> <dt>

*исходное \_ значение* \[ out\]
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Исходное значение.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Ничего

## <a name="remarks"></a>Remarks

Эта операция может выполняться только с типизированными ресурсами int и uint и переменными общей памяти. Существует три возможных способа использования этой функции. Первый — когда R является переменной общей памяти. В этом случае функция выполняет атомарный минимум значения для регистра общей памяти, на который ссылается dest. Второй сценарий заключается в том, что R является типом переменной ресурса. В этом сценарии функция выполняет атомарное минимальное значение для расположения ресурса, на которое ссылается dest. Наконец, третий сценарий происходит, когда R является локальным типом переменной. В этом сценарии функция сокращает до минимума значение dest и value, хранящееся в dest. Перегруженная функция имеет дополнительную выходную переменную, которой будет присвоено исходное значение dest. Эта перегруженная операция доступна только в том случае, если R доступен для чтения и записи.

Эта функция поддерживается в следующих типах шейдеров:



| VS  | HS  | DS  | GS  | PS  | CS  |
|-----|-----|-----|-----|-----|-----|
| x   |  x  | x   | x   | x   | x   |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[рвбитеаддрессбуффер](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[Модель шейдера 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
---
title: 'Функция Рвбитеаддрессбуффер:: Интерлоккедмакс'
description: Находит максимальное значение, атомарно.
ms.assetid: 2e78065f-c1ee-47ac-a826-c8a46c730c4a
keywords:
- Функция Интерлоккедмакс HLSL
topic_type:
- apiref
api_name:
- InterlockedMax
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5ca02966843d74aa17c3f5292ee3edf868140ae5722c26f47ec0270722cbbae2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118790279"
---
# <a name="interlockedmax-function"></a>Функция Интерлоккедмакс

Находит максимальное значение, атомарно.

## <a name="syntax"></a>Синтаксис

``` syntax
void InterlockedMax(
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

Эта функция не возвращает значение.

## <a name="remarks"></a>Remarks

Эта операция может выполняться только с типизированными ресурсами int и uint и переменными общей памяти. Существует три возможных способа использования этой функции. Первый — когда R является переменной общей памяти. В этом случае функция выполняет атомарный максимум значений для регистра общей памяти, на который ссылается dest. Второй сценарий заключается в том, что R является типом переменной ресурса. В этом сценарии функция выполняет атомарное максимальное значение для расположения ресурса, на которое ссылается dest. Наконец, третий сценарий происходит, когда R является локальным типом переменной. В этом сценарии функция сокращает до максимального значения dest и value, хранящегося в dest. Перегруженная функция имеет дополнительную выходную переменную, которой будет присвоено исходное значение dest. Эта перегруженная операция доступна только в том случае, если R доступен для чтения и записи.

Эта функция поддерживается в следующих типах шейдеров:



| VS  | HS  | DS  | GS  | PS  | CS  |
|-----|-----|-----|-----|-----|-----|
| x   | x   | x   | x   | x   | x   |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[рвбитеаддрессбуффер](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[Модель шейдера 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
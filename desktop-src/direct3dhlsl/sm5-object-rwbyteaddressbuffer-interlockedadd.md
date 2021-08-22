---
title: 'Функция Рвбитеаддрессбуффер:: Интерлоккедадд'
description: Добавляет значение атомарным образом.
ms.assetid: 27274aae-1e75-4626-9997-57c4e9393000
keywords:
- Функция Интерлоккедадд HLSL
topic_type:
- apiref
api_name:
- InterlockedAdd
api_location:
- winnt.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88fb2f9dd6b2e42cb8f63a7c77186386c7cff06e9008a5b45cc7e95a7d9c0e21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118790299"
---
# <a name="interlockedadd-function"></a>Функция Интерлоккедадд

Добавляет значение атомарным образом.

## <a name="syntax"></a>Синтаксис

``` syntax
void InterlockedAdd(
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

Эту операцию можно выполнить только для типизированных ресурсов типа int или uint и переменных общей памяти. Существует три возможных способа использования этой функции. Первый — когда R является переменной общей памяти. В этом случае функция выполняет атомарное Добавление значения в регистр общей памяти, на который ссылается dest. Второй сценарий заключается в том, что R является типом переменной ресурса. В этом сценарии функция выполняет атомарное Добавление значения в расположение ресурса, на которое ссылается dest. Наконец, третий сценарий происходит, когда R является локальным типом переменной. В этом сценарии функция сокращается до суммы значений dest и value, сохраненных в dest. Перегруженная функция имеет дополнительную выходную переменную, которой будет присвоено исходное значение dest. Эта перегруженная операция доступна только в том случае, если R доступен для чтения и записи.

Эта функция поддерживается в следующих типах шейдеров:



| VS  | HS  | DS  | GS  | PS  | CS  |
|-----|-----|-----|-----|-----|-----|
| x   | x   | x   | x   | x   | x   |



 

## <a name="requirements"></a>Требования




## <a name="see-also"></a>См. также раздел

<dl> <dt>

[рвбитеаддрессбуффер](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[Модель шейдера 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 


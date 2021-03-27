---
title: 'Функция Рвбитеаддрессбуффер:: Интерлоккедкомпаресторе'
description: Ккомпарес входные данные для значения сравнения атомарно.
ms.assetid: d82a73b6-24a5-4eb3-9f20-15ba263c93d0
keywords:
- Функция Интерлоккедкомпаресторе HLSL
topic_type:
- apiref
api_name:
- InterlockedCompareStore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: abaa390ba74657e42b54a5147a7bc4006564a5fb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103890909"
---
# <a name="interlockedcomparestore-function"></a>Функция Интерлоккедкомпаресторе

Ккомпарес входные данные для значения сравнения атомарно.

## <a name="syntax"></a>Синтаксис

``` syntax
void InterlockedCompareStore(
  in UINT dest,
  in UINT compare_value,
  in UINT value
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*конечный адрес* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Адрес назначения.

</dd> <dt>

*сравнить \_ значение* \[ в\]
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Значение сравнения.

</dd> <dt>

*значение* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Входное значение.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="remarks"></a>Примечания

Эта операция может выполняться только с типизированными ресурсами типа int или uint и переменными общей памяти. Существует три возможных способа использования этой функции. Первый — когда R является переменной общей памяти. В этом случае функция выполняет операцию с регистром общей памяти, на который ссылается dest. Второй сценарий заключается в том, что R является типом переменной ресурса. В этом сценарии функция выполняет операцию с расположением ресурса, на которое ссылается dest. Наконец, третий сценарий происходит, когда R является локальным типом переменной. В этом сценарии функция сокращается до операции, выполняемой с помощью локальных операций.

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

 

 
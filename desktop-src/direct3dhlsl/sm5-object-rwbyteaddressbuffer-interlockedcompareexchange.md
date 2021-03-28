---
title: 'Функция Рвбитеаддрессбуффер:: Интерлоккедкомпариксчанже'
description: Сравнивает входные данные со значением сравнения и обменивает результат атомарным образом.
ms.assetid: 9d6e8d95-5157-49a7-8a79-f3ca6ba87ebb
keywords:
- Функция Интерлоккедкомпариксчанже HLSL
topic_type:
- apiref
api_name:
- InterlockedCompareExchange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 18c7e5d58fe926d09e7ec48ee12a2336627d5db2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793008"
---
# <a name="interlockedcompareexchange-function"></a>Функция Интерлоккедкомпариксчанже

Сравнивает входные данные со значением сравнения и обменивает результат атомарным образом.

## <a name="syntax"></a>Синтаксис

``` syntax
void InterlockedCompareExchange(
  in  UINT dest,
  in  UINT compare_value,
  in  UINT value,
  out UINT original_value
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

</dd> <dt>

*исходное \_ значение* \[ out\]
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Исходное значение.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="remarks"></a>Примечания

Атомарно сравнивает значение в *dest* для сравнения со *\_ значением*, сохраняет значение в *dest* , если значения совпадают, и возвращает исходное значение *dest* в *исходном \_ значении*. Эта операция может выполняться только с типизированными ресурсами **типа int** или *uint* и переменными общей памяти. Существует три возможных способа использования этой функции. Первый — когда R является переменной общей памяти. В этом случае функция выполняет операцию с регистром общей памяти, на который ссылается *dest*. Второй сценарий заключается в том, что R является типом переменной ресурса. В этом сценарии функция выполняет операцию с расположением ресурса, на которое ссылается *dest*. Наконец, третий сценарий происходит, когда R является локальным типом переменной. В этом сценарии функция сокращается до операции, выполняемой с помощью локальных операций. Эта операция доступна только в том случае, если R доступен для чтения и записи.

> [!Note]  
> Если вы вызываете **интерлоккедкомпариксчанже** в цикле [**for**](dx-graphics-hlsl-for.md) или [**while**](dx-graphics-hlsl-while.md) COMPUTE, для правильной компиляции необходимо использовать атрибут **\[ allow \_ UAV \_ Condition \]** в этом цикле.

 

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

 

 
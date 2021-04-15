---
title: Метод выделения Имеморяллокатор
description: Метод Allocate выделяет память для функции Стгконвертпропертитовариант, когда функция преобразует тип данных СЕРИАЛИЗЕДПРОПЕРТИВАЛУЕ в тип данных ПРОПВАРИАНТ.
ms.assetid: aa9c9308-fb55-405c-901a-9d5abfac5395
keywords:
- Выделить структурированное хранилище методов
- Выделить структурированное хранилище методов, интерфейс Имеморяллокатор
- Структурированное хранилище интерфейса Имеморяллокатор, метод Allocate
topic_type:
- apiref
api_name:
- IMemoryAllocator.Allocate
api_location:
- Ole32.lib
- Ole32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7ee4b220e1c1e14ceed685e9b2adc694a44d2e4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661819"
---
# <a name="imemoryallocatorallocate-method"></a>Метод Имеморяллокатор:: allocate

Метод **allocate** выделяет память для функции [**стгконвертпропертитовариант**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) , когда функция преобразует тип данных **сериализедпропертивалуе** в тип данных **пропвариант** .

## <a name="syntax"></a>Синтаксис


```C++
virtual void* Allocate(
  [in] ULONG cbSize
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*кбсизе* \[ окне\]
</dt> <dd>

Задает размер выделяемой памяти.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                           |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                 |
| Библиотека<br/>                  | <dl> <dt>Ole32. lib</dt> </dl> |



 


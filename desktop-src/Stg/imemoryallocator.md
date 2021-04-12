---
title: Класс Имеморяллокатор
description: Реализуется механизмом выделения памяти для функции Стгконвертпропертитовариант.
ms.assetid: a0735b62-5ed3-42df-a320-b58c742645a8
keywords:
- Структурированное хранилище класса Имеморяллокатор
- Структурированное хранилище класса Имеморяллокатор, описание
topic_type:
- apiref
api_name:
- IMemoryAllocator
api_location:
- Ole32.lib
- Ole32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 421162fd0ee6228f1dbae03eeb52e5643b0e0b15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415640"
---
# <a name="imemoryallocator-class"></a>Класс Имеморяллокатор

Класс **имеморяллокатор** реализуется механизмом выделения памяти для функции [**стгконвертпропертитовариант**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) .

## <a name="methods"></a>Методы



| Имя                                                     | Описание                                                                                                                                                                                                        |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Памяти**](imemoryallocator-allocate.md)<br/> | Выделяет память для функции [**стгконвертпропертитовариант**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) , когда функция преобразует тип данных **сериализедпропертивалуе** в тип данных **пропвариант** .<br/> |
| [**Бесплатный**](/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-initialize)<br/>        | Освобождает память, выделенную методом [**выделения**](imemoryallocator-allocate.md) .<br/>                                                                                                                 |



 

## <a name="remarks"></a>Комментарии

Этот класс используется только функцией [**стгконвертпропертитовариант**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                           |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                 |
| Библиотека<br/>                  | <dl> <dt>Ole32. lib</dt> </dl> |



 


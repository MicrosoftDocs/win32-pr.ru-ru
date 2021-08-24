---
title: Функция Утилстрингкопивисаллок (Ндаттрибутилс. h)
description: Выделяет и копирует исходную строку.
ms.assetid: e1400ae1-0edd-4b59-af03-3da1b9d7073b
keywords:
- Утилстрингкопивисаллок функция NDF
topic_type:
- apiref
api_name:
- UtilStringCopyWithAlloc
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3654fa5eefd45a51d963325e10fbcba765420afe25a5c47a058bbaf4e4093ef0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801534"
---
# <a name="utilstringcopywithalloc-function"></a>Функция Утилстрингкопивисаллок

Функция **утилстрингкопивисаллок** выделяет и копирует исходную строку.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT UtilStringCopyWithAlloc(
  _Out_ LPWSTR  *Buffer,
  _In_  UINT    BufferMax,
  _In_  LPCWSTR Source
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Буфер* \[ заполняет\]
</dt> <dd>

Тип: **LPWSTR \***

Расположение, в котором хранится указатель на выделенную память. Если он больше не нужен, он должен быть выпущен с помощью [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree). Этот буфер всегда завершается нулем.

</dd> <dt>

*Буффермакс* \[ окне\]
</dt> <dd>

Тип: **uint**

Максимальное число символов для чтения из *источника*.

</dd> <dt>

*Исходный код* \[ окне\]
</dt> <dd>

Тип: **лпквстр**

Копируемая строка.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Возможные возвращаемые значения включают, но не ограничиваются следующим.



| Код возврата                                                                                  | Описание                                                        |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>         | Операция успешно выполнена.<br/>                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Один или несколько параметров указаны неправильно.<br/> |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                       |
| Заголовок<br/>                   | <dl> <dt>Ндаттрибутилс. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> <dt>

[**утилассемблестрингсвисаллок**](utilassemblestringswithalloc.md)
</dt> <dt>

[**утиллоадстрингвисаллок**](utilloadstringwithalloc.md)
</dt> </dl>

 


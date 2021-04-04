---
title: Функция Утиллоадстрингвисаллок (Ндаттрибутилс. h)
description: Выделяет и загружает строку из таблицы ресурсов.
ms.assetid: 34bf0b93-2bec-49c3-9441-c83686c4abdb
keywords:
- Утиллоадстрингвисаллок функция NDF
topic_type:
- apiref
api_name:
- UtilLoadStringWithAlloc
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72e13930fe9bb11ae9c9456152c823491eabc462
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137779"
---
# <a name="utilloadstringwithalloc-function"></a>Функция Утиллоадстрингвисаллок

Функция **утиллоадстрингвисаллок** выделяет и загружает строку из таблицы ресурсов.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT UtilLoadStringWithAlloc(
  _In_  UINT   uID,
  _Out_ LPWSTR *ppwzBuffer,
  _In_  UINT   cchBufferMax
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*UID* \[ окне\]
</dt> <dd>

Тип: **uint**

Идентификатор загружаемой строки.

</dd> <dt>

*ппвзбуффер* \[ заполняет\]
</dt> <dd>

Введите: **LPWSTR \** _

Расположение, в которое будет помещена вновь выделенная строка. Строка должна быть освобождена с помощью [_ *CoTaskMemFree* *](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) , если она больше не нужна.

</dd> <dt>

*кчбуффермакс* \[ окне\]
</dt> <dd>

Тип: **uint**

Максимальное число символов, загружаемых из таблицы ресурсов. Если длина строки ресурса превышает указанное число символов, она усекается и завершается нулем.

> [!Note]  
> Этот параметр не может иметь значение 0.

 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Возможные возвращаемые значения включают, но не ограничиваются следующим.



| Код возврата                                                                                  | Описание                                                        |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>         | Операция успешно выполнена.<br/>                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Один или несколько параметров указаны неправильно.<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                                 |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Ндаттрибутилс. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**утилстрингкопивисаллок**](utilstringcopywithalloc.md)
</dt> <dt>

[**утилассемблестрингсвисаллок**](utilassemblestringswithalloc.md)
</dt> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 


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
ms.openlocfilehash: ca649599e2a8a29ecdab2dbbfe2c188947b40487ceb82ab4937622ce82c701a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685614"
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

Тип: **LPWSTR \***

Расположение, в которое будет помещена вновь выделенная строка. Строка должна быть освобождена с помощью [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) , если она больше не нужна.

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



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                       |
| Заголовок<br/>                   | <dl> <dt>Ндаттрибутилс. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**утилстрингкопивисаллок**](utilstringcopywithalloc.md)
</dt> <dt>

[**утилассемблестрингсвисаллок**](utilassemblestringswithalloc.md)
</dt> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 


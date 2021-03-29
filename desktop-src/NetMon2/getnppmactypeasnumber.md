---
description: Извлекает тип MAC из категории Нетворкинфо раздела НПП большого двоичного объекта и преобразует данные типа в MAC-тип.
ms.assetid: 53aa538c-69ee-4b34-93fb-9e61c6baadea
title: Функция Жетнппмактипеаснумбер (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPMacTypeAsNumber
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 9174b1deeb04d8d9665509daeff56d832d447892
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540202"
---
# <a name="getnppmactypeasnumber-function"></a>Функция Жетнппмактипеаснумбер

Функция **жетнппмактипеаснумбер** ИЗВЛЕКАЕТ тип Mac из категории нетворкинфо в разделе НПП большого двоичного объекта и преобразует данные типа в Mac-тип.

## <a name="syntax"></a>Синтаксис


```C++
DWORD GetNPPMacTypeAsNumber(
  _In_  HBLOB   hBlob,
  _Out_ LPDWORD lpMacType
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хблоб* \[ окне\]
</dt> <dd>

Маркер указанного большого двоичного объекта.

</dd> <dt>

*лпмактипе* \[ заполняет\]
</dt> <dd>

Указатель на тип MAC.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция выполнена успешно, возвращается значение НМЕРР \_ Success.

Если тег недоступен, возвращаемое значение имеет \_ тип Mac \_ Unknown.

## <a name="remarks"></a>Комментарии

Эта функция сопоставляет тег **НПП: нетворкинфо: MacType** с **\_ \_ \* типом Mac** , как определено в файле нпптипес. h.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                              |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                    |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl>     |
| Библиотека<br/>                  | <dl> <dt>Нпптулс. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



 

 





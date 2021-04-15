---
description: Функция Стрингтоаддресс преобразует строку в адрес.
ms.assetid: b1ada88d-04bb-4869-87c6-99f5046356c5
title: Функция Стрингтоаддресс (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StringToAddress
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 70a9e6b42359a2f73fba55194c9b6e6e21ffa9a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683224"
---
# <a name="stringtoaddress-function"></a>Функция Стрингтоаддресс

Функция **стрингтоаддресс** преобразует строку в адрес.

## <a name="syntax"></a>Синтаксис


```C++
LPBYTE WINAPI StringToAddress(
  _Out_ BYTE  *lpAddress,
  _In_  LPSTR string
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*лпаддресс* \[ заполняет\]
</dt> <dd>

Указатель на адрес, в который преобразуется строка.

</dd> <dt>

*строка* \[ окне\]
</dt> <dd>

Строка, которая преобразуется в адрес.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение является указателем на преобразованную строку.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                            |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl>   |
| Библиотека<br/>                  | <dl> <dt>Parser. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 





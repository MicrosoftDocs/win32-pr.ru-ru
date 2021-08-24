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
ms.openlocfilehash: 9dbac01f5df9d32a65fe5afb1c1437064f6dd0d4480c95dacd0fe8f7d58e2fb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676694"
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



 

 





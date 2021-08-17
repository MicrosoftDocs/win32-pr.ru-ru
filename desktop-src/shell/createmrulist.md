---
description: Создает новый список последних использованных (MRU) списков.
title: Функция CreateMRUListW
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateMRUListW
- CreateMRUListW
api_type:
- DllExport
api_location:
- Comctl32.dll
ms.assetid: b2d9e3c7-8151-45ef-9658-bd33a87b4c9c
ms.openlocfilehash: e5f97d1f50dae081eac00014415129d8a4c858a0e6e2c3406e1a6c4f6905c71c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117861401"
---
# <a name="createmrulistw-function"></a>Функция CreateMRUListW

Создает новый список последних использованных (MRU) списков.

## <a name="syntax"></a>Синтаксис


```C++
int CreateMRUListW(
  _In_ LPMRUINFO lpmi
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*лпми* \[ окне\]
</dt> <dd>

Тип: **лпмруинфо**

Указатель на структуру [**мруинфо**](mruinfo.md) , определяющую список MRU.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **int**

Возвращает маркер нового списка MRU или значение 0 в случае ошибки.

## <a name="remarks"></a>Remarks

Эта функция не включена в общедоступный заголовок или библиотеку. Доступ к нему можно получить с помощью [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) или извлечь из comctl32.dll по порядковому номеру, 400 для **креатемрулиств**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                     |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (версия 5,0 или более поздняя)</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **Креатемрулиств** (Юникод)<br/>                                                                        |



 

 

---
description: Получает состояние кэша автономные файлы.
ms.assetid: a8cc0dbb-0005-4e74-892e-898e2ebe0465
title: Функция Ксккуеридатабасестатус
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCQueryDatabaseStatus
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: badd869306290609ccadeba80e6ea67ca3479be8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648978"
---
# <a name="cscquerydatabasestatus-function"></a>Функция Ксккуеридатабасестатус

\[Эта функция не поддерживается и не должна использоваться.\]

Получает состояние кэша автономные файлы.

## <a name="syntax"></a>Синтаксис


```C++
BOOL WINAPI CSCQueryDatabaseStatus(
   ULONG *pulStatus,
   ULONG *pulErrors
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пулстатус* 
</dt> <dd>

Состояние. Этот параметр может принимать одно из указанных ниже значений.



| Значение                                                                                                                                                                                                                                                                                                               | Значение                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span id="FLAG_DATABASESTATUS_ENCRYPTED"></span><span id="flag_databasestatus_encrypted"></span><dl> <dt>**Флаг \_ DATABASESTATUS, \_ зашифрованный**</dt> <dt>0x00000002</dt> </dl>                                      | Кэш помечен для шифрования, и все файлы в кэше шифруются.<br/>                |
| <span id="FLAG_DATABASESTATUS_PARTIALLY_ENCRYPTED"></span><span id="flag_databasestatus_partially_encrypted"></span><dl> <dt>**Флаг \_ DATABASESTATUS с \_ частичным \_ шифрованием**</dt> <dt>0x00000004</dt> </dl>       | Кэш помечен для шифрования, но некоторые файлы в кэше не шифруются.<br/>          |
| <span id="FLAG_DATABASESTATUS_PARTIALLY_UNENCRYPTED"></span><span id="flag_databasestatus_partially_unencrypted"></span><dl> <dt>**Флаг \_ DATABASESTATUS \_ частично без \_ шифрования**</dt> <dt>0x00000004</dt> </dl> | Кэш не помечен для шифрования, но не все файлы в кэше были расшифрованы.<br/> |
| <span id="FLAG_DATABASESTATUS_UNENCRYPTED"></span><span id="flag_databasestatus_unencrypted"></span><dl> <dt>**Флаг \_ DATABASESTATUS без \_ шифрования**</dt> <dt>0x00000000</dt> </dl>                                | Кэш не помечен для шифрования, и все файлы в кэше были расшифрованы.<br/>      |



 

</dd> <dt>

*пулеррорс* 
</dt> <dd>

Этот параметр имеет ненулевое значение, если возникла внутренняя ошибка базы данных или 0 в противном случае.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает **значение true** , если она выполнена. в противном случае возвращается **значение false**.

## <a name="remarks"></a>Комментарии

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cscmig.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ксЦисксценаблед**](csciscscenabled.md)
</dt> </dl>

 

 

---
description: Создает сертификат пользователя для использования с Конференцией NetMeeting.
ms.assetid: 22acdcbe-c9c9-4f1b-a62d-44a35e101eec
title: Функция Нммакецерт
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NmMakeCert
api_type:
- DllExport
api_location:
- Nmmkcert.dll
ms.openlocfilehash: f90af11ada2bca330bbabeb83f4a8aa94e611630
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648847"
---
# <a name="nmmakecert-function"></a>Функция Нммакецерт

Создает сертификат пользователя для использования с Конференцией NetMeeting.

## <a name="syntax"></a>Синтаксис


```C++
void NmMakeCert(
   LPCSTR szFirstName,
   LPCSTR szLastName,
   LPCSTR szEmailName,
   LPCSTR szCity,
   LPCSTR szCountry,
   DWORD  dwFlags
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*сзфирстнаме* 
</dt> <dd>

Имя пользователя.

</dd> <dt>

*сзластнаме* 
</dt> <dd>

Фамилия пользователя.

</dd> <dt>

*сземаилнаме* 
</dt> <dd>

Имя электронной почты пользователя.

</dd> <dt>

*сзЦити* 
</dt> <dd>

Город пользователя.

</dd> <dt>

*сзкаунтри* 
</dt> <dd>

Страна или регион пользователя.

</dd> <dt>

*dwFlags* 
</dt> <dd>

Значение, указывающее, как должен быть создан сертификат. Может принимать любое из следующих значений.



| Значение                                                                                                                                                                                                                                                            | Значение                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <span id="NMMKCERT_F_CLEANUP_ONLY"></span><span id="nmmkcert_f_cleanup_only"></span><dl> <dt>**Нммкцерт \_ F \_ Очистка \_ только**</dt> <dt>0x00000004</dt> </dl>    | Удалите старый сертификат, не создавая новый. <br/>            |
| <span id="NMMKCERT_F_DELETEOLDCERT"></span><span id="nmmkcert_f_deleteoldcert"></span><dl> <dt>**Нммкцерт \_ F \_ делетеолдцерт**</dt> <dt>0x00000001</dt> </dl>  | Удалите старый сертификат, созданный ранее с помощью этой функции. <br/> |
| <span id="NMMKCERT_F_LOCAL_MACHINE"></span><span id="nmmkcert_f_local_machine"></span><dl> <dt>**Нммкцерт \_ \_Локальный \_ компьютер F**</dt> ( <dt>0x00000002</dt> ) </dl> | Создайте сертификат в хранилище сертификатов на локальном компьютере. <br/>    |



 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 1, если функция завершается успешно, и – 1, если функция завершается ошибкой.

## <a name="remarks"></a>Комментарии

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Nmmkcert.dll</dt> </dl> |



 

 

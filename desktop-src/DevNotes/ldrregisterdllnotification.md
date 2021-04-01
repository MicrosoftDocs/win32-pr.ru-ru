---
description: Регистрируется для уведомления при первой загрузке библиотеки DLL. Это уведомление происходит до того, как будет выполнена динамическая компоновка.
ms.assetid: c2757aa0-76fa-427a-a4f6-cb26e7f7d0d1
title: Функция Лдррегистердллнотификатион
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LdrRegisterDllNotification
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: 82ec05a24f4cccc89cece666b18cb63412a78259
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072361"
---
# <a name="ldrregisterdllnotification-function"></a>Функция Лдррегистердллнотификатион

\[Эта функция может быть изменена или удалена из Windows без предварительного уведомления.\]

Регистрируется для уведомления при первой загрузке библиотеки DLL. Это уведомление происходит до того, как будет выполнена динамическая компоновка.

## <a name="syntax"></a>Синтаксис


```C++
NTSTATUS NTAPI LdrRegisterDllNotification(
  _In_     ULONG                          Flags,
  _In_     PLDR_DLL_NOTIFICATION_FUNCTION NotificationFunction,
  _In_opt_ PVOID                          Context,
  _Out_    PVOID                          *Cookie
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Флаги* \[ окне\]
</dt> <dd>

Этот параметр должен быть равен нулю.

</dd> <dt>

*Нотификатионфунктион* \[ окне\]
</dt> <dd>

Указатель на функцию обратного вызова уведомления [*лдрдллнотификатион*](ldrdllnotification.md) для вызова при загрузке библиотеки DLL.

</dd> <dt>

*Контекст* \[ в необязательное\]
</dt> <dd>

Указатель на данные контекста для функции обратного вызова.

</dd> <dt>

*Файл cookie* \[ заполняет\]
</dt> <dd>

Указатель на переменную, которая получает идентификатор для функции обратного вызова. Этот идентификатор используется для отмены регистрации функции обратного вызова уведомлений.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция завершается успешно, возвращается **состояние \_ Success**.

Формы и значения кодов ошибок **NTSTATUS** перечислены в файле заголовка NTSTATUS. h, доступном в WDK, и описаны в документации по WDK.

## <a name="remarks"></a>Комментарии

Эта функция не имеет связанного файла заголовка. Связанная библиотека импорта, NTDLL. lib, доступна в WDK. Можно также использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Ntdll.dll.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[*лдрдллнотификатион*](ldrdllnotification.md)
</dt> <dt>

[**лдрунрегистердллнотификатион**](ldrunregisterdllnotification.md)
</dt> </dl>

 

 

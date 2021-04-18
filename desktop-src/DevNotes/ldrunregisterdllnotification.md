---
description: Отменяет уведомление о загрузке DLL, зарегистрированное ранее путем вызова функции Лдррегистердллнотификатион.
ms.assetid: 18c3a027-e3cb-4083-afdc-00f416a70d8c
title: Функция Лдрунрегистердллнотификатион
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LdrUnregisterDllNotification
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: 1fee03b4a06d274b495070eb40833b270a795158
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423190"
---
# <a name="ldrunregisterdllnotification-function"></a>Функция Лдрунрегистердллнотификатион

\[Эта функция может быть изменена или удалена из Windows без предварительного уведомления.\]

Отменяет уведомление о загрузке DLL, зарегистрированное ранее путем вызова функции [**лдррегистердллнотификатион**](ldrregisterdllnotification.md) .

## <a name="syntax"></a>Синтаксис


```C++
NTSTATUS NTAPI LdrUnregisterDllNotification(
  _In_ PVOID Cookie
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Файл cookie* \[ окне\]
</dt> <dd>

Указатель на идентификатор обратного вызова, полученный из вызова [**лдррегистердллнотификатион**](ldrregisterdllnotification.md) , зарегистрированного для уведомления.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает код **NTSTATUS** или ошибки.

Если функция завершается успешно, возвращается **состояние \_ Success**.

Если функция обратного вызова не найдена, функция возвращает **\_ библиотеку DLL состояния \_ не \_ найдена**.

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

[**лдррегистердллнотификатион**](ldrregisterdllnotification.md)
</dt> </dl>

 

 

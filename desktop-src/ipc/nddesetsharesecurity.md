---
description: Задает дескриптор безопасности, связанный с общим ресурсом DDE.
ms.assetid: 8bb8c466-3dd7-49a6-8ba5-632001b8a47f
title: Функция Нддесетшаресекурити (Нддеапи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeSetShareSecurity
- NDdeSetShareSecurityA
- NDdeSetShareSecurityW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 112752bcd0953fbbc358c75080cb2749273ed95d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683880"
---
# <a name="nddesetsharesecurity-function"></a>Функция Нддесетшаресекурити

\[Сетевой DDE больше не поддерживается. Nddeapi.dll имеется в Windows Vista, но все вызовы функций возвращают НДДЕ \_ не \_ реализован.\]

Задает дескриптор безопасности, связанный с общим ресурсом DDE. Это обычно происходит после изменения списка DACL, назначенного общему ресурсу DDE.

## <a name="syntax"></a>Синтаксис


```C++
UINT NDdeSetShareSecurity(
  _In_ LPTSTR               lpszServer,
  _In_ LPTSTR               lpszShareName,
  _In_ SECURITY_INFORMATION si,
  _In_ PSECURITY_DESCRIPTOR pSD
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*лпсзсервер* \[ окне\]
</dt> <dd>

Имя сервера, DSDM которого необходимо изменить.

</dd> <dt>

*лпсзшаренаме* \[ окне\]
</dt> <dd>

Имя общей папки, дескриптор безопасности которой необходимо изменить. Этот параметр не может иметь **значение NULL**.

</dd> <dt>

*Si* \[ окне\]
</dt> <dd>

Значение [**\_ сведений о безопасности**](/windows/desktop/SecAuthZ/security-information) , идентифицирующее сведения о безопасности для извлечения.

</dd> <dt>

*pSD* \[ - окне\]
</dt> <dd>

Указатель на структуру [**\_ дескриптора безопасности**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) , содержащую сведения о безопасности. Этот параметр не может иметь **значение NULL** и указывать на допустимый дескриптор безопасности.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция выполнена удачно, возвращается значение НДДЕ \_ No \_ Error.

Если функция завершается ошибкой, возвращаемое значение является кодом ошибки, который может быть преобразован в текстовое сообщение об ошибке путем вызова [**нддежетеррорстринг**](nddegeterrorstring.md).

## <a name="remarks"></a>Комментарии

Чтобы изменить [**\_ дескриптор безопасности**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) , связанный с общим ресурсом DDE в DSDM, пользователь должен иметь соответствующие права доступа. Автор общей папки имеет эту привилегию.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                             |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                   |
| Заголовок<br/>                   | <dl> <dt>Нддеапи. h</dt> </dl>   |
| Библиотека<br/>                  | <dl> <dt>Нддеапи. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **Нддесетшаресекуритив** (Юникод) и **нддесетшаресекуритя** (ANSI)<br/>    |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Общие сведения о сетевом платформа динамических данных Exchange](network-dynamic-data-exchange.md)
</dt> <dt>

[Сетевые функции DDE](network-dde-functions.md)
</dt> <dt>

[**\_сведения о безопасности**](/windows/desktop/SecAuthZ/security-information)
</dt> <dt>

[**нддежетшаресекурити**](nddegetsharesecurity.md)
</dt> </dl>

 


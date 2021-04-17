---
description: Задает безопасность открытого раздела реестра в автономном кусте реестра.
ms.assetid: 002866bb-1532-41ad-a4db-a32d6e1c0a6a
title: Функция Орсеткэйсекурити (Оффрег. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORSetKeySecurity
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: ff63a7d896964f486b5fcb168c08513f8d5703be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665119"
---
# <a name="orsetkeysecurity-function"></a>Функция Орсеткэйсекурити

Задает безопасность открытого раздела реестра в автономном кусте реестра.

## <a name="syntax"></a>Синтаксис


```C++
DWORD ORSetKeySecurity(
  _In_ ORHKEY               Handle,
  _In_ SECURITY_INFORMATION SecurityInformation,
  _In_ PSECURITY_DESCRIPTOR pSecurityDescriptor
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Обработчик* \[ окне\]
</dt> <dd>

Маркер открытого раздела реестра в автономном кусте реестра.

</dd> <dt>

*Секуритинформатион* \[ окне\]
</dt> <dd>

Битовые флаги, указывающие тип сведений о безопасности для установки. Этот параметр может быть сочетанием битовых флагов [ \_ сведений о безопасности](../secauthz/security-information.md) .

</dd> <dt>

*псекуритидескриптор* \[ окне\]
</dt> <dd>

Указатель на структуру [ \_ дескриптора безопасности](/windows/win32/api/winnt/ns-winnt-security_descriptor) , указывающую атрибуты безопасности, которые необходимо задать для указанного ключа.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция завершается успешно, функция возвращает ошибку \_ Success.

Если функция завершается ошибкой, она возвращает ненулевой код ошибки, определенный в файле Winerror. h. [](/windows/win32/api/winbase/nf-winbase-formatmessage) \_ \_ \_ Для получения обобщенного описания ошибки можно использовать функцию FormatMessage с флагом формата Message от System.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------|---------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | Автономная библиотека реестра Windows версии 1,0 или более поздней<br/>                      |
| Header<br/>          | <dl> <dt>Оффрег. h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**орклосекэй**](orclosekey.md)
</dt> <dt>

[**орделетекэй**](ordeletekey.md)
</dt> <dt>

[**оропенкэй**](oropenkey.md)
</dt> <dt>

[**оржеткэйсекурити**](orgetkeysecurity.md)
</dt> <dt>

[\_дескриптор безопасности](/windows/win32/api/winnt/ns-winnt-security_descriptor)
</dt> <dt>

[\_сведения о безопасности](../secauthz/security-information.md)
</dt> </dl>

 

 

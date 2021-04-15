---
title: Метод Сетсессионтимеаут класса Win32_TSGatewayConnectionAuthorizationPolicy
description: Задает свойства SessionTimeout и Сессионтимеаутактион.
ms.assetid: 11491c97-3ef8-46c1-9504-696c613e374e
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетсессионтимеаут
- Службы удаленных рабочих столов метода Сетсессионтимеаут, класс Win32_TSGatewayConnectionAuthorizationPolicy
- Класс Win32_TSGatewayConnectionAuthorizationPolicy службы удаленных рабочих столов, метод Сетсессионтимеаут
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetSessionTimeout
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8e544b59ae4fe0b74d0c120e6884ab81743cac6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534547"
---
# <a name="setsessiontimeout-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Метод Сетсессионтимеаут \_ класса Win32 тсгатевайконнектионаусоризатионполици

Задает свойства **SessionTimeout** и **сессионтимеаутактион** .

## <a name="syntax"></a>Синтаксис


```mof
uint32 SetSessionTimeout(
  [in] uint32 SessionTimeout,
  [in] uint32 SessionTimeoutAction
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*SessionTimeout* \[ окне\]
</dt> <dd>

Тип: **UInt32**

Новое значение времени ожидания в минутах. Значение 0 означает отсутствие времени ожидания.

</dd> <dt>

*Сессионтимеаутактион* \[ окне\]
</dt> <dd>

Тип: **UInt32**

Указывает действие, выполняемое в случае истечения времени ожидания сеанса. Это может быть одно из следующих значений.

<dt>

0
</dt> <dd>

Отключите сеанс.

</dd> <dt>

1
</dt> <dd>

Попытка повторно авторизовать сеанс.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **UInt32**

Если метод завершается с ошибкой, он возвращает ноль. Если метод завершился неудачно, он возвращает ненулевое значение. Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Комментарии

Для вызова этого метода необходимо быть членом группы администраторов.

Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008 R2<br/>                                                        |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Тсгатевайконнектионаусоризатионполици Win32**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 


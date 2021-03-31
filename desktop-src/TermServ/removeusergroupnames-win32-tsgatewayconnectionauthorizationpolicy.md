---
title: Метод Ремовеусерграупнамес класса Win32_TSGatewayConnectionAuthorizationPolicy
description: Удаляет указанные имена групп пользователей из существующих групп пользователей в свойстве Усерграупнамес.
ms.assetid: 4ddbac15-7054-482a-8b5c-49551561673e
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Ремовеусерграупнамес
- Службы удаленных рабочих столов метода Ремовеусерграупнамес, класс Win32_TSGatewayConnectionAuthorizationPolicy
- Класс Win32_TSGatewayConnectionAuthorizationPolicy службы удаленных рабочих столов, метод Ремовеусерграупнамес
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.RemoveUserGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69e4c3d9556243bcb28167378fea6018b4cd2ded
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988388"
---
# <a name="removeusergroupnames-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Метод Ремовеусерграупнамес \_ класса Win32 тсгатевайконнектионаусоризатионполици

Удаляет указанные имена групп пользователей из существующих групп пользователей в свойстве **усерграупнамес** .

## <a name="syntax"></a>Синтаксис


```mof
uint32 RemoveUserGroupNames(
  [in] string UserGroupNames
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Усерграупнамес* \[ окне\]
</dt> <dd>

Имена удаляемых групп пользователей. Имена групп пользователей должны иметь формат *домена \\ усерграупнаме*.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается с ошибкой, он возвращает ноль. Если метод завершился неудачно, он возвращает ненулевое значение. Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Комментарии

Если в параметре *усерграупнамес* указано несколько имен групп пользователей и одно из имен не может быть обработано, никакие имена не будут обработаны.

Для вызова этого метода необходимо быть членом группы администраторов.

Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                           |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Тсгатевайконнектионаусоризатионполици Win32**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 


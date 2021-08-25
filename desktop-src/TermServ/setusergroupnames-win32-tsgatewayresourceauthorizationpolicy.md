---
title: Метод Сетусерграупнамес класса Win32_TSGatewayResourceAuthorizationPolicy
description: Задает свойство Усерграупнамес для политики авторизации ресурсов удаленный рабочий стол (RD \ 160; RAP).
ms.assetid: 91b77cd6-779e-460a-88a3-eda7a6fe99e5
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетусерграупнамес
- Службы удаленных рабочих столов метода Сетусерграупнамес, класс Win32_TSGatewayResourceAuthorizationPolicy
- Класс Win32_TSGatewayResourceAuthorizationPolicy службы удаленных рабочих столов, метод Сетусерграупнамес
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.SetUserGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18d4a54f042ebf99ff5a3b1bf16081ce0719578ef7fc2fd272e9ccc07a832822
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008574"
---
# <a name="setusergroupnames-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a>Метод Сетусерграупнамес \_ класса Win32 тсгатевайресаурцеаусоризатионполици

Задает свойство **усерграупнамес** для политики авторизации ресурсов (RD RAP) удаленный рабочий стол.

## <a name="syntax"></a>Синтаксис


```mof
uint32 SetUserGroupNames(
  [in] string UserGroupNames
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Усерграупнамес* \[ окне\]
</dt> <dd>

Разделенный точками с запятой список имен групп пользователей. Имена имеют формат *домена \\ усерграупнаме*. Если пользователь принадлежит к любой из этих групп пользователей, доступ будет разрешен.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается с ошибкой, он возвращает ноль. Если метод завершился неудачно, он возвращает ненулевое значение. Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Remarks

Если в параметре *усерграупнамес* указано несколько имен групп пользователей и одно из имен не может быть обработано, никакие имена не будут обработаны.

Для вызова этого метода необходимо быть членом группы администраторов.

файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). файлы MOF не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows Software Development Kit (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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

[**\_Тсгатевайресаурцеаусоризатионполици Win32**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 


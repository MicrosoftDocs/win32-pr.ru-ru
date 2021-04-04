---
title: Метод Сетдевицередиректионтипе класса Win32_TSGatewayConnectionAuthorizationPolicy
description: Задает свойство Девицередиректионтипе, которое управляет тем, какие устройства будут перенаправляться.
ms.assetid: d97a0a7d-a08e-4703-b0f0-ba5d20688dc8
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетдевицередиректионтипе
- Службы удаленных рабочих столов метода Сетдевицередиректионтипе, класс Win32_TSGatewayConnectionAuthorizationPolicy
- Класс Win32_TSGatewayConnectionAuthorizationPolicy службы удаленных рабочих столов, метод Сетдевицередиректионтипе
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetDeviceRedirectionType
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98b369e0b6031aa503e2f7f55860d004f63b7f93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988572"
---
# <a name="setdeviceredirectiontype-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Метод Сетдевицередиректионтипе \_ класса Win32 тсгатевайконнектионаусоризатионполици

Задает свойство **девицередиректионтипе** , которое управляет тем, какие устройства будут перенаправляться.

## <a name="syntax"></a>Синтаксис


```mof
uint32 SetDeviceRedirectionType(
  [in] uint32 DeviceRedirectionType
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Девицередиректионтипе* \[ окне\]
</dt> <dd>

Тип перенаправления устройства.

<dt>

0
</dt> <dd>

Все устройства будут перенаправляться.

</dd> <dt>

1
</dt> <dd>

Устройства не будут перенаправлены.

</dd> <dt>

2
</dt> <dd>

Указанные устройства не будут перенаправляться. Свойства **дискдривесдисаблед**, **принтерсдисаблед**, **сериалпортсдисаблед**, **клипбоарддисаблед** и **плугандплайдевицесдисаблед** определяют, какие устройства не будут перенаправляться.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается с ошибкой, он возвращает ноль. Если метод завершился неудачно, он возвращает ненулевое значение. Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Комментарии

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

 


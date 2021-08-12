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
ms.openlocfilehash: bdd3ccbe06acbc75e8c7c29632d7fd83dc0af222eb004c6b83976e3f6478f705
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118604663"
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

## <a name="remarks"></a>Remarks

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

[**\_Тсгатевайконнектионаусоризатионполици Win32**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 


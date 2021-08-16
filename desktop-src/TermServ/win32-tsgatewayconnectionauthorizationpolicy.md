---
title: Класс Win32_TSGatewayConnectionAuthorizationPolicy
description: Описание политики авторизации подключений удаленный рабочий стол (RD \ 160; CAP). RD \ 160; С помощью политик можно определить, разрешено ли пользователю подключаться к серверу шлюза удаленный рабочий стол (шлюз удаленных рабочих столов).
ms.assetid: 50ff3f97-0818-4e9c-9db7-a822cfed0e82
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSGatewayConnectionAuthorizationPolicy службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSGatewayConnectionAuthorizationPolicy, описание
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy
- Win32_TSGatewayConnectionAuthorizationPolicy.Name
- Win32_TSGatewayConnectionAuthorizationPolicy.Order
- Win32_TSGatewayConnectionAuthorizationPolicy.SmartcardAllowed
- Win32_TSGatewayConnectionAuthorizationPolicy.PasswordAllowed
- Win32_TSGatewayConnectionAuthorizationPolicy.SecureIdAllowed
- Win32_TSGatewayConnectionAuthorizationPolicy.CookieAuthenticationAllowed
- Win32_TSGatewayConnectionAuthorizationPolicy.Enabled
- Win32_TSGatewayConnectionAuthorizationPolicy.IdleTimeout
- Win32_TSGatewayConnectionAuthorizationPolicy.SessionTimeout
- Win32_TSGatewayConnectionAuthorizationPolicy.SessionTimeoutAction
- Win32_TSGatewayConnectionAuthorizationPolicy.DeviceRedirectionType
- Win32_TSGatewayConnectionAuthorizationPolicy.DiskDrivesDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.PrintersDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.SerialPortsDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.ClipboardDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.PlugAndPlayDevicesDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.UserGroupNames
- Win32_TSGatewayConnectionAuthorizationPolicy.ComputerGroupNames
- Win32_TSGatewayConnectionAuthorizationPolicy.HasNapAttributes
- Win32_TSGatewayConnectionAuthorizationPolicy.AllowOnlySDRServers
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bfaefb0a3062db27622afe90023928507c6d127c64edb60041347f73c1b261c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118349249"
---
# <a name="win32_tsgatewayconnectionauthorizationpolicy-class"></a>\_Класс Win32 тсгатевайконнектионаусоризатионполици

Описание политики авторизации подключений удаленный рабочий стол (RD CAP). RD CAP используется, чтобы определить, разрешено ли пользователю подключаться к серверу шлюза удаленный рабочий стол (шлюз удаленных рабочих столов).

## <a name="syntax"></a>Синтаксис

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayConnectionAuthorizationPolicy
{
  string  Name;
  uint32  Order;
  boolean SmartcardAllowed;
  boolean PasswordAllowed;
  boolean SecureIdAllowed;
  boolean CookieAuthenticationAllowed;
  boolean Enabled;
  uint32  IdleTimeout;
  uint32  SessionTimeout;
  uint32  SessionTimeoutAction;
  uint32  DeviceRedirectionType;
  boolean DiskDrivesDisabled;
  boolean PrintersDisabled;
  boolean SerialPortsDisabled;
  boolean ClipboardDisabled;
  boolean PlugAndPlayDevicesDisabled;
  string  UserGroupNames;
  string  ComputerGroupNames;
  boolean HasNapAttributes;
  boolean AllowOnlySDRServers;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ тсгатевайконнектионаусоризатионполици** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **Win32 \_ тсгатевайконнектионаусоризатионполици** содержит следующие методы.



| Метод                                                                                                                | Описание                                                                                                                                                                     |
|:----------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**аддкомпутерграупнамес**](addcomputergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                   | Добавляет указанные имена групп компьютеров в свойство **компутерграупнамес** .<br/>                                                                                      |
| [**аддусерграупнамес**](addusergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                           | Добавляет указанные имена групп пользователей в свойство **усерграупнамес** .<br/>                                                                                              |
| [**Создание**](create-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | Создает ограничение удаленных рабочих столов.<br/>                                                                                                                                                   |
| [**Удален**](delete-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | Удаляет текущую политику авторизации подключений к удаленным рабочим столам.<br/>                                                                                                                                          |
| [**дисаблеклипбоард**](disableclipboard-win32-tsgatewayconnectionauthorizationpolicy.md)                             | Задает свойство **клипбоарддисаблед** .<br/>                                                                                                                             |
| [**дисабледискдривес**](disablediskdrives-win32-tsgatewayconnectionauthorizationpolicy.md)                           | Задает свойство **дискдривесдисаблед** .<br/>                                                                                                                            |
| [**дисаблеплугандплайдевицес**](disableplugandplaydevices-win32-tsgatewayconnectionauthorizationpolicy.md)           | Задает свойство **плугандплайдевицесдисаблед** .<br/>                                                                                                                    |
| [**дисаблепринтерс**](disableprinters-win32-tsgatewayconnectionauthorizationpolicy.md)                               | Задает свойство **принтерсдисаблед** .<br/>                                                                                                                              |
| [**дисаблесериалпортс**](disableserialports-win32-tsgatewayconnectionauthorizationpolicy.md)                         | Задает свойство **сериалпортсдисаблед** .<br/>                                                                                                                           |
| [**енаблеалловонлисдрсерверс**](win32-tsgatewayconnectionauthorizationpolicy-enableallowonlysdrservers.md)           | Используется для переключения свойства **алловонлисдрсерверс**<br/> **Windows Server 2008:** этот метод недоступен до Windows Server 2008 R2.<br/>                  |
| [**Вниз**](movedown-win32-tsgatewayconnectionauthorizationpolicy.md)                                             | Перемещает текущую закрепление удаленных рабочих столов в списке вниз.<br/>                                                                                                              |
| [**MoveUp**](moveup-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | Перемещает текущую закрепление удаленных рабочих столов в списке.<br/>                                                                                                                |
| [**ремовекомпутерграупнамес**](removecomputergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)             | Удаляет указанные имена групп компьютеров из свойства **компутерграупнамес** .<br/>                                                                                 |
| [**ремовеусерграупнамес**](removeusergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                     | Удаляет указанные имена групп пользователей из свойства **усерграупнамес** .<br/>                                                                                             |
| [**сеткомпутерграупнамес**](setcomputergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                   | Задает свойство **компутерграупнамес** .<br/>                                                                                                                            |
| [**сеткукиеаусентикатионалловед**](setcookieauthenticationallowed-win32-tsgatewayconnectionauthorizationpolicy.md) | Задает свойство **кукиеаусентикатионалловед** .<br/> **Windows Server 2008:** Этот метод недоступен.<br/>                                                 |
| [**сетдевицередиректионтипе**](setdeviceredirectiontype-win32-tsgatewayconnectionauthorizationpolicy.md)             | Задает свойство **девицередиректионтипе** .<br/>                                                                                                                         |
| [**сетенаблед**](setenabled-win32-tsgatewayconnectionauthorizationpolicy.md)                                         | Включает или отключает текущую политику авторизации подключений к удаленным рабочим столам.<br/>                                                                                                                              |
| [**сетидлетимеаут**](setidletimeout-win32-tsgatewayconnectionauthorizationpolicy.md)                                 | Задает свойство **IdleTimeout** .<br/> **Windows Server 2008:** этот метод недоступен до Windows Server 2008 R2.<br/>                                   |
| [**SetName**](setname-win32-tsgatewayconnectionauthorizationpolicy.md)                                               | Задает новое имя для этого ограничения удаленных рабочих столов. Этот метод гарантирует, что имена будут уникальными.<br/>                                                                                      |
| [**сетпассвордалловед**](setpasswordallowed-win32-tsgatewayconnectionauthorizationpolicy.md)                         | Задает свойство **пассвордалловед** .<br/>                                                                                                                               |
| [**сетсекуреидалловед**](setsecureidallowed-win32-tsgatewayconnectionauthorizationpolicy.md)                         | Задает свойство **секуреидалловед** .<br/> **Windows Server 2008:** Этот метод зарезервирован для использования в будущем.<br/>                                                   |
| [**сетсессионтимеаут**](setsessiontimeout-win32-tsgatewayconnectionauthorizationpolicy.md)                           | Задает свойства **SessionTimeout** и **сессионтимеаутактион** .<br/> **Windows Server 2008:** этот метод недоступен до Windows Server 2008 R2.<br/> |
| [**сетсмарткардалловед**](setsmartcardallowed-win32-tsgatewayconnectionauthorizationpolicy.md)                       | Задает свойство **смарткардалловед** .<br/>                                                                                                                              |
| [**сетусерграупнамес**](setusergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                           | Задает свойство **усерграупнамес** .<br/>                                                                                                                                |
| [**Update**](update-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | Обновляет текущую политику авторизации подключений к удаленным рабочим столам.<br/>                                                                                                                                          |



 

### <a name="properties"></a>Свойства

Класс **Win32 \_ тсгатевайконнектионаусоризатионполици** имеет следующие свойства.

<dl> <dt>

**алловонлисдрсерверс**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, разрешены ли подключения только для защиты RDS-серверов перенаправления устройств (SDR). Это свойство можно задать с помощью метода [**енаблеалловонлисдрсерверс**](win32-tsgatewayconnectionauthorizationpolicy-enableallowonlysdrservers.md) .

**Windows Server 2008:** это свойство недоступно до Windows Server 2008 R2.

</dd> <dt>

**клипбоарддисаблед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, будет ли отключено перенаправление буфера обмена. Это свойство действует, только если свойство **девицередиректионтипе** имеет значение 2.

</dd> <dt>

**компутерграупнамес**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Список имен групп компьютеров, разделенных точкой с запятой. Это значение может быть пустым. Имена имеют формат *домена \\ компутерграупнаме*. Если указано значение, то клиентский компьютер должен принадлежать к одной из этих групп компьютеров для доступа пользователя к серверу шлюза удаленных рабочих столов.

</dd> <dt>

**кукиеаусентикатионалловед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, можно ли использовать проверку подлинности файлов cookie для подключения к серверу шлюза удаленных рабочих столов. Это свойство можно задать с помощью метода [**сеткукиеаусентикатионалловед**](setcookieauthenticationallowed-win32-tsgatewayconnectionauthorizationpolicy.md) .

**Windows Server 2008:** Это свойство недоступно.

</dd> <dt>

**девицередиректионтипе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, какие устройства будут перенаправляться.

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

</dd> </dl>

</dd> <dt>

**дискдривесдисаблед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, будет ли перенаправление диска отключено. Это свойство действует, только если свойство **девицередиректионтипе** имеет значение 2.

</dd> <dt>

**Включен**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, будет ли использоваться эта политика авторизации подключений удаленных рабочих столов для проверки подлинности пользователя.

</dd> <dt>

**хаснапаттрибутес**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, использует ли политика авторизации подключений к удаленному рабочему столу атрибуты защиты доступа к сети (NAP).

</dd> <dt>

**IdleTimeout**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Значение времени ожидания простоя в минутах. Значение 0 означает отсутствие времени ожидания. Это свойство можно задать с помощью метода [**сетидлетимеаут**](setidletimeout-win32-tsgatewayconnectionauthorizationpolicy.md) .

**Windows Server 2008:** Это свойство недоступно.

</dd> <dt>

**Имя**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Имя политики авторизации подключений к удаленному рабочему столу.

</dd> <dt>

**Заказ**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Порядок вычисления политики авторизации подключений к удаленным рабочим столам. Первое вычисление авторизации подключений к удаленному рабочему столу имеет значение "1". Свойство **Order** можно изменить при вызове методов [**CREATE**](create-win32-tsgatewayconnectionauthorizationpolicy.md), [**Delete**](delete-win32-tsgatewayconnectionauthorizationpolicy.md), [**MoveUp**](moveup-win32-tsgatewayconnectionauthorizationpolicy.md)или [**вниз**](movedown-win32-tsgatewayconnectionauthorizationpolicy.md) .

</dd> <dt>

**пассвордалловед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, можно ли использовать пароль для подключения к серверу шлюза удаленных рабочих столов. Это свойство можно изменить с помощью метода [**сетпассвордалловед**](setpasswordallowed-win32-tsgatewayconnectionauthorizationpolicy.md) .

</dd> <dt>

**плугандплайдевицесдисаблед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, будет ли отключено перенаправление устройств самонастраивающийся. Это свойство действует, только если свойство **девицередиректионтипе** имеет значение 2.

</dd> <dt>

**принтерсдисаблед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, будет ли перенаправление принтера отключено. Это свойство действует, только если свойство **девицередиректионтипе** имеет значение 2.

</dd> <dt>

**секуреидалловед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, можно ли использовать безопасный идентификатор для подключения к серверу шлюза удаленных рабочих столов.

**Windows Server 2008:** Это свойство не используется.

</dd> <dt>

**сериалпортсдисаблед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, будет ли перенаправление последовательного порта отключено. Это свойство действует, только если свойство **девицередиректионтипе** имеет значение 2.

</dd> <dt>

**SessionTimeout**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Значение времени ожидания сеанса в минутах. Значение 0 означает отсутствие времени ожидания. Это свойство можно задать с помощью метода [**сетсессионтимеаут**](setsessiontimeout-win32-tsgatewayconnectionauthorizationpolicy.md) .

**Windows Server 2008:** Это свойство недоступно.

</dd> <dt>

**сессионтимеаутактион**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Задает действие, выполняемое в случае истечения времени ожидания сеанса. Это свойство можно задать с помощью метода [**сетсессионтимеаут**](setsessiontimeout-win32-tsgatewayconnectionauthorizationpolicy.md) .

Это может быть одно из следующих значений.

**Windows Server 2008:** Это свойство недоступно.

<dt>

0
</dt> <dd>

Отключите сеанс.

</dd> <dt>

1
</dt> <dd>

Попытка повторно авторизовать сеанс.

</dd> </dl>

</dd> <dt>

**смарткардалловед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, можно ли использовать смарт-карту для подключения к серверу шлюза удаленных рабочих столов. Это свойство можно изменить с помощью метода [**сетсмарткардалловед**](setsmartcardallowed-win32-tsgatewayconnectionauthorizationpolicy.md) .

</dd> <dt>

**усерграупнамес**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Список имен групп пользователей, разделенных точкой с запятой. Имена имеют формат *домена \\ усерграупнаме*. Если пользователь принадлежит к любой из этих групп пользователей, ему будет разрешен доступ к серверу шлюза удаленных рабочих столов.

</dd> </dl>

## <a name="remarks"></a>Remarks

Для использования этого класса необходимо быть членом группы администраторов.

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

[**\_Тсгатевайконнектион Win32**](win32-tsgatewayconnection.md)
</dt> <dt>

[**\_Тсгатевайлоадбаланцер Win32**](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[**\_Тсгатевайрадиуссервер Win32**](win32-tsgatewayradiusserver.md)
</dt> <dt>

[**\_Тсгатевайресаурцеаусоризатионполици Win32**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[**\_Тсгатевайресаурцеграуп Win32**](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[**\_Тсгатевайсерверсеттингс Win32**](win32-tsgatewayserversettings.md)
</dt> </dl>

 


---
title: Класс Win32_TSGatewayServerSettings
description: Предоставляет методы и свойства для просмотра и настройки параметров сервера шлюза удаленный рабочий стол (шлюза удаленных рабочих столов).
ms.assetid: f772bf71-68ef-4345-8123-f6ad50ee4d61
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSGatewayServerSettings службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSGatewayServerSettings, описание
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings.MaxConnections
- Win32_TSGatewayServerSettings.UnlimitedConnections
- Win32_TSGatewayServerSettings.MaximumAllowedConnectionsBySku
- Win32_TSGatewayServerSettings.SkuName
- Win32_TSGatewayServerSettings.MaxProtocols
- Win32_TSGatewayServerSettings.MaxLogEvents
- Win32_TSGatewayServerSettings.adminMessageText
- Win32_TSGatewayServerSettings.adminMessageStartTime
- Win32_TSGatewayServerSettings.adminMessageEndTime
- Win32_TSGatewayServerSettings.consentMessageText
- Win32_TSGatewayServerSettings.OnlyConsentCapableClients
- Win32_TSGatewayServerSettings.CentralCAPEnabled
- Win32_TSGatewayServerSettings.RequestSOH
- Win32_TSGatewayServerSettings.AuthenticationPluginName
- Win32_TSGatewayServerSettings.AuthenticationPluginCLSID
- Win32_TSGatewayServerSettings.AuthenticationPluginDescription
- Win32_TSGatewayServerSettings.AuthorizationPluginName
- Win32_TSGatewayServerSettings.AuthorizationPluginCLSID
- Win32_TSGatewayServerSettings.AuthorizationPluginDescription
- Win32_TSGatewayServerSettings.SslBridging
- Win32_TSGatewayServerSettings.IsConfigured
- Win32_TSGatewayServerSettings.CertHash
- Win32_TSGatewayServerSettings.EnforceChannelBinding
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00c199b4b8e98832dcc8dbe65b8fc2ef636df71c8bd6e3c096670e6333f83a75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008524"
---
# <a name="win32_tsgatewayserversettings-class"></a>\_Класс Win32 тсгатевайсерверсеттингс

Предоставляет методы и свойства для просмотра и настройки параметров сервера шлюза удаленный рабочий стол (шлюза удаленных рабочих столов). Администратор может использовать этот класс для настройки набора протоколов, набора событий, которые будут записываться в журнал событий, и максимального числа подключений через шлюз удаленных рабочих столов.

## <a name="syntax"></a>Синтаксис

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayServerSettings
{
  uint32  MaxConnections;
  boolean UnlimitedConnections;
  uint32  MaximumAllowedConnectionsBySku;
  string  SkuName;
  uint32  MaxProtocols;
  uint32  MaxLogEvents;
  string  adminMessageText;
  string  adminMessageStartTime;
  string  adminMessageEndTime;
  string  consentMessageText;
  boolean OnlyConsentCapableClients;
  boolean CentralCAPEnabled;
  boolean RequestSOH;
  string  AuthenticationPluginName;
  string  AuthenticationPluginCLSID;
  string  AuthenticationPluginDescription;
  string  AuthorizationPluginName;
  string  AuthorizationPluginCLSID;
  string  AuthorizationPluginDescription;
  uint32  SslBridging;
  boolean IsConfigured;
  uint8   CertHash[];
  boolean EnforceChannelBinding;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ тсгатевайсерверсеттингс** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **Win32 \_ тсгатевайсерверсеттингс** содержит следующие методы.



| Метод                                                                                                                                             | Описание                                                                                                                                                                                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Configure**](configure-win32-tsgatewayserversettings.md)                                                                                       | Настраивает параметры IIS и RPC, необходимые для службы шлюза удаленных рабочих столов.<br/> **Windows Server 2008:** этот метод недоступен до Windows Server 2008 R2.<br/>                                                                               |
| [**енаблецентралкап**](enablecentralcap-win32-tsgatewayserversettings.md)                                                                         | Включает или отключает свойство **централкапенаблед** , которое определяет, используются ли центральные серверы политики авторизации удаленный рабочий стол подключений (RD CAP) для управления политиками авторизации подключений для этого сервера.<br/>                    |
| [**енаблеложевент**](enablelogevent-win32-tsgatewayserversettings.md)                                                                             | Включает или отключает ведение журнала для указанного типа событий.<br/>                                                                                                                                                                                              |
| [**енаблеонликонсенткапаблеклиентс**](enableonlyconsentcapableclients-win32-tsgatewayserversettings.md)                                           | Задает свойство **онликонсенткапаблеклиентс** .<br/> **Windows Server 2008:** этот метод недоступен до Windows Server 2008 R2.<br/>                                                                                                      |
| [**енаблерекуестсох**](win32-tsgatewayserversettings-enablerequestsoh.md)                                                                         | Этот метод не поддерживается начиная с Windows Server 2016.<br/> **Windows Server 2012 r2, Windows Server 2012, Windows server 2008 r2 и Windows Server 2008:** Включает или отключает запросы состояния работоспособности (SoH).<br/> <br/> |
| [**енаблетранспорт**](enabletransport-win32-tsgatewayserversettings.md)                                                                           | Включает или отключает указанный транспорт.<br/> **Windows server 2008 R2 и Windows server 2008:** Этот метод недоступен до Windows Server 2012.<br/>                                                                                  |
| [**енумаусентикатионплугинс**](enumauthenticationplugins-win32-tsgatewayserversettings.md)                                                       | Перечисляет все зарегистрированные подключаемые модули проверки подлинности.<br/> **Windows Server 2008:** Этот метод недоступен.<br/>                                                                                                                                  |
| [**енумаусоризатионплугинс**](enumauthorizationplugins-win32-tsgatewayserversettings.md)                                                         | Перечисляет все зарегистрированные подключаемые модули авторизации.<br/> **Windows Server 2008:** этот метод недоступен до Windows Server 2008 R2.<br/>                                                                                                     |
| [**жетипандпорт**](getipandport-win32-tsgatewayserversettings.md)                                                                                 | Получает IP-адрес прослушивания и номер порта для указанного транспорта.<br/> **Windows server 2008 R2 и Windows server 2008:** Этот метод недоступен до Windows Server 2012.<br/>                                                 |
| [**жетложевентнаме**](getlogeventname-win32-tsgatewayserversettings.md)                                                                           | Возвращает имя события журнала для указанного индекса событий журнала.<br/>                                                                                                                                                                                         |
| [**жетпротоколнаме**](getprotocolname-win32-tsgatewayserversettings.md)                                                                           | Возвращает имя протокола для указанного индекса протокола.<br/>                                                                                                                                                                                           |
| [**исложевентенаблед**](islogeventenabled-win32-tsgatewayserversettings.md)                                                                       | Указывает, включен ли указанный тип журнала событий.<br/>                                                                                                                                                                                            |
| [**истранспортенаблед**](istransportenabled-win32-tsgatewayserversettings.md)                                                                     | Определяет, включен ли указанный транспорт.<br/> **Windows server 2008 R2 и Windows server 2008:** Этот метод недоступен до Windows Server 2012.<br/>                                                                        |
| [**куерицертконтекст**](win32-tsgatewayserversettings-querycertcontext.md)                                                                         | Указывает, установлен ли указанный сертификат.<br/>                                                                                                                                                                                             |
| [**рециклерпкаппликатионпулс**](recyclerpcapplicationpools-win32-tsgatewayserversettings.md)                                                     | Повторное использование пулов приложений RPC в службах IIS.<br/> **Windows Server 2008:** этот метод недоступен до Windows Server 2008 R2.<br/>                                                                                                            |
| [**рефрешцертконтекст**](win32-tsgatewayserversettings-refreshcertcontext.md)                                                                     | Обновляет сертификат, используемый сервером шлюза удаленных рабочих столов.<br/>                                                                                                                                                                                      |
| [**сетаусентикатионплугин**](setauthenticationplugin-win32-tsgatewayserversettings.md)                                                           | Задает текущий подключаемый модуль проверки подлинности для сервера шлюза удаленных рабочих столов.<br/> **Windows Server 2008:** этот метод недоступен до Windows Server 2008 R2.<br/>                                                                                    |
| [**сетаусентикатионплугинандрециклерпкаппликатионпулс**](setauthenticationpluginandrecyclerpcapplicationpools-win32-tsgatewayserversettings.md) | Задает текущий подключаемый модуль проверки подлинности для сервера шлюза удаленных рабочих столов и выполняет повторный запуск пулов приложений RPC в службах IIS.<br/> **Windows Server 2008:** этот метод недоступен до Windows Server 2008 R2.<br/>                                      |
| [**сетаусоризатионплугин**](setauthorizationplugin-win32-tsgatewayserversettings.md)                                                             | Задает текущий подключаемый модуль авторизации для сервера шлюза удаленных рабочих столов.<br/> **Windows Server 2008:** этот метод недоступен до Windows Server 2008 R2.<br/>                                                                                     |
| [**сетцертификате**](setcertificate-win32-tsgatewayserversettings.md)                                                                             | Задает хэш сертификата для привязки HTTPS через порт 443 в IIS.<br/> **Windows Server 2008:** этот метод недоступен до Windows Server 2008 R2.<br/>                                                                                       |
| [**сетцертификатеакл**](setcertificateacl-win32-tsgatewayserversettings.md)                                                                       | Задает списки управления доступом (ACL) сертификатов для этого сервера.<br/>                                                                                                                                                                                     |
| [**сетдефаултплугинсандрециклерпкаппликатионпулс**](setdefaultpluginsandrecyclerpcapplicationpools-win32-tsgatewayserversettings.md)             | Задает текущие подключаемые модули проверки подлинности и авторизации для сервера шлюза удаленных рабочих столов и выполняет повторный запуск пулов приложений RPC в службах IIS.<br/> **Windows Server 2008:** этот метод недоступен до Windows Server 2008 R2.<br/>                   |
| [**сетенфорцечаннелбиндинг**](setenforcechannelbinding-win32-tsgatewayserversettings.md)                                                         | Задает свойство **енфорцечаннелбиндинг** .<br/> **Windows server 2008 R2 и Windows server 2008:** Этот метод недоступен до Windows Server 2012.<br/>                                                                                  |
| [**сетипандпорт**](setipandport-win32-tsgatewayserversettings.md)                                                                                 | Задает IP-адрес прослушивания и номер порта для указанного транспорта.<br/> **Windows server 2008 R2 и Windows server 2008:** Этот метод недоступен до Windows Server 2012.<br/>                                                    |
| [**сетмаксконнектионс**](setmaxconnections-win32-tsgatewayserversettings.md)                                                                       | Задает максимальное число разрешенных подключений через шлюз удаленных рабочих столов. Этот метод изменяет свойства **MaxConnections** и **унлимитедконнектионс** .<br/>                                                                                                |
| [**сетсслбридгинг**](setsslbridging-win32-tsgatewayserversettings.md)                                                                             | Задает тип моста SSL, который будет использоваться сервером шлюза удаленных рабочих столов.<br/> **Windows Server 2008:** этот метод недоступен до Windows Server 2008 R2.<br/>                                                                                    |
| [**тсгремовеадминмсг**](tsgremoveadminmsg-win32-tsgatewayserversettings.md)                                                                       | Удаляет административное сообщение для сервера шлюза.<br/> **Windows Server 2008:** этот метод недоступен до Windows Server 2008 R2.<br/>                                                                                            |
| [**тсгремовеконсентмсг**](tsgremoveconsentmsg-win32-tsgatewayserversettings.md)                                                                   | Удаляет административное сообщение для сервера шлюза.<br/> **Windows Server 2008:** этот метод недоступен до Windows Server 2008 R2.<br/>                                                                                            |
| [**тсгстореадминмсг**](tsgstoreadminmsg-win32-tsgatewayserversettings.md)                                                                         | Обновляет административное сообщение для сервера шлюза.<br/> **Windows Server 2008:** этот метод недоступен до Windows Server 2008 R2.<br/>                                                                                            |
| [**тсгстореконсентмсг**](tsgstoreconsentmsg-win32-tsgatewayserversettings.md)                                                                     | Обновляет сообщение согласия для сервера шлюза.<br/> **Windows Server 2008:** этот метод недоступен до Windows Server 2008 R2.<br/>                                                                                                   |



 

### <a name="properties"></a>Свойства

Класс **Win32 \_ тсгатевайсерверсеттингс** имеет следующие свойства.

<dl> <dt>

**админмессажеендтиме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Время окончания административного сообщения.

**Windows Server 2008:** это свойство недоступно до Windows Server 2008 R2.

</dd> <dt>

**админмессажестарттиме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Время начала административного сообщения.

**Windows Server 2008:** это свойство недоступно до Windows Server 2008 R2.

</dd> <dt>

**админмессажетекст**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Текст административного сообщения.

**Windows Server 2008:** это свойство недоступно до Windows Server 2008 R2.

</dd> <dt>

**аусентикатионплугинклсид**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Идентификатор CLSID текущего подключаемого модуля проверки подлинности.

**Windows Server 2008:** это свойство недоступно до Windows Server 2008 R2.

</dd> <dt>

**аусентикатионплугиндескриптион**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Описание текущего подключаемого модуля проверки подлинности.

**Windows Server 2008:** это свойство недоступно до Windows Server 2008 R2.

</dd> <dt>

**аусентикатионплугиннаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя текущего подключаемого модуля проверки подлинности.

**Windows Server 2008:** это свойство недоступно до Windows Server 2008 R2.

</dd> <dt>

**аусоризатионплугинклсид**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Идентификатор CLSID текущего подключаемого модуля авторизации.

**Windows Server 2008:** это свойство недоступно до Windows Server 2008 R2.

</dd> <dt>

**аусоризатионплугиндескриптион**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Описание текущего подключаемого модуля авторизации.

**Windows Server 2008:** это свойство недоступно до Windows Server 2008 R2.

</dd> <dt>

**аусоризатионплугиннаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя текущего подключаемого модуля авторизации.

**Windows Server 2008:** это свойство недоступно до Windows Server 2008 R2.

</dd> <dt>

**централкапенаблед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, используются ли центральные серверы ограниченного использования удаленных рабочих столов для управления этим сервером. Это свойство можно изменить, вызвав метод [**енаблецентралкап**](enablecentralcap-win32-tsgatewayserversettings.md) .

</dd> <dt>

**CertHash**
</dt> <dd> <dl> <dt>

Тип данных: массив **Uint8**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает хэш сертификата для привязки HTTPS через порт 443 в службах IIS.

**Windows Server 2008:** это свойство недоступно до Windows Server 2008 R2.

</dd> <dt>

**консентмессажетекст**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Текст сообщения согласия.

**Windows Server 2008:** это свойство недоступно до Windows Server 2008 R2.

</dd> <dt>

**енфорцечаннелбиндинг**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, применяется ли привязка канала для транспорта HTTP. Это значение свойства можно изменить с помощью метода [**сетенфорцечаннелбиндинг**](setenforcechannelbinding-win32-tsgatewayserversettings.md) .

**Windows server 2008 R2 и Windows server 2008:** Это свойство недоступно до Windows Server 2012.

</dd> <dt>

**Флажка IsConfigured**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, настроены ли параметры IIS и RPC, необходимые для службы шлюза удаленных рабочих столов.

**Windows Server 2008:** это свойство недоступно до Windows Server 2008 R2.

</dd> <dt>

**MaxConnections**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Возвращает максимальное число подключений, разрешенных через шлюз удаленных рабочих столов. Это свойство можно задать с помощью метода [**сетмаксконнектионс**](setmaxconnections-win32-tsgatewayserversettings.md) .

</dd> <dt>

**максимумалловедконнектионсбиску**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Максимальное число подключений, разрешенное модулем хранения запасов (SKU).

</dd> <dt>

**максложевентс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возвращает максимальное число событий журнала.

</dd> <dt>

**макспротоколс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Число протоколов, поддерживаемых шлюзом удаленных рабочих столов.

</dd> <dt>

**онликонсенткапаблеклиентс**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, разрешено ли подключение к шлюзу удаленных рабочих столов только клиентам, которым могут быть предоставлены сообщения согласия.

**Windows Server 2008:** это свойство недоступно до Windows Server 2008 R2.

<dt>

отличные
</dt> <dd>

Подключаться могут только клиенты, поддерживающие сообщения согласия.

</dd> <dt>

нуль
</dt> <dd>

Клиенты, не поддерживающие сообщение согласия, могут также подключаться.

</dd> </dl>

</dd> <dt>

**рекуестсох**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Это свойство не поддерживается начиная с Windows Server 2016.

* * Windows Server 2012 R2, Windows Server 2012, Windows server 2008 r2 и Windows Server 2008: * *

Указывает, должен ли сервер запросить состояние работоспособности (SoH) от клиента. Это свойство можно изменить с помощью метода [**енаблерекуестсох**](win32-tsgatewayserversettings-enablerequestsoh.md) .

</dd> <dt>

**SkuName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя SKU.

</dd> <dt>

**сслбридгинг**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает тип моста SSL, который будет использоваться сервером шлюза удаленных рабочих столов. Это может быть одно из следующих значений.

**Windows Server 2008:** это свойство недоступно до Windows Server 2008 R2.

<dt>

0
</dt> <dd>

Мост SSL отсутствует.

</dd> <dt>

1
</dt> <dd>

Мост HTTPS для HTTP.

</dd> <dt>

2
</dt> <dd>

Мост HTTPS для HTTPS.

</dd> </dl>

</dd> <dt>

**унлимитедконнектионс**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, разрешено ли неограниченное число подключений через шлюз удаленных рабочих столов. Это свойство можно задать с помощью метода [**сетмаксконнектионс**](setmaxconnections-win32-tsgatewayserversettings.md) .

</dd> </dl>

## <a name="remarks"></a>Remarks

Для использования этого класса необходимо быть членом группы администраторов.

файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). файлы MOF не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows Software Development Kit (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                           |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Тсгатевайконнектион Win32**](win32-tsgatewayconnection.md)
</dt> <dt>

[**\_Тсгатевайконнектионаусоризатионполици Win32**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[**\_Тсгатевайлоадбаланцер Win32**](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[**\_Тсгатевайрадиуссервер Win32**](win32-tsgatewayradiusserver.md)
</dt> <dt>

[**\_Тсгатевайресаурцеаусоризатионполици Win32**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[**\_Тсгатевайресаурцеграуп Win32**](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 


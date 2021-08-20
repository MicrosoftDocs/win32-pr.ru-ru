---
title: Класс ReplicationProvider1
description: Базовый класс для экземпляра поставщика.
ms.assetid: c3c6efda-faa7-42af-a635-060967fdcc35
ms.tgt_platform: multiple
keywords:
- Active Directory класса ReplicationProvider1
- Active Directory класс ReplicationProvider1, описание
topic_type:
- apiref
api_name:
- ReplicationProvider1
- ReplicationProvider1.ClientLoadableCLSID
- ReplicationProvider1.CLSID
- ReplicationProvider1.Concurrency
- ReplicationProvider1.DefaultMachineName
- ReplicationProvider1.Enabled
- ReplicationProvider1.ImpersonationLevel
- ReplicationProvider1.InitializationReentrancy
- ReplicationProvider1.InitializationTimeoutInterval
- ReplicationProvider1.InitializeAsAdminFirst
- ReplicationProvider1.Name
- ReplicationProvider1.OperationTimeoutInterval
- ReplicationProvider1.PerLocaleInitialization
- ReplicationProvider1.PerUserInitialization
- ReplicationProvider1.Pure
- ReplicationProvider1.SecurityDescriptor
- ReplicationProvider1.SupportsExplicitShutdown
- ReplicationProvider1.SupportsExtendedStatus
- ReplicationProvider1.SupportsQuotas
- ReplicationProvider1.SupportsSendStatus
- ReplicationProvider1.SupportsShutdown
- ReplicationProvider1.SupportsThrottling
- ReplicationProvider1.UnloadTimeout
- ReplicationProvider1.Version
- ReplicationProvider1.HostingModel
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3e8ca70d2bb5f37303c20117ddba59db6950d1dda58779179c6ef08c95abc4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025132"
---
# <a name="replicationprovider1-class"></a>Класс ReplicationProvider1

Базовый класс для экземпляра поставщика.

Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
class ReplicationProvider1 : __Win32Provider
{
  string   ClientLoadableCLSID;
  string   CLSID;
  sint32   Concurrency;
  string   DefaultMachineName;
  boolean  Enabled;
  sint32   ImpersonationLevel = 0;
  sint32   InitializationReentrancy = 0;
  datetime InitializationTimeoutInterval;
  boolean  InitializeAsAdminFirst;
  string   Name;
  datetime OperationTimeoutInterval;
  boolean  PerLocaleInitialization = FALSE;
  boolean  PerUserInitialization = FALSE;
  boolean  Pure = TRUE;
  string   SecurityDescriptor;
  boolean  SupportsExplicitShutdown;
  boolean  SupportsExtendedStatus;
  boolean  SupportsQuotas;
  boolean  SupportsSendStatus;
  boolean  SupportsShutdown;
  boolean  SupportsThrottling;
  datetime UnloadTimeout;
  uint32   Version;
  string   HostingModel;
};
```

## <a name="members"></a>Члены

Класс **ReplicationProvider1** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **ReplicationProvider1** имеет следующие свойства.

<dl> <dt>

**клиентлоадаблеклсид**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Идентификатор класса, используемый WMI для определения необходимости загрузки высокопроизводительного поставщика в клиентский процесс или в процесс WMI. Если поставщик и клиент расположены на одном компьютере, WMI загружает поставщик в процессе в клиенте с помощью **клиентлоадаблеклсид** в качестве идентификатора класса. Когда поставщик и клиент расположены на разных компьютерах, Инструментарий WMI загружает поставщик в службу WMI. Инструментарий WMI также использует **клиентлоадаблеклсид** для поддержки операций обновления.

Дополнительные сведения см [. в разделе Регистрация поставщика High-Performance.](/windows/desktop/WmiSdk/registering-a-high-performance-provider)

Это свойство наследуется от [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**ЭТОМУ**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Идентификатор **GUID** , представляющий идентификатор класса (**CLSID**) COM-объекта поставщика. Этот COM-объект должен содержать реализацию интерфейса [**ивбемпровидеринит**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) .

Это свойство наследуется от [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**Параллелизм**
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Не используется.

Это свойство наследуется от [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**дефаултмачиненаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Определяет компьютер, на котором будет запущен поставщик. Если поставщик запущен на локальном компьютере, он имеет **значение NULL**.

Это свойство наследуется от [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**Включен**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Если **значение — true**, этот экземпляр включен и может использоваться для выполнения клиентских запросов.

Это свойство наследуется от [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**хостингмодел**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("хостингмодел")
</dt> </dl>

Содержит модель размещения поставщика.

</dd> <dt>

**ImpersonationLevel**
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Зарезервировано. Значение по умолчанию равно нулю (0).

Это свойство наследуется от [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**инитиализатионринтранци**
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Набор флагов, предоставляющих сведения о сериализации. Значение по умолчанию равно нулю (0).

Это свойство наследуется от [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

<dt>

<span id="0"></span>

<span id="0"></span>**0,0**


</dt> <dd>

Все инициализации этого поставщика должны быть сериализованы.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Все инициализации этого поставщика в одном пространстве имен должны быть сериализованы.

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Сериализация инициализации не требуется.

</dd> </dl>

</dd> <dt>

**инитиализатионтимеаутинтервал**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Не используется.

Это свойство наследуется от [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**инитиализеасадминфирст**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

**Windows Server 2003:** Это свойство отключено.

Это свойство наследуется от [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**Имя**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Имя поставщика.

Это свойство наследуется от [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**оператионтимеаутинтервал**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Не используется.

Это свойство наследуется от [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**перлокалеинитиализатион**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Если **значение — true**, поставщик инициализируется для каждого языкового стандарта, когда пользователь соединяется с одним и тем же пространством имен более одного раза, используя разные языковые стандарты. Значение по умолчанию — **FALSE**.

Это свойство наследуется от [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**перусеринитиализатион**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Если **значение — true**, поставщик инициализируется один раз для каждого пользователя NT LAN Manager (NTLM), который выполняет запросы к поставщику. Если **значение равно false** (по умолчанию), поставщик инициализируется один раз для всех пользователей.

Это свойство наследуется от [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**Чистый**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Если **значение — true**, поставщик соглашается подготовиться к выгрузке путем вызова метода [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) для всех необработанных точек интерфейса, когда WMI вызывает метод **Release** своего основного интерфейса. Поставщики, которые должны оставаться клиентами инструментария WMI после того, как они не работают, так как поставщики должны задать для **чистого** значения **false**. Значение по умолчанию — **true**. Дополнительные сведения см. в подразделе «Примечания» этого раздела.

Это свойство наследуется от [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**SecurityDescriptor**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Дескриптор безопасности (SD) в языке определения дескрипторов безопасности (SDDL), определяющий набор пользователей, которые могут успешно вызывать [**ивбемдекаупледрегистрар: Register**](/windows/desktop/api/wbemprov/nf-wbemprov-iwbemdecoupledregistrar-register) для несвязанного поставщика. дополнительные сведения см. в разделе о [языке определения дескрипторов безопасности](/windows/desktop/SecAuthZ/security-descriptor-definition-language) в разделе "безопасность" Windows SDK. Этот дескриптор безопасности используется только для несвязанных поставщиков и не влияет на других поставщиков. Дополнительные сведения см. [в разделе Включение поставщика в приложение](/windows/desktop/WmiSdk/incorporating-a-provider-in-an-application).

Инструментарий WMI выполняет проверки доступа для несвязанных поставщиков, использующих интерфейсы [**ивбемпровидеринит**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) и [**ивбемобжектсинк**](/windows/desktop/WmiSdk/iwbemobjectsink) . Если дескриптор безопасности имеет **значение NULL**, то для запуска несвязанного поставщика могут использоваться только приложения или службы, работающие под учетными записями LocalSystem, NetworkService, LocalService.

В следующей строке показан несвязанный поставщик, который будет запускаться только встроенными администраторами». О:БАГ: ОШИБКА: (A;; 0 x1;;; Ба) "

Дополнительные сведения о настройке свойства **SecurityDescriptor** см. в разделе [обслуживание безопасности WMI](/windows/desktop/WmiSdk/maintaining-wmi-security).

Это свойство наследуется от [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**суппортсексплиЦитшутдовн**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Не используется.

Это свойство наследуется от [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**суппортсекстендедстатус**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Не используется.

Это свойство наследуется от [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**суппортскуотас**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Не используется.

Это свойство наследуется от [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**суппортссендстатус**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Не используется.

Это свойство наследуется от [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**суппортсшутдовн**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Не используется.

Это свойство наследуется от [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**суппортссроттлинг**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Не используется.

Это свойство наследуется от [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**унлоадтимеаут**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

[Формат даты и времени](/windows/desktop/WmiSdk/date-and-time-format) , указывающий, как долго WMI позволяет поставщику оставаться в состоянии простоя перед выгрузкой. Как правило, поставщики запрашивают, что инструментарий WMI ожидает не более пяти минут.

Для текущей версии инструментария WMI значение этого свойства игнорируется. Инструментарий WMI выгружает поставщик на основе значения времени ожидания во внутреннем классе \\ корневого пространства имен. Рекомендуется, чтобы поставщики установили **унлоадтимеаут**. Дополнительные сведения см. [в разделе выгрузка поставщика](/windows/desktop/WmiSdk/unloading-a-provider).

Это свойство наследуется от [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Версия поставщика. Поддерживаемые версии: 1 и 2. Версия 2 повысит проверку достоверности для всех связанных регистраций свойств, в частности свойство [**имперсонатионлевел**](/windows/desktop/WmiSdk/swbemsecurity-impersonationlevel) .

Это свойство наследуется от [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> </dl>

## <a name="remarks"></a>Remarks

Экземпляр этого класса представляет поставщик WMI для служб домен Active Directory. По умолчанию используются следующие параметры.

-   Name = "ReplProv1"
-   ClsID = "{29288F43-39B1-40db-B41F-CE899450E911}"
-   Хостингмодел = "Нетворксервицехост"

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ микрософтактиведиректори<br/>                                               |
| MOF<br/>                      | <dl> <dt>Replprov. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Replprov.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider)
</dt> </dl>

 


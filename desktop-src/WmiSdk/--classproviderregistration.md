---
description: Регистрирует поставщики классов в WMI.
ms.assetid: 1af7d9ed-c5e4-47e4-839d-53d579ef7cea
ms.tgt_platform: multiple
title: Класс __ClassProviderRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ClassProviderRegistration
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 945f0dcde3568ea6d1a6bc89c583f49919a463abf228121515367df95efc77c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117926337"
---
# <a name="__classproviderregistration-class"></a>\_\_Класс Класспровидеррегистратион

Класс System **\_ \_ класспровидеррегистратион** регистрирует поставщики классов в WMI.

Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
class __ClassProviderRegistration : __ObjectProviderRegistration
{
  boolean        SupportsBatching;
  datetime       CacheRefreshInterval;
  sint32         InteractionType = 0;
  __Provider REF provider;
  boolean        PerUserSchema;
  string         QuerySupportLevels[];
  string         ReferencedSetQueries[];
  string         ResultSetQueries[];
  boolean        ReSynchroniseOnNamespaceOpen;
  boolean        SuppportsBatching;
  boolean        SupportsEnumeration = False;
  boolean        SupportsDelete = False;
  boolean        SupportsGet = False;
  boolean        SupportsPut = False;
  boolean        SupportsTransactions;
  string         UnsupportedQueries[];
  uint32         Version;
};
```

## <a name="members"></a>Члены

Класс **\_ \_ класспровидеррегистратион** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **\_ \_ класспровидеррегистратион** имеет следующие свойства.

<dl> <dt>

**качерефрешинтервал**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Не используется.

</dd> <dt>

**интерактионтипе**
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Указывает, передает ли поставщик класса или экземпляра данные или использует WMI и репозиторий модель CIM (CIM). Поставщики услуг извлечения поддерживают динамический доступ к данным, а поставщики push-уведомлений хранят данные в репозитории CIM и используют инструментарий WMI для предоставления доступа к нему. Значение по умолчанию — 0 (нуль). Это свойство наследуется от [**\_ \_ обжектпровидеррегистратион**](--objectproviderregistration.md). Дополнительные сведения см. в разделе [Определение состояния принудительной отправки или извлечения](determining-push-or-pull-status.md).

<dt>

<span id="Pull"></span><span id="pull"></span><span id="PULL"></span>

<span id="Pull"></span><span id="pull"></span><span id="PULL"></span>По **запросу** (0)


</dt> <dd>

Поставщик является поставщиком опрашивающей репликации.

</dd> <dt>

<span id="Push"></span><span id="push"></span><span id="PUSH"></span>

<span id="Push"></span><span id="push"></span><span id="PUSH"></span>**Принудительная отправка** (1)


</dt> <dd>

Поставщик является поставщиком услуг push-уведомлений.

</dd> <dt>

<span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>

<span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>**Пушверифи** (2)


</dt> <dd>

Поставщик — это поставщик принудительной проверки. Обратите внимание, что в настоящее время поставщики **пушверифи** не поддерживаются.

</dd> </dl>

</dd> <dt>

**перусерсчема**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Не используется.

</dd> <dt>

**поставщики**
</dt> <dd> <dl> <dt>

Тип данных: **\_ \_ поставщик**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Путь к объекту поставщика класса. Это свойство наследуется от [**\_ \_ провидеррегистратион**](--providerregistration.md).

</dd> <dt>

**куерисуппортлевелс**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Массив типов поддержки, реализованных поставщиком для обработки запросов. Это свойство наследуется от [**\_ \_ обжектпровидеррегистратион**](--objectproviderregistration.md). Поставщики классов должны поддерживать хотя бы один тип запросов. Поставщики экземпляров могут установить **куерисуппортлевелс** в **значение NULL** , если они не поддерживают обработку запросов. Поставщики, поддерживающие запросы, реализуют метод [**IWbemServices:: ексеккуерясинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) и устанавливают для этого свойства одно или несколько из следующих значений:

<dt>



 ("WQL: Унариселект")


</dt> <dd></dd> <dt>



 ("WQL: References")


</dt> <dd></dd> <dt>



 ("WQL: соединители")


</dt> <dd></dd> <dt>



 ("WQL: V1ProviderDefined")


</dt> <dd></dd> </dl>

</dd> <dt>

**референцедсеткуериес**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Один или несколько запросов, описывающих набор ссылочных классов, поддерживаемых поставщиком классов. Поставщики, которые могут предоставлять классы ассоциаций, должны содержать по крайней мере один запрос в этом свойстве.

</dd> <dt>

**ресултсеткуериес**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Один или несколько запросов, описывающих набор всех классов, которые могут быть предоставлены поставщиком класса, или надмножество этих классов. Это свойство никогда не указывает подмножество поддерживаемых классов.

</dd> <dt>

**ресинчронисеоннамеспацеопен**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Не используется.

</dd> <dt>

**суппортсбатчинг**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Не используется.

Это свойство наследуется от [**\_ \_ обжектпровидеррегистратион**](--objectproviderregistration.md).

</dd> <dt>

**суппортсделете**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Если **значение — true**, поставщик поддерживает удаление данных. Это свойство наследуется от [**\_ \_ обжектпровидеррегистратион**](--objectproviderregistration.md).

<dt>



 Условия


</dt> <dd>

Поставщик поддерживает удаление классов или экземпляров путем реализации одного из следующих методов [**::D елетеклассасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) (поставщики классов) или [**IWbemServices::D елетеинстанцеасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) (поставщики экземпляров).

</dd> <dt>



 IsFalse


</dt> <dd>

Поставщик не поддерживает удаление данных и возвращает **поставщик WBEM E, \_ \_ \_ не \_ поддерживающий** [**делетеклассасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) или [**делетеинстанцеасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync).

</dd> </dl>

</dd> <dt>

**суппортсенумератион**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Если **значение — true**, поставщик поддерживает перечисление данных. Это свойство наследуется от [**\_ \_ обжектпровидеррегистратион**](--objectproviderregistration.md).

<dt>



 Условия


</dt> <dd>

Поставщик поддерживает перечисление данных путем реализации одного из следующих методов [**IWbemServices:: креатеклассенумасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) (классы поставщиков) или [**IWbemServices:: креатеинстанцеенумасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) (поставщики экземпляров).

</dd> <dt>



 IsFalse


</dt> <dd>

Поставщик не поддерживает перечисление данных и возвращает **поставщик WBEM \_ E \_ , \_ не \_ поддерживающий** [**креатеклассенумасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) или [**креатеинстанцеенумасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync).

</dd> </dl>

</dd> <dt>

**суппортсжет**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Если **значение — true**, то поставщик класса или экземпляра поддерживает извлечение данных. Это свойство наследуется от [**\_ \_ обжектпровидеррегистратион**](--objectproviderregistration.md).

<dt>



 Условия


</dt> <dd>

Поставщик поддерживает получение данных путем реализации [**IWbemServices:: жетобжектасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).

</dd> <dt>



 IsFalse


</dt> <dd>

Поставщик не поддерживает извлечение данных и возвращает **\_ поставщик WBEM E, \_ \_ не \_ поддерживающий** из [**жетобжектасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).

</dd> </dl>

</dd> <dt>

**суппортспут**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Если **значение — true**, то поставщик класса или экземпляра поддерживает изменение данных. Это свойство наследуется от [**\_ \_ обжектпровидеррегистратион**](--objectproviderregistration.md).

<dt>



 Условия


</dt> <dd>

Поставщик поддерживает изменение класса или экземпляра путем реализации одного из следующих методов [**::P утклассасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (поставщики классов) или [**IWbemServices::P утинстанцеасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (поставщики классов).

</dd> <dt>



 IsFalse


</dt> <dd>

Поставщик не поддерживает изменение данных и возвращает **\_ поставщик WBEM E, \_ \_ не \_ поддерживающий** [**путклассасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) или [**путинстанцеасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).

</dd> </dl>

</dd> <dt>

**SupportsTransactions**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Не используется.

</dd> <dt>

**супппортсбатчинг**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Не используется.

</dd> <dt>

**унсуппортедкуериес**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Один или несколько запросов, описывающих набор классов, которые не поддерживаются поставщиком класса. Это свойство используется для вычитания из набора классов, подразумеваемых **ресултсеткуериес**.

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Версия этого поставщика класса.

</dd> </dl>

## <a name="remarks"></a>Remarks

Класс **\_ \_ класспровидеррегистратион** является производным от [**\_ \_ обжектпровидеррегистратион**](--objectproviderregistration.md), который является производным от [**\_ \_ провидеррегистратион**](--providerregistration.md).

Свойства, наследуемые от [**\_ \_ обжектпровидеррегистратион**](--objectproviderregistration.md) , указывают, поддерживает ли поставщик класса получение, изменение, удаление, перечисление и обработку запросов. Свойство **интерактионтипе** указывает, предназначен ли поставщик класса в качестве поставщика Pull или Push-уведомления. Дополнительные сведения см. в разделе [Определение состояния принудительной отправки или извлечения](determining-push-or-pull-status.md).

Класс [**\_ \_ провидеррегистратион**](--providerregistration.md) определяет свойство [**provider**](/windows/desktop/api/Provider/nl-provider-provider) . Только администраторы могут зарегистрировать поставщик, создав экземпляр [**\_ \_ Win32Provider**](--win32provider.md) и **\_ \_ класспровидеррегистратион**. Только администраторы могут удалить поставщика.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>       |
| Минимальная версия сервера<br/> | Windows Server 2008<br/> |
| Пространство имен<br/>                | Все пространства имен WMI<br/>  |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_\_обжектпровидеррегистратион**](/windows/desktop/WmiSdk/--objectproviderregistration)
</dt> <dt>

[Системные классы WMI](wmi-system-classes.md)
</dt> <dt>

[Регистрация поставщика класса](registering-a-class-provider.md)
</dt> <dt>

[Регистрация поставщика экземпляра](registering-an-instance-provider.md)
</dt> <dt>

[**\_\_Win32Provider**](--win32provider.md)
</dt> </dl>

 


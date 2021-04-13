---
description: Выступает в качестве родительского класса для классов, которые используются для регистрации поставщиков классов и экземпляров в WMI.
ms.assetid: f7c569be-8927-42a4-b96a-abe4b7e3e23c
ms.tgt_platform: multiple
title: Класс __ObjectProviderRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ObjectProviderRegistration
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
ms.openlocfilehash: a60b24278fb235cec38c127e7ebbbb481e49a140
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104345902"
---
# <a name="__objectproviderregistration-class"></a>\_\_Класс Обжектпровидеррегистратион

Абстрактный системный класс **\_ \_ обжектпровидеррегистратион** выступает в качестве родительского класса для классов, которые используются для регистрации поставщиков классов и экземпляров в WMI.

Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[abstract]
class __ObjectProviderRegistration : __ProviderRegistration
{
  sint32         InteractionType = 0;
  __Provider REF provider;
  string         QuerySupportLevels[];
  boolean        SupportsBatching;
  boolean        SupportsDelete = False;
  boolean        SupportsEnumeration = False;
  boolean        SupportsGet = False;
  boolean        SupportsPut = False;
  boolean        SupportsTransactions;
};
```

## <a name="members"></a>Члены

Класс **\_ \_ обжектпровидеррегистратион** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **\_ \_ обжектпровидеррегистратион** имеет следующие свойства.

<dl> <dt>

**интерактионтипе**
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Указывает, предоставляет ли поставщик класса или экземпляра собственные данные или использует WMI и репозиторий модель CIM (CIM). Поставщики услуг извлечения поддерживают динамический доступ к своим данным, а поставщики push-уведомлений хранят свои данные в репозитории CIM и используют инструментарий WMI для предоставления доступа к ним. Дополнительные сведения см. в разделе [Определение состояния принудительной отправки или извлечения](determining-push-or-pull-status.md). Значение по умолчанию — 0 (нуль).

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

Поставщик — это поставщик принудительной проверки. Обратите внимание, что в настоящее время принудительная проверка не поддерживается.

</dd> </dl>

</dd> <dt>

**поставщики**
</dt> <dd> <dl> <dt>

Тип данных: **\_ \_ поставщик**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Ссылка на экземпляр [**\_ \_ поставщика**](--provider.md) , представляющий путь к объекту поставщика объектов. Это свойство наследуется от [**\_ \_ провидеррегистратион**](--providerregistration.md).

</dd> <dt>

**куерисуппортлевелс**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Массив типов поддержки, реализованных поставщиком для обработки запросов. Поставщики классов не поддерживают запросы любого типа. Поставщики экземпляров могут установить **куерисуппортлевелс** в **значение NULL** , если они не поддерживают обработку запросов. Поставщики, поддерживающие запросы, реализуют метод [**IWbemServices:: ексеккуерясинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) и присвойте этому свойству одно или несколько из следующих значений (тип свойства является массивом).

"WQL: Унариселект"

"WQL: References"

"WQL: соединители"

"WQL: V1ProviderDefined"

</dd> <dt>

**суппортсбатчинг**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Не используется.

</dd> <dt>

**суппортсделете**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Если **значение — true**, поставщик поддерживает удаление данных.

<dt>

True
</dt> <dd>

Поставщик поддерживает удаление классов или экземпляров путем реализации одного из следующих методов [**::D елетеклассасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) (поставщики классов) или [**IWbemServices::D елетеинстанцеасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) (поставщики экземпляров).

</dd> <dt>

Неверно
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

Если **значение — true**, поставщик поддерживает перечисление данных.

<dt>

True
</dt> <dd>

Поставщик поддерживает перечисление данных путем реализации одного из следующих методов [**IWbemServices:: креатеклассенумасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) (классы поставщиков) или [**IWbemServices:: креатеинстанцеенумасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) (поставщики экземпляров).

</dd> <dt>

Неверно
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

Если **значение — true**, то поставщик класса или экземпляра поддерживает извлечение данных.

<dt>

True
</dt> <dd>

Поставщик поддерживает получение данных путем реализации [**IWbemServices:: жетобжектасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).

</dd> <dt>

Неверно
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

Если **значение — true**, то поставщик класса или экземпляра поддерживает изменение данных.

<dt>

True
</dt> <dd>

Поставщик поддерживает изменение класса или экземпляра путем реализации одного из следующих методов [**::P утклассасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (поставщики классов) или [**IWbemServices::P утинстанцеасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (поставщики классов).

</dd> <dt>

Неверно
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

</dd> </dl>

## <a name="remarks"></a>Комментарии

Класс **\_ \_ обжектпровидеррегистратион** является производным от [**\_ \_ провидеррегистратион**](--providerregistration.md).

Поставщики классов должны присвоить свойству **Суппортсенумератион** **значение true** , поскольку поставщики должны иметь возможность предоставлять Инструментарий WMI со списком их классов. Если поставщик класса пытается установить это свойство в **значение false**, WMI помечает регистрацию как недопустимую. Поставщики экземпляров не обязательно должны поддерживать перечисление и могут установить для **суппортсенумератион** значение **true** или **false**.

Поставщик, который устанавливает **куерисуппортлевелс** в "WQL: унариселект", может принимать запрос, состоящий из базовой инструкции SELECT, которая поддерживается в WMI версии 1,0. Как поставщик классов, так и поставщики экземпляров должны иметь возможность обрабатывать системное свойство **\_ \_ класса** . Поставщики классов также должны обрабатывать свойство системы **\_ \_ суперкласса** и оператор ISA. Оператор ISA используется для расширения результирующего набора на производные классы. Если поставщику предоставлен запрос, который он не может интерпретировать, он запрашивает его обработку WMI, возвращая **\_ \_ слишком \_ сложное значение ошибки WBEM E** . Описание допустимого синтаксиса WQL см. в разделе [запросы с помощью WQL](querying-with-wql.md).

Поставщик, устанавливающий **куерисуппортлевелс** в **WQL: V1ProviderDefined** , может попытаться поддерживать более крупный набор синтаксиса SQL на своем собственном риске, например в `ORDER BY` предложении. Инструментарий WMI не интерпретирует дополнительные предложения или пытается убедиться в правильности результирующего набора.

Только администраторы могут зарегистрировать или удалить поставщик, создав экземпляр [**\_ \_ Win32Provider**](--win32provider.md) и зарегистрировав его.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>       |
| Минимальная версия сервера<br/> | Windows Server 2008<br/> |
| Пространство имен<br/>                | Все пространства имен WMI<br/>  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_\_провидеррегистратион**](/windows/desktop/WmiSdk/--providerregistration)
</dt> <dt>

[Системные классы WMI](wmi-system-classes.md)
</dt> <dt>

[Регистрация поставщика](registering-a-provider.md)
</dt> </dl>

 


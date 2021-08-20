---
description: Регистрирует поставщиков экземпляров в WMI.
ms.assetid: 6eba9bff-a5b9-4741-94ef-7d65b33d9aff
ms.tgt_platform: multiple
title: Класс __InstanceProviderRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __InstanceProviderRegistration
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
ms.openlocfilehash: 773bb54ec4d132e629f21513ffa617cbe3435d35941e7c98c55810d267f614c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118821159"
---
# <a name="__instanceproviderregistration-class"></a>\_\_Класс Инстанцепровидеррегистратион

Системный класс **\_ \_ инстанцепровидеррегистратион** регистрирует поставщиков экземпляров в WMI.

Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
class __InstanceProviderRegistration : __ObjectProviderRegistration
{
  sint32         InteractionType = 0;
  __Provider REF provider;
  string         QuerySupportLevels[];
  boolean        SupportsBatching;
  boolean        SupportsDelete = False;
  boolean        SupportsEnumeration = True;
  boolean        SupportsGet = False;
  boolean        SupportsPut = False;
  boolean        SupportsTransactions;
};
```

## <a name="members"></a>Члены

Класс **\_ \_ инстанцепровидеррегистратион** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **\_ \_ инстанцепровидеррегистратион** имеет следующие свойства.

<dl> <dt>

**интерактионтипе**
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Указывает, что поставщик класса или экземпляра предоставляет данные или получает данные из WMI и репозитория модель CIM (CIM). Поставщики услуг извлечения поддерживают динамический доступ к своим данным. и поставщики push-уведомлений хранят свои данные в репозитории CIM и используют инструментарий WMI для предоставления доступа к нему. Дополнительные сведения см. в разделе [Определение состояния принудительной отправки или извлечения](determining-push-or-pull-status.md). Значение по умолчанию — 0 (нуль).

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

Поставщик — это поставщик принудительной проверки. Обратите внимание, что в настоящее время поставщики Push-проверки не поддерживаются.

</dd> </dl>

</dd> <dt>

**поставщики**
</dt> <dd> <dl> <dt>

Тип данных: **\_ \_ поставщик**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Ссылка на экземпляр [**\_ \_ поставщика**](--provider.md) , представляющий путь к объекту для поставщика экземпляра. Это свойство наследуется от [**\_ \_ провидеррегистратион**](--providerregistration.md).

</dd> <dt>

**куерисуппортлевелс**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Массив типов поддержки, реализованных поставщиком для обработки запросов. Поставщики классов не поддерживают все типы запросов. Поставщики экземпляров могут установить **куерисуппортлевелс** в **значение NULL** , если они не поддерживают обработку запросов. Поставщики, поддерживающие запросы, реализуют метод [**IWbemServices:: ексеккуерясинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) и присвойте этому свойству одно или несколько из следующих значений.

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

Верно
</dt> <dd>

Поставщик поддерживает удаление классов или экземпляров путем реализации [**IWbemServices::D елетеклассасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) (поставщики классов) или [**IWbemServices::D елетеинстанцеасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) (поставщики экземпляров).

</dd> <dt>

Нет
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

Если **значение — true**, то поставщик класса или экземпляра поддерживает извлечение данных.

<dt>

Верно
</dt> <dd>

Поставщик поддерживает получение данных путем реализации [**IWbemServices:: жетобжектасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).

</dd> <dt>

Нет
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



 Условия


</dt> <dd>

Поставщик поддерживает изменение класса или экземпляра, реализуя один из следующих методов: [**IWbemServices::P утклассасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (поставщики классов) или [**IWbemServices::P утинстанцеасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (поставщики классов).

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

</dd> </dl>

## <a name="remarks"></a>Remarks

Класс **\_ \_ инстанцепровидеррегистратион** является производным от [**\_ \_ обжектпровидеррегистратион**](--objectproviderregistration.md), который является производным от [**\_ \_ провидеррегистратион**](--providerregistration.md). Только администраторы могут зарегистрировать поставщик экземпляра, создав экземпляр [**\_ \_ Win32Provider**](--win32provider.md) и **\_ \_ инстанцепровидеррегистратион**. Только администраторы могут удалить поставщика.

## <a name="requirements"></a>Requirements (Требования)



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
</dt> </dl>

 


---
description: '\_Часовой пояс Win32&\# 8194; Класс WMI представляет сведения о часовом поясе для компьютерной системы под Windows, включая изменения, необходимые для перехода на переход на летнее время.'
ms.assetid: c1c7731e-768f-42ea-a36c-57b00df6848e
ms.tgt_platform: multiple
title: Класс Win32_TimeZone
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_TimeZone
- Win32_TimeZone.Caption
- Win32_TimeZone.Description
- Win32_TimeZone.SettingID
- Win32_TimeZone.Bias
- Win32_TimeZone.DaylightBias
- Win32_TimeZone.DaylightDay
- Win32_TimeZone.DaylightDayOfWeek
- Win32_TimeZone.DaylightHour
- Win32_TimeZone.DaylightMillisecond
- Win32_TimeZone.DaylightMinute
- Win32_TimeZone.DaylightMonth
- Win32_TimeZone.DaylightName
- Win32_TimeZone.DaylightSecond
- Win32_TimeZone.DaylightYear
- Win32_TimeZone.StandardBias
- Win32_TimeZone.StandardDay
- Win32_TimeZone.StandardDayOfWeek
- Win32_TimeZone.StandardHour
- Win32_TimeZone.StandardMillisecond
- Win32_TimeZone.StandardMinute
- Win32_TimeZone.StandardMonth
- Win32_TimeZone.StandardName
- Win32_TimeZone.StandardSecond
- Win32_TimeZone.StandardYear
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 433682f045ca7fb127c7dc69e3a26ed8356371ed
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895785"
---
# <a name="win32_timezone-class"></a>\_Класс часового пояса Win32

 [Класс WMI](../wmisdk/retrieving-a-class.md) **\_ TimeZone для Win32** представляет сведения о часовом поясе для компьютерной системы под Windows, включая изменения, необходимые для перехода на переход на летнее время.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства. Свойства и методы имеют алфавитный порядок, а не порядок MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4EC-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_TimeZone : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  sint32 Bias;
  sint32 DaylightBias;
  uint32 DaylightDay;
  uint8  DaylightDayOfWeek;
  uint32 DaylightHour;
  uint32 DaylightMillisecond;
  uint32 DaylightMinute;
  uint32 DaylightMonth;
  string DaylightName;
  uint32 DaylightSecond;
  uint32 DaylightYear;
  uint32 StandardBias;
  uint32 StandardDay;
  uint8  StandardDayOfWeek;
  uint32 StandardHour;
  uint32 StandardMillisecond;
  uint32 StandardMinute;
  uint32 StandardMonth;
  string StandardName;
  uint32 StandardSecond;
  uint32 StandardYear;
};
```

## <a name="members"></a>Члены

Класс **\_ часового пояса Win32** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **\_ часового пояса Win32** имеет следующие свойства.

<dl> <dt>

**Смещение**
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| времени структуры времени \| [**часового \_ пояса \_**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| "), [**единицы**](../wmisdk/standard-qualifiers.md) ("минуты")
</dt> </dl>

Текущий сдвиг для локального перевода времени. Смещение — это разница между всеобщим скоординированным временем (UTC) и местным временем. Все переводы между временем в формате UTC и местным временем основаны на следующей формуле: UTC = местное время — смещение. Это свойство обязательно.

</dd> <dt>

**Заголовок**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Краткое текстовое описание текущего объекта.

Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).

</dd> <dt>

**дайлигхтбиас**
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры времени Win32API \| [**\_ \_ сведения о часовом поясе**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| дайлигхтбиас"), [**единицы**](../wmisdk/standard-qualifiers.md) ("минуты")
</dt> </dl>

Значение смещения, которое будет использоваться при переводе на летнее время. Это свойство пропускается, если не указано значение свойства **дайлигхтдай** . Значение этого свойства добавляется к свойству " **смещение** " для формирования смещения, используемого во время летнего времени. В большинстве часовых поясов значение этого свойства равно-60.

</dd> <dt>

**дайлигхтдай**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры времени Win32API \| [**\_ \_ сведения о часовом поясе**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| дайлигхтдате \| вдай")
</dt> </dl>

**Дайлигхтдайофвик** **дайлигхтмонс** , когда в этой операционной системе происходит переход со зимнего времени на летнее время.

Пример. Если день перехода (**дайлигхтдайофвик**) происходит в воскресенье, значение "1" обозначает первое воскресенье **дайлигхтмонс**, "2" — второе воскресенье и т. д. Значение «5» обозначает последний **дайлигхтдайофвик** в месяце.

</dd> <dt>

**дайлигхтдайофвик**
</dt> <dd> <dl> <dt>

Тип данных: **Uint8**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры времени Win32API \| [**\_ \_ сведения о часовом поясе**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| дайлигхтдате \| вдайофвик")
</dt> </dl>

День недели, когда переход со зимнего времени на летнее время происходит в операционной системе.

<dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>

**Воскресенье** (0)


</dt> <dd></dd> <dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>

**Понедельник** (1)


</dt> <dd></dd> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>

**Вторник** (2)


</dt> <dd></dd> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>

**Среда** (3)


</dt> <dd></dd> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>

**Четверг** (4)


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

**Пятница** (5)


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

**Суббота** (6)


</dt> <dd></dd> </dl>

Пример: 1

</dd> <dt>

**дайлигхсаур**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры времени Win32API \| [**\_ \_ сведения о часовом поясе**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| дайлигхтдате \| вхаур")
</dt> </dl>

Час дня, когда переход со зимнего времени на летнее время происходит в операционной системе.

Пример: 2

</dd> <dt>

**дайлигхтмиллисеконд**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры времени Win32API \| [**\_ \_ сведения о часовом поясе**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| дайлигхтдате \| вмиллисекондс")
</dt> </dl>

Миллисекунда **дайлигхтсеконд** , когда переход со зимнего времени на летнее время происходит в операционной системе.

</dd> <dt>

**дайлигхтминуте**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры времени Win32API \| [**\_ \_ сведения о часовом поясе**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| дайлигхтдате \| вминуте")
</dt> </dl>

Минута **дайлигхсаур** , когда переход со зимнего времени на летнее время происходит в операционной системе.

Пример: 59

</dd> <dt>

**дайлигхтмонс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры времени Win32API \| [**\_ \_ сведения о часовом поясе**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| дайлигхтдате \| вмонс")
</dt> </dl>

Месяц, когда переход со зимнего времени на летнее время происходит в операционной системе.

<dt>

<span id="January"></span><span id="january"></span><span id="JANUARY"></span>

**Январь** (1)


</dt> <dd></dd> <dt>

<span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>

**Февраль** (2)


</dt> <dd></dd> <dt>

<span id="March"></span><span id="march"></span><span id="MARCH"></span>

**Март** (3)


</dt> <dd></dd> <dt>

<span id="April"></span><span id="april"></span><span id="APRIL"></span>

**Апрель** (4)


</dt> <dd></dd> <dt>

<span id="May"></span><span id="may"></span><span id="MAY"></span>

**Май** (5)


</dt> <dd></dd> <dt>

<span id="June"></span><span id="june"></span><span id="JUNE"></span>

**Июнь** (6)


</dt> <dd></dd> <dt>

<span id="July"></span><span id="july"></span><span id="JULY"></span>

**Июль** (7)


</dt> <dd></dd> <dt>

<span id="August"></span><span id="august"></span><span id="AUGUST"></span>

**Август** (8)


</dt> <dd></dd> <dt>

<span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>

**Сентябрь** (9)


</dt> <dd></dd> <dt>

<span id="October"></span><span id="october"></span><span id="OCTOBER"></span>

**Октябрь** (10)


</dt> <dd></dd> <dt>

<span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>

**Ноябрь** (11)


</dt> <dd></dd> <dt>

<span id="December"></span><span id="december"></span><span id="DECEMBER"></span>

**Декабрь** (12)


</dt> <dd></dd> </dl>

</dd> <dt>

**дайлигхтнаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры времени Win32API \| [**\_ \_ сведения о часовом поясе**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| дайлигхтнаме")
</dt> </dl>

Часовой пояс, который будет представлен, если действует летнее время.

Пример: "EDT" (восточное время (лето))

</dd> <dt>

**дайлигхтсеконд**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры времени Win32API \| [**\_ \_ сведения о часовом поясе**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| дайлигхтдате \| всеконд")
</dt> </dl>

Второй из **дайлигхтминуте** , когда переход со зимнего времени на летнее время происходит в операционной системе.

Пример: 59

</dd> <dt>

**дайлигхтеар**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры времени Win32API \| [**\_ \_ сведения о часовом поясе**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| дайлигхтдате \| ВЕАР")
</dt> </dl>

Год, когда действует летнее время. Это свойство не является обязательным.

Пример: 1997

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Текстовое описание текущего объекта.

Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Идентификатор, по которому известен текущий объект.

Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).

</dd> <dt>

**стандардбиас**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры времени Win32API \| [**\_ \_ сведения о часовом поясе**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| стандардбиас"), [**единицы**](../wmisdk/standard-qualifiers.md) ("минуты")
</dt> </dl>

Значение смещения, используемое, если переход на летнее время не действует. Это свойство игнорируется, если не указано значение для **стандарддай** . Значение этого свойства добавляется к свойству " **смещение** " для формирования смещения во время стандартного времени.

Пример: 0

</dd> <dt>

**стандарддай**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры времени Win32API \| [**\_ \_ сведения о часовом поясе**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| стандарддате \| вдай")
</dt> </dl>

**Стандарддайофвик** **стандардмонс** , когда переход с летнего времени на зимнее время происходит в операционной системе.

Если день перехода (**стандарддайофвик**) происходит в воскресенье, значение "1" обозначает первое воскресенье **стандардмонс**, "2" — второе воскресенье и т. д. Значение «5» обозначает последний **стандарддайофвик** в месяце.

</dd> <dt>

**стандарддайофвик**
</dt> <dd> <dl> <dt>

Тип данных: **Uint8**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры времени Win32API \| [**\_ \_ сведения о часовом поясе**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| стандарддате \| вдайофвик")
</dt> </dl>

День недели, когда переход с летнего времени на зимнее время происходит в операционной системе.

<dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>

**Воскресенье** (0)


</dt> <dd></dd> <dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>

**Понедельник** (1)


</dt> <dd></dd> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>

**Вторник** (2)


</dt> <dd></dd> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>

**Среда** (3)


</dt> <dd></dd> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>

**Четверг** (4)


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

**Пятница** (5)


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

**Суббота** (6)


</dt> <dd></dd> </dl>

</dd> <dt>

**стандардхаур**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры времени Win32API \| [**\_ \_ сведения о часовом поясе**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| стандарддате \| вхаур")
</dt> </dl>

Час дня, когда переход с летнего времени на зимнее время происходит в операционной системе.

Пример: 11

</dd> <dt>

**стандардмиллисеконд**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры времени Win32API \| [**\_ \_ сведения о часовом поясе**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| стандарддате \| вмиллисекондс")
</dt> </dl>

Миллисекунда **стандардсеконд** , когда переход с летнего времени на зимнее время происходит в операционной системе.

</dd> <dt>

**стандардминуте**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры времени Win32API \| [**\_ \_ сведения о часовом поясе**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| стандарддате \| вминуте")
</dt> </dl>

Минута **стандарддай** , когда переход с летнего времени на зимнее время происходит в операционной системе.

Пример: 59

</dd> <dt>

**стандардмонс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры времени Win32API \| [**\_ \_ сведения о часовом поясе**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| стандарддате \| вмонс")
</dt> </dl>

Месяц, когда переход с летнего времени на зимнее время происходит в операционной системе.

<dt>

<span id="January"></span><span id="january"></span><span id="JANUARY"></span>

**Январь** (1)


</dt> <dd></dd> <dt>

<span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>

**Февраль** (2)


</dt> <dd></dd> <dt>

<span id="March"></span><span id="march"></span><span id="MARCH"></span>

**Март** (3)


</dt> <dd></dd> <dt>

<span id="April"></span><span id="april"></span><span id="APRIL"></span>

**Апрель** (4)


</dt> <dd></dd> <dt>

<span id="May"></span><span id="may"></span><span id="MAY"></span>

**Май** (5)


</dt> <dd></dd> <dt>

<span id="June"></span><span id="june"></span><span id="JUNE"></span>

**Июнь** (6)


</dt> <dd></dd> <dt>

<span id="July"></span><span id="july"></span><span id="JULY"></span>

**Июль** (7)


</dt> <dd></dd> <dt>

<span id="August"></span><span id="august"></span><span id="AUGUST"></span>

**Август** (8)


</dt> <dd></dd> <dt>

<span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>

**Сентябрь** (9)


</dt> <dd></dd> <dt>

<span id="October"></span><span id="october"></span><span id="OCTOBER"></span>

**Октябрь** (10)


</dt> <dd></dd> <dt>

<span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>

**Ноябрь** (11)


</dt> <dd></dd> <dt>

<span id="December"></span><span id="december"></span><span id="DECEMBER"></span>

**Декабрь** (12)


</dt> <dd></dd> </dl>

</dd> <dt>

**StandardName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры времени Win32API \| [**\_ \_ сведения о часовом поясе**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardName")
</dt> </dl>

Имя часового пояса, представленного в результате использования стандартного времени.

Пример: "EST" (восточное стандартное время)

</dd> <dt>

**стандардсеконд**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры времени Win32API \| [**\_ \_ сведения о часовом поясе**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| стандарддате \| всеконд")
</dt> </dl>

Второй из **стандардминуте** , когда переход с летнего времени на зимнее время происходит в операционной системе.

Пример: 59

</dd> <dt>

**стандардеар**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры времени Win32API \| [**\_ \_ сведения о часовом поясе**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| стандарддате \| ВЕАР")
</dt> </dl>

Год, когда действует стандартное время. Это свойство не является обязательным.

Пример: 1997

</dd> </dl>

## <a name="remarks"></a>Комментарии

Класс **\_ часового пояса Win32** является производным от [**\_ параметра CIM**](cim-setting.md).

При написании запросов WMI нельзя использовать стандартные форматы даты и времени, например 10/18/2002. Вместо этого необходимо преобразовать все даты, используемые в запросах, в формат UTC. Для этого требуется два шага: 1) необходимо определить смещение (разница в минутах) между часовым поясом и временем по Гринвичу, а 2) необходимо преобразовать 10/18/2002 в значение времени в формате UTC.

Определение смещения относительно среднего времени по Гринвичу

Следует признать, что инструментарий WMI затрудняет работу с датами и временем. к счастью, Инструментарий WMI, как минимум, упрощает определение смещения между часовым поясом и временем по Гринвичу. Часовой пояс Win32 класса WMI \_ включает сдвиг свойства, который возвращает смещение GMT.


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colTimeZone = objSWbemServices.ExecQuery _
 ("SELECT * FROM Win32_TimeZone")
For Each objTimeZone in colTimeZone
 Wscript.Echo "Offset: "& objTimeZone.Bias
Next
```



Преобразование даты в значение в формате UTC

После определения смещения GMT необходимо преобразовать стандартную дату, например 10/18/2002, в дату в формате UTC. Чтобы преобразовать стандартную дату в дату в формате UTC, можно использовать функции даты VBScript, такие как год, месяц и день, чтобы изолировать отдельные компоненты, которые составляют дату в формате UTC. После создания отдельных значений для этих компонентов их можно объединить так же, как и любые другие строковые значения. Даты в формате UTC обрабатываются как строки, так как смещение GMT должно быть добавлено к концу. Если дата показана в виде числа, это значение:

`20011018113047.000000-480`

Будет ошибочно рассматриваться как математическое уравнение (для ясности добавлены круглые скобки):

`(20011018113047.000000) - (480)`

Например, в дате 10/18/2002 отдельные компоненты:

-   Год: 2002
-   Месяц: 10
-   День: 18

Скрипту потребуется объединить эти три значения, строку "113047,000000" (представляющую время, включая миллисекунды) и смещение GMT для получения даты в формате UTC. Например, для ясности добавлены скобки.

`(2002) & (10) & (18) & (113047.000000) & (-480)`

> [!Note]  
> Для преобразования временной части даты в формате UTC можно использовать функции VBScript час, минуту и секунду. Таким образом, такое время, как 11:30:47 утра будет преобразовано в 113047.

 

Существует один усложненный фактор. Месяц должен занимать в строке позиции 5 и 6; день должен занимать 7 и 8 единиц. Это не проблема с 10 и 18-го дня. Но как получить 5 июля (месяц 7, день 5), чтобы заполнить позиции необходимых условий? Ответ заключается в том, чтобы добавить к каждому значению ноль в начале, что приведет к изменению 7 на 07 и 5 на 05.

Для этого используйте функцию "len" языка VBScript, чтобы проверить длину (число символов) в месяце и день. Если длина равна 1 (это означает, что имеется только один символ), добавьте начальный нуль. Следовательно


```VB
If Len(dtmMonth) = 1 Then
    dtmMonth = "0" & dtmMonth
End If
```



## <a name="examples"></a>Примеры

В следующем примере на языке VBScript текущая дата преобразуется в дату в формате UTC.


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colTimeZone = objSWbemServices.ExecQuery _
 ("SELECT * FROM Win32_TimeZone")
For Each objTimeZone in colTimeZone
 strBias = objTimeZone.Bias
Next

dtmCurrentDate = Date
dtmTargetDate = Year(dtmCurrentDate)

dtmMonth = Month(dtmCurrentDate)
If Len(dtmMonth) = 1 Then
 dtmMonth = "0" & dtmMonth
End If

dtmTargetDate = dtmTargetDate & dtmMonth

dtmDay = Day(dtmCurrentDate)
If Len(dtmDay) = 1 Then
 dtmDay = "0" & dtmDay
End If

dtmTargetDate = dtmTargetDate & dtmDay & "000000.000000"
dtmTargetDate = dtmTargetDate & Cstr(strBias)
```



Следующий сценарий VBScript сампледетерминес смещение GMT, а затем преобразует указанную текущую дату (в данном случае 10/18/2002) в формат даты и времени в формате UTC. После преобразования даты это значение используется для поиска компьютера и возвращает список всех папок, созданных после 10/18/2002.


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colTimeZone = objSWbemServices.ExecQuery _
 ("SELECT * FROM Win32_TimeZone")
For Each objTimeZone in colTimeZone
 strBias = objTimeZone.Bias
Next

dtmCurrentDate = "10/18/2002"
dtmTargetDate = Year(dtmCurrentDate)

dtmMonth = Month(dtmCurrentDate)
If Len(dtmMonth) = 1 Then
 dtmMonth = "0" & dtmMonth
End If

dtmTargetDate = dtmTargetDate & dtmMonth

dtmDay = Day(dtmCurrentDate)
If Len(dtmDay) = 1 Then
 dtmDay = "0" & dtmDay
End If

dtmTargetDate = dtmTargetDate & dtmDay & "000000.000000"
dtmTargetDate = dtmTargetDate & Cstr(strBias)

Set colFolders = objSWbemServices.ExecQuery _
 ("SELECT * FROM Win32_Directory WHERE CreationDate < '" & _
 dtmtargetDate & "'")
For Each objFolder in colFolders
 Wscript.Echo objFolder.Name
Next
```



В следующем примере кода VBScript отображаются параметры для \_ экземпляров часового пояса Win32.


```VB
Dim arDayOrWeek(7)
arDayOrWeek(0) = "Sunday"
arDayOrWeek(1) = "Monday"
arDayOrWeek(2) = "Tuesday"
arDayOrWeek(3) = "Wednesday"
arDayOrWeek(4) = "Thursday"
arDayOrWeek(5) = "Friday"
arDayOrWeek(6) = "Saturday"

Dim arMonth(13)
arMonth(1) = "January"
arMonth(2) = "Feburary"
arMonth(3) = "March"
arMonth(4) = "April"
arMonth(5) = "May"
arMonth(6) = "June"
arMonth(7) = "July"
arMonth(8) = "August"
arMonth(9) = "September"
arMonth(10) = "October"
arMonth(11) = "November"
arMonth(12) = "December"

strComputer = "."
wmiQuery = "Select * from Win32_TimeZone"
Set objWMIService = GetObject("winmgmts:\\" & _
    strComputer & "\root\cimv2")
Set colItems = objWMIService.ExecQuery(wmiQuery)

For Each objItem in colItems
    WScript.Echo "Day of Week setting is: " _
        & objItem.dayLightDayOfWeek _
        & " which is: " & arDayOrWeek(objItem.DaylightDayOfWeek)
    WScript.Echo "Hour: " & objItem.DaylightHour 
    WScript.Echo "Month: " & objItem.DaylightMonth _
        & " which is: " & arMonth(objItem.DaylightMonth )
    WScript.Echo "Description: " & objItem.DaylightName 
    WScript.Echo "The transition from DLS to Standard occurs: " 
    WScript.Echo "Day of Week setting is: " _
        & objItem.standardDayOfWeek _
        & " which is: " & arDayOrWeek(objItem.DaylightDayOfWeek)
    WScript.Echo "Hour: " & objItem.StandardHour 
    WScript.Echo "Month: " & objItem.StandardMonth _ 
        & " which is: " & arMonth(objItem.StandardMonth )
    WScript.Echo "Description: " & objItem.StandardName 
Next

```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Параметр CIM**](cim-setting.md)
</dt> <dt>

[Классы операционной системы](./operating-system-classes.md)
</dt> <dt>

[**SWbemDateTime**](../wmisdk/swbemdatetime.md)
</dt> <dt>

[Формат даты и времени](../wmisdk/date-and-time-format.md)
</dt> <dt>

[Задачи WMI: даты и время](../wmisdk/wmi-tasks--dates-and-times.md)
</dt> </dl>

 

 

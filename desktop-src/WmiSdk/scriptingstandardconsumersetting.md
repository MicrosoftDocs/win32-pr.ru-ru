---
description: Одноэлементный класс Скриптингстандардконсумерсеттинг предоставляет данные регистрации, общие для всех экземпляров класса-получателя Активескриптевентконсумер Standard.
ms.assetid: d217e058-3529-4173-b896-ebff3d7b05c6
ms.tgt_platform: multiple
title: Класс Скриптингстандардконсумерсеттинг
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ScriptingStandardConsumerSetting
- ScriptingStandardConsumerSetting.Caption
- ScriptingStandardConsumerSetting.Description
- ScriptingStandardConsumerSetting.MaximumScripts
- ScriptingStandardConsumerSetting.SettingID
- ScriptingStandardConsumerSetting.Timeout
api_type:
- DllExport
api_location:
- Scrcons.exe
ms.openlocfilehash: a69d30511d01fba2df39483d1f76616bfae7c92812ce75989fd0c23558558b33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118316208"
---
# <a name="scriptingstandardconsumersetting-class"></a>Класс Скриптингстандардконсумерсеттинг

Одноэлементный класс **скриптингстандардконсумерсеттинг** предоставляет данные регистрации, общие для всех экземпляров класса-получателя [**активескриптевентконсумер**](activescripteventconsumer.md) Standard. Экземпляр **активескриптевентконсумер** использует свойства **максимумскриптс** и **timeout** . Дополнительные сведения см. [в разделе Мониторинг и реагирование на события с помощью стандартных потребителей](monitoring-and-responding-to-events-with-standard-consumers.md).

Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства. Свойства и методы имеют алфавитный порядок, а не порядок MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Singleton, AMENDMENT]
class ScriptingStandardConsumerSetting : CIM_Setting
{
  string Caption = "Scripting Standard Consumer Setting";
  string Description = "Registration data common to all instances of the Scripting Standard Consumer";
  uint32 MaximumScripts = 300;
  string SettingID = "ScriptingStandardConsumerSetting";
  uint32 Timeout = 0;
};
```

## <a name="members"></a>Члены

Класс **скриптингстандардконсумерсеттинг** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **скриптингстандардконсумерсеттинг** имеет следующие свойства.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](standard-qualifiers.md) (64)
</dt> </dl>

Краткое описание объекта — одна строка строки. Содержит строку **скриптингстандардконсумерсеттинг** , так как это одноэлементный класс.

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Текстовое описание объекта.

</dd> <dt>

**максимумскриптс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Максимальное количество скриптов, выполняемых до того, как потребитель запустит новый экземпляр. Чтобы очистить утечки памяти из скриптов, регулярно выполняйте очистку потребителя. Значение по умолчанию — 300.

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](standard-qualifiers.md) (256)
</dt> </dl>

Идентификатор объекта параметра.

</dd> <dt>

**Timeout**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**единицы**](standard-qualifiers.md) ("минуты")
</dt> </dl>

Максимальное число минут, по истечении которого потребитель запускает новый экземпляр. Если значение равно 0 (ноль), свойство **максимумскриптс** управляет жизненным циклом потребителя. Допустимый диапазон значений для **времени ожидания** — от 0 до 71 000, а значение по умолчанию — 0 (ноль).

</dd> </dl>

## <a name="remarks"></a>Remarks

Единственный экземпляр класса **скриптингстандардконсумерсеттинг** находится в корневом \\ пространстве имен CIMV2.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                         |
| Пространство имен<br/>                | Корневая \\ Подписка<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Скрконс. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scrcons.exe</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Параметр CIM**](/windows/desktop/CIMWin32Prov/cim-setting)
</dt> <dt>

[Классы стандартных потребителей](standard-consumer-classes.md)
</dt> <dt>

[Выполнение скрипта на основе события](running-a-script-based-on-an-event.md)
</dt> <dt>

[Создание логического потребителя](creating-a-logical-consumer.md)
</dt> <dt>

[Получение событий в любое время](receiving-events-at-all-times.md)
</dt> <dt>

[**\_\_евентконсумер**](--eventconsumer.md)
</dt> </dl>

 


---
description: Класс Нтевентложевентконсумер регистрирует конкретное сообщение в журнале событий операционной системы при доставке события в него.
ms.assetid: cf986812-f09a-4f32-ba76-db76a23e2e4c
ms.tgt_platform: multiple
title: Класс Нтевентложевентконсумер
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NTEventLogEventConsumer
- NTEventLogEventConsumer.CreatorSID
- NTEventLogEventConsumer.MachineName
- NTEventLogEventConsumer.MaximumQueueSize
- NTEventLogEventConsumer.Category
- NTEventLogEventConsumer.NameOfRawDataProperty
- NTEventLogEventConsumer.EventID
- NTEventLogEventConsumer.EventType
- NTEventLogEventConsumer.InsertionStringTemplates
- NTEventLogEventConsumer.Name
- NTEventLogEventConsumer.NumberOfInsertionStrings
- NTEventLogEventConsumer.NameOfUserSidProperty
- NTEventLogEventConsumer.SourceName
- NTEventLogEventConsumer.UNCServerName
api_type:
- DllExport
api_location:
- Wbemcons.dll
ms.openlocfilehash: dfa2a1dcf15b65808af758820604df6aa62d7bc59d4e1c69e8d4d6e06b1d93a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118555174"
---
# <a name="nteventlogeventconsumer-class"></a>Класс Нтевентложевентконсумер

Класс **нтевентложевентконсумер** регистрирует конкретное сообщение в журнале событий операционной системы при доставке события в него. Этот класс является одним из стандартных потребителей событий, предоставляемых инструментарием WMI. Дополнительные сведения см. [в разделе Мониторинг и реагирование на события с помощью стандартных потребителей](monitoring-and-responding-to-events-with-standard-consumers.md).

## <a name="syntax"></a>Синтаксис

``` syntax
[AMENDMENT]
class NTEventLogEventConsumer : __EventConsumer
{
  uint8  CreatorSID[];
  string MachineName;
  uint32 MaximumQueueSize;
  uint16 Category;
  string NameOfRawDataProperty;
  uint32 EventID;
  uint32 EventType = 1;
  string InsertionStringTemplates[] = {""};
  string Name;
  uint32 NumberOfInsertionStrings = 0;
  string NameOfUserSidProperty;
  string SourceName;
  string UNCServerName;
};
```

## <a name="members"></a>Члены

Класс **нтевентложевентконсумер** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **нтевентложевентконсумер** имеет следующие свойства.

<dl> <dt>

**Категория**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Категория событий. Это сведения, зависящие от источника, и могут иметь любое значение.

</dd> <dt>

**креаторсид**
</dt> <dd> <dl> <dt>

Тип данных: массив **Uint8**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Идентификатор безопасности (SID), однозначно определяющий пользователя, который создает фильтр. WMI хранит идентификатор безопасности пользователя, создающего экземпляр [**\_ \_ евентконсумер**](--eventconsumer.md) , или идентификатор безопасности администратора в зависимости от операционной системы. Дополнительные сведения см. в статьях [Привязка фильтра событий к логическому потребителю](binding-an-event-filter-with-a-logical-consumer.md) и [мониторинг и реагирование на события с помощью стандартных потребителей](monitoring-and-responding-to-events-with-standard-consumers.md).

Это свойство наследуется от [**\_ \_ евентконсумер**](--eventconsumer.md).

</dd> <dt>

**EventID**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Сообщение о событии в библиотеке DLL сообщения. Это свойство не может иметь **значение NULL**.

</dd> <dt>

**EventType**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Тип события. Этот параметр может иметь одно из значений, перечисленных в следующем списке, которые определены в Winnt. h.

<dt>

<span id="EVENTLOG_SUCCESS"></span><span id="eventlog_success"></span>

<span id="EVENTLOG_SUCCESS"></span><span id="eventlog_success"></span>**Журнал событий \_ УСПЕШНО** (0 (0x0))


</dt> <dd>

Успешное событие

</dd> <dt>

<span id="EVENTLOG_ERROR_TPYE"></span><span id="eventlog_error_tpye"></span>

<span id="EVENTLOG_ERROR_TPYE"></span><span id="eventlog_error_tpye"></span>**Журнал событий \_ Ошибка \_ ТПЕ** (1 (0x1))


</dt> <dd>

Событие ошибки

</dd> <dt>

<span id="EVENTLOG_WARNING_TYPE"></span><span id="eventlog_warning_type"></span>

<span id="EVENTLOG_WARNING_TYPE"></span><span id="eventlog_warning_type"></span>**Журнал событий \_ \_Тип предупреждения** (2 (0x2))


</dt> <dd>

Событие предупреждения

</dd> <dt>

<span id="EVENTLOG_INFORMATION_TYPE"></span><span id="eventlog_information_type"></span>

<span id="EVENTLOG_INFORMATION_TYPE"></span><span id="eventlog_information_type"></span>**Журнал событий \_ \_Тип сведений** (4 (0x4))


</dt> <dd>

Информационное событие

</dd> <dt>

<span id="EVENTLOG_AUDIT_SUCCESS"></span><span id="eventlog_audit_success"></span>

<span id="EVENTLOG_AUDIT_SUCCESS"></span><span id="eventlog_audit_success"></span>**Журнал событий \_ \_Успешный аудит** (8 (0x8))


</dt> <dd>

Тип аудита успехов

</dd> <dt>

<span id="EVENTLOG_AUDIT_FAILURE"></span><span id="eventlog_audit_failure"></span>

<span id="EVENTLOG_AUDIT_FAILURE"></span><span id="eventlog_audit_failure"></span>**Журнал событий \_ \_Сбой аудита** (16 (0x10))


</dt> <dd>

Тип аудита сбоев

</dd> </dl>

</dd> <dt>

**инсертионстрингтемплатес**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Массив стандартных строковых шаблонов, который используется в качестве строки вставки для записи журнала событий.

</dd> <dt>

**MachineName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

имя компьютера, на который инструментарий управления Windows (WMI) (WMI) отправляет события.

Это свойство наследуется от [**\_ \_ евентконсумер**](--eventconsumer.md).

</dd> <dt>

**максимумкуеуесизе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Максимальная очередь для конкретного потребителя в байтах.

Это свойство наследуется от [**\_ \_ евентконсумер**](--eventconsumer.md).

</dd> <dt>

**Имя**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](key-qualifier.md)
</dt> </dl>

Уникальное имя потребителя.

</dd> <dt>

**намеофравдатапроперти**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя свойства события, которое содержит данные, передаваемые в параметр *лправдата* функции [**репортевент**](/windows/desktop/api/winbase/nf-winbase-reporteventa) .

</dd> <dt>

**намеофусерсидпроперти**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя свойства события, которое содержит идентификатор безопасности (SID), передаваемый в параметр *лпусерсид* функции [**репортевент**](/windows/desktop/api/winbase/nf-winbase-reporteventa) . Свойство должно быть либо массивом из байтов (**Uint8**), либо строкой. Если это массив байтов, предполагается, что он является идентификатором безопасности. Если это строка, то это строковый идентификатор безопасности, который преобразуется в идентификатор безопасности.

</dd> <dt>

**нумберофинсертионстрингс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Число элементов в массиве **инсертионстрингтемплатес** .

</dd> <dt>

**SourceName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя источника, в котором находится сообщение. Предполагается, что клиент зарегистрировал библиотеку DLL с необходимыми сообщениями.

> [!Note]  
> Значение этого параметра не должно включать двоеточие (:) символов.

 

</dd> <dt>

**унксервернаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя компьютера, на котором регистрируется событие, или **значение NULL** , если событие должно быть зарегистрировано на локальном сервере.

Пользователи, прошедшие проверку подлинности, по умолчанию не могут регистрировать события в журнале приложений на удаленном компьютере. В результате использование этого свойства для указания удаленного компьютера не будет работать. Чтобы узнать, как изменить безопасность журнала событий, ознакомьтесь с этой [статьей в базе знаний](https://support.microsoft.com/kb/323076).

</dd> </dl>

## <a name="remarks"></a>Remarks

Класс **нтевентложевентконсумер** является производным от абстрактного класса [**\_ \_ евентконсумер**](--eventconsumer.md) .

## <a name="examples"></a>Примеры

Пример использования **нтевентложевентконсумер** для создания потребителя см. в разделе [ведение журнала событий NT на основе события](logging-to-nt-event-log-based-on-an-event.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневая \\ Подписка<br/>                                                           |
| MOF<br/>                      | <dl> <dt>Вбемконс. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemcons.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Классы стандартных потребителей](standard-consumer-classes.md)
</dt> <dt>

[Создание логического потребителя](creating-a-logical-consumer.md)
</dt> <dt>

[Получение событий в любое время](receiving-events-at-all-times.md)
</dt> <dt>

[**\_\_евентконсумер**](--eventconsumer.md)
</dt> </dl>

 


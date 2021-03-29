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
ms.openlocfilehash: e98948688b0fee37316102b2c37039de1c139310
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898090"
---
# <a name="nteventlogeventconsumer-class"></a><span data-ttu-id="0a589-103">Класс Нтевентложевентконсумер</span><span class="sxs-lookup"><span data-stu-id="0a589-103">NTEventLogEventConsumer class</span></span>

<span data-ttu-id="0a589-104">Класс **нтевентложевентконсумер** регистрирует конкретное сообщение в журнале событий операционной системы при доставке события в него.</span><span class="sxs-lookup"><span data-stu-id="0a589-104">The **NTEventLogEventConsumer** class logs a specific message to the operating system event log when an event is delivered to it.</span></span> <span data-ttu-id="0a589-105">Этот класс является одним из стандартных потребителей событий, предоставляемых инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="0a589-105">This class is one of the standard event consumers that WMI provides.</span></span> <span data-ttu-id="0a589-106">Дополнительные сведения см. [в разделе Мониторинг и реагирование на события с помощью стандартных потребителей](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="0a589-106">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0a589-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0a589-107">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="0a589-108">Члены</span><span class="sxs-lookup"><span data-stu-id="0a589-108">Members</span></span>

<span data-ttu-id="0a589-109">Класс **нтевентложевентконсумер** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="0a589-109">The **NTEventLogEventConsumer** class has these types of members:</span></span>

-   [<span data-ttu-id="0a589-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="0a589-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0a589-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="0a589-111">Properties</span></span>

<span data-ttu-id="0a589-112">Класс **нтевентложевентконсумер** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="0a589-112">The **NTEventLogEventConsumer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0a589-113">**Категория**</span><span class="sxs-lookup"><span data-stu-id="0a589-113">**Category**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a589-114">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0a589-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0a589-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0a589-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0a589-116">Категория событий.</span><span class="sxs-lookup"><span data-stu-id="0a589-116">Event category.</span></span> <span data-ttu-id="0a589-117">Это сведения, зависящие от источника, и могут иметь любое значение.</span><span class="sxs-lookup"><span data-stu-id="0a589-117">This is source-specific information and can have any value.</span></span>

</dd> <dt>

<span data-ttu-id="0a589-118">**креаторсид**</span><span class="sxs-lookup"><span data-stu-id="0a589-118">**CreatorSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a589-119">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="0a589-119">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="0a589-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0a589-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0a589-121">Идентификатор безопасности (SID), однозначно определяющий пользователя, который создает фильтр.</span><span class="sxs-lookup"><span data-stu-id="0a589-121">Security identifier (SID) that uniquely identifies the user who creates a filter.</span></span> <span data-ttu-id="0a589-122">WMI хранит идентификатор безопасности пользователя, создающего экземпляр [**\_ \_ евентконсумер**](--eventconsumer.md) , или идентификатор безопасности администратора в зависимости от операционной системы.</span><span class="sxs-lookup"><span data-stu-id="0a589-122">WMI stores the SID of the user who creates an instance of [**\_\_EventConsumer**](--eventconsumer.md) or the Administrator SID, depending on the operating system.</span></span> <span data-ttu-id="0a589-123">Дополнительные сведения см. в статьях [Привязка фильтра событий к логическому потребителю](binding-an-event-filter-with-a-logical-consumer.md) и [мониторинг и реагирование на события с помощью стандартных потребителей](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="0a589-123">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md) and [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

<span data-ttu-id="0a589-124">Это свойство наследуется от [**\_ \_ евентконсумер**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="0a589-124">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a589-125">**EventID**</span><span class="sxs-lookup"><span data-stu-id="0a589-125">**EventID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a589-126">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0a589-126">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0a589-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0a589-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0a589-128">Сообщение о событии в библиотеке DLL сообщения.</span><span class="sxs-lookup"><span data-stu-id="0a589-128">Event message in the message DLL.</span></span> <span data-ttu-id="0a589-129">Это свойство не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="0a589-129">This property cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="0a589-130">**EventType**</span><span class="sxs-lookup"><span data-stu-id="0a589-130">**EventType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a589-131">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0a589-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0a589-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0a589-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0a589-133">Тип события.</span><span class="sxs-lookup"><span data-stu-id="0a589-133">Type of event.</span></span> <span data-ttu-id="0a589-134">Этот параметр может иметь одно из значений, перечисленных в следующем списке, которые определены в Winnt. h.</span><span class="sxs-lookup"><span data-stu-id="0a589-134">This parameter can have one of the values listed in the following list, which are defined in Winnt.h.</span></span>

<dt>

<span id="EVENTLOG_SUCCESS"></span><span id="eventlog_success"></span>

<span data-ttu-id="0a589-135"><span id="EVENTLOG_SUCCESS"></span><span id="eventlog_success"></span>**Журнал событий \_ УСПЕШНО** (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="0a589-135"><span id="EVENTLOG_SUCCESS"></span><span id="eventlog_success"></span>**EVENTLOG\_SUCCESS** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="0a589-136">Успешное событие</span><span class="sxs-lookup"><span data-stu-id="0a589-136">Successful event</span></span>

</dd> <dt>

<span id="EVENTLOG_ERROR_TPYE"></span><span id="eventlog_error_tpye"></span>

<span data-ttu-id="0a589-137"><span id="EVENTLOG_ERROR_TPYE"></span><span id="eventlog_error_tpye"></span>**Журнал событий \_ Ошибка \_ ТПЕ** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="0a589-137"><span id="EVENTLOG_ERROR_TPYE"></span><span id="eventlog_error_tpye"></span>**EVENTLOG\_ERROR\_TPYE** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="0a589-138">Событие ошибки</span><span class="sxs-lookup"><span data-stu-id="0a589-138">Error event</span></span>

</dd> <dt>

<span id="EVENTLOG_WARNING_TYPE"></span><span id="eventlog_warning_type"></span>

<span data-ttu-id="0a589-139"><span id="EVENTLOG_WARNING_TYPE"></span><span id="eventlog_warning_type"></span>**Журнал событий \_ \_Тип предупреждения** (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="0a589-139"><span id="EVENTLOG_WARNING_TYPE"></span><span id="eventlog_warning_type"></span>**EVENTLOG\_WARNING\_TYPE** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="0a589-140">Событие предупреждения</span><span class="sxs-lookup"><span data-stu-id="0a589-140">Warning event</span></span>

</dd> <dt>

<span id="EVENTLOG_INFORMATION_TYPE"></span><span id="eventlog_information_type"></span>

<span data-ttu-id="0a589-141"><span id="EVENTLOG_INFORMATION_TYPE"></span><span id="eventlog_information_type"></span>**Журнал событий \_ \_Тип сведений** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="0a589-141"><span id="EVENTLOG_INFORMATION_TYPE"></span><span id="eventlog_information_type"></span>**EVENTLOG\_INFORMATION\_TYPE** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="0a589-142">Информационное событие</span><span class="sxs-lookup"><span data-stu-id="0a589-142">Information event</span></span>

</dd> <dt>

<span id="EVENTLOG_AUDIT_SUCCESS"></span><span id="eventlog_audit_success"></span>

<span data-ttu-id="0a589-143"><span id="EVENTLOG_AUDIT_SUCCESS"></span><span id="eventlog_audit_success"></span>**Журнал событий \_ \_Успешный аудит** (8 (0x8))</span><span class="sxs-lookup"><span data-stu-id="0a589-143"><span id="EVENTLOG_AUDIT_SUCCESS"></span><span id="eventlog_audit_success"></span>**EVENTLOG\_AUDIT\_SUCCESS** (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="0a589-144">Тип аудита успехов</span><span class="sxs-lookup"><span data-stu-id="0a589-144">Success audit type</span></span>

</dd> <dt>

<span id="EVENTLOG_AUDIT_FAILURE"></span><span id="eventlog_audit_failure"></span>

<span data-ttu-id="0a589-145"><span id="EVENTLOG_AUDIT_FAILURE"></span><span id="eventlog_audit_failure"></span>**Журнал событий \_ \_Сбой аудита** (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="0a589-145"><span id="EVENTLOG_AUDIT_FAILURE"></span><span id="eventlog_audit_failure"></span>**EVENTLOG\_AUDIT\_FAILURE** (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="0a589-146">Тип аудита сбоев</span><span class="sxs-lookup"><span data-stu-id="0a589-146">Failure audit type</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0a589-147">**инсертионстрингтемплатес**</span><span class="sxs-lookup"><span data-stu-id="0a589-147">**InsertionStringTemplates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a589-148">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="0a589-148">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0a589-149">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0a589-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0a589-150">Массив стандартных строковых шаблонов, который используется в качестве строки вставки для записи журнала событий.</span><span class="sxs-lookup"><span data-stu-id="0a589-150">Array of standard string templates that is used as the insertion string for an event log record.</span></span>

</dd> <dt>

<span data-ttu-id="0a589-151">**MachineName**</span><span class="sxs-lookup"><span data-stu-id="0a589-151">**MachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a589-152">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0a589-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0a589-153">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0a589-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0a589-154">Имя компьютера, на который инструментарий управления Windows (WMI) (WMI) отправляет события.</span><span class="sxs-lookup"><span data-stu-id="0a589-154">Name of the computer to which Windows Management Instrumentation (WMI) sends events.</span></span>

<span data-ttu-id="0a589-155">Это свойство наследуется от [**\_ \_ евентконсумер**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="0a589-155">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a589-156">**максимумкуеуесизе**</span><span class="sxs-lookup"><span data-stu-id="0a589-156">**MaximumQueueSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a589-157">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0a589-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0a589-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0a589-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0a589-159">Максимальная очередь для конкретного потребителя в байтах.</span><span class="sxs-lookup"><span data-stu-id="0a589-159">Maximum queue for a specific consumer, in bytes.</span></span>

<span data-ttu-id="0a589-160">Это свойство наследуется от [**\_ \_ евентконсумер**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="0a589-160">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a589-161">**Name**</span><span class="sxs-lookup"><span data-stu-id="0a589-161">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a589-162">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0a589-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0a589-163">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0a589-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a589-164">Квалификаторы: [ **ключ**](key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="0a589-164">Qualifiers: [**key**](key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="0a589-165">Уникальное имя потребителя.</span><span class="sxs-lookup"><span data-stu-id="0a589-165">Unique name of a consumer.</span></span>

</dd> <dt>

<span data-ttu-id="0a589-166">**намеофравдатапроперти**</span><span class="sxs-lookup"><span data-stu-id="0a589-166">**NameOfRawDataProperty**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a589-167">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0a589-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0a589-168">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0a589-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0a589-169">Имя свойства события, которое содержит данные, передаваемые в параметр *лправдата* функции [**репортевент**](/windows/desktop/api/winbase/nf-winbase-reporteventa) .</span><span class="sxs-lookup"><span data-stu-id="0a589-169">Name of the event property that contains data to be passed to the [**ReportEvent**](/windows/desktop/api/winbase/nf-winbase-reporteventa) function *lpRawData* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="0a589-170">**намеофусерсидпроперти**</span><span class="sxs-lookup"><span data-stu-id="0a589-170">**NameOfUserSidProperty**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a589-171">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0a589-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0a589-172">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0a589-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0a589-173">Имя свойства события, которое содержит идентификатор безопасности (SID), передаваемый в параметр *лпусерсид* функции [**репортевент**](/windows/desktop/api/winbase/nf-winbase-reporteventa) .</span><span class="sxs-lookup"><span data-stu-id="0a589-173">Name of the event property that contains a security identifier (SID) to be passed to the [**ReportEvent**](/windows/desktop/api/winbase/nf-winbase-reporteventa) function *lpUserSid* parameter.</span></span> <span data-ttu-id="0a589-174">Свойство должно быть либо массивом из байтов (**Uint8**), либо строкой.</span><span class="sxs-lookup"><span data-stu-id="0a589-174">The property must be either an array of bytes (**uint8**) or a string.</span></span> <span data-ttu-id="0a589-175">Если это массив байтов, предполагается, что он является идентификатором безопасности.</span><span class="sxs-lookup"><span data-stu-id="0a589-175">If it is an array of bytes, it is assumed to be a SID.</span></span> <span data-ttu-id="0a589-176">Если это строка, то это строковый идентификатор безопасности, который преобразуется в идентификатор безопасности.</span><span class="sxs-lookup"><span data-stu-id="0a589-176">If it is a string, it is a string SID that is converted into a SID.</span></span>

</dd> <dt>

<span data-ttu-id="0a589-177">**нумберофинсертионстрингс**</span><span class="sxs-lookup"><span data-stu-id="0a589-177">**NumberOfInsertionStrings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a589-178">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0a589-178">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0a589-179">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0a589-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0a589-180">Число элементов в массиве **инсертионстрингтемплатес** .</span><span class="sxs-lookup"><span data-stu-id="0a589-180">Number of elements in the **InsertionStringTemplates** array.</span></span>

</dd> <dt>

<span data-ttu-id="0a589-181">**SourceName**</span><span class="sxs-lookup"><span data-stu-id="0a589-181">**SourceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a589-182">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0a589-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0a589-183">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0a589-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0a589-184">Имя источника, в котором находится сообщение.</span><span class="sxs-lookup"><span data-stu-id="0a589-184">Source name where a message is located.</span></span> <span data-ttu-id="0a589-185">Предполагается, что клиент зарегистрировал библиотеку DLL с необходимыми сообщениями.</span><span class="sxs-lookup"><span data-stu-id="0a589-185">The customer is assumed to have registered a DLL with the necessary messages.</span></span>

> [!Note]  
> <span data-ttu-id="0a589-186">Значение этого параметра не должно включать двоеточие (:) символов.</span><span class="sxs-lookup"><span data-stu-id="0a589-186">The value of this parameter must not include a colon (:) character.</span></span>

 

</dd> <dt>

<span data-ttu-id="0a589-187">**унксервернаме**</span><span class="sxs-lookup"><span data-stu-id="0a589-187">**UNCServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a589-188">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0a589-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0a589-189">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0a589-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0a589-190">Имя компьютера, на котором регистрируется событие, или **значение NULL** , если событие должно быть зарегистрировано на локальном сервере.</span><span class="sxs-lookup"><span data-stu-id="0a589-190">Name of the computer on which to log an event, or **NULL** if the event is to be logged on a local server.</span></span>

<span data-ttu-id="0a589-191">Пользователи, прошедшие проверку подлинности, по умолчанию не могут регистрировать события в журнале приложений на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="0a589-191">Authenticated users cannot, by default, log events to the Application log on a remote computer.</span></span> <span data-ttu-id="0a589-192">В результате использование этого свойства для указания удаленного компьютера не будет работать.</span><span class="sxs-lookup"><span data-stu-id="0a589-192">As a result, using this property to specify a remote computer will not work.</span></span> <span data-ttu-id="0a589-193">Чтобы узнать, как изменить безопасность журнала событий, ознакомьтесь с этой [статьей в базе знаний](https://support.microsoft.com/kb/323076).</span><span class="sxs-lookup"><span data-stu-id="0a589-193">To learn how to change event log security, consult this [KB article](https://support.microsoft.com/kb/323076).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0a589-194">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0a589-194">Remarks</span></span>

<span data-ttu-id="0a589-195">Класс **нтевентложевентконсумер** является производным от абстрактного класса [**\_ \_ евентконсумер**](--eventconsumer.md) .</span><span class="sxs-lookup"><span data-stu-id="0a589-195">The **NTEventLogEventConsumer** class is derived from the [**\_\_EventConsumer**](--eventconsumer.md) abstract class.</span></span>

## <a name="examples"></a><span data-ttu-id="0a589-196">Примеры</span><span class="sxs-lookup"><span data-stu-id="0a589-196">Examples</span></span>

<span data-ttu-id="0a589-197">Пример использования **нтевентложевентконсумер** для создания потребителя см. в разделе [ведение журнала событий NT на основе события](logging-to-nt-event-log-based-on-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="0a589-197">For an example of using **NTEventLogEventConsumer** to create a consumer, see [Logging to NT Event Log Based on an Event](logging-to-nt-event-log-based-on-an-event.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0a589-198">Требования</span><span class="sxs-lookup"><span data-stu-id="0a589-198">Requirements</span></span>



| <span data-ttu-id="0a589-199">Требование</span><span class="sxs-lookup"><span data-stu-id="0a589-199">Requirement</span></span> | <span data-ttu-id="0a589-200">Значение</span><span class="sxs-lookup"><span data-stu-id="0a589-200">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0a589-201">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0a589-201">Minimum supported client</span></span><br/> | <span data-ttu-id="0a589-202">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0a589-202">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0a589-203">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0a589-203">Minimum supported server</span></span><br/> | <span data-ttu-id="0a589-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0a589-204">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0a589-205">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0a589-205">Namespace</span></span><br/>                | <span data-ttu-id="0a589-206">Корневая \\ Подписка</span><span class="sxs-lookup"><span data-stu-id="0a589-206">Root\\subscription</span></span><br/>                                                           |
| <span data-ttu-id="0a589-207">MOF</span><span class="sxs-lookup"><span data-stu-id="0a589-207">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0a589-208"><dt>Вбемконс. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0a589-208"><dt>Wbemcons.mof</dt></span></span> </dl> |
| <span data-ttu-id="0a589-209">DLL</span><span class="sxs-lookup"><span data-stu-id="0a589-209">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a589-210"><dt>Wbemcons.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a589-210"><dt>Wbemcons.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a589-211">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0a589-211">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a589-212">Классы стандартных потребителей</span><span class="sxs-lookup"><span data-stu-id="0a589-212">Standard Consumer Classes</span></span>](standard-consumer-classes.md)
</dt> <dt>

[<span data-ttu-id="0a589-213">Создание логического потребителя</span><span class="sxs-lookup"><span data-stu-id="0a589-213">Creating a Logical Consumer</span></span>](creating-a-logical-consumer.md)
</dt> <dt>

[<span data-ttu-id="0a589-214">Получение событий в любое время</span><span class="sxs-lookup"><span data-stu-id="0a589-214">Receiving Events At All Times</span></span>](receiving-events-at-all-times.md)
</dt> <dt>

[<span data-ttu-id="0a589-215">**\_\_евентконсумер**</span><span class="sxs-lookup"><span data-stu-id="0a589-215">**\_\_EventConsumer**</span></span>](--eventconsumer.md)
</dt> </dl>

 


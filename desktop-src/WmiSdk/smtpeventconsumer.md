---
description: Класс Смтпевентконсумер отправляет сообщение электронной почты с помощью протокола SMTP каждый раз, когда в него передается событие.
ms.assetid: 42178360-9e22-4cd1-9b72-5f6b0d7e6c9c
ms.tgt_platform: multiple
title: Класс Смтпевентконсумер
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SMTPEventConsumer
- SMTPEventConsumer.CreatorSID
- SMTPEventConsumer.MachineName
- SMTPEventConsumer.MaximumQueueSize
- SMTPEventConsumer.BccLine
- SMTPEventConsumer.CcLine
- SMTPEventConsumer.FromLine
- SMTPEventConsumer.HeaderFields
- SMTPEventConsumer.Message
- SMTPEventConsumer.Name
- SMTPEventConsumer.ReplyToLine
- SMTPEventConsumer.SMTPServer
- SMTPEventConsumer.Subject
- SMTPEventConsumer.ToLine
api_type:
- DllExport
api_location:
- Smtpcons.dll
ms.openlocfilehash: 76c7fad3b5cb4bbf6c3c0c03689607ba64fbcc67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272570"
---
# <a name="smtpeventconsumer-class"></a><span data-ttu-id="2b875-103">Класс Смтпевентконсумер</span><span class="sxs-lookup"><span data-stu-id="2b875-103">SMTPEventConsumer class</span></span>

<span data-ttu-id="2b875-104">Класс **смтпевентконсумер** отправляет сообщение электронной почты с помощью протокола SMTP каждый раз, когда в него передается событие.</span><span class="sxs-lookup"><span data-stu-id="2b875-104">The **SMTPEventConsumer** class sends an email message by using Simple Mail Transfer Protocol (SMTP) each time an event is delivered to it.</span></span> <span data-ttu-id="2b875-105">SMTP-сервер должен существовать в сети.</span><span class="sxs-lookup"><span data-stu-id="2b875-105">An SMTP server must exist on the network.</span></span> <span data-ttu-id="2b875-106">Класс Смтпевентконсумер не поддерживает вложения.</span><span class="sxs-lookup"><span data-stu-id="2b875-106">The SMTPEventConsumer class does not support attachments.</span></span> <span data-ttu-id="2b875-107">Кодировка сообщения электронной почты должна быть US-ASCII.</span><span class="sxs-lookup"><span data-stu-id="2b875-107">The encoding of the email message must be US-ASCII.</span></span>

<span data-ttu-id="2b875-108">Этот класс является одним из стандартных потребителей событий, предоставляемых инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="2b875-108">This class is one of the standard event consumers that WMI provides.</span></span> <span data-ttu-id="2b875-109">Пример использования **смтпевентконсумер** для создания потребителя см. в разделе [Отправка сообщения электронной почты на основе события](sending-e-mail-based-on-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="2b875-109">For an example of using **SMTPEventConsumer** to create a consumer, see [Sending Email Based on an Event](sending-e-mail-based-on-an-event.md).</span></span> <span data-ttu-id="2b875-110">Дополнительные сведения см. [в разделе Мониторинг и реагирование на события с помощью стандартных потребителей](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="2b875-110">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

<span data-ttu-id="2b875-111">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="2b875-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="2b875-112">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="2b875-112">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b875-113">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2b875-113">Syntax</span></span>

``` syntax
[AMENDMENT]
class SMTPEventConsumer : __EventConsumer
{
  uint8  CreatorSID[];
  string MachineName;
  uint32 MaximumQueueSize;
  string BccLine;
  string CcLine;
  string FromLine;
  string HeaderFields[];
  string Message;
  string Name;
  string ReplyToLine;
  string SMTPServer;
  string Subject;
  string ToLine;
};
```

## <a name="members"></a><span data-ttu-id="2b875-114">Члены</span><span class="sxs-lookup"><span data-stu-id="2b875-114">Members</span></span>

<span data-ttu-id="2b875-115">Класс **смтпевентконсумер** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="2b875-115">The **SMTPEventConsumer** class has these types of members:</span></span>

-   [<span data-ttu-id="2b875-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="2b875-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2b875-117">Свойства</span><span class="sxs-lookup"><span data-stu-id="2b875-117">Properties</span></span>

<span data-ttu-id="2b875-118">Класс **смтпевентконсумер** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="2b875-118">The **SMTPEventConsumer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2b875-119">**бкклине**</span><span class="sxs-lookup"><span data-stu-id="2b875-119">**BccLine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b875-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2b875-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b875-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b875-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b875-122">Список адресов, разделенных запятой или точкой с запятой, в формате стандартного строкового шаблона, в который сообщение отправляется в виде скрытой копии.</span><span class="sxs-lookup"><span data-stu-id="2b875-122">A list of addresses, separated by a comma or semicolon, in the format of a standard string template to which the message is sent as a blind carbon copy.</span></span> <span data-ttu-id="2b875-123">Дополнительные сведения см. в подразделе «Примечания» этого раздела.</span><span class="sxs-lookup"><span data-stu-id="2b875-123">For more information, see the Remarks section of this topic.</span></span>

</dd> <dt>

<span data-ttu-id="2b875-124">**кклине**</span><span class="sxs-lookup"><span data-stu-id="2b875-124">**CcLine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b875-125">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2b875-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b875-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b875-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b875-127">Список адресов, разделенных запятой или точкой с запятой, в формате стандартного строкового шаблона, в который отправляется сообщение в виде копии.</span><span class="sxs-lookup"><span data-stu-id="2b875-127">A list of addresses, separated by a comma or semicolon, in the format of a standard string template to which the message is sent as a carbon copy.</span></span> <span data-ttu-id="2b875-128">Дополнительные сведения см. в подразделе «Примечания» этого раздела.</span><span class="sxs-lookup"><span data-stu-id="2b875-128">For more information, see the Remarks section of this topic.</span></span>

</dd> <dt>

<span data-ttu-id="2b875-129">**креаторсид**</span><span class="sxs-lookup"><span data-stu-id="2b875-129">**CreatorSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b875-130">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="2b875-130">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="2b875-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b875-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b875-132">Идентификатор безопасности (SID), однозначно определяющий пользователя, который создает фильтр.</span><span class="sxs-lookup"><span data-stu-id="2b875-132">Security identifier (SID) that uniquely identifies the user who creates a filter.</span></span> <span data-ttu-id="2b875-133">WMI хранит идентификатор безопасности пользователя, создающего экземпляр [**\_ \_ евентконсумер**](--eventconsumer.md) , или идентификатор безопасности администратора в зависимости от операционной системы.</span><span class="sxs-lookup"><span data-stu-id="2b875-133">WMI stores the SID of the user who creates an instance of [**\_\_EventConsumer**](--eventconsumer.md) or the Administrator SID, depending on the operating system.</span></span> <span data-ttu-id="2b875-134">Дополнительные сведения см. в статьях [Привязка фильтра событий к логическому потребителю](binding-an-event-filter-with-a-logical-consumer.md) и [мониторинг и реагирование на события с помощью стандартных потребителей](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="2b875-134">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md) and [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

<span data-ttu-id="2b875-135">Это свойство наследуется от [**\_ \_ евентконсумер**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="2b875-135">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="2b875-136">**фромлине**</span><span class="sxs-lookup"><span data-stu-id="2b875-136">**FromLine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b875-137">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2b875-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b875-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b875-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b875-139">Строка из строки сообщения электронной почты в формате стандартного строкового шаблона.</span><span class="sxs-lookup"><span data-stu-id="2b875-139">From line of an email message in the format of a standard string template.</span></span> <span data-ttu-id="2b875-140">Если **значение равно NULL**, строка From создается в виде "Winmgmt@*MachineName*".</span><span class="sxs-lookup"><span data-stu-id="2b875-140">If **NULL**, a From line is constructed in the form of "WinMgmt@*MachineName*".</span></span>

</dd> <dt>

<span data-ttu-id="2b875-141">**хеадерфиелдс**</span><span class="sxs-lookup"><span data-stu-id="2b875-141">**HeaderFields**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b875-142">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="2b875-142">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2b875-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b875-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b875-144">Массив полей заголовков, которые вставляются в сообщение электронной почты без интерпретации.</span><span class="sxs-lookup"><span data-stu-id="2b875-144">Array of header fields that are inserted into an email message without interpretation.</span></span>

</dd> <dt>

<span data-ttu-id="2b875-145">**MachineName**</span><span class="sxs-lookup"><span data-stu-id="2b875-145">**MachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b875-146">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2b875-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b875-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b875-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b875-148">Имя компьютера, на который инструментарий управления Windows (WMI) (WMI) отправляет события.</span><span class="sxs-lookup"><span data-stu-id="2b875-148">Name of the computer to which Windows Management Instrumentation (WMI) sends events.</span></span>

<span data-ttu-id="2b875-149">Это свойство наследуется от [**\_ \_ евентконсумер**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="2b875-149">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="2b875-150">**максимумкуеуесизе**</span><span class="sxs-lookup"><span data-stu-id="2b875-150">**MaximumQueueSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b875-151">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2b875-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2b875-152">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b875-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b875-153">Максимальная очередь для конкретного потребителя в байтах.</span><span class="sxs-lookup"><span data-stu-id="2b875-153">Maximum queue for a specific consumer, in bytes.</span></span>

<span data-ttu-id="2b875-154">Это свойство наследуется от [**\_ \_ евентконсумер**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="2b875-154">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="2b875-155">**Message**</span><span class="sxs-lookup"><span data-stu-id="2b875-155">**Message**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b875-156">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2b875-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b875-157">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b875-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b875-158">Стандартный строковый шаблон, содержащий текст сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="2b875-158">Standard string template that contains the body of an email message.</span></span>

</dd> <dt>

<span data-ttu-id="2b875-159">**Name**</span><span class="sxs-lookup"><span data-stu-id="2b875-159">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b875-160">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2b875-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b875-161">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b875-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b875-162">Квалификаторы: [ **ключ**](key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="2b875-162">Qualifiers: [**key**](key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="2b875-163">Уникальный идентификатор потребителя событий.</span><span class="sxs-lookup"><span data-stu-id="2b875-163">Unique identifier for the event consumer.</span></span>

</dd> <dt>

<span data-ttu-id="2b875-164">**реплитолине**</span><span class="sxs-lookup"><span data-stu-id="2b875-164">**ReplyToLine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b875-165">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2b875-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b875-166">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b875-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b875-167">Строка ответа на сообщение электронной почты в формате стандартного строкового шаблона.</span><span class="sxs-lookup"><span data-stu-id="2b875-167">Reply-to line of an email message in the format of a standard string template.</span></span> <span data-ttu-id="2b875-168">Если **значение равно NULL**, строка ответа не используется.</span><span class="sxs-lookup"><span data-stu-id="2b875-168">If **NULL**, no Reply-to line is used.</span></span>

</dd> <dt>

<span data-ttu-id="2b875-169">**SMTPServer**</span><span class="sxs-lookup"><span data-stu-id="2b875-169">**SMTPServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b875-170">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2b875-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b875-171">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b875-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b875-172">Имя SMTP-сервера, через который отправляется сообщение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="2b875-172">Name of the SMTP server through which an email is sent.</span></span> <span data-ttu-id="2b875-173">Допустимые имена: IP-адрес, DNS или NetBIOS-имя.</span><span class="sxs-lookup"><span data-stu-id="2b875-173">Permissible names are an IP address, or a DNS or NetBIOS name.</span></span> <span data-ttu-id="2b875-174">Это свойство не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="2b875-174">This property cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="2b875-175">**Тема**</span><span class="sxs-lookup"><span data-stu-id="2b875-175">**Subject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b875-176">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2b875-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b875-177">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b875-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b875-178">Стандартный строковый шаблон, содержащий тему сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="2b875-178">Standard string template that contains the subject of an email message.</span></span>

</dd> <dt>

<span data-ttu-id="2b875-179">**Поле ToLine**</span><span class="sxs-lookup"><span data-stu-id="2b875-179">**ToLine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b875-180">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2b875-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b875-181">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b875-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b875-182">Список адресов, разделенных запятой или точкой с запятой, в формате стандартного строкового шаблона, определяющего место отправки сообщения.</span><span class="sxs-lookup"><span data-stu-id="2b875-182">A list of addresses, separated by a comma or semicolon, in the format of a standard string template that identifies where the message is to be sent.</span></span> <span data-ttu-id="2b875-183">Дополнительные сведения см. в подразделе «Примечания» этого раздела.</span><span class="sxs-lookup"><span data-stu-id="2b875-183">For more information, see the Remarks section of this topic.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2b875-184">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2b875-184">Remarks</span></span>

<span data-ttu-id="2b875-185">Класс смтпевентконсумер является производным от абстрактного класса [**\_ \_ евентконсумер**](--eventconsumer.md) .</span><span class="sxs-lookup"><span data-stu-id="2b875-185">The SMTPEventConsumer class is derived from the [**\_\_EventConsumer**](--eventconsumer.md) abstract class.</span></span>

<span data-ttu-id="2b875-186">Некоторые свойства **поле ToLine**, **кклине** или **бкклине** могут иметь **значение NULL**, но они не могут иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="2b875-186">Some of the **ToLine**, **CcLine**, or **BccLine** properties can be **NULL**, but they cannot all be **NULL**.</span></span>

<span data-ttu-id="2b875-187">Получение кода возврата ошибки от службы SMTP считается сбоем.</span><span class="sxs-lookup"><span data-stu-id="2b875-187">Receiving an error return code from the SMTP service is considered a failure.</span></span>

## <a name="examples"></a><span data-ttu-id="2b875-188">Примеры</span><span class="sxs-lookup"><span data-stu-id="2b875-188">Examples</span></span>

<span data-ttu-id="2b875-189">Пример использования **смтпевентконсумер** для создания потребителя см. в разделе [Отправка сообщения электронной почты на основе события](sending-e-mail-based-on-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="2b875-189">For an example of using **SMTPEventConsumer** to create a consumer, see [Sending Email Based on an Event](sending-e-mail-based-on-an-event.md).</span></span> <span data-ttu-id="2b875-190">Дополнительные сведения см. [в разделе Мониторинг и реагирование на события с помощью стандартных потребителей](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="2b875-190">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2b875-191">Требования</span><span class="sxs-lookup"><span data-stu-id="2b875-191">Requirements</span></span>



| <span data-ttu-id="2b875-192">Требование</span><span class="sxs-lookup"><span data-stu-id="2b875-192">Requirement</span></span> | <span data-ttu-id="2b875-193">Значение</span><span class="sxs-lookup"><span data-stu-id="2b875-193">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b875-194">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2b875-194">Minimum supported client</span></span><br/> | <span data-ttu-id="2b875-195">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2b875-195">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2b875-196">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2b875-196">Minimum supported server</span></span><br/> | <span data-ttu-id="2b875-197">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2b875-197">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2b875-198">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2b875-198">Namespace</span></span><br/>                | <span data-ttu-id="2b875-199">Корневая \\ Подписка</span><span class="sxs-lookup"><span data-stu-id="2b875-199">Root\\subscription</span></span><br/>                                                           |
| <span data-ttu-id="2b875-200">MOF</span><span class="sxs-lookup"><span data-stu-id="2b875-200">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2b875-201"><dt>Смтпконс. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2b875-201"><dt>Smtpcons.mof</dt></span></span> </dl> |
| <span data-ttu-id="2b875-202">DLL</span><span class="sxs-lookup"><span data-stu-id="2b875-202">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b875-203"><dt>Smtpcons.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b875-203"><dt>Smtpcons.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b875-204">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2b875-204">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b875-205">**\_\_евентконсумер**</span><span class="sxs-lookup"><span data-stu-id="2b875-205">**\_\_EventConsumer**</span></span>](--eventconsumer.md)
</dt> <dt>

[<span data-ttu-id="2b875-206">Классы стандартных потребителей</span><span class="sxs-lookup"><span data-stu-id="2b875-206">Standard Consumer Classes</span></span>](standard-consumer-classes.md)
</dt> <dt>

[<span data-ttu-id="2b875-207">Отправка сообщения электронной почты на основе события</span><span class="sxs-lookup"><span data-stu-id="2b875-207">Sending Email Based on an Event</span></span>](sending-e-mail-based-on-an-event.md)
</dt> <dt>

[<span data-ttu-id="2b875-208">Создание логического потребителя</span><span class="sxs-lookup"><span data-stu-id="2b875-208">Creating a Logical Consumer</span></span>](creating-a-logical-consumer.md)
</dt> <dt>

[<span data-ttu-id="2b875-209">Получение событий в любое время</span><span class="sxs-lookup"><span data-stu-id="2b875-209">Receiving Events At All Times</span></span>](receiving-events-at-all-times.md)
</dt> </dl>

 

 





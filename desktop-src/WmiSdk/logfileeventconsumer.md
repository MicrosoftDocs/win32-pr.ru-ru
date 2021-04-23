---
description: Класс Логфиливентконсумер записывает настраиваемые строки в текстовый файл журнала при доставке событий в него.
ms.assetid: 8934b60e-3763-4b85-89fd-58fe6136dff6
ms.tgt_platform: multiple
title: Класс Логфиливентконсумер
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LogFileEventConsumer
- LogFileEventConsumer.CreatorSID
- LogFileEventConsumer.MachineName
- LogFileEventConsumer.MaximumQueueSize
- LogFileEventConsumer.Filename
- LogFileEventConsumer.IsUnicode
- LogFileEventConsumer.MaximumFileSize
- LogFileEventConsumer.Name
- LogFileEventConsumer.Text
api_type:
- DllExport
api_location:
- Wbemcons.dll
ms.openlocfilehash: 462989b740aaf6a6bd78968c951b7c676038cea5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692826"
---
# <a name="logfileeventconsumer-class"></a><span data-ttu-id="b8721-103">Класс Логфиливентконсумер</span><span class="sxs-lookup"><span data-stu-id="b8721-103">LogFileEventConsumer class</span></span>

<span data-ttu-id="b8721-104">Класс **логфиливентконсумер** записывает настраиваемые строки в текстовый файл журнала при доставке событий в него.</span><span class="sxs-lookup"><span data-stu-id="b8721-104">The **LogFileEventConsumer** class writes customized strings to a text log file when events are delivered to it.</span></span> <span data-ttu-id="b8721-105">Строки разделяются символами конца строки.</span><span class="sxs-lookup"><span data-stu-id="b8721-105">The strings are separated by end-of-line sequences.</span></span> <span data-ttu-id="b8721-106">Этот класс является одним из стандартных потребителей событий, предоставляемых инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="b8721-106">This class is one of the standard event consumers that WMI provides.</span></span> <span data-ttu-id="b8721-107">Дополнительные сведения см. [в разделе Мониторинг и реагирование на события с помощью стандартных потребителей](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="b8721-107">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b8721-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b8721-108">Syntax</span></span>

``` syntax
[AMENDMENT]
class LogFileEventConsumer : __EventConsumer
{
  uint8   CreatorSID[];
  string  MachineName;
  uint32  MaximumQueueSize;
  string  Filename;
  boolean IsUnicode;
  uint64  MaximumFileSize = 65535;
  string  Name;
  string  Text;
};
```

## <a name="members"></a><span data-ttu-id="b8721-109">Члены</span><span class="sxs-lookup"><span data-stu-id="b8721-109">Members</span></span>

<span data-ttu-id="b8721-110">Класс **логфиливентконсумер** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="b8721-110">The **LogFileEventConsumer** class has these types of members:</span></span>

-   [<span data-ttu-id="b8721-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="b8721-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b8721-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="b8721-112">Properties</span></span>

<span data-ttu-id="b8721-113">Класс **логфиливентконсумер** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="b8721-113">The **LogFileEventConsumer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b8721-114">**креаторсид**</span><span class="sxs-lookup"><span data-stu-id="b8721-114">**CreatorSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8721-115">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="b8721-115">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="b8721-116">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b8721-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8721-117">Идентификатор безопасности (SID), однозначно определяющий пользователя, который создает фильтр.</span><span class="sxs-lookup"><span data-stu-id="b8721-117">Security identifier (SID) that uniquely identifies the user who creates a filter.</span></span> <span data-ttu-id="b8721-118">WMI хранит идентификатор безопасности пользователя, создающего экземпляр [**\_ \_ евентконсумер**](--eventconsumer.md) , или идентификатор безопасности администратора в зависимости от операционной системы.</span><span class="sxs-lookup"><span data-stu-id="b8721-118">WMI stores the SID of the user who creates an instance of [**\_\_EventConsumer**](--eventconsumer.md) or the Administrator SID, depending on the operating system.</span></span> <span data-ttu-id="b8721-119">Дополнительные сведения см. в статьях [Привязка фильтра событий к логическому потребителю](binding-an-event-filter-with-a-logical-consumer.md) и [мониторинг и реагирование на события с помощью стандартных потребителей](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="b8721-119">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md) and [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

<span data-ttu-id="b8721-120">Это свойство наследуется от [**\_ \_ евентконсумер**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="b8721-120">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8721-121">**Имя файла**</span><span class="sxs-lookup"><span data-stu-id="b8721-121">**Filename**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8721-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b8721-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8721-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b8721-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8721-124">Имя файла, содержащего путь к которому добавляются записи журнала.</span><span class="sxs-lookup"><span data-stu-id="b8721-124">Name of a file that includes the path to which the log entries are appended.</span></span> <span data-ttu-id="b8721-125">Если файл не существует, **логфиливентконсумер** попытается создать его.</span><span class="sxs-lookup"><span data-stu-id="b8721-125">If the file does not exist, **LogFileEventConsumer** attempts to create it.</span></span> <span data-ttu-id="b8721-126">Потребитель завершается ошибкой, если путь не существует, или когда пользователь, создавший потребитель, не имеет разрешений на запись для файла или пути.</span><span class="sxs-lookup"><span data-stu-id="b8721-126">The consumer fails when the path does not exist, or when the user who creates the consumer does not have write permissions for the file or path.</span></span>

</dd> <dt>

<span data-ttu-id="b8721-127">**Прев Юникоде**</span><span class="sxs-lookup"><span data-stu-id="b8721-127">**IsUnicode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8721-128">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="b8721-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b8721-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b8721-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8721-130">**Значение true**, если файл журнала является текстовым файлом в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="b8721-130">If **TRUE**, the log file is a Unicode text file.</span></span> <span data-ttu-id="b8721-131">Если **значение равно false**, то файл журнала является текстовым файлом многобайтового кода.</span><span class="sxs-lookup"><span data-stu-id="b8721-131">If **FALSE**, the log file is a multibyte code text file.</span></span> <span data-ttu-id="b8721-132">Если файл существует, это свойство игнорируется и используется текущий параметр файла.</span><span class="sxs-lookup"><span data-stu-id="b8721-132">If the file exists, this property is ignored and the current file setting is used.</span></span> <span data-ttu-id="b8721-133">Например **, если в параметре** IsFalse задано **значение false**, но существующий файл является файлом Юникода, то используется Юникод.</span><span class="sxs-lookup"><span data-stu-id="b8721-133">For example, if **IsUnicode** is **FALSE**, but the existing file is a Unicode file, then Unicode is used.</span></span> <span data-ttu-id="b8721-134">Если  **значение IsTrue равно true**, а файл — многобайтовый код, то используется многобайтовый код.</span><span class="sxs-lookup"><span data-stu-id="b8721-134">If **IsUnicode** is **TRUE**, but the file is multibyte code, then multibyte code is used.</span></span>

</dd> <dt>

<span data-ttu-id="b8721-135">**MachineName**</span><span class="sxs-lookup"><span data-stu-id="b8721-135">**MachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8721-136">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b8721-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8721-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b8721-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8721-138">Имя компьютера, на который инструментарий управления Windows (WMI) (WMI) отправляет события.</span><span class="sxs-lookup"><span data-stu-id="b8721-138">Name of the computer to which Windows Management Instrumentation (WMI) sends events.</span></span>

<span data-ttu-id="b8721-139">Это свойство наследуется от [**\_ \_ евентконсумер**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="b8721-139">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8721-140">**максимумфилесизе**</span><span class="sxs-lookup"><span data-stu-id="b8721-140">**MaximumFileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8721-141">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b8721-141">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b8721-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b8721-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8721-143">Максимальный размер файла журнала в байтах.</span><span class="sxs-lookup"><span data-stu-id="b8721-143">Maximum size of a log file in bytes.</span></span> <span data-ttu-id="b8721-144">Если размер первичного файла превышает максимальный, содержимое перемещается в другой файл, а первичный файл очищается.</span><span class="sxs-lookup"><span data-stu-id="b8721-144">If the primary file exceeds its maximum size, the contents are moved to a different file and the primary file is emptied.</span></span> <span data-ttu-id="b8721-145">Значение 0 (ноль) означает отсутствие ограничения на размер.</span><span class="sxs-lookup"><span data-stu-id="b8721-145">A value of 0 (zero) means there is no size limit.</span></span> <span data-ttu-id="b8721-146">Значение по умолчанию — 65 535 байт.</span><span class="sxs-lookup"><span data-stu-id="b8721-146">The default value is 65,535 bytes.</span></span> <span data-ttu-id="b8721-147">Размер файла проверяется перед операцией записи.</span><span class="sxs-lookup"><span data-stu-id="b8721-147">The size of the file is checked before a write operation.</span></span> <span data-ttu-id="b8721-148">Поэтому у вас может быть файл, размер которого немного больше заданного предела.</span><span class="sxs-lookup"><span data-stu-id="b8721-148">Therefore, you can have a file that is slightly larger than the specified size limit.</span></span> <span data-ttu-id="b8721-149">Следующая операция записи перехватывает ее и запускает новый файл.</span><span class="sxs-lookup"><span data-stu-id="b8721-149">The next write operation catches it and starts a new file.</span></span>

<span data-ttu-id="b8721-150">В следующем списке указывается структура именования для файла резервной копии.</span><span class="sxs-lookup"><span data-stu-id="b8721-150">The following list identifies the naming structure for the backup file:</span></span>

-   <span data-ttu-id="b8721-151">Если исходное имя файла — 8,3, расширение заменяется строкой в формате "001", "002" и т. д. с наименьшим числом, превышающим все ранее использованные и выбранные числа.</span><span class="sxs-lookup"><span data-stu-id="b8721-151">If the original filename is 8.3, the extension is replaced by a string in the format of "001", "002", and so on with the smallest number larger than all the previously used and chosen numbers.</span></span> <span data-ttu-id="b8721-152">Если используется значение "999", то выбранное число является наименьшим неиспользуемым числом.</span><span class="sxs-lookup"><span data-stu-id="b8721-152">If "999" is used, then the number chosen is the smallest unused number.</span></span>
-   <span data-ttu-id="b8721-153">Если исходное имя файла не 8,3, то строка в формате "001", "002" и т. д. добавляется к имени файла.</span><span class="sxs-lookup"><span data-stu-id="b8721-153">If the original filename is not 8.3, a string in the format of "001", "002", and so on is appended to the file name.</span></span>

<span data-ttu-id="b8721-154">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b8721-154">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b8721-155">**максимумкуеуесизе**</span><span class="sxs-lookup"><span data-stu-id="b8721-155">**MaximumQueueSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8721-156">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b8721-156">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b8721-157">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b8721-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8721-158">Максимальная очередь для конкретного потребителя в байтах.</span><span class="sxs-lookup"><span data-stu-id="b8721-158">Maximum queue for a specific consumer, in bytes.</span></span>

<span data-ttu-id="b8721-159">Это свойство наследуется от [**\_ \_ евентконсумер**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="b8721-159">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8721-160">**Name**</span><span class="sxs-lookup"><span data-stu-id="b8721-160">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8721-161">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b8721-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8721-162">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b8721-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8721-163">Квалификаторы: [ **ключ**](key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="b8721-163">Qualifiers: [**key**](key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="b8721-164">Уникальное имя для этого потребителя.</span><span class="sxs-lookup"><span data-stu-id="b8721-164">Unique name for this consumer.</span></span>

</dd> <dt>

<span data-ttu-id="b8721-165">**Text**</span><span class="sxs-lookup"><span data-stu-id="b8721-165">**Text**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8721-166">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b8721-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8721-167">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b8721-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8721-168">Стандартный строковый [шаблон](using-standard-string-templates.md) для текста записи журнала.</span><span class="sxs-lookup"><span data-stu-id="b8721-168">Standard string [template](using-standard-string-templates.md) for the text of a log entry.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b8721-169">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b8721-169">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b8721-170">**Логфиливентконсумер** не защищает файл журнала.</span><span class="sxs-lookup"><span data-stu-id="b8721-170">The **LogFileEventConsumer** does not secure the log file.</span></span> <span data-ttu-id="b8721-171">Поэтому при настройке **логфиливентконсумер** важно указать каталог, защищенный с учетом требуемого уровня.</span><span class="sxs-lookup"><span data-stu-id="b8721-171">Therefore, when you configure the **LogFileEventConsumer**, it is important to specify a directory that is secured to the level that you require.</span></span>

 

<span data-ttu-id="b8721-172">Класс **логфиливентконсумер** является производным от абстрактного класса [**\_ \_ евентконсумер**](--eventconsumer.md) .</span><span class="sxs-lookup"><span data-stu-id="b8721-172">The **LogFileEventConsumer** class is derived from the [**\_\_EventConsumer**](--eventconsumer.md) abstract class.</span></span>

## <a name="examples"></a><span data-ttu-id="b8721-173">Примеры</span><span class="sxs-lookup"><span data-stu-id="b8721-173">Examples</span></span>

<span data-ttu-id="b8721-174">Пример использования **логфиливентконсумер** для создания потребителя см. в разделе [запись в файл журнала на основе события](writing-to-a-log-file-based-on-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="b8721-174">For an example of using **LogFileEventConsumer** to create a consumer, see [Writing to a Log File Based on an Event](writing-to-a-log-file-based-on-an-event.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b8721-175">Требования</span><span class="sxs-lookup"><span data-stu-id="b8721-175">Requirements</span></span>



| <span data-ttu-id="b8721-176">Требование</span><span class="sxs-lookup"><span data-stu-id="b8721-176">Requirement</span></span> | <span data-ttu-id="b8721-177">Значение</span><span class="sxs-lookup"><span data-stu-id="b8721-177">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8721-178">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b8721-178">Minimum supported client</span></span><br/> | <span data-ttu-id="b8721-179">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b8721-179">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b8721-180">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b8721-180">Minimum supported server</span></span><br/> | <span data-ttu-id="b8721-181">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b8721-181">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b8721-182">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b8721-182">Namespace</span></span><br/>                | <span data-ttu-id="b8721-183">Корневая \\ Подписка</span><span class="sxs-lookup"><span data-stu-id="b8721-183">Root\\subscription</span></span><br/>                                                           |
| <span data-ttu-id="b8721-184">MOF</span><span class="sxs-lookup"><span data-stu-id="b8721-184">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b8721-185"><dt>Вбемконс. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b8721-185"><dt>Wbemcons.mof</dt></span></span> </dl> |
| <span data-ttu-id="b8721-186">DLL</span><span class="sxs-lookup"><span data-stu-id="b8721-186">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8721-187"><dt>Wbemcons.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8721-187"><dt>Wbemcons.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8721-188">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b8721-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8721-189">Классы стандартных потребителей</span><span class="sxs-lookup"><span data-stu-id="b8721-189">Standard Consumer Classes</span></span>](standard-consumer-classes.md)
</dt> <dt>

[<span data-ttu-id="b8721-190">Запись в файл журнала на основе события</span><span class="sxs-lookup"><span data-stu-id="b8721-190">Writing to a Log File Based on an Event</span></span>](writing-to-a-log-file-based-on-an-event.md)
</dt> <dt>

[<span data-ttu-id="b8721-191">Создание логического потребителя</span><span class="sxs-lookup"><span data-stu-id="b8721-191">Creating a Logical Consumer</span></span>](creating-a-logical-consumer.md)
</dt> <dt>

[<span data-ttu-id="b8721-192">Получение событий в любое время</span><span class="sxs-lookup"><span data-stu-id="b8721-192">Receiving Events At All Times</span></span>](receiving-events-at-all-times.md)
</dt> <dt>

[<span data-ttu-id="b8721-193">**\_\_евентконсумер**</span><span class="sxs-lookup"><span data-stu-id="b8721-193">**\_\_EventConsumer**</span></span>](--eventconsumer.md)
</dt> </dl>

 


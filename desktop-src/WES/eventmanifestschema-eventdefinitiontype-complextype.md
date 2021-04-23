---
title: Сложный тип Евентдефинитионтипе
description: Определяет событие, которое может записывать поставщик.
ms.assetid: 09ea89c9-6618-4874-ac72-5ee19cde4040
keywords:
- Журнал событий сложных типов Евентдефинитионтипе
topic_type:
- apiref
api_name:
- EventDefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b7719abea1e97cae88edd47d176e5c578d73f0b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691960"
---
# <a name="eventdefinitiontype-complex-type"></a><span data-ttu-id="55559-104">Сложный тип Евентдефинитионтипе</span><span class="sxs-lookup"><span data-stu-id="55559-104">EventDefinitionType Complex Type</span></span>

<span data-ttu-id="55559-105">Определяет событие, которое может записывать поставщик.</span><span class="sxs-lookup"><span data-stu-id="55559-105">Defines an event that your provider can write.</span></span>

``` syntax
<xs:complexType name="EventDefinitionType">
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="value"
                type="UInt32Type"
                use="required"
             />
            <xs:attribute name="level"
                type="QName"
                use="optional"
             />
            <xs:attribute name="template"
                type="token"
                use="optional"
             />
            <xs:attribute name="channel"
                type="token"
                use="optional"
             />
            <xs:attribute name="keywords"
                type="QNameList"
                use="optional"
             />
            <xs:attribute name="task"
                type="QName"
                use="optional"
             />
            <xs:attribute name="opcode"
                type="QName"
                use="optional"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
            <xs:attribute name="version"
                type="unsignedByte"
                use="optional"
             />
            <xs:attribute name="message"
                type="strTableRef"
                use="optional"
             />
            <xs:attribute name="notLogged"
                type="boolean"
                use="optional"
                default="false"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="55559-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="55559-106">Attributes</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="55559-107">Имя</span><span class="sxs-lookup"><span data-stu-id="55559-107">Name</span></span></th>
<th><span data-ttu-id="55559-108">Тип</span><span class="sxs-lookup"><span data-stu-id="55559-108">Type</span></span></th>
<th><span data-ttu-id="55559-109">Описание</span><span class="sxs-lookup"><span data-stu-id="55559-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="55559-110">channel</span><span class="sxs-lookup"><span data-stu-id="55559-110">channel</span></span></td>
<td><span data-ttu-id="55559-111">token</span><span class="sxs-lookup"><span data-stu-id="55559-111">token</span></span></td>
<td><span data-ttu-id="55559-112">Идентификатор, определяющий канал, на который записывается событие.</span><span class="sxs-lookup"><span data-stu-id="55559-112">An identifier that identifies the channel to where the event is written.</span></span> <span data-ttu-id="55559-113">Укажите идентификатор канала одного из определенных или импортированных каналов.</span><span class="sxs-lookup"><span data-stu-id="55559-113">Specify a channel identifier of one of the channels that you defined or imported.</span></span> <span data-ttu-id="55559-114">Если канал не указывает идентификатор канала, используйте имя канала.</span><span class="sxs-lookup"><span data-stu-id="55559-114">If the channel does not specify a channel identifier, use the channel's name.</span></span> <span data-ttu-id="55559-115">Дополнительные сведения об определении или импорте канала см. в описании сложного типа <a href="eventmanifestschema-channellisttype-complextype.md"><strong>чаннеллисттипе</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="55559-115">For details on defining or importing a channel, see the <a href="eventmanifestschema-channellisttype-complextype.md"><strong>ChannelListType</strong></a> complex type.</span></span><br/> <span data-ttu-id="55559-116">Если канал не указан, событие не записывается в канал.</span><span class="sxs-lookup"><span data-stu-id="55559-116">If you do not specify a channel, the event is not written to a channel.</span></span> <span data-ttu-id="55559-117">Как правило, единственной причиной, по которой не нужно указывать канал, является запись событий только в сеанс ETW.</span><span class="sxs-lookup"><span data-stu-id="55559-117">Typically, the only reason not to specify a channel is if you are writing events only to an ETW session.</span></span> <span data-ttu-id="55559-118">Дополнительные сведения см. в разделе Управление сеансами <a href="/windows/desktop/ETW/controlling-event-tracing-sessions">трассировки событий</a>Windows.</span><span class="sxs-lookup"><span data-stu-id="55559-118">For details, see creating an ETW session, see <a href="/windows/desktop/ETW/controlling-event-tracing-sessions">Controlling Event Tracing Sessions</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="55559-119">keywords</span><span class="sxs-lookup"><span data-stu-id="55559-119">keywords</span></span></td>
<td><span data-ttu-id="55559-120"><a href="eventmanifestschema-qnamelist-simpletype.md"><strong>кнамелист</strong></a></span><span class="sxs-lookup"><span data-stu-id="55559-120"><a href="eventmanifestschema-qnamelist-simpletype.md"><strong>QNameList</strong></a></span></span></td>
<td><span data-ttu-id="55559-121">Разделенный пробелами список имен ключевых слов, которые определяют категорию событий, к которым относится это событие.</span><span class="sxs-lookup"><span data-stu-id="55559-121">A space-separated list of keyword names that identify the category of events to which this event belongs.</span></span> <span data-ttu-id="55559-122">Укажите имя ключевого слова из списка определяемых вами ключевых слов.</span><span class="sxs-lookup"><span data-stu-id="55559-122">Specify a keyword name from the list of keywords that you define.</span></span> <span data-ttu-id="55559-123">Дополнительные сведения об определении ключевых слов см. в описании сложного типа <a href="eventmanifestschema-keywordtype-complextype.md"><strong>кэйвордтипе</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="55559-123">For details on defining keywords, see the <a href="eventmanifestschema-keywordtype-complextype.md"><strong>KeywordType</strong></a> complex type.</span></span><br/> <span data-ttu-id="55559-124">Если не указать ключевые слова, то дескриптор события будет содержать ноль для ключевых слов.</span><span class="sxs-lookup"><span data-stu-id="55559-124">If you do not specify keywords, the event descriptor will contain a zero for keywords.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="55559-125">уровень</span><span class="sxs-lookup"><span data-stu-id="55559-125">level</span></span></td>
<td><span data-ttu-id="55559-126"><strong>QName</strong></span><span class="sxs-lookup"><span data-stu-id="55559-126"><strong>QName</strong></span></span></td>
<td><span data-ttu-id="55559-127">Уровень детализации, используемый при записи события.</span><span class="sxs-lookup"><span data-stu-id="55559-127">The level of verbosity to use when writing the event.</span></span> <span data-ttu-id="55559-128">Укажите имя уровня, определенного в манифесте, или одного из уровней, определенных в \Include\Winmeta.xml файле, включенном в Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="55559-128">Specify the name of a level that you defined in the manifest or one of the levels defined in the \Include\Winmeta.xml file that is included in the Windows SDK.</span></span> <span data-ttu-id="55559-129">Дополнительные сведения об определении уровня см. в разделе сложный тип <a href="eventmanifestschema-leveltype-complextype.md"><strong>левелтипе</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="55559-129">For details on defining a level, see the <a href="eventmanifestschema-leveltype-complextype.md"><strong>LevelType</strong></a> complex type.</span></span><br/> <span data-ttu-id="55559-130">Если уровень не указан, дескриптор события будет содержать ноль для Level.</span><span class="sxs-lookup"><span data-stu-id="55559-130">If you do not specify a level, the event descriptor will contain a zero for level.</span></span><br/> <span data-ttu-id="55559-131">Необходимо указать уровень, если тип канала, на который записано событие, — Admin; уровень должен быть одним из следующих уровней, определенных в Winmeata.xml:</span><span class="sxs-lookup"><span data-stu-id="55559-131">You must specify a level if the channel type to which the event is written is Admin; the level must be one of the following levels defined in Winmeata.xml:</span></span>
<ul>
<li><span data-ttu-id="55559-132">win:Critical</span><span class="sxs-lookup"><span data-stu-id="55559-132">win:Critical</span></span></li>
<li><span data-ttu-id="55559-133">win:Error</span><span class="sxs-lookup"><span data-stu-id="55559-133">win:Error</span></span></li>
<li><span data-ttu-id="55559-134">win:Warning</span><span class="sxs-lookup"><span data-stu-id="55559-134">win:Warning</span></span></li>
<li><span data-ttu-id="55559-135">win:Informational</span><span class="sxs-lookup"><span data-stu-id="55559-135">win:Informational</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="55559-136">message</span><span class="sxs-lookup"><span data-stu-id="55559-136">message</span></span></td>
<td><span data-ttu-id="55559-137"><a href="eventmanifestschema-strtableref-simpletype.md"><strong>стртаблереф</strong></a></span><span class="sxs-lookup"><span data-stu-id="55559-137"><a href="eventmanifestschema-strtableref-simpletype.md"><strong>strTableRef</strong></a></span></span></td>
<td><span data-ttu-id="55559-138">Локализованное сообщение для события.</span><span class="sxs-lookup"><span data-stu-id="55559-138">The localized message for the event.</span></span> <span data-ttu-id="55559-139">Строка сообщения ссылается на локализованную строку в разделе " <a href="eventmanifestschema-stringtable-resources-element.md"><strong>STRINGTABLE</strong></a> " манифеста.</span><span class="sxs-lookup"><span data-stu-id="55559-139">The message string references a localized string in the <a href="eventmanifestschema-stringtable-resources-element.md"><strong>stringTable</strong></a> section of the manifest.</span></span><br/> <span data-ttu-id="55559-140">Необходимо указать сообщение, если тип канала, на который написано событие, — admin.</span><span class="sxs-lookup"><span data-stu-id="55559-140">You must specify a message if the channel type to which the event is written is Admin.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="55559-141">нотлогжед</span><span class="sxs-lookup"><span data-stu-id="55559-141">notLogged</span></span></td>
<td><span data-ttu-id="55559-142">Логическое</span><span class="sxs-lookup"><span data-stu-id="55559-142">boolean</span></span></td>
<td><span data-ttu-id="55559-143">Определяет, регистрирует ли поставщик это событие.</span><span class="sxs-lookup"><span data-stu-id="55559-143">Determines whether the provider logs this event.</span></span> <span data-ttu-id="55559-144">Укажите значение true, если поставщик регистрирует это событие; в противном случае — значение false.</span><span class="sxs-lookup"><span data-stu-id="55559-144">Specify true if the provider logs this event; otherwise, false.</span></span> <span data-ttu-id="55559-145">Используйте этот атрибут, чтобы указать, что поставщик больше не регистрирует это событие вместо удаления события из манифеста.</span><span class="sxs-lookup"><span data-stu-id="55559-145">Use this attribute to indicate that the provider is no longer logging this event instead of removing the event from the manifest.</span></span> <span data-ttu-id="55559-146">При хранении события в манифесте пользователи смогут декодировать старые ETL-файлы, включающие событие.</span><span class="sxs-lookup"><span data-stu-id="55559-146">Retaining the event in the manifest will let consumers decode older etl files that include the event.</span></span><br/> <span data-ttu-id="55559-147"><strong>Windows Server 2008 и Windows Vista:</strong> Этот атрибут не поддерживается в версиях компилятора сообщений, поставляемых до версии Windows 7 Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="55559-147"><strong>Windows Server 2008 and Windows Vista:</strong> This attribute is not supported in versions of the message compiler that shipped prior to the Windows 7 version of the Windows SDK.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="55559-148">транслируют</span><span class="sxs-lookup"><span data-stu-id="55559-148">opcode</span></span></td>
<td><span data-ttu-id="55559-149"><strong>QName</strong></span><span class="sxs-lookup"><span data-stu-id="55559-149"><strong>QName</strong></span></span></td>
<td><span data-ttu-id="55559-150">Имя кода операции, определяющего операцию в задаче.</span><span class="sxs-lookup"><span data-stu-id="55559-150">The name of an opcode that identifies an operation within the task.</span></span> <span data-ttu-id="55559-151">Укажите имя кода операции, определенного в манифесте, или одного из кодов операций, определенных в Winmeta.xml.</span><span class="sxs-lookup"><span data-stu-id="55559-151">Specify the name of an opcode that you defined in the manifest or one of the opcodes defined in Winmeta.xml.</span></span> <span data-ttu-id="55559-152">Дополнительные сведения об определении кода операции см. в разделе сложный тип <a href="eventmanifestschema-opcodetype-complextype.md"><strong>опкодетипе</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="55559-152">For details on defining an opcode, see the <a href="eventmanifestschema-opcodetype-complextype.md"><strong>OpcodeType</strong></a> complex type.</span></span><br/> <span data-ttu-id="55559-153">Если задача, на которую указывает ссылка, содержит операции (локальные) для конкретных задач, можно указать один из его специфических кодов задач или код операции, определенный на уровне поставщика (Глобальный код операции).</span><span class="sxs-lookup"><span data-stu-id="55559-153">If the task that you reference contains task-specific (local) opcodes, you can specify one of its task-specific opcodes or an opcode defined at the provider level (a global opcode).</span></span> <span data-ttu-id="55559-154">При указании глобального кода операции значение глобального кода операции не может совпадать с одним из локальных кодов операций для задачи.</span><span class="sxs-lookup"><span data-stu-id="55559-154">If you specify a global opcode, the value of the global opcode cannot be the same as one of the local opcodes for the task.</span></span><br/> <span data-ttu-id="55559-155">Если вы ссылаетесь на локальный код операции, атрибут Task должен ссылаться на задачу, которой принадлежит локальный код операции.</span><span class="sxs-lookup"><span data-stu-id="55559-155">If you reference a local opcode, the task attribute must reference the task to which the local opcode belongs.</span></span><br/> <span data-ttu-id="55559-156">Если не указать код операции, то дескриптор события будет содержать ноль для кода операции.</span><span class="sxs-lookup"><span data-stu-id="55559-156">If you do not specify an opcode, the event descriptor will contain a zero for opcode.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="55559-157">символ</span><span class="sxs-lookup"><span data-stu-id="55559-157">symbol</span></span></td>
<td><span data-ttu-id="55559-158"><a href="eventmanifestschema-csymboltype-simpletype.md"><strong>ксимболтипе</strong></a></span><span class="sxs-lookup"><span data-stu-id="55559-158"><a href="eventmanifestschema-csymboltype-simpletype.md"><strong>CSymbolType</strong></a></span></span></td>
<td><span data-ttu-id="55559-159">Символ, используемый для ссылки на дескриптор события для этого события в приложении.</span><span class="sxs-lookup"><span data-stu-id="55559-159">The symbol to use to reference the event descriptor for this event in your application.</span></span> <span data-ttu-id="55559-160"><a href="message-compiler--mc-exe-.md"><strong>Компилятор сообщений (MC.exe)</strong></a> использует символ, чтобы создать константу для дескриптора события в файле заголовка, создаваемом компилятором.</span><span class="sxs-lookup"><span data-stu-id="55559-160">The <a href="message-compiler--mc-exe-.md"><strong>Message Compiler (MC.exe)</strong></a> uses the symbol to create a constant for the event descriptor in the header file that the compiler generates.</span></span> <span data-ttu-id="55559-161">Если не указать символ, компилятор создаст его.</span><span class="sxs-lookup"><span data-stu-id="55559-161">If you do not specify a symbol, the compiler generates one for you.</span></span> <span data-ttu-id="55559-162">Дескриптор используется при вызове функции <a href="/windows/desktop/api/evntprov/nf-evntprov-eventwrite"><strong>EventWrite</strong></a> для записи события.</span><span class="sxs-lookup"><span data-stu-id="55559-162">You use the descriptor when you call the <a href="/windows/desktop/api/evntprov/nf-evntprov-eventwrite"><strong>EventWrite</strong></a> function to write the event.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="55559-163">задача</span><span class="sxs-lookup"><span data-stu-id="55559-163">task</span></span></td>
<td><span data-ttu-id="55559-164"><strong>QName</strong></span><span class="sxs-lookup"><span data-stu-id="55559-164"><strong>QName</strong></span></span></td>
<td><span data-ttu-id="55559-165">Имя задачи, определяющей компонент или подкомпонент, который создает это событие.</span><span class="sxs-lookup"><span data-stu-id="55559-165">The name of a task that identifies the component or subcomponent that generates this event.</span></span> <span data-ttu-id="55559-166">Укажите имя задачи, определенной в манифесте.</span><span class="sxs-lookup"><span data-stu-id="55559-166">Specify the name of a task that you defined in the manifest.</span></span> <span data-ttu-id="55559-167">Дополнительные сведения об определении задачи см. в описании сложного типа <a href="eventmanifestschema-tasktype-complextype.md"><strong>TaskType</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="55559-167">For details on defining a task, see the <a href="eventmanifestschema-tasktype-complextype.md"><strong>TaskType</strong></a> complex type.</span></span><br/> <span data-ttu-id="55559-168">Если задача не указана, то дескриптор события будет содержать ноль для задачи.</span><span class="sxs-lookup"><span data-stu-id="55559-168">If you do not specify a task, the event descriptor will contain a zero for task.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="55559-169">шаблон</span><span class="sxs-lookup"><span data-stu-id="55559-169">template</span></span></td>
<td><span data-ttu-id="55559-170">token</span><span class="sxs-lookup"><span data-stu-id="55559-170">token</span></span></td>
<td><span data-ttu-id="55559-171">Идентификатор шаблона шаблона, который определяет элементы данных, включаемые в это событие.</span><span class="sxs-lookup"><span data-stu-id="55559-171">The template identifier of the template that defines the data items that this event includes.</span></span> <span data-ttu-id="55559-172">Укажите идентификатор шаблона, определенного в манифесте.</span><span class="sxs-lookup"><span data-stu-id="55559-172">Specify the identifier of a template that you defined in the manifest.</span></span> <span data-ttu-id="55559-173">Дополнительные сведения об определении шаблона см. в разделе сложный тип <a href="eventmanifestschema-templateitemtype-complextype.md"><strong>темплатеитемтипе</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="55559-173">For details on defining a template, see the <a href="eventmanifestschema-templateitemtype-complextype.md"><strong>TemplateItemType</strong></a> complex type.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="55559-174">значение</span><span class="sxs-lookup"><span data-stu-id="55559-174">value</span></span></td>
<td><span data-ttu-id="55559-175"><a href="eventmanifestschema-hexint32type-simpletype.md"><strong>UInt32Type</strong></a></span><span class="sxs-lookup"><span data-stu-id="55559-175"><a href="eventmanifestschema-hexint32type-simpletype.md"><strong>UInt32Type</strong></a></span></span></td>
<td><span data-ttu-id="55559-176">Идентификатор события.</span><span class="sxs-lookup"><span data-stu-id="55559-176">The event identifier.</span></span> <span data-ttu-id="55559-177">Идентификатор должен быть уникальным в пределах списка определяемых вами событий.</span><span class="sxs-lookup"><span data-stu-id="55559-177">The identifier must be unique within the list of events that you define.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="55559-178">version</span><span class="sxs-lookup"><span data-stu-id="55559-178">version</span></span></td>
<td><span data-ttu-id="55559-179">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="55559-179">unsignedByte</span></span></td>
<td><span data-ttu-id="55559-180">Однобайтовый номер версии определения события.</span><span class="sxs-lookup"><span data-stu-id="55559-180">A one-byte version number of the event definition.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="55559-181">Комментарии</span><span class="sxs-lookup"><span data-stu-id="55559-181">Remarks</span></span>

<span data-ttu-id="55559-182">Если для форматирования строки сообщения для события используется [**евтформатмессаже**](/windows/desktop/api/WinEvt/nf-winevt-evtformatmessage) (или Просмотр событий для просмотра строки сообщения), строка сообщения может содержать строки вставки и любые строки формата, поддерживаемые функцией Win32 **FormatMessage** .</span><span class="sxs-lookup"><span data-stu-id="55559-182">If you use [**EvtFormatMessage**](/windows/desktop/api/WinEvt/nf-winevt-evtformatmessage) to format the message string for the event (or use the Event Viewer to view the message string), the message string can contain insertion strings and any of the format strings that the Win32 **FormatMessage** function supports.</span></span> <span data-ttu-id="55559-183">Строки вставки ограничены%*n* или%*n*! s!</span><span class="sxs-lookup"><span data-stu-id="55559-183">The insertion strings are limited to %*n* or %*n*!s!</span></span> <span data-ttu-id="55559-184">(например, %1), где *n* — это односторонняя ссылка на элементы данных, определенные в шаблоне события.</span><span class="sxs-lookup"><span data-stu-id="55559-184">(for example, %1) where *n* is the one-based reference the data items defined in the event's template.</span></span> <span data-ttu-id="55559-185">Строка сообщения также может содержать строки вставки параметров в форме%%*n* (например,% %4).</span><span class="sxs-lookup"><span data-stu-id="55559-185">The message string can also contain parameter insertion strings in the form %%*n* (for example, %%4).</span></span> <span data-ttu-id="55559-186">Максимальное число строк вставки, которое может содержать сообщение, — 100.</span><span class="sxs-lookup"><span data-stu-id="55559-186">The maximum number of insertion strings that the message can contain is 100.</span></span>

## <a name="requirements"></a><span data-ttu-id="55559-187">Требования</span><span class="sxs-lookup"><span data-stu-id="55559-187">Requirements</span></span>



| <span data-ttu-id="55559-188">Требование</span><span class="sxs-lookup"><span data-stu-id="55559-188">Requirement</span></span> | <span data-ttu-id="55559-189">Значение</span><span class="sxs-lookup"><span data-stu-id="55559-189">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="55559-190">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="55559-190">Minimum supported client</span></span><br/> | <span data-ttu-id="55559-191">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="55559-191">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="55559-192">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="55559-192">Minimum supported server</span></span><br/> | <span data-ttu-id="55559-193">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="55559-193">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 


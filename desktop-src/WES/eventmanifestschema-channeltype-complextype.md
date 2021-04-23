---
title: Сложный тип Чаннелтипе
description: Определяет канал, к которому поставщики могут регистрировать события.
ms.assetid: 882506e5-222b-45c8-af4b-59db8baa1dae
keywords:
- Журнал событий сложных типов Чаннелтипе
topic_type:
- apiref
api_name:
- ChannelType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 81158306285631748830d8aaaaf9cf329d7c0af1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492036"
---
# <a name="channeltype-complex-type"></a><span data-ttu-id="6aab1-104">Сложный тип Чаннелтипе</span><span class="sxs-lookup"><span data-stu-id="6aab1-104">ChannelType Complex Type</span></span>

<span data-ttu-id="6aab1-105">Определяет канал, к которому поставщики могут регистрировать события.</span><span class="sxs-lookup"><span data-stu-id="6aab1-105">Defines a channel to which providers can log events.</span></span>

``` syntax
<xs:complexType name="ChannelType"
    mixed="true"
>
    <xs:sequence>
        <xs:element name="logging"
            type="ChannelLoggingType"
            minOccurs="0"
         />
        <xs:element name="publishing"
            type="ChannelPublishingType"
            minOccurs="0"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="anyURI"
        use="required"
     />
    <xs:attribute name="chid"
        type="token"
        use="optional"
     />
    <xs:attribute name="type"
        type="string"
        use="required"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="optional"
     />
    <xs:attribute name="access"
        type="string"
        use="optional"
     />
    <xs:attribute name="isolation"
        type="string"
        use="optional"
     />
    <xs:attribute name="enabled"
        type="boolean"
        default="false"
        use="optional"
     />
    <xs:attribute name="value"
        type="UInt8Type"
        use="optional"
     />
    <xs:attribute name="message"
        type="string"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="6aab1-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="6aab1-106">Child elements</span></span>



| <span data-ttu-id="6aab1-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="6aab1-107">Element</span></span>                                                                  | <span data-ttu-id="6aab1-108">Тип</span><span class="sxs-lookup"><span data-stu-id="6aab1-108">Type</span></span>                                                                                   | <span data-ttu-id="6aab1-109">Описание</span><span class="sxs-lookup"><span data-stu-id="6aab1-109">Description</span></span>                                                                                                                                                                                                |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6aab1-110">**Подробности**</span><span class="sxs-lookup"><span data-stu-id="6aab1-110">**logging**</span></span>](eventmanifestschema-logging-channeltype-element.md)       | [<span data-ttu-id="6aab1-111">**чаннеллоггингтипе**</span><span class="sxs-lookup"><span data-stu-id="6aab1-111">**ChannelLoggingType**</span></span>](eventmanifestschema-channelloggingtype-complextype.md)       | <span data-ttu-id="6aab1-112">Определяет свойства файла журнала, который осуществляет резервное копирование канала, например его емкость, а также указывает, является ли файл журнала последовательным или циклическим.</span><span class="sxs-lookup"><span data-stu-id="6aab1-112">Defines the properties of the log file that backs the channel, such as its capacity and whether the log file is sequential or circular.</span></span><br/>                                                         |
| [<span data-ttu-id="6aab1-113">**Publish**</span><span class="sxs-lookup"><span data-stu-id="6aab1-113">**publishing**</span></span>](eventmanifestschema-publishing-channeltype-element.md) | [<span data-ttu-id="6aab1-114">**чаннелпублишингтипе**</span><span class="sxs-lookup"><span data-stu-id="6aab1-114">**ChannelPublishingType**</span></span>](eventmanifestschema-channelpublishingtype-complextype.md) | <span data-ttu-id="6aab1-115">Определяет свойства ведения журнала для сеанса, используемого каналом.</span><span class="sxs-lookup"><span data-stu-id="6aab1-115">Defines the logging properties for the session that the channel uses.</span></span> <span data-ttu-id="6aab1-116">Свойства ведения журнала для сеанса могут указываться только в отладочных и аналитических каналах и каналах, использующих пользовательскую изоляцию.</span><span class="sxs-lookup"><span data-stu-id="6aab1-116">Only Debug and Analytic channels and channels that use Custom isolation can specify logging properties for their session.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="6aab1-117">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="6aab1-117">Attributes</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6aab1-118">Имя</span><span class="sxs-lookup"><span data-stu-id="6aab1-118">Name</span></span></th>
<th><span data-ttu-id="6aab1-119">Тип</span><span class="sxs-lookup"><span data-stu-id="6aab1-119">Type</span></span></th>
<th><span data-ttu-id="6aab1-120">Описание</span><span class="sxs-lookup"><span data-stu-id="6aab1-120">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6aab1-121">access</span><span class="sxs-lookup"><span data-stu-id="6aab1-121">access</span></span></td>
<td><span data-ttu-id="6aab1-122">строка</span><span class="sxs-lookup"><span data-stu-id="6aab1-122">string</span></span></td>
<td><span data-ttu-id="6aab1-123">Дескриптор доступа на <a href="/windows/desktop/SecAuthZ/security-descriptor-definition-language">языке определения дескрипторов безопасности</a> (SDDL), который управляет доступом к файлу журнала, который производит резервное копирование канала.</span><span class="sxs-lookup"><span data-stu-id="6aab1-123">A <a href="/windows/desktop/SecAuthZ/security-descriptor-definition-language">Security Descriptor Definition Language</a> (SDDL) access descriptor that controls access to the log file that backs the channel.</span></span> <span data-ttu-id="6aab1-124">Если для атрибута <strong>изоляции</strong> задано значение Application или System, то дескриптор доступа управляет доступом для чтения к файлу (разрешения на запись игнорируются).</span><span class="sxs-lookup"><span data-stu-id="6aab1-124">If the <strong>isolation</strong> attribute is set to Application or System, the access descriptor controls read access to the file (the write permissions are ignored).</span></span> <span data-ttu-id="6aab1-125">Если для атрибута <strong>изоляции</strong> задано значение Custom, дескриптор доступа управляет доступом на запись к каналу и доступ для чтения к файлу.</span><span class="sxs-lookup"><span data-stu-id="6aab1-125">If the <strong>isolation</strong> attribute is set to Custom, the access descriptor controls write access to the channel and read access to the file.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6aab1-126">чид</span><span class="sxs-lookup"><span data-stu-id="6aab1-126">chid</span></span></td>
<td><span data-ttu-id="6aab1-127">token</span><span class="sxs-lookup"><span data-stu-id="6aab1-127">token</span></span></td>
<td><span data-ttu-id="6aab1-128">Идентификатор, который уникальным образом идентифицирует канал в списке каналов, определяемых или импортируемых поставщиком.</span><span class="sxs-lookup"><span data-stu-id="6aab1-128">An identifier that uniquely identifies the channel in the list of channels that the provider defines or imports.</span></span> <span data-ttu-id="6aab1-129">Используйте это значение при ссылке на канал в событии.</span><span class="sxs-lookup"><span data-stu-id="6aab1-129">Use this value when referencing the channel in an event.</span></span> <span data-ttu-id="6aab1-130">Если идентификатор канала не указан, используйте имя канала для ссылки на этот канал в определении события.</span><span class="sxs-lookup"><span data-stu-id="6aab1-130">If you do not specify a channel identifier, use the channel's name to reference this channel in an event definition.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6aab1-131">Включено</span><span class="sxs-lookup"><span data-stu-id="6aab1-131">enabled</span></span></td>
<td><span data-ttu-id="6aab1-132">Логическое</span><span class="sxs-lookup"><span data-stu-id="6aab1-132">boolean</span></span></td>
<td><span data-ttu-id="6aab1-133">Определяет, включен ли канал.</span><span class="sxs-lookup"><span data-stu-id="6aab1-133">Determines whether the channel is enabled.</span></span> <span data-ttu-id="6aab1-134">Задайте значение <strong>true</strong> , чтобы разрешить ведение журнала для канала. в противном случае — <strong>значение false</strong>.</span><span class="sxs-lookup"><span data-stu-id="6aab1-134">Set to <strong>true</strong> to allow logging to the channel; otherwise, <strong>false</strong>.</span></span> <span data-ttu-id="6aab1-135">Значение по умолчанию — <strong>false</strong> (ведение журнала отключено).</span><span class="sxs-lookup"><span data-stu-id="6aab1-135">The default is <strong>false</strong> (logging is disabled).</span></span><br/> <span data-ttu-id="6aab1-136">Так как типы каналов отладки и аналитики являются каналами большого объема, необходимо включить канал только при исследовании проблемы с компонентом, записывающим данные в этот канал. в противном случае канал должен оставаться отключенным.</span><span class="sxs-lookup"><span data-stu-id="6aab1-136">Because Debug and Analytic channel types are high volume channels, you should enable the channel only when investigating an issue with a component that writes to that channel; otherwise, the channel should remain disabled.</span></span><br/> <span data-ttu-id="6aab1-137">Каждый раз, когда вы включаете канал отладки и анализа, служба удаляет события из канала.</span><span class="sxs-lookup"><span data-stu-id="6aab1-137">Each time you enable a Debug and Analytic channel, the service clears the events from the channel.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6aab1-138">изоляция</span><span class="sxs-lookup"><span data-stu-id="6aab1-138">isolation</span></span></td>
<td><span data-ttu-id="6aab1-139">строка</span><span class="sxs-lookup"><span data-stu-id="6aab1-139">string</span></span></td>
<td><span data-ttu-id="6aab1-140">Значение изоляции определяет разрешения на доступ по умолчанию для канала.</span><span class="sxs-lookup"><span data-stu-id="6aab1-140">The isolation value defines the default access permissions for the channel.</span></span> <span data-ttu-id="6aab1-141">Можно указать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="6aab1-141">You can specify one of the following values:</span></span>
<ul>
<li><span data-ttu-id="6aab1-142"><strong>Приложение</strong></span><span class="sxs-lookup"><span data-stu-id="6aab1-142"><strong>Application</strong></span></span></li>
<li><span data-ttu-id="6aab1-143"><strong>Система</strong></span><span class="sxs-lookup"><span data-stu-id="6aab1-143"><strong>System</strong></span></span></li>
<li><span data-ttu-id="6aab1-144"><strong>Пользовательский</strong></span><span class="sxs-lookup"><span data-stu-id="6aab1-144"><strong>Custom</strong></span></span></li>
</ul>
<span data-ttu-id="6aab1-145">Изоляция по умолчанию — <strong>Application</strong>.</span><span class="sxs-lookup"><span data-stu-id="6aab1-145">The default isolation is <strong>Application</strong>.</span></span> <span data-ttu-id="6aab1-146">Разрешения по умолчанию для <strong>приложения</strong> (показаны с помощью SDDL):</span><span class="sxs-lookup"><span data-stu-id="6aab1-146">The default permissions for <strong>Application</strong> are (shown using SDDL):</span></span> <br/> <span data-codelanguage="Text"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6aab1-147">Текст</span><span class="sxs-lookup"><span data-stu-id="6aab1-147">Text</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>            L&quot;O:BAG:SYD:&quot;
            L&quot;(A;;0xf0007;;;SY)&quot;                // local system               (read, write, clear)
            L&quot;(A;;0x7;;;BA)&quot;                    // built-in admins            (read, write, clear)
            L&quot;(A;;0x7;;;SO)&quot;                    // server operators           (read, write, clear)
            L&quot;(A;;0x3;;;IU)&quot;                    // INTERACTIVE LOGON          (read, write)
            L&quot;(A;;0x3;;;SU)&quot;                    // SERVICES LOGON             (read, write)
            L&quot;(A;;0x3;;;S-1-5-3)&quot;               // BATCH LOGON                (read, write)
            L&quot;(A;;0x3;;;S-1-5-33)&quot;              // write restricted service   (read, write)
            L&quot;(A;;0x1;;;S-1-5-32-573)&quot;;         // event log readers          (read) </code></pre></td>
</tr>
</tbody>
</table>

<p><span data-ttu-id="6aab1-148">Разрешения по умолчанию для <strong>System</strong> (показаны с помощью SDDL):</span><span class="sxs-lookup"><span data-stu-id="6aab1-148">The default permissions for <strong>System</strong> are (shown using SDDL):</span></span></p>
<div class="code">
<span data-codelanguage="Text"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6aab1-149">Текст</span><span class="sxs-lookup"><span data-stu-id="6aab1-149">Text</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>            L&quot;O:BAG:SYD:&quot;
            L&quot;(A;;0xf0007;;;SY)&quot;                // local system             (read, write, clear)
            L&quot;(A;;0x7;;;BA)&quot;                    // built-in admins          (read, write, clear)
            L&quot;(A;;0x3;;;BO)&quot;                    // backup operators         (read, write)
            L&quot;(A;;0x5;;;SO)&quot;                    // server operators         (read, clear) 
            L&quot;(A;;0x1;;;IU)&quot;                    // INTERACTIVE LOGON        (read)
            L&quot;(A;;0x3;;;SU)&quot;                    // SERVICES LOGON           (read, write)
            L&quot;(A;;0x1;;;S-1-5-3)&quot;               // BATCH LOGON              (read)
            L&quot;(A;;0x2;;;S-1-5-33)&quot;              // write restricted service (write)
            L&quot;(A;;0x1;;;S-1-5-32-573)&quot;;         // event log readers        (read)</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="6aab1-150">Разрешения по умолчанию для <strong>пользовательской</strong> изоляции совпадают с разрешениями приложения.</span><span class="sxs-lookup"><span data-stu-id="6aab1-150">The default permissions for <strong>Custom</strong> isolation is the same as Application.</span></span></p>
<p><span data-ttu-id="6aab1-151">Каналы, указывающие изоляцию <strong>приложений</strong> , используют один и тот же сеанс ETW.</span><span class="sxs-lookup"><span data-stu-id="6aab1-151">Channels that specify <strong>Application</strong> isolation use the same ETW session.</span></span> <span data-ttu-id="6aab1-152">Это справедливо и для изоляции <strong>системы</strong> .</span><span class="sxs-lookup"><span data-stu-id="6aab1-152">The same is true for <strong>System</strong> isolation.</span></span> <span data-ttu-id="6aab1-153">Однако при указании <strong>пользовательской</strong> изоляции служба создает отдельный сеанс ETW для канала.</span><span class="sxs-lookup"><span data-stu-id="6aab1-153">However, if you specify <strong>Custom</strong> isolation, the service creates a separate ETW session for the channel.</span></span> <span data-ttu-id="6aab1-154">Использование <strong>пользовательской</strong> изоляции позволяет управлять разрешениями на доступ к каналу и резервному файлу.</span><span class="sxs-lookup"><span data-stu-id="6aab1-154">Using <strong>Custom</strong> isolation lets you control the access permissions for the channel and backing file.</span></span> <span data-ttu-id="6aab1-155">Так как доступно только 64 сеансов ETW, следует ограничить использование <strong>пользовательской</strong> изоляции.</span><span class="sxs-lookup"><span data-stu-id="6aab1-155">Because there are only 64 ETW sessions available, you should limit your use of <strong>Custom</strong> isolation.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6aab1-156">message</span><span class="sxs-lookup"><span data-stu-id="6aab1-156">message</span></span></td>
<td><span data-ttu-id="6aab1-157">строка</span><span class="sxs-lookup"><span data-stu-id="6aab1-157">string</span></span></td>
<td><p><span data-ttu-id="6aab1-158">Локализованное отображаемое имя для канала.</span><span class="sxs-lookup"><span data-stu-id="6aab1-158">The localized display name for the channel.</span></span> <span data-ttu-id="6aab1-159">Строка сообщения ссылается на локализованную строку в разделе " <a href="eventmanifestschema-stringtable-resources-element.md"><strong>STRINGTABLE</strong></a> " манифеста.</span><span class="sxs-lookup"><span data-stu-id="6aab1-159">The message string references a localized string in the <a href="eventmanifestschema-stringtable-resources-element.md"><strong>stringTable</strong></a> section of the manifest.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6aab1-160">name</span><span class="sxs-lookup"><span data-stu-id="6aab1-160">name</span></span></td>
<td><span data-ttu-id="6aab1-161">anyURI</span><span class="sxs-lookup"><span data-stu-id="6aab1-161">anyURI</span></span></td>
<td><p><span data-ttu-id="6aab1-162">Имя канала.</span><span class="sxs-lookup"><span data-stu-id="6aab1-162">The name of the channel.</span></span> <span data-ttu-id="6aab1-163">Имя должно быть уникальным в списке каналов, используемых поставщиком.</span><span class="sxs-lookup"><span data-stu-id="6aab1-163">The name must be unique within the list of channels that the provider uses.</span></span> <span data-ttu-id="6aab1-164">Соглашение об именовании каналов заключается в добавлении типа канала к имени поставщика.</span><span class="sxs-lookup"><span data-stu-id="6aab1-164">The convention for naming channels is to append the channel type to the provider's name.</span></span> <span data-ttu-id="6aab1-165">Например, если выбран диапазон 10.0.0.0/20 для виртуальной сети, для пространства клиентских адресов можно выбрать 10.1.0.0/24.</span><span class="sxs-lookup"><span data-stu-id="6aab1-165">For example.</span></span> <span data-ttu-id="6aab1-166">Если имя поставщика — компонент "компания-продукт", и вы определяете операционный канал, это имя будет иметь вид "компания-продукт-компонент" или "операционная".</span><span class="sxs-lookup"><span data-stu-id="6aab1-166">if the provider's name is Company-Product-Component and you are defining an operational channel, the name would be Company-Product-Component/Operational.</span></span></p>
<p><span data-ttu-id="6aab1-167">Имена каналов должны быть меньше 255 символов и не могут содержать следующие символы: ">", "</span><span class="sxs-lookup"><span data-stu-id="6aab1-167">Channel names must be less that 255 characters and cannot contain the following characters: '>', '</span></span><', '&', '&quot;', '|', '\', ':', '`', '?', '*', or characters with codes less than 31.</p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6aab1-168">символ</span><span class="sxs-lookup"><span data-stu-id="6aab1-168">symbol</span></span></td>
<td><span data-ttu-id="6aab1-169"><a href="eventmanifestschema-csymboltype-simpletype.md"><strong>ксимболтипе</strong></a></span><span class="sxs-lookup"><span data-stu-id="6aab1-169"><a href="eventmanifestschema-csymboltype-simpletype.md"><strong>CSymbolType</strong></a></span></span></td>
<td><p><span data-ttu-id="6aab1-170">Символ, используемый для ссылки на канал в приложении.</span><span class="sxs-lookup"><span data-stu-id="6aab1-170">The symbol to use to reference the channel in your application.</span></span> <span data-ttu-id="6aab1-171"><a href="message-compiler--mc-exe-.md"><strong>Компилятор сообщений (MC.exe)</strong></a> использует символ, чтобы создать константу для канала в файле заголовка, создаваемом компилятором.</span><span class="sxs-lookup"><span data-stu-id="6aab1-171">The <a href="message-compiler--mc-exe-.md"><strong>Message Compiler (MC.exe)</strong></a> uses the symbol to create a constant for the channel in the header file that the compiler generates.</span></span> <span data-ttu-id="6aab1-172">Если символ не указан, компилятор создаст это имя.</span><span class="sxs-lookup"><span data-stu-id="6aab1-172">If you do not specify a symbol, the compiler generates the name for you.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6aab1-173">type</span><span class="sxs-lookup"><span data-stu-id="6aab1-173">type</span></span></td>
<td><span data-ttu-id="6aab1-174">строка</span><span class="sxs-lookup"><span data-stu-id="6aab1-174">string</span></span></td>
<td><p><span data-ttu-id="6aab1-175">Идентифицирует тип канала.</span><span class="sxs-lookup"><span data-stu-id="6aab1-175">Identifies the channel's type.</span></span> <span data-ttu-id="6aab1-176">Можно указать один из следующих типов:</span><span class="sxs-lookup"><span data-stu-id="6aab1-176">You can specify one of the following types:</span></span></p>
<ul>
<li><span data-ttu-id="6aab1-177"><strong>Администратор</strong></span><span class="sxs-lookup"><span data-stu-id="6aab1-177"><strong>Admin</strong></span></span></li>
<li><span data-ttu-id="6aab1-178"><strong>Операционный</strong></span><span class="sxs-lookup"><span data-stu-id="6aab1-178"><strong>Operational</strong></span></span></li>
<li><span data-ttu-id="6aab1-179"><strong>Аналитический</strong></span><span class="sxs-lookup"><span data-stu-id="6aab1-179"><strong>Analytic</strong></span></span></li>
<li><span data-ttu-id="6aab1-180"><strong>Отладка</strong></span><span class="sxs-lookup"><span data-stu-id="6aab1-180"><strong>Debug</strong></span></span></li>
</ul>
<p><span data-ttu-id="6aab1-181">Каналы типа администратора поддерживают события, предназначенные для конечных пользователей, администраторов и сотрудников службы поддержки.</span><span class="sxs-lookup"><span data-stu-id="6aab1-181">Admin type channels support events that target end users, administrators, and support personnel.</span></span> <span data-ttu-id="6aab1-182">События, записываемые в каналы администрирования, должны иметь четко определенное решение, которое может действовать администратор. Примером события администратора является событие, возникающее, когда приложению не удается подключиться к принтеру.</span><span class="sxs-lookup"><span data-stu-id="6aab1-182">Events written to the Admin channels should have a well-defined solution on which the administrator can act. An example of an admin event is an event that occurs when an application fails to connect to a printer.</span></span> <span data-ttu-id="6aab1-183">Эти события либо хорошо документированы, либо имеют связанное с ними сообщение, которое предоставляет читателям инструкции, которые должны быть выполнены для устранения проблемы.</span><span class="sxs-lookup"><span data-stu-id="6aab1-183">These events are either well-documented or have a message associated with them that gives the reader direct instructions of what must be done to rectify the problem.</span></span></p>
<p><span data-ttu-id="6aab1-184">Каналы рабочих типов поддерживают события, которые используются для анализа и диагностики проблемы или вхождения.</span><span class="sxs-lookup"><span data-stu-id="6aab1-184">Operational type channels support events that are used for analyzing and diagnosing a problem or occurrence.</span></span> <span data-ttu-id="6aab1-185">Они могут использоваться для запуска инструментальных средств или задач, исходя из проблемы или происхождения события.</span><span class="sxs-lookup"><span data-stu-id="6aab1-185">They can be used to trigger tools or tasks based on the problem or occurrence.</span></span> <span data-ttu-id="6aab1-186">Примером события операционного типа может служить событие, происходящее при добавлении или удалении принтера из системы.</span><span class="sxs-lookup"><span data-stu-id="6aab1-186">An example of an operational event is an event that occurs when a printer is added or removed from a system.</span></span></p>
<p><span data-ttu-id="6aab1-187">Каналы аналитических типов поддерживают события, опубликованные в большом объеме.</span><span class="sxs-lookup"><span data-stu-id="6aab1-187">Analytic type channels support events that are published in high volume.</span></span> <span data-ttu-id="6aab1-188">Они описывают функционирование программы и указывают проблемы, которые не могут быть устранены вмешательством пользователя.</span><span class="sxs-lookup"><span data-stu-id="6aab1-188">They describe program operation and indicate problems that cannot be handled by user intervention.</span></span></p>
<p><span data-ttu-id="6aab1-189">Каналы типов отладки поддерживают события, которые используются исключительно разработчиками для диагностики проблемы при отладке.</span><span class="sxs-lookup"><span data-stu-id="6aab1-189">Debug type channels support events that are used solely by developers to diagnose a problem for debugging.</span></span></p>
<p><span data-ttu-id="6aab1-190">Аналитические и отладочные каналы по умолчанию отключены, и их следует включать только для определения причины проблемы.</span><span class="sxs-lookup"><span data-stu-id="6aab1-190">Analytic and debug channels are disabled by default and should only enabled to determine the cause of an issue.</span></span> <span data-ttu-id="6aab1-191">Например, можно включить канал, запустить сценарий, который вызывает проблему, отключить канал, а затем запросить события.</span><span class="sxs-lookup"><span data-stu-id="6aab1-191">For example, you would enable the channel, run the scenario that is causing the issue, disable the channel, and then query the events.</span></span> <span data-ttu-id="6aab1-192">Обратите внимание, что включение канала очищает канал существующих событий.</span><span class="sxs-lookup"><span data-stu-id="6aab1-192">Note that enabling the channel clears the channel of existing events.</span></span> <span data-ttu-id="6aab1-193">Если в канале аналитики и отладки используется циклический резервный файл, необходимо отключить канал для запроса его событий.</span><span class="sxs-lookup"><span data-stu-id="6aab1-193">If the analytic and debug channel uses a circular backing file, you must disable the channel to query its events.</span></span></p>
<p><span data-ttu-id="6aab1-194">Все каналы администрирования используют один и тот же сеанс ETW. Это справедливо и для рабочих каналов.</span><span class="sxs-lookup"><span data-stu-id="6aab1-194">All Admin channels use the same ETW session; the same is true for Operational channels.</span></span> <span data-ttu-id="6aab1-195">Однако каждый аналитический и отладочный канал использует отдельный сеанс ETW, что является еще одной причиной включения этих типов каналов только при необходимости (доступно ограниченное количество сеансов ETW).</span><span class="sxs-lookup"><span data-stu-id="6aab1-195">However, each Analytic and Debug channel uses a separate ETW session, which is another reason to only enable these channel types when needed (there is a limited number of ETW sessions available).</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6aab1-196">значение</span><span class="sxs-lookup"><span data-stu-id="6aab1-196">value</span></span></td>
<td><span data-ttu-id="6aab1-197"><a href="eventmanifestschema-hexint8type-simpletype.md"><strong>UInt8Type</strong></a></span><span class="sxs-lookup"><span data-stu-id="6aab1-197"><a href="eventmanifestschema-hexint8type-simpletype.md"><strong>UInt8Type</strong></a></span></span></td>
<td><p><span data-ttu-id="6aab1-198">Числовой идентификатор, который однозначно определяет канал в списке каналов, определяемых поставщиком.</span><span class="sxs-lookup"><span data-stu-id="6aab1-198">A numeric identifier that uniquely identifies the channel within the list of channels that the provider defines.</span></span> <span data-ttu-id="6aab1-199">Компилятор сообщений присваивает значение, если оно не указано.</span><span class="sxs-lookup"><span data-stu-id="6aab1-199">The message compiler assigns the value if not specified.</span></span></p></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="6aab1-200">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6aab1-200">Remarks</span></span>

<span data-ttu-id="6aab1-201">Если имя канала соответствует соглашению об именовании каналов, Просмотр событий Windows будет перечислять канал, используя строку, следующую за обратной косой чертой.</span><span class="sxs-lookup"><span data-stu-id="6aab1-201">If the channel's name follows the channel naming convention, the Windows Event Viewer will list the channel using the string that follows the backslash.</span></span> <span data-ttu-id="6aab1-202">Например, если имя канала — "компания-продукт — компонент/Рабочая", то Просмотр событий будет перечислять канал как работоспособный в рамках поставщика компонентов компании и продукта.</span><span class="sxs-lookup"><span data-stu-id="6aab1-202">For example, if the channel name is Company-Product-Component/Operational, then the Event Viewer will list the channel as Operational under the Company-Product-Component provider.</span></span> <span data-ttu-id="6aab1-203">В противном случае в поставщике отображается имя всего канала.</span><span class="sxs-lookup"><span data-stu-id="6aab1-203">Otherwise, the entire channel name is shown under the provider.</span></span> <span data-ttu-id="6aab1-204">Локализованное отображаемое имя используется, если оно указано.</span><span class="sxs-lookup"><span data-stu-id="6aab1-204">The localized display name is used if provided.</span></span>

## <a name="requirements"></a><span data-ttu-id="6aab1-205">Требования</span><span class="sxs-lookup"><span data-stu-id="6aab1-205">Requirements</span></span>



| <span data-ttu-id="6aab1-206">Требование</span><span class="sxs-lookup"><span data-stu-id="6aab1-206">Requirement</span></span> | <span data-ttu-id="6aab1-207">Значение</span><span class="sxs-lookup"><span data-stu-id="6aab1-207">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6aab1-208">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6aab1-208">Minimum supported client</span></span><br/> | <span data-ttu-id="6aab1-209">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6aab1-209">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6aab1-210">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6aab1-210">Minimum supported server</span></span><br/> | <span data-ttu-id="6aab1-211">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6aab1-211">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




`

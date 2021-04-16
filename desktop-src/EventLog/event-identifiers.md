---
description: Идентификаторы событий однозначно идентифицируют определенное событие.
ms.assetid: 83a84db4-572b-48bd-bc0f-071b2089a5ca
title: Идентификаторы событий (ведение журнала событий)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 402337cb2c7e862785a88ec604c6382152736fd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543055"
---
# <a name="event-identifiers-event-logging"></a><span data-ttu-id="c73ca-103">Идентификаторы событий (ведение журнала событий)</span><span class="sxs-lookup"><span data-stu-id="c73ca-103">Event Identifiers (Event Logging)</span></span>

<span data-ttu-id="c73ca-104">Идентификаторы событий однозначно идентифицируют определенное событие.</span><span class="sxs-lookup"><span data-stu-id="c73ca-104">Event identifiers uniquely identify a particular event.</span></span> <span data-ttu-id="c73ca-105">Каждый [источник событий](event-sources.md) может определять свои собственные пронумерованные события и строки описания, с которыми они сопоставляются в файле сообщений.</span><span class="sxs-lookup"><span data-stu-id="c73ca-105">Each [event source](event-sources.md) can define its own numbered events and the description strings to which they are mapped in its message file.</span></span> <span data-ttu-id="c73ca-106">Средства просмотра событий могут предоставлять пользователю эти строки.</span><span class="sxs-lookup"><span data-stu-id="c73ca-106">Event viewers can present these strings to the user.</span></span> <span data-ttu-id="c73ca-107">Они должны помочь пользователю понять, что пошло не так, и предложить, какие действия следует предпринять.</span><span class="sxs-lookup"><span data-stu-id="c73ca-107">They should help the user understand what went wrong and suggest what actions to take.</span></span> <span data-ttu-id="c73ca-108">Направьте описание у пользователей, которое решает свои проблемы, а не для администраторов или специалистов службы поддержки.</span><span class="sxs-lookup"><span data-stu-id="c73ca-108">Direct the description at users solving their own problems, not at administrators or support technicians.</span></span> <span data-ttu-id="c73ca-109">Дополнительные сведения см. в разделе [рекомендации по сообщениям об ошибках](/windows/desktop/Debug/error-message-guidelines).</span><span class="sxs-lookup"><span data-stu-id="c73ca-109">For more information, see [Error Message Guidelines](/windows/desktop/Debug/error-message-guidelines).</span></span>

## <a name="format"></a><span data-ttu-id="c73ca-110">Формат</span><span class="sxs-lookup"><span data-stu-id="c73ca-110">Format</span></span>

<span data-ttu-id="c73ca-111">На следующей схеме показан формат идентификатора события.</span><span class="sxs-lookup"><span data-stu-id="c73ca-111">The following diagram illustrates the format of an event identifier.</span></span>

``` syntax
  3 3 2 2 2 2 2 2 2 2 2 2 1 1 1 1 1 1 1 1 1 1
  1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0
 +---+-+-+-----------------------+-------------------------------+
 |Sev|C|R|     Facility          |               Code            |
 +---+-+-+-----------------------+-------------------------------+
```

<dl> <dt>

<span data-ttu-id="c73ca-112"><span id="Sev"></span><span id="sev"></span><span id="SEV"></span>Уровень серьезности</span><span class="sxs-lookup"><span data-stu-id="c73ca-112"><span id="Sev"></span><span id="sev"></span><span id="SEV"></span>Sev</span></span>
</dt> <dd>

<span data-ttu-id="c73ca-113">серьезность.</span><span class="sxs-lookup"><span data-stu-id="c73ca-113">Severity.</span></span> <span data-ttu-id="c73ca-114">Уровень серьезности определяется следующим образом.</span><span class="sxs-lookup"><span data-stu-id="c73ca-114">The severity is defined as follows:</span></span>

<dl> <dd><span data-ttu-id="c73ca-115">00 — успешное завершение</span><span class="sxs-lookup"><span data-stu-id="c73ca-115">00 - Success</span></span></dd> <dd><span data-ttu-id="c73ca-116">01-информационная</span><span class="sxs-lookup"><span data-stu-id="c73ca-116">01 - Informational</span></span></dd> <dd><span data-ttu-id="c73ca-117">10 — предупреждение</span><span class="sxs-lookup"><span data-stu-id="c73ca-117">10 - Warning</span></span></dd> <dd><span data-ttu-id="c73ca-118">11 — ошибка</span><span class="sxs-lookup"><span data-stu-id="c73ca-118">11 - Error</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="c73ca-119"><span id="C"></span><span id="c"></span>Ц</span><span class="sxs-lookup"><span data-stu-id="c73ca-119"><span id="C"></span><span id="c"></span>C</span></span>
</dt> <dd>

<span data-ttu-id="c73ca-120">Бит клиента.</span><span class="sxs-lookup"><span data-stu-id="c73ca-120">Customer bit.</span></span> <span data-ttu-id="c73ca-121">Этот бит определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c73ca-121">This bit is defined as follows:</span></span>

<dl> <dd><span data-ttu-id="c73ca-122">0 — системный код</span><span class="sxs-lookup"><span data-stu-id="c73ca-122">0 - System code</span></span></dd> <dd><span data-ttu-id="c73ca-123">1. код клиента</span><span class="sxs-lookup"><span data-stu-id="c73ca-123">1 - Customer code</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="c73ca-124"><span id="R"></span><span id="r"></span>Cерверный</span><span class="sxs-lookup"><span data-stu-id="c73ca-124"><span id="R"></span><span id="r"></span>R</span></span>
</dt> <dd>

<span data-ttu-id="c73ca-125">Зарезервированный бит.</span><span class="sxs-lookup"><span data-stu-id="c73ca-125">Reserved bit.</span></span>

</dd> <dt>

<span data-ttu-id="c73ca-126"><span id="Facility"></span><span id="facility"></span><span id="FACILITY"></span>Объектом</span><span class="sxs-lookup"><span data-stu-id="c73ca-126"><span id="Facility"></span><span id="facility"></span><span id="FACILITY"></span>Facility</span></span>
</dt> <dd>

<span data-ttu-id="c73ca-127">Код устройства.</span><span class="sxs-lookup"><span data-stu-id="c73ca-127">Facility code.</span></span> <span data-ttu-id="c73ca-128">Это значение может быть \_ равно null.</span><span class="sxs-lookup"><span data-stu-id="c73ca-128">This value can be FACILITY\_NULL.</span></span>

</dd> <dt>

<span data-ttu-id="c73ca-129"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Приведен</span><span class="sxs-lookup"><span data-stu-id="c73ca-129"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
</dt> <dd>

<span data-ttu-id="c73ca-130">Код состояния для средства.</span><span class="sxs-lookup"><span data-stu-id="c73ca-130">Status code for the facility.</span></span>

</dd> </dl>

## <a name="message-definitions"></a><span data-ttu-id="c73ca-131">Определения сообщений</span><span class="sxs-lookup"><span data-stu-id="c73ca-131">Message Definitions</span></span>

<span data-ttu-id="c73ca-132">Сообщения определяются в файле сообщений о событиях.</span><span class="sxs-lookup"><span data-stu-id="c73ca-132">Messages are defined in the event message file.</span></span> <span data-ttu-id="c73ca-133">Строки описания в файле сообщений о событиях индексируются по идентификатору события, что позволяет Просмотр событий отображать текст, относящийся к конкретному событию, для любого события, основанного на идентификаторе события.</span><span class="sxs-lookup"><span data-stu-id="c73ca-133">The description strings in the event message file are indexed by event identifier, enabling Event Viewer to display event-specific text for any event based on the event identifier.</span></span> <span data-ttu-id="c73ca-134">Все описания локализованы и зависят от языка.</span><span class="sxs-lookup"><span data-stu-id="c73ca-134">All descriptions are localized and language dependent.</span></span> <span data-ttu-id="c73ca-135">Дополнительные сведения о создании файла сообщений см. в разделе [текстовые файлы сообщений](message-text-files.md).</span><span class="sxs-lookup"><span data-stu-id="c73ca-135">For more information on building a message file, see [Message Text Files](message-text-files.md).</span></span>

<span data-ttu-id="c73ca-136">Строки описания могут содержать заполнители строки вставки в форме%*n*, где %1 обозначает первую строку вставки и т. д.</span><span class="sxs-lookup"><span data-stu-id="c73ca-136">The description strings may contain insertion string placeholders, of the form %*n*, where %1 indicates the first insertion string, and so on.</span></span> <span data-ttu-id="c73ca-137">Например, ниже приведен пример записи в MC-файле:</span><span class="sxs-lookup"><span data-stu-id="c73ca-137">For example, the following is a sample entry in the .mc file:</span></span>

``` syntax
MessageId=0x4
Severity=Error
Facility=System
SymbolicName=MSG_CMD_DELETE
Language=English
File %1 contains %2, which is in error.
.
```

<span data-ttu-id="c73ca-138">В этом случае буфер, возвращенный [**реадевентлог**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) , содержит строки вставки.</span><span class="sxs-lookup"><span data-stu-id="c73ca-138">In this case, the buffer returned by [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) contains insertion strings.</span></span> <span data-ttu-id="c73ca-139">Элемент **нумстрингс** структуры [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) указывает количество вставляемых строк.</span><span class="sxs-lookup"><span data-stu-id="c73ca-139">The **NumStrings** member of the [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) structure indicates the number of insertion strings.</span></span> <span data-ttu-id="c73ca-140">Элемент **стрингоффсет** структуры **EVENTLOGRECORD** указывает расположение первой вставляемой строки в буфере.</span><span class="sxs-lookup"><span data-stu-id="c73ca-140">The **StringOffset** member of the **EVENTLOGRECORD** structure indicates the location of the first insertion string in the buffer.</span></span> <span data-ttu-id="c73ca-141">Можно передать массив DWORD \_ ПТРС, указывающий на адрес каждой строки в буфере при вызове функции [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) , и вставит строки в сообщение.</span><span class="sxs-lookup"><span data-stu-id="c73ca-141">You can pass an array of DWORD\_PTRs that point to the address each string in the buffer when calling the [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) function and it will insert the strings into the message.</span></span>

<span data-ttu-id="c73ca-142">Строка описания может также содержать заполнители для строк параметров из файла сообщений параметров.</span><span class="sxs-lookup"><span data-stu-id="c73ca-142">The description string can also contain placeholders for parameter strings from the parameter message file.</span></span> <span data-ttu-id="c73ca-143">Заполнители имеют форму%%*n*, где% %1 заменяется строкой параметра с идентификатором 1 и т. д.</span><span class="sxs-lookup"><span data-stu-id="c73ca-143">The placeholders are of the form %%*n*, where %%1 is replaced by the parameter string with the identifier of 1, and so on.</span></span> <span data-ttu-id="c73ca-144">Однако можно вставить строки параметров в строку сообщения, возвращаемую [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) .</span><span class="sxs-lookup"><span data-stu-id="c73ca-144">However, it is up to you to insert the parameter strings into the message string that [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) returns.</span></span> <span data-ttu-id="c73ca-145">Как правило, метод **FormatMessage** вызывается для получения строки сообщения для события.</span><span class="sxs-lookup"><span data-stu-id="c73ca-145">Typically, you call **FormatMessage** to get the message string for the event.</span></span> <span data-ttu-id="c73ca-146">Затем выполняется синтаксический анализ строки сообщения для параметров%%*n* .</span><span class="sxs-lookup"><span data-stu-id="c73ca-146">You then parse the message string for %%*n* parameters.</span></span> <span data-ttu-id="c73ca-147">Если сообщение содержит один или несколько параметров, загрузите значение реестра **параметермессажефиле** для источника.</span><span class="sxs-lookup"><span data-stu-id="c73ca-147">If the message contains one or more parameters, load the **ParameterMessageFile** registry value for the source.</span></span> <span data-ttu-id="c73ca-148">Для каждого параметра в строке сообщения получите идентификатор и передайте его в **FormatMessage** , чтобы получить строку параметра.</span><span class="sxs-lookup"><span data-stu-id="c73ca-148">For each parameter in the message string, get the identifier and pass it to **FormatMessage** to get the parameter string.</span></span> <span data-ttu-id="c73ca-149">Замените параметр в строке сообщения строкой параметра, возвращаемой **FormatMessage** .</span><span class="sxs-lookup"><span data-stu-id="c73ca-149">Replace the parameter in the message string with the parameter string that **FormatMessage** returned.</span></span>

## <a name="insertion-strings"></a><span data-ttu-id="c73ca-150">Строки вставки</span><span class="sxs-lookup"><span data-stu-id="c73ca-150">Insertion Strings</span></span>

<span data-ttu-id="c73ca-151">Строки вставки — это необязательные независящие от языка строки, используемые для заполнения значений заполнителей в строках описания.</span><span class="sxs-lookup"><span data-stu-id="c73ca-151">Insertion strings are optional language-independent strings used to fill in values for placeholders in description strings.</span></span> <span data-ttu-id="c73ca-152">Поскольку строки не локализованы, крайне важно, чтобы эти заполнители использовались только для представления независимых от языка строк, таких как числовые значения, имена файлов, имена пользователей и т. д.</span><span class="sxs-lookup"><span data-stu-id="c73ca-152">Because the strings are not localized, it is critical that these placeholders be used only to represent language-independent strings such as numeric values, file names, user names, and so on.</span></span> <span data-ttu-id="c73ca-153">Длина строки не должна превышать 32 КБ-1 символов.</span><span class="sxs-lookup"><span data-stu-id="c73ca-153">The string length must not exceed 32 kilobytes - 1 characters.</span></span>

<span data-ttu-id="c73ca-154">Избегайте использования нескольких строк для создания более крупного описания.</span><span class="sxs-lookup"><span data-stu-id="c73ca-154">Avoid using several strings to create a larger description.</span></span> <span data-ttu-id="c73ca-155">Строка вставки должна обрабатываться как данные, а не как текст.</span><span class="sxs-lookup"><span data-stu-id="c73ca-155">An insertion string should be treated as data, not text.</span></span> <span data-ttu-id="c73ca-156">Например, в следующем примере pszString1 и pszString2 не должны использоваться в качестве вставляемых строк для Псздескриптион.</span><span class="sxs-lookup"><span data-stu-id="c73ca-156">For example, in the following example, pszString1 and pszString2 should not be used as insertion strings for pszDescription.</span></span>

``` syntax
LPSTR pszString1 = "successfully"; 
LPSTR pszString2 = "not"; 
LPSTR pszDescription = "The user was %1 added to the database.";
```

<span data-ttu-id="c73ca-157">В следующем примере можно использовать pszString1 или pszString2 для строки вставки в Псздескриптион.</span><span class="sxs-lookup"><span data-stu-id="c73ca-157">In the following example, it is appropriate to use either pszString1 or pszString2 for the insertion string in pszDescription.</span></span>

``` syntax
LPSTR pszString1 = "c:\\testapp1.c"; 
LPSTR pszString2 = "c:\\testapp2.c"; 
LPSTR pszDescription = "Access denied. Attempted to open the file %1."
```

 

 

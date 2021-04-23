---
description: Каждый журнал в разделе EventLog содержит подразделы, которые называются источниками событий. Источник события — это имя программного обеспечения, записывающего событие в журнал.
ms.assetid: bc7fdc74-be41-4d17-997c-27171ef73f0f
title: Источники событий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab2b408b76cdbc6e93e44099fea2842f9655a963
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662877"
---
# <a name="event-sources"></a><span data-ttu-id="b4351-104">Источники событий</span><span class="sxs-lookup"><span data-stu-id="b4351-104">Event Sources</span></span>

<span data-ttu-id="b4351-105">Каждый журнал в [разделе EventLog](eventlog-key.md) содержит подразделы, которые называются *источниками событий*.</span><span class="sxs-lookup"><span data-stu-id="b4351-105">Each log in the [Eventlog key](eventlog-key.md) contains subkeys called *event sources*.</span></span> <span data-ttu-id="b4351-106">Источник события — это имя программного обеспечения, записывающего событие в журнал.</span><span class="sxs-lookup"><span data-stu-id="b4351-106">The event source is the name of the software that logs the event.</span></span> <span data-ttu-id="b4351-107">Часто это имя приложения или имя подкомпонента приложения, если приложение велико.</span><span class="sxs-lookup"><span data-stu-id="b4351-107">It is often the name of the application or the name of a subcomponent of the application if the application is large.</span></span> <span data-ttu-id="b4351-108">В реестр можно добавить не более 16 384 источников событий.</span><span class="sxs-lookup"><span data-stu-id="b4351-108">You can add a maximum of 16,384 event sources to the registry.</span></span> <span data-ttu-id="b4351-109">Журнал **безопасности** предназначен только для системного использования.</span><span class="sxs-lookup"><span data-stu-id="b4351-109">The **Security** log is for system use only.</span></span> <span data-ttu-id="b4351-110">Драйверы устройств должны добавлять свои имена в **системный** журнал.</span><span class="sxs-lookup"><span data-stu-id="b4351-110">Device drivers should add their names to the **System** log.</span></span> <span data-ttu-id="b4351-111">Приложения и службы должны добавлять свои имена в журнал **приложений** или создавать пользовательские журналы.</span><span class="sxs-lookup"><span data-stu-id="b4351-111">Applications and services should add their names to the **Application** log or create a custom log.</span></span>

<span data-ttu-id="b4351-112">Структура источников событий выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="b4351-112">The structure of the event sources is as follows:</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            EventLog
               Application
                  AppName
               Security
               System
                  DriverName
               CustomLog
                  AppName
```

<span data-ttu-id="b4351-113">Нельзя использовать имя источника, которое уже использовалось как имя журнала.</span><span class="sxs-lookup"><span data-stu-id="b4351-113">You cannot use a source name that has already been used as a log name.</span></span> <span data-ttu-id="b4351-114">Кроме того, имена источников не могут быть иерархическими; то есть они не могут содержать символ обратной косой черты (" \\ ").</span><span class="sxs-lookup"><span data-stu-id="b4351-114">In addition, source names cannot be hierarchical; that is, they cannot contain the backslash character ("\\").</span></span>

<span data-ttu-id="b4351-115">Каждый источник событий содержит сведения (например, [файл сообщений](message-files.md)), относящиеся к программному обеспечению, которое будет регистрировать события, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="b4351-115">Each event source contains information (such as a [message file](message-files.md)) specific to the software that will be logging the events, as shown in the following table.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b4351-116">Значение реестра</span><span class="sxs-lookup"><span data-stu-id="b4351-116">Registry Value</span></span></th>
<th><span data-ttu-id="b4351-117">Описание</span><span class="sxs-lookup"><span data-stu-id="b4351-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b4351-118"><strong>категорикаунт</strong></span><span class="sxs-lookup"><span data-stu-id="b4351-118"><strong>CategoryCount</strong></span></span></td>
<td><span data-ttu-id="b4351-119">Число поддерживаемых категорий событий.</span><span class="sxs-lookup"><span data-stu-id="b4351-119">Number of event categories supported.</span></span> <span data-ttu-id="b4351-120">Это значение имеет тип <strong>REG_DWORD</strong>.</span><span class="sxs-lookup"><span data-stu-id="b4351-120">This value is of type <strong>REG_DWORD</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4351-121"><strong>категоримессажефиле</strong></span><span class="sxs-lookup"><span data-stu-id="b4351-121"><strong>CategoryMessageFile</strong></span></span></td>
<td><span data-ttu-id="b4351-122">Путь к файлу сообщения категории.</span><span class="sxs-lookup"><span data-stu-id="b4351-122">Path to the category message file.</span></span> <span data-ttu-id="b4351-123">Файл сообщения категории содержит строки, зависящие от языка, которые описывают категории.</span><span class="sxs-lookup"><span data-stu-id="b4351-123">A category message file contains language-dependent strings that describe the categories.</span></span> <span data-ttu-id="b4351-124">Это значение может иметь тип <strong>REG_SZ</strong> или <strong>REG_EXPAND_SZ</strong>.</span><span class="sxs-lookup"><span data-stu-id="b4351-124">This value can be of type <strong>REG_SZ</strong> or <strong>REG_EXPAND_SZ</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4351-125"><strong>евентмессажефиле</strong></span><span class="sxs-lookup"><span data-stu-id="b4351-125"><strong>EventMessageFile</strong></span></span></td>
<td><span data-ttu-id="b4351-126">Путь к одному или нескольким файлам сообщений о событиях; Используйте точку с запятой для разделения нескольких файлов.</span><span class="sxs-lookup"><span data-stu-id="b4351-126">Path to one or more event message files; use a semicolon to delimit multiple files.</span></span> <span data-ttu-id="b4351-127">Файл сообщений о событиях содержит зависящие от языка строки, описывающие события.</span><span class="sxs-lookup"><span data-stu-id="b4351-127">An event message file contains language-dependent strings that describe the events.</span></span> <span data-ttu-id="b4351-128">Это значение может иметь тип <strong>REG_SZ</strong> или <strong>REG_EXPAND_SZ</strong>.</span><span class="sxs-lookup"><span data-stu-id="b4351-128">This value can be of type <strong>REG_SZ</strong> or <strong>REG_EXPAND_SZ</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4351-129"><strong>параметермессажефиле</strong></span><span class="sxs-lookup"><span data-stu-id="b4351-129"><strong>ParameterMessageFile</strong></span></span></td>
<td><span data-ttu-id="b4351-130">Путь к файлу сообщения параметров.</span><span class="sxs-lookup"><span data-stu-id="b4351-130">Path to the parameter message file.</span></span> <span data-ttu-id="b4351-131">Файл сообщения с параметрами содержит не зависящие от языка строки, которые вставляются в строки описания события.</span><span class="sxs-lookup"><span data-stu-id="b4351-131">A parameter message file contains language-independent strings that are to be inserted into the event description strings.</span></span> <span data-ttu-id="b4351-132">Это значение может иметь тип <strong>REG_SZ</strong> или <strong>REG_EXPAND_SZ</strong>.</span><span class="sxs-lookup"><span data-stu-id="b4351-132">This value can be of type <strong>REG_SZ</strong> or <strong>REG_EXPAND_SZ</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4351-133"><strong>типессуппортед</strong></span><span class="sxs-lookup"><span data-stu-id="b4351-133"><strong>TypesSupported</strong></span></span></td>
<td><span data-ttu-id="b4351-134">Битовая маска поддерживаемых типов.</span><span class="sxs-lookup"><span data-stu-id="b4351-134">Bitmask of supported types.</span></span> <span data-ttu-id="b4351-135">Это значение имеет тип <strong>REG_DWORD</strong>.</span><span class="sxs-lookup"><span data-stu-id="b4351-135">This value is of type <strong>REG_DWORD</strong>.</span></span> <span data-ttu-id="b4351-136">Это может быть одно или несколько из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="b4351-136">It can be one or more of the following values:</span></span> <dl> <span data-ttu-id="b4351-137"><strong>EVENTLOG_AUDIT_FAILURE</strong> (0x0010)</span><span class="sxs-lookup"><span data-stu-id="b4351-137"><strong>EVENTLOG_AUDIT_FAILURE</strong> (0x0010)</span></span><br /><span data-ttu-id="b4351-138">
<strong>EVENTLOG_AUDIT_SUCCESS</strong> (0x0008)</span><span class="sxs-lookup"><span data-stu-id="b4351-138">
<strong>EVENTLOG_AUDIT_SUCCESS</strong> (0x0008)</span></span><br /><span data-ttu-id="b4351-139">
<strong>EVENTLOG_ERROR_TYPE</strong> (0x0001)</span><span class="sxs-lookup"><span data-stu-id="b4351-139">
<strong>EVENTLOG_ERROR_TYPE</strong> (0x0001)</span></span><br /><span data-ttu-id="b4351-140">
<strong>EVENTLOG_INFORMATION_TYPE</strong> (0x0004)</span><span class="sxs-lookup"><span data-stu-id="b4351-140">
<strong>EVENTLOG_INFORMATION_TYPE</strong> (0x0004)</span></span><br /><span data-ttu-id="b4351-141">
<strong>EVENTLOG_WARNING_TYPE</strong> (0x0002)</span><span class="sxs-lookup"><span data-stu-id="b4351-141">
<strong>EVENTLOG_WARNING_TYPE</strong> (0x0002)</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="b4351-142">Когда приложение использует функцию [**регистеревентсаурце**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) или [**опеневентлог**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) для получения маркера журнала событий, служба ведения журнала событий выполняет поиск указанного источника событий в реестре.</span><span class="sxs-lookup"><span data-stu-id="b4351-142">When an application uses the [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) or [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) function to get a handle to an event log, the event logging service searches for the specified event source in the registry.</span></span> <span data-ttu-id="b4351-143">Например, журнал **приложений** может содержать источники событий для Microsoft SQL Server и Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="b4351-143">For example, the **Application** log might contain event sources for Microsoft SQL Server and Microsoft Excel.</span></span> <span data-ttu-id="b4351-144">Если приложение использует [**регистеревентсаурце**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) или **опеневентлог** с исходным именем приложения, SQL или Excel, служба ведения журнала событий возвращает маркер журнала **приложений** .</span><span class="sxs-lookup"><span data-stu-id="b4351-144">If an application uses [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) or **OpenEventLog** with a source name of Application, SQL, or Excel, the event logging service returns a handle to the **Application** log.</span></span>

<span data-ttu-id="b4351-145">Приложение может использовать журнал **приложений** без добавления нового источника событий в реестр.</span><span class="sxs-lookup"><span data-stu-id="b4351-145">An application can use the **Application** log without adding a new event source to the registry.</span></span> <span data-ttu-id="b4351-146">Если приложение вызывает [**регистеревентсаурце**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) и передает имя источника, которое не удается найти в реестре, служба ведения журнала событий по умолчанию использует журнал **приложений** .</span><span class="sxs-lookup"><span data-stu-id="b4351-146">If the application calls [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) and passes a source name that cannot be found in the registry, the event-logging service uses the **Application** log by default.</span></span> <span data-ttu-id="b4351-147">Однако из-за отсутствия файлов сообщений Просмотр событий не может сопоставлять идентификаторы событий или категории событий с строкой описания и выводит сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="b4351-147">However, because there are no message files, the Event Viewer cannot map any event identifiers or event categories to a description string, and will display an error.</span></span> <span data-ttu-id="b4351-148">По этой причине необходимо добавить уникальный источник событий в реестр для приложения и указать файл сообщения.</span><span class="sxs-lookup"><span data-stu-id="b4351-148">For this reason, you should add a unique event source to the registry for your application and specify a message file.</span></span>

 

 




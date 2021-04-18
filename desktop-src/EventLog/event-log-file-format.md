---
description: Каждый журнал событий содержит заголовок (представленный \_ \_ структурой заголовка файла журнала ELF) с фиксированным размером, за которым следуют переменное число записей событий (представленное структурами EVENTLOGRECORD) и запись конца файла (представленная \_ \_ структурой записи EOF ELF).
ms.assetid: 2b62b807-4ffd-4a8f-afe4-34e109d01856
title: Формат файла журнала событий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af4ba5c8bc0114e319107272e706801544e3effa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545026"
---
# <a name="event-log-file-format"></a><span data-ttu-id="744ec-103">Формат файла журнала событий</span><span class="sxs-lookup"><span data-stu-id="744ec-103">Event Log File Format</span></span>

<span data-ttu-id="744ec-104">Каждый журнал событий содержит заголовок (представленный структурой [**\_ \_ заголовка файла журнала ELF**](/previous-versions/windows/desktop/legacy/bb309024(v=vs.85)) ) с фиксированным размером, за которым следуют переменное число записей событий (представленное структурами [**EVENTLOGRECORD**](/windows/desktop/api/winnt/ns-winnt-eventlogrecord) ) и запись конца файла (представленная структурой [**\_ \_ записи EOF ELF**](/previous-versions/windows/desktop/legacy/bb309022(v=vs.85)) ).</span><span class="sxs-lookup"><span data-stu-id="744ec-104">Each event log contains a header (represented by the [**ELF\_LOGFILE\_HEADER**](/previous-versions/windows/desktop/legacy/bb309024(v=vs.85)) structure) that has a fixed size, followed by a variable number of event records (represented by [**EVENTLOGRECORD**](/windows/desktop/api/winnt/ns-winnt-eventlogrecord) structures), and an end-of-file record (represented by the [**ELF\_EOF\_RECORD**](/previous-versions/windows/desktop/legacy/bb309022(v=vs.85)) structure).</span></span>

<span data-ttu-id="744ec-105">Структура **\_ \_ заголовка файла журнала ELF** и структура **\_ \_ записи ELF EOF** записываются в журнал событий при создании журнала событий и обновляются каждый раз при записи события в журнал.</span><span class="sxs-lookup"><span data-stu-id="744ec-105">The **ELF\_LOGFILE\_HEADER** structure and the **ELF\_EOF\_RECORD** structure are written in the event log when the event log is created and are updated each time an event is written to the log.</span></span>

<span data-ttu-id="744ec-106">Когда приложение вызывает функцию [**репортевент**](/windows/desktop/api/Winbase/nf-winbase-reporteventa) для записи записи в журнал событий, система передает параметры в службу ведения журнала событий.</span><span class="sxs-lookup"><span data-stu-id="744ec-106">When an application calls the [**ReportEvent**](/windows/desktop/api/Winbase/nf-winbase-reporteventa) function to write an entry to the event log, the system passes the parameters to the event-logging service.</span></span> <span data-ttu-id="744ec-107">Служба ведения журнала событий использует эти сведения для записи структуры **EVENTLOGRECORD** в журнал событий.</span><span class="sxs-lookup"><span data-stu-id="744ec-107">The event-logging service uses the information to write an **EVENTLOGRECORD** structure to the event log.</span></span> <span data-ttu-id="744ec-108">Этот процесс представлен на схеме ниже.</span><span class="sxs-lookup"><span data-stu-id="744ec-108">The following diagram illustrates this process.</span></span>

![запись файла журнала](images/evreport.png)

<span data-ttu-id="744ec-110">Записи событий упорядочены одним из следующих способов.</span><span class="sxs-lookup"><span data-stu-id="744ec-110">The event records are organized in one of the following ways:</span></span>

-   <span data-ttu-id="744ec-111">Без упаковки.</span><span class="sxs-lookup"><span data-stu-id="744ec-111">Non-wrapping.</span></span> <span data-ttu-id="744ec-112">Самая старая запись сразу после заголовка журнала событий и добавления новых записей после последней добавленной записи (до **\_ \_ записи ELF EOF**).</span><span class="sxs-lookup"><span data-stu-id="744ec-112">The oldest record is immediately after the event log header and new records are added after the last record that was added (before the **ELF\_EOF\_RECORD**).</span></span> <span data-ttu-id="744ec-113">В следующем примере показан метод без упаковки:</span><span class="sxs-lookup"><span data-stu-id="744ec-113">The following example shows the non-wrapping method:</span></span>

    ``` syntax
    HEADER                   (ELF_LOGFILE_HEADER)
    EVENT RECORD 1           (EVENTLOGRECORD)
    EVENT RECORD 2           (EVENTLOGRECORD)
    EOF RECORD               (ELF_EOF_RECORD)
    ```

    <span data-ttu-id="744ec-114">Необолочка может произойти при создании журнала событий или при очистке журнала событий.</span><span class="sxs-lookup"><span data-stu-id="744ec-114">Non-wrapping can occur when the event log is created or when the event log is cleared.</span></span> <span data-ttu-id="744ec-115">Журнал событий остается без оболочки, пока не будет достигнут предел размера журнала событий.</span><span class="sxs-lookup"><span data-stu-id="744ec-115">The event log continues to be non-wrapping until the event log size limit is reached.</span></span> <span data-ttu-id="744ec-116">Размер журнала событий ограничен значением конфигурации **MAXSIZE** или объемом системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="744ec-116">The event log size is limited by either the **MaxSize** configuration value or the amount of system resources.</span></span>

    <span data-ttu-id="744ec-117">При достижении предельного размера журнала событий он может начать перенос.</span><span class="sxs-lookup"><span data-stu-id="744ec-117">When the event log size limit is reached, it might start wrapping.</span></span> <span data-ttu-id="744ec-118">Оболочка управляется значением конфигурации **хранения** .</span><span class="sxs-lookup"><span data-stu-id="744ec-118">Wrapping is controlled by the **Retention** configuration value.</span></span> <span data-ttu-id="744ec-119">Дополнительные сведения о значениях конфигурации журнала событий см. в разделе [EventLog](eventlog-key.md).</span><span class="sxs-lookup"><span data-stu-id="744ec-119">For more information about the event log configuration values, see [Eventlog Key](eventlog-key.md).</span></span>

-   <span data-ttu-id="744ec-120">Переход.</span><span class="sxs-lookup"><span data-stu-id="744ec-120">Wrapping.</span></span> <span data-ttu-id="744ec-121">Записи организованы в виде кольцевого буфера.</span><span class="sxs-lookup"><span data-stu-id="744ec-121">The records are organized as a circular buffer.</span></span> <span data-ttu-id="744ec-122">По мере добавления новых записей самые старые записи заменяются.</span><span class="sxs-lookup"><span data-stu-id="744ec-122">As new records are added, the oldest records are replaced.</span></span> <span data-ttu-id="744ec-123">Расположение самых старых и новых записей будет различным.</span><span class="sxs-lookup"><span data-stu-id="744ec-123">The location of the oldest and newest records will vary.</span></span> <span data-ttu-id="744ec-124">В следующем примере показан метод переноса.</span><span class="sxs-lookup"><span data-stu-id="744ec-124">The following example shows the wrapping method.</span></span>

    ``` syntax
    HEADER                   (ELF_LOGFILE_HEADER)
    Part of EVENT RECORD 300 (EVENTLOGRECORD)
    EVENT RECORD 301         (EVENTLOGRECORD)
    .
    .
    .
    EVENT RECORD 400         (EVENTLOGRECORD)
    EOF RECORD               (ELF_EOF_RECORD)
    Wasted space
    EVENT RECORD 102         (EVENTLOGRECORD)
    EVENT RECORD 103         (EVENTLOGRECORD)
    .
    .
    .
    EVENT RECORD 299         (EVENTLOGRECORD)
    Part of EVENT RECORD 300 (EVENTLOGRECORD)
    ```

    <span data-ttu-id="744ec-125">В примере самая старая запись больше 1, но — 102, поскольку пространство для записей от 1 до 101 было перезаписано.</span><span class="sxs-lookup"><span data-stu-id="744ec-125">In the example the oldest record is no longer 1, but is 102 because the space for records 1 to 101 was overwritten.</span></span>

    <span data-ttu-id="744ec-126">Между **\_ \_ записью EOF ELF** и самой старой записью имеется некоторое пространство, поскольку система удалит целое число записей, чтобы освободить место для последней записи.</span><span class="sxs-lookup"><span data-stu-id="744ec-126">There is some space between the **ELF\_EOF\_RECORD** and the oldest record because the system will erase an integral number of records to free space for the newest record.</span></span> <span data-ttu-id="744ec-127">Например, если последняя запись составляет 100 байт и две самые старые записи имеют длину 75 байт, система удалит две самые старые записи.</span><span class="sxs-lookup"><span data-stu-id="744ec-127">For example, if the newest record is 100 bytes long and the two oldest records are 75 bytes long, then the system will remove the two oldest records.</span></span> <span data-ttu-id="744ec-128">Дополнительные 50 байта будут использоваться позже при записи новых записей.</span><span class="sxs-lookup"><span data-stu-id="744ec-128">The extra 50 bytes will be used later when new records are written.</span></span>

    <span data-ttu-id="744ec-129">Файл журнала событий имеет фиксированный размер, и когда записи в файле переносятся в оболочку, запись в конце файла обычно разбивается на две записи.</span><span class="sxs-lookup"><span data-stu-id="744ec-129">An event log file has a fixed size and when the records in the file wrap, the record at the end of the file will typically be split into two records.</span></span> <span data-ttu-id="744ec-130">Например, если в позиции следующей записи находится 100 байт с конца файла, а размер записи составляет 300 байт, первые 100 байт будут записаны в конец файла, а следующие 200 байты будут записаны в начало файла сразу после **\_ \_ заголовка ELF**.</span><span class="sxs-lookup"><span data-stu-id="744ec-130">For example, if the position for the next write is 100 bytes from the end of the file and the size of the record is 300 bytes, the first 100 bytes will be written at the end of the file and the next 200 bytes will be written at the beginning of the file immediately after the **ELF\_LOGFILE\_HEADER**.</span></span> <span data-ttu-id="744ec-131">Если доступное место в конце файла меньше фиксированной части **EVENTLOGRECORD** (0x38 байт), то вся новая запись будет записана в начале файла сразу после **\_ \_ заголовков файла журнала ELF**.</span><span class="sxs-lookup"><span data-stu-id="744ec-131">If the available space at the end of the file is less than the fixed portion of the **EVENTLOGRECORD** (0x38 bytes), all of the new record will be written at the beginning of the file immediately after the **ELF\_LOGFILE\_HEADER**.</span></span> <span data-ttu-id="744ec-132">Неиспользуемые байты в конце файла будут заполнены шаблоном 0x00000027.</span><span class="sxs-lookup"><span data-stu-id="744ec-132">The unused bytes at the end of the file will be filled with the pattern 0x00000027.</span></span>

<span data-ttu-id="744ec-133">Дополнительные сведения и пример кода см. в разделе [сообщение о событии](reporting-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="744ec-133">For more information and a code example, see [Reporting an Event](reporting-an-event.md).</span></span>

 

 

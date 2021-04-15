---
description: Для ведения журнала событий используются следующие функции.
ms.assetid: fd5c12ec-3a3d-4b75-a573-0b27ae7a890b
title: Функции ведения журнала событий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 437899684861c5fc7ddbfe98c2499dc07bd9da8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683286"
---
# <a name="event-logging-functions"></a><span data-ttu-id="79397-103">Функции ведения журнала событий</span><span class="sxs-lookup"><span data-stu-id="79397-103">Event Logging Functions</span></span>

<span data-ttu-id="79397-104">Для ведения журнала событий используются следующие функции.</span><span class="sxs-lookup"><span data-stu-id="79397-104">The following functions are used with event logging.</span></span>



| <span data-ttu-id="79397-105">Функция</span><span class="sxs-lookup"><span data-stu-id="79397-105">Function</span></span>                                                         | <span data-ttu-id="79397-106">Описание</span><span class="sxs-lookup"><span data-stu-id="79397-106">Description</span></span>                                                                                         |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="79397-107">**баккупевентлог**</span><span class="sxs-lookup"><span data-stu-id="79397-107">**BackupEventLog**</span></span>](/windows/desktop/api/Winbase/nf-winbase-backupeventloga)                         | <span data-ttu-id="79397-108">Сохраняет указанный журнал событий в файл резервной копии.</span><span class="sxs-lookup"><span data-stu-id="79397-108">Saves the specified event log to a backup file.</span></span>                                                     |
| [<span data-ttu-id="79397-109">**клеаревентлог**</span><span class="sxs-lookup"><span data-stu-id="79397-109">**ClearEventLog**</span></span>](/windows/desktop/api/Winbase/nf-winbase-cleareventloga)                           | <span data-ttu-id="79397-110">Очищает указанный журнал событий и при необходимости сохраняет текущую копию журнала в файл резервной копии.</span><span class="sxs-lookup"><span data-stu-id="79397-110">Clears the specified event log, and optionally saves the current copy of the log to a backup file.</span></span>  |
| [<span data-ttu-id="79397-111">**клосивентлог**</span><span class="sxs-lookup"><span data-stu-id="79397-111">**CloseEventLog**</span></span>](/windows/desktop/api/Winbase/nf-winbase-closeeventlog)                           | <span data-ttu-id="79397-112">Закрывает маркер чтения для указанного журнала событий.</span><span class="sxs-lookup"><span data-stu-id="79397-112">Closes a read handle to the specified event log.</span></span>                                                    |
| [<span data-ttu-id="79397-113">**дерегистеревентсаурце**</span><span class="sxs-lookup"><span data-stu-id="79397-113">**DeregisterEventSource**</span></span>](/windows/desktop/api/Winbase/nf-winbase-deregistereventsource)           | <span data-ttu-id="79397-114">Закрывает маркер записи в указанный журнал событий.</span><span class="sxs-lookup"><span data-stu-id="79397-114">Closes a write handle to the specified event log.</span></span>                                                   |
| [<span data-ttu-id="79397-115">**жетевентлогинформатион**</span><span class="sxs-lookup"><span data-stu-id="79397-115">**GetEventLogInformation**</span></span>](/windows/desktop/api/Winbase/nf-winbase-geteventloginformation)         | <span data-ttu-id="79397-116">Извлекает сведения о указанном журнале событий.</span><span class="sxs-lookup"><span data-stu-id="79397-116">Retrieves information about the specified event log.</span></span>                                                |
| [<span data-ttu-id="79397-117">**жетнумберофевентлогрекордс**</span><span class="sxs-lookup"><span data-stu-id="79397-117">**GetNumberOfEventLogRecords**</span></span>](/windows/desktop/api/Winbase/nf-winbase-getnumberofeventlogrecords) | <span data-ttu-id="79397-118">Возвращает количество записей в указанном журнале событий.</span><span class="sxs-lookup"><span data-stu-id="79397-118">Retrieves the number of records in the specified event log.</span></span>                                         |
| [<span data-ttu-id="79397-119">**жетолдестевентлогрекорд**</span><span class="sxs-lookup"><span data-stu-id="79397-119">**GetOldestEventLogRecord**</span></span>](/windows/desktop/api/Winbase/nf-winbase-getoldesteventlogrecord)       | <span data-ttu-id="79397-120">Возвращает абсолютный номер записи самой старой записи в указанном журнале событий.</span><span class="sxs-lookup"><span data-stu-id="79397-120">Retrieves the absolute record number of the oldest record in the specified event log.</span></span>               |
| [<span data-ttu-id="79397-121">**нотифичанжеевентлог**</span><span class="sxs-lookup"><span data-stu-id="79397-121">**NotifyChangeEventLog**</span></span>](/windows/desktop/api/Winbase/nf-winbase-notifychangeeventlog)             | <span data-ttu-id="79397-122">Позволяет приложению принимать уведомления при записи события в указанный журнал событий.</span><span class="sxs-lookup"><span data-stu-id="79397-122">Enables an application to receive notification when an event is written to the specified event log.</span></span> |
| [<span data-ttu-id="79397-123">**опенбаккупевентлог**</span><span class="sxs-lookup"><span data-stu-id="79397-123">**OpenBackupEventLog**</span></span>](/windows/desktop/api/Winbase/nf-winbase-openbackupeventloga)                 | <span data-ttu-id="79397-124">Открывает обработчик для журнала событий резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="79397-124">Opens a handle to a backup event log.</span></span>                                                               |
| [<span data-ttu-id="79397-125">**опеневентлог**</span><span class="sxs-lookup"><span data-stu-id="79397-125">**OpenEventLog**</span></span>](/windows/desktop/api/Winbase/nf-winbase-openeventloga)                             | <span data-ttu-id="79397-126">Открывает обработчик для указанного журнала событий.</span><span class="sxs-lookup"><span data-stu-id="79397-126">Opens a handle to the specified event log.</span></span>                                                          |
| [<span data-ttu-id="79397-127">**реадевентлог**</span><span class="sxs-lookup"><span data-stu-id="79397-127">**ReadEventLog**</span></span>](/windows/desktop/api/Winbase/nf-winbase-readeventloga)                             | <span data-ttu-id="79397-128">Считывает целое число записей из указанного журнала событий.</span><span class="sxs-lookup"><span data-stu-id="79397-128">Reads a whole number of entries from the specified event log.</span></span>                                       |
| [<span data-ttu-id="79397-129">**регистеревентсаурце**</span><span class="sxs-lookup"><span data-stu-id="79397-129">**RegisterEventSource**</span></span>](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea)               | <span data-ttu-id="79397-130">Извлекает зарегистрированный обработчик в указанный журнал событий.</span><span class="sxs-lookup"><span data-stu-id="79397-130">Retrieves a registered handle to the specified event log.</span></span>                                           |
| [<span data-ttu-id="79397-131">**репортевент**</span><span class="sxs-lookup"><span data-stu-id="79397-131">**ReportEvent**</span></span>](/windows/desktop/api/Winbase/nf-winbase-reporteventa)                               | <span data-ttu-id="79397-132">Записывает запись в конец указанного журнала событий.</span><span class="sxs-lookup"><span data-stu-id="79397-132">Writes an entry at the end of the specified event log.</span></span>                                              |



 

 

 




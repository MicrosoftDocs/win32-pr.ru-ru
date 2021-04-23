---
description: Когда пользователь запускает Просмотр событий для просмотра записей журнала событий, он вызывает функцию Реадевентлог для получения структур EVENTLOGRECORD.
ms.assetid: 1d5b62cb-cf5b-4f4c-8521-1c783ae3afc7
title: Просмотр журнала событий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58c566fef29cfb110883741ddc0e6c298d6a1255
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264048"
---
# <a name="viewing-the-event-log"></a><span data-ttu-id="39c21-103">Просмотр журнала событий</span><span class="sxs-lookup"><span data-stu-id="39c21-103">Viewing the Event Log</span></span>

<span data-ttu-id="39c21-104">Когда пользователь запускает Просмотр событий для просмотра записей журнала событий, он вызывает функцию [**реадевентлог**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) для получения структур [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) .</span><span class="sxs-lookup"><span data-stu-id="39c21-104">When the user starts Event Viewer to view the event log entries, it calls the [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) function to obtain the [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) structures.</span></span> <span data-ttu-id="39c21-105">Просмотр событий использует источник события и идентификатор события для получения текста сообщения для каждого события из зарегистрированного файла сообщения (указывается значением реестра **евентмессажефиле** для источника).</span><span class="sxs-lookup"><span data-stu-id="39c21-105">The Event Viewer uses the event source and event identifier to get message text for each event from the registered message file (indicated by the **EventMessageFile** registry value for the source).</span></span> <span data-ttu-id="39c21-106">Просмотр событий использует функцию [**LoadLibraryEx**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa) для загрузки файла сообщения.</span><span class="sxs-lookup"><span data-stu-id="39c21-106">The Event Viewer uses the [**LoadLibraryEx**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa) function to load the message file.</span></span> <span data-ttu-id="39c21-107">Затем Просмотр событий использует функцию [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) для получения базовой строки описания из загруженного модуля.</span><span class="sxs-lookup"><span data-stu-id="39c21-107">The Event Viewer then uses the [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) function to retrieve the base description string from the loaded module.</span></span> <span data-ttu-id="39c21-108">Наконец, Просмотр событий заменяет параметры вставки в базовой строке описания для получения окончательной строки сообщения.</span><span class="sxs-lookup"><span data-stu-id="39c21-108">Finally, the Event Viewer replaces the insertion parameters in the base description string to yield the final message string.</span></span>

 

 

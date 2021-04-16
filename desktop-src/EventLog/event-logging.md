---
description: Многие приложения регистрируют ошибки и события в собственных журналах ошибок, каждый из которых имеет собственный формат и пользовательский интерфейс.
ms.assetid: 5ec95938-ac5d-4f63-9080-2de71454eb17
title: Ведение журнала событий (ведение журнала событий)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d9871fdb7c7b81bdf57a8c5de87a0a09d5a0570
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684202"
---
# <a name="event-logging-event-logging"></a><span data-ttu-id="26b0a-103">Ведение журнала событий (ведение журнала событий)</span><span class="sxs-lookup"><span data-stu-id="26b0a-103">Event Logging (Event Logging)</span></span>

<span data-ttu-id="26b0a-104">Многие приложения регистрируют ошибки и события в собственных журналах ошибок, каждый из которых имеет собственный формат и пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="26b0a-104">Many applications record errors and events in proprietary error logs, each with their own format and user interface.</span></span> <span data-ttu-id="26b0a-105">Данные из разных приложений не могут быть легко объединены в один полный отчет, поэтому системным администраторам или представителям службы поддержки следует проверять различные источники для диагностики проблем.</span><span class="sxs-lookup"><span data-stu-id="26b0a-105">Data from different applications can't easily be merged into one complete report, requiring system administrators or support representatives to check a variety of sources to diagnose problems.</span></span>

<span data-ttu-id="26b0a-106">Ведение журнала событий предоставляет стандартный, централизованный способ, с помощью которого приложения (и операционная система) записывают важные события программного обеспечения и оборудования.</span><span class="sxs-lookup"><span data-stu-id="26b0a-106">Event logging provides a standard, centralized way for applications (and the operating system) to record important software and hardware events.</span></span> <span data-ttu-id="26b0a-107">Служба ведения журнала событий записывает события из различных источников и сохраняет их в одной коллекции, называемой *журналом событий*.</span><span class="sxs-lookup"><span data-stu-id="26b0a-107">The event logging service records events from various sources and stores them in a single collection called an *event log*.</span></span> <span data-ttu-id="26b0a-108">Просмотр событий позволяет просматривать журналы; программный интерфейс также позволяет анализировать журналы.</span><span class="sxs-lookup"><span data-stu-id="26b0a-108">The Event Viewer enables you to view logs; the programming interface also enables you to examine logs.</span></span>

-   [<span data-ttu-id="26b0a-109">Сведения о ведении журнала событий</span><span class="sxs-lookup"><span data-stu-id="26b0a-109">About Event Logging</span></span>](about-event-logging.md)
-   [<span data-ttu-id="26b0a-110">Использование ведения журнала событий</span><span class="sxs-lookup"><span data-stu-id="26b0a-110">Using Event Logging</span></span>](using-event-logging.md)
-   [<span data-ttu-id="26b0a-111">Справочник по ведению журнала событий</span><span class="sxs-lookup"><span data-stu-id="26b0a-111">Event Logging Reference</span></span>](event-logging-reference.md)

> [!Note]  
> <span data-ttu-id="26b0a-112">API ведения журнала событий предназначен для приложений, работающих в операционной системе Windows Server 2003, Windows XP или Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="26b0a-112">The Event Logging API was designed for applications that run on the Windows Server 2003, Windows XP, or Windows 2000 operating system.</span></span> <span data-ttu-id="26b0a-113">В Windows Vista инфраструктура ведения журнала событий была изменена.</span><span class="sxs-lookup"><span data-stu-id="26b0a-113">In Windows Vista, the event logging infrastructure was redesigned.</span></span> <span data-ttu-id="26b0a-114">Приложения, предназначенные для работы в Windows Vista или более поздних операционных системах, должны использовать [журнал событий Windows](/windows/desktop/WES/windows-event-log) для регистрации событий.</span><span class="sxs-lookup"><span data-stu-id="26b0a-114">Applications that are designed to run on Windows Vista or later operating systems should use [Windows Event Log](/windows/desktop/WES/windows-event-log) to log events.</span></span>

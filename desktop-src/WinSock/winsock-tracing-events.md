---
description: Сведения о событиях трассировки Winsock.
ms.assetid: 246AE0BE-E8E2-4291-8BF4-577F889F055B
title: События трассировки Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aeabd2d06741f8dfa1f47b513a09c941ee1490b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144932"
---
# <a name="winsock-tracing-events"></a><span data-ttu-id="3d584-103">События трассировки Winsock</span><span class="sxs-lookup"><span data-stu-id="3d584-103">Winsock Tracing Events</span></span>

<span data-ttu-id="3d584-104">В этом разделе описаны подробные сведения о конкретных событиях трассировки Winsock.</span><span class="sxs-lookup"><span data-stu-id="3d584-104">This section describes detailed information on specific Winsock Tracing Events details.</span></span>

<span data-ttu-id="3d584-105">Трассировка Winsock — это функция устранения неполадок, которую можно включить в двоичных файлах розничной торговли для трассировки определенных событий Windows Socket с минимальными издержками.</span><span class="sxs-lookup"><span data-stu-id="3d584-105">Winsock tracing is a troubleshooting feature that can be enabled in retail binaries to trace certain Windows socket events with minimal overhead.</span></span> <span data-ttu-id="3d584-106">Эта функция обеспечивает улучшенные возможности диагностики для разработчиков и поддержки продуктов.</span><span class="sxs-lookup"><span data-stu-id="3d584-106">This feature allows for better diagnostic capabilities for developers and product support.</span></span> <span data-ttu-id="3d584-107">Трассировка событий сети Winsock поддерживает операции сокета трассировки для приложений IPv4 и IPv6.</span><span class="sxs-lookup"><span data-stu-id="3d584-107">Winsock network event tracing supports tracing socket operations for IPv4 and IPv6 applications.</span></span> <span data-ttu-id="3d584-108">Трассировка изменений каталога Winsock поддерживает трассировку изменений, внесенных в каталог Winsock с помощью многоуровневых поставщиков служб (LSP).</span><span class="sxs-lookup"><span data-stu-id="3d584-108">Winsock catalog change tracing supports tracing changes made to the Winsock catalog by layered service providers (LSPs).</span></span>

> [!Note]  
> <span data-ttu-id="3d584-109">Многоуровневые поставщики служб являются устаревшими.</span><span class="sxs-lookup"><span data-stu-id="3d584-109">Layered Service Providers are deprecated.</span></span> <span data-ttu-id="3d584-110">Начиная с Windows 8 и Windows Server 2012, используйте [платформу фильтрации Windows](../fwp/windows-filtering-platform-start-page.md).</span><span class="sxs-lookup"><span data-stu-id="3d584-110">Starting with Windows 8 and Windows Server 2012, use [Windows Filtering Platform](../fwp/windows-filtering-platform-start-page.md).</span></span>

 

<span data-ttu-id="3d584-111">Трассировка Winsock использует средство трассировки событий для Windows (ETW), предназначенное для общего назначения, высокоскоростной трассировки, обеспечиваемой операционной системой.</span><span class="sxs-lookup"><span data-stu-id="3d584-111">Winsock tracing uses Event Tracing for Windows (ETW), a general-purpose, high-speed tracing facility provided by the operating system.</span></span> <span data-ttu-id="3d584-112">ETW предоставляет механизм трассировки для событий, создаваемых как приложениями пользовательского режима, так и драйверами устройств в режиме ядра.</span><span class="sxs-lookup"><span data-stu-id="3d584-112">ETW provides a tracing mechanism for events raised by both user-mode applications and kernel-mode device drivers.</span></span> <span data-ttu-id="3d584-113">ETW может динамически включать и отключать ведение журнала, что упрощает выполнение подробной трассировки в рабочих средах без необходимости перезагрузки или перезапуска приложений.</span><span class="sxs-lookup"><span data-stu-id="3d584-113">ETW can enable and disable logging dynamically, making it easy to perform detailed tracing in production environments without requiring reboots or application restarts.</span></span> <span data-ttu-id="3d584-114">Поддержка трассировки Winsock с помощью ETW была добавлена в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="3d584-114">Support for Winsock tracing using ETW was added on Windows Vista and later.</span></span> <span data-ttu-id="3d584-115">Общие сведения о трассировке событий Windows см. в статье [улучшение отладки и настройка производительности с помощью ETW](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw).</span><span class="sxs-lookup"><span data-stu-id="3d584-115">For general information on ETW, see [Improve Debugging And Performance Tuning With ETW](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw).</span></span>

<span data-ttu-id="3d584-116">В следующем списке приведены подробные сведения о каждом событии трассировки Winsock.</span><span class="sxs-lookup"><span data-stu-id="3d584-116">The following list provides detailed information for each Winsock tracing event.</span></span> <span data-ttu-id="3d584-117">Для получения дополнительных сведений о любом событии щелкните имя события.</span><span class="sxs-lookup"><span data-stu-id="3d584-117">For additional information on any event, click the event name.</span></span>



| <span data-ttu-id="3d584-118">Название мероприятия</span><span class="sxs-lookup"><span data-stu-id="3d584-118">Event Name</span></span>                                                            | <span data-ttu-id="3d584-119">Описание</span><span class="sxs-lookup"><span data-stu-id="3d584-119">Description</span></span>                                                                               |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3d584-120">**\_Создание события \_ АФД**</span><span class="sxs-lookup"><span data-stu-id="3d584-120">**AFD\_EVENT\_CREATE**</span></span>](afd-event-create.md)                        | <span data-ttu-id="3d584-121">Событие трассировки сети Winsock для операции создания сокета.</span><span class="sxs-lookup"><span data-stu-id="3d584-121">Winsock network tracing event for a socket creation operation.</span></span>                            |
| [<span data-ttu-id="3d584-122">**\_закрытие события \_ АФД**</span><span class="sxs-lookup"><span data-stu-id="3d584-122">**AFD\_EVENT\_CLOSE**</span></span>](afd-event-close.md)                          | <span data-ttu-id="3d584-123">Событие трассировки сети Winsock для операции закрытия сокета.</span><span class="sxs-lookup"><span data-stu-id="3d584-123">Winsock network tracing event for socket close operation.</span></span>                                 |
| [<span data-ttu-id="3d584-124">**\_ \_ Установка LSP Winsock \_ WS2HELP**</span><span class="sxs-lookup"><span data-stu-id="3d584-124">**WINSOCK\_WS2HELP\_LSP\_INSTALL**</span></span>](winsock-ws2help-lsp-install.md) | <span data-ttu-id="3d584-125">Событие изменения каталога Winsock для операции установки поставщика многоуровневой службы (LSP).</span><span class="sxs-lookup"><span data-stu-id="3d584-125">Winsock catalog change event for a layered service provider (LSP) installation operation.</span></span> |
| [<span data-ttu-id="3d584-126">**\_ \_ Удаление LSP Winsock \_ WS2HELP**</span><span class="sxs-lookup"><span data-stu-id="3d584-126">**WINSOCK\_WS2HELP\_LSP\_REMOVE**</span></span>](winsock-ws2help-lsp-remove.md)   | <span data-ttu-id="3d584-127">Событие изменения каталога Winsock для операции удаления поставщика многоуровневой службы (LSP).</span><span class="sxs-lookup"><span data-stu-id="3d584-127">Winsock catalog change event for a layered service provider (LSP) removal operation.</span></span>      |
| [<span data-ttu-id="3d584-128">**\_ \_ Отключение LSP Winsock \_ WS2HELP**</span><span class="sxs-lookup"><span data-stu-id="3d584-128">**WINSOCK\_WS2HELP\_LSP\_DISABLE**</span></span>](winsock-ws2help-lsp-disable.md) | <span data-ttu-id="3d584-129">Событие изменения каталога Winsock для операции отключения поставщика многоуровневой службы (LSP).</span><span class="sxs-lookup"><span data-stu-id="3d584-129">Winsock catalog change event for a layered service provider (LSP) disable operation.</span></span>      |
| [<span data-ttu-id="3d584-130">**\_ \_ Сброс LSP Winsock \_ WS2HELP**</span><span class="sxs-lookup"><span data-stu-id="3d584-130">**WINSOCK\_WS2HELP\_LSP\_RESET**</span></span>](winsock-ws2help-lsp-reset.md)     | <span data-ttu-id="3d584-131">Событие изменения каталога Winsock для операции сброса каталога Winsock.</span><span class="sxs-lookup"><span data-stu-id="3d584-131">Winsock catalog change event for a Winsock catalog reset operation.</span></span>                       |



 

## <a name="related-topics"></a><span data-ttu-id="3d584-132">См. также</span><span class="sxs-lookup"><span data-stu-id="3d584-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d584-133">Усовершенствованные отладка и настройка производительности с помощью приложения ETW</span><span class="sxs-lookup"><span data-stu-id="3d584-133">Improve Debugging And Performance Tuning With ETW</span></span>](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw)
</dt> <dt>

[<span data-ttu-id="3d584-134">Трассировка Winsock</span><span class="sxs-lookup"><span data-stu-id="3d584-134">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="3d584-135">Уровни трассировки Winsock</span><span class="sxs-lookup"><span data-stu-id="3d584-135">Winsock Tracing Levels</span></span>](winsock-tracing-levels.md)
</dt> <dt>

[<span data-ttu-id="3d584-136">Управление трассировкой Winsock</span><span class="sxs-lookup"><span data-stu-id="3d584-136">Control of Winsock Tracing</span></span>](control-of-winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="3d584-137">Сведения о трассировке событий сети Winsock</span><span class="sxs-lookup"><span data-stu-id="3d584-137">Winsock Network Event Tracing Details</span></span>](winsock-tracing-event-details.md)
</dt> <dt>

[<span data-ttu-id="3d584-138">Сведения о трассировке изменений каталога Winsock</span><span class="sxs-lookup"><span data-stu-id="3d584-138">Winsock Catalog Change Tracing Details</span></span>](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

 

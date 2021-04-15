---
description: Мониторы предназначены для запуска событий на локальных или удаленных компьютерах с помощью инструментарий управления Windows (WMI) (WMI).
ms.assetid: b20746dd-d8d9-49b6-95b7-5151ee02901d
title: Мониторинг событий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d98241081d8a59c33ab173447eaedd903e72eb09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497613"
---
# <a name="monitor-events"></a><span data-ttu-id="d29ec-103">Мониторинг событий</span><span class="sxs-lookup"><span data-stu-id="d29ec-103">Monitor Events</span></span>

<span data-ttu-id="d29ec-104">Мониторы предназначены для запуска событий на локальных или удаленных компьютерах с помощью [инструментарий управления Windows (WMI)](/windows/desktop/WmiSdk/wmi-start-page) (WMI).</span><span class="sxs-lookup"><span data-stu-id="d29ec-104">Monitors are designed to use [Windows Management Instrumentation](/windows/desktop/WmiSdk/wmi-start-page) (WMI) to fire events to local or remote computers.</span></span>

> [!Note]  
> <span data-ttu-id="d29ec-105">Так как мониторы используют запись в режиме реального времени, они могут записывать только данные на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="d29ec-105">Because monitors use a real-time capture they can only capture data at the local computer.</span></span> <span data-ttu-id="d29ec-106">Это ограничение интерфейса **ИРТК** поставщика сетевых пакетов.</span><span class="sxs-lookup"><span data-stu-id="d29ec-106">This is a limitation of the network packet provider's **IRTC** interface.</span></span> <span data-ttu-id="d29ec-107">Однако с помощью событий WMI захваченные данные могут быть проверены локально, а события могут отправляться на локальные или удаленные компьютеры.</span><span class="sxs-lookup"><span data-stu-id="d29ec-107">However, by using WMI events, the captured data can be examined locally while events can be sent to local or remote computers.</span></span>

 

<span data-ttu-id="d29ec-108">Мониторы не взаимодействуют напрямую с WMI.</span><span class="sxs-lookup"><span data-stu-id="d29ec-108">Monitors do not communicate directly with WMI.</span></span> <span data-ttu-id="d29ec-109">[*Служба контроля мониторинга*](m.md) (мксвк) предоставляет интерфейс (именуемый [имониторевентер](imonitoreventer.md)), который монитор может использовать для получения структуры данных событий и заполнения ее соответствующими данными.</span><span class="sxs-lookup"><span data-stu-id="d29ec-109">The [*Monitor Control Service*](m.md) (MCSVC) provides an interface (called [IMonitorEventer](imonitoreventer.md)), which the monitor can use to obtain an event data structure and fill it with the relevant information.</span></span> <span data-ttu-id="d29ec-110">Затем МКСВК может отправить структуру данных события в WMI, что, в свою очередь, вызывает событие.</span><span class="sxs-lookup"><span data-stu-id="d29ec-110">The MCSVC can then send the event data structure to WMI, which in turn fires the event.</span></span>

 

 

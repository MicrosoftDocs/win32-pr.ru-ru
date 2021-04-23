---
title: Трассировка сети в Windows 7
description: Windows 7 расширяет инфраструктуру диагностики сети (NDF), чтобы обеспечить быстрый способ устранения проблем с сетевым подключением, включив сбор всех необходимых данных за один шаг и используя средство трассировки событий Windows (ETW) для записи пакетов событий сети в один файл.
ms.assetid: 7d331362-ff26-4ca0-aa45-07cc97304c7c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e3abb4283262703123f8e7060a09af0b810477b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413672"
---
# <a name="network-tracing-in-windows-7"></a><span data-ttu-id="fc7d4-103">Трассировка сети в Windows 7</span><span class="sxs-lookup"><span data-stu-id="fc7d4-103">Network Tracing in Windows 7</span></span>

<span data-ttu-id="fc7d4-104">По мере роста сложности сетевого стека часто бывает трудно быстро отслеживать и диагностировать проблемы в стеке.</span><span class="sxs-lookup"><span data-stu-id="fc7d4-104">As the complexity of the networking stack increases, it is often difficult to quickly trace and diagnose issues within the stack.</span></span> <span data-ttu-id="fc7d4-105">Windows 7 расширяет инфраструктуру диагностики сети (NDF), чтобы обеспечить быстрый способ устранения проблем с сетевым подключением, включив сбор всех необходимых данных за один шаг и используя средство [трассировки событий Windows (ETW)](../etw/event-tracing-portal.md) для записи в журнал событий сети, & пакеты в одном файле.</span><span class="sxs-lookup"><span data-stu-id="fc7d4-105">Windows 7 expands on the Network Diagnostic Framework (NDF) to provide a quick method for troubleshooting network connectivity issues by enabling collection of all the needed information in one step, and by leveraging [Event Tracing for Windows (ETW)](../etw/event-tracing-portal.md) to log network events & packets in a single file.</span></span>

<span data-ttu-id="fc7d4-106">Связанные события и пакеты группируются для конкретного действия, например для обзора веб-сайта, по различным компонентам в сетевом стеке.</span><span class="sxs-lookup"><span data-stu-id="fc7d4-106">Related events and packets are grouped together for a given activity, such as browsing a website, across the various components in the networking stack.</span></span> <span data-ttu-id="fc7d4-107">Выходными данными этого процесса является файл журнала трассировки событий (ETL).</span><span class="sxs-lookup"><span data-stu-id="fc7d4-107">The output of this process is an Event Trace Log (ETL) file.</span></span> <span data-ttu-id="fc7d4-108">Разрешая всем событиям, связанным с конкретным действием, одновременно просматриваться в этом файле, время, необходимое для изоляции и диагностики сетевых проблем, может значительно снизиться.</span><span class="sxs-lookup"><span data-stu-id="fc7d4-108">By allowing all of the events related to a specific activity to be viewed at once in this file, the time required to isolate and diagnose network issues can be greatly reduced.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="fc7d4-109">в этом разделе</span><span class="sxs-lookup"><span data-stu-id="fc7d4-109">In This Section</span></span>



| <span data-ttu-id="fc7d4-110">Раздел</span><span class="sxs-lookup"><span data-stu-id="fc7d4-110">Topic</span></span>                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fc7d4-111">Трассировка сети в Windows 7: архитектура</span><span class="sxs-lookup"><span data-stu-id="fc7d4-111">Network Tracing in Windows 7: Architecture</span></span>](network-tracing-in-windows-7-architecture.md)                                |
| [<span data-ttu-id="fc7d4-112">Средства для устранения неполадок с помощью трассировки сети в Windows 7</span><span class="sxs-lookup"><span data-stu-id="fc7d4-112">Tools for Troubleshooting using Network Tracing in Windows 7</span></span>](tools-for-troubleshooting-network-tracing-in-windows-7.md) |
| [<span data-ttu-id="fc7d4-113">Трассировка сети в Windows 7: сценарии</span><span class="sxs-lookup"><span data-stu-id="fc7d4-113">Network Tracing in Windows 7: Scenarios</span></span>](network-tracing-in-windows-7-scenarios.md)                                      |



 

 

 
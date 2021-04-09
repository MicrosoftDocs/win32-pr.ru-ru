---
title: О SNMP
description: Протокол SNMP использует распределенную архитектуру, состоящую из руководителей и агентов.
ms.assetid: 55be55a8-1968-4373-a969-f7e03b75a824
keywords:
- SNMP, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd1dab65173c96dce4bbd2f30edbca2a91f6153d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070448"
---
# <a name="about-snmp"></a><span data-ttu-id="7b889-104">О SNMP</span><span class="sxs-lookup"><span data-stu-id="7b889-104">About SNMP</span></span>

<span data-ttu-id="7b889-105">\[Протокол SNMP доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="7b889-105">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7b889-106">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="7b889-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="7b889-107">Вместо этого используйте [Служба удаленного управления Windows](/windows/desktop/WinRM/portal), который является реализацией Microsoft WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="7b889-107">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="7b889-108">Протокол SNMP использует распределенную архитектуру, состоящую из руководителей и агентов.</span><span class="sxs-lookup"><span data-stu-id="7b889-108">SNMP uses a distributed architecture consisting of managers and agents.</span></span> <span data-ttu-id="7b889-109">Агент — это приложение SNMP, которое реагирует на запросы от приложений диспетчера SNMP.</span><span class="sxs-lookup"><span data-stu-id="7b889-109">An agent is an SNMP application that responds to queries from SNMP manager applications.</span></span> <span data-ttu-id="7b889-110">Агент SNMP отвечает за получение и обновление сведений о локальном управлении на основе запросов диспетчера SNMP.</span><span class="sxs-lookup"><span data-stu-id="7b889-110">The SNMP agent is responsible for retrieving and updating local management information based on the requests of the SNMP manager.</span></span> <span data-ttu-id="7b889-111">Агент также сообщает зарегистрированным диспетчерам о возникновении значительных событий или ловушек.</span><span class="sxs-lookup"><span data-stu-id="7b889-111">The agent also notifies registered managers when significant events or traps occur.</span></span> <span data-ttu-id="7b889-112">Диспетчер — это приложение SNMP, которое создает запросы к приложениям агента SNMP и получает ловушки от приложений агента SNMP.</span><span class="sxs-lookup"><span data-stu-id="7b889-112">A manager is an SNMP application that generates queries to SNMP agent applications and receives traps from SNMP agent applications.</span></span>

<span data-ttu-id="7b889-113">На компьютерах под управлением Microsoft Windows XP/Windows 2000 или Windows NT агент SNMP реализуется службой SNMP (SNMP.EXE).</span><span class="sxs-lookup"><span data-stu-id="7b889-113">On computers running Microsoft Windows XP/Windows 2000/Windows NT, the SNMP agent is implemented by the SNMP service (SNMP.EXE).</span></span> <span data-ttu-id="7b889-114">Диспетчер SNMP обычно является консольным приложением управления SNMP стороннего производителя.</span><span class="sxs-lookup"><span data-stu-id="7b889-114">The SNMP manager is typically a third-party SNMP management console application.</span></span> <span data-ttu-id="7b889-115">Консольное приложение управления не требуется запускать на том же узле, что и агент SNMP.</span><span class="sxs-lookup"><span data-stu-id="7b889-115">The management console application does not need to run on the same host as the SNMP agent.</span></span> <span data-ttu-id="7b889-116">Чтобы использовать сведения, предоставляемые службой Microsoft SNMP, необходимо по крайней мере одно консольное приложение управления SNMP.</span><span class="sxs-lookup"><span data-stu-id="7b889-116">To use the information the Microsoft SNMP service provides, you need at least one SNMP management console application.</span></span> <span data-ttu-id="7b889-117">Система включает библиотеки, поддерживающие консольные приложения управления SNMP, но в настоящее время она не включает в себя консольное приложение управления SNMP.</span><span class="sxs-lookup"><span data-stu-id="7b889-117">The system includes libraries that support SNMP management console applications, but it does not include an SNMP management console application at this time.</span></span>

 

 
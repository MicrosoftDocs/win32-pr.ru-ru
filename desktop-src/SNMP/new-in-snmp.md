---
title: Новые в SNMP
description: Протокол SNMP поддерживает использование IPv6, начиная с Windows Vista.
ms.assetid: 38d71c0a-8de1-45a7-958c-aa44411451bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 913f71cdf0b23800340f2c43f7b7fa22f45883a2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793488"
---
# <a name="new-in-snmp"></a><span data-ttu-id="b4729-103">Новые в SNMP</span><span class="sxs-lookup"><span data-stu-id="b4729-103">New in SNMP</span></span>

<span data-ttu-id="b4729-104">\[Протокол SNMP доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="b4729-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b4729-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="b4729-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="b4729-106">Вместо этого используйте [Служба удаленного управления Windows](/windows/desktop/WinRM/portal), который является реализацией Microsoft WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="b4729-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="b4729-107">Протокол SNMP поддерживает использование IPv6, начиная с Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b4729-107">SNMP supports the use of IPv6 starting with Windows Vista.</span></span> <span data-ttu-id="b4729-108">Однако протокол SNMP поддерживает IPv6 только для сетей под управлением Windows Server 2008 и Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b4729-108">However, SNMP supports IPv6 only for networks running Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="b4729-109">Это связано с тем, что для поддержки IPv6 протоколу SNMP требуется обновленный стек протокола, доступный в этих операционных системах.</span><span class="sxs-lookup"><span data-stu-id="b4729-109">This is because SNMP requires the updated protocol stack available in these operating systems for its IPv6 support.</span></span>

<span data-ttu-id="b4729-110">Если сеть не является исключительно сетью Windows Server 2008, связь по протоколу IPv6 завершится сбоем, даже если на тех компьютерах, где работают предыдущие версии Windows, установлен стек протокола IPv6.</span><span class="sxs-lookup"><span data-stu-id="b4729-110">Unless your network is solely a Windows Server 2008 network, IPv6 communications will fail, even if an IPv6 protocol stack is separately installed on those computers that run earlier versions of Windows.</span></span> <span data-ttu-id="b4729-111">Например, агенты SNMP, работающие на Windows Server 2003, Windows XP или Windows 2000, отвечают только на запросы, созданные для их IPv4-адресов.</span><span class="sxs-lookup"><span data-stu-id="b4729-111">For example, SNMP agents that run on Windows Server 2003, or Windows XP, or Windows 2000, respond only to queries that are made to their IPv4 addresses.</span></span>

 

 
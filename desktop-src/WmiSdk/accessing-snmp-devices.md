---
description: Позволяет клиентским приложениям получать доступ к информации SNMP через WMI.
ms.assetid: d9e3fd1d-8320-4407-9a9e-e2eb5dd62fef
ms.tgt_platform: multiple
title: Доступ к SNMP-устройствам
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37a349053f054f3e8ad9dffb7c108d2bee6c6d8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693751"
---
# <a name="accessing-snmp-devices"></a><span data-ttu-id="1e115-103">Доступ к SNMP-устройствам</span><span class="sxs-lookup"><span data-stu-id="1e115-103">Accessing SNMP Devices</span></span>

<span data-ttu-id="1e115-104">Поставщик SNMP позволяет клиентским приложениям получать доступ к информации SNMP через WMI.</span><span class="sxs-lookup"><span data-stu-id="1e115-104">The Simple Network Management Protocol (SNMP) provider allows client applications to access SNMP information through WMI.</span></span> <span data-ttu-id="1e115-105">[Поставщик SNMP](snmp-provider.md) выступает в качестве шлюза для систем и устройств, использующих SNMP для управления.</span><span class="sxs-lookup"><span data-stu-id="1e115-105">The [SNMP provider](snmp-provider.md) acts as a gateway to systems and devices that use SNMP for management.</span></span> <span data-ttu-id="1e115-106">Только на компьютере управления или мониторинга должен быть установлен инструментарий WMI, так как он может выполнять чтение с любого устройства с поддержкой SNMP.</span><span class="sxs-lookup"><span data-stu-id="1e115-106">Only the management or monitoring computer must be running WMI because it can read from any SNMP-enabled device.</span></span>

> [!Note]  
> <span data-ttu-id="1e115-107">Дополнительные сведения об установке поставщика см. в разделе [Настройка среды SNMP WMI](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="1e115-107">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="1e115-108">Переменные объектов MIB могут быть считаны и записаны в, а SNMP-ловушки могут быть автоматически сопоставлены с событиями WMI, которые могут быть определены для любых произвольных операций создания, удаления или обновления данных за пределами ловушек, определенных MIB.</span><span class="sxs-lookup"><span data-stu-id="1e115-108">SNMP Management Information Base (MIB) object variables can be read from and written to, and SNMP traps can be automatically mapped to WMI events, which can be defined for any arbitrary create, delete, or update operations to data beyond the MIB-defined traps.</span></span> <span data-ttu-id="1e115-109">Эта функция инструментария WMI работает в качестве расширения стандартных возможностей SNMP.</span><span class="sxs-lookup"><span data-stu-id="1e115-109">This feature of WMI functions as an extension of standard SNMP capabilities.</span></span> <span data-ttu-id="1e115-110">Дополнительные сведения см. в разделе [наблюдение за событиями](monitoring-events.md).</span><span class="sxs-lookup"><span data-stu-id="1e115-110">For more information, see [Monitoring Events](monitoring-events.md).</span></span>

<span data-ttu-id="1e115-111">Средства, описанные в следующих разделах, предназначены для программистов, использующих сценарии Windows и C/C++.</span><span class="sxs-lookup"><span data-stu-id="1e115-111">The tools described in the following topics are designed for use by Windows scripting and C/C++ programmers.</span></span> <span data-ttu-id="1e115-112">Мы советуем ознакомиться с инструментарием WMI, систем с интерфейсом и SNMPv2C и опытом работы с сетями и понятиями управления сетью.</span><span class="sxs-lookup"><span data-stu-id="1e115-112">Familiarity with WMI, SNMPv1 and SNMPv2C, and a working knowledge of networking and network management concepts are recommended.</span></span>

<span data-ttu-id="1e115-113">Дополнительные сведения об использовании WMI с SNMP см. [в разделе Настройка среды SNMP WMI](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="1e115-113">For more information about using WMI with SNMP, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

 




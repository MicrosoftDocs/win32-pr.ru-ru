---
description: Поставщики событий SNMP получают пакеты событий SNMP из стека WINSNMP и преобразуют сведения, содержащиеся в пакетах, в события WMI.
ms.assetid: 4ae0a734-39b0-4418-b55c-6d8f093806a8
ms.tgt_platform: multiple
title: Выбор поставщиков событий SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dabd8f6d432025406a5faecc3ace423cd6671e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712529"
---
# <a name="choosing-between-snmp-event-providers"></a><span data-ttu-id="ff256-103">Выбор поставщиков событий SNMP</span><span class="sxs-lookup"><span data-stu-id="ff256-103">Choosing Between SNMP Event Providers</span></span>

<span data-ttu-id="ff256-104">Поставщики событий SNMP получают пакеты событий SNMP из стека WINSNMP и преобразуют сведения, содержащиеся в пакетах, в события WMI.</span><span class="sxs-lookup"><span data-stu-id="ff256-104">SNMP event providers receive SNMP event packets from the WINSNMP stack and translate the information included in the packets into WMI events.</span></span>

<span data-ttu-id="ff256-105">WMI включает следующие два поставщика событий SNMP:</span><span class="sxs-lookup"><span data-stu-id="ff256-105">WMI includes the following two SNMP event providers:</span></span>

-   <span data-ttu-id="ff256-106">Поставщик инкапсулированных событий SNMP (СиП)</span><span class="sxs-lookup"><span data-stu-id="ff256-106">SNMP Encapsulated Event provider (SEEP)</span></span>

    <span data-ttu-id="ff256-107">Инкапсулированная инициализация означает, что экземпляр события имеет простые свойства, описывающие информацию, сопоставленную непосредственно с SNMP-ловушкой.</span><span class="sxs-lookup"><span data-stu-id="ff256-107">Encapsulated provision means that the event instance has simple properties describing the information mapped directly from the SNMP trap.</span></span>

-   <span data-ttu-id="ff256-108">Поставщик событий SNMP референт (СРЕП)</span><span class="sxs-lookup"><span data-stu-id="ff256-108">SNMP Referent Event provider (SREP)</span></span>

    <span data-ttu-id="ff256-109">Референтная инициализация абстрагирует сведения, присутствующие в ловушке SNMP, чтобы свойства, использующие один и тот же класс и экземпляр, представлялись как внедренные объекты.</span><span class="sxs-lookup"><span data-stu-id="ff256-109">Referent provision abstracts the information present within the SNMP trap so that properties which share the same class and instance are presented as embedded objects.</span></span> <span data-ttu-id="ff256-110">Это позволяет получить уникальный экземпляр, с которым связана ловушка, после получения события с помощью SNMP \_ \_ релпас.</span><span class="sxs-lookup"><span data-stu-id="ff256-110">This allows for the unique instance, with which the trap is associated, to be retrieved after the receipt of the event, using the SNMP \_\_RELPATH.</span></span>

> [!Note]  
> <span data-ttu-id="ff256-111">Дополнительные сведения об установке поставщика см. в разделе [Настройка среды SNMP WMI](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="ff256-111">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="ff256-112">Независимо от того, является ли событие SNMP незашифрованным или SNMPv2C уведомлением, стек сообщает об этом как уведомление SNMPv2.</span><span class="sxs-lookup"><span data-stu-id="ff256-112">Regardless of whether the SNMP event is an SNMPv1 trap or an SNMPv2C notification, the stack reports it as an SNMPv2 notification.</span></span> <span data-ttu-id="ff256-113">Поэтому поставщики событий обрабатывают все события SNMP как уведомления SNMPv2.</span><span class="sxs-lookup"><span data-stu-id="ff256-113">Therefore, the event providers process all SNMP events as SNMPv2 notifications.</span></span>

<span data-ttu-id="ff256-114">Для описания событий SNMP для потребителей WMI каждый поставщик событий поддерживает иерархию классов, производных от класса System [**\_ \_ екстринсицевент**](--extrinsicevent.md) .</span><span class="sxs-lookup"><span data-stu-id="ff256-114">To describe the SNMP events to WMI consumers, each event provider supports a hierarchy of classes that derives from the [**\_\_ExtrinsicEvent**](--extrinsicevent.md) system class.</span></span> <span data-ttu-id="ff256-115">Класс [снмпнотификатион](snmpnotification.md) является родительским классом для иерархии СиП; класс [снмпекстендеднотификатион](snmpextendednotification.md) является родительским классом для иерархии среп.</span><span class="sxs-lookup"><span data-stu-id="ff256-115">The [SNMPNotification](snmpnotification.md) class is the parent class for the SEEP hierarchy; the [SNMPExtendedNotification](snmpextendednotification.md) class is the parent class for the SREP hierarchy.</span></span>

 

 




---
title: Модель WinSNMP
description: В основе WinSNMP-совместимой модели содержатся следующие основные компоненты.
ms.assetid: 491df017-0b91-4fcf-97c3-4e296c3324bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff7ae4fa1c1ee56fc534e4aa4c9bffefb8d7f4d2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067630"
---
# <a name="the-winsnmp-model"></a><span data-ttu-id="e4701-103">Модель WinSNMP</span><span class="sxs-lookup"><span data-stu-id="e4701-103">The WinSNMP Model</span></span>

<span data-ttu-id="e4701-104">В основе WinSNMP-совместимой модели имеются следующие основные компоненты.</span><span class="sxs-lookup"><span data-stu-id="e4701-104">The WinSNMP-compliant model includes the following basic components:</span></span>

-   <span data-ttu-id="e4701-105">Общедоступное приложение для управления сетью SNMP, то есть *приложение* , совместимое с WinSNMP</span><span class="sxs-lookup"><span data-stu-id="e4701-105">A WinSNMP-enabled SNMP network management application, that is, a WinSNMP-compliant *application*</span></span>
-   <span data-ttu-id="e4701-106">Слой функции WinSNMP</span><span class="sxs-lookup"><span data-stu-id="e4701-106">The WinSNMP function layer</span></span>
-   <span data-ttu-id="e4701-107">Поставщик службы SNMP с поддержкой WinSNMP, то есть *Реализация* , совместимая с WinSNMP</span><span class="sxs-lookup"><span data-stu-id="e4701-107">A WinSNMP-enabled SNMP service provider, that is, a WinSNMP-compliant *implementation*</span></span>

<span data-ttu-id="e4701-108">Приложения управления сетью, которые должны передавать SNMP-сообщения, эффективно работают в среде, управляемой событиями.</span><span class="sxs-lookup"><span data-stu-id="e4701-108">Network management applications that must convey SNMP messages operate efficiently in an event-driven environment.</span></span> <span data-ttu-id="e4701-109">Это связано с тем, что SNMP является протоколом на основе датаграмм или без подключения между удаленными сущностями, которые не устанавливают виртуальные цепи.</span><span class="sxs-lookup"><span data-stu-id="e4701-109">This is because SNMP is a datagram-based or connectionless protocol between remote entities that do not establish virtual circuits.</span></span>

<span data-ttu-id="e4701-110">Поскольку приложения Microsoft Windows также управляются событиями, в базе данных WinSNMP используется модель программирования, в которой получение и обработка асинхронных событий управления дисками *сообщений о событиях* .</span><span class="sxs-lookup"><span data-stu-id="e4701-110">Since Microsoft Windows applications are also event-driven, WinSNMP uses a programming model in which the receipt and processing of asynchronous *message-events* drive management applications.</span></span> <span data-ttu-id="e4701-111">Асинхронное событие сообщения может быть запросом операции SNMP приложением диспетчера или ответом на запрос, выполняемым приложением агента.</span><span class="sxs-lookup"><span data-stu-id="e4701-111">An asynchronous message-event can be an SNMP operation request by a manager application, or the response to a request by an agent application.</span></span>

<span data-ttu-id="e4701-112">SNMP отправляет запросы и ответы в виде SNMP-сообщений.</span><span class="sxs-lookup"><span data-stu-id="e4701-112">SNMP sends requests and responses as SNMP messages.</span></span> <span data-ttu-id="e4701-113">SNMP-сообщение — это единица данных протокола SNMP (PDU), а также дополнительные элементы заголовка сообщения, определенные соответствующим RFC.</span><span class="sxs-lookup"><span data-stu-id="e4701-113">An SNMP message is an SNMP protocol data unit (PDU) plus additional message header elements defined by the relevant RFC.</span></span> <span data-ttu-id="e4701-114">Дополнительные сведения см. в статьях [об SNMP-сообщениях](about-snmp-messages.md), [работе со списками привязок переменных](working-with-variable-binding-lists.md) и [работе с единицами данных протокола](working-with-protocol-data-units.md).</span><span class="sxs-lookup"><span data-stu-id="e4701-114">For more information, see [About SNMP Messages](about-snmp-messages.md), [Working with Variable Binding Lists](working-with-variable-binding-lists.md) and [Working with Protocol Data Units](working-with-protocol-data-units.md).</span></span>

 

 





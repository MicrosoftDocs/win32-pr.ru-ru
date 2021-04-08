---
title: Форматы ловушек
description: Формат PDU ловушки отличается от формата других устройств PDU. Формат ловушек и ловушек SNMPv2C не отличается.
ms.assetid: 2d2b4520-28b7-4a2e-8dee-456e17d9d6f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e87adc3222808fcc7e81904ade07c09afa13bc6d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067629"
---
# <a name="trap-formats"></a><span data-ttu-id="c53cc-104">Форматы ловушек</span><span class="sxs-lookup"><span data-stu-id="c53cc-104">Trap Formats</span></span>

<span data-ttu-id="c53cc-105">Формат PDU ловушки отличается от формата других устройств PDU.</span><span class="sxs-lookup"><span data-stu-id="c53cc-105">The format of trap PDUs is different than that of other PDUs.</span></span> <span data-ttu-id="c53cc-106">Формат ловушек и ловушек SNMPv2C не отличается.</span><span class="sxs-lookup"><span data-stu-id="c53cc-106">The format of SNMPv1 traps and SNMPv2C traps is also different.</span></span>

<span data-ttu-id="c53cc-107">В SNMPv2C Framework формат ловушки PDU представляет собой список привязок переменных для *n* записей привязки переменных, организованных следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c53cc-107">Under the SNMPv2C framework, the PDU trap format is a variable binding list of *n* variable binding entries organized in the following manner:</span></span>

-   <span data-ttu-id="c53cc-108">Первая запись привязки переменной содержит метку времени.</span><span class="sxs-lookup"><span data-stu-id="c53cc-108">The first variable binding entry contains a time-stamp.</span></span>
-   <span data-ttu-id="c53cc-109">Вторая запись привязки переменной — это идентификатор объекта, определяющий ловушку.</span><span class="sxs-lookup"><span data-stu-id="c53cc-109">The second variable binding entry is an object identifier that identifies the trap.</span></span>
-   <span data-ttu-id="c53cc-110">Третья — *n* записей привязки переменных, если они есть, содержат дополнительные сведения, связанные с ловушкой.</span><span class="sxs-lookup"><span data-stu-id="c53cc-110">The third through *n* variable binding entries, if present, contain additional information associated with the trap.</span></span>

<span data-ttu-id="c53cc-111">В среде с кодом версии не ниже, используется следующий формат ловушек PDU.</span><span class="sxs-lookup"><span data-stu-id="c53cc-111">Under the SNMPv1 framework, the PDU trap format is as follows.</span></span>

| <span data-ttu-id="c53cc-112">Поле</span><span class="sxs-lookup"><span data-stu-id="c53cc-112">Field</span></span>                      | <span data-ttu-id="c53cc-113">Описание</span><span class="sxs-lookup"><span data-stu-id="c53cc-113">Description</span></span>                                                      |
|----------------------------|------------------------------------------------------------------|
| <span data-ttu-id="c53cc-114">корпоративные</span><span class="sxs-lookup"><span data-stu-id="c53cc-114">enterprise</span></span>                 | <span data-ttu-id="c53cc-115">Определяет тип устройства, создавшего ловушку.</span><span class="sxs-lookup"><span data-stu-id="c53cc-115">Identifies the type of device that generated the trap.</span></span>           |
| <span data-ttu-id="c53cc-116">"Агент-адрес"</span><span class="sxs-lookup"><span data-stu-id="c53cc-116">agent-addr</span></span>                 | <span data-ttu-id="c53cc-117">Определяет IP-адрес устройства, создавшего ловушку.</span><span class="sxs-lookup"><span data-stu-id="c53cc-117">Identifies the IP address of the device that generated the trap.</span></span> |
| <span data-ttu-id="c53cc-118">универсальный — ловушка/особая ловушка</span><span class="sxs-lookup"><span data-stu-id="c53cc-118">generic-trap/specific-trap</span></span> | <span data-ttu-id="c53cc-119">Определяет предопределенный тип ловушки.</span><span class="sxs-lookup"><span data-stu-id="c53cc-119">Identifies a predefined trap type.</span></span>                               |
| <span data-ttu-id="c53cc-120">Временная метка</span><span class="sxs-lookup"><span data-stu-id="c53cc-120">time-stamp</span></span>                 | <span data-ttu-id="c53cc-121">Определяет, когда была создана ловушка.</span><span class="sxs-lookup"><span data-stu-id="c53cc-121">Identifies when the trap was generated.</span></span>                          |
| <span data-ttu-id="c53cc-122">переменные привязки</span><span class="sxs-lookup"><span data-stu-id="c53cc-122">variable-bindings</span></span>          | <span data-ttu-id="c53cc-123">Содержит дополнительные сведения, связанные с ловушкой.</span><span class="sxs-lookup"><span data-stu-id="c53cc-123">Contains additional information associated with the trap.</span></span>        |



 

<span data-ttu-id="c53cc-124">Функция [**снмпреквмсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) всегда возвращает сообщение в формате SNMPv2c.</span><span class="sxs-lookup"><span data-stu-id="c53cc-124">The [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) function always returns a message in the SNMPv2C format.</span></span> <span data-ttu-id="c53cc-125">Если сообщение содержит тип операции **\_ \_ ловушка PDU SNMP**, приложение может считывать записи привязки переменных сообщения и получать сведения, связанные с этой ловушкой.</span><span class="sxs-lookup"><span data-stu-id="c53cc-125">If the message contains the operation type **SNMP\_PDU\_TRAP**, the application can read the variable binding entries of the message and retrieve the information associated with the trap.</span></span>

 

 





---
title: Дублирование PDU
description: Функция Снмпдупликатепду дублирует PDU, выделяя любой необходимый объем памяти. Чтобы освободить ресурсы, выделенные Снмпдупликатепду для нового PDU, приложение WinSNMP должно вызывать функцию Снмпфрипду.
ms.assetid: 371e566b-0577-4089-b081-17085c9587fd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acd860d84ac102f2c2cdd1132476b3279e640f9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777273"
---
# <a name="duplicating-a-pdu"></a><span data-ttu-id="bee7e-104">Дублирование PDU</span><span class="sxs-lookup"><span data-stu-id="bee7e-104">Duplicating a PDU</span></span>

<span data-ttu-id="bee7e-105">Функция [**снмпдупликатепду**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu) дублирует PDU, выделяя любой необходимый объем памяти.</span><span class="sxs-lookup"><span data-stu-id="bee7e-105">The [**SnmpDuplicatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu) function duplicates a PDU, allocating any necessary memory.</span></span> <span data-ttu-id="bee7e-106">Чтобы освободить ресурсы, выделенные **снмпдупликатепду** для нового PDU, приложение WinSNMP должно вызывать функцию [**снмпфрипду**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu) .</span><span class="sxs-lookup"><span data-stu-id="bee7e-106">To release resources allocated by **SnmpDuplicatePdu** for a new PDU, a WinSNMP application must call the [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu) function.</span></span>

 

 





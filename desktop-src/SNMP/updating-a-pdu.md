---
title: Обновление PDU
description: Приложение WinSNMP может извлекать и обновлять выбранные поля PDU с помощью функций Снмпжетпдудата и Снмпсетпдудата.
ms.assetid: 001f5252-aa54-490b-8ff0-39a7780baff8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 678f980882b350669321cf676f9bc69af4369de8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778872"
---
# <a name="updating-a-pdu"></a><span data-ttu-id="52d0c-103">Обновление PDU</span><span class="sxs-lookup"><span data-stu-id="52d0c-103">Updating a PDU</span></span>

<span data-ttu-id="52d0c-104">Приложение WinSNMP может извлекать и обновлять выбранные поля PDU с помощью функций [**снмпжетпдудата**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) и [**снмпсетпдудата**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) .</span><span class="sxs-lookup"><span data-stu-id="52d0c-104">A WinSNMP application can retrieve and update selected PDU fields by using the [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) and the [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) functions.</span></span>

<span data-ttu-id="52d0c-105">Приложение может получить поля типа PDU, идентификатора запроса, состояния ошибки и индекса ошибок из определенного PDU.</span><span class="sxs-lookup"><span data-stu-id="52d0c-105">The application can retrieve the PDU type, request identifier, error status, and error index fields from a specific PDU.</span></span> <span data-ttu-id="52d0c-106">Он также может получить маркер для списка привязок переменных.</span><span class="sxs-lookup"><span data-stu-id="52d0c-106">It can also retrieve the handle to the variable binding list.</span></span> <span data-ttu-id="52d0c-107">Приложение может обновлять поля **\_ типа PDU** и **\_ идентификатора запроса** .</span><span class="sxs-lookup"><span data-stu-id="52d0c-107">The application can update the **PDU\_type** and **request\_id** fields.</span></span>

<span data-ttu-id="52d0c-108">Если тип PDU равен числу PDU SNMP \_ \_ , то приложение также может обновлять **\_ неповторяющиеся** значения и поля **максимального числа \_ повторений** PDU.</span><span class="sxs-lookup"><span data-stu-id="52d0c-108">If the PDU type is equal to SNMP\_PDU\_GETBULK, the application can also update the **non\_repeaters** and the **max\_repetitions** fields of the PDU.</span></span>

 

 





---
title: Как работает SNMP
description: Как стороннее консоль управления SNMP возвращает сведения из службы SNMP.
ms.assetid: 2edbf9ff-b9e3-4103-affc-a5c0f22b80a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39d58943f0765b60f9c235094642d3fa759402db
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986335"
---
# <a name="how-snmp-works"></a><span data-ttu-id="ad5c5-103">Как работает SNMP</span><span class="sxs-lookup"><span data-stu-id="ad5c5-103">How SNMP Works</span></span>

<span data-ttu-id="ad5c5-104">Ниже показано, как приложение консоли управления SNMP от стороннего производителя Возвращает сведения из службы SNMP:</span><span class="sxs-lookup"><span data-stu-id="ad5c5-104">The following steps outline how a third-party SNMP management console application returns information from the SNMP service:</span></span>

1.  <span data-ttu-id="ad5c5-105">Консольное приложение управления SNMP формирует SNMP-сообщение на основе входных данных пользователя.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-105">The SNMP management console application formulates an SNMP message based on input from the user.</span></span> <span data-ttu-id="ad5c5-106">Сообщение включает блок данных протокола (PDU) и сведения о проверке подлинности.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-106">The message includes a protocol data unit (PDU) and authentication information.</span></span> <span data-ttu-id="ad5c5-107">Для выполнения этого шага приложение консоли управления может использовать библиотеку API управления Microsoft SNMP (MGMTAPI.DLL) или библиотеку Microsoft [WINSNMP API](winsnmp-api.md) (WSNMP32.DLL).</span><span class="sxs-lookup"><span data-stu-id="ad5c5-107">The management console application can use the Microsoft SNMP Management API library (MGMTAPI.DLL) or the Microsoft [WinSNMP API](winsnmp-api.md) library (WSNMP32.DLL) to perform this step.</span></span>
2.  <span data-ttu-id="ad5c5-108">Консольное приложение управления SNMP отправляет SNMP-сообщение службе SNMP, используя библиотеки службы SNMP.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-108">The SNMP management console application sends the SNMP message to the SNMP service, using the SNMP service libraries.</span></span>
3.  <span data-ttu-id="ad5c5-109">Служба SNMP получает запрос.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-109">The SNMP service receives the request.</span></span> <span data-ttu-id="ad5c5-110">Он проверяет данные проверки подлинности и исходный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-110">It verifies the authentication information and the source IP address.</span></span>
4.  <span data-ttu-id="ad5c5-111">Служба SNMP выбирает соответствующий агент расширения и запрашивает получение агентом запрошенной информации.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-111">The SNMP service selects the appropriate extension agent and requests that the agent retrieve the requested information.</span></span>
5.  <span data-ttu-id="ad5c5-112">Служба SNMP отправляет ответ в консольное приложение управления SNMP.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-112">The SNMP service sends the response to the SNMP management console application.</span></span>

 

 





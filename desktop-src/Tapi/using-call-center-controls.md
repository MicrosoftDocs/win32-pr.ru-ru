---
description: Элементы управления центра обработки вызовов расширяют модель объектов TAPI 3 для поддержки требований к системам автоматического распределения вызовов (ACD).
ms.assetid: cb7a4231-6249-4ab9-9de7-243768a18775
title: Использование элементов управления центра обработки вызовов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdc01cac4b068c5ec17ff5794e2e7ffff46dbf95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683030"
---
# <a name="using-call-center-controls"></a><span data-ttu-id="4eb82-103">Использование элементов управления центра обработки вызовов</span><span class="sxs-lookup"><span data-stu-id="4eb82-103">Using Call Center Controls</span></span>

<span data-ttu-id="4eb82-104">Элементы управления центра обработки вызовов расширяют модель объектов TAPI 3 для поддержки требований к системам автоматического распределения вызовов (ACD).</span><span class="sxs-lookup"><span data-stu-id="4eb82-104">Call center controls extend the TAPI 3 object model to support the requirements of Automatic Call Distribution (ACD) systems.</span></span> <span data-ttu-id="4eb82-105">Центр обработки звонков — это расположение с агентами или операторами в банках телефонных звонков, которые осуществляют исходящие телефонные звонки или Филдинг входящие.</span><span class="sxs-lookup"><span data-stu-id="4eb82-105">A call center is a location with agents or operators at banks of telephones either making outgoing telephone calls or fielding incoming ones.</span></span> <span data-ttu-id="4eb82-106">Например, компания банка или кредитной карты будет использовать центр обработки звонков, чтобы обрабатывать запросы к учетным записям.</span><span class="sxs-lookup"><span data-stu-id="4eb82-106">For example, a bank or credit card company will use a call center to process account inquiries.</span></span>

<span data-ttu-id="4eb82-107">Приложения центра обработки вызовов делятся на три основных типа:</span><span class="sxs-lookup"><span data-stu-id="4eb82-107">Call center applications are divided into three basic types:</span></span>

-   <span data-ttu-id="4eb82-108">[ACD-прокси](acd-proxy.md): обрабатывает входящие или исходящие сеансы на сервере, что может быть любым из частных коммутаторов телефона на шлюзе Интернета.</span><span class="sxs-lookup"><span data-stu-id="4eb82-108">[ACD Proxy](acd-proxy.md): Handles incoming or outgoing sessions at the server, which can be anything from a proprietary telephone switch to an Internet gateway.</span></span>
-   <span data-ttu-id="4eb82-109">[Клиент агента ACD](acd-agent-client.md): службы — отдельный агент, принимающий или выполняющий вызовы.</span><span class="sxs-lookup"><span data-stu-id="4eb82-109">[ACD Agent Client](acd-agent-client.md): Services an individual agent who is receiving or making calls.</span></span>
-   <span data-ttu-id="4eb82-110">Клиент ACD супервизора: предоставляет общее представление об операциях агента и ACD.</span><span class="sxs-lookup"><span data-stu-id="4eb82-110">ACD Supervisor Client: Provides an overall view of agent and ACD operations.</span></span>

> [!Note]  
> <span data-ttu-id="4eb82-111">Для Windows 2000 функциональность прокси-сервера доступна с помощью TAPI 2,2, а функции супервизора не реализуются.</span><span class="sxs-lookup"><span data-stu-id="4eb82-111">For Windows 2000, proxy functionality is available using TAPI 2.2, and supervisor functions are not implemented.</span></span>

 

<span data-ttu-id="4eb82-112">Раздел Samples (примеры) Windows SDK содержит примеры кода ACD в разделе Нетдс \\ TAPI \\ Tapi2 \\ ACD и нетдс \\ TAPI \\ Tapi3 \\ ACD.</span><span class="sxs-lookup"><span data-stu-id="4eb82-112">The samples section of the Windows SDK contains ACD code samples under Netds\\Tapi\\Tapi2\\Acd and Netds\\Tapi\\Tapi3\\Acd.</span></span>

 

 




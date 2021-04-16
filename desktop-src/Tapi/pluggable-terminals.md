---
description: Подключаемые терминалы позволяют приложению создавать терминалы во время выполнения.
ms.assetid: 34ba4f3c-0a14-4705-9490-817c70700746
title: Подключаемые терминалы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52802d98d7eb6985dbb7de9ca3facab90a5550e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684052"
---
# <a name="pluggable-terminals"></a><span data-ttu-id="beb9e-103">Подключаемые терминалы</span><span class="sxs-lookup"><span data-stu-id="beb9e-103">Pluggable Terminals</span></span>

<span data-ttu-id="beb9e-104">Подключаемые терминалы позволяют приложению создавать терминалы во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="beb9e-104">Pluggable terminals allow an application to create terminals during run time.</span></span> <span data-ttu-id="beb9e-105">Обычно терминалы создаются и контролируются парой поставщика услуг телефонии/поставщика услуг мультимедиа (TSP/MSP), и это остается самым универсальным и стабильным способом манипуляций с терминалами.</span><span class="sxs-lookup"><span data-stu-id="beb9e-105">Terminals are normally created and controlled by a telephony service provider/media service provider (TSP/MSP) pair, and this remains the most versatile and stable means of manipulating terminals.</span></span> <span data-ttu-id="beb9e-106">Однако некоторые приложения должны использовать простые терминалы в ситуациях, когда соответствующая пара TSP/MSP недоступна.</span><span class="sxs-lookup"><span data-stu-id="beb9e-106">However, some applications need to use simple terminals in situations where an appropriate TSP/MSP pair is not available.</span></span> <span data-ttu-id="beb9e-107">Использовать подключаемые терминалы могут только те разработчики приложений, которые хорошо знакомы с операциями TSP/MSP.</span><span class="sxs-lookup"><span data-stu-id="beb9e-107">Only application writers who are thoroughly familiar with TSP/MSP operations should use pluggable terminals.</span></span>

<span data-ttu-id="beb9e-108">В TAPI версии 3,1 подключаемые терминалы добавляются в модель TAPI.</span><span class="sxs-lookup"><span data-stu-id="beb9e-108">In TAPI version 3.1, pluggable terminals are added to the TAPI model.</span></span> <span data-ttu-id="beb9e-109">Подключаемые терминалы позволяют сторонним разработчикам добавлять новый объект терминала, который может использовать любой MSP.</span><span class="sxs-lookup"><span data-stu-id="beb9e-109">Pluggable terminals allow a third party to add a new terminal object that any MSP can use.</span></span>

<span data-ttu-id="beb9e-110">Дополнительные сведения см. в разделе [подключаемый модуль регистрации терминалов](pluggable-terminal-registration.md) и [запись подключаемого терминала](writing-a-pluggable-terminal.md) .</span><span class="sxs-lookup"><span data-stu-id="beb9e-110">See [Pluggable Terminal Registration](pluggable-terminal-registration.md) and [Writing a Pluggable Terminal](writing-a-pluggable-terminal.md) for more information.</span></span>

 

 




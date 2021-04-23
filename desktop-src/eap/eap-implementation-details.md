---
title: Сведения о реализации EAP
description: Точки доступа (ТД), например служба удаленного доступа (RAS), взаимодействуют с реализациями EAP с помощью вызовов функций, которые должны быть экспортированы сторонней библиотекой DLL EAP.
ms.assetid: 85775c03-7538-41a1-9f83-42e71025a79c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41115b16d843b0c1b087eac1c348a0491df1173a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337140"
---
# <a name="eap-implementation-details"></a><span data-ttu-id="eb684-103">Сведения о реализации EAP</span><span class="sxs-lookup"><span data-stu-id="eb684-103">EAP Implementation Details</span></span>

<span data-ttu-id="eb684-104">Точки доступа (ТД), например служба удаленного доступа (RAS), взаимодействуют с реализациями EAP с помощью вызовов функций, которые должны быть экспортированы сторонней библиотекой DLL EAP.</span><span class="sxs-lookup"><span data-stu-id="eb684-104">Access Points (APs), such as Remote Access Service (RAS), interact with EAP implementations through the use of function calls that must be exported by the third-party EAP DLL.</span></span> <span data-ttu-id="eb684-105">Иными словами, протокол EAP является API поставщика, то есть подключаемые модули или библиотеки DLL реализуют код для того, чтобы стать поставщиком EAP, но не должны вызывать сами интерфейсы API EAP.</span><span class="sxs-lookup"><span data-stu-id="eb684-105">In other words, EAP is a provider API, meaning that plug-ins or DLLs implement code to become an EAP provider, but must not call the EAP APIs themselves.</span></span> <span data-ttu-id="eb684-106">Например, программист библиотеки DLL EAP создает код для подпрограммы инициализации EAP и размещает этот код в предопределенной функции EAP [**расеапинитиализе**](/previous-versions/windows/desktop/legacy/aa363527(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="eb684-106">For example, a programmer of an EAP DLL creates code for an EAP initialization routine and places this code in the EAP predefined function [**RasEapInitialize**](/previous-versions/windows/desktop/legacy/aa363527(v=vs.85)).</span></span> <span data-ttu-id="eb684-107">Затем во время выполнения диспетчер соединений AP вызывает функцию **расеапинитиализе** , которая содержит код, для инициализации реализации EAP.</span><span class="sxs-lookup"><span data-stu-id="eb684-107">Then at run-time, the AP connection manager calls the **RasEapInitialize** function, which contains the code, to initialize the EAP implementation.</span></span>

<span data-ttu-id="eb684-108">В следующих разделах подробно описывается это взаимодействие:</span><span class="sxs-lookup"><span data-stu-id="eb684-108">The following topics detail this interaction:</span></span>

-   [<span data-ttu-id="eb684-109">Инициализация точки доступа EAP</span><span class="sxs-lookup"><span data-stu-id="eb684-109">Access Point Initialization of EAP</span></span>](ras-initialization-of-eap.md)
-   [<span data-ttu-id="eb684-110">Инициализация протокола проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="eb684-110">Authentication Protocol Initialization</span></span>](authentication-protocol-initialization.md)
-   [<span data-ttu-id="eb684-111">Взаимодействие с точкой доступа и протоколом проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="eb684-111">Access Point and Authentication Protocol Interaction</span></span>](ras-and-authentication-protocol-interaction-during-authentication.md)
-   [<span data-ttu-id="eb684-112">Завершение сеанса проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="eb684-112">Completion of the Authentication Session</span></span>](completion-of-the-authentication-session.md)

 

 
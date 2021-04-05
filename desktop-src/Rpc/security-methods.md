---
title: Методы безопасности
description: Microsoft RPC поддерживает два разных способа добавления безопасности в распределенное приложение.
ms.assetid: 10dd8e71-668a-46bf-ab5d-e4b1e0e56a46
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 367c4d052301ac1100d84cf18dc63e1540ed34b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068427"
---
# <a name="security-methods"></a><span data-ttu-id="dd388-103">Методы безопасности</span><span class="sxs-lookup"><span data-stu-id="dd388-103">Security Methods</span></span>

<span data-ttu-id="dd388-104">Microsoft RPC поддерживает два разных способа добавления безопасности в распределенное приложение.</span><span class="sxs-lookup"><span data-stu-id="dd388-104">Microsoft RPC supports two different methods for adding security to your distributed application.</span></span> <span data-ttu-id="dd388-105">Первый способ — использовать интерфейс поставщика поддержки безопасности (SSPI), доступ к которому можно получить с помощью функций RPC.</span><span class="sxs-lookup"><span data-stu-id="dd388-105">The first method is to use the Security Support Provider Interface (SSPI), which can be accessed using the RPC functions.</span></span> <span data-ttu-id="dd388-106">Как правило, этот метод лучше использовать.</span><span class="sxs-lookup"><span data-stu-id="dd388-106">In general, it is best to use this method.</span></span> <span data-ttu-id="dd388-107">SSPI предоставляет наиболее гибкие и независимые от сети функции проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="dd388-107">The SSPI provides the most flexible and network-independent authentication features.</span></span>

<span data-ttu-id="dd388-108">Второй способ заключается в использовании функций безопасности, встроенных в транспортные протоколы системы.</span><span class="sxs-lookup"><span data-stu-id="dd388-108">The second method is to use the security features built into the system transport protocols.</span></span> <span data-ttu-id="dd388-109">Метод безопасности на транспортном уровне не является предпочтительным методом.</span><span class="sxs-lookup"><span data-stu-id="dd388-109">The transport-level security method is not the preferred method.</span></span> <span data-ttu-id="dd388-110">Рекомендуется использовать SSPI, так как он работает на всех транспортировках, на разных платформах и обеспечивает высокий уровень безопасности, включая конфиденциальность.</span><span class="sxs-lookup"><span data-stu-id="dd388-110">Using the SSPI is recommended because it works on all transports, across platforms, and provides high levels of security, including privacy.</span></span>

<span data-ttu-id="dd388-111">В этом разделе приведены обзоры безопасности на уровне SSPI и транспорта в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="dd388-111">This section provides overviews of both SSPI and transport-level security in the following topics:</span></span>

-   [<span data-ttu-id="dd388-112">интерфейс поставщика поддержки безопасности (SSPI)</span><span class="sxs-lookup"><span data-stu-id="dd388-112">Security Support Provider Interface (SSPI)</span></span>](security-support-provider-interface-sspi-.md)
-   [<span data-ttu-id="dd388-113">Безопасность транспорта</span><span class="sxs-lookup"><span data-stu-id="dd388-113">Transport Security</span></span>](transport-security.md)

 

 





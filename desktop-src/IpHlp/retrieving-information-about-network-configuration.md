---
description: Вспомогательная служба IP предоставляет сведения о конфигурации сети локального компьютера.
ms.assetid: 6135dca5-00c8-4ed4-bb89-7c99abeb7c7c
title: Получение сведений о конфигурации сети
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64a6860b329ba7c69575be1dfeaaa2e19c57558f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999405"
---
# <a name="retrieving-information-about-network-configuration"></a><span data-ttu-id="ab50a-103">Получение сведений о конфигурации сети</span><span class="sxs-lookup"><span data-stu-id="ab50a-103">Retrieving Information About Network Configuration</span></span>

<span data-ttu-id="ab50a-104">Вспомогательная служба IP предоставляет сведения о конфигурации сети локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="ab50a-104">IP Helper provides information about the network configuration of the local computer.</span></span> <span data-ttu-id="ab50a-105">Чтобы получить общие сведения о конфигурации, используйте функцию [**жетнетворкпарамс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) .</span><span class="sxs-lookup"><span data-stu-id="ab50a-105">To retrieve general configuration information, use the [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) function.</span></span> <span data-ttu-id="ab50a-106">Эта функция возвращает сведения, не относящиеся к конкретному адаптеру или интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="ab50a-106">This function returns information that is not specific to a particular adapter or interface.</span></span> <span data-ttu-id="ab50a-107">Например, **жетнетворкпарамс** возвращает список DNS-серверов, используемых локальным компьютером.</span><span class="sxs-lookup"><span data-stu-id="ab50a-107">For example, **GetNetworkParams** returns a list of the DNS servers that are used by the local computer.</span></span>

-   <span data-ttu-id="ab50a-108">Примеры кода, включающие [**жетнетворкпарамс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) , см. [в разделе Получение сведений с помощью жетнетворкпарамс](retrieving-information-using-getnetworkparams.md).</span><span class="sxs-lookup"><span data-stu-id="ab50a-108">For code samples involving [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) see [Retrieving Information Using GetNetworkParams](retrieving-information-using-getnetworkparams.md).</span></span>

 

 




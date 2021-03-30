---
title: Client Security во время асинхронного вызова
description: Client Security во время асинхронного вызова
ms.assetid: 26d1f2c2-cb08-49f1-8beb-b99b029f0d8c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bea2f83bf6341704dd0265a37ec2f64b79e9b2a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778473"
---
# <a name="client-security-during-an-asynchronous-call"></a><span data-ttu-id="87ae5-103">Client Security во время асинхронного вызова</span><span class="sxs-lookup"><span data-stu-id="87ae5-103">Client Security During an Asynchronous Call</span></span>

<span data-ttu-id="87ae5-104">Диспетчер прокси-сервера, созданный MIDL для объектов, использующих стандартный маршалирование, реализует интерфейс [**иклиентсекурити**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) .</span><span class="sxs-lookup"><span data-stu-id="87ae5-104">The proxy manager created by MIDL for objects that use standard marshaling implements the [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) interface.</span></span> <span data-ttu-id="87ae5-105">Клиенты могут управлять безопасностью упакованных вызовов, запрашивая **иклиентсекурити** на объекте Call и получая или изменяя параметры безопасности.</span><span class="sxs-lookup"><span data-stu-id="87ae5-105">Clients can manage the security of marshaled calls by querying for **IClientSecurity** on the call object and obtaining or changing security settings.</span></span>

## <a name="related-topics"></a><span data-ttu-id="87ae5-106">См. также</span><span class="sxs-lookup"><span data-stu-id="87ae5-106">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87ae5-107">Выполнение асинхронного вызова</span><span class="sxs-lookup"><span data-stu-id="87ae5-107">Making an Asynchronous Call</span></span>](making-an-asynchronous-call.md)
</dt> </dl>

 

 





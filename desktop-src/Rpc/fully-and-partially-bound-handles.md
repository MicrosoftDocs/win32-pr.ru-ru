---
title: Полностью и частично привязанные дескрипторы
description: При использовании динамических конечных точек библиотеки времени выполнения получают сведения о конечной точке по мере необходимости.
ms.assetid: 13f2f783-2c10-4122-ba4d-a97b9c0378c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc1f434ec53ebcfd992b0090ed9066dce2ec627
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486824"
---
# <a name="fully-and-partially-bound-handles"></a><span data-ttu-id="5240c-103">Полностью и частично привязанные дескрипторы</span><span class="sxs-lookup"><span data-stu-id="5240c-103">Fully and Partially Bound Handles</span></span>

<span data-ttu-id="5240c-104">При использовании динамических конечных точек библиотеки времени выполнения получают сведения о конечной точке по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="5240c-104">When you use dynamic endpoints, the run-time libraries obtain endpoint information as they need it.</span></span> <span data-ttu-id="5240c-105">Библиотеки времени выполнения делают различие между *полностью привязанным маркером* (который включает сведения о конечной точке) и *частично привязанным маркером* (который не включает сведения о конечной точке).</span><span class="sxs-lookup"><span data-stu-id="5240c-105">The run-time libraries make the distinction between a *fully bound handle* (one that includes endpoint information) and a *partially bound handle* (one that does not include endpoint information).</span></span>

<span data-ttu-id="5240c-106">Клиентская библиотека времени выполнения должна преобразовать частично привязанный маркер в полностью привязанный, прежде чем клиент сможет выполнить привязку к серверу.</span><span class="sxs-lookup"><span data-stu-id="5240c-106">The client run-time library must convert the partially bound handle to a fully bound handle before the client can bind to the server.</span></span> <span data-ttu-id="5240c-107">Клиентская библиотека времени выполнения пытается преобразовать частично привязанный обработчик для клиентского приложения, получая сведения о конечной точке, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="5240c-107">The client run-time library tries to convert the partially bound handle for the client application by obtaining the endpoint information as shown:</span></span>

-   <span data-ttu-id="5240c-108">Из спецификации интерфейса клиента</span><span class="sxs-lookup"><span data-stu-id="5240c-108">From the client's interface specification</span></span>
-   <span data-ttu-id="5240c-109">Из службы сопоставления конечных точек, работающей на сервере</span><span class="sxs-lookup"><span data-stu-id="5240c-109">From an endpoint-mapping service running on the server</span></span>

<span data-ttu-id="5240c-110">Если клиент пытается использовать частично привязанный обработчик, когда сведения о конечной точке недоступны в спецификации интерфейса и модуль сопоставления конечных точек сервера не имеет сведений о конечной точке сервера, то у клиента не будет достаточно информации для выполнения удаленного вызова процедуры, и вызов завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="5240c-110">If the client tries to use a partially bound handle when the endpoint information is not available in the interface specification and the server's endpoint-mapper does not have information about the server endpoint, the client will not have enough information to make its remote procedure call and that call will fail.</span></span> <span data-ttu-id="5240c-111">Чтобы избежать этого, необходимо зарегистрировать конечную точку в модуле сопоставления конечных точек, если распределенное приложение использует дескрипторы с частичным связыванием.</span><span class="sxs-lookup"><span data-stu-id="5240c-111">To prevent this, you must register the endpoint in the endpoint mapper when your distributed application uses partially bound handles.</span></span> <span data-ttu-id="5240c-112">Дополнительные сведения о сопоставителе конечных точек см. в разделе [Указание динамических конечных узлов](specifying-endpoints.md).</span><span class="sxs-lookup"><span data-stu-id="5240c-112">For more information about the endpoint mapper, see [Specifying Dynamic Endpoints](specifying-endpoints.md).</span></span>

<span data-ttu-id="5240c-113">При сбое удаленного вызова процедуры клиентское приложение может вызвать [**рпкбиндингресет**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset) для удаления устаревшей информации о конечных точках.</span><span class="sxs-lookup"><span data-stu-id="5240c-113">When a remote procedure call fails, the client application can call [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset) to remove out-of-date endpoint information.</span></span> <span data-ttu-id="5240c-114">Когда клиент пытается вызвать удаленную процедуру, Библиотека времени выполнения клиента снова пытается преобразовать полностью привязанный маркер в маркер частичной привязки.</span><span class="sxs-lookup"><span data-stu-id="5240c-114">When the client tries to call the remote procedure, the client run-time library again tries to convert the fully bound handle to a partially bound handle.</span></span> <span data-ttu-id="5240c-115">Это полезно, когда сервер был остановлен и перезапущен с другой динамической конечной точки.</span><span class="sxs-lookup"><span data-stu-id="5240c-115">This is useful when the server has been stopped and restarted using a different dynamic endpoint.</span></span>

 

 





---
title: Отправка рекомендаций
description: Хигхлоадс может вызвать различные условия времени ожидания сервера, которые могут, в свою очередь, увеличить нагрузку при попытке клиента.
ms.assetid: 8210f849-2aae-497b-b5dd-af25f6f4b8bf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b95a229ff1e229c41fde8fd377e347f91cf43010
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067421"
---
# <a name="upload-best-practices"></a><span data-ttu-id="69a00-103">Отправка рекомендаций</span><span class="sxs-lookup"><span data-stu-id="69a00-103">Upload Best Practices</span></span>

<span data-ttu-id="69a00-104">Хигхлоадс может вызвать различные условия времени ожидания сервера, которые могут, в свою очередь, увеличить нагрузку при попытке клиента.</span><span class="sxs-lookup"><span data-stu-id="69a00-104">Highloads may cause various server timeout conditions, which may in turn increase the load when the client retries.</span></span> <span data-ttu-id="69a00-105">Кроме того, большое количество необработанных подключений будет потреблять больше ресурсов сервера и усложнить ситуацию.</span><span class="sxs-lookup"><span data-stu-id="69a00-105">Also, a large number of outstanding connections will consume more server resources and make the situation worse.</span></span> <span data-ttu-id="69a00-106">Поверх этого, если серверное приложение не записывается для работы с высокими условиями загрузки, оно может привести к сбою или некорректной работе.</span><span class="sxs-lookup"><span data-stu-id="69a00-106">On top of that, if backend app is not written to handle high load conditions, it may crash or mal-behave.</span></span> <span data-ttu-id="69a00-107">Чтобы ограничить нагрузку на серверную часть, приложение должно выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="69a00-107">The app shall perform the following steps to limit the load on the backend.</span></span>

<span data-ttu-id="69a00-108">Если серверное приложение не записывается для работы с большими объемами томов, могут возникать условия времени ожидания, которые, в свою очередь, увеличивают нагрузку при попытке клиента.</span><span class="sxs-lookup"><span data-stu-id="69a00-108">If the server application is not written to handle high volumes, timeout conditions may occur, which may in turn increase the load when the client retries.</span></span> <span data-ttu-id="69a00-109">Кроме того, большое количество необработанных подключений будет потреблять больше ресурсов сервера.</span><span class="sxs-lookup"><span data-stu-id="69a00-109">Also, a large number of outstanding connections will consume more server resources.</span></span>

<span data-ttu-id="69a00-110">При тестировании серверного приложения протестируйте максимально возможную нагрузку.</span><span class="sxs-lookup"><span data-stu-id="69a00-110">When testing your server application, test with highest load possible.</span></span> <span data-ttu-id="69a00-111">Следует использовать несколько клиентских компьютеров, каждый из которых имеет несколько параллельных заданий битов и измеряет максимальную пропускную способность в серверной части.</span><span class="sxs-lookup"><span data-stu-id="69a00-111">You should use multiple client machines, each with several concurrent, foreground BITS jobs, and measure the maximum throughput at the backend.</span></span> <span data-ttu-id="69a00-112">Если вы не можете измерить пропускную способность, вам придется оценить пропускную способность.</span><span class="sxs-lookup"><span data-stu-id="69a00-112">If you cannot measure the throughput, you will have to estimate the throughput.</span></span>

<span data-ttu-id="69a00-113">Серверное приложение должно располагаться на другом URL-адресе для отправки URL (см. свойство BITS IIS, **битссервернотификатионурл**).</span><span class="sxs-lookup"><span data-stu-id="69a00-113">The server application should reside on a different URL from the upload URL (see the BITS IIS property, **BITSServerNotificationURL**).</span></span>

<span data-ttu-id="69a00-114">Рекомендуется ограничить нагрузку на сервер приложений на основе проверенных значений пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="69a00-114">It is good practice to limit the load on the application server based on proven throughput values.</span></span> <span data-ttu-id="69a00-115">Для ограничения нагрузки на сервер приложений следует использовать свойства IIS **MaxBandwidth** и **MaxConnections**.</span><span class="sxs-lookup"><span data-stu-id="69a00-115">You should use the IIS properties, **MaxBandwidth** and **MaxConnections**, to limit the load on the application server.</span></span>

 

 





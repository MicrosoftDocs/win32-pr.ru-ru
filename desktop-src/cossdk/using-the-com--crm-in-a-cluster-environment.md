---
description: Использование COM+ CRM в среде кластера
ms.assetid: 753461c5-880c-4df0-b552-b962dc06524f
title: Использование COM+ CRM в среде кластера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14a05ff281748c35128349ef5d0d0f43d7beae86
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342242"
---
# <a name="using-the-com-crm-in-a-cluster-environment"></a><span data-ttu-id="d7879-103">Использование COM+ CRM в среде кластера</span><span class="sxs-lookup"><span data-stu-id="d7879-103">Using the COM+ CRM in a Cluster Environment</span></span>

<span data-ttu-id="d7879-104">При разработке Крмс COM+ для работы в средах кластера основным фактором, который следует учитывать, является то, что конкретный CRM заботится о том, на каком узле кластера он работает.</span><span class="sxs-lookup"><span data-stu-id="d7879-104">When developing COM+ CRMs to work in cluster environments, the main factor to consider is whether a specific CRM cares which node of the cluster it is operating on.</span></span> <span data-ttu-id="d7879-105">Например, если ресурсом, управляемым модулем CRM, является файловая система или реестр компьютера, любые изменения относятся к узлу, на котором выполняется приложение сервера CRM.</span><span class="sxs-lookup"><span data-stu-id="d7879-105">For example, if the resource managed by the CRM is the machine file system or registry, any changes are specific to the node that the CRM server application is running on at the time.</span></span> <span data-ttu-id="d7879-106">В этом случае отработка отказа серверного приложения CRM на другой узел не будет желательным.</span><span class="sxs-lookup"><span data-stu-id="d7879-106">In this case, failover of the CRM server application to another node would not be desirable.</span></span> <span data-ttu-id="d7879-107">В другом случае, когда CRM управляет некоторыми общими ресурсами кластера, полезно отработка отказа серверного приложения CRM на другой узел.</span><span class="sxs-lookup"><span data-stu-id="d7879-107">In a different case, where the CRM is managing some resource common to the cluster, failover of the CRM server application to another node is useful.</span></span>

<span data-ttu-id="d7879-108">Расположением каталога по умолчанию для файлов журналов CRM является тот же каталог, что и файл журнала DTC.</span><span class="sxs-lookup"><span data-stu-id="d7879-108">The default directory location for CRM log files is the same directory as the DTC log file.</span></span> <span data-ttu-id="d7879-109">В кластерах файл журнала DTC размещается на общем диске, на котором произошел переход между узлами кластера.</span><span class="sxs-lookup"><span data-stu-id="d7879-109">On clusters, the DTC log file is placed on a shared disk that is failed over between the nodes of the cluster.</span></span> <span data-ttu-id="d7879-110">Это означает, что поведение по умолчанию для серверных приложений CRM заключается в отработке отказа между узлами кластера.</span><span class="sxs-lookup"><span data-stu-id="d7879-110">This means that the default behavior for CRM server applications is to failover between nodes of the cluster.</span></span> <span data-ttu-id="d7879-111">Таким образом, если конкретному CRM требуется альтернативное поведение отказа между узлами, необходимо изменить расположение файла журнала CRM для этого конкретного серверного приложения CRM.</span><span class="sxs-lookup"><span data-stu-id="d7879-111">Therefore, if a specific CRM requires the alternative behavior of not failing over between nodes, the location of the CRM log file for that particular CRM server application should be changed.</span></span>

<span data-ttu-id="d7879-112">Кроме того, если для приложения CRM требуется отработка отказа, его следует настроить как универсальное приложение в группе кластера.</span><span class="sxs-lookup"><span data-stu-id="d7879-112">In addition, if failover is required for the CRM application, it should be configured as a generic application in a cluster group.</span></span> <span data-ttu-id="d7879-113">Его зависимость должна быть DTC.</span><span class="sxs-lookup"><span data-stu-id="d7879-113">Its dependency should be DTC.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d7879-114">См. также</span><span class="sxs-lookup"><span data-stu-id="d7879-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7879-115">Основные понятия о компенсации диспетчер ресурсов COM+</span><span class="sxs-lookup"><span data-stu-id="d7879-115">COM+ Compensating Resource Manager Concepts</span></span>](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 




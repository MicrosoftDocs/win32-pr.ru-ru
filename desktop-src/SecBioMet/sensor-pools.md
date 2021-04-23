---
title: Пулы датчиков
description: Описание трех возможных пулов датчиков, частных и неназначенных.
ms.assetid: d7fd3c39-d719-4cfd-9af0-a87837f3f328
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 263275af5c7decff37ef70ad3a5396ec562562f4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413198"
---
# <a name="sensor-pools"></a><span data-ttu-id="69502-103">Пулы датчиков</span><span class="sxs-lookup"><span data-stu-id="69502-103">Sensor Pools</span></span>

<span data-ttu-id="69502-104">Для поддержки сценариев проверки подлинности Windows и проверки подлинности, определенных поставщиком, биометрическая служба Windows организует биометрические единицы на три возможных пула датчиков:</span><span class="sxs-lookup"><span data-stu-id="69502-104">To support both Windows authentication scenarios and vendor defined authentication, the Windows Biometric service organizes biometric units into three possible sensor pools:</span></span>

-   <span data-ttu-id="69502-105">**Частный пул** коллекция биометрических модулей, выделенная для монопольного использования клиентским приложением.</span><span class="sxs-lookup"><span data-stu-id="69502-105">**Private pool** a collection of biometric units allocated for exclusive use by a client application.</span></span> <span data-ttu-id="69502-106">Частные пулы могут поддерживать сценарии проверки подлинности, не основанные на Windows, и позволяют приложению получать доступ к оборудованию биометрического модуля в определенном поставщиком виде.</span><span class="sxs-lookup"><span data-stu-id="69502-106">Private pools can support authentication scenarios that are not Windows-based, and they make it possible for an application to access the hardware of a biometric unit in a vendor-defined fashion.</span></span> <span data-ttu-id="69502-107">В системе может быть столько частных пулов датчиков, сколько есть биометрические единицы.</span><span class="sxs-lookup"><span data-stu-id="69502-107">There can be as many private sensor pools on the system as there are biometric units.</span></span>
-   <span data-ttu-id="69502-108">**Пул датчиков системы** коллекция биометрических единиц, которые предоставляют доступ к службам проверки подлинности Windows.</span><span class="sxs-lookup"><span data-stu-id="69502-108">**System sensor pool** a collection of sharable biometric units that provide access to Windows authentication services.</span></span> <span data-ttu-id="69502-109">Этот пул используется Winlogon, UAC и любым другим клиентом, связывающим идентификатор безопасности с конкретным биометрической шаблоном.</span><span class="sxs-lookup"><span data-stu-id="69502-109">This pool is used by Winlogon, UAC, and any other client that associates a SID with a specific biometric template.</span></span> <span data-ttu-id="69502-110">Каждый поставщик биометрической службы имеет один пул датчиков системы.</span><span class="sxs-lookup"><span data-stu-id="69502-110">Each biometric service provider has one system sensor pool.</span></span>
-   <span data-ttu-id="69502-111">**Неназначенный пул** содержит (возможно, пустую) коллекцию биометрических единиц, которые не назначены системному пулу или частному пулу.</span><span class="sxs-lookup"><span data-stu-id="69502-111">**Unassigned pool** contains a (possibly empty) collection of biometric units that are not assigned to either the system pool or the private pool.</span></span>

<span data-ttu-id="69502-112">Приложения могут использовать общий пул систем, или же они могут создать частный пул, соличный из системных или неназначенных пулов.</span><span class="sxs-lookup"><span data-stu-id="69502-112">Applications can use the shared system pool or they can create a private pool made up of biometric units removed from the system or unassigned pools.</span></span> <span data-ttu-id="69502-113">Когда приложение освобождает частный пул, биометрические единицы перестраиваются и возвращаются в исходные пулы.</span><span class="sxs-lookup"><span data-stu-id="69502-113">When an application releases its private pool, the biometric units are reconfigured and returned to their original pools.</span></span> <span data-ttu-id="69502-114">Чтобы предотвратить атаки типа "отказ в обслуживании", только привилегированные пользователи могут удалить последний датчик из системного пула.</span><span class="sxs-lookup"><span data-stu-id="69502-114">To prevent denial of service attacks, only privileged users are permitted to remove the last sensor from the system pool.</span></span> <span data-ttu-id="69502-115">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="69502-115">For more information, see the following topics.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="69502-116">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="69502-116">In this section</span></span>



| <span data-ttu-id="69502-117">Раздел</span><span class="sxs-lookup"><span data-stu-id="69502-117">Topic</span></span>                                                       | <span data-ttu-id="69502-118">Описание</span><span class="sxs-lookup"><span data-stu-id="69502-118">Description</span></span>                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="69502-119">Частный пул датчиков</span><span class="sxs-lookup"><span data-stu-id="69502-119">Private Sensor Pool</span></span>](private-sensor-pool.md)<br/>   | <span data-ttu-id="69502-120">Коллекция биометрических блоков, зарезервированных для монопольного использования клиентским приложением.</span><span class="sxs-lookup"><span data-stu-id="69502-120">A collection of biometric units reserved for exclusive use by a client application.</span></span> <span data-ttu-id="69502-121">Частные пулы поддерживают собственные методы проверки подлинности и позволяют клиентскому приложению получать доступ к биометрической единице с помощью определяемых поставщиком команд управления.</span><span class="sxs-lookup"><span data-stu-id="69502-121">Private pools support proprietary authentication methods and enable a client application to access a biometric unit by using vendor-specified control commands.</span></span><br/> |
| [<span data-ttu-id="69502-122">Пул датчиков системы</span><span class="sxs-lookup"><span data-stu-id="69502-122">System Sensor Pool</span></span>](system-sensor-pool.md)<br/>     | <span data-ttu-id="69502-123">Коллекция биометрических единиц, которые предоставляют доступ к службам проверки подлинности Windows.</span><span class="sxs-lookup"><span data-stu-id="69502-123">A collection of sharable biometric units that provide access to Windows authentication services.</span></span> <span data-ttu-id="69502-124">Этот пул используется Winlogon, UAC и любым другим клиентом, связывающим идентификатор безопасности с конкретным биометрической шаблоном.</span><span class="sxs-lookup"><span data-stu-id="69502-124">This pool is used by Winlogon, UAC, and any other client that associates a SID with a specific biometric template.</span></span><br/>                                 |
| [<span data-ttu-id="69502-125">Поведение системного пула</span><span class="sxs-lookup"><span data-stu-id="69502-125">System Pool Behavior</span></span>](system-pool-behavior.md)<br/> | <span data-ttu-id="69502-126">Обсуждение действий, выполняемых системным пулом при отправке уведомлений о событиях, а также в случаях, когда никакие биометрические операции не выполняются.</span><span class="sxs-lookup"><span data-stu-id="69502-126">Discussion about the actions taken by the system pool when event notices are sent and when no biometric operations are pending.</span></span><br/>                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="69502-127">См. также</span><span class="sxs-lookup"><span data-stu-id="69502-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69502-128">Сведения об API биометрическая платформа Windows</span><span class="sxs-lookup"><span data-stu-id="69502-128">About the Windows Biometric Framework API</span></span>](./biometric-service-api-portal.md)
</dt> </dl>

 


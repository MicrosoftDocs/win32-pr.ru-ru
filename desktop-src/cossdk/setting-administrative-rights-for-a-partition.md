---
description: Установка прав администратора для секции
ms.assetid: d38e4a63-9ff9-4acb-bb7e-d6c96644bd32
title: Установка прав администратора для секции
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c421b37dd50fa21ee9cf146749ec00b0c91d98c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807360"
---
# <a name="setting-administrative-rights-for-a-partition"></a><span data-ttu-id="1e070-103">Установка прав администратора для секции</span><span class="sxs-lookup"><span data-stu-id="1e070-103">Setting Administrative Rights for a Partition</span></span>

<span data-ttu-id="1e070-104">Пользователям, которым назначена роль администратора системного приложения COM+, разрешено создавать, изменять и удалять разделы COM+.</span><span class="sxs-lookup"><span data-stu-id="1e070-104">Users assigned the Administrator role of the COM+ System Application are allowed to create, modify, and delete COM+ partitions.</span></span> <span data-ttu-id="1e070-105">В средстве администрирования «службы компонентов» административные роли можно назначать пользователям, развернув папку « **роли** » системного приложения COM+.</span><span class="sxs-lookup"><span data-stu-id="1e070-105">Within the Component Services administrative tool, administrative roles can be assigned to users by expanding the **Roles** folder of the COM+ System Application.</span></span>

<span data-ttu-id="1e070-106">Начиная с Windows Server 2003, функция проверки подлинности для системного приложения COM+ включает значение ЕОАК \_ disable \_ AAA.</span><span class="sxs-lookup"><span data-stu-id="1e070-106">As of Windows Server 2003, the authentication capability for the COM+ System Application includes the value EOAC\_DISABLE\_AAA.</span></span> <span data-ttu-id="1e070-107">Это значение, которое отключает активацию активации на основе активатора (AAA), используется в вызове [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) при запуске системного приложения.</span><span class="sxs-lookup"><span data-stu-id="1e070-107">This value, which disables activate-as-activator (AAA) activations, is used in the [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) call when launching the System Application.</span></span> <span data-ttu-id="1e070-108">Установка функции проверки подлинности в ЕОАК \_ disable \_ AAA позволяет приложению, работающему под привилегированной учетной записью (например, LocalSystem), предотвратить использование удостоверения для запуска ненадежных компонентов.</span><span class="sxs-lookup"><span data-stu-id="1e070-108">Setting the authentication capability to EOAC\_DISABLE\_AAA allows an application that runs under a privileged account (such as LocalSystem) to help prevent its identity from being used to launch untrusted components.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1e070-109">См. также</span><span class="sxs-lookup"><span data-stu-id="1e070-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e070-110">Сбор метрик секции</span><span class="sxs-lookup"><span data-stu-id="1e070-110">Collecting Partition Metrics</span></span>](collecting-partition-metrics.md)
</dt> <dt>

[<span data-ttu-id="1e070-111">Настройка кэша секций</span><span class="sxs-lookup"><span data-stu-id="1e070-111">Configuring the Partition Cache</span></span>](configuring-the-partition-cache.md)
</dt> <dt>

[<span data-ttu-id="1e070-112">Группирование приложений в секции</span><span class="sxs-lookup"><span data-stu-id="1e070-112">Grouping Applications into Partitions</span></span>](grouping-applications-into-partitions.md)
</dt> <dt>

[<span data-ttu-id="1e070-113">Управление локальными секциями</span><span class="sxs-lookup"><span data-stu-id="1e070-113">Managing Local Partitions</span></span>](managing-local-partitions.md)
</dt> <dt>

[<span data-ttu-id="1e070-114">Управление секциями в Active Directory</span><span class="sxs-lookup"><span data-stu-id="1e070-114">Managing Partitions Within Active Directory</span></span>](managing-partitions-within-active-directory.md)
</dt> </dl>

 

 

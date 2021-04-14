---
title: Пользовательский интерфейс предыдущих версий удален для локальных томов
description: Пользовательский интерфейс предыдущих версий удален для локальных томов
ms.assetid: 0BD3D046-EB06-4C9A-952C-306AC99396C6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b25d898be8d079ee713e0fa3e508e552b3cd4009
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "104488405"
---
# <a name="previous-versions-ui-removed-for-local-volumes"></a><span data-ttu-id="795ff-103">Пользовательский интерфейс предыдущих версий удален для локальных томов</span><span class="sxs-lookup"><span data-stu-id="795ff-103">Previous versions UI removed for local volumes</span></span>

## <a name="platform"></a><span data-ttu-id="795ff-104">Платформа</span><span class="sxs-lookup"><span data-stu-id="795ff-104">Platform</span></span>

<span data-ttu-id="795ff-105">**Клиенты** — Windows 8</span><span class="sxs-lookup"><span data-stu-id="795ff-105">**Clients** – Windows 8</span></span> 


## <a name="description"></a><span data-ttu-id="795ff-106">Описание</span><span class="sxs-lookup"><span data-stu-id="795ff-106">Description</span></span>

<span data-ttu-id="795ff-107">Более ранние версии Windows позволяли пользователям восстанавливать предыдущие версии отдельных файлов из "теневых копий" локальных томов.</span><span class="sxs-lookup"><span data-stu-id="795ff-107">Earlier versions of Windows allowed users to restore previous versions of individual files from “shadow copies” of local volumes.</span></span> <span data-ttu-id="795ff-108">Эти теневые копии создаются функцией "предыдущие версии" через службу теневого копирования томов (VSS).</span><span class="sxs-lookup"><span data-stu-id="795ff-108">These shadow copies are created by the “Previous Versions” feature through Volume Shadow Copy service (VSS).</span></span> <span data-ttu-id="795ff-109">В Windows 7 пользователи могли настраивать и планировать теневые копии в пользовательском интерфейсе защиты системы, доступном через свойства системы.</span><span class="sxs-lookup"><span data-stu-id="795ff-109">In Windows 7, users could configure and schedule shadow copies in System Protection UI available through System Properties.</span></span>

<span data-ttu-id="795ff-110">Однако предыдущие версии редко использовались и негативно влияли на общую производительность Windows; в результате функция была удалена.</span><span class="sxs-lookup"><span data-stu-id="795ff-110">However, Previous Versions were rarely used and negatively impacted the overall Windows performance; as a result the feature was removed.</span></span> <span data-ttu-id="795ff-111">В Windows 8 эти функции больше не доступны:</span><span class="sxs-lookup"><span data-stu-id="795ff-111">In Windows 8, these features are no longer available:</span></span>

-   <span data-ttu-id="795ff-112">Возможность просмотра, поиска или восстановления предыдущих версий файлов с помощью пользовательского интерфейса предыдущих версий</span><span class="sxs-lookup"><span data-stu-id="795ff-112">The ability to browse, search or restore previous versions of files through Previous Versions UI</span></span>
-   <span data-ttu-id="795ff-113">Возможность настройки или планирования предыдущих версий файлов с помощью пользовательского интерфейса защиты системы</span><span class="sxs-lookup"><span data-stu-id="795ff-113">The ability to configure or schedule previous versions of files through System Protection UI</span></span>

<span data-ttu-id="795ff-114">Однако пользователи по-прежнему могут использовать вкладку предыдущие версии при доступе к общим папкам на сервере Windows.</span><span class="sxs-lookup"><span data-stu-id="795ff-114">However, users can still use the Previous Versions tab when accessing file shares on a Windows server.</span></span>

## <a name="manifestation"></a><span data-ttu-id="795ff-115">Проявление</span><span class="sxs-lookup"><span data-stu-id="795ff-115">Manifestation</span></span>

<span data-ttu-id="795ff-116">Параметр предыдущие версии больше не доступен для локальных томов в меню свойства проводника Windows.</span><span class="sxs-lookup"><span data-stu-id="795ff-116">The Previous Versions option is no longer available for local volumes in the Windows Explorer Properties menu.</span></span>

## <a name="solution"></a><span data-ttu-id="795ff-117">Решение</span><span class="sxs-lookup"><span data-stu-id="795ff-117">Solution</span></span>

<span data-ttu-id="795ff-118">Разработчики, которым требуется создавать теневые копии локальных томов, по-прежнему могут сделать это путем вызова API-интерфейсов VSS в пользовательском коде.</span><span class="sxs-lookup"><span data-stu-id="795ff-118">Developers who need to create shadow copies of local volumes can still do so by calling VSS APIs in custom code.</span></span>

 

 





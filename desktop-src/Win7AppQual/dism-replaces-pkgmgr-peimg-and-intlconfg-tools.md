---
description: Система обслуживания образов развертывания и управления ими (DISM)
ms.assetid: bbfee966-121b-4b53-9e3e-08a747559da0
title: Система обслуживания образов развертывания и управления ими (DISM)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 234d16233927dca2d5dba296fd33fb64135f691e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088492"
---
# <a name="deployment-image-servicing-and-management-dism"></a><span data-ttu-id="a991d-103">Система обслуживания образов развертывания и управления ими (DISM)</span><span class="sxs-lookup"><span data-stu-id="a991d-103">Deployment Image Servicing and Management (DISM)</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="a991d-104">Затронутые платформы</span><span class="sxs-lookup"><span data-stu-id="a991d-104">Affected Platforms</span></span>

<span data-ttu-id="a991d-105">**Клиенты** — Windows Vista SP1 и более поздние версии \| Windows 7</span><span class="sxs-lookup"><span data-stu-id="a991d-105">**Clients** - Windows Vista SP1 and later \| Windows 7</span></span>  
<span data-ttu-id="a991d-106">**Серверы** — windows Server 2008 RTM и более поздние версии \| Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a991d-106">**Servers** - Windows Server 2008 RTM and later \| Windows Server 2008 R2</span></span>  


## <a name="description"></a><span data-ttu-id="a991d-107">Описание</span><span class="sxs-lookup"><span data-stu-id="a991d-107">Description</span></span>

<span data-ttu-id="a991d-108">Средство обслуживания образов развертывания и управления ими (DISM) заменяет средства pkgmgr, PEImg и Интлконфг, снятые в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a991d-108">The Deployment Image Servicing and Management (DISM) tool replaces the pkgmgr, PEImg, and IntlConfg tools that are being retired in Windows 7.</span></span> <span data-ttu-id="a991d-109">DISM предоставляет единое централизованное средство для выполнения всех функций этих трех инструментов в более эффективном и стандартизированном виде, устраняя при этом источник многих разочарований, которые были опытными пользователями этих средств.</span><span class="sxs-lookup"><span data-stu-id="a991d-109">DISM provides a single centralized tool for performing all of the functions of these three tools in a more efficient and standardized way, eliminating the source of many of the frustrations experienced by current users of these tools.</span></span>

<span data-ttu-id="a991d-110">DISM включает оболочку совместимости для Windows Vista с пакетом обновления 1 (SP1) и более поздних версий, а также Windows Server 2008 RTM и более поздних версий, которая перенаправляет вызовы pkgmgr из устаревших приложений, работающих в Windows 7, в DISM.</span><span class="sxs-lookup"><span data-stu-id="a991d-110">DISM includes a shim for Windows Vista SP1 and later, as well as for Windows Server 2008 RTM and later, that redirects pkgmgr calls from legacy applications running on Windows 7 to DISM.</span></span> <span data-ttu-id="a991d-111">Если приложение работает в одной из поддерживаемых операционных систем, оболочка совместимости направляет вызов Pkgmgr.</span><span class="sxs-lookup"><span data-stu-id="a991d-111">If the application is running on one of the supported operating systems, the shim routes the call to pkgmgr.</span></span> <span data-ttu-id="a991d-112">Для устаревших приложений, вызывающих PEImg или Интлконфг, не существует оболочек совместимости.</span><span class="sxs-lookup"><span data-stu-id="a991d-112">No shims exist for legacy applications that call PEImg or IntlConfg.</span></span>

## <a name="usage"></a><span data-ttu-id="a991d-113">Использование</span><span class="sxs-lookup"><span data-stu-id="a991d-113">Usage</span></span>

<span data-ttu-id="a991d-114">Система DISM прозрачна для конечных пользователей pkgmgr на любой из поддерживаемых платформ.</span><span class="sxs-lookup"><span data-stu-id="a991d-114">DISM is transparent to pkgmgr end users on any of the supported platforms.</span></span> <span data-ttu-id="a991d-115">Однако если приложение вызывает программу PEImg или Интлконфг из Windows 7, вызов завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="a991d-115">However, if an application calls either PEImg or IntlConfg from Windows 7, the call will fail.</span></span>

<span data-ttu-id="a991d-116">Обновите все скрипты, вызывающие pkgmgr, PEImg или Интлконфг, для вызова DISM.</span><span class="sxs-lookup"><span data-stu-id="a991d-116">Update any scripts that call pkgmgr, PEImg, or IntlConfg to call DISM instead.</span></span> <span data-ttu-id="a991d-117">В этом случае важно включить обновление скриптов pkgmgr, так как оболочка совместимости, обеспечивающая обратную совместимость для pkgmgr, будет удалена в будущих версиях операционных систем Windows.</span><span class="sxs-lookup"><span data-stu-id="a991d-117">It is important to include the updating of pkgmgr scripts in this effort, since the shim that provides backward compatibility for pkgmgr will be removed in future versions of the Windows operating systems.</span></span>

<span data-ttu-id="a991d-118">Убедитесь, что вызовы DISM заменили все вызовы pkgmgr, PEImg и Интлконфг, и что операция выполняется успешно.</span><span class="sxs-lookup"><span data-stu-id="a991d-118">Check to ensure that calls to DISM have replaced any calls to pkgmgr, PEImg, and IntlConfg, and that the operation executes successfully.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a991d-119">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="a991d-119">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="a991d-120">[Система обслуживания образов развертывания и управления ими (TechNet)](/previous-versions/windows/it-pro/windows-7/dd744256(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="a991d-120">[Deployment Image Servicing and Management (TechNet)](/previous-versions/windows/it-pro/windows-7/dd744256(v=ws.10))</span></span>
</dt> </dl>

 

 

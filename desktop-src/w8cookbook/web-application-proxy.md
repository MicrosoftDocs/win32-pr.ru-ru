---
title: Прокси-сервер веб-приложения
description: Прокси-сервер веб-приложения
ms.assetid: DE47843C-D58B-4C71-99C2-D54073CBA531
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 220ac5f52a8f5130cdb6fb21649ff302e6693b1b
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "104134699"
---
# <a name="web-application-proxy"></a><span data-ttu-id="40a4c-103">Прокси-сервер веб-приложения</span><span class="sxs-lookup"><span data-stu-id="40a4c-103">Web Application Proxy</span></span>

## <a name="platform"></a><span data-ttu-id="40a4c-104">Платформа</span><span class="sxs-lookup"><span data-stu-id="40a4c-104">Platform</span></span>

<span data-ttu-id="40a4c-105">**Серверы —** Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="40a4c-105">**Servers -** Windows Server 2012 R2</span></span>  






## <a name="description"></a><span data-ttu-id="40a4c-106">Описание</span><span class="sxs-lookup"><span data-stu-id="40a4c-106">Description</span></span>

<span data-ttu-id="40a4c-107">В Windows Server 2012 R2 мы добавили в роль удаленного доступа новую службу, именуемую прокси-службой веб приложения, которая позволяет администраторам публиковать приложения для внешнего доступа.</span><span class="sxs-lookup"><span data-stu-id="40a4c-107">In Windows Server 2012 R2, we added a new service called the Web Application Proxy under the Remote Access role that allows administrators to publish applications for external access.</span></span> <span data-ttu-id="40a4c-108">Эта служба действует как обратный прокси-сервер и как прокси-сервер службы федерации Active Directory (AD FS) (AD FS).</span><span class="sxs-lookup"><span data-stu-id="40a4c-108">This service acts as a reverse proxy and as an Active Directory Federation Services (AD FS) proxy.</span></span> <span data-ttu-id="40a4c-109">Фактически эта служба заменяет службу AD FS proxy, как она была известна в Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="40a4c-109">In fact, this service replaces the AD FS proxy service as it was known in Windows Server 2012.</span></span>

<span data-ttu-id="40a4c-110">С помощью прокси веб-приложения организация может сделать локальные веб-ресурсы доступными для внешнего доступа, одновременно управляя риском этого доступа путем управления политиками проверки подлинности и авторизации на AD FS.</span><span class="sxs-lookup"><span data-stu-id="40a4c-110">With the Web Application Proxy, an organization can make on-premises web resources available for external access while at the same time managing the risk of this access by controlling authentication and authorization policies on the AD FS.</span></span>

## <a name="manifestation"></a><span data-ttu-id="40a4c-111">Проявление</span><span class="sxs-lookup"><span data-stu-id="40a4c-111">Manifestation</span></span>

<span data-ttu-id="40a4c-112">Служба AD FS прокси больше не находится в роли службы федерации Active Directory (AD FS) (AD FS), но была заменена прокси-службой в роли удаленного доступа.</span><span class="sxs-lookup"><span data-stu-id="40a4c-112">The AD FS proxy service is no longer under the Active Directory Federation Services role (AD FS), but has been replaced by the Web Application Proxy under the Remote Access role.</span></span> <span data-ttu-id="40a4c-113">Это представляет расширение службы AD FS прокси, включая функции обратных прокси-серверов для публикации приложений.</span><span class="sxs-lookup"><span data-stu-id="40a4c-113">This represents an expansion of the AD FS proxy service by including reverse proxy functionality for application publishing.</span></span>

## <a name="solution"></a><span data-ttu-id="40a4c-114">Решение</span><span class="sxs-lookup"><span data-stu-id="40a4c-114">Solution</span></span>

<span data-ttu-id="40a4c-115">Чтобы получить доступ к прокси веб-приложения, администраторы могут перейти на диспетчер сервера и добавить новую роль или службу роли.</span><span class="sxs-lookup"><span data-stu-id="40a4c-115">To access the Web Application Proxy, administrators can go to Server Manager and add a new role/role service.</span></span> <span data-ttu-id="40a4c-116">Администратор найдет прокси веб-приложения в роли удаленного доступа.</span><span class="sxs-lookup"><span data-stu-id="40a4c-116">The administrator will find the Web Application Proxy under the Remote Access role.</span></span>

## <a name="resources"></a><span data-ttu-id="40a4c-117">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="40a4c-117">Resources</span></span>

-   <span data-ttu-id="40a4c-118">[Руководство по решению](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/dn280942(v=ws.11))</span><span class="sxs-lookup"><span data-stu-id="40a4c-118">[Solution guide](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/dn280942(v=ws.11))</span></span>

 

 
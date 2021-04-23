---
title: Удаленная служба данных удалена
description: Удаленные компоненты сервера удаленной службы данных в Windows 8
ms.assetid: 53ECB92C-8868-4A1A-82BD-4ADE75F7BB59
keywords:
- Сервер RDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b6588b029fe37f1312c709be168fd695bdc5738
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "103987952"
---
# <a name="remote-data-service-server-components-are-removed-in-windows-8"></a><span data-ttu-id="4ef5e-104">Удаленные компоненты сервера удаленной службы данных в Windows 8</span><span class="sxs-lookup"><span data-stu-id="4ef5e-104">Remote data service server components are removed in Windows 8</span></span>

## <a name="platforms"></a><span data-ttu-id="4ef5e-105">Платформы</span><span class="sxs-lookup"><span data-stu-id="4ef5e-105">Platforms</span></span>

 <span data-ttu-id="4ef5e-106">**Клиенты** — Windows 8</span><span class="sxs-lookup"><span data-stu-id="4ef5e-106">**Clients** - Windows 8</span></span>  
<span data-ttu-id="4ef5e-107">**Серверы** — Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4ef5e-107">**Servers** - Windows Server 2012</span></span>  



## <a name="description"></a><span data-ttu-id="4ef5e-108">Описание</span><span class="sxs-lookup"><span data-stu-id="4ef5e-108">Description</span></span>

<span data-ttu-id="4ef5e-109">Сервер удаленной службы данных (RDS) недоступен в Windows 8:</span><span class="sxs-lookup"><span data-stu-id="4ef5e-109">The remote data service (RDS) server is not available in Windows 8:</span></span>

-   <span data-ttu-id="4ef5e-110">Файл msadcf.dll, в котором размещается по умолчанию "бизнес-объект" RDSServer. DataObject, удаляется, а связанные с ним файлы (msadcfr.dll, msadcfr.dll. MUI, handler. reg и хандсафе. reg) удаляются.</span><span class="sxs-lookup"><span data-stu-id="4ef5e-110">File msadcf.dll, which hosts the default "business object" RDSServer.DataFactory, is removed, and its associated files (msadcfr.dll, msadcfr.dll.mui, handler.reg and handsafe.reg) are removed</span></span>
-   <span data-ttu-id="4ef5e-111">Файл msdfmap.dll, который является обработчиком по умолчанию, удаляется, а файл msdfmap.ini удаляется.</span><span class="sxs-lookup"><span data-stu-id="4ef5e-111">File msdfmap.dll, which is the default Handler, is removed, and the file msdfmap.ini is removed</span></span>
-   <span data-ttu-id="4ef5e-112">Файл msadcs.dll, ISAPI, удален</span><span class="sxs-lookup"><span data-stu-id="4ef5e-112">File msadcs.dll, the ISAPI, is removed</span></span>

## <a name="manifestation"></a><span data-ttu-id="4ef5e-113">Проявление</span><span class="sxs-lookup"><span data-stu-id="4ef5e-113">Manifestation</span></span>

<span data-ttu-id="4ef5e-114">Клиенты не могут размещать RDS Server в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4ef5e-114">Customers cannot host an RDS server on Windows 8.</span></span>

## <a name="mitigation"></a><span data-ttu-id="4ef5e-115">Меры по снижению риска</span><span class="sxs-lookup"><span data-stu-id="4ef5e-115">Mitigation</span></span>

<span data-ttu-id="4ef5e-116">Клиенты могут размещать свои RDS-серверы на компьютере с Windows 7 или с другими операционными системами нижнего уровня.</span><span class="sxs-lookup"><span data-stu-id="4ef5e-116">Customers can keep their RDS server on a machine with Windows 7 or other down-level operating systems.</span></span>

## <a name="solution"></a><span data-ttu-id="4ef5e-117">Решение</span><span class="sxs-lookup"><span data-stu-id="4ef5e-117">Solution</span></span>

<span data-ttu-id="4ef5e-118">Клиенты могут размещать свои RDS-серверы на компьютере с Windows 7 или с другими операционными системами нижнего уровня.</span><span class="sxs-lookup"><span data-stu-id="4ef5e-118">Customers can keep their RDS server on a machine with Windows 7 or other down-level operating systems.</span></span>

## <a name="resources"></a><span data-ttu-id="4ef5e-119">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="4ef5e-119">Resources</span></span>

[<span data-ttu-id="4ef5e-120">Схема технологий доступа к данным</span><span class="sxs-lookup"><span data-stu-id="4ef5e-120">Data Access Technologies Roadmap</span></span>](/sql/connect/connect-history?view=sqlallproducts-allversions)

 

 
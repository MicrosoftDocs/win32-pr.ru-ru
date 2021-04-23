---
description: API-интерфейсы видео Direct3D 9
ms.assetid: 2f5f46a0-f21f-4e57-9297-bad2b791da52
title: API-интерфейсы видео Direct3D 9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7346741b5e78f052b7c895ca417735614930d35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539569"
---
# <a name="direct3d-9-video-apis"></a><span data-ttu-id="d5c56-103">API-интерфейсы видео Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="d5c56-103">Direct3D 9 Video APIs</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d5c56-104">Приложения для Магазина Windows должны использовать Microsoft Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="d5c56-104">Windows Store apps must use Microsoft Direct3D 11.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="d5c56-105">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="d5c56-105">In this section</span></span>



| <span data-ttu-id="d5c56-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="d5c56-106">Topic</span></span>                                                                       | <span data-ttu-id="d5c56-107">Описание</span><span class="sxs-lookup"><span data-stu-id="d5c56-107">Description</span></span>                                                                                                                                 |
|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d5c56-108">Защита содержимого на основе GPU</span><span class="sxs-lookup"><span data-stu-id="d5c56-108">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)<br/> | <span data-ttu-id="d5c56-109">Описание содержимого видео — возможностей защиты, которые может предоставить графический драйвер.</span><span class="sxs-lookup"><span data-stu-id="d5c56-109">Describes video content–protection capabilities that a graphics driver can provide.</span></span><br/>                                              |
| [<span data-ttu-id="d5c56-110">Поддержка наложения оборудования</span><span class="sxs-lookup"><span data-stu-id="d5c56-110">Hardware Overlay Support</span></span>](hardware-overlay-support.md)<br/>         | <span data-ttu-id="d5c56-111">Описывает, как использовать наложение оборудования в Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="d5c56-111">Describes how to use hardware overlays in Direct3D 9.</span></span><br/>                                                                            |
| [<span data-ttu-id="d5c56-112">Отчеты о нехватке памяти</span><span class="sxs-lookup"><span data-stu-id="d5c56-112">Memory Pressure Reporting</span></span>](memory-pressure-reporting.md)<br/>       | <span data-ttu-id="d5c56-113">Отчеты о нехватке памяти позволяют приложению Direct3D определить, когда рабочий набор видеопамяти стал слишком большим.</span><span class="sxs-lookup"><span data-stu-id="d5c56-113">Memory pressure reporting enables a Direct3D application to determine when its video-memory working set has grown too large.</span></span><br/>     |
| [<span data-ttu-id="d5c56-114">Интерфейсы видео Direct3D</span><span class="sxs-lookup"><span data-stu-id="d5c56-114">Direct3D Video Interfaces</span></span>](direct3d-video-interfaces.md)<br/>       | <span data-ttu-id="d5c56-115">Описание интерфейсов видео Microsoft Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="d5c56-115">Describes the Microsoft Direct3D 9 video interfaces.</span></span><br/>                                                                             |
| [<span data-ttu-id="d5c56-116">Видеоструктуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="d5c56-116">Direct3D Video Structures</span></span>](direct3d-video-structures.md)<br/>       | <span data-ttu-id="d5c56-117">Описывает структуры, используемые интерфейсами видео Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="d5c56-117">Describes the structures used by the Direct3D 9 video interfaces.</span></span><br/>                                                                |
| [<span data-ttu-id="d5c56-118">Перечисления видео Direct3D</span><span class="sxs-lookup"><span data-stu-id="d5c56-118">Direct3D Video Enumerations</span></span>](direct3d-video-enumerations.md)<br/>   | <span data-ttu-id="d5c56-119">Описывает перечисления, используемые интерфейсами видео Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="d5c56-119">Describes the enumerations used by the Direct3D 9 video interfaces.</span></span><br/>                                                              |
| [<span data-ttu-id="d5c56-120">Защита содержимого команды</span><span class="sxs-lookup"><span data-stu-id="d5c56-120">Content Protection Commands</span></span>](content-protection-commands.md)<br/>   | <span data-ttu-id="d5c56-121">Содержит список команд для метода [**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) .</span><span class="sxs-lookup"><span data-stu-id="d5c56-121">Lists the commands for the [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) method.</span></span><br/> |
| [<span data-ttu-id="d5c56-122">Запросы Защита содержимого</span><span class="sxs-lookup"><span data-stu-id="d5c56-122">Content Protection Queries</span></span>](content-protection-queries.md)<br/>     | <span data-ttu-id="d5c56-123">Выводит список запросов для метода [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) .</span><span class="sxs-lookup"><span data-stu-id="d5c56-123">Lists the queries for the [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) method.</span></span><br/>          |



 

## <a name="related-topics"></a><span data-ttu-id="d5c56-124">См. также</span><span class="sxs-lookup"><span data-stu-id="d5c56-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5c56-125">Media Foundationое программное руководством</span><span class="sxs-lookup"><span data-stu-id="d5c56-125">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> </dl>

 

 





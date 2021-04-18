---
title: Функции администрирования RAS
description: В этой документации описываются функции RRAS, которые используются для разработки программного обеспечения для администрирования подключений удаленного доступа RAS.
ms.assetid: 27cf63e2-9dd3-4bc1-98af-e93055d89492
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec0a18f6c49964d89c308b065289dd4de9fc22c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332043"
---
# <a name="ras-administration-functions"></a><span data-ttu-id="adcc4-103">Функции администрирования RAS</span><span class="sxs-lookup"><span data-stu-id="adcc4-103">RAS Administration Functions</span></span>

<span data-ttu-id="adcc4-104">В этой документации описываются функции RRAS, которые используются для разработки программного обеспечения для администрирования подключений удаленного доступа RAS.</span><span class="sxs-lookup"><span data-stu-id="adcc4-104">This documentation describes RRAS functions that are used to develop software to administer RAS dial-up connections.</span></span> <span data-ttu-id="adcc4-105">К этим функциям относятся:</span><span class="sxs-lookup"><span data-stu-id="adcc4-105">These functions include:</span></span>

-   [<span data-ttu-id="adcc4-106">**мпрадминконнектионклеарстатс**</span><span class="sxs-lookup"><span data-stu-id="adcc4-106">**MprAdminConnectionClearStats**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionclearstats)
-   [<span data-ttu-id="adcc4-107">**мпрадминконнектионенум**</span><span class="sxs-lookup"><span data-stu-id="adcc4-107">**MprAdminConnectionEnum**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionenum)
-   [<span data-ttu-id="adcc4-108">**мпрадминконнектионенумекс**</span><span class="sxs-lookup"><span data-stu-id="adcc4-108">**MprAdminConnectionEnumEx**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionenumex)
-   [<span data-ttu-id="adcc4-109">**мпрадминконнектионжетинфо**</span><span class="sxs-lookup"><span data-stu-id="adcc4-109">**MprAdminConnectionGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectiongetinfo)
-   [<span data-ttu-id="adcc4-110">**мпрадминконнектионжетинфоекс**</span><span class="sxs-lookup"><span data-stu-id="adcc4-110">**MprAdminConnectionGetInfoEx**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectiongetinfoex)
-   [<span data-ttu-id="adcc4-111">**мпрадминконнектионремовекуарантине**</span><span class="sxs-lookup"><span data-stu-id="adcc4-111">**MprAdminConnectionRemoveQuarantine**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionremovequarantine)
-   [<span data-ttu-id="adcc4-112">**мпрадминпортклеарстатс**</span><span class="sxs-lookup"><span data-stu-id="adcc4-112">**MprAdminPortClearStats**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats)
-   [<span data-ttu-id="adcc4-113">**мпрадминпортдисконнект**</span><span class="sxs-lookup"><span data-stu-id="adcc4-113">**MprAdminPortDisconnect**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportdisconnect)
-   [<span data-ttu-id="adcc4-114">**мпрадминпортенум**</span><span class="sxs-lookup"><span data-stu-id="adcc4-114">**MprAdminPortEnum**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum)
-   [<span data-ttu-id="adcc4-115">**мпрадминпортжетинфо**</span><span class="sxs-lookup"><span data-stu-id="adcc4-115">**MprAdminPortGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo)
-   [<span data-ttu-id="adcc4-116">**мпрадминпортресет**</span><span class="sxs-lookup"><span data-stu-id="adcc4-116">**MprAdminPortReset**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportreset)

<span data-ttu-id="adcc4-117">Дополнительные функции используются как для администрирования службы удаленного доступа, так и для администрирования маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="adcc4-117">Additional functions are used for both RAS administration and router administration.</span></span> <span data-ttu-id="adcc4-118">Следующие функции описаны в справочнике по [функциям администрирования маршрутизатора](router-administration-functions.md) :</span><span class="sxs-lookup"><span data-stu-id="adcc4-118">The following functions documented in the [Router Administration Functions](router-administration-functions.md) reference:</span></span>

-   [<span data-ttu-id="adcc4-119">**мпрадминбуфферфри**</span><span class="sxs-lookup"><span data-stu-id="adcc4-119">**MprAdminBufferFree**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree)
-   [<span data-ttu-id="adcc4-120">**мпрадминжетеррорстринг**</span><span class="sxs-lookup"><span data-stu-id="adcc4-120">**MprAdminGetErrorString**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingeterrorstring)
-   [<span data-ttu-id="adcc4-121">**мпрадминиссервицеруннинг**</span><span class="sxs-lookup"><span data-stu-id="adcc4-121">**MprAdminIsServiceRunning**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminisservicerunning)
-   [<span data-ttu-id="adcc4-122">**мпрадминсерверконнект**</span><span class="sxs-lookup"><span data-stu-id="adcc4-122">**MprAdminServerConnect**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminserverconnect)
-   [<span data-ttu-id="adcc4-123">**мпрадминсервердисконнект**</span><span class="sxs-lookup"><span data-stu-id="adcc4-123">**MprAdminServerDisconnect**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminserverdisconnect)

<span data-ttu-id="adcc4-124">Для реализации библиотеки DLL администрирования RAS используйте функции, описанные в следующем разделе:</span><span class="sxs-lookup"><span data-stu-id="adcc4-124">To implement a RAS administration DLL, use the functions described in the following topic:</span></span>

-   [<span data-ttu-id="adcc4-125">Функции DLL администратора RAS</span><span class="sxs-lookup"><span data-stu-id="adcc4-125">RAS Admin DLL Functions</span></span>](ras-admin-dll-functions.md)

<span data-ttu-id="adcc4-126">Для управления пользователями сервера RAS используйте функции, описанные в следующем разделе:</span><span class="sxs-lookup"><span data-stu-id="adcc4-126">To manage users of a RAS server, use the functions described in the following topic:</span></span>

-   [<span data-ttu-id="adcc4-127">Функции администрирования пользователей RAS</span><span class="sxs-lookup"><span data-stu-id="adcc4-127">RAS User Administration Functions</span></span>](ras-user-administration-functions.md)

 

 





---
title: Архитектура служба удаленного управления Windows
description: Архитектура служба удаленного управления Windows состоит из компонентов на клиентских и серверных компьютерах.
ms.assetid: 82e67851-fe46-4bb0-8278-9718b5e0c7ae
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0f5576913c5e4a1f2a105fb77e2282dc682c6659
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793039"
---
# <a name="windows-remote-management-architecture"></a><span data-ttu-id="9c2ba-103">Архитектура служба удаленного управления Windows</span><span class="sxs-lookup"><span data-stu-id="9c2ba-103">Windows Remote Management Architecture</span></span>

<span data-ttu-id="9c2ba-104">Архитектура служба удаленного управления Windows состоит из компонентов на клиентских и серверных компьютерах.</span><span class="sxs-lookup"><span data-stu-id="9c2ba-104">The Windows Remote Management architecture consists of components on the client and server computers.</span></span> <span data-ttu-id="9c2ba-105">На следующем рисунке показаны компоненты на обоих компьютерах, как компоненты взаимодействуют с другими компонентами, и протокол, используемый для обмена данными между компьютерами.</span><span class="sxs-lookup"><span data-stu-id="9c2ba-105">The following illustration shows the components on both computers, how the components interact with other components, and the protocol that is used to communicate between the computers.</span></span>

![Архитектура WinRM](images/winrm-architecture.png)

## <a name="requesting-client"></a><span data-ttu-id="9c2ba-107">Запрос клиента</span><span class="sxs-lookup"><span data-stu-id="9c2ba-107">Requesting Client</span></span>

<span data-ttu-id="9c2ba-108">Следующие компоненты WinRM находятся на компьютере, на котором работает сценарий, запрашивающий данные.</span><span class="sxs-lookup"><span data-stu-id="9c2ba-108">The following WinRM components reside on the computer that is running the script that requests data.</span></span>

-   <span data-ttu-id="9c2ba-109">Приложение WinRM</span><span class="sxs-lookup"><span data-stu-id="9c2ba-109">WinRM application</span></span>

    <span data-ttu-id="9c2ba-110">Это сценарий или средство командной строки **WinRM** , которое использует API скриптов WinRM для вызова данных запроса или выполнения методов.</span><span class="sxs-lookup"><span data-stu-id="9c2ba-110">This is the script or **Winrm** command-line tool that uses the WinRM scripting API to make calls to request data or to execute methods.</span></span> <span data-ttu-id="9c2ba-111">Дополнительные сведения см. в разделе [API сценариев WinRM](winrm-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="9c2ba-111">For more information, see the [WinRM Scripting API](winrm-scripting-api.md).</span></span>

-   <span data-ttu-id="9c2ba-112">WSMAuto.dll</span><span class="sxs-lookup"><span data-stu-id="9c2ba-112">WSMAuto.dll</span></span>

    <span data-ttu-id="9c2ba-113">Уровень автоматизации, обеспечивающий поддержку сценариев.</span><span class="sxs-lookup"><span data-stu-id="9c2ba-113">The Automation layer that provides scripting support.</span></span>

-   <span data-ttu-id="9c2ba-114">WsmCL.dll</span><span class="sxs-lookup"><span data-stu-id="9c2ba-114">WsmCL.dll</span></span>

    <span data-ttu-id="9c2ba-115">Уровень API C в операционной системе.</span><span class="sxs-lookup"><span data-stu-id="9c2ba-115">C API layer within the operating system.</span></span>

-   <span data-ttu-id="9c2ba-116">API HTTP</span><span class="sxs-lookup"><span data-stu-id="9c2ba-116">HTTP API</span></span>

    <span data-ttu-id="9c2ba-117">Для WinRM требуется поддержка транспорта HTTP и HTTPS.</span><span class="sxs-lookup"><span data-stu-id="9c2ba-117">WinRM requires support for HTTP and HTTPS transport.</span></span>

## <a name="responding-server"></a><span data-ttu-id="9c2ba-118">Отвечающий сервер</span><span class="sxs-lookup"><span data-stu-id="9c2ba-118">Responding Server</span></span>

<span data-ttu-id="9c2ba-119">Следующие компоненты WinRM находятся на отвечающем компьютере.</span><span class="sxs-lookup"><span data-stu-id="9c2ba-119">The following WinRM components reside on the responding computer.</span></span>

-   <span data-ttu-id="9c2ba-120">API HTTP</span><span class="sxs-lookup"><span data-stu-id="9c2ba-120">HTTP API</span></span>

    <span data-ttu-id="9c2ba-121">Для WinRM требуется поддержка транспорта HTTP и HTTPS.</span><span class="sxs-lookup"><span data-stu-id="9c2ba-121">WinRM requires support for HTTP and HTTPS transport.</span></span>

-   <span data-ttu-id="9c2ba-122">WSMAuto.dll</span><span class="sxs-lookup"><span data-stu-id="9c2ba-122">WSMAuto.dll</span></span>

    <span data-ttu-id="9c2ba-123">Уровень автоматизации, обеспечивающий поддержку сценариев.</span><span class="sxs-lookup"><span data-stu-id="9c2ba-123">The Automation layer that provides scripting support.</span></span>

-   <span data-ttu-id="9c2ba-124">WsmCL.dll</span><span class="sxs-lookup"><span data-stu-id="9c2ba-124">WsmCL.dll</span></span>

    <span data-ttu-id="9c2ba-125">Уровень API C в операционной системе.</span><span class="sxs-lookup"><span data-stu-id="9c2ba-125">C API layer within the operating system.</span></span>

-   <span data-ttu-id="9c2ba-126">WsmSvc.dll</span><span class="sxs-lookup"><span data-stu-id="9c2ba-126">WsmSvc.dll</span></span>

    <span data-ttu-id="9c2ba-127">Служба [*прослушивателя*](windows-remote-management-glossary.md) WinRM.</span><span class="sxs-lookup"><span data-stu-id="9c2ba-127">WinRM [*listener*](windows-remote-management-glossary.md) service.</span></span>

-   <span data-ttu-id="9c2ba-128">WsmProv.dll</span><span class="sxs-lookup"><span data-stu-id="9c2ba-128">WsmProv.dll</span></span>

    <span data-ttu-id="9c2ba-129">Подсистема поставщика.</span><span class="sxs-lookup"><span data-stu-id="9c2ba-129">Provider subsystem.</span></span>

-   <span data-ttu-id="9c2ba-130">WsmRes.dll</span><span class="sxs-lookup"><span data-stu-id="9c2ba-130">WsmRes.dll</span></span>

    <span data-ttu-id="9c2ba-131">Файл ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9c2ba-131">Resource file.</span></span>

-   <span data-ttu-id="9c2ba-132">WsmWmiPl.dll</span><span class="sxs-lookup"><span data-stu-id="9c2ba-132">WsmWmiPl.dll</span></span>

    <span data-ttu-id="9c2ba-133">[*Подключаемый модуль WMI*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="9c2ba-133">[*WMI plug-in*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="9c2ba-134">Это позволяет получать данные WMI с помощью WinRM.</span><span class="sxs-lookup"><span data-stu-id="9c2ba-134">This allows you to obtain WMI data through WinRM.</span></span>

-   <span data-ttu-id="9c2ba-135">Драйвер IPMI и поставщик IPMI WMI</span><span class="sxs-lookup"><span data-stu-id="9c2ba-135">Intelligent Platform Management Interface (IPMI) driver and WMI IPMI provider</span></span>

    <span data-ttu-id="9c2ba-136">Эти компоненты предоставляют все данные оборудования, запрашиваемые с помощью классов IPMI.</span><span class="sxs-lookup"><span data-stu-id="9c2ba-136">These components supply any hardware data that is requested using the IPMI classes.</span></span> <span data-ttu-id="9c2ba-137">Дополнительные сведения см. в разделе [поставщик IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider).</span><span class="sxs-lookup"><span data-stu-id="9c2ba-137">For more information, see [IPMI Provider](/previous-versions/windows/desktop/ipmiprv/ipmi-provider).</span></span> <span data-ttu-id="9c2ba-138">Оборудование BMC должно быть обнаружено SMBIOS или устройством, созданным вручную путем загрузки драйвера.</span><span class="sxs-lookup"><span data-stu-id="9c2ba-138">BMC hardware must have been detected by the SMBIOS or the device created manually by loading the driver.</span></span> <span data-ttu-id="9c2ba-139">Дополнительные сведения см. в разделе [Установка и настройка для служба удаленного управления Windows](installation-and-configuration-for-windows-remote-management.md).</span><span class="sxs-lookup"><span data-stu-id="9c2ba-139">For more information, see [Installation and Configuration for Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9c2ba-140">См. также</span><span class="sxs-lookup"><span data-stu-id="9c2ba-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c2ba-141">О служба удаленного управления Windows</span><span class="sxs-lookup"><span data-stu-id="9c2ba-141">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> </dl>

 

 
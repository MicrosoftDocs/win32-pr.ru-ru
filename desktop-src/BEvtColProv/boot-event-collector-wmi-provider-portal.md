---
description: Поставщик WMI сборщика событий загрузки предоставляет доступ к сведениям о подключении и конфигурации для функции сбора событий установки и загрузки в Windows Server.
ms.assetid: ab9ac8f0-69a5-4a2d-8ee5-1f003aa1bb5b
ms.tgt_platform: multiple
title: Поставщик WMI сборщика событий загрузки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a38ef27b2989f856fdcfda82d4ee0e68c3913167
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895329"
---
# <a name="boot-event-collector-wmi-provider"></a><span data-ttu-id="50fdb-103">Поставщик WMI сборщика событий загрузки</span><span class="sxs-lookup"><span data-stu-id="50fdb-103">Boot Event Collector WMI Provider</span></span>

## <a name="purpose"></a><span data-ttu-id="50fdb-104">Назначение</span><span class="sxs-lookup"><span data-stu-id="50fdb-104">Purpose</span></span>

<span data-ttu-id="50fdb-105">Поставщик WMI сборщика событий загрузки предоставляет доступ к сведениям о подключении и конфигурации для функции сбора событий установки и загрузки в Windows Server.</span><span class="sxs-lookup"><span data-stu-id="50fdb-105">The Boot Event Collector WMI provider provides access to connection and configuration information for the Setup and Boot Event Collection feature on Windows Server.</span></span> <span data-ttu-id="50fdb-106">Это позволяет просматривать список текущих подключений и журнал подключений между сервером сборщика и его конечными компьютерами.</span><span class="sxs-lookup"><span data-stu-id="50fdb-106">This allows you to view a list of the current connections and the connection history between a collector server and its target computers.</span></span> <span data-ttu-id="50fdb-107">Кроме того, этот поставщик позволяет управлять конфигурацией сервера сборщика.</span><span class="sxs-lookup"><span data-stu-id="50fdb-107">In addition, this provider allows you to manage the configuration of a collector server.</span></span>

> [!Note]  
> <span data-ttu-id="50fdb-108">Поставщик WMI сборщика событий загрузки реализуется в BEvtCol.exe.</span><span class="sxs-lookup"><span data-stu-id="50fdb-108">The Boot Event Collector WMI provider is implemented in BEvtCol.exe.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="50fdb-109">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="50fdb-109">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="50fdb-110">**таржетфорвардинг**</span><span class="sxs-lookup"><span data-stu-id="50fdb-110">**TargetForwarding**</span></span>](targetforwarding.md)
</dt> <dd>

<span data-ttu-id="50fdb-111">Извлекает данные пересылки с конечного компьютера.</span><span class="sxs-lookup"><span data-stu-id="50fdb-111">Retrieves forwarding data from a target computer.</span></span>

</dd> <dt>

[<span data-ttu-id="50fdb-112">**таржетфорвардингдестинатион**</span><span class="sxs-lookup"><span data-stu-id="50fdb-112">**TargetForwardingDestination**</span></span>](targetforwardingdestination.md)
</dt> <dd>

<span data-ttu-id="50fdb-113">Известные места назначения, содержащие собранные данные.</span><span class="sxs-lookup"><span data-stu-id="50fdb-113">The known destinations containing the collected data.</span></span> <span data-ttu-id="50fdb-114">Доступно, только если сборщик работает с включенным журналом состояния.</span><span class="sxs-lookup"><span data-stu-id="50fdb-114">Available only if the collector is running with the status log enabled.</span></span>

</dd> <dt>

[<span data-ttu-id="50fdb-115">**таржетфорвардингхистори**</span><span class="sxs-lookup"><span data-stu-id="50fdb-115">**TargetForwardingHistory**</span></span>](targetforwardinghistory.md)
</dt> <dd>

<span data-ttu-id="50fdb-116">Журнал последних изменений пересылаемых данных для конечного компьютера.</span><span class="sxs-lookup"><span data-stu-id="50fdb-116">The recent history of changes to the forwarding data for a target computer.</span></span>

</dd> <dt>

[<span data-ttu-id="50fdb-117">**Элемента**</span><span class="sxs-lookup"><span data-stu-id="50fdb-117">**Control**</span></span>](control.md)
</dt> <dd>

<span data-ttu-id="50fdb-118">Управление экземпляром сборщика.</span><span class="sxs-lookup"><span data-stu-id="50fdb-118">Control of the collector instance.</span></span> <span data-ttu-id="50fdb-119">Требуются права администратора (BA).</span><span class="sxs-lookup"><span data-stu-id="50fdb-119">Requires the Administrator (BA) privileges.</span></span>

</dd> </dl>

 

 




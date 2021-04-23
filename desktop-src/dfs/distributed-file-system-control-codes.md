---
title: Коды управления распределенная файловая система
description: распределенная файловая система управляющих кодов DFS
ms.assetid: 1d9bebe6-f494-41e5-8a8d-51bf98eaa374
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe054f87210c40da595dd731b263c485311729a7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987640"
---
# <a name="distributed-file-system-control-codes"></a><span data-ttu-id="423ca-103">Коды управления распределенная файловая система</span><span class="sxs-lookup"><span data-stu-id="423ca-103">Distributed File System Control Codes</span></span>

<span data-ttu-id="423ca-104">Ниже приведены коды управления распределенная файловая система (DFS):</span><span class="sxs-lookup"><span data-stu-id="423ca-104">The following are the Distributed File System (DFS) control codes:</span></span>

## <a name="in-this-section"></a><span data-ttu-id="423ca-105">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="423ca-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="423ca-106">**FSCTL_DFS_GET_PKT_ENTRY_STATE**</span><span class="sxs-lookup"><span data-stu-id="423ca-106">**FSCTL_DFS_GET_PKT_ENTRY_STATE**</span></span>](fsctl-dfs-get-pkt-entry-state.md)
</dt> <dd>

<span data-ttu-id="423ca-107">Код элемента управления [**FSCTL_DFS_GET_PKT_ENTRY_STATE**](fsctl-dfs-get-pkt-entry-state.md) может получить те же сведения, что и функция [**нетдфсжетклиентинфо**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo) , но может обеспечить лучшую производительность в некоторых конфигурациях с высокой задержкой для серверов DFS.</span><span class="sxs-lookup"><span data-stu-id="423ca-107">The [**FSCTL_DFS_GET_PKT_ENTRY_STATE**](fsctl-dfs-get-pkt-entry-state.md) control code can get the same information as the [**NetDfsGetClientInfo**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo) function but can provide better performance in some configurations with high latencies to the DFS servers.</span></span> <span data-ttu-id="423ca-108">Не рекомендуется использовать управляющий код **FSCTL_DFS_GET_PKT_ENTRY_STATE** , если нет проблем с производительностью.</span><span class="sxs-lookup"><span data-stu-id="423ca-108">It is not recommended to use the **FSCTL_DFS_GET_PKT_ENTRY_STATE** control code unless there are performance issues.</span></span>

<span data-ttu-id="423ca-109">Чтобы выполнить эту операцию, вызовите функцию [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) .</span><span class="sxs-lookup"><span data-stu-id="423ca-109">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function.</span></span>

</dd> </dl>
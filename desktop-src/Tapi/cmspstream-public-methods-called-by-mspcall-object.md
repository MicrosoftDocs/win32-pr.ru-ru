---
description: В следующем списке содержатся методы Кмспстреам, вызываемые объектом Мспкалл.
ms.assetid: 7a59ca78-b5e8-45e9-8fdb-89402ffef916
title: Методы Кмспстреам, вызываемые объектом Мспкалл
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89744f9e4cf2739fa11f07edc4be7e331beb620a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683796"
---
# <a name="cmspstream-public-methods-called-by-mspcall-object"></a><span data-ttu-id="2686b-103">Кмспстреам открытые методы, вызываемые объектом Мспкалл</span><span class="sxs-lookup"><span data-stu-id="2686b-103">CMSPStream Public Methods Called by MSPCall Object</span></span>



| <span data-ttu-id="2686b-104">Кмспстреам открытые методы</span><span class="sxs-lookup"><span data-stu-id="2686b-104">CMSPStream public methods</span></span>                                 | <span data-ttu-id="2686b-105">Описание</span><span class="sxs-lookup"><span data-stu-id="2686b-105">Description</span></span>                                                                             |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="2686b-106">**Ini**</span><span class="sxs-lookup"><span data-stu-id="2686b-106">**Init**</span></span>](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-init)                           | <span data-ttu-id="2686b-107">Вызывается **мспкалл** при создании потока.</span><span class="sxs-lookup"><span data-stu-id="2686b-107">Called by the **MSPCall** when the stream is created.</span></span>                                   |
| [<span data-ttu-id="2686b-108">**Закрытия**</span><span class="sxs-lookup"><span data-stu-id="2686b-108">**ShutDown**</span></span>](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-shutdown)                   | <span data-ttu-id="2686b-109">Вызывается методом **мспкалл** для отмены выбора всех объектов терминала и освобождения объекта вызова.</span><span class="sxs-lookup"><span data-stu-id="2686b-109">Called by the **MSPCall** to unselect all terminal objects and release the call object.</span></span> |
| [<span data-ttu-id="2686b-110">**GetState**</span><span class="sxs-lookup"><span data-stu-id="2686b-110">**GetState**</span></span>](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-getstate)                   | <span data-ttu-id="2686b-111">Вызывается объектом Мспкалл для получения текущего состояния потока.</span><span class="sxs-lookup"><span data-stu-id="2686b-111">Called by the MSPCall object to get the current status of the stream.</span></span>                   |
| [<span data-ttu-id="2686b-112">**хандлетспдата**</span><span class="sxs-lookup"><span data-stu-id="2686b-112">**HandleTSPData**</span></span>](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-handletspdata)         | <span data-ttu-id="2686b-113">Производный объект call может вызвать этот метод, чтобы поток мог выполнять команды TSP.</span><span class="sxs-lookup"><span data-stu-id="2686b-113">Derived call object may call this method to let the stream handle the TSP commands.</span></span>     |
| [<span data-ttu-id="2686b-114">**процессграфевент**</span><span class="sxs-lookup"><span data-stu-id="2686b-114">**ProcessGraphEvent**</span></span>](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-processgraphevent) | <span data-ttu-id="2686b-115">Вызывается объектом Мспкалл, чтобы позволить потоку выполнять события графа.</span><span class="sxs-lookup"><span data-stu-id="2686b-115">Called by the MSPCall object to let the stream handle graph events.</span></span>                     |



 

 

 




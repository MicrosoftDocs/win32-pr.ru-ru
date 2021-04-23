---
title: Обзор записи службы имен
description: Запись службы имен состоит из трех различных разделов.
ms.assetid: 3059a9a9-174d-4d04-8565-e4558f17f465
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efc3855f586582b013bc47b11eb058ae461014f4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105672173"
---
# <a name="an-overview-of-the-name-service-entry"></a><span data-ttu-id="49d67-103">Обзор записи службы имен</span><span class="sxs-lookup"><span data-stu-id="49d67-103">An Overview of the Name Service Entry</span></span>

<span data-ttu-id="49d67-104">Запись службы имен состоит из трех различных разделов.</span><span class="sxs-lookup"><span data-stu-id="49d67-104">The name service entry consists of three distinct sections.</span></span> <span data-ttu-id="49d67-105">Первый раздел предназначен для интерфейсов (UUID + Version), второй раздел содержит идентификаторы UUID объекта, а третий раздел — для дескрипторов привязки.</span><span class="sxs-lookup"><span data-stu-id="49d67-105">The first section is for interfaces (UUID + version), the second section contains the object UUIDs, and the third section is for binding handles.</span></span> <span data-ttu-id="49d67-106">Вы указываете имя для записи, которое будет служить способом ее распознавания.</span><span class="sxs-lookup"><span data-stu-id="49d67-106">You provide a name for the entry that will serve as a way to identify it.</span></span>

<span data-ttu-id="49d67-107">При вызове [**рпкнсбиндинжекспорт**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta)сервер указывает имя записи, в которую следует поместить экспортированные данные.</span><span class="sxs-lookup"><span data-stu-id="49d67-107">When calling [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta), the server specifies the name of the entry in which to place the exported information.</span></span> <span data-ttu-id="49d67-108">После этого вновь экспортированный интерфейс добавляется в раздел Interface записи службы имен.</span><span class="sxs-lookup"><span data-stu-id="49d67-108">This newly exported interface is then added to the interface section of the name service entry.</span></span> <span data-ttu-id="49d67-109">Все интерфейсы, которые уже имеются в записи службы имен, остаются также.</span><span class="sxs-lookup"><span data-stu-id="49d67-109">Any interfaces that are already present in the name service entry remain as well.</span></span> <span data-ttu-id="49d67-110">Этот же процесс выполняется для идентификаторов UUID объекта и дескрипторов привязки.</span><span class="sxs-lookup"><span data-stu-id="49d67-110">This same process is followed for object UUIDs and binding handles.</span></span>

<span data-ttu-id="49d67-111">Клиент вызывает [**рпкнсбиндинглукупбегин**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina) (или [**рпкнсбиндингимпортбегин**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)) для поиска соответствующего маркера привязки.</span><span class="sxs-lookup"><span data-stu-id="49d67-111">The client calls [**RpcNsBindingLookupBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina) (or [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)) to search for an appropriate binding handle.</span></span> <span data-ttu-id="49d67-112">Извлекаются имя записи, маркер интерфейса и идентификатор UUID объекта.</span><span class="sxs-lookup"><span data-stu-id="49d67-112">The entry name, interface handle, and an object UUID are extracted.</span></span> <span data-ttu-id="49d67-113">Они ограничивают записи, из которых возвращаются дескрипторы привязки.</span><span class="sxs-lookup"><span data-stu-id="49d67-113">These restrict the entries from which binding handles are returned.</span></span> <span data-ttu-id="49d67-114">Если запись соответствует критериям поиска, все дескрипторы привязки в этой записи возвращаются из [**рпкнсбиндингимпортнекст**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext).</span><span class="sxs-lookup"><span data-stu-id="49d67-114">If an entry matches the search criteria, all the binding handles in that entry are returned from [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext).</span></span>

 

 





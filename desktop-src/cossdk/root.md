---
description: Содержит коллекции верхнего уровня в каталоге.
ms.assetid: 6cd23e6a-53b8-42ec-97df-59281f019252
title: Корневая коллекция
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Root
api_type:
- COM
api_location: ''
ms.openlocfilehash: ad896c69ab6fad75179c9bb30668143aa2ea741e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692008"
---
# <a name="root-collection"></a><span data-ttu-id="8ca83-103">Корневая коллекция</span><span class="sxs-lookup"><span data-stu-id="8ca83-103">Root collection</span></span>

<span data-ttu-id="8ca83-104">Содержит коллекции верхнего уровня в каталоге.</span><span class="sxs-lookup"><span data-stu-id="8ca83-104">Contains the top-level collections in the catalog.</span></span> <span data-ttu-id="8ca83-105">Он не содержит ни одного объекта [**комадминкаталогобжект**](comadmincatalogobject.md) или не поддерживает какие бы то ни было свойства.</span><span class="sxs-lookup"><span data-stu-id="8ca83-105">It does not contain any [**COMAdminCatalogObject**](comadmincatalogobject.md) objects or support any properties.</span></span>

<span data-ttu-id="8ca83-106">**Корневая** коллекция не поддерживает методы [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) и [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) объекта [**комадминкаталогколлектион**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="8ca83-106">The **Root** collection does not support the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

<span data-ttu-id="8ca83-107">Нельзя переходить к **корневой** коллекции из любой коллекции.</span><span class="sxs-lookup"><span data-stu-id="8ca83-107">You cannot navigate to the **Root** collection from any collection.</span></span>

## <a name="members"></a><span data-ttu-id="8ca83-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="8ca83-108">Members</span></span>

<span data-ttu-id="8ca83-109">**Корневая** коллекция наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , но не содержит дополнительных элементов.</span><span class="sxs-lookup"><span data-stu-id="8ca83-109">The **Root** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="8ca83-110">Связанные коллекции</span><span class="sxs-lookup"><span data-stu-id="8ca83-110">Related Collections</span></span>

<span data-ttu-id="8ca83-111">Ниже перечислены коллекции верхнего уровня в каталоге.</span><span class="sxs-lookup"><span data-stu-id="8ca83-111">The following are the top-level collections in the catalog:</span></span>

-   [<span data-ttu-id="8ca83-112">**аппликатионклустер**</span><span class="sxs-lookup"><span data-stu-id="8ca83-112">**ApplicationCluster**</span></span>](applicationcluster.md)
-   [<span data-ttu-id="8ca83-113">**аппликатионинстанцес**</span><span class="sxs-lookup"><span data-stu-id="8ca83-113">**ApplicationInstances**</span></span>](applicationinstances.md)
-   [<span data-ttu-id="8ca83-114">**Приложения**</span><span class="sxs-lookup"><span data-stu-id="8ca83-114">**Applications**</span></span>](applications.md)
-   [<span data-ttu-id="8ca83-115">**компутерлист**</span><span class="sxs-lookup"><span data-stu-id="8ca83-115">**ComputerList**</span></span>](computerlist.md)
-   [<span data-ttu-id="8ca83-116">**дкомпротоколс**</span><span class="sxs-lookup"><span data-stu-id="8ca83-116">**DCOMProtocols**</span></span>](dcomprotocols.md)
-   [<span data-ttu-id="8ca83-117">**евентклассесфориид**</span><span class="sxs-lookup"><span data-stu-id="8ca83-117">**EventClassesForIID**</span></span>](eventclassesforiid.md)
-   [<span data-ttu-id="8ca83-118">**филесфоримпорт**</span><span class="sxs-lookup"><span data-stu-id="8ca83-118">**FilesForImport**</span></span>](filesforimport.md)
-   [<span data-ttu-id="8ca83-119">**инпроксерверс**</span><span class="sxs-lookup"><span data-stu-id="8ca83-119">**InprocServers**</span></span>](inprocservers.md)
-   [<span data-ttu-id="8ca83-120">**легацисерверс**</span><span class="sxs-lookup"><span data-stu-id="8ca83-120">**LegacyServers**</span></span>](legacyservers.md)
-   [<span data-ttu-id="8ca83-121">**локалкомпутер**</span><span class="sxs-lookup"><span data-stu-id="8ca83-121">**LocalComputer**</span></span>](localcomputer.md)
-   [<span data-ttu-id="8ca83-122">**Секции**</span><span class="sxs-lookup"><span data-stu-id="8ca83-122">**Partitions**</span></span>](partitions.md)
-   [<span data-ttu-id="8ca83-123">**партитионусерс**</span><span class="sxs-lookup"><span data-stu-id="8ca83-123">**PartitionUsers**</span></span>](partitionusers.md)
-   [<span data-ttu-id="8ca83-124">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="8ca83-124">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="8ca83-125">**релатедколлектионинфо**</span><span class="sxs-lookup"><span data-stu-id="8ca83-125">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)
-   [<span data-ttu-id="8ca83-126">**трансиентсубскриптионс**</span><span class="sxs-lookup"><span data-stu-id="8ca83-126">**TransientSubscriptions**</span></span>](transientsubscriptions.md)
-   [<span data-ttu-id="8ca83-127">**вовинпроксерверс**</span><span class="sxs-lookup"><span data-stu-id="8ca83-127">**WOWInprocServers**</span></span>](wowinprocservers.md)
-   [<span data-ttu-id="8ca83-128">**вовлегацисерверс**</span><span class="sxs-lookup"><span data-stu-id="8ca83-128">**WOWLegacyServers**</span></span>](wowlegacyservers.md)

## <a name="see-also"></a><span data-ttu-id="8ca83-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8ca83-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ca83-130">Коллекции администрирования COM+</span><span class="sxs-lookup"><span data-stu-id="8ca83-130">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 

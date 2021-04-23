---
description: Обратный вызов для возврата версий всех поддерживаемых интерфейсов. Это позволяет потребителю не синхронизироваться с подсистемой захвата.
MS-HAID: vspixengine.IVersionCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Интерфейс Иверсионкаллбакк
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 7135E175-C537-4B0C-8F0A-CB77E3F2D945
api_name:
- IVersionCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5c53008e625d63e2e876bef9ab8cbdd376508c2f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105701126"
---
# <a name="span-idvspixengineiversioncallbackspaniversioncallback-interface"></a><span data-ttu-id="c9774-104"><span id="vspixengine.iversioncallback"></span>Интерфейс Иверсионкаллбакк</span><span class="sxs-lookup"><span data-stu-id="c9774-104"><span id="vspixengine.iversioncallback"></span>IVersionCallback interface</span></span>

<span data-ttu-id="c9774-105">Обратный вызов для возврата версий всех поддерживаемых интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="c9774-105">Callback to return the versions of all the interfaces supported.</span></span> <span data-ttu-id="c9774-106">Это позволяет потребителю не синхронизироваться с подсистемой захвата.</span><span class="sxs-lookup"><span data-stu-id="c9774-106">This allows the consumer to be out of sync with the capture engine.</span></span>

## <a name="members"></a><span data-ttu-id="c9774-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="c9774-107">Members</span></span>

<span data-ttu-id="c9774-108">Интерфейс **иверсионкаллбакк** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="c9774-108">The **IVersionCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c9774-109">**Иверсионкаллбакк** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c9774-109">**IVersionCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="c9774-110">Методы</span><span class="sxs-lookup"><span data-stu-id="c9774-110">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="c9774-111"><span id="methods"></span>Методы</span><span class="sxs-lookup"><span data-stu-id="c9774-111"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="c9774-112">Интерфейс **иверсионкаллбакк** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="c9774-112">The **IVersionCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="c9774-113">Метод</span><span class="sxs-lookup"><span data-stu-id="c9774-113">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="c9774-114">Описание</span><span class="sxs-lookup"><span data-stu-id="c9774-114">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="c9774-115"><a href="/windows/desktop/direct3dtools/iversioncallback-versiontableready-guid-arr-uint"><strong>версионтаблереади</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9774-115"><a href="/windows/desktop/direct3dtools/iversioncallback-versiontableready-guid-arr-uint"><strong>VersionTableReady</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="c9774-116">Функция обратного вызова, используемая для уведомления узла о том, какие интерфейсы поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="c9774-116">A callback function used to notify the host of which interfaces are supported.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="c9774-117">Требования</span><span class="sxs-lookup"><span data-stu-id="c9774-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="c9774-118">Header</span><span class="sxs-lookup"><span data-stu-id="c9774-118">Header</span></span></p></td><td><span data-ttu-id="c9774-119">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="c9774-119">Vspixengine.h</span></span></td></tr></tbody></table>

 

 

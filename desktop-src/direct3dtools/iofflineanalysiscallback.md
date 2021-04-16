---
description: Обратный вызов для возврата данных анализа вне сети.
MS-HAID: vspixengine.IOfflineAnalysisCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Интерфейс Иоффлинеаналисискаллбакк
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 39E6B9CA-C17A-42C8-AC6D-118DC8DE3AD9
api_name:
- IOfflineAnalysisCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 496ca07544cdc38ff9f0e3f29c0ebbd2b9e8753c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105719254"
---
# <a name="span-idvspixengineiofflineanalysiscallbackspaniofflineanalysiscallback-interface"></a><span data-ttu-id="104b7-103"><span id="vspixengine.iofflineanalysiscallback"></span>Интерфейс Иоффлинеаналисискаллбакк</span><span class="sxs-lookup"><span data-stu-id="104b7-103"><span id="vspixengine.iofflineanalysiscallback"></span>IOfflineAnalysisCallback interface</span></span>

<span data-ttu-id="104b7-104">Обратный вызов для возврата данных анализа вне сети.</span><span class="sxs-lookup"><span data-stu-id="104b7-104">Callback to returns offline analysis data.</span></span>

## <a name="members"></a><span data-ttu-id="104b7-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="104b7-105">Members</span></span>

<span data-ttu-id="104b7-106">Интерфейс **иоффлинеаналисискаллбакк** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="104b7-106">The **IOfflineAnalysisCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="104b7-107">**Иоффлинеаналисискаллбакк** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="104b7-107">**IOfflineAnalysisCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="104b7-108">Методы</span><span class="sxs-lookup"><span data-stu-id="104b7-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="104b7-109"><span id="methods"></span>Методы</span><span class="sxs-lookup"><span data-stu-id="104b7-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="104b7-110">Интерфейс **иоффлинеаналисискаллбакк** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="104b7-110">The **IOfflineAnalysisCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="104b7-111">Метод</span><span class="sxs-lookup"><span data-stu-id="104b7-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="104b7-112">Описание</span><span class="sxs-lookup"><span data-stu-id="104b7-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="104b7-113"><a href="/windows/desktop/direct3dtools/iofflineanalysiscallback-offlineanalysiscomplete-dword-hresult-bstr"><strong>оффлинеаналисискомплете</strong></a></span><span class="sxs-lookup"><span data-stu-id="104b7-113"><a href="/windows/desktop/direct3dtools/iofflineanalysiscallback-offlineanalysiscomplete-dword-hresult-bstr"><strong>OfflineAnalysisComplete</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="104b7-114">Функция обратного вызова, используемая для уведомления узла о завершении автономного анализа.</span><span class="sxs-lookup"><span data-stu-id="104b7-114">A callback function used to notify the host that offline analysis has completed.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="104b7-115"><a href="/windows/desktop/direct3dtools/iofflineanalysiscallback-offlineanalysisprogress-dword-double"><strong>оффлинеаналисиспрогресс</strong></a></span><span class="sxs-lookup"><span data-stu-id="104b7-115"><a href="/windows/desktop/direct3dtools/iofflineanalysiscallback-offlineanalysisprogress-dword-double"><strong>OfflineAnalysisProgress</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="104b7-116">Функция обратного вызова, используемая для уведомления узла о ходе автономного анализа.</span><span class="sxs-lookup"><span data-stu-id="104b7-116">A callback function used to notify the host of offline analysis progress.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="104b7-117">Требования</span><span class="sxs-lookup"><span data-stu-id="104b7-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="104b7-118">Header</span><span class="sxs-lookup"><span data-stu-id="104b7-118">Header</span></span></p></td><td><span data-ttu-id="104b7-119">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="104b7-119">Vspixengine.h</span></span></td></tr></tbody></table>

 

 

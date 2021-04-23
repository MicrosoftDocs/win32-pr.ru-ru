---
description: Обратный вызов для возврата сведений о том, кэшируется ли запрос вне сети.
MS-HAID: vspixengine.IOfflineAnalysisCacheCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Интерфейс Иоффлинеаналисискачекаллбакк
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: E226B1A6-D028-4562-9C8C-D25EC91A2DB2
api_name:
- IOfflineAnalysisCacheCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e0107f97353bf7ad5b62472bc54a2b8388fb6aff
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537928"
---
# <a name="span-idvspixengineiofflineanalysiscachecallbackspaniofflineanalysiscachecallback-interface"></a><span data-ttu-id="f80a4-103"><span id="vspixengine.iofflineanalysiscachecallback"></span>Интерфейс Иоффлинеаналисискачекаллбакк</span><span class="sxs-lookup"><span data-stu-id="f80a4-103"><span id="vspixengine.iofflineanalysiscachecallback"></span>IOfflineAnalysisCacheCallback interface</span></span>

<span data-ttu-id="f80a4-104">Обратный вызов для возврата сведений о том, кэшируется ли запрос вне сети.</span><span class="sxs-lookup"><span data-stu-id="f80a4-104">Callback to return information on whether an offline request is cached or not.</span></span>

## <a name="members"></a><span data-ttu-id="f80a4-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="f80a4-105">Members</span></span>

<span data-ttu-id="f80a4-106">Интерфейс **иоффлинеаналисискачекаллбакк** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="f80a4-106">The **IOfflineAnalysisCacheCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f80a4-107">**Иоффлинеаналисискачекаллбакк** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f80a4-107">**IOfflineAnalysisCacheCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="f80a4-108">Методы</span><span class="sxs-lookup"><span data-stu-id="f80a4-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="f80a4-109"><span id="methods"></span>Методы</span><span class="sxs-lookup"><span data-stu-id="f80a4-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="f80a4-110">Интерфейс **иоффлинеаналисискачекаллбакк** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="f80a4-110">The **IOfflineAnalysisCacheCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="f80a4-111">Метод</span><span class="sxs-lookup"><span data-stu-id="f80a4-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="f80a4-112">Описание</span><span class="sxs-lookup"><span data-stu-id="f80a4-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="f80a4-113"><a href="/windows/desktop/direct3dtools/iofflineanalysiscachecallback-offlineanalaysisreportavailabilitycallback-dword-dword-arr"><strong>оффлинеаналайсисрепортаваилабилитикаллбакк</strong></a></span><span class="sxs-lookup"><span data-stu-id="f80a4-113"><a href="/windows/desktop/direct3dtools/iofflineanalysiscachecallback-offlineanalaysisreportavailabilitycallback-dword-dword-arr"><strong>OfflineAnalaysisReportAvailabilityCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="f80a4-114">Функция обратного вызова, используемая для уведомления узла о том, какие кадры имеют доступ к автономным отчетам анализа.</span><span class="sxs-lookup"><span data-stu-id="f80a4-114">A callback function used to notify the host about which frames have offline analysis reports available.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="f80a4-115">Требования</span><span class="sxs-lookup"><span data-stu-id="f80a4-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="f80a4-116">Header</span><span class="sxs-lookup"><span data-stu-id="f80a4-116">Header</span></span></p></td><td><span data-ttu-id="f80a4-117">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="f80a4-117">Vspixengine.h</span></span></td></tr></tbody></table>

 

 

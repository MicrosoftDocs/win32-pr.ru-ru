---
description: Обратный вызов для возврата пересечения журнала пикселей (прорисовки уровня вызова) и примитивов (уровень треугольника) в двух разных результатах.
MS-HAID: vspixengine.IPixelHistoryCallback2
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Интерфейс IPixelHistoryCallback2
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 0111482E-B66A-4763-8890-85B1711F38B2
api_name:
- IPixelHistoryCallback2
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 473f3540ad9c6a16659a6e43c3aa31eef706ec59
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537322"
---
# <a name="span-idvspixengineipixelhistorycallback2spanipixelhistorycallback2-interface"></a><span data-ttu-id="4a9fc-103"><span id="vspixengine.ipixelhistorycallback2"></span>Интерфейс IPixelHistoryCallback2</span><span class="sxs-lookup"><span data-stu-id="4a9fc-103"><span id="vspixengine.ipixelhistorycallback2"></span>IPixelHistoryCallback2 interface</span></span>

<span data-ttu-id="4a9fc-104">Обратный вызов для возврата пересечения журнала пикселей (прорисовки уровня вызова) и примитивов (уровень треугольника) в двух разных результатах.</span><span class="sxs-lookup"><span data-stu-id="4a9fc-104">Callback to return pixel history intersections (draw call level) and primitives (triangle level) in two different results.</span></span>

## <a name="members"></a><span data-ttu-id="4a9fc-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="4a9fc-105">Members</span></span>

<span data-ttu-id="4a9fc-106">Интерфейс **IPixelHistoryCallback2** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="4a9fc-106">The **IPixelHistoryCallback2** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="4a9fc-107">**IPixelHistoryCallback2** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="4a9fc-107">**IPixelHistoryCallback2** also has these types of members:</span></span>

-   [<span data-ttu-id="4a9fc-108">Методы</span><span class="sxs-lookup"><span data-stu-id="4a9fc-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="4a9fc-109"><span id="methods"></span>Методы</span><span class="sxs-lookup"><span data-stu-id="4a9fc-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="4a9fc-110">Интерфейс **IPixelHistoryCallback2** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="4a9fc-110">The **IPixelHistoryCallback2** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="4a9fc-111">Метод</span><span class="sxs-lookup"><span data-stu-id="4a9fc-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="4a9fc-112">Описание</span><span class="sxs-lookup"><span data-stu-id="4a9fc-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="4a9fc-113"><a href="/windows/desktop/direct3dtools/ipixelhistorycallback2-intersectionscallback-dword-pixelhistoryintersection-arr"><strong>интерсектионскаллбакк</strong></a></span><span class="sxs-lookup"><span data-stu-id="4a9fc-113"><a href="/windows/desktop/direct3dtools/ipixelhistorycallback2-intersectionscallback-dword-pixelhistoryintersection-arr"><strong>IntersectionsCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="4a9fc-114">Обратный вызов, уведомляющий узел о размещении сведений о пересечении журнала пикселей, возвращаемых запросом связана.</span><span class="sxs-lookup"><span data-stu-id="4a9fc-114">A callback that notifies the host of pixel history intersection information returned by the assocaited request.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="4a9fc-115"><a href="/windows/desktop/direct3dtools/ipixelhistorycallback2-primitivescallback-dword-pixelhistoryoperation-arr"><strong>примитивескаллбакк</strong></a></span><span class="sxs-lookup"><span data-stu-id="4a9fc-115"><a href="/windows/desktop/direct3dtools/ipixelhistorycallback2-primitivescallback-dword-pixelhistoryoperation-arr"><strong>PrimitivesCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="4a9fc-116">Обратный вызов, уведомляющий узел о том, что сведения о операции примитива журнала пикселей возвращены связанным запросом.</span><span class="sxs-lookup"><span data-stu-id="4a9fc-116">A callback that notifies the host of pixel history primitive operation information returned by the associated request.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="4a9fc-117">Требования</span><span class="sxs-lookup"><span data-stu-id="4a9fc-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="4a9fc-118">Header</span><span class="sxs-lookup"><span data-stu-id="4a9fc-118">Header</span></span></p></td><td><span data-ttu-id="4a9fc-119">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="4a9fc-119">Vspixengine.h</span></span></td></tr></tbody></table>

 

 

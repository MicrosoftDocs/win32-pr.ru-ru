---
description: Запрос мозаичной текстуры для занесения в качестве файла DDS.
MS-HAID: vspixengine.ITileRequest
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Интерфейс Итилерекуест
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: DBA493E7-EBB6-490D-BDC6-946265A474D6
api_name:
- ITileRequest
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ceb630661cfe67bc8beb28b2d1de2480726ec594
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806251"
---
# <a name="span-idvspixengineitilerequestspanitilerequest-interface"></a><span data-ttu-id="be6f2-103"><span id="vspixengine.itilerequest"></span>Интерфейс Итилерекуест</span><span class="sxs-lookup"><span data-stu-id="be6f2-103"><span id="vspixengine.itilerequest"></span>ITileRequest interface</span></span>

<span data-ttu-id="be6f2-104">Запрос мозаичной текстуры для занесения в качестве файла DDS.</span><span class="sxs-lookup"><span data-stu-id="be6f2-104">Request for a tiled texture to be written as a DDS file.</span></span>

## <a name="members"></a><span data-ttu-id="be6f2-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="be6f2-105">Members</span></span>

<span data-ttu-id="be6f2-106">Интерфейс **итилерекуест** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="be6f2-106">The **ITileRequest** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="be6f2-107">**Итилерекуест** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="be6f2-107">**ITileRequest** also has these types of members:</span></span>

-   [<span data-ttu-id="be6f2-108">Методы</span><span class="sxs-lookup"><span data-stu-id="be6f2-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="be6f2-109"><span id="methods"></span>Методы</span><span class="sxs-lookup"><span data-stu-id="be6f2-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="be6f2-110">Интерфейс **итилерекуест** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="be6f2-110">The **ITileRequest** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="be6f2-111">Метод</span><span class="sxs-lookup"><span data-stu-id="be6f2-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="be6f2-112">Описание</span><span class="sxs-lookup"><span data-stu-id="be6f2-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="be6f2-113"><a href="/windows/desktop/direct3dtools/itilerequest-requestbuffertileasync-eventid-dword-bstr-uint-ibufferobjectdatacallback-ptr-dword-dword"><strong>рекуестбуффертилеасинк</strong></a></span><span class="sxs-lookup"><span data-stu-id="be6f2-113"><a href="/windows/desktop/direct3dtools/itilerequest-requestbuffertileasync-eventid-dword-bstr-uint-ibufferobjectdatacallback-ptr-dword-dword"><strong>RequestBufferTileAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="be6f2-114">Запросы на получение необработанного содержимого плитки.</span><span class="sxs-lookup"><span data-stu-id="be6f2-114">Requests to get the raw contents of a tile.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="be6f2-115"><a href="/windows/desktop/direct3dtools/itilerequest-requesttexturetileasync-eventid-dword-uint-uint-uint-uint-bstr-itexturecallback-ptr-dword-dword"><strong>рекуесттекстуретилеасинк</strong></a></span><span class="sxs-lookup"><span data-stu-id="be6f2-115"><a href="/windows/desktop/direct3dtools/itilerequest-requesttexturetileasync-eventid-dword-uint-uint-uint-uint-bstr-itexturecallback-ptr-dword-dword"><strong>RequestTextureTileAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="be6f2-116">Запросы на получение содержимого мозаичной текстуры в виде. Файл DDS (поверхность DirectDraw).</span><span class="sxs-lookup"><span data-stu-id="be6f2-116">Requests to get the contents of a tiled texture as a .DDS (DirectDraw Surface) file.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="be6f2-117">Требования</span><span class="sxs-lookup"><span data-stu-id="be6f2-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="be6f2-118">Header</span><span class="sxs-lookup"><span data-stu-id="be6f2-118">Header</span></span></p></td><td><span data-ttu-id="be6f2-119">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="be6f2-119">Vspixengine.h</span></span></td></tr></tbody></table>

 

 

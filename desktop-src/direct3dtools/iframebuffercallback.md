---
description: Обратный вызов для возврата целевого объекта прорисовки. Формат возвращаемого целевого объекта прорисовки — R8G8B8A8 \_ UNORM независимо от формата рендертаржет in-Engine.
MS-HAID: vspixengine.IFrameBufferCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Интерфейс Ифрамебуфферкаллбакк
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 613AD7AC-0732-49E2-8155-AE0A76597BE9
api_name:
- IFrameBufferCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 565813999cda898f693aab37b24f7979896a8497
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104422933"
---
# <a name="span-idvspixengineiframebuffercallbackspaniframebuffercallback-interface"></a><span data-ttu-id="d5009-104"><span id="vspixengine.iframebuffercallback"></span>Интерфейс Ифрамебуфферкаллбакк</span><span class="sxs-lookup"><span data-stu-id="d5009-104"><span id="vspixengine.iframebuffercallback"></span>IFrameBufferCallback interface</span></span>

<span data-ttu-id="d5009-105">Обратный вызов для возврата целевого объекта прорисовки.</span><span class="sxs-lookup"><span data-stu-id="d5009-105">Callback to return a render target.</span></span> <span data-ttu-id="d5009-106">Формат возвращаемого целевого объекта прорисовки — R8G8B8A8 \_ UNORM независимо от формата рендертаржет in-Engine.</span><span class="sxs-lookup"><span data-stu-id="d5009-106">The format of the returned render target is R8G8B8A8\_UNORM regardless of the format of the in-engine rendertarget.</span></span>

## <a name="members"></a><span data-ttu-id="d5009-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="d5009-107">Members</span></span>

<span data-ttu-id="d5009-108">Интерфейс **ифрамебуфферкаллбакк** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="d5009-108">The **IFrameBufferCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d5009-109">**Ифрамебуфферкаллбакк** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d5009-109">**IFrameBufferCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="d5009-110">Методы</span><span class="sxs-lookup"><span data-stu-id="d5009-110">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="d5009-111"><span id="methods"></span>Методы</span><span class="sxs-lookup"><span data-stu-id="d5009-111"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="d5009-112">Интерфейс **ифрамебуфферкаллбакк** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="d5009-112">The **IFrameBufferCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="d5009-113">Метод</span><span class="sxs-lookup"><span data-stu-id="d5009-113">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="d5009-114">Описание</span><span class="sxs-lookup"><span data-stu-id="d5009-114">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="d5009-115"><a href="/windows/desktop/direct3dtools/iframebuffercallback-resultcallback-dword-dword-dword-dword-double-dword-byte-arr"><strong>ресулткаллбакк</strong></a></span><span class="sxs-lookup"><span data-stu-id="d5009-115"><a href="/windows/desktop/direct3dtools/iframebuffercallback-resultcallback-dword-dword-dword-dword-double-dword-byte-arr"><strong>ResultCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="d5009-116">Обратный вызов, уведомляющий узел о буфера кадров данных, возвращаемых связанным запросом.</span><span class="sxs-lookup"><span data-stu-id="d5009-116">A callback that notifies the host of framebuffer information returned by the associated request.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="d5009-117">Требования</span><span class="sxs-lookup"><span data-stu-id="d5009-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="d5009-118">Header</span><span class="sxs-lookup"><span data-stu-id="d5009-118">Header</span></span></p></td><td><span data-ttu-id="d5009-119">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="d5009-119">Vspixengine.h</span></span></td></tr></tbody></table>

 

 

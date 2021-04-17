---
description: Обратный вызов для возврата списка событий в кадре.
MS-HAID: vspixengine.IFrameEventsCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Интерфейс Ифрамивентскаллбакк
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F40DD5DC-E78E-41F3-9D25-4D7CAE27DE45
api_name:
- IFrameEventsCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 98815681db182c99a86c05c1ea22eaad41526438
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105710616"
---
# <a name="span-idvspixengineiframeeventscallbackspaniframeeventscallback-interface"></a><span data-ttu-id="f04e2-103"><span id="vspixengine.iframeeventscallback"></span>Интерфейс Ифрамивентскаллбакк</span><span class="sxs-lookup"><span data-stu-id="f04e2-103"><span id="vspixengine.iframeeventscallback"></span>IFrameEventsCallback interface</span></span>

<span data-ttu-id="f04e2-104">Обратный вызов для возврата списка событий в кадре.</span><span class="sxs-lookup"><span data-stu-id="f04e2-104">Callback to return the list of events in a frame.</span></span>

## <a name="members"></a><span data-ttu-id="f04e2-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="f04e2-105">Members</span></span>

<span data-ttu-id="f04e2-106">Интерфейс **ифрамивентскаллбакк** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="f04e2-106">The **IFrameEventsCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f04e2-107">**Ифрамивентскаллбакк** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f04e2-107">**IFrameEventsCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="f04e2-108">Методы</span><span class="sxs-lookup"><span data-stu-id="f04e2-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="f04e2-109"><span id="methods"></span>Методы</span><span class="sxs-lookup"><span data-stu-id="f04e2-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="f04e2-110">Интерфейс **ифрамивентскаллбакк** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="f04e2-110">The **IFrameEventsCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="f04e2-111">Метод</span><span class="sxs-lookup"><span data-stu-id="f04e2-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="f04e2-112">Описание</span><span class="sxs-lookup"><span data-stu-id="f04e2-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="f04e2-113"><a href="/windows/desktop/direct3dtools/iframeeventscallback-getsupportedeventcolumns-dword-eventcolumnid-arr-bstr-arr"><strong>жетсуппортедевентколумнс</strong></a></span><span class="sxs-lookup"><span data-stu-id="f04e2-113"><a href="/windows/desktop/direct3dtools/iframeeventscallback-getsupportedeventcolumns-dword-eventcolumnid-arr-bstr-arr"><strong>GetSupportedEventColumns</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="f04e2-114">Возвращает сведения о том, какие столбцы (типы данных событий) поддерживаются списком событий.</span><span class="sxs-lookup"><span data-stu-id="f04e2-114">Gets information about which columns (types of event data) are supported by the event list.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="f04e2-115"><a href="/windows/desktop/direct3dtools/iframeeventscallback-resultcallback-dword-dword-dword-dword-variant-arr"><strong>ресулткаллбакк</strong></a></span><span class="sxs-lookup"><span data-stu-id="f04e2-115"><a href="/windows/desktop/direct3dtools/iframeeventscallback-resultcallback-dword-dword-dword-dword-variant-arr"><strong>ResultCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="f04e2-116">Функция обратного вызова, используемая для уведомления узла о событиях в списке событий.</span><span class="sxs-lookup"><span data-stu-id="f04e2-116">A callback function used to notify the host of information about events in the event list.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="f04e2-117">Требования</span><span class="sxs-lookup"><span data-stu-id="f04e2-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="f04e2-118">Header</span><span class="sxs-lookup"><span data-stu-id="f04e2-118">Header</span></span></p></td><td><span data-ttu-id="f04e2-119">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="f04e2-119">Vspixengine.h</span></span></td></tr></tbody></table>

 

 

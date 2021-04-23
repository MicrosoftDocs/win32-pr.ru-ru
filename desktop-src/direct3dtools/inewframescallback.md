---
description: Обратный вызов из обработчика, указывающий, что он завершил анализ всех новых кадров, добавленных в журнал.
MS-HAID: vspixengine.INewFramesCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Интерфейс Иневфрамескаллбакк
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A73E1EA4-F9D5-43F1-B363-20B3F7B3D8B0
api_name:
- INewFramesCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 134de14d95ceb625f1c5d4461c0b379b7f9e8a0a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104423134"
---
# <a name="span-idvspixengineinewframescallbackspaninewframescallback-interface"></a><span data-ttu-id="d165b-103"><span id="vspixengine.inewframescallback"></span>Интерфейс Иневфрамескаллбакк</span><span class="sxs-lookup"><span data-stu-id="d165b-103"><span id="vspixengine.inewframescallback"></span>INewFramesCallback interface</span></span>

<span data-ttu-id="d165b-104">Обратный вызов из обработчика, указывающий, что он завершил анализ всех новых кадров, добавленных в журнал.</span><span class="sxs-lookup"><span data-stu-id="d165b-104">Callback from engine indicating that it is done parsing any new frames added to the log.</span></span>

## <a name="members"></a><span data-ttu-id="d165b-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="d165b-105">Members</span></span>

<span data-ttu-id="d165b-106">Интерфейс **иневфрамескаллбакк** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="d165b-106">The **INewFramesCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d165b-107">**Иневфрамескаллбакк** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d165b-107">**INewFramesCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="d165b-108">Методы</span><span class="sxs-lookup"><span data-stu-id="d165b-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="d165b-109"><span id="methods"></span>Методы</span><span class="sxs-lookup"><span data-stu-id="d165b-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="d165b-110">Интерфейс **иневфрамескаллбакк** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="d165b-110">The **INewFramesCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="d165b-111">Метод</span><span class="sxs-lookup"><span data-stu-id="d165b-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="d165b-112">Описание</span><span class="sxs-lookup"><span data-stu-id="d165b-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="d165b-113"><a href="/windows/desktop/direct3dtools/inewframescallback-cancelall"><strong>канцелалл</strong></a></span><span class="sxs-lookup"><span data-stu-id="d165b-113"><a href="/windows/desktop/direct3dtools/inewframescallback-cancelall"><strong>CancelAll</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="d165b-114">Обратный вызов, уведомляющий узел о том, что все запросы отменены.</span><span class="sxs-lookup"><span data-stu-id="d165b-114">A callback that notifies the host that all requests have been cancelled.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="d165b-115"><a href="/windows/desktop/direct3dtools/inewframescallback-cancelusingcallback-iunknown-ptr"><strong>канцелусингкаллбакк</strong></a></span><span class="sxs-lookup"><span data-stu-id="d165b-115"><a href="/windows/desktop/direct3dtools/inewframescallback-cancelusingcallback-iunknown-ptr"><strong>CancelUsingCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="d165b-116">Обратный вызов, уведомляющий узел об отмене запроса.</span><span class="sxs-lookup"><span data-stu-id="d165b-116">A callback that notifies the host of a canceled request.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="d165b-117"><a href="/windows/desktop/direct3dtools/inewframescallback-cancelusingcookie-dword"><strong>канцелусингкукие</strong></a></span><span class="sxs-lookup"><span data-stu-id="d165b-117"><a href="/windows/desktop/direct3dtools/inewframescallback-cancelusingcookie-dword"><strong>CancelUsingCookie</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="d165b-118">Обратный вызов, уведомляющий узел об отмене запроса с помощью файла cookie, уникально идентифицирующего запрос.</span><span class="sxs-lookup"><span data-stu-id="d165b-118">A callback that notifies the host of a canceled request by using a cookie that uniquely identifies the request.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="d165b-119"><a href="/windows/desktop/direct3dtools/inewframescallback-newframesavailable"><strong>невфрамесаваилабле</strong></a></span><span class="sxs-lookup"><span data-stu-id="d165b-119"><a href="/windows/desktop/direct3dtools/inewframescallback-newframesavailable"><strong>NewFramesAvailable</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="d165b-120">Обратный вызов, уведомляющий основное приложение о том, что новые кадры доступны для обработки.</span><span class="sxs-lookup"><span data-stu-id="d165b-120">A callback that notifies the host that new frames are available to be processed.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="d165b-121">Требования</span><span class="sxs-lookup"><span data-stu-id="d165b-121">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="d165b-122">Header</span><span class="sxs-lookup"><span data-stu-id="d165b-122">Header</span></span></p></td><td><span data-ttu-id="d165b-123">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="d165b-123">Vspixengine.h</span></span></td></tr></tbody></table>

 

 

---
description: Расширения для исходного интерфейса Ипиксенгине.
MS-HAID: vspixengine.IPixEngine2
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Интерфейс IPixEngine2
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: D650FB4C-C332-4E2E-85EB-DDCE3DA87B0C
api_name:
- IPixEngine2
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bf8fe4537a6f4c8703482289302ffa8f3a645903
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494694"
---
# <a name="span-idvspixengineipixengine2spanipixengine2-interface"></a><span data-ttu-id="ec1e3-103"><span id="vspixengine.ipixengine2"></span>Интерфейс IPixEngine2</span><span class="sxs-lookup"><span data-stu-id="ec1e3-103"><span id="vspixengine.ipixengine2"></span>IPixEngine2 interface</span></span>

<span data-ttu-id="ec1e3-104">Расширения для исходного интерфейса Ипиксенгине.</span><span class="sxs-lookup"><span data-stu-id="ec1e3-104">Extensions to the original IPixEngine interface.</span></span>

## <a name="members"></a><span data-ttu-id="ec1e3-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="ec1e3-105">Members</span></span>

<span data-ttu-id="ec1e3-106">Интерфейс **IPixEngine2** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="ec1e3-106">The **IPixEngine2** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="ec1e3-107">**IPixEngine2** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ec1e3-107">**IPixEngine2** also has these types of members:</span></span>

-   [<span data-ttu-id="ec1e3-108">Методы</span><span class="sxs-lookup"><span data-stu-id="ec1e3-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="ec1e3-109"><span id="methods"></span>Методы</span><span class="sxs-lookup"><span data-stu-id="ec1e3-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="ec1e3-110">Интерфейс **IPixEngine2** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="ec1e3-110">The **IPixEngine2** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="ec1e3-111">Метод</span><span class="sxs-lookup"><span data-stu-id="ec1e3-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="ec1e3-112">Описание</span><span class="sxs-lookup"><span data-stu-id="ec1e3-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="ec1e3-113"><a href="/windows/desktop/direct3dtools/ipixengine2-endexperiment-bstr-ifileiocallback-ptr"><strong>ендексперимент</strong></a></span><span class="sxs-lookup"><span data-stu-id="ec1e3-113"><a href="/windows/desktop/direct3dtools/ipixengine2-endexperiment-bstr-ifileiocallback-ptr"><strong>EndExperiment</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="ec1e3-114">Завершает експериемент и завершает работу с журналом графики.</span><span class="sxs-lookup"><span data-stu-id="ec1e3-114">Ends the experiement and completes the graphics log.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="ec1e3-115"><a href="/windows/desktop/direct3dtools/ipixengine2-getplaybackmachine-bstr-bool-ptr-bstr-ptr"><strong>жетплайбаккмачине</strong></a></span><span class="sxs-lookup"><span data-stu-id="ec1e3-115"><a href="/windows/desktop/direct3dtools/ipixengine2-getplaybackmachine-bstr-bool-ptr-bstr-ptr"><strong>GetPlaybackMachine</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="ec1e3-116">Возвращает сведения о текущем компьютере воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="ec1e3-116">Gets information about the current playback machine.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="ec1e3-117"><a href="/windows/desktop/direct3dtools/ipixengine2-onnewdataavailable-bool-bool-int64-int64-int32-byte-arr"><strong>онневдатааваилабле</strong></a></span><span class="sxs-lookup"><span data-stu-id="ec1e3-117"><a href="/windows/desktop/direct3dtools/ipixengine2-onnewdataavailable-bool-bool-int64-int64-int32-byte-arr"><strong>OnNewDataAvailable</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="ec1e3-118">Запросы, указывающие, что в журнале графики есть новые данные.</span><span class="sxs-lookup"><span data-stu-id="ec1e3-118">Requests to indicate that the graphics log has new data inside of it.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="ec1e3-119"><a href="/windows/desktop/direct3dtools/ipixengine2-setplaybackmachine-bstr-bool-bstr"><strong>сетплайбаккмачине</strong></a></span><span class="sxs-lookup"><span data-stu-id="ec1e3-119"><a href="/windows/desktop/direct3dtools/ipixengine2-setplaybackmachine-bstr-bool-bstr"><strong>SetPlaybackMachine</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="ec1e3-120">Задает текущий компьютер воспроизведения для указанного журнала графики.</span><span class="sxs-lookup"><span data-stu-id="ec1e3-120">Sets the current playback machine for the specified graphics log.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="ec1e3-121">Требования</span><span class="sxs-lookup"><span data-stu-id="ec1e3-121">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="ec1e3-122">Header</span><span class="sxs-lookup"><span data-stu-id="ec1e3-122">Header</span></span></p></td><td><span data-ttu-id="ec1e3-123">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="ec1e3-123">Vspixengine.h</span></span></td></tr></tbody></table>

 

 

---
description: Исходный интерфейс для обмена данными о vsglog.
MS-HAID: vspixengine.IPixEngine
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Интерфейс Ипиксенгине
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 87AB1D07-8E90-49F0-B44D-F6185923B8D4
api_name:
- IPixEngine
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2f02538f7acbd88daf166af657382e507a4e5661
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495735"
---
# <a name="span-idvspixengineipixenginespanipixengine-interface"></a><span data-ttu-id="6ffc5-103"><span id="vspixengine.ipixengine"></span>Интерфейс Ипиксенгине</span><span class="sxs-lookup"><span data-stu-id="6ffc5-103"><span id="vspixengine.ipixengine"></span>IPixEngine interface</span></span>

<span data-ttu-id="6ffc5-104">Исходный интерфейс для обмена данными о vsglog.</span><span class="sxs-lookup"><span data-stu-id="6ffc5-104">Original interface for communicating data about a vsglog .</span></span>

## <a name="members"></a><span data-ttu-id="6ffc5-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="6ffc5-105">Members</span></span>

<span data-ttu-id="6ffc5-106">Интерфейс **ипиксенгине** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="6ffc5-106">The **IPixEngine** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="6ffc5-107">**Ипиксенгине** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="6ffc5-107">**IPixEngine** also has these types of members:</span></span>

-   [<span data-ttu-id="6ffc5-108">Методы</span><span class="sxs-lookup"><span data-stu-id="6ffc5-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="6ffc5-109"><span id="methods"></span>Методы</span><span class="sxs-lookup"><span data-stu-id="6ffc5-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="6ffc5-110">Интерфейс **ипиксенгине** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="6ffc5-110">The **IPixEngine** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="6ffc5-111">Метод</span><span class="sxs-lookup"><span data-stu-id="6ffc5-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="6ffc5-112">Описание</span><span class="sxs-lookup"><span data-stu-id="6ffc5-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="6ffc5-113"><a href="/windows/desktop/direct3dtools/ipixengine-openfile-bstr-bstr-inewframescallback-ptr-ifileiocallback-ptr-lcid"><strong>OpenFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="6ffc5-113"><a href="/windows/desktop/direct3dtools/ipixengine-openfile-bstr-bstr-inewframescallback-ptr-ifileiocallback-ptr-lcid"><strong>OpenFile</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="6ffc5-114">Открывает журнал графики.</span><span class="sxs-lookup"><span data-stu-id="6ffc5-114">Opens a graphics log.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="6ffc5-115"><a href="/windows/desktop/direct3dtools/ipixengine-runexperiment-experiment-irunexperimentcallback-ptr-inewframescallback-ptr-ifileiocallback-ptr-dword-experimenttrigger-arr"><strong>рунексперимент</strong></a></span><span class="sxs-lookup"><span data-stu-id="6ffc5-115"><a href="/windows/desktop/direct3dtools/ipixengine-runexperiment-experiment-irunexperimentcallback-ptr-inewframescallback-ptr-ifileiocallback-ptr-dword-experimenttrigger-arr"><strong>RunExperiment</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="6ffc5-116">Выполняет эксперимент.</span><span class="sxs-lookup"><span data-stu-id="6ffc5-116">Runs an experiment.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="6ffc5-117"><a href="/windows/desktop/direct3dtools/ipixengine-savefile-bstr-ifileiocallback-ptr"><strong>SaveFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="6ffc5-117"><a href="/windows/desktop/direct3dtools/ipixengine-savefile-bstr-ifileiocallback-ptr"><strong>SaveFile</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="6ffc5-118">Сохраняет журнал графики в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="6ffc5-118">Saves the graphics log to the specified location.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="6ffc5-119"><a href="/windows/desktop/direct3dtools/ipixengine-setparentprocess-dword"><strong>сетпарентпроцесс</strong></a></span><span class="sxs-lookup"><span data-stu-id="6ffc5-119"><a href="/windows/desktop/direct3dtools/ipixengine-setparentprocess-dword"><strong>SetParentProcess</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="6ffc5-120">Не используется.</span><span class="sxs-lookup"><span data-stu-id="6ffc5-120">Not used.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="6ffc5-121"><a href="/windows/desktop/direct3dtools/ipixengine-shutdown"><strong>Закрытия</strong></a></span><span class="sxs-lookup"><span data-stu-id="6ffc5-121"><a href="/windows/desktop/direct3dtools/ipixengine-shutdown"><strong>ShutDown</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="6ffc5-122">Завершает работу подсистемы.</span><span class="sxs-lookup"><span data-stu-id="6ffc5-122">Shuts down the engine.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="6ffc5-123">Требования</span><span class="sxs-lookup"><span data-stu-id="6ffc5-123">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="6ffc5-124">Header</span><span class="sxs-lookup"><span data-stu-id="6ffc5-124">Header</span></span></p></td><td><span data-ttu-id="6ffc5-125">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="6ffc5-125">Vspixengine.h</span></span></td></tr></tbody></table>

 

 

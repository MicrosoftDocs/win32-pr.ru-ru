---
description: Обратный вызов обработчика для обработки ошибок.
MS-HAID: vspixengine.IPixErrorCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Интерфейс Ипиксерроркаллбакк
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2FEAB4CF-80C8-4A3F-9D62-DFBAB34DE8C8
api_name:
- IPixErrorCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: df9e34f83f3cdd4c8c36024cf0d4ed042da0070f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104416553"
---
# <a name="span-idvspixengineipixerrorcallbackspanipixerrorcallback-interface"></a><span data-ttu-id="ad002-103"><span id="vspixengine.ipixerrorcallback"></span>Интерфейс Ипиксерроркаллбакк</span><span class="sxs-lookup"><span data-stu-id="ad002-103"><span id="vspixengine.ipixerrorcallback"></span>IPixErrorCallback interface</span></span>

<span data-ttu-id="ad002-104">Обратный вызов обработчика для обработки ошибок.</span><span class="sxs-lookup"><span data-stu-id="ad002-104">Callback from engine to handle errors.</span></span>

## <a name="members"></a><span data-ttu-id="ad002-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="ad002-105">Members</span></span>

<span data-ttu-id="ad002-106">Интерфейс **ипиксерроркаллбакк** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="ad002-106">The **IPixErrorCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="ad002-107">**Ипиксерроркаллбакк** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ad002-107">**IPixErrorCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="ad002-108">Методы</span><span class="sxs-lookup"><span data-stu-id="ad002-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="ad002-109"><span id="methods"></span>Методы</span><span class="sxs-lookup"><span data-stu-id="ad002-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="ad002-110">Интерфейс **ипиксерроркаллбакк** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="ad002-110">The **IPixErrorCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="ad002-111">Метод</span><span class="sxs-lookup"><span data-stu-id="ad002-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="ad002-112">Описание</span><span class="sxs-lookup"><span data-stu-id="ad002-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="ad002-113"><a href="/windows/desktop/direct3dtools/ipixerrorcallback-errorlistcallback-dword-issue-arr-dword-issue-arr"><strong>еррорлисткаллбакк</strong></a></span><span class="sxs-lookup"><span data-stu-id="ad002-113"><a href="/windows/desktop/direct3dtools/ipixerrorcallback-errorlistcallback-dword-issue-arr-dword-issue-arr"><strong>ErrorListCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="ad002-114">Обратный вызов, уведомляющий основное приложение об ошибках, возвращенных связанным запросом.</span><span class="sxs-lookup"><span data-stu-id="ad002-114">A callback that notifies the host of errors returned by the associated request.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="ad002-115"><a href="/windows/desktop/direct3dtools/ipixerrorcallback-messagescallback-dword-issue-arr"><strong>мессажескаллбакк</strong></a></span><span class="sxs-lookup"><span data-stu-id="ad002-115"><a href="/windows/desktop/direct3dtools/ipixerrorcallback-messagescallback-dword-issue-arr"><strong>MessagesCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="ad002-116">Обратный вызов, уведомляющий узел о сообщениях, возвращенных связанным запросом.</span><span class="sxs-lookup"><span data-stu-id="ad002-116">A callback that notifies the host of messages returned by the associated request.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="ad002-117"><a href="/windows/desktop/direct3dtools/ipixerrorcallback-warninglistcallback"><strong>варнинглисткаллбакк</strong></a></span><span class="sxs-lookup"><span data-stu-id="ad002-117"><a href="/windows/desktop/direct3dtools/ipixerrorcallback-warninglistcallback"><strong>WarningListCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="ad002-118">Обратный вызов, уведомляющий узел о предупреждениях, возвращаемых связанным запросом.</span><span class="sxs-lookup"><span data-stu-id="ad002-118">A callback that notifies the host of warnings returned by the associated request.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="ad002-119">Требования</span><span class="sxs-lookup"><span data-stu-id="ad002-119">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="ad002-120">Header</span><span class="sxs-lookup"><span data-stu-id="ad002-120">Header</span></span></p></td><td><span data-ttu-id="ad002-121">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="ad002-121">Vspixengine.h</span></span></td></tr></tbody></table>

 

 

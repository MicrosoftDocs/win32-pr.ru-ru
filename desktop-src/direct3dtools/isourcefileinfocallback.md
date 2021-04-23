---
description: Обратный вызов для возврата сведений о исходном файле из стека вызовов.
MS-HAID: vspixengine.ISourceFileInfoCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Интерфейс Исаурцефилеинфокаллбакк
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 0430DFF0-F3EA-4645-9B91-E849C0F99609
api_name:
- ISourceFileInfoCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6c627d07bfbf455a9c62a922f62adcab945d5741
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806838"
---
# <a name="span-idvspixengineisourcefileinfocallbackspanisourcefileinfocallback-interface"></a><span data-ttu-id="136f7-103"><span id="vspixengine.isourcefileinfocallback"></span>Интерфейс Исаурцефилеинфокаллбакк</span><span class="sxs-lookup"><span data-stu-id="136f7-103"><span id="vspixengine.isourcefileinfocallback"></span>ISourceFileInfoCallback interface</span></span>

<span data-ttu-id="136f7-104">Обратный вызов для возврата сведений о исходном файле из стека вызовов.</span><span class="sxs-lookup"><span data-stu-id="136f7-104">Callback to return source file info from a callstack.</span></span>

## <a name="members"></a><span data-ttu-id="136f7-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="136f7-105">Members</span></span>

<span data-ttu-id="136f7-106">Интерфейс **исаурцефилеинфокаллбакк** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="136f7-106">The **ISourceFileInfoCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="136f7-107">**Исаурцефилеинфокаллбакк** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="136f7-107">**ISourceFileInfoCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="136f7-108">Методы</span><span class="sxs-lookup"><span data-stu-id="136f7-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="136f7-109"><span id="methods"></span>Методы</span><span class="sxs-lookup"><span data-stu-id="136f7-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="136f7-110">Интерфейс **исаурцефилеинфокаллбакк** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="136f7-110">The **ISourceFileInfoCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="136f7-111">Метод</span><span class="sxs-lookup"><span data-stu-id="136f7-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="136f7-112">Описание</span><span class="sxs-lookup"><span data-stu-id="136f7-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="136f7-113"><a href="/windows/desktop/direct3dtools/isourcefileinfocallback-resultcallback-dword-sourcefileinfo-arr"><strong>ресулткаллбакк</strong></a></span><span class="sxs-lookup"><span data-stu-id="136f7-113"><a href="/windows/desktop/direct3dtools/isourcefileinfocallback-resultcallback-dword-sourcefileinfo-arr"><strong>ResultCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="136f7-114">Функция обратного вызова, используемая для уведомления узла о файлах исходного кода, связанных с стеком вызовов.</span><span class="sxs-lookup"><span data-stu-id="136f7-114">A callback function used to notify the host of information about source files associated with the callstack.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="136f7-115">Требования</span><span class="sxs-lookup"><span data-stu-id="136f7-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="136f7-116">Header</span><span class="sxs-lookup"><span data-stu-id="136f7-116">Header</span></span></p></td><td><span data-ttu-id="136f7-117">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="136f7-117">Vspixengine.h</span></span></td></tr></tbody></table>

 

 

---
description: Обратный вызов для возврата инструкций, созданных при создании трассировки шейдера.
MS-HAID: vspixengine.IDebugShaderCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Интерфейс Идебугшадеркаллбакк
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9A4A3FD3-15E5-4DB5-8777-55797E32ABA3
api_name:
- IDebugShaderCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 676d76a0dbc199880badebc904a4eb66d2ad4d0e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105701118"
---
# <a name="span-idvspixengineidebugshadercallbackspanidebugshadercallback-interface"></a><span data-ttu-id="8802b-103"><span id="vspixengine.idebugshadercallback"></span>Интерфейс Идебугшадеркаллбакк</span><span class="sxs-lookup"><span data-stu-id="8802b-103"><span id="vspixengine.idebugshadercallback"></span>IDebugShaderCallback interface</span></span>

<span data-ttu-id="8802b-104">Обратный вызов для возврата инструкций, созданных при создании трассировки шейдера.</span><span class="sxs-lookup"><span data-stu-id="8802b-104">Callback to return the instructions generated from creating a shader trace.</span></span>

## <a name="members"></a><span data-ttu-id="8802b-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="8802b-105">Members</span></span>

<span data-ttu-id="8802b-106">Интерфейс **идебугшадеркаллбакк** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="8802b-106">The **IDebugShaderCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="8802b-107">**Идебугшадеркаллбакк** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="8802b-107">**IDebugShaderCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="8802b-108">Методы</span><span class="sxs-lookup"><span data-stu-id="8802b-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="8802b-109"><span id="methods"></span>Методы</span><span class="sxs-lookup"><span data-stu-id="8802b-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="8802b-110">Интерфейс **идебугшадеркаллбакк** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="8802b-110">The **IDebugShaderCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="8802b-111">Метод</span><span class="sxs-lookup"><span data-stu-id="8802b-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="8802b-112">Описание</span><span class="sxs-lookup"><span data-stu-id="8802b-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="8802b-113"><a href="/windows/desktop/direct3dtools/idebugshadercallback-resultinstructions-dword-byte-arr"><strong>ресултинструктионс</strong></a></span><span class="sxs-lookup"><span data-stu-id="8802b-113"><a href="/windows/desktop/direct3dtools/idebugshadercallback-resultinstructions-dword-byte-arr"><strong>ResultInstructions</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="8802b-114">Обратный вызов, уведомляющий узел о инструктрион данных, возвращаемых связанным запросом.</span><span class="sxs-lookup"><span data-stu-id="8802b-114">A callback that notifies the host of instructrion information returned by the associated request.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="8802b-115">Требования</span><span class="sxs-lookup"><span data-stu-id="8802b-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="8802b-116">Header</span><span class="sxs-lookup"><span data-stu-id="8802b-116">Header</span></span></p></td><td><span data-ttu-id="8802b-117">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="8802b-117">Vspixengine.h</span></span></td></tr></tbody></table>

 

 

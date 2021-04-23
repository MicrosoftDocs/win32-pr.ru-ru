---
title: Справочник по функциям поддержки
description: В диспетчере маршрутизаторов предоставляются следующие функции для маршрутизации протоколов.
ms.assetid: 4e88c9fe-f6ec-4f9c-88b1-8726e10d0f6d
keywords:
- Интерфейс протокола маршрутизации RRAS, функции поддержки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbbaba49c5f7e4130491a50176d560ee565b0046
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488069"
---
# <a name="support-functions-reference"></a><span data-ttu-id="ceb1f-104">Справочник по функциям поддержки</span><span class="sxs-lookup"><span data-stu-id="ceb1f-104">Support Functions Reference</span></span>

<span data-ttu-id="ceb1f-105">В диспетчере маршрутизаторов предоставляются следующие функции для маршрутизации протоколов.</span><span class="sxs-lookup"><span data-stu-id="ceb1f-105">The following functions are provided to routing protocols by the router manager.</span></span> <span data-ttu-id="ceb1f-106">Когда диспетчер маршрутизатора вызывает функцию [**стартпротокол**](/windows/desktop/api/Routprot/nc-routprot-pstart_protocol) (реализованную протоколом маршрутизации), диспетчер маршрутизатора передает в протокол маршрутизации структуру [**\_ функций поддержки**](/windows/desktop/api/Routprot/ns-routprot-support_functions_50) , содержащую указатели на эти функции:</span><span class="sxs-lookup"><span data-stu-id="ceb1f-106">When the router manager calls the [**StartProtocol**](/windows/desktop/api/Routprot/nc-routprot-pstart_protocol) function (implemented by the routing protocol), the router manager passes the routing protocol a [**SUPPORT\_FUNCTIONS**](/windows/desktop/api/Routprot/ns-routprot-support_functions_50) structure containing pointers to these functions:</span></span>

<span data-ttu-id="ceb1f-107">[**деманддиалрекуест**](/previous-versions/windows/desktop/legacy/aa373924(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ceb1f-107">[**DemandDialRequest**](/previous-versions/windows/desktop/legacy/aa373924(v=vs.85))</span></span>

<span data-ttu-id="ceb1f-108">[**мибентрикреате**](/previous-versions/windows/desktop/legacy/aa374538(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ceb1f-108">[**MIBEntryCreate**](/previous-versions/windows/desktop/legacy/aa374538(v=vs.85))</span></span>

<span data-ttu-id="ceb1f-109">[**мибентриделете**](/previous-versions/windows/desktop/legacy/aa374539(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ceb1f-109">[**MIBEntryDelete**](/previous-versions/windows/desktop/legacy/aa374539(v=vs.85))</span></span>

<span data-ttu-id="ceb1f-110">[**мибентрижет**](/previous-versions/windows/desktop/legacy/aa374540(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ceb1f-110">[**MIBEntryGet**](/previous-versions/windows/desktop/legacy/aa374540(v=vs.85))</span></span>

<span data-ttu-id="ceb1f-111">[**мибентрижетфирст**](/previous-versions/windows/desktop/legacy/aa374541(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ceb1f-111">[**MIBEntryGetFirst**](/previous-versions/windows/desktop/legacy/aa374541(v=vs.85))</span></span>

<span data-ttu-id="ceb1f-112">[**мибентрижетнекст**](/previous-versions/windows/desktop/legacy/aa374542(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ceb1f-112">[**MIBEntryGetNext**](/previous-versions/windows/desktop/legacy/aa374542(v=vs.85))</span></span>

<span data-ttu-id="ceb1f-113">[**мибентрисет**](/previous-versions/windows/desktop/legacy/aa374543(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ceb1f-113">[**MIBEntrySet**](/previous-versions/windows/desktop/legacy/aa374543(v=vs.85))</span></span>

<span data-ttu-id="ceb1f-114">[**сетинтерфацерецеиветипе**](/previous-versions/windows/desktop/legacy/aa382181(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ceb1f-114">[**SetInterfaceReceiveType**](/previous-versions/windows/desktop/legacy/aa382181(v=vs.85))</span></span>

<span data-ttu-id="ceb1f-115">[**валидатерауте**](/previous-versions/windows/desktop/legacy/aa382342(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ceb1f-115">[**ValidateRoute**](/previous-versions/windows/desktop/legacy/aa382342(v=vs.85))</span></span>

 

 
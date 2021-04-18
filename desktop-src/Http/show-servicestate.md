---
title: show servicestate
description: Показывает моментальный снимок службы HTTP.
ms.assetid: a50a3ef5-5e62-412e-a443-11d453778f70
keywords:
- показывать servicestate HTTP
topic_type:
- apiref
api_name:
- show servicestate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f79bfdb946d286c31ce284efa09e75ad93c34438
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2019
ms.locfileid: "105681570"
---
# <a name="show-servicestate"></a><span data-ttu-id="33949-104">show servicestate</span><span class="sxs-lookup"><span data-stu-id="33949-104">show servicestate</span></span>

<span data-ttu-id="33949-105">Показывает моментальный снимок службы HTTP.</span><span class="sxs-lookup"><span data-stu-id="33949-105">Shows a snapshot of the HTTP service.</span></span>

``` syntax
show servicestate [[view=]{session|requestq}] [[verbose=]{yes|no}]
 
```

## <a name="parameters"></a><span data-ttu-id="33949-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="33949-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33949-107"><span id="__view___session_requestq__"></span><span id="__VIEW___SESSION_REQUESTQ__"></span>**\[\[представление = \] {Session \| рекуестк}\]**</span><span class="sxs-lookup"><span data-stu-id="33949-107"><span id="__view___session_requestq__"></span><span id="__VIEW___SESSION_REQUESTQ__"></span>**\[\[view=\]{session\|requestq}\]**</span></span>
</dt> <dd>

<span data-ttu-id="33949-108">Просмотр моментального снимка состояния службы HTTP на основе сеанса сервера или очередей запросов.</span><span class="sxs-lookup"><span data-stu-id="33949-108">View snapshot of HTTP service state based on server session or request queues.</span></span>

</dd> <dt>

<span data-ttu-id="33949-109"><span id="__verbose___yes_no__"></span><span id="__VERBOSE___YES_NO__"></span>**\[\[verbose = \] {Да \| нет}\]**</span><span class="sxs-lookup"><span data-stu-id="33949-109"><span id="__verbose___yes_no__"></span><span id="__VERBOSE___YES_NO__"></span>**\[\[verbose=\]{yes\|no}\]**</span></span>
</dt> <dd>

<span data-ttu-id="33949-110">Просмотрите подробную информацию, в которой отображаются сведения о свойствах.</span><span class="sxs-lookup"><span data-stu-id="33949-110">View verbose information showing property information too.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="33949-111">Примеры</span><span class="sxs-lookup"><span data-stu-id="33949-111">Examples</span></span>

<span data-ttu-id="33949-112">**Показать servicestate представление = сеанс**</span><span class="sxs-lookup"><span data-stu-id="33949-112">**show servicestate view=session**</span></span>

<span data-ttu-id="33949-113">**Показать servicestateное представление = рекуестк verbose = Yes**</span><span class="sxs-lookup"><span data-stu-id="33949-113">**show servicestate view=requestq verbose=yes**</span></span>

 

 





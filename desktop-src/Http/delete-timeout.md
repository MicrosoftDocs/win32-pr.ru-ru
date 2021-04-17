---
title: delete timeout
description: Удаляет глобальное время ожидания, после чего служба HTTP.sys возвращает значения по умолчанию.
ms.assetid: 5fcd5df4-023e-486d-b41a-639e210a128f
keywords:
- Удаление HTTP timeout
topic_type:
- apiref
api_name:
- delete timeout
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6ee436e1eb7f545a74aa56f6c146afbd1c57066
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2019
ms.locfileid: "105661671"
---
# <a name="delete-timeout"></a><span data-ttu-id="0a017-104">delete timeout</span><span class="sxs-lookup"><span data-stu-id="0a017-104">delete timeout</span></span>

<span data-ttu-id="0a017-105">Удаляет глобальное время ожидания, после чего служба HTTP.sys возвращает значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0a017-105">Deletes a global timeout and makes the HTTP.sys service revert to default values.</span></span>

``` syntax
delete timeout [timeouttype=]{idleconnectiontimeout|headerwaittimeout}
 
```

## <a name="parameters"></a><span data-ttu-id="0a017-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0a017-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a017-107"><span id="_timeouttype___idleconnectiontimeout_headerwaittimeout_"></span><span id="_TIMEOUTTYPE___IDLECONNECTIONTIMEOUT_HEADERWAITTIMEOUT_"></span>**\[тимеауттипе = \] {idleconnectiontimeout \| хеадерваиттимеаут}**</span><span class="sxs-lookup"><span data-stu-id="0a017-107"><span id="_timeouttype___idleconnectiontimeout_headerwaittimeout_"></span><span id="_TIMEOUTTYPE___IDLECONNECTIONTIMEOUT_HEADERWAITTIMEOUT_"></span>**\[timeouttype=\]{idleconnectiontimeout\|headerwaittimeout}**</span></span>
</dt> <dd>

<span data-ttu-id="0a017-108">Указывает тип параметра времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="0a017-108">Specifies the type of timeout setting.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="0a017-109">Примеры</span><span class="sxs-lookup"><span data-stu-id="0a017-109">Examples</span></span>

<span data-ttu-id="0a017-110">**delete timeout timeouttype=idleconnectiontimeout**</span><span class="sxs-lookup"><span data-stu-id="0a017-110">**delete timeout timeouttype=idleconnectiontimeout**</span></span>

<span data-ttu-id="0a017-111">**delete timeout timeouttype=headerwaittimeout**</span><span class="sxs-lookup"><span data-stu-id="0a017-111">**delete timeout timeouttype=headerwaittimeout**</span></span>

 

 





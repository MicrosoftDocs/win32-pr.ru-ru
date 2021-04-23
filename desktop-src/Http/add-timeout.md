---
title: add timeout
description: Добавляет глобальное время ожидания в службу HTTP.sys.
ms.assetid: c59a64e2-36aa-4428-b727-df21f5632d0d
keywords:
- Добавление HTTP timeout
topic_type:
- apiref
api_name:
- add timeout
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2637cb5db663ea36b15eb382a16b02b166e98f88
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2019
ms.locfileid: "104412034"
---
# <a name="add-timeout"></a><span data-ttu-id="c6b43-104">add timeout</span><span class="sxs-lookup"><span data-stu-id="c6b43-104">add timeout</span></span>

<span data-ttu-id="c6b43-105">Добавляет глобальное время ожидания в службу HTTP.sys.</span><span class="sxs-lookup"><span data-stu-id="c6b43-105">Adds a global timeout to the HTTP.sys service.</span></span>

``` syntax
add timeout [timeouttype=]{idleconnectiontimeout|headerwaittimeout}
            [value=]u-short

 
```

## <a name="parameters"></a><span data-ttu-id="c6b43-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c6b43-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6b43-107"><span id="_timeouttype___idleconnectiontimeout_headerwaittimeout_"></span><span id="_TIMEOUTTYPE___IDLECONNECTIONTIMEOUT_HEADERWAITTIMEOUT_"></span>**\[тимеауттипе = \] {idleconnectiontimeout \| хеадерваиттимеаут}**</span><span class="sxs-lookup"><span data-stu-id="c6b43-107"><span id="_timeouttype___idleconnectiontimeout_headerwaittimeout_"></span><span id="_TIMEOUTTYPE___IDLECONNECTIONTIMEOUT_HEADERWAITTIMEOUT_"></span>**\[timeouttype=\]{idleconnectiontimeout\|headerwaittimeout}**</span></span>
</dt> <dd>

<span data-ttu-id="c6b43-108">Указывает тип времени ожидания для параметра.</span><span class="sxs-lookup"><span data-stu-id="c6b43-108">Specifies the type of timeout for setting.</span></span>

</dd> <dt>

<span data-ttu-id="c6b43-109"><span id="_value__u-short"></span><span id="_VALUE__U-SHORT"></span>\**\[значение = \] \* \* \* u-Short*</span><span class="sxs-lookup"><span data-stu-id="c6b43-109"><span id="_value__u-short"></span><span id="_VALUE__U-SHORT"></span>\**\[value=\]\*\*\*u-short*</span></span>
</dt> <dd>

<span data-ttu-id="c6b43-110">Задает значение времени ожидания (в секундах).</span><span class="sxs-lookup"><span data-stu-id="c6b43-110">Specifies the value of the timeout (in seconds).</span></span> <span data-ttu-id="c6b43-111">Если значение является шестнадцатеричным, добавьте префикс 0x.</span><span class="sxs-lookup"><span data-stu-id="c6b43-111">If value is hexadecimal, then add the prefix 0x.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="c6b43-112">Примеры</span><span class="sxs-lookup"><span data-stu-id="c6b43-112">Examples</span></span>

<span data-ttu-id="c6b43-113">**add timeout timeouttype=idleconnectiontimeout value=120**</span><span class="sxs-lookup"><span data-stu-id="c6b43-113">**add timeout timeouttype=idleconnectiontimeout value=120**</span></span>

<span data-ttu-id="c6b43-114">**add timeout timeouttype=headerwaittimeout value=0x40**</span><span class="sxs-lookup"><span data-stu-id="c6b43-114">**add timeout timeouttype=headerwaittimeout value=0x40**</span></span>

 

 





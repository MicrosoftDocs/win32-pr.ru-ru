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
# <a name="add-timeout"></a>add timeout

Добавляет глобальное время ожидания в службу HTTP.sys.

``` syntax
add timeout [timeouttype=]{idleconnectiontimeout|headerwaittimeout}
            [value=]u-short

 
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="_timeouttype___idleconnectiontimeout_headerwaittimeout_"></span><span id="_TIMEOUTTYPE___IDLECONNECTIONTIMEOUT_HEADERWAITTIMEOUT_"></span>**\[тимеауттипе = \] {idleconnectiontimeout \| хеадерваиттимеаут}**
</dt> <dd>

Указывает тип времени ожидания для параметра.

</dd> <dt>

<span id="_value__u-short"></span><span id="_VALUE__U-SHORT"></span>**\[значение = \] * * * u-Short*
</dt> <dd>

Задает значение времени ожидания (в секундах). Если значение является шестнадцатеричным, добавьте префикс 0x.

</dd> </dl>

## <a name="examples"></a>Примеры

**add timeout timeouttype=idleconnectiontimeout value=120**

**add timeout timeouttype=headerwaittimeout value=0x40**

 

 





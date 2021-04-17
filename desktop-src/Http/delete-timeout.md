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
# <a name="delete-timeout"></a>delete timeout

Удаляет глобальное время ожидания, после чего служба HTTP.sys возвращает значения по умолчанию.

``` syntax
delete timeout [timeouttype=]{idleconnectiontimeout|headerwaittimeout}
 
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="_timeouttype___idleconnectiontimeout_headerwaittimeout_"></span><span id="_TIMEOUTTYPE___IDLECONNECTIONTIMEOUT_HEADERWAITTIMEOUT_"></span>**\[тимеауттипе = \] {idleconnectiontimeout \| хеадерваиттимеаут}**
</dt> <dd>

Указывает тип параметра времени ожидания.

</dd> </dl>

## <a name="examples"></a>Примеры

**delete timeout timeouttype=idleconnectiontimeout**

**delete timeout timeouttype=headerwaittimeout**

 

 





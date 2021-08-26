---
title: " в, String и out, строковый прототип"
description: 'В следующем прототипе функции используются два параметра: "\ in", "String \" и "\ out", "String \".'
ms.assetid: acb0ec4f-1846-4fa2-98c2-2081b52a8260
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 498d12c85130bba8d7d8dcddfc400e2a90fa2d0e2c3cb11c4a7d89696cfe9aa4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073624"
---
# <a name="in-string-and-out-string-prototype"></a>\[в, String \] и \[ out, строковый \] прототип

В следующем прототипе функции используются два параметра: \[ [**в**](/windows/desktop/Midl/in), [**строковый**](/windows/desktop/Midl/string) \] параметр и \[ параметр [**out**](/windows/desktop/Midl/out-idl), **строковый** \] .

``` syntax
void Analyze(
    [in, string]                       *pszInput,
    [out, string, size_is(STRSIZE)]    *pszOutput);
```

Первый параметр доступен только \[ [**в**](/windows/desktop/Midl/in) \] . Эта входная строка передается только с клиента на сервер. Сервер использует его в качестве основания для дальнейшей обработки. Строка не изменяется и не требуется повторно клиентом, поэтому она не должна возвращаться клиенту.

Второй параметр, представляющий ответ врача, является \[ только [**выходом**](/windows/desktop/Midl/out-idl) \] . Эта строка ответа передается клиенту только с сервера. Размер выделения предоставляется таким образом, чтобы заглушки сервера могли выделить память для него. Так как *псзаутпут* является \[ [**ссылочным**](/windows/desktop/Midl/ref) \] указателем, клиент должен иметь достаточно памяти, выделенной для строки перед вызовом. Строка ответа записывается в эту область памяти при возврате удаленной процедуры.

 

 
---
description: Следующее определение Винтернл. h является статическим адресом памяти активного сеанса консоли служб терминалов. идентификатор сеанса активной консоли не определен в версиях операционной системы Microsoft Windows, предшествующей Windows XP.
ms.assetid: f3022ab8-60ea-490b-a87d-cc1afc99d26f
title: Получение идентификатора активного сеанса консоли
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46f7b23669240f0cd109a48f454ee6f6329f6839221a1677e81b75712430cb42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002304"
---
# <a name="getting-the-active-console-session-id"></a>Получение идентификатора активного сеанса консоли

Следующее определение Винтернл. h является статическим адресом памяти активного сеанса консоли служб терминалов. идентификатор сеанса активной консоли не определен в версиях операционной системы Microsoft Windows, предшествующей Windows XP.

> [!Note]  
> Это определение может измениться в будущих выпусках Windows. Чтобы обеспечить правильную работу приложения в будущем, приложение должно вызвать [**втсжетактивеконсолесессионид**](/windows/win32/api/winbase/nf-winbase-wtsgetactiveconsolesessionid).

 

``` syntax
#define INTERNAL_TS_ACTIVE_CONSOLE_ID    
        (*((volatile ULONG*)(0x7ffe02d8)))
```

 

 

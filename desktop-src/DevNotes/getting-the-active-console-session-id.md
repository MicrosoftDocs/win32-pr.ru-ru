---
description: Следующее определение Винтернл. h является статическим адресом памяти активного сеанса консоли служб терминалов. Идентификатор сеанса активной консоли не определен в версиях операционной системы Microsoft Windows, предшествующих Windows XP.
ms.assetid: f3022ab8-60ea-490b-a87d-cc1afc99d26f
title: Получение идентификатора активного сеанса консоли
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 936db3f8038348864fc90fc55eeb4287a67c45d6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895765"
---
# <a name="getting-the-active-console-session-id"></a>Получение идентификатора активного сеанса консоли

Следующее определение Винтернл. h является статическим адресом памяти активного сеанса консоли служб терминалов. Идентификатор сеанса активной консоли не определен в версиях операционной системы Microsoft Windows, предшествующих Windows XP.

> [!Note]  
> Это определение может измениться в будущих выпусках Windows. Чтобы обеспечить правильную работу приложения в будущем, приложение должно вызвать [**втсжетактивеконсолесессионид**](/windows/win32/api/winbase/nf-winbase-wtsgetactiveconsolesessionid).

 

``` syntax
#define INTERNAL_TS_ACTIVE_CONSOLE_ID    
        (*((volatile ULONG*)(0x7ffe02d8)))
```

 

 

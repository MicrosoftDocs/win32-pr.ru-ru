---
title: Выбор последовательности протокола
description: Рекомендации по выбору последовательности протоколов предполагают использование нкакн \_ IP \_ TCP и нкалрпк, а не нкакн \_ NP, нкакн \_ SPX и нкадг \_ \.
ms.assetid: 4b81b534-f001-4522-bf63-044bf5f414f2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 732e00d46f1b471870447e228935a794db8d5dc5aa6486e3296b9936cd1be7cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118932227"
---
# <a name="choosing-a-protocol-sequence"></a>Выбор последовательности протокола

**Рекомендации:** При удаленном вызове используйте [**нкакн \_ IP \_ TCP**](/windows/desktop/Midl/ncacn-ip-tcp) . Используйте [**нкалрпк**](/windows/desktop/Midl/ncalrpc) для локальных вызовов. Не используйте [**нкакн \_ NP**](/windows/desktop/Midl/ncacn-np), [**нкакн \_ SPX**](/windows/desktop/Midl/ncacn-spx)или любую из последовательностей протокола **нкадг \_ \*** . они менее эффективны и имеют более низкий уровень возможностей.

 

 
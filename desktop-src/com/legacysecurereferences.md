---
title: легацисекуререференцес
description: Определяет, защищены ли вызовы AddRef/Release для приложений, которые не вызывают CoInitializeSecurity.
ms.assetid: 955b599b-1858-475a-95c4-a55038a28e69
keywords:
- COM-значение реестра Легацисекуререференцес
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2776bf3661013f1e622bbc2e1c553f2551c62808
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700586"
---
# <a name="legacysecurereferences"></a>легацисекуререференцес

Определяет  / , защищены ли вызовы **выпуска** AddRef для приложений, которые не вызывают [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).

## <a name="registry-entry"></a>Запись реестра

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   LegacySecureReferences = value
```

## <a name="remarks"></a>Комментарии

Это значение **reg \_ SZ** . Значение "Y" или "y" указывает, что **AddRef** и **Release** защищены. Если это значение реестра отсутствует или имеет значение, отличное от "Y" или "y", **AddRef** и **Release** не защищаются. Включение защиты ссылок снижает производительность удаленных вызовов.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Регистрация серверов COM](registering-com-servers.md)
</dt> <dt>

[Настройка безопасности на уровне процесса](setting-processwide-security.md)
</dt> </dl>

 

 





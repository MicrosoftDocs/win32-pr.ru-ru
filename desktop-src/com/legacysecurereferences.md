---
title: легацисекуререференцес
description: Определяет, защищены ли вызовы AddRef/Release для приложений, которые не вызывают CoInitializeSecurity.
ms.assetid: 955b599b-1858-475a-95c4-a55038a28e69
keywords:
- COM-значение реестра Легацисекуререференцес
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef3a4ab964d73fa4b194c734f28c23ff068239370088c090051464129b6caf14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736551"
---
# <a name="legacysecurereferences"></a>легацисекуререференцес

Определяет  / , защищены ли вызовы **выпуска** AddRef для приложений, которые не вызывают [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).

## <a name="registry-entry"></a>Запись реестра

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   LegacySecureReferences = value
```

## <a name="remarks"></a>Remarks

Это значение **reg \_ SZ** . Значение "Y" или "y" указывает, что **AddRef** и **Release** защищены. Если это значение реестра отсутствует или имеет значение, отличное от "Y" или "y", **AddRef** и **Release** не защищаются. Включение защиты ссылок снижает производительность удаленных вызовов.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Регистрация серверов COM](registering-com-servers.md)
</dt> <dt>

[Настройка безопасности на уровне процесса](setting-processwide-security.md)
</dt> </dl>

 

 





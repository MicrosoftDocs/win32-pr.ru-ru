---
title: легациаусентикатионлевел
description: Задает уровень проверки подлинности по умолчанию для приложений, которые не вызывают CoInitializeSecurity.
ms.assetid: e14d2203-c84e-46af-befd-d82ef1936c9d
keywords:
- COM-значение реестра Легациаусентикатионлевел
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2d87d808287418f635629e15324f2f517619be6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068624"
---
# <a name="legacyauthenticationlevel"></a>легациаусентикатионлевел

Задает уровень проверки подлинности по умолчанию для приложений, которые не вызывают [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).

> [!Caution]  
> Не рекомендуется изменять это значение, так как это повлияет на все серверные приложения COM, не устанавливающие собственный уровень безопасности на уровне процесса, и может препятствовать их правильной работе. Если вы изменяете это значение, чтобы оно влияло на параметры безопасности для конкретного приложения COM, вместо этого следует изменить параметры безопасности для этого конкретного COM-приложения. Дополнительные сведения о настройке безопасности на уровне процесса см. в разделе [Настройка безопасности на уровне процесса](setting-processwide-security.md).

 

## <a name="registry-entry"></a>Запись реестра

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   LegacyAuthenticationLevel = value
```

## <a name="remarks"></a>Комментарии

Это значение **\_ слова reg** , эквивалентное \_ \_ \_ константам уровня RPC C AUTHN.



| Значение | Константа                             |
|-------|--------------------------------------|
| 1     | \_уровень RPC \_ C \_ AUTHN \_ None           |
| 2     | \_подключение на уровне RPC C \_ AUTHN \_ \_        |
| 3     | \_ \_ \_ вызов уровня RPC C \_ AUTHN           |
| 4     | \_PKT на уровне RPC C \_ AUTHN \_ \_            |
| 5     | \_ \_ \_ \_ целостность PKT RPC C AUTHN Level \_ |
| 6     | \_Конфиденциальность RPC C \_ AUTHN \_ Level \_ PKT \_   |



 

Если это значение реестра отсутствует, уровень проверки подлинности по умолчанию, установленный системой, — 2 (RPC \_ C \_ AUTHN \_ Connect).

## <a name="related-topics"></a>См. также

<dl> <dt>

[**аусентикатионлевел**](authenticationlevel.md)
</dt> <dt>

[Регистрация серверов COM](registering-com-servers.md)
</dt> <dt>

[Настройка безопасности на уровне процесса](setting-processwide-security.md)
</dt> </dl>

 

 





---
title: легациаусентикатионлевел
description: Задает уровень проверки подлинности по умолчанию для приложений, которые не вызывают CoInitializeSecurity.
ms.assetid: e14d2203-c84e-46af-befd-d82ef1936c9d
keywords:
- COM-значение реестра Легациаусентикатионлевел
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae6be9f562a543e4750695ec2bf967b5a261209aae70d0bf91269bc2a074a9e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096954"
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

## <a name="remarks"></a>Remarks

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

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**аусентикатионлевел**](authenticationlevel.md)
</dt> <dt>

[Регистрация серверов COM](registering-com-servers.md)
</dt> <dt>

[Настройка безопасности на уровне процесса](setting-processwide-security.md)
</dt> </dl>

 

 





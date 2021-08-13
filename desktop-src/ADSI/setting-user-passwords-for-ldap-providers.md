---
title: Настройка и изменение паролей пользователей с помощью поставщика LDAP
description: Чтобы задать пароль пользователя, используйте метод IADsUser. SetPassword.
ms.assetid: da3d9861-dd04-406c-9356-db1e4ff0eebc
ms.tgt_platform: multiple
keywords:
- ADSI поставщика LDAP, объект User, установка паролей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efbbd0439a011575fbc9278dbe506d46db2210ce03d807ea74097499cb764b43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118690529"
---
# <a name="setting-and-changing-user-passwords-with-the-ldap-provider"></a>Настройка и изменение паролей пользователей с помощью поставщика LDAP

Чтобы задать пароль пользователя, используйте метод [**IADsUser. SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword) .

Поставщик LDAP для Active Directory использует один из трех процессов для задания пароля (сторонние каталоги LDAP, такие как iPlanet, не используют этот процесс проверки подлинности пароля). Метод может отличаться в зависимости от конфигурации сети. Методы задания пароля выполняются в следующем порядке:

-   Во-первых, поставщик LDAP пытается использовать LDAP через 128-разрядное подключение SSL. Чтобы протокол LDAP SSL успешно работал, на сервере LDAP должен быть установлен соответствующий сертификат проверки подлинности сервера, а клиенты, выполняющие код ADSI, должны доверять центру сертификации, выдавшей сертификаты. Как сервер, так и клиент должны поддерживать 128-разрядное шифрование.
-   Во-вторых, в случае неудачного подключения SSL поставщик LDAP пытается использовать Kerberos. в Windows 2000 Kerberos может не поддерживать проверку подлинности между лесами. Более поздние усовершенствования поддерживают проверку подлинности между лесами.
-   В-третьих, если Kerberos не удалось, поставщик LDAP пытается вызвать API [**нетусерсетинфо**](/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo) . В предыдущих выпусках ADSI назывался **нетусерсетинфо** в контексте безопасности, в котором выполнялся поток, а не в контексте безопасности, указанном в вызове [**иадсопендсобжект. опендсобжект**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) или [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject). В более поздних выпусках это было изменено, так что поставщик ADSI LDAP будет олицетворять пользователя, указанного в вызове **опендсобжект** при вызове **нетусерсетинфо**.

Чтобы изменить пароль пользователя, используйте метод [**IADsUser. ChangePassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-changepassword) . Как и [**SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword), этот метод может использовать несколько процессов для изменения пароля. Методы изменения пароля выполняются в следующем порядке:

-   Во-первых, поставщик LDAP пытается использовать LDAP через 128-разрядное подключение SSL.
-   Во-вторых, если не удалось выполнить подключение 128 SSL, поставщик LDAP пытается вызвать API [**нетусерчанжепассворд**](/windows/desktop/api/lmaccess/nf-lmaccess-netuserchangepassword) . Как и [**SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword), в более ранних выпусках поставщик LDAP ADSI олицетворяет учетные данные пользователя, переданные с помощью метода [**иадсопендсобжект. Опендсобжект**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) или функции [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) .

 

 
---
description: Объясняет, как изменить привилегии в токене с помощью функций AdjustTokenPrivileges и CreateRestrictedToken.
ms.assetid: b8e47d04-07c1-4d57-8209-6b0c397476e5
title: Изменение привилегий в токене
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a8b77d966acf90db101269b77a767550bcae3ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664410"
---
# <a name="changing-privileges-in-a-token"></a>Изменение привилегий в токене

Вы можете изменить привилегии в первичном или токене олицетворения двумя способами:

-   Включите или отключите привилегии с помощью функции [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) .
-   Ограничьте или удалите привилегии с помощью функции [**CreateRestrictedToken**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) .

[**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) не может добавлять или удалять привилегии из токена. Он может включать только существующие привилегии, которые в настоящее время отключены, или отключать существующие привилегии, которые в настоящее время включены. Примеры см. [в разделе Включение и отключение привилегий в C++](/windows/desktop/SecAuthZ/enabling-and-disabling-privileges-in-c--).

Чтобы назначить привилегии учетной записи пользователя, см. раздел [назначение привилегий учетной записи](assigning-privileges-to-an-account.md).

[**CreateRestrictedToken**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) обладает более широкими возможностями, как показано ниже.

-   Удаление привилегий. Обратите внимание, что удаление привилегий не так же, как и при ее отключении. После удаления привилегий из токена ее нельзя вернуть обратно.
-   Присоединение атрибута Deny-only к идентификаторам безопасности в токене. Это позволяет запретить доступ к определенному файлу для определенных групп или учетных записей, например для запрета доступа к группе Everyone. Дополнительные сведения о том, как ограничивать идентификаторы безопасности, см. [в разделе атрибуты SID в маркере доступа](/windows/desktop/SecAuthZ/sid-attributes-in-an-access-token).
-   Указание списка запрещенных идентификаторов безопасности в токене. Дополнительные сведения об ограничении идентификаторов безопасности см. в разделе [ограничения токенов](/windows/desktop/SecAuthZ/restricted-tokens).

 

 

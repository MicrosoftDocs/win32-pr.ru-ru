---
description: Объясняет, как изменить привилегии в токене с помощью функций AdjustTokenPrivileges и CreateRestrictedToken.
ms.assetid: b8e47d04-07c1-4d57-8209-6b0c397476e5
title: Изменение привилегий в токене
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c511ca66c5d4739057f5ea75cae589ee97e849f659002a612e7d22fd6be8eecb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119622754"
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

 

 
